---
title: นำธีมสีเข้มไปใช้กับข้อความใน OneNote - Aspose.Note
linktitle: นำธีมสีเข้มไปใช้กับข้อความใน OneNote - Aspose.Note
second_title: Aspose.Note Java API
description: สำรวจขั้นตอนง่ายๆ ในการปรับใช้ธีมสีเข้มกับข้อความ OneNote ของคุณโดยใช้ Aspose.Note for Java ยกระดับประสบการณ์ด้านเอกสารดิจิทัลของคุณอย่างง่ายดาย
type: docs
weight: 11
url: /th/java/onenote-text-manipulation/apply-dark-theme/
---
## การแนะนำ
ในภูมิทัศน์ของเอกสารดิจิทัลที่เปลี่ยนแปลงตลอดเวลา ความสวยงามของบันทึกย่อของคุณอาจส่งผลกระทบอย่างมากต่อความสามารถในการอ่านและประสบการณ์ผู้ใช้ แง่มุมหนึ่งที่น่าสังเกตคือการใช้ธีมสีเข้ม เพื่อสร้างสภาพแวดล้อมที่ดึงดูดสายตาและสะดวกสบาย ในบทช่วยสอนนี้ เราจะแนะนำคุณตลอดขั้นตอนการนำธีมสีเข้มไปใช้กับข้อความใน OneNote โดยใช้ Aspose.Note for Java
## ข้อกำหนดเบื้องต้น
ก่อนที่จะเข้าสู่บทช่วยสอน ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:
-  Aspose.Note สำหรับ Java: ดาวน์โหลดและติดตั้งไลบรารี Aspose.Note สำหรับ Java จาก[ที่นี่](https://releases.aspose.com/note/java/).
- Java Development Kit (JDK): ตรวจสอบให้แน่ใจว่าคุณได้ติดตั้ง Java บนเครื่องของคุณแล้ว
- สภาพแวดล้อมการพัฒนาแบบรวม (IDE): เลือก IDE เช่น Eclipse หรือ IntelliJ เพื่อการพัฒนาที่ราบรื่น
## แพ็คเกจนำเข้า
ในการเริ่มต้น ให้นำเข้าแพ็คเกจที่จำเป็นไปยังโปรเจ็กต์ Java ของคุณ:
```java
import com.aspose.note.*;
import java.awt.*;
import java.io.IOException;
import java.nio.file.Paths;
```
## ขั้นตอนที่ 1: ตั้งค่าสีพื้นหลังของหน้า
```java
// เส้นทางไปยังไดเร็กทอรีเอกสาร
String dataDir = "Your Document Directory";
// โหลดเอกสารลงใน Aspose.Note
Document doc = new Document(Paths.get(dataDir, "Aspose.one").toString());
for (Page page: doc)
{
    page.setBackgroundColor(Color.BLACK);
}
```
## ขั้นตอนที่ 2: ปรับสีข้อความ
```java
for (RichText node: doc.getChildNodes(RichText.class))
{
    Color c = node.getParagraphStyle().getFontColor();
    if (c.getAlpha() <= 10 || Math.abs(c.getRed() - Color.BLACK.getRed()) + Math.abs(c.getGreen() - Color.BLACK.getGreen()) + Math.abs(c.getBlue() - Color.BLACK.getBlue()) <= 30)
    {
        node.getParagraphStyle().setFontColor(Color.WHITE);
    }
}
```
## ขั้นตอนที่ 3: บันทึกเอกสาร
```java
doc.save(Paths.get(dataDir, "AsposeDarkTheme.pdf").toString());
```
ทำซ้ำขั้นตอนเหล่านี้สำหรับแต่ละเอกสาร และคุณจะสามารถใช้ธีมสีเข้มกับข้อความ OneNote ของคุณได้สำเร็จโดยใช้ Aspose.Note for Java
## บทสรุป
โดยสรุป การปรับปรุงรูปลักษณ์ของบันทึกย่อดิจิทัลของคุณนั้นทำได้ง่ายด้วย Aspose.Note สำหรับ Java ด้วยการทำตามคำแนะนำทีละขั้นตอนนี้ คุณจะสามารถนำธีมสีเข้มไปใช้กับข้อความใน OneNote ได้อย่างง่ายดาย ซึ่งจะช่วยยกระดับประสบการณ์การใช้งานเอกสารของคุณ
## คำถามที่พบบ่อย
### ฉันสามารถใช้ธีมสีเข้มกับส่วนใดส่วนหนึ่งเท่านั้นได้หรือไม่
ได้ คุณสามารถแก้ไขโค้ดเพื่อใช้ธีมสีเข้มแบบเลือกสรรกับส่วนเฉพาะภายในเอกสารของคุณได้
### มีธีมสีเข้มที่กำหนดไว้ล่วงหน้าใน Aspose.Note สำหรับ Java หรือไม่
ณ ตอนนี้ Aspose.Note สำหรับ Java อนุญาตให้คุณปรับแต่งธีมได้ แต่ไม่มีธีมสีเข้มที่กำหนดไว้ล่วงหน้า
### Aspose.Note สำหรับ Java รองรับรูปแบบเอกสารอื่นหรือไม่
ใช่ Aspose.Note สำหรับ Java รองรับรูปแบบเอกสารที่หลากหลาย รวมถึง PDF, DOCX และ HTML
### มีเวอร์ชันทดลองใช้สำหรับ Aspose.Note สำหรับ Java หรือไม่
 ใช่ คุณสามารถเข้าถึงเวอร์ชันทดลองใช้ฟรีได้[ที่นี่](https://releases.aspose.com/).
### ฉันจะรับการสนับสนุนสำหรับ Aspose.Note สำหรับ Java ได้อย่างไร
 เยี่ยมชม[ฟอรั่ม Aspose.Note](https://forum.aspose.com/c/note/28) สำหรับการสนับสนุนจากชุมชนหรือสำรวจตัวเลือกการสนับสนุนระดับพรีเมียม[ที่นี่](https://purchase.aspose.com/temporary-license/).