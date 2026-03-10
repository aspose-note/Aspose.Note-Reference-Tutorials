---
date: 2025-12-21
description: เรียนรู้วิธีสร้างเอกสาร OneNote ด้วย Java และแทรกรูปภาพได้อย่างง่ายดายโดยใช้
  Aspose.Note for Java คู่มือขั้นตอนต่อขั้นตอนสำหรับนักพัฒนา Java
linktitle: How to create onenote document java – Build Doc and Insert Image with Stream
second_title: Aspose.Note Java API
title: วิธีสร้างเอกสาร OneNote ด้วย Java – สร้างเอกสารและแทรกรูปภาพด้วยสตรีม
url: /th/java/onenote-hyperlinks-images/build-doc-insert-image-stream/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# วิธีสร้างเอกสาร onenote ด้วย Java – สร้างเอกสารและแทรกรูปภาพด้วย Stream

## บทนำ

ยินดีต้อนรับ! ในบทเรียนนี้คุณจะ **สร้างเอกสาร onenote ด้วย Java** ตั้งแต่เริ่มต้นและเรียนรู้วิธีแทรกรูปภาพโดยใช้สตรีมของรูปภาพ เราจะเดินผ่านแต่ละขั้นตอน อธิบายว่าทำไมแต่ละส่วนจึงสำคัญ และให้เคล็ดลับที่เป็นประโยชน์เพื่อให้คุณสามารถนำเทคนิคนี้ไปใช้ในโครงการจริงได้ เมื่อเสร็จสิ้น คุณจะสามารถสร้างหน้า OneNote ด้วยโปรแกรมและฝังรูปภาพได้อย่างแม่นยำตามที่ต้องการ

## คำตอบสั้น ๆ
- **ต้องใช้ไลบรารีอะไร?** Aspose.Note for Java  
- **สามารถแทรกรูปภาพจากสตรีมได้หรือไม่?** ได้ – เพียงส่ง `InputStream` ไปยังคอนสตรัคเตอร์ของ `Image`  
- **สามารถส่งออกเป็นฟอร์แมตใดได้บ้าง?** ฟอร์แมตใด ๆ ที่ Aspose.Note รองรับ เช่น PDF, DOCX, HTML  
- **ต้องมีลิขสิทธิ์สำหรับการพัฒนาหรือไม่?** ลิขสิทธิ์ชั่วคราวฟรีใช้สำหรับการประเมิน; ต้องมีลิขสิทธิ์เต็มสำหรับการใช้งานจริง  
- **ต้องใช้ Java เวอร์ชันใด?** Java 8 หรือสูงกว่า  

## “สร้างเอกสาร onenote ด้วย Java” คืออะไร?

การสร้างเอกสาร OneNote ด้วย Java หมายถึงการใช้ Aspose.Note API เพื่อสร้างโครงสร้างโน้ตบุ๊กแบบโปรแกรม – หน้า, โครงร่าง, และองค์ประกอบ – โดยไม่ต้องเปิดไคลเอนต์ OneNote บนเดสก์ท็อป วิธีนี้เหมาะสำหรับการสร้างรายงานอัตโนมัติ, การประมวลผลโน้ตเป็นชุด, หรือการรวมเนื้อหา OneNote เข้าไปในแอปพลิเคชัน Java ขนาดใหญ่

## ทำไมต้องใช้ Aspose.Note for Java เพื่อสร้างเอกสาร onenote ด้วย Java?

- **ควบคุมเต็มรูปแบบ** บนการจัดวางหน้า, ตำแหน่งโครงร่าง, และการจัดสไตล์ขององค์ประกอบ  
- **ไม่มี COM interop** – ทำงานบนระบบปฏิบัติการใด ๆ ที่รองรับ Java  
- **ตัวเลือกการส่งออกหลากหลาย** – แปลงเอกสารเดียวกันเป็น PDF, DOCX, HTML ฯลฯ ด้วยการเรียกเดียว  
- **รองรับสตรีม** – สามารถโหลดรูปภาพโดยตรงจากหน่วยความจำ, เครือข่าย, หรือคลาวด์สตอเรจ  

## ข้อกำหนดเบื้องต้น

ก่อนที่เราจะเริ่ม ให้ตรวจสอบว่าคุณได้ตั้งค่าต่อไปนี้เรียบร้อยแล้ว:

### Java Development Kit (JDK)

JDK รุ่นล่าสุด (8 หรือใหม่กว่า) ติดตั้งบนเครื่องของคุณ

### Aspose.Note for Java Library

ดาวน์โหลดไลบรารีจากหน้ารีลีสของ Aspose อย่างเป็นทางการ: [https://releases.aspose.com/note/java/](https://releases.aspose.com/note/java/)

### การตั้งค่า IDE

กำหนดค่า IDE ที่คุณชื่นชอบ (IntelliJ IDEA, Eclipse, VS Code) ให้รวมไฟล์ JAR ของ Aspose.Note ไว้ใน classpath ของโปรเจกต์

## นำเข้าแพ็กเกจ

เพื่อเริ่มต้น ให้นำเข้าคลาส Java และ Aspose.Note ที่จำเป็น การนำเข้าตัวนี้จะทำให้คุณเข้าถึงการสร้างเอกสาร, การจัดการหน้า, การจัดการโครงร่าง, และการแทรกรูปภาพได้

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

## ขั้นตอนที่ 1: ตั้งค่าโฟลเดอร์เอกสาร

กำหนดโฟลเดอร์ที่บรรจุรูปภาพต้นฉบับและที่ที่ไฟล์ผลลัพธ์จะถูกบันทึก แทนที่ตัวแปรตำแหน่งที่เก็บด้วยพาธจริงบนเครื่องของคุณ

```java
String dataDir = "Your Document Directory";
```

## ขั้นตอนที่ 2: สร้างอ็อบเจกต์ Document

สร้างอินสแตนซ์ใหม่ของ `Document` ซึ่งอ็อบเจกต์นี้แทนโน้ตบุ๊ก OneNote ที่คุณกำลังสร้าง

```java
Document doc = new Document();
```

## ขั้นตอนที่ 3: เริ่มต้นอ็อบเจกต์ Page

สร้าง `Page` ที่จะบรรจุโครงร่างและองค์ประกอบทั้งหมดสำหรับหน้าโน้ตนี้

```java
Page page = new Page();
```

## ขั้นตอนที่ 4: สร้าง Outline

`Outline` ทำหน้าที่เป็นคอนเทนเนอร์สำหรับองค์ประกอบที่กำหนดตำแหน่ง ที่นี่เราตั้งค่า offset แนวตั้งและแนวนอนเพื่อวางโครงร่างบนหน้า

```java
Outline outline1 = new Outline();
outline1.setVerticalOffset(600);
outline1.setHorizontalOffset(0);
```

## ขั้นตอนที่ 5: สร้าง Outline Element

`OutlineElement` จะเป็นที่โฮสต์รูปภาพที่เรากำลังจะแทรก

```java
OutlineElement outlineElem1 = new OutlineElement();
```

## ขั้นตอนที่ 6: โหลด Image Stream

เปิดไฟล์รูปภาพเป็นสตรีม การใช้สตรีมทำให้คุณอ่านรูปจากแหล่งใดก็ได้ (ไฟล์ระบบ, เครือข่าย, ฐานข้อมูล) โดยไม่ต้องบันทึกลงดิสก์ก่อน

```java
InputStream fs = null;
try {
    fs = new FileInputStream(dataDir + "image.jpg");
} catch (FileNotFoundException e) {
    e.printStackTrace();
}
```

## ขั้นตอนที่ 7: แทรกรูปภาพ

สร้างอ็อบเจกต์ `Image` อาร์กิวเมนต์แรกสามารถเป็น `null` เมื่อคุณจะให้สตรีมภายหลัง แต่เพื่อความง่าย เราอ้างอิงพาธไฟล์ที่นี่และตั้งค่าการจัดตำแหน่งให้ชิดด้านขวาของหน้า

```java
Image image = new Image(null, dataDir + "image1.jpg");
image.setAlignment(HorizontalAlignment.Right);
```

## ขั้นตอนที่ 8: เพิ่มรูปภาพลงใน Outline Element

เพิ่มรูปภาพลงใน `OutlineElement` เพื่อให้มันเป็นส่วนหนึ่งของลำดับชั้นภาพบนหน้า

```java
outlineElem1.appendChildLast(image);
```

## ขั้นตอนที่ 9: เพิ่ม Outline Element ลงใน Outline

ต่อไปให้แนบ `OutlineElement` (ซึ่งมีรูปภาพ) ไปยังคอนเทนเนอร์ `Outline`

```java
outline1.appendChildLast(outlineElem1);
```

## ขั้นตอนที่ 10: เพิ่ม Outline ลงใน Page

วาง `Outline` ลงบน `Page`

```java
page.appendChildLast(outline1);
```

## ขั้นตอนที่ 11: เพิ่ม Page ลงใน Document

เพิ่มหน้าเต็มที่สร้างเสร็จแล้วเข้าไปในอ็อบเจกต์ `Document`

```java
doc.appendChildLast(page);
```

## ขั้นตอนที่ 12: บันทึก Document

สุดท้ายบันทึกเอกสาร OneNote ในฟอร์แมตที่คุณต้องการ ในตัวอย่างนี้เราส่งออกเป็น PDF แต่คุณสามารถเลือกฟอร์แมตใดก็ได้ที่ Aspose.Note รองรับ

```java
try {
    doc.save("D://Aspose_JavaProjects//OneNote//out3.pdf", SaveFormat.Pdf);
} catch (IOException e) {
    e.printStackTrace();
}
```

โดยทำตามขั้นตอนเหล่านี้ คุณได้ **สร้างเอกสาร onenote ด้วย Java** และฝังรูปภาพโดยใช้ `InputStream` อย่างสำเร็จ

## ข้อผิดพลาดทั่วไป & เคล็ดลับ

- **สตรีมไม่ถูกปิด** – ในสภาพแวดล้อมการผลิต ควรปิด `InputStream` ในบล็อก `finally` หรือใช้ try‑with‑resources  
- **พาธไฟล์ไม่ถูกต้อง** – ตรวจสอบให้แน่ใจว่า `dataDir` ลงท้ายด้วยตัวคั่นที่เหมาะสม (`/` หรือ `\`)  
- **การจัดตำแหน่งรูปภาพ** – หากรูปปรากฏอยู่นอกหน้าจอ ให้ปรับค่า `VerticalOffset`/`HorizontalOffset` ของโครงร่าง  
- **ข้อยกเว้นลิขสิทธิ์** – เวอร์ชันประเมินอาจใส่น้ำลายน้ำในผลลัพธ์; ใช้ลิขสิทธิ์ที่ถูกต้องเพื่อเอาออก  

## คำถามที่พบบ่อย

### Q1: Aspose.Note for Java รองรับเวอร์ชัน OneNote ทั้งหมดหรือไม่?

A1: Aspose.Note for Java รองรับรูปแบบไฟล์ OneNote ต่าง ๆ ทำให้เข้ากันได้กับเวอร์ชันเดสก์ท็อป, ออนไลน์, และมือถือ

### Q2: สามารถปรับแต่งลักษณะของรูปภาพที่แทรกในเอกสาร OneNote ด้วย Aspose.Note for Java ได้หรือไม่?

A2: ได้ คุณสามารถแก้ไขการจัดตำแหน่ง, ขนาด, การหมุน, และแม้กระทั่งการครอปโดยใช้คุณสมบัติต่าง ๆ ของอ็อบเจกต์ `Image`

### Q3: Aspose.Note for Java รองรับฟอร์แมตเอกสารอื่น ๆ นอกจาก PDF หรือไม่?

A3: แน่นอน API สามารถส่งออกเป็น DOCX, HTML, XPS และหลายฟอร์แมตอื่น ๆ ให้คุณมีความยืดหยุ่นในการแชร์หรือเก็บบันทึกโน้ตของคุณ

### Q4: จะหาแหล่งข้อมูลและการสนับสนุนเพิ่มเติมสำหรับ Aspose.Note for Java ได้จากที่ไหน?

A4: เว็บไซต์อย่างเป็นทางการของ Aspose มีเอกสารละเอียด, ตัวอย่างโค้ด, ฟอรั่ม, และลิขสิทธิ์ชั่วคราวสำหรับการประเมิน

### Q5: มีเวอร์ชันทดลองของ Aspose.Note for Java หรือไม่?

A5: มี คุณสามารถดาวน์โหลดเวอร์ชันทดลองฟรีจากหน้ารีลีสของ Aspose เพื่อสำรวจคุณสมบัติต่าง ๆ ก่อนตัดสินใจซื้อ

---

**อัปเดตล่าสุด:** 2025-12-21  
**ทดสอบกับ:** Aspose.Note for Java 24.12 (ล่าสุด ณ เวลาที่เขียน)  
**ผู้เขียน:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}