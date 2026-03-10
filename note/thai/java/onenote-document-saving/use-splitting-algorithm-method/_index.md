---
date: 2025-12-18
description: เรียนรู้วิธีส่งออกหน้าของ OneNote เป็น PDF ด้วย Aspose.Note สำหรับ Java
  เลือกอัลกอริทึมการแบ่ง ตั้งค่าการแบ่งหน้า และสร้างไฟล์ PDF ได้อย่างง่ายดาย
linktitle: Export OneNote Pages with Splitting Algorithm Method – Aspose.Note
second_title: Aspose.Note Java API
title: ส่งออกหน้า OneNote ด้วยวิธีการแยกอัลกอริทึม – Aspose.Note
url: /th/java/onenote-document-saving/use-splitting-algorithm-method/
weight: 26
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# ส่งออกหน้า OneNote ด้วยวิธีอัลกอริทึมการแยก – Aspose.Note

## บทนำ

หากคุณต้องการ **export OneNote pages** ไปยังเอกสาร PDF อย่างอัตโนมัติ Aspose.Note for Java ทำให้กระบวนการง่ายดาย ในบทแนะนำนี้เราจะพาไปผ่านวิธี Splitting Algorithm Method ซึ่งช่วยให้คุณควบคุมวิธีการแบ่งเนื้อหาในหลายหน้า เพื่อให้ได้ผลลัพธ์ PDF ที่สะอาดและอ่านง่าย คุณจะได้เห็นวิธีตั้งค่า PDF save options, เลือกอัลกอริทึมการแยกหน้าให้เหมาะสมและสุดท้ายสร้างไฟล์ PDF — ทั้งหมดด้วยเพียงไม่กี่บรรทัดของโค้ด Java

## คำตอบสั้น
- **What does the Splitting Algorithm do?** มันกำหนดวิธีการจัดการกับอ็อบเจ็กต์ที่ข้ามขอบหน้าขณะ export OneNote pages ไปเป็น PDF.  
- **Which library is required?** Aspose.Note for Java (ดาวน์โหลดจากเว็บไซต์อย่างเป็นทางการของ Aspose).  
- **Do I need a license?** จำเป็นต้องมีไลเซนส์แบบชั่วคราวหรือเต็มสำหรับการใช้งานในสภาพแวดล้อมการผลิต; มีการทดลองใช้ฟรี.  
- **Can I export large OneNote notebooks?** ใช่ — ไลบรารีประมวลผลไฟล์ขนาดใหญ่อย่างมีประสิทธิภาพและให้คุณตั้งกฎการแยกหน้า.  
- **What output formats are supported?** PDF, JPEG, PNG, XPS และอื่น ๆ; คู่มือนี้เน้นการส่งออกเป็น PDF.

## **export onenote pages** คืออะไร?
การ Export OneNote pages หมายถึงการแปลงไฟล์รูปแบบ `.one` ดั้งเดิมให้เป็นรูปแบบที่พกพาได้ง่ายเช่น PDF ซึ่งมีประโยชน์สำหรับการแชร์, เก็บถาวร, หรือพิมพ์เนื้อหาโดยไม่ต้องใช้แอปพลิเคชัน OneNote.

## ทำไมต้องใช้ Splitting Algorithm สำหรับ **export onenote pages**?
อัลกอริทึมนี้ให้การควบคุมอย่างละเอียดเกี่ยวกับวิธีการจัดการอ็อบเจ็กต์ซับซ้อน (ตาราง, รูปภาพ, การวาด) ที่จุดแบ่งหน้า โดยการเลือกอัลกอริทึมที่เหมาะสมคุณสามารถ:
* รักษาเลย์เอาต์ภาพของแต่ละหน้าไว้  
* หลีกเลี่ยงเนื้อหาที่ถูกตัดที่อาจเกิดขึ้น  
* ลดจำนวนหน้าที่สร้างเมื่ออ็อบเจ็กต์สามารถย้ายไปยังหน้าถัดไปได้อย่างสะอาด  

## ข้อกำหนดเบื้องต้น
ก่อนเริ่มต้น โปรดตรวจสอบว่าคุณมีข้อกำหนดต่อไปนี้:
1. Java Development Kit (JDK): ตรวจสอบว่าคุณได้ติดตั้ง JDK บนระบบของคุณแล้ว คุณสามารถดาวน์โหลดได้จาก [website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).  
2. Aspose.Note for Java Library: ดาวน์โหลดและติดตั้งไลบรารี Aspose.Note for Java จาก [download link](https://releases.aspose.com/note/java/).

## นำเข้าแพ็กเกจ
ในโปรเจกต์ Java ของคุณ ให้นำเข้าแพ็กเกจที่จำเป็นเพื่อใช้ฟังก์ชันของ Aspose.Note

```java
import java.io.IOException;
import com.aspose.note.AlwaysSplitObjectsAlgorithm;
import com.aspose.note.Document;
import com.aspose.note.KeepPartAndCloneSolidObjectToNextPageAlgorithm;
import com.aspose.note.KeepSolidObjectsAlgorithm;
import com.aspose.note.PdfSaveOptions;
```

## ขั้นตอนที่ 1: กำหนดไดเรกทอรีเอกสาร
ตั้งค่าไดเรกทอรีที่เก็บเอกสาร OneNote ของคุณ

```java
String dataDir = "Your Document Directory";
```

## ขั้นตอนที่ 2: โหลดเอกสาร OneNote
โหลดเอกสาร OneNote ด้วยคลาส `Document` ของ Aspose.Note

```java
Document doc = new Document(dataDir + "Sample1.one");
```

## ขั้นตอนที่ 3: ตั้งค่า PDF Save Options
สร้างอินสแตนซ์ของ `PdfSaveOptions` เพื่อระบุการตั้งค่าสำหรับการบันทึกเอกสารเป็น PDF ที่นี่คุณจะ **set page splitting** พฤติกรรมและการตั้งค่าอื่น ๆ ที่เกี่ยวกับ PDF

```java
PdfSaveOptions pdfSaveOptions = new PdfSaveOptions();
```

## ขั้นตอนที่ 4: ตั้งค่าอัลกอริทึมการแยกหน้า
เลือกอัลกอริทึมการแยกที่เหมาะสมตามความต้องการของคุณ ที่นี่เราใช้ `KeepPartAndCloneSolidObjectToNextPageAlgorithm` ซึ่งจะเก็บส่วนหนึ่งของอ็อบเจ็กต์ไว้บนหน้าปัจจุบันและคัดลอกส่วนที่เหลือไปยังหน้าถัดไป

```java
pdfSaveOptions.setPageSplittingAlgorithm(new KeepPartAndCloneSolidObjectToNextPageAlgorithm(100));
```

## ขั้นตอนที่ 5: บันทึกเอกสาร
บันทึกเอกสารด้วยการตั้งค่า PDF save options ที่ระบุ ขั้นตอนนี้ **generates PDF onenote** ผลลัพธ์ที่คุณสามารถเปิด, แชร์ หรือพิมพ์ได้

```java
try {
    doc.save(dataDir + "UsingSplittingAlgorithmMethod_out.Jpeg", pdfSaveOptions);
} catch (Exception ex) {
    System.out.println("Exception: " + ex.getMessage());
}
```

## ปัญหาทั่วไปและวิธีแก้
| ปัญหา | วิธีแก้ |
|-------|----------|
| **Objects are cut off at page boundaries** | ลองใช้อัลกอริทึมอื่นเช่น `AlwaysSplitObjectsAlgorithm` หรือเพิ่มค่าขีดจำกัดใน `KeepPartAndCloneSolidObjectToNextPageAlgorithm`. |
| **Output PDF is blank** | ตรวจสอบว่าไฟล์ `.one` ต้นทางไม่ได้เสียหายและเส้นทาง `dataDir` ถูกต้อง. |
| **Performance is slow with large notebooks** | ใช้ `pdfSaveOptions.setCompressImages(true)` เพื่อลดการใช้หน่วยความจำ และพิจารณาประมวลผลโน๊ตบุ๊คเป็นส่วนย่อย ๆ. |

## คำถามที่พบบ่อย
**Q: Can I use Aspose.Note for Java with other programming languages?**  
A: ใช่, Aspose.Note มีให้ใช้งานสำหรับ .NET, C++ และ Python ด้วย  

**Q: Is Aspose.Note suitable for processing large OneNote files?**  
A: แน่นอน. ไลบรารีได้รับการปรับให้ทำงานกับโน้ตบุ๊กขนาดใหญ่ได้อย่างมีประสิทธิภาพ  

**Q: Where can I find additional resources and support for Aspose.Note?**  
A: คุณสามารถดูที่ [documentation](https://reference.aspose.com/note/java/) และ [forum](https://forum.aspose.com/c/note/28) เพื่อรับการสนับสนุนและคำแนะนำ  

**Q: Can I try Aspose.Note before purchasing?**  
A: ใช่, คุณสามารถใช้ [free trial](https://releases.aspose.com/) เพื่อสำรวจคุณลักษณะก่อนทำการซื้อ  

**Q: How can I obtain a temporary license for Aspose.Note?**  
A: คุณสามารถขอ [temporary license](https://purchase.aspose.com/temporary-license/) เพื่อประเมินผลิตภัณฑ์ในช่วงทดลองใช้งาน  

**อัปเดตล่าสุด:** 2025-12-18  
**ทดสอบกับ:** Aspose.Note 24.12 for Java  
**ผู้เขียน:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}