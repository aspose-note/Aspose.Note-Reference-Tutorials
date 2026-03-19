---
date: 2026-03-19
description: เรียนรู้วิธีเพิ่มรูปภาพลงใน OneNote ด้วย Java และ Aspose.Note for Java
  รวมถึงวิธีตั้งค่าขนาดรูปภาพใน Java และบันทึก OneNote เป็น PDF.
linktitle: Insert an Image in OneNote Document with Java
second_title: Aspose.Note Java API
title: เพิ่มรูปภาพไปยัง OneNote ด้วย Java
url: /th/java/onenote-hyperlinks-images/insert-image/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# แทรกรูปภาพในเอกสาร OneNote ด้วย Java

## Introduction

ในบทแนะนำนี้คุณจะได้เรียนรู้ **วิธีเพิ่มรูปภาพลงใน OneNote** อย่างโปรแกรมมิ่งโดยใช้ Java และไลบรารี Aspose.Note for Java การฝังรูปภาพในหน้า OneNote มีประโยชน์เมื่อคุณต้องสร้างบันทึกการประชุม รายงานอัตโนมัติ หรือเอกสารที่ผสานข้อความกับข้อมูลภาพโดยรวม เมื่อจบคู่มือคุณจะสามารถโหลดไฟล์ OneNote ที่มีอยู่แล้ว แทรกรูปภาพ ปรับขนาดและตำแหน่งตามต้องการ และแม้กระทั่ง **บันทึก OneNote เป็น PDF** – ทั้งหมดโดยไม่ต้องเปิด UI ของ OneNote

## Quick Answers
- **วิธีที่ง่ายที่สุดในการเพิ่มรูปภาพลงใน OneNote ด้วย Java คืออะไร?**  
  ใช้คลาส `Image` ของ Aspose.Note for Java และเพิ่มลงในหน้า
- **ฉันต้องมีใบอนุญาตสำหรับการใช้งานในโปรดักชันหรือไม่?**  
  ใช่ จำเป็นต้องมีใบอนุญาตเชิงพาณิชย์สำหรับการใช้งานในสภาพแวดล้อมการผลิต
- **ฉันสามารถกำหนดขนาดที่กำหนดเองให้กับรูปภาพได้หรือไม่?**  
  ได้เลย – เรียก `setWidth()` และ `setHeight()` บนวัตถุ `Image`
- **สามารถบันทึกไฟล์ OneNote เป็น PDF หลังจากเพิ่มรูปภาพได้หรือไม่?**  
  ได้, เรียก `save(..., SaveFormat.Pdf)` เพื่อ **บันทึก OneNote เป็น PDF**
- **เวอร์ชัน Java ที่รองรับคืออะไร?**  
  Aspose.Note for Java ทำงานกับ JDK 8 และรุ่นต่อไป

## Why add image to OneNote?

การเพิ่มองค์ประกอบภาพทำให้โน้ตเข้าใจง่ายขึ้นและน่าสนใจมากขึ้น รูปภาพสามารถอธิบายแผนภาพ, ภาพหน้าจอ หรือแผนภูมิต่าง ๆ ที่หากไม่มีภาพจะต้องอธิบายด้วยข้อความยาว ๆ การทำขั้นตอนนี้อัตโนมัติช่วยประหยัดเวลา โดยเฉพาะเมื่อสร้างโน้ตจำนวนมากจากแหล่งข้อมูลต่าง ๆ

## Prerequisites

ก่อนที่เราจะเริ่ม โปรดตรวจสอบว่าคุณมีสิ่งต่อไปนี้พร้อมใช้งาน:

### 1. Java Development Kit (JDK)
ติดตั้ง JDK 8 หรือใหม่กว่า คุณสามารถดาวน์โหลดได้จากเว็บไซต์ของ Oracle หรือใช้การแจกจ่าย OpenJDK

### 2. Aspose.Note for Java Library
ดาวน์โหลดไลบรารี Aspose.Note for Java รุ่นล่าสุดและเพิ่มเข้าไปใน classpath ของโปรเจกต์ คำแนะนำการตั้งค่าโดยละเอียดสามารถดูได้ใน [documentation](https://reference.aspose.com/note/java/)

## Import Packages

เริ่มต้นด้วยการนำเข้าคลาสที่จำเป็น การนำเข้าต่าง ๆ นี้ให้คุณเข้าถึงฟังก์ชันหลักของ Aspose.Note รวมถึงยูทิลิตี้พื้นฐานของ Java

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.HorizontalAlignment;
import com.aspose.note.Image;
import com.aspose.note.LoadOptions;
import com.aspose.note.Page;
import com.aspose.note.SaveFormat;
```

## Step‑by‑Step Guide

ด้านล่างเป็นขั้นตอนสั้น ๆ ที่จัดเป็นลำดับเลขแต่ละขั้นตอนประกอบด้วยคำอธิบายสั้น ๆ ตามด้วยโค้ดที่ต้องคัดลอกใช้

### Step 1: Load the OneNote document

เราจะสร้างอินสแตนซ์ `LoadOptions` (มีประโยชน์สำหรับการปรับแต่งในอนาคต) แล้วเปิดไฟล์ `.one` ที่มีอยู่

```java
LoadOptions options = new LoadOptions();
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Sample1.one", options);
```

### Step 2: Get the target page

เพื่อความง่าย เราจะทำงานกับหน้าแรกของเอกสาร แต่คุณสามารถนำทางไปยังหน้าใดก็ได้ที่ต้องการ

```java
Page page = oneFile.getFirstChild();
```

### Step 3: Load the image you want to embed

สร้างอ็อบเจ็กต์ `Image` โดยส่งอ้างอิงเอกสารและพาธของไฟล์รูปภาพเข้าไป

```java
Image image = new Image(oneFile, dataDir + "Input.jpg");
```

### Step 4: Set image dimensions Java (optional)

หากต้องการให้รูปภาพพอดีกับพื้นที่เฉพาะ ให้ปรับความกว้าง, ความสูง และออฟเซ็ต นี่คือจุดที่คีย์เวิร์ดรอง **set image dimensions java** มีประโยชน์

```java
image.setWidth(100);
image.setHeight(100);
image.setVerticalOffset(400);
image.setHorizontalOffset(100);
image.setAlignment(HorizontalAlignment.Right);
```

### Step 5: Append the image to the page

เมธอด `appendChildLast` จะเพิ่มรูปภาพเป็นองค์ประกอบสุดท้ายบนหน้าที่เลือก

```java
page.appendChildLast(image);
```

### Step 6: Save the document – you can also save OneNote as PDF

สุดท้ายให้บันทึกการเปลี่ยนแปลง ตัวอย่างนี้แสดงการบันทึกไฟล์เป็น PDF เพื่อตอบสนองคีย์เวิร์ดรอง **save onenote as pdf**

```java
try {
    oneFile.save(dataDir + "InsertanImage_out.pdf", SaveFormat.Pdf);
} catch (IOException e) {
    e.printStackTrace();
}
```

## Common Issues and Solutions

| อาการ | สาเหตุที่เป็นไปได้ | วิธีแก้ |
|---------|--------------|-----|
| `FileNotFoundException` เมื่อโหลดรูปภาพ | พาธรูปภาพไม่ถูกต้อง | ตรวจสอบให้แน่ใจว่า `dataDir` และชื่อไฟล์รูปภาพถูกต้อง |
| รูปภาพแสดงบิดเบี้ยว | ตั้งค่าความกว้าง/ความสูงไม่ถูกต้อง | ใช้ขนาดเดิมของรูปภาพหรือคำนวณอัตราส่วนที่เหมาะก่อนเรียก `setWidth`/`setHeight` |
| ผลลัพธ์ PDF ว่างเปล่า | ขาดใบอนุญาตสำหรับ Aspose.Note | ใส่ใบอนุญาตที่ถูกต้องก่อนเรียก `save` |

## Frequently Asked Questions

### Q1: Can I insert multiple images into a single OneNote document using this method?

**A:** ใช่ เพียงทำซ้ำขั้นตอน 3‑5 สำหรับแต่ละรูปภาพที่ต้องการเพิ่ม โดยกำหนดหน้าเดียวกันหรือหน้าต่าง ๆ ตามต้องการ

### Q2: Is Aspose.Note for Java compatible with all versions of OneNote?

**A:** Aspose.Note for Java รองรับไฟล์ OneNote ที่สร้างด้วย Microsoft OneNote 2010 และรุ่นต่อ ๆ ไป

### Q3: Can I insert images of different formats, such as PNG or GIF, into a OneNote document?

**A:** แน่นอน ไลบรารีรองรับ PNG, JPEG, GIF, BMP และรูปแบบทั่วไปอื่น ๆ อีกหลายประเภท

### Q4: Is there a trial version of Aspose.Note for Java available for testing purposes?

**A:** มี คุณสามารถดาวน์โหลดเวอร์ชันทดลองฟรีจากเว็บไซต์ Aspose เพื่อประเมิน API ก่อนตัดสินใจซื้อ

### Q5: How can I get technical support for Aspose.Note for Java?

**A:** คุณสามารถขอความช่วยเหลือได้โดยไปที่ [forum](https://forum.aspose.com/c/note/28) ที่ทุ่มเทให้กับผลิตภัณฑ์ Aspose.Note

## Conclusion

ตอนนี้คุณมีตัวอย่างที่ครบถ้วนและพร้อมใช้งานในสภาพแวดล้อมการผลิต ซึ่งแสดง **วิธีเพิ่มรูปภาพลงใน OneNote** ด้วย Java ปรับแต่งลักษณะของรูปภาพได้ตามต้องการ และสามารถ **บันทึก OneNote เป็น PDF** ได้ตามต้องการ ปรับใช้โค้ดนี้ให้เข้ากับเวิร์กโฟลว์ของคุณ ไม่ว่าจะเป็นการสร้างเครื่องมือรายงาน ระบบเอกสารอัตโนมัติ หรือแอปพลิเคชันจดบันทึกแบบกำหนดเอง

---

**Last Updated:** 2026-03-19  
**Tested With:** Aspose.Note for Java 24.10  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}