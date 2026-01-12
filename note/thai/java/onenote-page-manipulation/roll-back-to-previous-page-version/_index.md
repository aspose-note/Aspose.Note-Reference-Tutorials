---
date: 2026-01-12
description: เรียนรู้วิธีย้อนกลับหน้าของ OneNote และกู้คืนเวอร์ชันก่อนหน้าของ OneNote
  ด้วย Aspose.Note สำหรับ Java. ปฏิบัติตามคู่มือขั้นตอนนี้เพื่อการจัดการเอกสารที่มีประสิทธิภาพ.
linktitle: How to Roll Back OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: วิธีย้อนกลับ OneNote - Aspose.Note
url: /th/java/onenote-page-manipulation/roll-back-to-previous-page-version/
weight: 19
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# วิธีการย้อนกลับ OneNote - Aspose.Note

## Introduction

หากคุณกำลังมองหาวิธีที่ชัดเจนและเป็นโปรแกรมเพื่อ **how to roll back onenote** หน้าเมื่อเกิดข้อผิดพลาด คุณมาถูกที่แล้ว ในบทแนะนำนี้เราจะอธิบายการใช้ Aspose.Note for Java เพื่อย้อนกลับหน้า OneNote ไปยังสถานะก่อนหน้า ไม่ว่าคุณจะกำลังสร้างเครื่องมือจัดการโน้ตอัตโนมัติหรือจำเป็นต้องมีเครือข่ายความปลอดภัยสำหรับสมุดบันทึกแบบร่วมมือ การย้อนกลับหน้าจะช่วยให้เนื้อหาของคุณแม่นยำและเชื่อถือได้

## Quick Answers
- **“roll back” หมายถึงอะไรใน OneNote?** การคืนหน้ากลับไปยังเวอร์ชันก่อนหน้าที่บันทึกไว้ในประวัติของมัน.  
- **API ใดที่จัดการการย้อนกลับ?** `PageHistory` class in Aspose.Note for Java.  
- **ฉันต้องการใบอนุญาตหรือไม่?** จำเป็นต้องมีใบอนุญาต Aspose.Note ที่ถูกต้องสำหรับการใช้งานในสภาพแวดล้อมการผลิต.  
- **ฉันสามารถเลือกเวอร์ชันก่อนหน้าใดก็ได้หรือไม่?** ได้ – คุณสามารถเลือกรายการใดก็ได้จากรายการประวัติของหน้า.  
- **วิธีนี้ปลอดภัยสำหรับสมุดบันทึกขนาดใหญ่หรือไม่?** แน่นอน; การดำเนินการทำงานบนหน้าแต่ละหน้าโดยไม่ต้องโหลดสมุดบันทึกทั้งหมดเข้าสู่หน่วยความจำ.

## วิธีการย้อนกลับเวอร์ชันหน้า OneNote
ต่อไปนี้เป็นคู่มือสั้น ๆ ที่เป็นขั้นตอนโดยละเอียดซึ่งแสดงวิธีทำการย้อนกลับอย่างชัดเจน แต่ละขั้นตอนมีคำอธิบายสั้น ๆ เพื่อให้คุณเข้าใจ *ทำไม* เราถึงทำเช่นนั้น ไม่ใช่แค่ *ทำอะไร* ที่ต้องพิมพ์

## Prerequisites

ก่อนที่เราจะลงลึกในโค้ด โปรดตรวจสอบว่าคุณมีสิ่งต่อไปนี้พร้อมแล้ว:

### Java Development Environment Setup
1. **Install Java Development Kit (JDK):** ดาวน์โหลด JDK เวอร์ชันล่าสุดจากเว็บไซต์ของ Oracle หรือจากตัวจัดการแพคเกจที่คุณชื่นชอบ.  
2. **Configure Environment Variables:** ตั้งค่า `JAVA_HOME` และอัปเดต `PATH` เพื่อให้คำสั่ง `java` และ `javac` สามารถเรียกใช้จากบรรทัดคำสั่งได้.  
3. **Add Aspose.Note for Java:** ดาวน์โหลดไลบรารีจาก [website](https://purchase.aspose.com/buy) และเพิ่มไฟล์ JAR ลงใน classpath ของโครงการของคุณ.

## Import Packages

เพื่อโต้ตอบกับไฟล์ OneNote ให้นำเข้าคลาส Aspose.Note ที่จำเป็น:

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.PageHistory;
```

## Step 1: Load OneNote Document
```java
String dataDir = "Your Document Directory";
Document document = new Document(dataDir + "Sample1.one");
```
เราจะชี้ไปยังโฟลเดอร์ที่เก็บไฟล์ `.one` แล้วโหลดมันเข้าสู่วัตถุ `Document`.

## Step 2: Get Page History
```java
Page page = document.getFirstChild();
PageHistory pageHistory = document.getPageHistory(page);
```
`PageHistory` ให้คุณเข้าถึงทุกเวอร์ชันที่บันทึกของหน้าที่เลือก ทำให้สามารถ **restore previous onenote version** ได้.

## Step 3: Remove Current Page
```java
document.removeChild(page);
```
โดยการลบหน้าปัจจุบัน เราจะสร้างพื้นที่สำหรับเวอร์ชันที่ต้องการนำกลับมา.

## Step 4: Append Previous Page Version
```java
document.appendChildLast(pageHistory.get_Item(pageHistory.size() - 1));
```
ที่นี่เราจะเลือกรายการประวัติที่ล่าสุด (คุณสามารถเปลี่ยนดัชนีเพื่อเลือกเวอร์ชันที่เก่ากว่า) แล้วเพิ่มกลับไปยังเอกสาร.

## Step 5: Save Document
```java
document.save(dataDir + "RollBackToPreviousPageVersion_out.one");
```
สุดท้าย บันทึกสมุดบันทึกที่แก้ไขแล้ว ไฟล์ผลลัพธ์จะมีหน้าที่ถูกย้อนกลับอยู่.

## Restore Previous OneNote Version
การผสมผสานของ `PageHistory` และ `appendChildLast` ทำให้คุณสามารถ **restore previous onenote version** ได้ด้วยเพียงไม่กี่บรรทัดของโค้ด ซึ่งเป็นประโยชน์อย่างยิ่งในเวิร์กโฟลว์อัตโนมัติที่ไม่สามารถทำการย้อนกลับด้วยมือได้.

## Common Issues & Tips
- **Empty History:** หาก `pageHistory.size()` คืนค่าเป็น 0 หน้าไม่มีเวอร์ชันที่บันทึกไว้—ตรวจสอบให้แน่ใจว่าได้เปิดใช้งานการเวอร์ชันใน OneNote.  
- **Index Out of Bounds:** จำไว้ว่ารายการประวัติมีการนับตั้งแต่ศูนย์ ปรับดัชนี (`size() - 1`) เพื่อเลือกเวอร์ชันที่ต้องการอย่างแม่นยำ.  
- **Performance:** การทำงานกับหน้าเดียวช่วยหลีกเลี่ยงการโหลดสมุดบันทึกทั้งหมดเข้าสู่หน่วยความจำ ทำให้การดำเนินการเร็วแม้กับไฟล์ขนาดใหญ่.

## Conclusion

ตอนนี้คุณมีวิธีที่ครบถ้วนและพร้อมใช้งานในสภาพแวดล้อมการผลิตสำหรับ **how to roll back onenote** หน้าโดยใช้ Aspose.Note for Java ด้วยการใช้ `PageHistory` คุณสามารถคืนสถานะก่อนหน้าของหน้าสมุดบันทึกได้อย่างปลอดภัย ทำให้มั่นใจในความสมบูรณ์ของข้อมูลและให้ผู้ใช้ปลายทางมั่นใจในสภาพแวดล้อมการทำงานร่วมกัน

## Frequently Asked Questions

**Q1: ฉันสามารถย้อนกลับหลายเวอร์ชันของหน้าได้หรือไม่?**  
A: ได้ คุณสามารถเข้าถึงประวัติของหน้าทั้งหมดและย้อนกลับไปยังเวอร์ชันก่อนหน้าใดก็ได้ตามต้องการ.

**Q2: Aspose.Note รองรับภาษาโปรแกรมอื่นนอกจาก Java หรือไม่?**  
A: ใช่, Aspose.Note มีไลบรารีสำหรับหลายภาษาโปรแกรม รวมถึง .NET, C++ และ Python.

**Q3: Aspose.Note เข้ากันได้กับทุกเวอร์ชันของ OneNote หรือไม่?**  
A: Aspose.Note รองรับรูปแบบ OneNote ต่าง ๆ ทำให้เข้ากันได้กับส่วนใหญ่ของเวอร์ชันเอกสาร.

**Q4: ฉันสามารถทำงานอัตโนมัติอื่น ๆ ใน OneNote ด้วย Aspose.Note ได้หรือไม่?**  
A: แน่นอน, Aspose.Note มีความสามารถที่ครอบคลุมในการเพิ่ม, ลบ, และแก้ไขเนื้อหาโดยโปรแกรม.

**Q5: มีฟอรั่มชุมชนหรือการสนับสนุนสำหรับ Aspose.Note หรือไม่?**  
A: มี, คุณสามารถเยี่ยมชม [Aspose.Note forum](https://forum.aspose.com/c/note/28) เพื่อรับการสนับสนุนจากชุมชน หรือ ติดต่อฝ่ายสนับสนุนลูกค้าของ Aspose เพื่อขอความช่วยเหลือ.

---

**อัปเดตล่าสุด:** 2026-01-12  
**ทดสอบด้วย:** Aspose.Note for Java (latest release)  
**ผู้เขียน:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}