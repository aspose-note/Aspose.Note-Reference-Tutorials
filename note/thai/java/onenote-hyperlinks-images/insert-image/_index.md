---
title: แทรกรูปภาพในเอกสาร OneNote ด้วย Java
linktitle: แทรกรูปภาพในเอกสาร OneNote ด้วย Java
second_title: Aspose.Note Java API
description: เรียนรู้วิธีแทรกรูปภาพลงในเอกสาร OneNote โดยใช้ Java กับ Aspose.Note สำหรับไลบรารี Java ปฏิบัติตามคำแนะนำทีละขั้นตอนของเราเพื่อการบูรณาการที่ราบรื่น
type: docs
weight: 16
url: /th/java/onenote-hyperlinks-images/insert-image/
---
## การแนะนำ

ในบทช่วยสอนนี้ เราจะสำรวจวิธีการแทรกรูปภาพลงในเอกสาร OneNote โดยใช้ Java ด้วยความช่วยเหลือของ Aspose.Note สำหรับ Java Aspose.Note for Java เป็นไลบรารีอันทรงพลังที่ช่วยให้นักพัฒนาสามารถทำงานกับไฟล์ Microsoft OneNote โดยทางโปรแกรม ช่วยให้ดำเนินการต่างๆ ได้ เช่น การสร้าง การอ่าน และการจัดการเอกสาร OneNote

## ข้อกำหนดเบื้องต้น

ก่อนที่เราจะเริ่มต้น ตรวจสอบให้แน่ใจว่าคุณได้ตั้งค่าข้อกำหนดเบื้องต้นต่อไปนี้:

### 1. ชุดพัฒนาจาวา (JDK)
ตรวจสอบให้แน่ใจว่าคุณได้ติดตั้ง Java Development Kit (JDK) บนระบบของคุณแล้ว คุณสามารถดาวน์โหลดและติดตั้ง JDK ได้จากเว็บไซต์ Oracle

### 2. Aspose.Note สำหรับไลบรารี Java
 ดาวน์โหลดและตั้งค่าไลบรารี Aspose.Note สำหรับ Java โดยทำตาม[เอกสารประกอบ](https://reference.aspose.com/note/java/).

## แพ็คเกจนำเข้า

เริ่มต้นด้วยการนำเข้าแพ็คเกจที่จำเป็นไปยังโปรเจ็กต์ Java ของคุณ แพ็คเกจเหล่านี้ประกอบด้วยไลบรารี Aspose.Note และการขึ้นต่อกันที่จำเป็นอื่นๆ

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.HorizontalAlignment;
import com.aspose.note.Image;
import com.aspose.note.LoadOptions;
import com.aspose.note.Page;
import com.aspose.note.SaveFormat;
```

แบ่งขั้นตอนการแทรกรูปภาพลงในเอกสาร OneNote ออกเป็นหลายขั้นตอน:

## ขั้นตอนที่ 1: โหลดเอกสาร OneNote

ขั้นแรก ให้โหลดเอกสาร OneNote ที่คุณต้องการแทรกรูปภาพ

```java
LoadOptions options = new LoadOptions();
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Sample1.one", options);
```

## ขั้นตอนที่ 2: รับเพจ

ดึงข้อมูลหน้าในเอกสารที่คุณต้องการแทรกรูปภาพ

```java
Page page = oneFile.getFirstChild();
```

## ขั้นตอนที่ 3: โหลดรูปภาพ

โหลดรูปภาพที่คุณต้องการแทรกลงในเอกสาร OneNote

```java
Image image = new Image(oneFile, dataDir + "Input.jpg");
```

## ขั้นตอนที่ 4: ปรับแต่งคุณสมบัติรูปภาพ (ไม่บังคับ)

หรือคุณสามารถปรับแต่งขนาด ตำแหน่ง และการจัดแนวของรูปภาพได้ตามความต้องการของคุณ

```java
image.setWidth(100);
image.setHeight(100);
image.setVerticalOffset(400);
image.setHorizontalOffset(100);
image.setAlignment(HorizontalAlignment.Right);
```

## ขั้นตอนที่ 5: เพิ่มรูปภาพลงในเพจ

เพิ่มรูปภาพลงในหน้าในเอกสาร OneNote

```java
page.appendChildLast(image);
```

## ขั้นตอนที่ 6: บันทึกเอกสาร

บันทึกเอกสารที่แก้ไข รวมถึงรูปภาพที่แทรก

```java
try {
    oneFile.save(dataDir + "InsertanImage_out.pdf", SaveFormat.Pdf);
} catch (IOException e) {
    e.printStackTrace();
}
```

## บทสรุป

ในบทช่วยสอนนี้ เราได้เรียนรู้วิธีแทรกรูปภาพลงในเอกสาร OneNote โดยใช้ Java ด้วยความช่วยเหลือของ Aspose.Note สำหรับไลบรารี Java ด้วยการทำตามคำแนะนำทีละขั้นตอน คุณสามารถรวมรูปภาพลงในเอกสาร OneNote ของคุณโดยทางโปรแกรมได้อย่างง่ายดาย

## คำถามที่พบบ่อย

### คำถามที่ 1: ฉันสามารถแทรกรูปภาพหลายรูปลงในเอกสาร OneNote เดียวโดยใช้วิธีนี้ได้หรือไม่

A1: ได้ คุณสามารถแทรกรูปภาพหลายรูปลงในเอกสาร OneNote เดียวได้โดยการทำซ้ำขั้นตอนที่อธิบายไว้ในบทช่วยสอนนี้สำหรับแต่ละรูปภาพ

### คำถามที่ 2: Aspose.Note สำหรับ Java เข้ากันได้กับ OneNote ทุกเวอร์ชันหรือไม่

ตอบ 2: Aspose.Note for Java รองรับการทำงานกับไฟล์ OneNote ที่สร้างใน Microsoft OneNote 2010 และเวอร์ชันที่ใหม่กว่า

### คำถามที่ 3: ฉันสามารถแทรกรูปภาพในรูปแบบที่แตกต่างกัน เช่น PNG หรือ GIF ลงในเอกสาร OneNote ได้หรือไม่

ตอบ 3: ใช่ Aspose.Note สำหรับ Java รองรับการแทรกรูปภาพในรูปแบบต่างๆ รวมถึง PNG, JPEG, GIF และอื่นๆ

### คำถามที่ 4: Aspose.Note สำหรับ Java เวอร์ชันทดลองใช้งานมีไว้เพื่อการทดสอบหรือไม่

ตอบ 4: ได้ คุณสามารถดาวน์โหลด Aspose.Note สำหรับ Java เวอร์ชันทดลองใช้ฟรีได้จากเว็บไซต์เพื่อวัตถุประสงค์ในการประเมิน

### คำถามที่ 5: ฉันจะได้รับการสนับสนุนด้านเทคนิคสำหรับ Aspose.Note สำหรับ Java ได้อย่างไร

 A5: คุณสามารถรับการสนับสนุนด้านเทคนิคสำหรับ Aspose.Note สำหรับ Java ได้โดยไปที่[ฟอรั่ม](https://forum.aspose.com/c/note/28) ทุ่มเทให้กับผลิตภัณฑ์ Aspose.Note