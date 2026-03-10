---
date: 2025-12-21
description: เรียนรู้วิธีเพิ่มรูปภาพลงในเอกสาร OneNote ด้วย Java และ Aspose.Note for
  Java. ปฏิบัติตามคู่มือขั้นตอนต่อขั้นตอนของเราเพื่อแทรกรูปภาพและบันทึก OneNote เป็น
  PDF ได้ตามต้องการ.
linktitle: Insert an Image in OneNote Document with Java
second_title: Aspose.Note Java API
title: วิธีเพิ่มรูปภาพลงใน OneNote ด้วย Java
url: /th/java/onenote-hyperlinks-images/insert-image/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# แทรกรูปภาพในเอกสาร OneNote ด้วย Java

## คำนำ

ในบทเรียนนี้ เราจะสำรวจวิธีการแทรกรูปภาพลงในเอกสาร OneNote ด้วย Java โดยใช้ Aspose.Note for Java Aspose.Note for Java เป็นไลบรารีที่ทรงพลังซึ่งช่วยให้นักพัฒนาสามารถทำงานกับไฟล์ Microsoft OneNote ผ่านโปรแกรมได้ ทำให้สามารถสร้าง อ่าน และจัดการเอกสาร OneNote ได้หลายรูปแบบ

## คำตอบสั้น
- **วิธีที่ง่ายที่สุดในการเพิ่มรูปภาพลงใน OneNote ด้วย Java คืออะไร?**  
  ใช้คลาส `Image` ของ Aspose.Note for Java และเพิ่มลงในหน้า
- **ต้องมีลิขสิทธิ์สำหรับการใช้งานในสภาพแวดล้อมจริงหรือไม่?**  
  ใช่ จำเป็นต้องมีลิขสิทธิ์เชิงพาณิชย์สำหรับการใช้งานในสภาพแวดล้อมจริง
- **สามารถกำหนดขนาดภาพเองได้หรือไม่?**  
  แน่นอน – เรียก `setWidth()` และ `setHeight()` บนวัตถุ `Image`
- **สามารถบันทึกไฟล์ OneNote เป็น PDF หลังจากเพิ่มภาพได้หรือไม่?**  
  ใช่ เรียก `save(..., SaveFormat.Pdf)` เพื่อ **บันทึก OneNote เป็น PDF**
- **รองรับเวอร์ชัน Java ใด?**  
  Aspose.Note for Java ทำงานกับ JDK 8 ขึ้นไป

## วิธีเพิ่มรูปภาพลงใน OneNote ด้วย Java?

ก่อนจะลงลึกในโค้ด เรามาพูดสั้น ๆ ว่าทำไมคุณอาจต้องการฝังรูปภาพลงใน OneNote ด้วยโปรแกรม ไม่ว่าจะเป็นการสร้างบันทึกการประชุม การสร้างรายงานอัตโนมัติ หรือการสร้างกระบวนการเอกสาร การแทรกรูปภาพช่วยให้โน้ตของคุณมีบริบทภาพที่ข้อความธรรมดาไม่สามารถให้ได้ ด้วย Aspose.Note for Java คุณทำได้ทั้งหมดโดยไม่ต้องเปิด UI ของ OneNote

## ข้อกำหนดเบื้องต้น

ก่อนเริ่ม โปรดตรวจสอบว่าคุณได้เตรียมสิ่งต่อไปนี้เรียบร้อยแล้ว:

### 1. Java Development Kit (JDK)
ตรวจสอบให้แน่ใจว่าคุณได้ติดตั้ง Java Development Kit (JDK) บนระบบของคุณแล้ว คุณสามารถดาวน์โหลดและติดตั้ง JDK จากเว็บไซต์ของ Oracle

### 2. Aspose.Note for Java Library
ดาวน์โหลดและตั้งค่าไลบรารี Aspose.Note for Java ตาม [documentation](https://reference.aspose.com/note/java/)

## นำเข้าแพ็กเกจ

เริ่มต้นด้วยการนำเข้าแพ็กเกจที่จำเป็นเข้าสู่โครงการ Java ของคุณ แพ็กเกจเหล่านี้รวมถึงไลบรารี Aspose.Note และการพึ่งพาอื่น ๆ ที่ต้องใช้

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.HorizontalAlignment;
import com.aspose.note.Image;
import com.aspose.note.LoadOptions;
import com.aspose.note.Page;
import com.aspose.note.SaveFormat;
```

เราจะทำการแยกกระบวนการแทรกรูปภาพลงในเอกสาร OneNote ออกเป็นหลายขั้นตอน:

## ขั้นตอนที่ 1: โหลดเอกสาร OneNote

แรกสุด ให้โหลดเอกสาร OneNote ที่คุณต้องการแทรกรูปภาพ

```java
LoadOptions options = new LoadOptions();
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Sample1.one", options);
```

## ขั้นตอนที่ 2: รับหน้าเอกสาร

ดึงหน้าที่ต้องการในเอกสารเพื่อทำการแทรกรูปภาพ

```java
Page page = oneFile.getFirstChild();
```

## ขั้นตอนที่ 3: โหลดรูปภาพ

โหลดรูปภาพที่คุณต้องการแทรกลงในเอกสาร OneNote

```java
Image image = new Image(oneFile, dataDir + "Input.jpg");
```

## ขั้นตอนที่ 4: ปรับแต่งคุณลักษณะของรูปภาพ (ไม่บังคับ)

หากต้องการ คุณสามารถปรับขนาด ตำแหน่ง และการจัดแนวของรูปภาพตามความต้องการของคุณ นี่คือจุดที่คุณ **ตั้งค่าขนาดรูปภาพในสไตล์ Java**

```java
image.setWidth(100);
image.setHeight(100);
image.setVerticalOffset(400);
image.setHorizontalOffset(100);
image.setAlignment(HorizontalAlignment.Right);
```

## ขั้นตอนที่ 5: เพิ่มรูปภาพลงในหน้า

เพิ่มรูปภาพลงในหน้าที่เลือกในเอกสาร OneNote

```java
page.appendChildLast(image);
```

## ขั้นตอนที่ 6: บันทึกเอกสาร

บันทึกเอกสารที่แก้ไขแล้วรวมถึงรูปภาพที่แทรก คุณยังสามารถ **บันทึก OneNote เป็น PDF** ได้ในขั้นตอนนี้

```java
try {
    oneFile.save(dataDir + "InsertanImage_out.pdf", SaveFormat.Pdf);
} catch (IOException e) {
    e.printStackTrace();
}
```

## สรุป

ในบทเรียนนี้ เราได้เรียนรู้วิธีการแทรกรูปภาพลงในเอกสาร OneNote ด้วย Java โดยใช้ไลบรารี Aspose.Note for Java ด้วยการทำตามขั้นตอนที่อธิบายไว้ คุณสามารถผสานรูปภาพเข้าไปในเอกสาร OneNote ของคุณได้อย่างง่ายดายโดยใช้โค้ด

## คำถามที่พบบ่อย

### Q1: สามารถแทรกรูปภาพหลายรูปลงในเอกสาร OneNote เดียวกันโดยใช้วิธีนี้ได้หรือไม่?

A1: ได้ คุณสามารถแทรกรูปภาพหลายรูปลงในเอกสาร OneNote เดียวกันโดยทำซ้ำขั้นตอนที่อธิบายไว้ในบทเรียนนี้สำหรับแต่ละรูป

### Q2: Aspose.Note for Java รองรับเวอร์ชันของ OneNote ทั้งหมดหรือไม่?

A2: Aspose.Note for Java รองรับการทำงานกับไฟล์ OneNote ที่สร้างใน Microsoft OneNote 2010 และรุ่นต่อ ๆ มา

### Q3: สามารถแทรกรูปภาพในรูปแบบต่าง ๆ เช่น PNG หรือ GIF ลงใน OneNote ได้หรือไม่?

A3: ได้ Aspose.Note for Java รองรับการแทรกรูปภาพในหลายรูปแบบ รวมถึง PNG, JPEG, GIF และอื่น ๆ

### Q4: มีเวอร์ชันทดลองของ Aspose.Note for Java สำหรับการทดสอบหรือไม่?

A4: มี คุณสามารถดาวน์โหลดเวอร์ชันทดลองฟรีของ Aspose.Note for Java จากเว็บไซต์เพื่อการประเมินผล

### Q5: จะขอรับการสนับสนุนทางเทคนิคสำหรับ Aspose.Note for Java ได้อย่างไร?

A5: คุณสามารถขอรับการสนับสนุนทางเทคนิคสำหรับ Aspose.Note for Java ได้โดยไปที่ [forum](https://forum.aspose.com/c/note/28) ที่อุทิศให้กับผลิตภัณฑ์ Aspose.Note

---

**อัปเดตล่าสุด:** 2025-12-21  
**ทดสอบด้วย:** Aspose.Note for Java 24.10  
**ผู้เขียน:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}