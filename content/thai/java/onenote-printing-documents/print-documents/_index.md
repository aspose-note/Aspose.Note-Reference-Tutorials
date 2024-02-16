---
title: พิมพ์เอกสารใน OneNote - Aspose.Note
linktitle: พิมพ์เอกสารใน OneNote - Aspose.Note
second_title: Aspose.Note Java API
description: เรียนรู้วิธีพิมพ์เอกสารใน OneNote โดยใช้ Aspose.Note สำหรับ Java คำแนะนำทีละขั้นตอนพร้อมตัวอย่างโค้ดและตัวเลือกที่ปรับแต่งได้
type: docs
weight: 10
url: /th/java/onenote-printing-documents/print-documents/
---
## การแนะนำ

การพิมพ์เอกสารเป็นข้อกำหนดทั่วไปสำหรับแอปพลิเคชันต่างๆ รวมถึง OneNote Aspose.Note สำหรับ Java มีความสามารถอันทรงพลังในการพิมพ์เอกสารภายในแอปพลิเคชัน Java ของคุณได้อย่างง่ายดาย ในบทช่วยสอนนี้ เราจะอธิบายขั้นตอนการพิมพ์เอกสารใน OneNote โดยใช้ Aspose.Note for Java

## ข้อกำหนดเบื้องต้น

ก่อนที่คุณจะเริ่มต้น ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:

1. Java Development Kit (JDK): ตรวจสอบให้แน่ใจว่าคุณได้ติดตั้ง JDK บนระบบของคุณแล้ว
2.  Aspose.Note สำหรับ Java JAR: ดาวน์โหลดและรวม Aspose.Note สำหรับไลบรารี Java ในโปรเจ็กต์ของคุณ คุณสามารถดาวน์โหลดได้จาก[ที่นี่](https://releases.aspose.com/note/java/).
3. เอกสาร OneNote: เตรียมเอกสาร OneNote ที่คุณต้องการพิมพ์

## แพ็คเกจนำเข้า

ขั้นแรก คุณต้องนำเข้าแพ็คเกจที่จำเป็นไปยังคลาส Java ของคุณ:

```java
import javax.print.PrintException;

import com.aspose.note.Document;
import com.aspose.note.DocumentPrintAttributeSet;
import com.aspose.note.PrintOptions;
```

## ขั้นตอนที่ 1: พิมพ์เอกสาร

เริ่มต้นด้วยการพิมพ์เอกสารโดยไม่มีตัวเลือกการพิมพ์เฉพาะใดๆ

```java
public static void PrintDocument() throws PrintException {
    // ระบุไดเร็กทอรีที่มีเอกสารของคุณอยู่
    String dataDir = "Your Document Directory";
    
    // โหลดเอกสาร OneNote
    Document document = new Document(dataDir + "YourDocument.one");
    
    // พิมพ์เอกสาร
    document.print();
}
```

## ขั้นตอนที่ 2: พิมพ์เอกสารด้วยตัวเลือกการพิมพ์

คุณสามารถปรับแต่งกระบวนการพิมพ์ได้โดยระบุตัวเลือกการพิมพ์ เช่น ช่วงการพิมพ์และการตั้งค่าเครื่องพิมพ์

```java
public static void PrintDocumentWithPrintOptions() throws PrintException {
    // ระบุไดเร็กทอรีที่มีเอกสารของคุณอยู่
    String dataDir = "Your Document Directory";

    // โหลดเอกสาร OneNote
    Document document = new Document(dataDir + "YourDocument.one");

    // กำหนดตัวเลือกการพิมพ์
    final DocumentPrintAttributeSet asposeAttr = new DocumentPrintAttributeSet("Microsoft XPS Document Writer");
    asposeAttr.setPrintRange(1, 2);

    // พิมพ์เอกสารด้วยตัวเลือกที่ระบุ
    document.print(asposeAttr);
}
```

## ขั้นตอนที่ 3: พิมพ์เอกสารด้วยเครื่องพิมพ์เสมือน

คุณยังสามารถใช้เครื่องพิมพ์เสมือนเพื่อพิมพ์เอกสารได้ ต่อไปนี้เป็นวิธีพิมพ์เอกสารด้วยเครื่องพิมพ์ PDF เสมือน

```java
public static void PrintDocumentsWithVirtualPrinter() throws PrintException {
    // ระบุไดเร็กทอรีที่มีเอกสารของคุณอยู่
    String dataDir = "Your Document Directory";
    Document doc = new Document(dataDir + "YourDocument.one");
     
    // กำหนดตัวเลือกการพิมพ์สำหรับเครื่องพิมพ์เสมือน
    final DocumentPrintAttributeSet asposeAttr = new DocumentPrintAttributeSet("doPDF 8");
    asposeAttr.setPrintRange(1, 2);
    asposeAttr.setCopies(3);
     
    PrintOptions printOptions = new PrintOptions();
    printOptions.setDocumentName("YourDocument.one");
    printOptions.setPrinterSettings(asposeAttr);
      
    // พิมพ์เอกสารโดยใช้เครื่องพิมพ์เสมือน
    doc.print(printOptions);
}
```

## บทสรุป

การพิมพ์เอกสารใน OneNote โดยใช้ Aspose.Note สำหรับ Java นั้นตรงไปตรงมาและยืดหยุ่น ด้วยการทำตามขั้นตอนที่ระบุไว้ในบทช่วยสอนนี้ คุณสามารถรวมฟังก์ชันการพิมพ์เอกสารเข้ากับแอปพลิเคชัน Java ของคุณได้อย่างราบรื่น

## คำถามที่พบบ่อย

### คำถามที่ 1: ฉันสามารถพิมพ์หน้าเฉพาะของเอกสาร OneNote ได้หรือไม่

A1: ได้ คุณสามารถระบุช่วงการพิมพ์เพื่อพิมพ์หน้าเอกสารเฉพาะได้

### คำถามที่ 2: Aspose.Note สำหรับ Java เข้ากันได้กับเครื่องพิมพ์เสมือนหรือไม่

ตอบ 2: ใช่ Aspose.Note สำหรับ Java รองรับการพิมพ์เอกสารด้วยเครื่องพิมพ์เสมือน

### คำถามที่ 3: ฉันสามารถปรับแต่งการตั้งค่าการพิมพ์ เช่น จำนวนสำเนาได้หรือไม่

A3: แน่นอน คุณสามารถปรับแต่งการตั้งค่าการพิมพ์ต่างๆ รวมถึงจำนวนสำเนา ช่วงการพิมพ์ และอื่นๆ อีกมากมาย

### คำถามที่ 4: Aspose.Note สำหรับ Java จำเป็นต้องมีใบอนุญาตในการพิมพ์เอกสารหรือไม่

ตอบ 4: ใช่ คุณต้องมีใบอนุญาตที่ถูกต้องเพื่อใช้ Aspose.Note สำหรับ Java ในสภาพแวดล้อมการใช้งานจริง

### คำถามที่ 5: ฉันจะค้นหาการสนับสนุนและทรัพยากรเพิ่มเติมสำหรับ Aspose.Note สำหรับ Java ได้ที่ไหน

 A5: คุณสามารถค้นหาเอกสาร ฟอรั่ม และทรัพยากรเพิ่มเติมได้ใน[Aspose.Note สำหรับหน้าสนับสนุน Java](https://forum.aspose.com/c/note/28).