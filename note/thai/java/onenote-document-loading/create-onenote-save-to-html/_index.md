---
date: 2025-12-02
description: เรียนรู้วิธีส่งออกแบบอักษรขณะบันทึก OneNote เป็น HTML ด้วย Aspose.Note
  for Java คู่มือนี้จะแสดงวิธีสร้าง OneNote อย่างโปรแกรมเมติกและฝังแบบอักษร, CSS และรูปภาพ
language: th
linktitle: How to Export Fonts When Saving OneNote as HTML – Java
second_title: Aspose.Note Java API
title: วิธีส่งออกฟอนต์เมื่อบันทึก OneNote เป็น HTML – Java
url: /java/onenote-document-loading/create-onenote-save-to-html/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# วิธีการส่งออกฟอนต์เมื่อบันทึก OneNote เป็น HTML – Java

## Introduction

ในบทเรียนนี้คุณจะได้เรียนรู้ **วิธีการส่งออกฟอนต์** เมื่อคุณ **บันทึก OneNote เป็น HTML** ด้วย Aspose.Note for Java เราจะอธิบายขั้นตอนการสร้างเอกสาร OneNote ด้วยโปรแกรม, การกำหนดค่าตัวเลือกการบันทึกเป็น HTML, และการฝังไฟล์ฟอนต์ที่จำเป็นเพื่อให้ HTML ที่ได้มีลักษณะเหมือนกับหน้า OneNote ดั้งเดิมอย่างแม่นยำ วิธีนี้เหมาะอย่างยิ่งเมื่อคุณต้องการรักษาความเที่ยงตรงของการแสดงผล OneNote ในรูปแบบที่เป็นมิตรต่อเว็บ

## Quick Answers
- **What library handles the export?** Aspose.Note for Java  
- **Can fonts be embedded in the HTML?** Yes – set `ExportFonts` to `ExportEmbedded`  
- **Do I need a license for production?** A valid Aspose.Note license is required for commercial use  
- **Which Java version is supported?** Java 8 or higher  
- **Is it possible to save resources to separate files?** Absolutely – configure `ResourceExportType` accordingly  

## What is “how to export fonts” in the context of OneNote HTML conversion?

เมื่อคุณแปลงสมุดบันทึก OneNote เป็น HTML รูปลักษณ์ของหน้าเว็บจะขึ้นอยู่กับ CSS, รูปภาพ, และโดยเฉพาะอย่างยิ่งฟอนต์ที่ใช้ในหน้าเดิม **การส่งออกฟอนต์** หมายถึงการฝังไฟล์ฟอนต์ (เช่น TTF) ลงในแพ็กเกจ HTML โดยตรง เพื่อให้เบราว์เซอร์สามารถแสดงข้อความได้เหมือนกับที่ปรากฏใน OneNote แม้ว่าผู้ใช้ปลายทางจะไม่ได้ติดตั้งฟอนต์เหล่านั้นไว้ในเครื่อง

## Why create OneNote programmatically and save it as HTML?

- **Automation:** สร้างรายงาน, เอกสาร, หรือบทความฐานความรู้จาก OneNote โดยอัตโนมัติโดยไม่ต้องคัดลอก‑วางด้วยมือ  
- **Consistency:** รักษาเลย์เอาต์, สไตล์, และฟอนต์ที่กำหนดเองให้คงที่บนอุปกรณ์ทุกเครื่อง  
- **Portability:** HTML สามารถดูได้ทั่วโลก—ไม่ต้องใช้ไคลเอนต์ OneNote  

## Prerequisites

1. Java Development Kit (JDK) 8 หรือใหม่กว่า  
2. ไลบรารี Aspose.Note for Java – ดาวน์โหลดจาก [here](https://releases.aspose.com/note/java/)  
3. ไฟล์ OneNote ตัวอย่าง (`.one`) เพื่อโหลด, หรือคุณสามารถสร้างไฟล์ใหม่ด้วยโปรแกรมได้  

## Import Packages

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

## How to Export Fonts While Saving OneNote as HTML?

Below is a step‑by‑step guide that shows you **how to export fonts** and other resources.

### Step 1: Create a OneNote document programmatically  

```java
Document document = new Document("Path_to_your_sample_one_file");
```

บรรทัดนี้โหลดไฟล์ `.one` ที่มีอยู่ หากคุณต้องการ **สร้าง OneNote ด้วยโปรแกรม** คุณสามารถสร้างอ็อบเจกต์ `Document` ใหม่และเพิ่มส่วน/หน้าโดยใช้ API (ไม่ได้แสดงในที่นี้เพื่อให้โฟกัสที่การส่งออกฟอนต์)

### Step 2: Save to a memory stream with embedded fonts  

```java
HtmlSaveOptions options = new HtmlSaveOptions();
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);
options.setFontFaceTypes(FontFaceType.Ttf);

ByteArrayOutputStream outputStream = new ByteArrayOutputStream();
document.save(outputStream, options);
```

- `setExportFonts(ResourceExportType.ExportEmbedded)` บอก Aspose.Note ให้ **ส่งออกฟอนต์** โดยตรงเข้าไปในแพ็กเกจ HTML  
- `setFontFaceTypes(FontFaceType.Ttf)` ทำให้ใช้ฟอนต์ TrueType ซึ่งรองรับโดยเบราว์เซอร์ส่วนใหญ่  

### Step 3: Save as HTML with separate resource files (still exporting fonts)  

```java
HtmlSaveOptions options = new HtmlSaveOptions();
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);

document.save("output_directory/document.html", options);
```

แม้ว่า CSS และรูปภาพจะถูกฝังไว้แล้ว คุณก็สามารถเปลี่ยน `ResourceExportType` เป็น `ExportExternal` หากต้องการไฟล์แยกสำหรับการแคชที่ง่ายขึ้น ส่วนสำคัญ—**การส่งออกฟอนต์**—ยังคงไม่เปลี่ยนแปลง

### Step 4: Use callbacks to control where each resource is stored  

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

คลาส `UserSavingCallbacks` (คุณต้องทำการ implement `ICssSavingCallback`, `IImageSavingCallback`, และ `IFontSavingCallback`) ให้คุณควบคุมโครงสร้างโฟลเดอร์ได้เต็มที่ ทำให้คุณสามารถเก็บฟอนต์ไว้ในไดเรกทอรี `fonts` แยกต่างหากในขณะที่ **ส่งออกฟอนต์** อย่างถูกต้อง

## Common Issues & Tips

- **Missing fonts in the output:** ตรวจสอบว่าได้ตั้งค่า `setExportFonts(ResourceExportType.ExportEmbedded)` แล้วและไฟล์ OneNote ต้นฉบับจริง ๆ มีการใช้ฟอนต์ที่ฝังอยู่  
- **Large HTML files:** การฝังฟอนต์อาจทำให้ไฟล์ขนาดใหญ่ หากกังวลเรื่องแบนด์วิธ ให้เปลี่ยน `ExportFonts` เป็น `ExportExternal` แล้วโฮสต์ฟอนต์บน CDN  
- **Callback implementation errors:** ให้แน่ใจว่าคลาส callback ของคุณเขียนสตรีมและปิดทรัพยากรอย่างถูกต้องเพื่อหลีกเลี่ยงไฟล์เสีย  

## Frequently Asked Questions

**Q: Can I convert multiple OneNote documents to HTML in one go?**  
A: Yes, loop through each `Document` instance and apply the same `HtmlSaveOptions`.  

**Q: Does Aspose.Note for Java support other output formats besides HTML?**  
A: Absolutely. You can export to PDF, DOCX, PNG, JPEG, and more using the appropriate save options.  

**Q: Is there a trial version available for Aspose.Note for Java?**  
A: Yes, download a free trial from [here](https://releases.aspose.com/).  

**Q: Where can I get support for Aspose.Note for Java?**  
A: Visit the [Aspose.Note forum](https://forum.aspose.com/c/note/28) for community and official assistance.  

**Q: How can I purchase a license for Aspose.Note for Java?**  
A: Licenses are available at the [Aspose website](https://purchase.aspose.com/buy).  

## Conclusion

You now know **how to export fonts** while you **save OneNote as HTML** using Aspose.Note for Java. By configuring `HtmlSaveOptions` and optionally using callbacks, you can preserve the exact look of your OneNote pages—including custom fonts—when delivering them on the web. Feel free to experiment with different `ResourceExportType` settings to suit your project’s performance and storage requirements.

---

**Last Updated:** 2025-12-02  
**Tested With:** Aspose.Note for Java 24.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
