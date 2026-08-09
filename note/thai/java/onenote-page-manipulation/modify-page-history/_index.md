---
date: 2026-05-31
description: เรียนรู้วิธีแก้ไข page history ของ OneNote, เปลี่ยนชื่อหน้า OneNote,
  และลบ page history ของ OneNote ด้วย Aspose.Note สำหรับ Java.
keywords:
- modify onenote page history
- change onenote page title
- Aspose.Note Java
linktitle: แก้ไข Page History ใน OneNote - Aspise.Note
schemas:
- author: Aspose
  dateModified: '2026-05-31'
  description: Learn how to modify onenote page history, change onenote page title,
    and delete page history onenote using Aspose.Note for Java.
  headline: How to modify onenote page history with Aspose.Note
  type: TechArticle
- description: Learn how to modify onenote page history, change onenote page title,
    and delete page history onenote using Aspose.Note for Java.
  name: How to modify onenote page history with Aspose.Note
  steps:
  - name: Load the OneNote Document
    text: '`Document` loads a OneNote file into memory and provides access to its
      pages and history.'
  - name: Retrieve the First Page and Its History
    text: '`PageHistory` is the Aspose.Note class that stores a notebook’s revision
      list. It offers methods to query, add, or remove historic pages.'
  - name: Delete a Range of History Items
    text: '`removeRange(int start, int count)` removes a consecutive block of history
      entries starting at the specified index.'
  - name: Replace a History Item
    text: '`set_Item(int index, Page page)` replaces the history entry at the given
      position with a new `Page` object.'
  - name: Change the Title of a History Page
    text: '`setTitle(String title)` updates the title of a historic `Page` instance.'
  - name: Add a New History Entry
    text: '`addItem(Page page)` appends a new page to the end of the history collection.'
  - name: Insert a Page at a Specific Position
    text: '`insertItem(int index, Page page)` inserts a page at the specified index,
      shifting subsequent items forward.'
  - name: Save the Modified Notebook
    text: '`save(String path)` writes the updated notebook to the given file location.'
  type: HowTo
- questions:
  - answer: Yes, Aspose.Note for Java integrates seamlessly with Spring, Hibernate,
      Android, and other Java ecosystems.
    question: Can I use Aspose.Note for Java with other Java frameworks?
  - answer: Absolutely—Aspose.Note supports both legacy OneNote 2007 files and the
      modern OneNote 2016/Online formats.
    question: Is Aspose.Note for Java compatible with different versions of OneNote
      files?
  - answer: No, the library is self‑contained; you only need the core JAR and a Java
      runtime.
    question: Does Aspose.Note for Java require any additional dependencies?
  - answer: Yes, you can loop through a directory of `.one` files and apply the same
      history‑editing logic to each notebook.
    question: Can I perform bulk modifications on multiple OneNote files simultaneously?
  - answer: Yes, you can visit the [Aspose.Note forum](https://forum.aspose.com/c/note/28)
      for assistance and to share examples.
    question: Is there a community forum for Aspose.Note for Java where I can ask
      for help?
  type: FAQPage
second_title: Aspose.Note Java API
title: วิธีแก้ไข page history ของ OneNote ด้วย Aspose.Note
url: /th/java/onenote-page-manipulation/modify-page-history/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# วิธีแก้ไขประวัติเพจ OneNote ด้วย Aspose.Note

ในบทแนะนำนี้คุณจะได้เรียนรู้ **วิธีแก้ไขประวัติเพจ OneNote** อย่างเป็นขั้นตอนโดยใช้ Aspose.Note for Java API ไม่ว่าคุณจะต้องการลบการแก้ไขเก่า, เปลี่ยนชื่อเพจในประวัติ, หรือแทรกรายการใหม่ คู่มือนี้จะพาคุณผ่านกระบวนการที่พร้อมใช้งานในระดับการผลิตและทำงานกับสมุดบันทึก OneNote ใดก็ได้

## คำตอบด่วน
- **ประวัติเพจหมายถึงอะไรใน OneNote?**  
  เป็นการรวบรวมเวอร์ชันของเพจก่อนหน้าที่เก็บไว้ในไฟล์ OneNote
- **ฉันสามารถลบรายการประวัติเฉพาะได้หรือไม่?**  
  ได้, ใช้เมธอด `removeRange` หรือ `removeItem` บนวัตถุ `PageHistory`
- **การเปลี่ยนชื่อเพจเป็นส่วนหนึ่งของการจัดการประวัติหรือไม่?**  
  แน่นอน—แต่ละรายการประวัติมีชื่อของตนเองที่คุณสามารถแก้ไขได้
- **ฉันต้องการใบอนุญาตเพื่อรันโค้ดนี้หรือไม่?**  
  ใบอนุญาตทดลองใช้ชั่วคราวสามารถใช้สำหรับการทดสอบได้; จำเป็นต้องมีใบอนุญาตเต็มรูปแบบสำหรับการใช้งานจริง
- **เวอร์ชัน Java ใดที่รองรับ?**  
  Aspose.Note for Java รองรับ JDK 8 และรุ่นต่อไป

## การแก้ไขประวัติเพจ OneNote คืออะไร?
*Modify onenote page history* หมายถึงการแก้ไข, เพิ่ม หรือ ลบรายการในรายการแก้ไขภายในของสมุดบันทึก OneNote อย่างโปรแกรมมิ่ง ซึ่งช่วยให้คุณเก็บเฉพาะเวอร์ชันที่เกี่ยวข้อง, เปลี่ยนชื่อประวัติ, และปรับขนาดสมุดบันทึกให้เหมาะสมขณะลดขนาดไฟล์โดยรวม

## ทำไมต้องแก้ไขประวัติเพจ OneNote?
การแก้ไขประวัติเพจสามารถปรับปรุงการจัดการสมุดบันทึกและประสิทธิภาพได้อย่างมาก โดยการตัดทอนการแก้ไขที่ไม่ได้ใช้คุณจะทำให้ไฟล์มีขนาดเล็กลง, โหลดเร็วขึ้น, และทำให้การนำทางสอดคล้องกันมากขึ้นสำหรับผู้ใช้ สิ่งเหล่านี้จะเห็นได้ชัดในสมุดบันทึกขนาดใหญ่ที่มีหลายร้อยหน้า

Aspose.Note รองรับ **50+ รูปแบบการนำเข้าและส่งออก** และสามารถประมวลผลสมุดบันทึกที่มี **สูงสุด 10,000 หน้า** โดยไม่ต้องโหลดไฟล์ทั้งหมดเข้าสู่หน่วยความจำ, ทำให้การดำเนินการมีประสิทธิภาพสูง

## ข้อกำหนดเบื้องต้น

1. **Java Development Kit (JDK)** – JDK 8 หรือใหม่กว่า ติดตั้งบนเครื่องของคุณ  
2. **Aspose.Note for Java library** – ดาวน์โหลดจาก [download page](https://releases.aspose.com/note/java/)  
3. **A sample OneNote document** – เช่น `Sample1.one` ที่คุณสามารถแก้ไขได้อย่างปลอดภัย

## นำเข้าแพ็กเกจ

คลาสต่อไปนี้จำเป็น: `Document` แทนสมุดบันทึกทั้งหมด, `Page` แทนหน้าเดี่ยว, และ `PageHistory` จัดการคอลเลกชันของหน้าในประวัติ

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.PageHistory;
```

## วิธีแก้ไขประวัติเพจ OneNote?

โหลดสมุดบันทึก, ดึงคอลเลกชัน `PageHistory` ของมัน, แล้วใช้เมธอดที่ให้มาเพื่อลบ, แทนที่, หรือแทรกรายการ การดำเนินการทั้งหมดทำในหน่วยความจำและคุณเพียงเรียก `save` ครั้งเดียวที่จบเพื่อบันทึกการเปลี่ยนแปลง

### ขั้นตอนที่ 1: โหลดเอกสาร OneNote

`Document` โหลดไฟล์ OneNote เข้าหน่วยความจำและให้เข้าถึงหน้าต่าง ๆ และประวัติของมัน

```java
String dataDir = "Your Document Directory";
Document document = new Document(dataDir + "Sample1.one");
```

### ขั้นตอนที่ 2: ดึงเพจแรกและประวัติของมัน

`PageHistory` เป็นคลาสของ Aspose.Note ที่เก็บรายการแก้ไขของสมุดบันทึก มันมีเมธอดสำหรับสอบถาม, เพิ่ม, หรือลบหน้าในประวัติ

```java
Page page = document.getFirstChild();
PageHistory pageHistory = document.getPageHistory(page);
```

### ขั้นตอนที่ 3: ลบช่วงของรายการประวัติ

`removeRange(int start, int count)` ลบบล็อกต่อเนื่องของรายการประวัติที่เริ่มจากตำแหน่งที่ระบุ

```java
pageHistory.removeRange(0, 1);
```

### ขั้นตอนที่ 4: แทนที่รายการประวัติ

`set_Item(int index, Page page)` แทนที่รายการประวัติที่ตำแหน่งที่กำหนดด้วยอ็อบเจกต์ `Page` ใหม่

```java
pageHistory.set_Item(0, new Page());
```

### ขั้นตอนที่ 5: เปลี่ยนชื่อของเพจในประวัติ

`setTitle(String title)` อัปเดตชื่อของอินสแตนซ์ `Page` ในประวัติ

```java
pageHistory.get_Item(1).getTitle().getTitleText().clear().append("New Title");
```

### ขั้นตอนที่ 6: เพิ่มรายการประวัติใหม่

`addItem(Page page)` เพิ่มหน้าใหม่ต่อท้ายคอลเลกชันประวัติ

```java
pageHistory.addItem(new Page());
```

### ขั้นตอนที่ 7: แทรกเพจในตำแหน่งที่กำหนด

`insertItem(int index, Page page)` แทรกหน้าในตำแหน่งที่ระบุ, ทำให้รายการต่อจากนั้นเลื่อนตำแหน่งไปข้างหน้า

```java
pageHistory.insertItem(1, new Page());
```

### ขั้นตอนที่ 8: บันทึกสมุดบันทึกที่แก้ไขแล้ว

`save(String path)` เขียนสมุดบันทึกที่อัปเดตไปยังตำแหน่งไฟล์ที่กำหนด

```java
document.save(dataDir + "ModifyPageHistory_out.one");
```

## ข้อผิดพลาดทั่วไป & เคล็ดลับ

- **Index out of bounds:** ตรวจสอบขนาดของคอลเลกชันก่อนเรียก `removeRange` หรือ `insertItem` เสมอ  
- **Null titles:** บางหน้าในประวัติอาจไม่มีชื่อ; ตรวจสอบ `null` ก่อนเรียก `getTitle()`  
- **Saving location:** ตรวจสอบให้แน่ใจว่าเส้นทางผลลัพธ์ (`ModifyPageHistory_out.one`) สามารถเขียนได้; หากไม่เช่นนั้นจะเกิด `IOException`  
- **Performance tip:** เมื่อทำงานกับสมุดบันทึกขนาดใหญ่มาก, เรียก `document.setLoadOptions(new LoadOptions(LoadFormat.OneNote))` เพื่อเปิดใช้งานการโหลดแบบ lazy และลดการใช้หน่วยความจำ

## คำถามที่พบบ่อย

**Q: ฉันสามารถใช้ Aspose.Note for Java กับเฟรมเวิร์ก Java อื่น ๆ ได้หรือไม่?**  
A: ใช่, Aspose.Note for Java ผสานรวมอย่างราบรื่นกับ Spring, Hibernate, Android และระบบนิเวศ Java อื่น ๆ  

**Q: Aspose.Note for Java รองรับไฟล์ OneNote เวอร์ชันต่าง ๆ หรือไม่?**  
A: แน่นอน—Aspose.Note รองรับไฟล์ OneNote 2007 รุ่นเก่าและรูปแบบ OneNote 2016/Online สมัยใหม่  

**Q: Aspose.Note for Java ต้องการ dependencies เพิ่มเติมหรือไม่?**  
A: ไม่, ไลบรารีเป็นอิสระ; คุณต้องการเพียง JAR หลักและ Java runtime  

**Q: ฉันสามารถทำการแก้ไขเป็นกลุ่มบนไฟล์ OneNote หลายไฟล์พร้อมกันได้หรือไม่?**  
A: ใช่, คุณสามารถวนลูปผ่านไดเรกทอรีของไฟล์ `.one` และใช้ตรรกะการแก้ไขประวัติเช่นเดียวกันกับแต่ละสมุดบันทึก  

**Q: มีฟอรั่มชุมชนสำหรับ Aspose.Note for Java ที่ฉันสามารถขอความช่วยเหลือได้หรือไม่?**  
A: ใช่, คุณสามารถเยี่ยมชม [Aspose.Note forum](https://forum.aspose.com/c/note/28) เพื่อขอความช่วยเหลือและแบ่งปันตัวอย่าง  

---

**อัปเดตล่าสุด:** 2026-05-31  
**ทดสอบกับ:** Aspose.Note for Java 24.11 (latest at time of writing)  
**ผู้เขียน:** Aspose  

{{< blocks/products/products-backtop-button >}}

## บทแนะนำที่เกี่ยวข้อง

- [บทแนะนำการแก้ไขหน้า aspose.note – รับประวัติเพจใน OneNote](/note/java/onenote-page-manipulation/get-page-revisions/)
- [วิธีบันทึกเวอร์ชันเพจ OneNote – ผลักดันเวอร์ชันเพจปัจจุบันใน OneNote - Aspose.Note](/note/java/onenote-page-manipulation/push-current-page-version/)
- [ติดตามการเปลี่ยนแปลง onenote – จัดการประวัติเพจด้วย Aspose.Note](/note/java/onenote-page-manipulation/working-with-page-revisions/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}