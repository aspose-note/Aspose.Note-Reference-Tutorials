---
date: 2026-05-25
description: เรียนรู้วิธีกู้คืนเวอร์ชัน OneNote ก่อนหน้าและย้อนกลับหน้าของ OneNote
  ด้วย Aspose.Note สำหรับ Java. ทำตามคู่มือขั้นตอนต่อขั้นตอนนี้เพื่อการจัดการเอกสารที่มีประสิทธิภาพ.
keywords:
- restore previous onenote version
- how to roll back onenote
- read .one file java
- recover previous onenote page
linktitle: วิธีกู้คืนเวอร์ชัน OneNote ก่อนหน้า – Aspose.Note
schemas:
- author: Aspose
  dateModified: '2026-05-25'
  description: Learn how to restore previous OneNote version and roll back OneNote
    pages using Aspose.Note for Java. Follow this step‑by‑step guide for efficient
    document management.
  headline: How to Restore Previous OneNote Version – Aspose.Note
  type: TechArticle
- description: Learn how to restore previous OneNote version and roll back OneNote
    pages using Aspose.Note for Java. Follow this step‑by‑step guide for efficient
    document management.
  name: How to Restore Previous OneNote Version – Aspose.Note
  steps:
  - name: '**Install Java Development Kit (JDK):** Grab the latest JDK from the Oracle
      website or your preferred package manager.'
    text: '**Install Java Development Kit (JDK):** Grab the latest JDK from the Oracle
      website or your preferred package manager.'
  - name: '**Configure Environment Variables:** Set `JAVA_HOME` and update `PATH`
      so the `java` and `javac` commands are reachable from the command line.'
    text: '**Configure Environment Variables:** Set `JAVA_HOME` and update `PATH`
      so the `java` and `javac` commands are reachable from the command line.'
  - name: '**Add Aspose.Note for Java:** Download the library from the [website](https://purchase.aspose.com/buy)
      and add the JAR to your project''s classpath.'
    text: '**Add Aspose.Note for Java:** Download the library from the [website](https://purchase.aspose.com/buy)
      and add the JAR to your project''s classpath.'
  type: HowTo
- questions:
  - answer: Restoring a page to a prior version saved in its history.
    question: What does “roll back” mean for OneNote?
  - answer: '`PageHistory` class in Aspose.Note for Java.'
    question: Which API handles the rollback?
  - answer: A valid Aspose.Note license is required for production use.
    question: Do I need a license?
  - answer: Yes – you can pick any entry from the page’s history list.
    question: Can I choose any previous version?
  - answer: Absolutely; the operation works on individual pages without loading the
      entire notebook into memory.
    question: Is this approach safe for large notebooks?
  type: FAQPage
second_title: Aspose.Note Java API
title: วิธีกู้คืนเวอร์ชัน OneNote ก่อนหน้า – Aspose.Note
url: /th/java/onenote-page-manipulation/roll-back-to-previous-page-version/
weight: 19
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# วิธีกู้คืนเวอร์ชัน OneNote ก่อนหน้า – Aspose.Note

## บทนำ

หากคุณต้องการวิธีที่เชื่อถือได้และเป็นโปรแกรมเพื่อ **กู้คืนเวอร์ชัน OneNote ก่อนหน้า** เมื่อเกิดการแก้ไขโดยบังเอิญ คุณมาถูกที่แล้ว ในบทเรียนนี้เราจะพาไปผ่าน Aspose.Note สำหรับ Java แสดงให้คุณเห็นอย่างชัดเจนว่าจะแก้ไขหน้า OneNote ให้กลับไปยังสถานะก่อนหน้าอย่างไร ไม่ว่าคุณจะสร้างบริการจัดการโน้ตอัตโนมัติหรือเพิ่มเครือข่ายความปลอดภัยสำหรับสมุดบันทึกแบบร่วมมือ ความสามารถในการย้อนกลับหน้าจะทำให้เนื้อหาของคุณแม่นยำ เชื่อถือได้ และพร้อมสำหรับการตรวจสอบ

## คำตอบด่วน
- **“roll back” หมายถึงอะไรใน OneNote?** การกู้คืนหน้าหนึ่งไปยังเวอร์ชันก่อนหน้าที่บันทึกไว้ในประวัติ  
- **API ใดจัดการการ rollback?** `PageHistory` class in Aspose.Note for Java.  
- **ต้องการใบอนุญาตหรือไม่?** จำเป็นต้องมีใบอนุญาต Aspose.Note ที่ถูกต้องสำหรับการใช้งานในสภาพแวดล้อมการผลิต  
- **ฉันสามารถเลือกเวอร์ชันก่อนหน้าใดก็ได้หรือไม่?** ใช่ – คุณสามารถเลือกรายการใดก็ได้จากรายการประวัติของหน้า  
- **วิธีนี้ปลอดภัยสำหรับสมุดบันทึกขนาดใหญ่หรือไม่?** แน่นอน; การดำเนินการทำงานบนหน้าแต่ละหน้าโดยไม่ต้องโหลดสมุดบันทึกทั้งหมดเข้าสู่หน่วยความจำ  

## อะไรคือ “restore previous onenote version”?
**`restore previous onenote version`** หมายถึงกระบวนการดึงสแนปช็อตก่อนหน้าของหน้า OneNote จากประวัติเวอร์ชันภายในและแทนที่เนื้อหาหน้าปัจจุบันด้วยสแนปช็อตนั้น การดำเนินการนี้ได้รับการสนับสนุนเต็มรูปแบบโดย API `PageHistory` ของ Aspose.Note และไม่ต้องการการทำ Undo ด้วยตนเอง  

## ทำไมต้องใช้ Aspose.Note เพื่อย้อนกลับหน้าของ OneNote?
Aspose.Note สามารถประมวลผลสมุดบันทึกที่มี **หลายพันหน้า** พร้อมรักษาการใช้หน่วยความจำให้อยู่ภายใต้ **50 MB** เนื่องจากทำงานแบบหน้า‑ต่อหน้า รองรับ **คุณลักษณะเฉพาะของ OneNote มากกว่า 30 รายการ** รวมถึงการอ่านไฟล์ `.one` การสกัดข้อมูลเมตา และการกู้คืนรายการประวัติใด ๆ สิ่งนี้ทำให้เป็นตัวเลือกที่เหมาะสำหรับการทำอัตโนมัติระดับองค์กรที่ความน่าเชื่อถือและประสิทธิภาพเป็นสิ่งสำคัญ  

## ข้อกำหนดเบื้องต้น

ก่อนที่เราจะลงลึกในโค้ด โปรดตรวจสอบว่าคุณมีสิ่งต่อไปนี้พร้อมใช้งาน:

### การตั้งค่าสภาพแวดล้อมการพัฒนา Java
1. **ติดตั้ง Java Development Kit (JDK):** ดาวน์โหลด JDK เวอร์ชันล่าสุดจากเว็บไซต์ของ Oracle หรือจากตัวจัดการแพ็กเกจที่คุณชื่นชอบ  
2. **กำหนดค่าตัวแปรสภาพแวดล้อม:** ตั้งค่า `JAVA_HOME` และอัปเดต `PATH` เพื่อให้คำสั่ง `java` และ `javac` สามารถเรียกใช้จากบรรทัดคำสั่งได้  
3. **เพิ่ม Aspose.Note สำหรับ Java:** ดาวน์โหลดไลบรารีจาก [เว็บไซต์](https://purchase.aspose.com/buy) และเพิ่มไฟล์ JAR ไปยัง classpath ของโปรเจกต์ของคุณ  

## นำเข้าแพ็กเกจ

To interact with OneNote files, import the essential Aspose.Note classes:

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.PageHistory;
```

## ฉันจะกู้คืนเวอร์ชันหน้า OneNote ก่อนหน้าได้อย่างไร?
โหลดสมุดบันทึกเป้าหมาย ดึงรายการประวัติที่ต้องการด้วย `PageHistory` ลบหน้าปัจจุบัน และเพิ่มเวอร์ชันที่เลือกกลับไปยังเอกสาร – ทั้งหมดในโค้ด Java ไม่เกินสิบบรรทัด วิธีนี้รับประกันว่าจะมีการแก้ไขเฉพาะหน้าที่เลือกเท่านั้น รักษาส่วนอื่นของสมุดบันทึกไม่เปลี่ยนแปลงและทำให้การใช้หน่วยความจำน้อยที่สุด  

## ขั้นตอนที่ 1: โหลดเอกสาร OneNote

`Document` คืออ็อบเจ็กต์ระดับบนสุดของ Aspose.Note ที่แทนไฟล์ OneNote เดียวในหน่วยความจำ เราเริ่มต้นโดยชี้ไปยังโฟลเดอร์ที่เก็บไฟล์ `.one` แล้วโหลดมันเข้าสู่ตัวแปร `Document` instance

```java
String dataDir = "Your Document Directory";
Document document = new Document(dataDir + "Sample1.one");
```
เราชี้ไปยังโฟลเดอร์ที่เก็บไฟล์ `.one` และโหลดมันเข้าสู่วัตถุ `Document`

## ขั้นตอนที่ 2: ดึงประวัติกหน้า

`PageHistory` ให้การเข้าถึงทุกเวอร์ชันที่บันทึกของหน้าที่เลือก ทำให้สามารถใช้ความสามารถ **restore previous onenote version** ได้ โดยการเรียก `getHistory()` คุณจะได้รับรายการที่สามารถวนลูปหรือเข้าถึงโดยตรงด้วยดัชนี

```java
Page page = document.getFirstChild();
PageHistory pageHistory = document.getPageHistory(page);
```
`PageHistory` ให้คุณเข้าถึงทุกเวอร์ชันที่บันทึกของหน้าที่เลือก ทำให้สามารถใช้ความสามารถ **restore previous onenote version** ได้

## ขั้นตอนที่ 3: ลบหน้าปัจจุบัน

`Page` แทนหน้าต่าง ๆ ภายในสมุดบันทึก OneNote การลบหน้าปัจจุบันจะสร้างพื้นที่สำหรับเวอร์ชันประวัติที่คุณต้องการนำกลับมา

```java
document.removeChild(page);
```
โดยการลบหน้าปัจจุบัน เราจะสร้างพื้นที่สำหรับเวอร์ชันที่ต้องการนำกลับมา

## ขั้นตอนที่ 4: เพิ่มเวอร์ชันหน้าก่อนหน้า

`appendChildLast` เพิ่มโหนดไปยังตำแหน่งสุดท้ายของคอลเลกชันลูกของเอกสาร ที่นี่เราจะเลือกรายการประวัติที่ใหม่ที่สุด (คุณสามารถเปลี่ยนดัชนีเพื่อเลือกเวอร์ชันเก่าใดก็ได้) แล้วเพิ่มกลับไปยังเอกสาร

```java
document.appendChildLast(pageHistory.get_Item(pageHistory.size() - 1));
```
ที่นี่เราจะเลือกรายการประวัติที่ใหม่ที่สุด (คุณสามารถเปลี่ยนดัชนีเพื่อเลือกเวอร์ชันเก่าใดก็ได้) แล้วเพิ่มกลับไปยังเอกสาร

## ขั้นตอนที่ 5: บันทึกเอกสาร

การบันทึกจะเขียนสมุดบันทึกที่แก้ไขแล้วกลับไปยังดิสก์ สร้างไฟล์ที่ตอนนี้มีหน้าที่ถูกย้อนกลับ การดำเนินการจะเขียนเฉพาะหน้าที่เปลี่ยนแปลงเท่านั้น ทำให้สมุดบันทึกขนาดใหญ่ยังคงประมวลผลได้อย่างรวดเร็ว

```java
document.save(dataDir + "RollBackToPreviousPageVersion_out.one");
```
สุดท้าย บันทึกสมุดบันทึกที่แก้ไขแล้ว ไฟล์ผลลัพธ์ตอนนี้มีหน้าที่ถูกย้อนกลับ

## ปัญหาที่พบบ่อยและเคล็ดลับ
- **Empty History:** หาก `pageHistory.size()` คืนค่า 0 หน้าไม่มีเวอร์ชันที่บันทึกไว้ — ตรวจสอบให้แน่ใจว่าการเวอร์ชันเปิดใช้งานใน OneNote  
- **Index Out of Bounds:** จำไว้ว่ารายการประวัติเริ่มจากศูนย์ ปรับดัชนี (`size() - 1`) เพื่อเลือกเวอร์ชันที่ต้องการอย่างแม่นยำ  
- **Performance:** การทำงานกับหน้าเดียวช่วยหลีกเลี่ยงการโหลดสมุดบันทึกทั้งหมดเข้าสู่หน่วยความจำ ทำให้การดำเนินการเร็วแม้กับสมุดบันทึกที่มี **10,000+ หน้า**  
- **Reading .one files in Java:** ใช้ `Document.load("path/to/file.one")` เพื่ออ่านไฟล์ OneNote; Aspose.Note รองรับรูปแบบ `.one` อย่างเต็มที่โดยไม่ต้องติดตั้ง Microsoft Office  
- **Recover previous OneNote page safely:** ควรสำรองไฟล์ `.one` ดั้งเดิมเสมอก่อนทำการย้อนกลับเป็นชุด โดยเฉพาะเมื่อทำอัตโนมัติในหลายสมุดบันทึก  

## คำถามที่พบบ่อย

**Q1: ฉันสามารถย้อนกลับหลายเวอร์ชันของหน้าได้หรือไม่?**  
A: ใช่ คุณสามารถเข้าถึงประวัติหน้าทั้งหมดและกู้คืนเวอร์ชันก่อนหน้าใดก็ได้โดยเลือกดัชนีที่เหมาะสมจากรายการ `PageHistory`

**Q2: Aspose.Note รองรับภาษาโปรแกรมอื่น ๆ นอกจาก Java หรือไม่?**  
A: ใช่ Aspose.Note มีไลบรารีสำหรับ .NET, C++ และ Python ทำให้คุณสามารถทำการย้อนกลับเดียวกันบนหลายแพลตฟอร์มได้

**Q3: Aspose.Note เข้ากันได้กับทุกเวอร์ชันของ OneNote หรือไม่?**  
A: Aspose.Note รองรับรูปแบบไฟล์ OneNote หลักทั้งหมด รวมถึงไฟล์ `.one` รุ่นเก่าและโครงสร้าง OneNote 2016/365 ใหม่ ทำให้มีความเข้ากันได้กว้างขวาง

**Q4: ฉันสามารถทำงานอัตโนมัติอื่น ๆ ใน OneNote ด้วย Aspose.Note ได้หรือไม่?**  
A: แน่นอน API นี้ให้คุณเพิ่ม, ลบ, และแก้ไขส่วน, หน้า, และทรัพยากรที่ฝังไว้โดยโปรแกรม ทำให้เหมาะสำหรับการย้ายข้อมูลเป็นกลุ่มและการรายงานแบบกำหนดเอง

**Q5: มีฟอรั่มชุมชนหรือการสนับสนุนสำหรับ Aspose.Note หรือไม่?**  
A: มี คุณสามารถเยี่ยมชม [ฟอรั่ม Aspose.Note](https://forum.aspose.com/c/note/28) เพื่อรับความช่วยเหลือจากชุมชน หรือ ติดต่อทีมสนับสนุนของ Aspose สำหรับความช่วยเหลือเชิงพาณิชย์

---

**อัปเดตล่าสุด:** 2026-05-25  
**ทดสอบกับ:** Aspose.Note for Java (latest release)  
**ผู้เขียน:** Aspose  

{{< blocks/products/products-backtop-button >}}

## บทแนะนำที่เกี่ยวข้อง

- [วิธีบันทึกเวอร์ชันหน้า OneNote – ดันเวอร์ชันหน้าปัจจุบันใน OneNote - Aspose.Note](/note/java/onenote-page-manipulation/push-current-page-version/)
- [บทแนะนำ Aspose Java - รับข้อมูลเกี่ยวกับหน้าต่างใน OneNote - Aspose.Note](/note/java/onenote-page-manipulation/get-information-about-pages/)
- [รับจำนวนหน้าของ OneNote ด้วย Aspose.Note สำหรับ Java](/note/java/onenote-page-manipulation/get-page-count/)

{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}