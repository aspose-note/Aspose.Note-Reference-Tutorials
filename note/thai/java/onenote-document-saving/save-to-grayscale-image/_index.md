---
date: 2025-12-17
description: เรียนรู้วิธีการส่งออก OneNote โดยบันทึกเอกสารเป็นภาพ PNG แบบระดับสีเทาโดยใช้
  Aspose.Note สำหรับ Java รวมขั้นตอนการโหลดเอกสาร OneNote และสร้างภาพระดับสีเทา
linktitle: How to Export OneNote as Grayscale Image – Aspose.Note
second_title: Aspose.Note Java API
title: วิธีส่งออก OneNote เป็นภาพระดับสีเทา – Aspose.Note
url: /th/java/onenote-document-saving/save-to-grayscale-image/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# บันทึกเป็นภาพระดับสีเทาใน OneNote - Aspose.Note

## บทนำ

ในบทแนะนำนี้ เราจะแสดงให้คุณเห็น **วิธีการส่งออก onenote** โดยการบันทึกเอกสารเป็นภาพระดับสีเทาโดยใช้ Aspose.Note สำหรับ Java. ภาพระดับสีเทาเป็นรูปภาพโมโนโครมที่มีเฉพาะเฉดสีเทา ซึ่งมีประโยชน์สำหรับการพิมพ์, การเก็บถาวร, หรือการลดขนาดไฟล์. เราจะอธิบายขั้นตอนการโหลดเอกสาร OneNote, การกำหนดค่าตัวเลือกการบันทึกเพื่อ **สร้างภาพระดับสีเทา**, และสุดท้าย **บันทึกเอกสารเป็น PNG**.

## คำตอบสั้น
- **What does “how to export onenote” mean?** It refers to converting a OneNote file into another format, such as an image, programmatically.  
- **Which format is best for grayscale output?** PNG works well because it preserves loss‑less quality and supports grayscale color mode.  
- **Do I need a license?** A valid Aspose.Note license is required for production use; a temporary trial license is available for testing.  
- **What Java version is required?** Java 8 or higher is recommended.  
- **Can I change the image size?** Yes, you can adjust the `ImageSaveOptions` properties like `Resolution` or `PageSize` before saving.

## “how to export onenote” คืออะไร?
Exporting OneNote means programmatically converting a OneNote `.one` file into another representation—such as PDF, HTML, or an image. In this guide we focus on exporting to a **grayscale PNG** image, which is a common requirement for documentation or printing workflows.

## ทำไมต้องส่งออก OneNote เป็นภาพระดับสีเทา?
- **Reduced file size** – Grayscale PNGs are typically smaller than full‑color images.  
- **Better readability** – For printed reports, grayscale often provides clearer contrast.  
- **Compatibility** – PNG is widely supported across browsers, editors, and mobile devices.  

## ข้อกำหนดเบื้องต้น

Before we begin, ensure you have the following:

1. Java Development Kit (JDK) installed on your system.  
2. Aspose.Note for Java library. You can download it from [here](https://releases.aspose.com/note/java/).  
3. Basic understanding of Java programming.  

## นำเข้าแพ็กเกจ

To get started, import the necessary packages:

```java
import com.aspose.note.ColorMode;
import com.aspose.note.Document;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.SaveFormat;
import java.io.IOException;
```

## ขั้นตอนที่ 1: โหลดเอกสาร OneNote

First, **load onenote document** into Aspose.Note. Replace `"Your Document Directory"` with the path to your local folder and `"Aspose.one"` with the name of your OneNote file.

```java
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Aspose.one");
```

## ขั้นตอนที่ 2: กำหนดเส้นทางและตัวเลือกการส่งออก

Define the output path for the grayscale image and specify the saving options. We'll set the `ColorMode` to `GrayScale` and use the **save document as png** format.

```java
dataDir = dataDir + "SaveAsGrayscaleImage_out.png";
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);
options.setColorMode(ColorMode.GrayScale);
```

## ขั้นตอนที่ 3: บันทึกเอกสาร

Finally, save the document as a grayscale PNG image using the configured options.

```java
oneFile.save(dataDir, options);
```

## ปัญหาที่พบบ่อยและวิธีแก้ไข
- **FileNotFoundException** – Verify that `dataDir` points to the correct folder and that the `.one` file exists.  
- **LicenseException** – Ensure you have applied a valid Aspose.Note license before calling `save`.  
- **Low‑resolution output** – Adjust `options.setResolution(300)` to increase DPI if needed.

## คำถามที่พบบ่อย

**Q1: Can I save the grayscale image in a different format?**  
A1: Yes, simply change the `SaveFormat` parameter in the `ImageSaveOptions` constructor to `Jpeg`, `Bmp`, etc.

**Q2: Is Aspose.Note compatible with all versions of OneNote documents?**  
A2: Aspose.Note supports Microsoft OneNote 2010 and later versions.

**Q3: Does Aspose.Note require a license to use?**  
A3: A valid license is required for production use, but a temporary trial license can be obtained for evaluation.

**Q4: Can I manipulate other aspects of the document before saving it as an image?**  
A4: Absolutely! Aspose.Note provides a comprehensive API for editing sections, pages, and content before export.

**Q5: Where can I find support if I encounter issues?**  
A5: You can find support on the Aspose.Note forum [here](https://forum.aspose.com/c/note/28).

## สรุป

You've now learned **how to export onenote** by loading a OneNote file, configuring the save options to **create a grayscale image**, and **saving the document as PNG**. This technique is handy for generating lightweight, print‑ready visuals from OneNote notebooks. Feel free to experiment with other `ColorMode` settings or image formats to fit your project's needs.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**อัปเดตล่าสุด:** 2025-12-17  
**ทดสอบด้วย:** Aspose.Note 24.12 for Java  
**ผู้เขียน:** Aspose  

---