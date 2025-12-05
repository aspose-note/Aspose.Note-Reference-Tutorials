---
date: 2025-12-04
description: เรียนรู้วิธีดึงรูปภาพจากไฟล์ OneNote และแปลง OneNote เป็นข้อความใน Java
  ด้วย Aspose.Note คู่มือทีละขั้นตอนพร้อมตัวอย่างโค้ด
language: th
linktitle: Extract Images from OneNote using Document Visitor - Java
second_title: Aspose.Note Java API
title: ดึงรูปภาพจาก OneNote ด้วย Document Visitor - Java
url: /java/onenote-document-loading/extract-content-using-document-visitor/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# ดึงรูปภาพจาก OneNote ด้วย Document Visitor - Java

## บทนำ

Aspose.Note for Java ทำให้การ **ดึงรูปภาพจาก OneNote** จากสมุดบันทึกเป็นเรื่องง่าย รวมถึงการอ่านไฟล์ `.one` ที่อยู่ด้านล่างใน Java ด้วย ในบทเรียนนี้เราจะพาคุณผ่านตัวอย่างเต็มรูปแบบที่ทำให้คุณเห็นวิธีโหลดไฟล์ OneNote, เดินทางผ่านโครงสร้างด้วย `DocumentVisitor` ที่กำหนดเอง, และดึงรูปภาพและข้อความธรรมดาออกมา เมื่อจบคุณจะรู้วิธี **แปลง OneNote เป็นข้อความ** หากคุณต้องการเพียงเนื้อหาข้อความเท่านั้น

## คำตอบด่วน
- **ฉันต้องใช้ไลบรารีอะไร?** Aspose.Note for Java (ลิงก์ดาวน์โหลดด้านล่าง).  
- **ฉันสามารถดึงรูปภาพเท่านั้นได้หรือไม่?** ได้ – ให้ทำการ implement เมธอด `VisitImageStart` ใน `DocumentVisitor`.  
- **ฉันจะอ่านไฟล์ .one ใน Java อย่างไร?** ใช้ `new Document(path, new LoadOptions())`.  
- **ฉันต้องการลิขสิทธิ์สำหรับการใช้งานจริงหรือไม่?** จำเป็นต้องมีลิขสิทธิ์เชิงพาณิชย์สำหรับการใช้งานที่ไม่ใช่รุ่นทดลอง.  
- **เวอร์ชัน Java ที่รองรับคืออะไร?** JDK 8 หรือสูงกว่า.

## ข้อกำหนดเบื้องต้น

ก่อนที่คุณจะเริ่ม, ตรวจสอบให้แน่ใจว่าคุณมี:

1. Java Development Kit (JDK) 8 หรือใหม่กว่า ติดตั้งแล้ว.  
2. ไลบรารี Aspose.Note for Java ที่ดาวน์โหลดแล้ว คุณสามารถดาวน์โหลดได้ **[ที่นี่](https://releases.aspose.com/note/java/)**.  
3. เอกสาร OneNote (`.one` file) ที่คุณต้องการดึงรูปภาพหรือแปลงเป็นข้อความ.

## นำเข้าแพ็กเกจ

แรก, ให้นำเข้าคลาสที่จำเป็นจาก Aspose.Note API.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.DocumentVisitor;
import com.aspose.note.Image;
import com.aspose.note.LoadOptions;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.OutlineGroup;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.Title;
```

## ขั้นตอนที่ 1: ตั้งค่า Custom Document Visitor

สร้างคลาสที่สืบทอดจาก `DocumentVisitor`. คลาสนี้จะถูกเรียกสำหรับแต่ละโหนดในเอกสาร One, ทำให้คุณสามารถ **ดึงรูปภาพจาก OneNote** และเก็บข้อความได้ตามต้องการ.

```java
public class ExtractOneNoteContentUsingDocumentvisitor extends DocumentVisitor {
    
    final private StringBuilder mBuilder;
    final private boolean mIsSkipText;
    private int nodecount;

    public ExtractOneNoteContentUsingDocumentvisitor() {
        nodecount = 0;
        mIsSkipText = false;
        mBuilder = new StringBuilder();
    }
    
    // Other methods will be implemented here
}
```

## ขั้นตอนที่ 2: Implement Visitor Methods

เพิ่มการ override สำหรับประเภทโหนดที่คุณสนใจ ด้านล่างเราจัดการกับ rich‑text, images, titles, pages, outlines, และ outline elements. เมธอด `VisitImageStart` คือที่ทำการดึงรูปภาพ.

```java
// Visitor methods for different types of nodes

public /* override */ void VisitRichTextStart(RichText run) {
    ++nodecount;
    AppendText(run.getText());
}

public /* override */ void VisitDocumentStart(Document document) {
    ++nodecount;
}

public /* override */ void VisitPageStart(Page page) {
    ++nodecount;
}

public /* override */ void VisitTitleStart(Title title) {
    ++nodecount;
}

public /* override */ void VisitImageStart(Image image) {
    ++nodecount;
    // Here you could save the image to disk or process it further
    System.out.println("Found image with size: " + image.getData().length + " bytes");
}

public /* override */ void VisitOutlineGroupStart(OutlineGroup outlineGroup) {
    ++nodecount;
}

public void VisitOutlineStart(Outline outline) {
    ++nodecount;
}

public void VisitOutlineElementStart(OutlineElement outlineElement) {
    ++nodecount;
}
```

### ทำไมต้อง implement เมธอดเหล่านี้?

- **ดึงรูปภาพจาก OneNote:** `VisitImageStart` ให้คุณเข้าถึงไบต์ของรูปภาพดิบโดยตรง.  
- **แปลง OneNote เป็นข้อความ:** `VisitRichTextStart` รวบรวมเนื้อหาข้อความ, ทำให้สามารถทำ **แปลง OneNote เป็นข้อความ** อย่างง่าย.  
- **อ่านไฟล์ .one ใน Java:** รูปแบบ Visitor แยกโครงสร้างไฟล์ `.one` พื้นฐานออก, ดังนั้นคุณไม่จำเป็นต้องแยกวิเคราะห์รูปแบบไบนารีด้วยตนเอง.

## ขั้นตอนที่ 3: เรียกใช้ Visitor จากเมธอด Main ของคุณ

โหลดไฟล์ `.one`, สร้างอินสแตนซ์ของ Visitor ของคุณ, และเริ่มการเดินทาง.

```java
public static void main(String[] args) throws IOException {
    // Open the document we want to convert.
    String dataDir = "Your Document Directory";
    Document doc = new Document(dataDir + "Sample1.one", new LoadOptions());
    
    // Create an object that inherits from the DocumentVisitor class.
    ExtractOneNoteContentUsingDocumentvisitor myConverter = new ExtractOneNoteContentUsingDocumentvisitor();
    
    // Accept the visitor to start the visiting process.
    doc.accept(myConverter);
    
    // Retrieve the result of the operation.
    System.out.println(myConverter.GetText());   // Text extracted from the notebook
    System.out.println(myConverter.NodeCount()); // Total nodes visited
}
```

## กรณีการใช้งานทั่วไป

- **การรายงานอัตโนมัติ:** ดึงรูปภาพและข้อความจากสมุดบันทึกการประชุม OneNote เพื่อสร้างสรุปเป็น PDF หรือ HTML.  
- **การย้ายเนื้อหา:** แปลงไฟล์ OneNote เก่าเป็นไฟล์ plain‑text เพื่อทำดัชนีหรือให้เครื่องมือค้นหาอ่าน.  
- **การสกัดสินทรัพย์ดิจิทัล:** เก็บภาพหน้าจอ, แผนภาพ, หรือรูปถ่ายที่ฝังอยู่เพื่อใช้ใหม่ในแอปพลิเคชันอื่น.

## การแก้ไขปัญหาและเคล็ดลับ

- **สมุดบันทึกขนาดใหญ่:** หากพบปัญหาหน่วยความจำ, ให้ประมวลผลหน้าแยกตาม `VisitPageStart` และโหลดทรัพยากรระดับหน้าตามความจำเป็น.  
- **รูปแบบภาพ:** อ็อบเจกต์ `Image` คืนค่าไบต์ดิบ; คุณอาจต้องตรวจจับรูปแบบ (PNG, JPEG) ก่อนบันทึก.  
- **ข้อผิดพลาดลิขสิทธิ์:** ตรวจสอบว่าคุณได้ตั้งค่าลิขสิทธิ์ Aspose (`License license = new License(); license.setLicense("Aspose.Note.Java.lic");`) ก่อนโหลดเอกสารในสภาพการผลิต.

## คำถามที่พบบ่อย

**Q: ฉันสามารถดึงประเภทเนื้อหาเฉพาะจากเอกสาร OneNote ได้หรือไม่?**  
A: ได้ – โดยการ override เฉพาะเมธอด Visitor ที่คุณต้องการ (เช่น `VisitImageStart` สำหรับรูปภาพ, `VisitRichTextStart` สำหรับข้อความ).

**Q: Aspose.Note for Java รองรับเวอร์ชันต่าง ๆ ของเอกสาร OneNote หรือไม่?**  
A: แน่นอน. ไลบรารีรองรับเวอร์ชันไฟล์ OneNote หลักทั้งหมด, ดังนั้นคุณสามารถ **อ่านไฟล์ .one ใน Java** ได้อย่างปลอดภัยไม่ว่าจะเป็นเวอร์ชันใดของ OneNote ที่มาจาก.

**Q: ฉันสามารถรวมกระบวนการสกัดนี้เข้ากับแอปพลิเคชัน Java ของฉันได้หรือไม่?**  
A: ได้. รูปแบบ Visitor ทำงานอย่างราบรื่นในโค้ด Java ใด ๆ; เพียงเพิ่ม JAR ของไลบรารีและเรียกใช้ตัวอย่างที่แสดงด้านบน.

**Q: Aspose.Note for Java มีการสนับสนุนการจัดการเอกสาร OneNote ที่ซับซ้อนหรือไม่?**  
A: มี. โครงร่างซ้อนกัน, สื่อฝัง, และข้อมูลกำหนดเองทั้งหมดสามารถเข้าถึงได้ผ่าน Visitor API.

**Q: มีขีดจำกัดขนาดของเอกสาร OneNote ที่สามารถประมวลผลได้หรือไม่?**  
A: ไม่มีขีดจำกัดที่แน่นอน, แต่สมุดบันทึกที่ใหญ่มากอาจต้องการหน่วยความจำ heap มากขึ้น; ควรพิจารณาประมวลผลเป็นหน้าทีละหน้า.

**Q: ฉันจะแปลงข้อความที่สกัดออกเป็นไฟล์ plain‑text อย่างไร?**  
A: หลังจาก `myConverter.GetText()` คืนค่า `String`, ให้เขียนลงไฟล์โดยใช้ Java I/O มาตรฐาน (`Files.write(Paths.get("output.txt"), text.getBytes());`).

---  

**อัปเดตล่าสุด:** 2025-12-04  
**ทดสอบกับ:** Aspose.Note for Java 24.10  
**ผู้เขียน:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}