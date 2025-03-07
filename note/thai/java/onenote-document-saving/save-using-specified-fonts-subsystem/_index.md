---
title: บันทึกโดยใช้ระบบย่อยแบบอักษรที่ระบุใน OneNote
linktitle: บันทึกโดยใช้ระบบย่อยแบบอักษรที่ระบุใน OneNote
second_title: Aspose.Note Java API
description: เรียนรู้วิธีบันทึกเอกสาร OneNote โดยใช้ระบบย่อยแบบอักษรที่ระบุใน Java ด้วย Aspose.Note รับประกันการแสดงแบบอักษรที่สอดคล้องกันบนแพลตฟอร์มต่างๆ ได้อย่างง่ายดาย
weight: 22
url: /th/java/onenote-document-saving/save-using-specified-fonts-subsystem/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# บันทึกโดยใช้ระบบย่อยแบบอักษรที่ระบุใน OneNote

## การแนะนำ

Aspose.Note for Java มอบความสามารถที่แข็งแกร่งสำหรับการทำงานกับเอกสาร OneNote ข้อกำหนดทั่วไปประการหนึ่งเมื่อทำงานกับเอกสารดังกล่าวคือต้องแน่ใจว่าแบบอักษรได้รับการดูแลอย่างเหมาะสม โดยเฉพาะอย่างยิ่งหากต้องการส่งออกหรือบันทึกเอกสารในรูปแบบที่แตกต่างกัน เช่น PDF บทช่วยสอนนี้จะแนะนำคุณตลอดขั้นตอนการบันทึกเอกสาร OneNote ในขณะที่ระบุระบบย่อยแบบอักษร เพื่อให้มั่นใจว่าการแสดงข้อความบนแพลตฟอร์มต่างๆ จะสอดคล้องและแม่นยำ

## ข้อกำหนดเบื้องต้น

ก่อนที่เราจะเจาะลึกบทช่วยสอน ตรวจสอบให้แน่ใจว่าคุณได้ตั้งค่าข้อกำหนดเบื้องต้นต่อไปนี้:

### 1. ชุดพัฒนาจาวา (JDK)

 ตรวจสอบให้แน่ใจว่าคุณได้ติดตั้ง Java Development Kit (JDK) บนระบบของคุณ คุณสามารถดาวน์โหลดได้จาก[ที่นี่](https://www.oracle.com/java/technologies/javase-jdk15-downloads.html) ถ้าคุณยังไม่ได้

### 2. Aspose.Note สำหรับไลบรารี Java

 ดาวน์โหลดและตั้งค่า Aspose.Note สำหรับไลบรารี Java คุณสามารถดาวน์โหลดได้จาก[เว็บไซต์](https://releases.aspose.com/note/java/).

## แพ็คเกจนำเข้า

ตรวจสอบให้แน่ใจว่าได้นำเข้าแพ็คเกจที่จำเป็นในโปรเจ็กต์ Java ของคุณ:

```java
import com.aspose.note.Document;
import com.aspose.note.PdfSaveOptions;
import com.aspose.note.fonts.DocumentFontsSubsystem;
import java.io.FileInputStream;
import java.io.IOException;
import java.io.InputStream;
import java.nio.file.Paths;
```

ตอนนี้เรามาแบ่งแต่ละตัวอย่างออกเป็นหลายขั้นตอนเพื่อทำความเข้าใจกระบวนการให้ดีขึ้น

## ขั้นตอนที่ 1: บันทึกโดยใช้ระบบย่อยแบบอักษรของเอกสารด้วยชื่อแบบอักษรเริ่มต้น

ขั้นตอนนี้สาธิตวิธีการบันทึกเอกสารในรูปแบบ PDF โดยใช้ชื่อแบบอักษรเริ่มต้นที่ระบุ

```java
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontName() throws IOException
{
    // โหลดเอกสารลงใน Aspose.Note
    Document oneFile = new Document("missing-font.one");

    // ระบุแบบอักษรเริ่มต้น
    PdfSaveOptions options = new PdfSaveOptions();
    options.setFontsSubsystem(DocumentFontsSubsystem.usingDefaultFont("Times New Roman"));

    // บันทึกเอกสารเป็น PDF
    oneFile.save("SaveUsingDocumentFontsSubsystemWithDefaultFontName_out.pdf", options);
}
```

ในขั้นตอนนี้:
- เอกสาร OneNote ถูกโหลดโดยใช้ Aspose.Note
- แบบอักษรเริ่มต้นระบุเป็น "Times New Roman"
- เอกสารจะถูกบันทึกในรูปแบบ PDF พร้อมแบบอักษรที่ระบุ

## ขั้นตอนที่ 2: บันทึกโดยใช้ระบบย่อยแบบอักษรของเอกสารพร้อมแบบอักษรเริ่มต้นจากไฟล์

ขั้นตอนนี้สาธิตวิธีการบันทึกเอกสารในรูปแบบ PDF โดยใช้แบบอักษรเริ่มต้นที่โหลดจากไฟล์

```java
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontFromFile() throws IOException
{
    // โหลดเอกสารลงใน Aspose.Note
    Document oneFile = new Document("missing-font.one");

    // ระบุเส้นทางไปยังไฟล์ฟอนต์
    String fontFile = "geo_1.ttf";

    // ระบุแบบอักษรเริ่มต้นจากไฟล์
    PdfSaveOptions options = new PdfSaveOptions();
    options.setFontsSubsystem(DocumentFontsSubsystem.usingDefaultFontFromFile(fontFile));

    // บันทึกเอกสารเป็น PDF
    oneFile.save("SaveUsingDocumentFontsSubsystemWithDefaultFontFromFile_out.pdf", options);
}
```

ในขั้นตอนนี้:
- ไฟล์ฟอนต์ "geo_1.ttf" ถูกโหลดแล้ว
- แบบอักษรเริ่มต้นจะถูกระบุจากไฟล์แบบอักษรที่โหลด
- เอกสารจะถูกบันทึกในรูปแบบ PDF พร้อมแบบอักษรที่ระบุ

## ขั้นตอนที่ 3: บันทึกโดยใช้ระบบย่อยแบบอักษรของเอกสารด้วยแบบอักษรเริ่มต้นจากสตรีม

ขั้นตอนนี้สาธิตวิธีการบันทึกเอกสารในรูปแบบ PDF โดยใช้แบบอักษรเริ่มต้นที่โหลดจากสตรีม

```java
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontFromStream() throws IOException
{
    // โหลดเอกสารลงใน Aspose.Note
    Document oneFile = new Document("missing-font.one");

    // ระบุเส้นทางไปยังไฟล์ฟอนต์
    String fontFile = "geo_1.ttf";

    // โหลดไฟล์ฟอนต์เป็นสตรีม
    InputStream stream = new FileInputStream(fontFile);

    try
    {
        // ระบุแบบอักษรเริ่มต้นจากสตรีม
        PdfSaveOptions options = new PdfSaveOptions();
        options.setFontsSubsystem(DocumentFontsSubsystem.usingDefaultFontFromStream(stream));

        // บันทึกเอกสารเป็น PDF
        oneFile.save("SaveUsingDocumentFontsSubsystemWithDefaultFontFromStream_out.pdf", options);
    }
    catch (Exception e)
    {
        stream.close();
    }
}
```

ในขั้นตอนนี้:
- ไฟล์ฟอนต์ "geo_1.ttf" ถูกโหลดเป็นสตรีม
- แบบอักษรเริ่มต้นถูกระบุจากสตรีมที่โหลด
- เอกสารจะถูกบันทึกในรูปแบบ PDF พร้อมแบบอักษรที่ระบุ

## บทสรุป

ในบทช่วยสอนนี้ เราได้เรียนรู้วิธีบันทึกเอกสาร OneNote โดยใช้ระบบย่อยแบบอักษรที่ระบุใน Java โดยใช้ Aspose.Note ด้วยการทำตามขั้นตอนเหล่านี้ คุณสามารถรับประกันการแสดงแบบอักษรที่สอดคล้องกันบนแพลตฟอร์มต่างๆ เมื่อส่งออกหรือบันทึกเอกสารของคุณ

## คำถามที่พบบ่อย

### คำถามที่ 1: ฉันสามารถระบุแบบอักษรที่แตกต่างกันสำหรับส่วนต่างๆ ของเอกสารได้หรือไม่

A1: ได้ คุณสามารถระบุแบบอักษรที่แตกต่างกันสำหรับส่วนต่างๆ ของเอกสารได้โดยใช้ Aspose.Note สำหรับ Java

### คำถามที่ 2: Aspose.Note เข้ากันได้กับ OneNote ทุกเวอร์ชันหรือไม่

ตอบ 2: Aspose.Note รองรับ OneNote เวอร์ชันต่างๆ เพื่อให้มั่นใจถึงความเข้ากันได้ในสภาพแวดล้อมที่แตกต่างกัน

### คำถามที่ 3: ฉันจะจัดการกับแบบอักษรที่หายไปเมื่อบันทึกเอกสารได้อย่างไร

A3: Aspose.Note มีตัวเลือกในการระบุแบบอักษรเริ่มต้นเพื่อจัดการกับแบบอักษรที่หายไปอย่างมีประสิทธิภาพในระหว่างการบันทึกเอกสาร

### คำถามที่ 4: ฉันสามารถปรับแต่งคุณสมบัติแบบอักษร เช่น ขนาดและสไตล์ได้หรือไม่

A4: ได้ คุณสามารถปรับแต่งคุณสมบัติแบบอักษร เช่น ขนาด สไตล์ และสีได้โดยใช้ Aspose.Note สำหรับ Java

### คำถามที่ 5: Aspose.Note สำหรับ Java มีเวอร์ชันทดลองใช้งานหรือไม่

A5: ได้ คุณสามารถทดลองใช้ Aspose.Note สำหรับ Java ได้ฟรีจากเว็บไซต์
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
