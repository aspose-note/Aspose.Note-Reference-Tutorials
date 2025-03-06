---
title: สร้าง Doc และแทรกรูปภาพด้วยสตรีมใน OneNote - Java
linktitle: สร้าง Doc และแทรกรูปภาพด้วยสตรีมใน OneNote - Java
second_title: Aspose.Note Java API
description: เรียนรู้วิธีรวมรูปภาพเข้ากับเอกสาร OneNote ได้อย่างง่ายดายโดยใช้ Aspose.Note for Java บทช่วยสอนทีละขั้นตอนสำหรับนักพัฒนา Java
weight: 13
url: /th/java/onenote-hyperlinks-images/build-doc-insert-image-stream/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# สร้าง Doc และแทรกรูปภาพด้วยสตรีมใน OneNote - Java

## การแนะนำ

ยินดีต้อนรับสู่บทช่วยสอนที่ครอบคลุมของเราเกี่ยวกับการใช้ Aspose.Note สำหรับ Java เพื่อสร้างเอกสารและแทรกรูปภาพโดยใช้สตรีมรูปภาพใน OneNote! ในบทช่วยสอนนี้ เราจะแนะนำคุณตลอดกระบวนการทีละขั้นตอน เพื่อให้มั่นใจว่าคุณมีความเข้าใจที่ชัดเจนในแต่ละขั้นตอน ในตอนท้าย คุณจะสามารถรวมรูปภาพเข้ากับเอกสาร OneNote ของคุณโดยใช้ Java ได้อย่างง่ายดาย

## ข้อกำหนดเบื้องต้น

ก่อนที่เราจะเจาะลึกบทช่วยสอน ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:

### ชุดพัฒนาจาวา (JDK)

ตรวจสอบให้แน่ใจว่าคุณได้ติดตั้ง Java Development Kit (JDK) บนระบบของคุณ คุณสามารถดาวน์โหลดได้จากเว็บไซต์ Oracle

### Aspose.Note สำหรับไลบรารี Java

 ดาวน์โหลดและติดตั้งไลบรารี Aspose.Note สำหรับ Java จากไฟล์ที่ให้มา[ลิงค์](https://releases.aspose.com/note/java/).

### การตั้งค่า IDE

ตั้งค่า Integrated Development Environment (IDE) ของคุณด้วยการกำหนดค่าที่จำเป็นเพื่อทำงานกับโปรเจ็กต์ Java

## แพ็คเกจนำเข้า

ในการเริ่มต้น ให้นำเข้าแพ็คเกจที่จำเป็นลงในโปรเจ็กต์ Java ของคุณ แพคเกจเหล่านี้จะมีฟังก์ชันการทำงานที่จำเป็นในการทำงานกับเอกสารและรูปภาพ OneNote

```java
import java.io.FileInputStream;
import java.io.FileNotFoundException;
import java.io.IOException;
import java.io.InputStream;
import com.aspose.note.Document;
import com.aspose.note.HorizontalAlignment;
import com.aspose.note.Image;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.SaveFormat;
```

## ขั้นตอนที่ 1: ตั้งค่าไดเร็กทอรีเอกสาร

 กำหนดไดเร็กทอรีที่มีเอกสารและรูปภาพของคุณอยู่ แทนที่`"Your Document Directory"` พร้อมเส้นทางไปยังไดเร็กทอรีของคุณ

```java
String dataDir = "Your Document Directory";
```

## ขั้นตอนที่ 2: สร้างวัตถุเอกสาร

 เริ่มต้นอินสแตนซ์ของ`Document` คลาสเพื่อเริ่มทำงานกับเอกสาร OneNote ของคุณ

```java
Document doc = new Document();
```

## ขั้นตอนที่ 3: เริ่มต้นวัตถุหน้า

 สร้างก`Page` วัตถุเพื่อแสดงหน้าภายในเอกสาร

```java
Page page = new Page();
```

## ขั้นตอนที่ 4: สร้างโครงร่าง

 เริ่มต้นอัน`Outline` วัตถุเพื่อจัดโครงสร้างเนื้อหาภายในหน้า

```java
Outline outline1 = new Outline();
outline1.setVerticalOffset(600);
outline1.setHorizontalOffset(0);
```

## ขั้นตอนที่ 5: สร้างองค์ประกอบเค้าร่าง

 สร้าง`OutlineElement` เพื่อเก็บภาพและระบุตำแหน่ง

```java
OutlineElement outlineElem1 = new OutlineElement();
```

## ขั้นตอนที่ 6: โหลดสตรีมรูปภาพ

 โหลดสตรีมภาพโดยใช้ไฟล์`FileInputStream` เพื่อภาพที่ต้องการ

```java
InputStream fs = null;
try {
    fs = new FileInputStream(dataDir + "image.jpg");
} catch (FileNotFoundException e) {
    e.printStackTrace();
}
```

## ขั้นตอนที่ 7: แทรกรูปภาพ

 แทรกรูปภาพลงในเอกสารโดยสร้างไฟล์`Image` วัตถุและการตั้งค่าการจัดตำแหน่ง

```java
Image image = new Image(null, dataDir + "image1.jpg");
image.setAlignment(HorizontalAlignment.Right);
```

## ขั้นตอนที่ 8: ผนวกรูปภาพเข้ากับองค์ประกอบโครงร่าง

เพิ่มรูปภาพต่อท้ายองค์ประกอบโครงร่าง

```java
outlineElem1.appendChildLast(image);
```

## ขั้นตอนที่ 9: ผนวกองค์ประกอบโครงร่างเข้ากับโครงร่าง

เพิ่มองค์ประกอบโครงร่างให้กับโครงร่าง

```java
outline1.appendChildLast(outlineElem1);
```

## ขั้นตอนที่ 10: ผนวกโครงร่างเข้ากับหน้า

เพิ่มโครงร่างลงในหน้า

```java
page.appendChildLast(outline1);
```

## ขั้นตอนที่ 11: ผนวกหน้าเข้ากับเอกสาร

สุดท้าย ให้ผนวกหน้าเข้ากับเอกสาร

```java
doc.appendChildLast(page);
```

## ขั้นตอนที่ 12: บันทึกเอกสาร

บันทึกเอกสารที่แก้ไข โดยระบุรูปแบบที่ต้องการ (เช่น PDF)

```java
try {
    doc.save("D://Aspose_JavaProjects//OneNote//out3.pdf", SaveFormat.Pdf);
} catch (IOException e) {
    e.printStackTrace();
}
```

เมื่อทำตามขั้นตอนเหล่านี้ คุณจะสามารถสร้างเอกสารและแทรกรูปภาพได้อย่างง่ายดายโดยใช้สตรีมรูปภาพใน OneNote โดยใช้ Aspose.Note for Java

## บทสรุป

โดยสรุป การเรียนรู้การรวมรูปภาพลงในเอกสาร OneNote ของคุณโดยใช้ Java สามารถปรับปรุงกระบวนการสร้างเอกสารของคุณได้อย่างมาก ด้วย Aspose.Note สำหรับ Java คุณจะมีเครื่องมืออันทรงพลังเพื่อให้คุณทำงานนี้ให้สำเร็จได้อย่างราบรื่น

## คำถามที่พบบ่อย

### คำถามที่ 1: Aspose.Note สำหรับ Java เข้ากันได้กับ OneNote ทุกเวอร์ชันหรือไม่

ตอบ 1: Aspose.Note for Java รองรับ OneNote เวอร์ชันต่างๆ เพื่อให้มั่นใจถึงความเข้ากันได้ในสภาพแวดล้อมที่แตกต่างกัน

### คำถามที่ 2: ฉันสามารถปรับแต่งลักษณะที่ปรากฏของรูปภาพที่แทรกในเอกสาร OneNote โดยใช้ Aspose.Note for Java ได้หรือไม่

ตอบ 2: ได้ คุณสามารถปรับแต่งแง่มุมต่างๆ ของรูปภาพที่แทรกได้ เช่น การจัดตำแหน่ง ขนาด และการวางแนว เพื่อให้เหมาะกับความต้องการเฉพาะของคุณ

### คำถามที่ 3: Aspose.Note สำหรับ Java รองรับรูปแบบเอกสารอื่นๆ นอกเหนือจาก PDF หรือไม่

ตอบ 3: ใช่ Aspose.Note สำหรับ Java รองรับรูปแบบเอกสารที่หลากหลาย รวมถึง DOCX, HTML และอื่นๆ อีกมากมาย ทำให้คุณมีความยืดหยุ่นในงานการจัดการเอกสารของคุณ

### คำถามที่ 4: ฉันจะค้นหาแหล่งข้อมูลเพิ่มเติมและการสนับสนุนสำหรับ Aspose.Note สำหรับ Java ได้ที่ไหน

ตอบ 4: คุณสามารถเข้าถึงเอกสารประกอบ ลิงก์ดาวน์โหลด ฟอรัมสนับสนุน และสิทธิ์การใช้งานชั่วคราวสำหรับ Aspose.Note สำหรับ Java ผ่านลิงก์ที่ให้ไว้

### คำถามที่ 5: Aspose.Note สำหรับ Java มีเวอร์ชันทดลองใช้งานหรือไม่

ตอบ 5: ได้ คุณสามารถขอรับ Aspose.Note สำหรับ Java รุ่นทดลองใช้ฟรีได้ เพื่อสำรวจคุณสมบัติและความสามารถของมันก่อนตัดสินใจซื้อ

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
