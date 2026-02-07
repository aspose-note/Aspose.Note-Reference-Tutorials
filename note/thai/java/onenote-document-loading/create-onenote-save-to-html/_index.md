---
date: 2026-02-07
description: เรียนรู้วิธีส่งออกแบบอักษรขณะบันทึก OneNote เป็น HTML ด้วย Aspose.Note
  for Java คู่มือนี้จะแสดงวิธีสร้าง OneNote ด้วยโปรแกรมและฝังแบบอักษร, CSS และรูปภาพ
linktitle: How to Export Fonts When Saving OneNote as HTML – Java
second_title: Aspose.Note Java API
title: วิธีส่งออกฟอนต์เมื่อบันทึก OneNote เป็น HTML – Java
url: /th/java/onenote-document-loading/create-onenote-save-to-html/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# วิธีการส่งออกฟอนต์เมื่อบันทึก OneNote เป็น HTML – Java

## บทนำ

ในบทเรียนนี้คุณจะได้ค้นพบ **วิธีการส่งออกฟอนต์** เมื่อคุณ **บันทึก OneNote เป็น HTML** โดยใช้ Aspose.Note for Java เราจะอธิบายขั้นตอนการสร้างเอกสาร OneNote ด้วยโปรแกรม, การกำหนดค่าตัวเลือกการบันทึก HTML, และการฝังไฟล์ฟอนต์ที่จำเป็นเพื่อให้ HTML ที่ได้ดูเหมือนกับหน้าของ OneNote ต้นฉบับอย่างแม่นยำ วิธีนี้เหมาะอย่างยิ่งเมื่อคุณต้องการรักษาความเที่ยงตรงของการแสดงผลของเนื้อหา OneNote ในรูปแบบที่เป็นมิตรกับเว็บ

## คำตอบสั้น
- **ไลบรารีที่จัดการการส่งออกคืออะไร?** Aspose.Note for Java  
- **สามารถฝังฟอนต์ใน HTML ได้หรือไม่?** ใช่ – ตั้งค่า `ExportFonts` เป็น `ExportEmbedded`  
- **ฉันต้องการใบอนุญาตสำหรับการใช้งานจริงหรือไม่?** จำเป็นต้องมีใบอนุญาต Aspose.Note ที่ถูกต้องสำหรับการใช้เชิงพาณิชย์  
- **เวอร์ชัน Java ที่รองรับคืออะไร?** Java 8 หรือสูงกว่า  
- **สามารถบันทึกทรัพยากรเป็นไฟล์แยกได้หรือไม่?** แน่นอน – ตั้งค่า `ResourceExportType` ตามที่ต้องการ  

## “วิธีการส่งออกฟอนต์” คืออะไรในบริบทของการแปลง OneNote เป็น HTML?

เมื่อคุณแปลงสมุดบันทึก OneNote เป็น HTML รูปลักษณ์ของหน้าจะขึ้นอยู่กับ CSS, รูปภาพ, และโดยเฉพาะฟอนต์ที่ใช้ในหน้าต้นฉบับ **การส่งออกฟอนต์** หมายถึงการฝังไฟล์ฟอนต์ (เช่น TTF) ลงในแพคเกจ HTML โดยตรง เพื่อให้เบราว์เซอร์สามารถแสดงข้อความได้เหมือนกับที่ปรากฏใน OneNote แม้ว่าผู้ใช้ปลายทางจะไม่ได้ติดตั้งฟอนต์เหล่านั้นบนเครื่องของตน

## ทำไมต้องสร้าง OneNote ด้วยโปรแกรมและบันทึกเป็น HTML?

- **Automation:** สร้างรายงาน, เอกสาร, หรือบทความฐานความรู้จาก OneNote โดยไม่ต้องคัดลอก‑วางด้วยมือ.  
- **Consistency:** รักษาเลย์เอาต์, สไตล์, และฟอนต์ที่กำหนดเองให้คงที่บนอุปกรณ์ต่าง ๆ.  
- **Portability:** HTML สามารถดูได้ทุกที่—ไม่ต้องใช้ไคลเอนต์ OneNote.  

## ข้อกำหนดเบื้องต้น

1. ติดตั้ง Java Development Kit (JDK) 8 หรือใหม่กว่า  
2. ไลบรารี Aspose.Note for Java – ดาวน์โหลดจาก [here](https://releases.aspose.com/note/java/).  
3. ไฟล์ OneNote ตัวอย่าง (`.one`) เพื่อโหลด, หรือคุณสามารถสร้างไฟล์ใหม่ด้วยโปรแกรมได้  

## นำเข้าแพ็กเกจ

First, import the required classes into your Java project:

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

## วิธีการส่งออกฟอนต์ขณะบันทึก OneNote เป็น HTML?

ต่อไปนี้เป็นคู่มือขั้นตอนที่แสดงให้คุณเห็น **วิธีการส่งออกฟอนต์** และทรัพยากรอื่น ๆ

### ขั้นตอนที่ 1: สร้างเอกสาร OneNote ด้วยโปรแกรม  

```java
Document document = new Document("Path_to_your_sample_one_file");
```

บรรทัดนี้โหลดไฟล์ `.one` ที่มีอยู่ หากคุณต้องการ **สร้าง OneNote ด้วยโปรแกรม**, คุณสามารถสร้างอ็อบเจกต์ `Document` ใหม่และเพิ่มส่วน/หน้าโดยใช้ API (ไม่ได้แสดงที่นี่เพื่อให้โฟกัสที่การส่งออกฟอนต์)

### ขั้นตอนที่ 2: บันทึกลงสตรีมหน่วยความจำพร้อมฝังฟอนต์  

```java
HtmlSaveOptions options = new HtmlSaveOptions();
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);
options.setFontFaceTypes(FontFaceType.Ttf);

ByteArrayOutputStream outputStream = new ByteArrayOutputStream();
document.save(outputStream, options);
```

- `setExportFonts(ResourceExportType.ExportEmbedded)` บอก Aspose.Note ให้ **ส่งออกฟอนต์** โดยตรงลงในแพคเกจ HTML.  
- `setFontFaceTypes(FontFaceType.Ttf)` ทำให้แน่ใจว่าใช้ฟอนต์ TrueType ซึ่งรองรับโดยเบราว์เซอร์หลายประเภท.  

### ขั้นตอนที่ 3: บันทึกเป็น HTML พร้อมไฟล์ทรัพยากรแยก (ยังคงส่งออกฟอนต์)  

```java
HtmlSaveOptions options = new HtmlSaveOptions();
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);

document.save("output_directory/document.html", options);
```

แม้ว่า CSS และรูปภาพจะถูกฝังอยู่แล้ว คุณสามารถเปลี่ยนค่า `ResourceExportType` เป็น `ExportExternal` หากต้องการไฟล์แยกเพื่อการแคชที่ง่ายขึ้น ส่วนสำคัญ—**การส่งออกฟอนต์**—ยังคงเหมือนเดิม

### ขั้นตอนที่ 4: ใช้ callback เพื่อควบคุมตำแหน่งการจัดเก็บของแต่ละทรัพยากร  

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

คลาส `UserSavingCallbacks` (คุณต้องทำการ implement `ICssSavingCallback`, `IImageSavingCallback`, และ `IFontSavingCallback`) ให้คุณควบคุมโครงสร้างโฟลเดอร์ได้อย่างเต็มที่ ทำให้คุณสามารถเก็บฟอนต์ในไดเรกทอรี `fonts` แยกเฉพาะในขณะที่ยัง **ส่งออกฟอนต์** อย่างถูกต้อง

## วิธีการฝังฟอนต์กำหนดเองเมื่อแปลง OneNote เป็น HTML

การฝังฟอนต์กำหนดเองรับประกันว่าการแสดงผล HTML จะตรงกับเลย์เอาต์ของ OneNote ต้นฉบับ แม้บนอุปกรณ์ที่ไม่ได้ติดตั้งฟอนต์เหล่านั้น โดยใช้ `ExportEmbedded` ร่วมกับ `FontFaceType.Ttf` ไฟล์ TrueType จะถูกเข้ารหัส base‑64 และแทรกโดยตรงลงใน CSS ที่สร้างขึ้น ทำให้ไม่ต้องโฮสต์ฟอนต์ภายนอก

## การใช้ ResourceExportType เพื่อควบคุมการส่งออกทรัพยากร

`ResourceExportType` ให้คุณเลือกได้ว่าต้องการเก็บ CSS, รูปภาพ, และฟอนต์ **ภายใน**ไฟล์ HTML (`ExportEmbedded`) หรือบันทึกเป็นไฟล์ **ภายนอก** (`ExportExternal`) เลือก `ExportEmbedded` หากต้องการโซลูชันไฟล์เดียว หรือ `ExportExternal` หากต้องการใช้ประโยชน์จากการแคชของเบราว์เซอร์สำหรับทรัพยากรขนาดใหญ่

## การสร้าง OneNote ด้วยโปรแกรมเพื่อส่งออกเป็น HTML

หากคุณเริ่มจากศูนย์ คุณสามารถสร้างเอกสาร OneNote ทั้งหมดด้วยโค้ด, เพิ่มส่วน, หน้า, และข้อความรูปแบบ rich text, จากนั้นใช้ `HtmlSaveOptions` เดียวกับที่แสดงด้านบน นี่จะให้การทำงานอัตโนมัติจากต้นจนจบ: ตั้งแต่การสร้างข้อมูลจนถึงผลลัพธ์ HTML ที่มีสไตล์เต็มรูปแบบพร้อมฝังฟอนต์กำหนดเอง

## ปัญหาที่พบบ่อยและเคล็ดลับ

- **ฟอนต์หายในผลลัพธ์:** ตรวจสอบว่าได้ตั้งค่า `setExportFonts(ResourceExportType.ExportEmbedded)` แล้วและไฟล์ OneNote ต้นทางจริง ๆ ใช้ฟอนต์ที่ฝังอยู่  
- **ไฟล์ HTML ขนาดใหญ่:** การฝังฟอนต์อาจทำให้ขนาดเพิ่มขึ้น หากกังวลเรื่องแบนด์วิธ ให้เปลี่ยน `ExportFonts` เป็น `ExportExternal` และโฮสต์ฟอนต์บน CDN  
- **ข้อผิดพลาดในการ implement callback:** ตรวจสอบให้แน่ใจว่าคลาส callback ของคุณเขียนสตรีมและปิดทรัพยากรอย่างถูกต้องเพื่อหลีกเลี่ยงไฟล์เสียหาย  

## คำถามที่พบบ่อย

**ถาม: ฉันสามารถแปลงหลายเอกสาร OneNote เป็น HTML พร้อมกันได้หรือไม่?**  
ตอบ: ได้, ให้วนลูปผ่านแต่ละอินสแตนซ์ `Document` และใช้ `HtmlSaveOptions` เดียวกัน  

**ถาม: Aspose.Note for Java รองรับรูปแบบผลลัพธ์อื่น ๆ นอกจาก HTML หรือไม่?**  
ตอบ: แน่นอน. คุณสามารถส่งออกเป็น PDF, DOCX, PNG, JPEG, และอื่น ๆ โดยใช้ตัวเลือกการบันทึกที่เหมาะสม  

**ถาม: มีเวอร์ชันทดลองสำหรับ Aspose.Note for Java หรือไม่?**  
ตอบ: มี, ดาวน์โหลดเวอร์ชันทดลองฟรีจาก [here](https://releases.aspose.com/).  

**ถาม: ฉันจะหาแหล่งสนับสนุนสำหรับ Aspose.Note for Java ได้จากที่ไหน?**  
ตอบ: เยี่ยมชม [Aspose.Note forum](https://forum.aspose.com/c/note/28) เพื่อรับความช่วยเหลือจากชุมชนและทีมอย่างเป็นทางการ.  

**ถาม: ฉันจะซื้อใบอนุญาตสำหรับ Aspose.Note for Java ได้อย่างไร?**  
ตอบ: สามารถซื้อใบอนุญาตได้ที่ [Aspose website](https://purchase.aspose.com/buy).  

## สรุป

ตอนนี้คุณรู้แล้วว่า **วิธีการส่งออกฟอนต์** ขณะ **บันทึก OneNote เป็น HTML** ด้วย Aspose.Note for Java โดยการกำหนดค่า `HtmlSaveOptions` และอาจใช้ callback คุณสามารถรักษลักษณะการแสดงผลที่ตรงกับหน้า OneNote ของคุณ—including ฟอนต์กำหนดเอง—เมื่อเผยแพร่บนเว็บ อย่าลังเลที่จะทดลองตั้งค่า `ResourceExportType` ต่าง ๆ เพื่อให้เหมาะกับประสิทธิภาพและความต้องการการจัดเก็บของโครงการของคุณ

---

**อัปเดตล่าสุด:** 2026-02-07  
**ทดสอบกับ:** Aspose.Note for Java 24.12  
**ผู้เขียน:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}