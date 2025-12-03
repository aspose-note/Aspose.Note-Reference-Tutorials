---
date: 2025-12-03
description: เรียนรู้วิธีแปลง OneNote เป็นข้อความโดยใช้ Aspose.Note สำหรับ Java คู่มือขั้นตอนต่อขั้นตอนที่ครอบคลุมการสกัดข้อความ
  การสกัดรูปภาพ และวิธีอ่านไฟล์ OneNote
language: th
linktitle: Convert OneNote to Text with Document Visitor – Java
second_title: Aspose.Note Java API
title: แปลง OneNote เป็นข้อความด้วย Document Visitor – Java
url: /java/onenote-document-loading/extract-content-using-document-visitor/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# แปลง OneNote เป็นข้อความด้วย Document Visitor – Java

## บทนำ

ในบทแนะนำนี้คุณจะได้เรียนรู้ **วิธีแปลง OneNote เป็นข้อความ** ด้วย Document Visitor ของ Aspose.Note for Java ไม่ว่าคุณจะต้องการอ่านไฟล์ OneNote ด้วยโปรแกรม, ดึงเนื้อหาเป็นข้อความธรรมดา, หรือดึงภาพที่ฝังอยู่, Document Visitor จะให้การควบคุมระดับละเอียดต่อแต่ละโหนดในไฟล์ .one

## คำตอบด่วน
- **“การแปลง OneNote เป็นข้อความ” หมายถึงอะไร?** หมายถึงการสกัดตัวแทนข้อความธรรมดา (และอาจรวมถึงภาพ) จากไฟล์ .one.  
- **ไลบรารีใดช่วยในเรื่องนี้?** Aspose.Note for Java มี API `DocumentVisitor`.  
- **ฉันต้องการไลเซนส์หรือไม่?** การทดลองใช้ฟรีเพียงพอสำหรับการประเมิน; จำเป็นต้องมีไลเซนส์แบบชำระเงินสำหรับการใช้งานจริง.  
- **ฉันสามารถสกัดภาพได้หรือไม่?** ได้ – เพียงทำการ implement เมธอด `VisitImageStart` เพื่อดึงรูปภาพออก.  
- **ข้อกำหนดเบื้องต้นคืออะไร?** Java JDK 8 ขึ้นไป, JAR ของ Aspose.Note for Java, และไฟล์ .one ที่ต้องการประมวลผล.

## “การแปลง OneNote เป็นข้อความ” คืออะไร?
การแปลง OneNote เป็นข้อความหมายถึงการอ่านไฟล์ OneNote (.one) ด้วยโปรแกรมและดึงเนื้อหาข้อความ, ชื่อเรื่อง, และองค์ประกอบอื่น ๆ โดยไม่ต้องใช้ UI ของ OneNote ดั้งเดิม ซึ่งเป็นประโยชน์สำหรับการทำดัชนีการค้นหา, การสร้างรายงาน, หรือการย้ายเนื้อหาไปยังแพลตฟอร์มอื่น

## ทำไมต้องใช้ Document Visitor เพื่อ **อ่านไฟล์ OneNote** ?
Document Visitor ใช้รูปแบบการออกแบบ Visitor ทำให้คุณสามารถเดินผ่านแต่ละองค์ประกอบ (หน้า, โครงร่าง, ภาพ, ชุดข้อความ rich‑text ฯลฯ) ในเอกสาร OneNote ได้ เมื่อเทียบกับการโหลดเอกสารทั้งหมดเข้าสู่หน่วยความจำและทำการพาร์สด้วยตนเอง วิธีการ Visitor มีคุณสมบัติดังนี้:

* **ประหยัดหน่วยความจำ** – ประมวลผลโหนดทีละหนึ่ง.  
* **ขยายได้** – คุณสามารถเพิ่มตรรกะแบบกำหนดเองสำหรับโหนดประเภทใดก็ได้ (เช่น สกัดภาพ).  
* **แม่นยำ** – รักษาโครงสร้างต้นฉบับไว้ ทำให้คุณไม่พลาดเนื้อหาที่ซ่อนอยู่.

## ข้อกำหนดเบื้องต้น

ก่อนเริ่มทำตามขั้นตอนต่อไปนี้ให้แน่ใจว่าคุณมี:

1. **Java Development Kit (JDK) 8 หรือใหม่กว่า** ติดตั้งแล้ว.  
2. ไลบรารี **Aspose.Note for Java** ดาวน์โหลดจากเว็บไซต์ทางการ – [download here](https://releases.aspose.com/note/java/).  
3. **เอกสาร OneNote** (`.one` file) ที่คุณต้องการแปลงเป็นข้อความ.  

## ขั้นตอนที่ 1: นำเข้าแพ็กเกจ

แรกเริ่มให้ import คลาสที่คุณต้องใช้ในการทำงานกับ Aspose.Note for Java.

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

## ขั้นตอนที่ 2: ตั้งค่าคลาส Document Visitor

สร้างคลาสที่สืบทอดจาก `DocumentVisitor`. Visitor แบบกำหนดเองนี้จะรวบรวมข้อความ, นับจำนวนโหนด, และ (หากต้องการ) เก็บภาพ.

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

## ขั้นตอนที่ 3: Implement Visitor Methods  

ที่นี่เราจะทำการ implement คอลแบ็กสำหรับประเภทโหนดที่เราต้องการ ประมวลผลจะเพิ่มตัวนับโหนดและสำหรับ `RichText` จะต่อข้อความจริงเข้าไปใน `StringBuilder` ของเรา คุณยังสามารถเพิ่มตรรกะเพื่อ **สกัดภาพจาก OneNote** โดยจัดการ `VisitImageStart`.

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
    // Pro tip: you can save the image stream here if you need to extract images.
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

## ขั้นตอนที่ 4: เมธอด main – เรียกใช้ Visitor

เมธอด `main` จะโหลดไฟล์ OneNote, สร้างอินสแตนซ์ของ Visitor ที่กำหนดเองของเรา, และเริ่มการเดินผ่าน หลังจากการเยี่ยมชม เราจะแสดงข้อความที่สกัดและจำนวนโหนดทั้งหมด.

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
    System.out.println(myConverter.GetText());
    System.out.println(myConverter.NodeCount());
}
```

## กรณีการใช้งานทั่วไป – **สกัดภาพจาก OneNote**

* **การทำดัชนีการค้นหา** – แปลงโน้ตบุ๊ก OneNote เป็นข้อความธรรมดาสำหรับเครื่องมือค้นหาแบบเต็มข้อความ.  
* **การย้ายเนื้อหา** – ย้ายโน้ตไปยัง CMS หรือพอร์ทัลเอกสาร.  
* **การวิเคราะห์ข้อมูล** – ดึงข้อความและภาพสำหรับการประมวลผลภาษาธรรมชาติหรือการวิเคราะห์ภาพ.  

## ปัญหาทั่วไปและวิธีแก้

| ปัญหา | วิธีแก้ |
|-------|----------|
| **NullPointerException เมื่ออ่านไฟล์ .one** | ตรวจสอบให้แน่ใจว่าเส้นทางไฟล์ (`dataDir`) ลงท้ายด้วยตัวคั่นเส้นทาง (`/` หรือ `\\`) และไฟล์มีอยู่จริง. |
| **ไม่สามารถสกัดภาพได้** | Implement logic ภายใน `VisitImageStart` เพื่อเขียน `image.getImageData()` ไปยังไฟล์หรือสตรีม. |
| **โน้ตบุ๊กขนาดใหญ่ทำให้ใช้หน่วยความจำสูง** | ประมวลผลเอกสารทีละหน้า หรือใช้ API สตรีมมิ่งหากมี. |

## คำถามที่พบบ่อย

**Q: ฉันสามารถสกัดประเภทเนื้อหาเฉพาะจากเอกสาร OneNote ได้หรือไม่?**  
A: ได้โดยการ implement เฉพาะเมธอด visitor ที่ต้องการ (เช่น `VisitRichTextStart` สำหรับข้อความ, `VisitImageStart` สำหรับภาพ).

**Q: Aspose.Note for Java รองรับไฟล์ OneNote เวอร์ชันต่าง ๆ หรือไม่?**  
A: แน่นอน ไลบรารีรองรับไฟล์ .one ที่สร้างโดยเวอร์ชันล่าสุดของ Microsoft OneNote.

**Q: ฉันสามารถรวมกระบวนการสกัดนี้เข้าในแอปพลิเคชัน Java ของฉันได้หรือไม่?**  
A: ได้ โค้ดที่แสดงเป็นตัวอย่างที่ทำงานอิสระซึ่งคุณสามารถฝังลงในโปรเจกต์ Java ใดก็ได้โดยตรง.

**Q: Aspose.Note for Java จัดการโครงสร้าง OneNote ที่ซับซ้อนได้หรือไม่?**  
A: ทำได้ รูปแบบ Visitor ช่วยให้คุณนำทางโครงร่างซ้อนกัน, กลุ่ม, และวัตถุฝังโดยไม่สูญเสียลำดับชั้น.

**Q: มีขีดจำกัดขนาดของเอกสาร OneNote ที่สามารถประมวลผลได้หรือไม่?**  
A: แม้จะไม่มีขีดจำกัดที่แน่นอน แต่โน้ตบุ๊กขนาดใหญ่มากอาจต้องการหน่วยความจำ heap เพิ่มเติม; ควรพิจารณาประมวลผลเป็นส่วน ๆ

**Q: ฉันจะสกัดภาพจาก OneNote อย่างไร?**  
A: Implement เมธอด `VisitImageStart` เพื่อเข้าถึง `image.getImageData()` และเขียนไบต์ไปยังไฟล์.

---

**อัปเดตล่าสุด:** 2025-12-03  
**ทดสอบกับ:** Aspose.Note for Java 24.11  
**ผู้เขียน:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}