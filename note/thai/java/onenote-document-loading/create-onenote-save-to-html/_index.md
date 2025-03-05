---
title: สร้างเอกสาร OneNote และบันทึกเป็น HTML - Java
linktitle: สร้างเอกสาร OneNote และบันทึกเป็น HTML - Java
second_title: Aspose.Note Java API
description: เรียนรู้วิธีการสร้างและบันทึกเอกสาร OneNote เป็น HTML โดยใช้ Aspose.Note สำหรับ Java ผสานรวมเข้ากับแอปพลิเคชัน Java สำหรับการจัดการไฟล์ OneNote แบบเป็นโปรแกรม

type: docs
weight: 18
url: /th/java/onenote-document-loading/create-onenote-save-to-html/
---
## การแนะนำ

Aspose.Note สำหรับ Java เป็นไลบรารีอันทรงพลังที่ช่วยให้นักพัฒนาสามารถทำงานกับไฟล์ Microsoft OneNote โดยทางโปรแกรม ในบทช่วยสอนนี้ เราจะสำรวจวิธีสร้างเอกสาร OneNote และบันทึกเป็นรูปแบบ HTML โดยใช้ Aspose.Note สำหรับ Java

## ข้อกำหนดเบื้องต้น

ก่อนที่เราจะเริ่ม ตรวจสอบให้แน่ใจว่าคุณมีสิ่งต่อไปนี้:

1. ติดตั้ง Java Development Kit (JDK) บนระบบของคุณ
2.  Aspose.Note สำหรับไลบรารี Java คุณสามารถดาวน์โหลดได้จาก[ที่นี่](https://releases.aspose.com/note/java/).
3. ความรู้พื้นฐานเกี่ยวกับการเขียนโปรแกรม Java

## แพ็คเกจนำเข้า

ขั้นแรก นำเข้าแพ็คเกจที่จำเป็นไปยังโปรเจ็กต์ Java ของคุณ:

```java
import java.io.ByteArrayOutputStream;
import java.io.File;
import java.io.FileOutputStream;
import java.io.IOException;
import java.io.OutputStream;
import java.io.OutputStreamWriter;
import java.nio.file.Paths;
import com.aspose.note.CssSavingArgs;
import com.aspose.note.Document;
import com.aspose.note.FontFaceType;
import com.aspose.note.FontSavingArgs;
import com.aspose.note.HtmlSaveOptions;
import com.aspose.note.ICssSavingCallback;
import com.aspose.note.IFontSavingCallback;
import com.aspose.note.IImageSavingCallback;
import com.aspose.note.ImageSavingArgs;
import com.aspose.note.ResourceExportType;
```

## ขั้นตอนที่ 1: สร้างวัตถุเอกสาร OneNote

```java
Document document = new Document("Path_to_your_sample_one_file");
```

 รหัสนี้เริ่มต้นก`Document` วัตถุโดยการโหลดไฟล์ OneNote ตัวอย่าง

## ขั้นตอนที่ 2: บันทึกเป็น HTML ไปยัง Memory Stream

```java
HtmlSaveOptions options = new HtmlSaveOptions();
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);
options.setFontFaceTypes(FontFaceType.Ttf);

ByteArrayOutputStream outputStream = new ByteArrayOutputStream();
document.save(outputStream, options);
```

ที่นี่ เราตั้งค่าตัวเลือกการบันทึก HTML และบันทึกเอกสารลงในสตรีมหน่วยความจำ

## ขั้นตอนที่ 3: บันทึกเป็น HTML พร้อมทรัพยากรในไฟล์แยก

```java
HtmlSaveOptions options = new HtmlSaveOptions();
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);

document.save("output_directory/document.html", options);
```

ขั้นตอนนี้จะบันทึกเอกสารเป็น HTML พร้อมด้วยทรัพยากร เช่น CSS, แบบอักษร และรูปภาพในไฟล์แยกกัน

## ขั้นตอนที่ 4: บันทึกเป็น HTML ไปยัง Memory Stream พร้อม Callbacks เพื่อบันทึกทรัพยากร

```java
Document document = new Document("Path_to_your_sample_one_file");

UserSavingCallbacks savingCallbacks = new UserSavingCallbacks();
savingCallbacks.setRootFolder("documentFolder");
savingCallbacks.setCssFolder("css");
savingCallbacks.setKeepCssStreamOpened(true);
savingCallbacks.setImagesFolder("images");
savingCallbacks.setFontsFolder("fonts");

HtmlSaveOptions options = new HtmlSaveOptions();
options.setFontFaceTypes(FontFaceType.Ttf);
options.setCssSavingCallback(savingCallbacks);
options.setImageSavingCallback(savingCallbacks);
options.setFontSavingCallback(savingCallbacks);
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);

File dir = new File(savingCallbacks.getRootFolder());
if (!dir.exists()) {
    dir.mkdir();
}

document.save(Paths.get(savingCallbacks.getRootFolder(), "document.html").toString(), options);
```

ที่นี่ เราบันทึกเอกสารเป็น HTML ลงในสตรีมหน่วยความจำโดยใช้การโทรกลับเพื่อจัดการการประหยัดทรัพยากร

## บทสรุป

ยินดีด้วย! คุณได้เรียนรู้วิธีสร้างเอกสาร OneNote และบันทึกเป็นรูปแบบ HTML โดยใช้ Aspose.Note สำหรับ Java ตอนนี้คุณสามารถรวมฟังก์ชันการทำงานนี้เข้ากับแอปพลิเคชัน Java ของคุณเพื่อทำงานกับไฟล์ OneNote โดยทางโปรแกรมได้

## คำถามที่พบบ่อย

### คำถามที่ 1: ฉันสามารถแปลงเอกสาร OneNote หลายฉบับเป็น HTML ได้ในคราวเดียวหรือไม่

A1: ได้ คุณสามารถวนซ้ำเอกสารหลายชุดและใช้กระบวนการบันทึกซ้ำได้

### คำถามที่ 2: Aspose.Note สำหรับ Java รองรับรูปแบบเอาต์พุตอื่นๆ นอกเหนือจาก HTML หรือไม่

ตอบ 2: ใช่ Aspose.Note สำหรับ Java รองรับรูปแบบเอาต์พุตที่หลากหลาย รวมถึง PDF, DOCX และรูปแบบรูปภาพ

### คำถามที่ 3: Aspose.Note สำหรับ Java มีเวอร์ชันทดลองใช้งานหรือไม่

A3: ได้ คุณสามารถดาวน์โหลดเวอร์ชันทดลองใช้ฟรีได้จาก[ที่นี่](https://releases.aspose.com/).

### คำถามที่ 4: ฉันจะรับการสนับสนุนสำหรับ Aspose.Note สำหรับ Java ได้ที่ไหน

 A4: คุณสามารถรับการสนับสนุนจาก[ฟอรั่ม Aspose.Note](https://forum.aspose.com/c/note/28).

### คำถามที่ 5: ฉันจะซื้อใบอนุญาตสำหรับ Aspose.Note สำหรับ Java ได้อย่างไร

 A5: คุณสามารถซื้อใบอนุญาตได้จาก[เว็บไซต์กำหนด](https://purchase.aspose.com/buy).