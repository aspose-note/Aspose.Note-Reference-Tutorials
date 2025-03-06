---
title: พุชเวอร์ชันหน้าปัจจุบันใน OneNote - Aspose.Note
linktitle: พุชเวอร์ชันหน้าปัจจุบันใน OneNote - Aspose.Note
second_title: Aspose.Note Java API
description: ทำให้เนื้อหา OneNote ใหม่อยู่เสมอ! เรียนรู้การอัปเดตประวัติหน้าและจัดการเวอร์ชัน คำแนะนำทีละขั้นตอน และโค้ดรวมอยู่ด้วย #OneNote #Java #Aspose
weight: 18
url: /th/java/onenote-page-manipulation/push-current-page-version/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# พุชเวอร์ชันหน้าปัจจุบันใน OneNote - Aspose.Note

## การแนะนำ

ในบทช่วยสอนนี้ เราจะสำรวจวิธีใช้ Aspose.Note สำหรับ Java เพื่อพุชเวอร์ชันหน้าปัจจุบันใน OneNote Aspose.Note เป็นไลบรารี Java ที่ทรงพลังซึ่งช่วยให้นักพัฒนาสามารถทำงานกับเอกสาร Microsoft OneNote โดยทางโปรแกรม ทำให้สามารถดำเนินการต่างๆ ได้ เช่น การสร้าง จัดการ และแปลงไฟล์ OneNote

## ข้อกำหนดเบื้องต้น

ก่อนที่เราจะเริ่มต้น ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นดังต่อไปนี้:
1. ความรู้พื้นฐานเกี่ยวกับภาษาการเขียนโปรแกรม Java
2. ติดตั้ง Java Development Kit (JDK) บนระบบของคุณ
3.  Aspose.Note สำหรับไลบรารี Java คุณสามารถดาวน์โหลดได้จาก[ที่นี่](https://releases.aspose.com/note/java/).
4. เอกสาร OneNote ตัวอย่างที่จะใช้งาน

## แพ็คเกจนำเข้า

ขั้นแรก คุณต้องนำเข้าแพ็คเกจที่จำเป็นในโปรเจ็กต์ Java ของคุณเพื่อใช้ฟังก์ชัน Aspose.Note

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.PageHistory;
```

## ขั้นตอนที่ 1: โหลดเอกสาร OneNote

```java
String dataDir = "Your Document Directory";
Document document = new Document(dataDir + "Sample1.one");
```

 ที่นี่,`dataDir` ควรชี้ไปยังไดเร็กทอรีที่มีเอกสาร OneNote ของคุณอยู่ แทนที่`"Sample1.one"` ด้วยชื่อไฟล์ OneNote ของคุณ

## ขั้นตอนที่ 2: รับหน้าปัจจุบันและประวัติของหน้า

```java
Page page = document.getFirstChild();
PageHistory pageHistory = document.getPageHistory(page);
```

 เราดึงหน้าแรกของเอกสารโดยใช้`getFirstChild()` แล้วรับประวัติโดยใช้`getPageHistory()`.

## ขั้นตอนที่ 3: พุชเวอร์ชันหน้าปัจจุบัน

```java
pageHistory.addItem(page.deepClone());
```

ที่นี่ เราเพิ่มเวอร์ชันปัจจุบันของเพจลงในประวัติโดยการโคลนและเพิ่มเป็นรายการใหม่

## ขั้นตอนที่ 4: บันทึกเอกสาร

```java
document.save(dataDir + "PushCurrentPageVersion_out.one");
```

สุดท้าย เราจะบันทึกเอกสารที่แก้ไขพร้อมกับประวัติหน้าที่อัปเดต

## บทสรุป

ในบทช่วยสอนนี้ เราได้เรียนรู้วิธีพุชเวอร์ชันหน้าปัจจุบันใน OneNote โดยใช้ Aspose.Note สำหรับ Java ด้วยการทำตามขั้นตอนเหล่านี้ คุณสามารถจัดการการกำหนดเวอร์ชันของเอกสาร OneNote ของคุณโดยทางโปรแกรมได้อย่างมีประสิทธิภาพ

## คำถามที่พบบ่อย

### คำถามที่ 1: ฉันสามารถใช้ Aspose.Note สำหรับ Java เพื่อทำงานกับไฟล์ OneNote ที่เข้ารหัสได้หรือไม่

ตอบ 1: ใช่ Aspose.Note สำหรับ Java รองรับการทำงานกับไฟล์ OneNote ที่เข้ารหัสและไม่ได้เข้ารหัส

### คำถามที่ 2: Aspose.Note สำหรับ Java เข้ากันได้กับ OneNote เวอร์ชันล่าสุดหรือไม่

ตอบ 2: Aspose.Note สำหรับ Java มุ่งมั่นที่จะรักษาความเข้ากันได้กับเอกสาร OneNote เวอร์ชันล่าสุด

### คำถามที่ 3: ฉันสามารถจัดการข้อความและรูปภาพภายในเอกสาร OneNote โดยใช้ Aspose.Note for Java ได้หรือไม่

ตอบ 3: แน่นอนว่า Aspose.Note สำหรับ Java มีฟังก์ชันการทำงานที่ครอบคลุมสำหรับการจัดการข้อความ รูปภาพ และองค์ประกอบอื่นๆ ภายในไฟล์ OneNote

### คำถามที่ 4: Aspose.Note for Java รองรับการแปลงไฟล์ OneNote เป็นรูปแบบอื่นหรือไม่

ตอบ 4: ใช่ Aspose.Note สำหรับ Java รองรับการแปลงไฟล์ OneNote เป็นรูปแบบต่างๆ เช่น PDF, HTML และรูปแบบรูปภาพ

### คำถามที่ 5: ฉันจะรับการสนับสนุนสำหรับ Aspose.Note สำหรับ Java ได้ที่ไหน หากฉันพบปัญหาใดๆ

 A5: คุณสามารถเยี่ยมชม[ฟอรั่ม Aspose.Note](https://forum.aspose.com/c/note/28) เพื่อขอความช่วยเหลือจากชุมชนหรือติดต่อฝ่ายสนับสนุน Aspose โดยตรง
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
