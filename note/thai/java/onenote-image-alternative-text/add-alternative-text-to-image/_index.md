---
date: 2025-12-23
description: เรียนรู้วิธีเพิ่มข้อความแทนรูปภาพในเอกสาร OneNote ด้วย Java และ Aspose.Note
  คู่มือนี้แสดงวิธีเพิ่มข้อความแทนรูปภาพเพื่อการเข้าถึงที่ดียิ่งขึ้น.
linktitle: How to Add Alt Text to Image in OneNote using Java
second_title: Aspose.Note Java API
title: วิธีเพิ่มข้อความอธิบายภาพให้กับรูปใน OneNote ด้วย Java
url: /th/java/onenote-image-alternative-text/add-alternative-text-to-image/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# วิธีเพิ่มข้อความ Alt ให้กับรูปภาพใน OneNote ด้วย Java

## Introduction

ในบทแนะนำนี้ คุณจะได้เรียนรู้ **วิธีเพิ่มข้อความ alt** ให้กับรูปภาพในเอกสาร OneNote ด้วย Java และ Aspose.Note API การเพิ่มข้อความอธิบาย (alt text) จะช่วยเพิ่มความสามารถในการเข้าถึงสำหรับผู้ใช้ที่ใช้โปรแกรมอ่านหน้าจอ และทำให้เนื้อหาของคุณเป็นมิตรต่อผู้ใช้มากยิ่งขึ้น เมื่ออ่านคู่มือนี้จนจบ คุณจะสามารถตั้งค่า alt text ให้กับรูปภาพใน Java ได้ ทำให้ไฟล์ OneNote ของคุณสอดคล้องกับมาตรฐานการเข้าถึงมากขึ้น

## Quick Answers
- **ต้องใช้ไลบรารีอะไร?** Aspose.Note for Java  
- **คีย์เวิร์ดหลักของบทแนะนำนี้คืออะไร?** how to add alt  
- **ต้องมีลิขสิทธิ์สำหรับการใช้งานในผลิตภัณฑ์หรือไม่?** ใช่ จำเป็นต้องมีลิขสิทธิ์เชิงพาณิชย์ (มีรุ่นทดลองฟรี)  
- **สามารถเพิ่มข้อความ alt ให้หลายรูปได้หรือไม่?** แน่นอน – เพียงทำซ้ำขั้นตอนสำหรับแต่ละรูปภาพ  
- **รองรับเวอร์ชัน Java ใด?** Java 8 หรือสูงกว่า

## What is “how to add alt” in the context of OneNote?

การเพิ่มข้อความ alt หมายถึงการให้คำอธิบายเป็นข้อความสำหรับรูปภาพที่โปรแกรมช่วยเหลือสามารถอ่านได้ คำอธิบายนี้ช่วยให้ผู้ใช้ที่ไม่สามารถมองเห็นรูปภาพเข้าใจวัตถุประสงค์ของรูปได้

## Why add alt text to images in OneNote?

- **Accessibility:** ปฏิบัติตามแนวทาง WCAG และปรับปรุงประสบการณ์สำหรับผู้ใช้ที่มีปัญหาการมองเห็น  
- **Searchability:** เครื่องมือค้นหาสามารถทำดัชนีคำอธิบายได้ ทำให้เนื้อหาของคุณค้นหาได้ง่ายขึ้น  
- **Professionalism:** แสดงถึงความมุ่งมั่นในการออกแบบที่ครอบคลุมทุกคน

## Prerequisites

ก่อนเริ่มทำตามบทแนะนำ โปรดตรวจสอบว่าคุณมีสิ่งต่อไปนี้พร้อมแล้ว:

1. Java Development Kit (JDK) – เวอร์ชัน 8 หรือใหม่กว่า  
2. Aspose.Note for Java Library – ดาวน์โหลดได้จาก [ที่นี่](https://releases.aspose.com/note/java/)  
3. IDE เช่น IntelliJ IDEA หรือ Eclipse  
4. ความรู้พื้นฐานด้านการเขียนโปรแกรม Java

## Import Packages

เริ่มต้นด้วยการนำเข้าแพ็กเกจที่จำเป็นในโปรเจกต์ Java ของคุณเพื่อใช้ฟังก์ชันของ Aspose.Note

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Image;
import com.aspose.note.Page;
```

ต่อไปนี้เป็นขั้นตอนแบบเป็นขั้นเป็นตอนสำหรับการเพิ่ม **alternative text image** ลงในเอกสาร OneNote ด้วย Java และ Aspose.Note

## How to Add Alt Text to Images in OneNote using Java

### Step 1: Set Up Document Directory

```java
String dataDir = "Your Document Directory";
```

แทนที่ `"Your Document Directory"` ด้วยเส้นทางไปยังโฟลเดอร์ที่เก็บรูปต้นฉบับและที่ต้องการบันทึกไฟล์ผลลัพธ์

### Step 2: Create a Document Object

```java
Document document = new Document();
```

โค้ดนี้จะสร้างอ็อบเจ็กต์เอกสาร OneNote ใหม่ที่ยังว่างเปล่า

### Step 3: Create a Page Object

```java
Page page = new Page();
```

สร้างหน้า (Page) ที่จะใช้เป็นที่โฮสต์รูปภาพที่เรากำลังจะเพิ่ม

### Step 4: Add an Image to the Page

```java
Image image = new Image(null, dataDir + "image.jpg");
```

คอนสตรัคเตอร์ `Image` จะโหลดไฟล์รูปจากเส้นทางที่ระบุ

### Step 5: Set Alternative Text Title

```java
image.setAlternativeTextTitle("ImageAlternativeText Title");
```

ที่นี่เราจะ **เพิ่มข้อความ alt** ที่ทำหน้าที่เป็นชื่อสั้น ๆ สำหรับรูปภาพ

### Step 6: Set Alternative Text Description

```java
image.setAlternativeTextDescription("ImageAlternativeText Description");
```

คำอธิบายนี้ให้รายละเอียดเพิ่มเติม – เหมาะสำหรับโปรแกรมอ่านหน้าจอ

### Step 7: Append Image to the Page

```java
page.appendChildLast(image);
```

รูปภาพ (พร้อมข้อความ alt) จะถูกเพิ่มลงในหน้า

### Step 8: Append Page to the Document

```java
document.appendChildLast(page);
```

แนบหน้าเข้ากับเอกสาร OneNote

### Step 9: Save Document

```java
document.save(dataDir + "AlternativeText_out.one");
```

บันทึกเอกสารพร้อมข้อความ alt ที่ฝังอยู่ในรูปภาพ

## Common Issues and Solutions

- **FileNotFoundException:** ตรวจสอบให้แน่ใจว่า `dataDir` ชี้ไปยังโฟลเดอร์ที่ถูกต้องและไฟล์ `image.jpg` มีอยู่จริง  
- **NullPointerException on image:** ยืนยันว่าเส้นทางรูปภาพถูกต้องและไฟล์ไม่เสียหาย  
- **License errors:** ใช้ไฟล์ลิขสิทธิ์ Aspose.Note ที่ถูกต้องหรือรันในโหมดทดลองเพื่อประเมินผล

## Frequently Asked Questions

**Q: สามารถเพิ่มข้อความ alt ให้หลายรูปในเอกสารเดียวได้หรือไม่?**  
A: ได้ เพียงทำซ้ำขั้นตอนที่ 4‑6 สำหรับแต่ละรูปที่ต้องการอธิบาย

**Q: รองรับรูปแบบไฟล์ภาพใดบ้างสำหรับการเพิ่มข้อความ alt?**  
A: Aspose.Note รองรับ JPEG, PNG, GIF, BMP และรูปแบบทั่วไปอื่น ๆ อีกหลายประเภท

**Q: สามารถแก้ไขหรือเอาข้อความ alt ออกหลังจากตั้งค่าแล้วได้หรือไม่?**  
A: แน่นอน เรียก `setAlternativeTextTitle("")` หรือ `setAlternativeTextDescription("")` เพื่อเคลียร์ค่า หรือส่งสตริงใหม่เพื่ออัปเดต

**Q: Aspose.Note มี API สำหรับภาษาอื่นนอกจาก Java หรือไม่?**  
A: มี ไลบรารีนี้ยังมีให้ใช้กับ .NET, C++ และ Python

**Q: จะดาวน์โหลดรุ่นทดลองของ Aspose.Note ได้จากที่ไหน?**  
A: คุณสามารถรับรุ่นทดลองฟรีจาก [ที่นี่](https://releases.aspose.com/)

## Conclusion

โดยทำตามคู่มือขั้นตอนนี้ คุณได้เรียนรู้ **วิธีเพิ่มข้อความ alt** ให้กับรูปภาพใน OneNote ด้วย Java การใช้ `add alternative text image` ไม่เพียงทำให้เอกสารของคุณเข้าถึงได้ง่ายขึ้น แต่ยังช่วยให้ค้นหาได้ง่ายและคุณภาพโดยรวมดีขึ้น อย่าลังเลที่จะทดลองใช้ชื่อและคำอธิบายที่แตกต่างกันเพื่อสื่อความหมายของแต่ละรูปให้ชัดเจนที่สุด

---

**Last Updated:** 2025-12-23  
**Tested With:** Aspose.Note for Java 24.11  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}