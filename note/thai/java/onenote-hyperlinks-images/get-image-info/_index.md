---
title: รับข้อมูลรูปภาพจาก OneNote โดยใช้ Java
linktitle: รับข้อมูลรูปภาพจาก OneNote โดยใช้ Java
second_title: Aspose.Note Java API
description: แยกข้อมูลรูปภาพจากเอกสาร OneNote ใน Java! ดูขนาดรูปภาพ ชื่อไฟล์ และอื่นๆ รวมขั้นตอนง่ายๆ และตัวอย่างโค้ด #OneNote #Java #Aspose
weight: 15
url: /th/java/onenote-hyperlinks-images/get-image-info/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# รับข้อมูลรูปภาพจาก OneNote โดยใช้ Java

## การแนะนำ

ในขอบเขตของการพัฒนา Java การดึงข้อมูลจากรูปแบบเอกสารต่างๆ ถือเป็นงานทั่วไป OneNote ซึ่งเป็นแพลตฟอร์มยอดนิยมสำหรับการจดบันทึก มักประกอบด้วยรูปภาพข้างข้อความ การดึงข้อมูลรูปภาพโดยทางโปรแกรมจากไฟล์ OneNote โดยใช้ Java สามารถปรับปรุงเวิร์กโฟลว์การประมวลผลเอกสารได้ ในบทช่วยสอนนี้ เราจะเจาะลึกวิธีการแยกรายละเอียดรูปภาพจากเอกสาร OneNote โดยใช้ Aspose.Note สำหรับ Java

## ข้อกำหนดเบื้องต้น

ก่อนที่เราจะเจาะลึกการนำไปปฏิบัติ ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:

### 1. ชุดพัฒนาจาวา (JDK)

ตรวจสอบให้แน่ใจว่าคุณได้ติดตั้ง Java Development Kit (JDK) บนระบบของคุณแล้ว คุณสามารถดาวน์โหลดและติดตั้ง JDK ล่าสุดได้จาก[เว็บไซต์ออราเคิล](https://www.oracle.com/java/technologies/javase-jdk15-downloads.html).

### 2. Aspose.Note สำหรับไลบรารี Java

 ดาวน์โหลดและรวมไลบรารี Aspose.Note สำหรับ Java ในโปรเจ็กต์ของคุณ คุณสามารถขอรับห้องสมุดได้จาก[หน้าดาวน์โหลด](https://releases.aspose.com/note/java/).

### 3. เอกสาร OneNote

เตรียมเอกสาร OneNote ตัวอย่างที่มีรูปภาพ เอกสารนี้จะใช้เพื่อแยกข้อมูลรูปภาพโดยทางโปรแกรม

## แพ็คเกจนำเข้า

ในการเริ่มต้น ให้นำเข้าแพ็คเกจที่จำเป็นจาก Aspose.Note สำหรับ Java:

```java
import java.io.IOException;
import java.util.List;
import com.aspose.note.Document;
import com.aspose.note.Image;
```

มาแบ่งโค้ดด้านบนออกเป็นคำแนะนำทีละขั้นตอน:

## ขั้นตอนที่ 1: ตั้งค่าไดเรกทอรีเอกสาร

```java
String dataDir = "Your Document Directory";
```

 แทนที่`"Your Document Directory"` พร้อมเส้นทางไปยังเอกสาร OneNote ของคุณ

## ขั้นตอนที่ 2: โหลดเอกสาร

```java
Document doc = new Document(dataDir + "Sample1.one");
```

โหลดเอกสาร OneNote โดยใช้ Aspose.Note สำหรับไลบรารี Java ตรวจสอบให้แน่ใจว่าคุณได้ระบุเส้นทางที่ถูกต้องไปยังเอกสารของคุณ

## ขั้นตอนที่ 3: รับรูปภาพทั้งหมด

```java
List<Image> list = doc.getChildNodes(Image.class);
```

ดึงรูปภาพทั้งหมดจากเอกสาร OneNote ที่โหลด

## ขั้นตอนที่ 4: พิมพ์จำนวนรูปภาพทั้งหมด

```java
System.out.printf("Total Images: %s\n\n", list.size());
```

พิมพ์จำนวนรูปภาพทั้งหมดที่พบในเอกสาร

## ขั้นตอนที่ 5: การสำรวจและพิมพ์ข้อมูลรูปภาพ

```java
for (Image image : list) {
    System.out.println("Width: " + image.getWidth());
    System.out.println("Height: " + image.getHeight());
    System.out.println("OriginalWidth: " + image.getOriginalWidth());
    System.out.println("OriginalHeight: " + image.getOriginalHeight());
    System.out.println("FileName: " + image.getFileName());
    System.out.println("LastModifiedTime: " + image.getLastModifiedTime());
    System.out.println();
}
```

วนซ้ำรายการรูปภาพและรายละเอียดการพิมพ์ เช่น ความกว้าง ความสูง ขนาดดั้งเดิม ชื่อไฟล์ และเวลาที่แก้ไขล่าสุดสำหรับแต่ละรูปภาพ

## บทสรุป

ด้วยการทำตามขั้นตอนที่ระบุไว้ในบทช่วยสอนนี้ คุณสามารถดึงข้อมูลรูปภาพจากเอกสาร OneNote ได้อย่างมีประสิทธิภาพโดยใช้ Java ด้วยความช่วยเหลือของ Aspose.Note สำหรับไลบรารี Java การรวมฟังก์ชันการทำงานนี้เข้ากับแอปพลิเคชันของคุณสามารถทำให้งานที่เกี่ยวข้องกับการประมวลผลเอกสารเป็นอัตโนมัติ เพิ่มประสิทธิภาพและประสิทธิผล

## คำถามที่พบบ่อย

### คำถามที่ 1: Aspose.Note for Java สามารถจัดการรูปแบบเอกสารอื่นๆ นอกเหนือจาก OneNote ได้หรือไม่

ตอบ 1: ใช่ Aspose.Note สำหรับ Java รองรับรูปแบบเอกสารที่หลากหลาย รวมถึง OneNote, PDF และ Microsoft Word

### คำถามที่ 2: Aspose.Note สำหรับ Java เหมาะสำหรับการใช้งานส่วนตัวและเชิงพาณิชย์หรือไม่

ตอบ 2: ได้ คุณสามารถใช้ Aspose.Note สำหรับ Java เพื่อวัตถุประสงค์ส่วนตัวและเชิงพาณิชย์ได้

### คำถามที่ 3: Aspose.Note สำหรับ Java มีการสนับสนุนทางเทคนิคหรือไม่

 A3: ใช่ การสนับสนุนทางเทคนิคมีอยู่ในฟอรัม Aspose ที่[ที่นี่](https://forum.aspose.com/c/note/28).

### คำถามที่ 4: ฉันสามารถลองใช้ Aspose.Note สำหรับ Java ก่อนตัดสินใจซื้อได้หรือไม่

 ตอบ 4: ได้ คุณสามารถสำรวจ Aspose.Note สำหรับ Java เวอร์ชันทดลองใช้ฟรีได้[Aspose.Note สำหรับ Java](https://releases.aspose.com/note/java/).

### คำถามที่ 5: ฉันจะขอรับใบอนุญาตชั่วคราวสำหรับ Aspose.Note สำหรับ Java ได้อย่างไร
 
 A5: คุณสามารถขอรับใบอนุญาตชั่วคราวได้จาก[ใบอนุญาตชั่วคราว/](https://purchase.aspose.com/temporary-license/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
