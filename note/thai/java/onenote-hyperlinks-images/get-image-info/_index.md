---
date: 2025-12-21
description: เรียนรู้วิธีการรับขนาดภาพใน Java ด้วย Aspose.Note ดึงความกว้าง ความสูง
  ชื่อไฟล์และข้อมูลอื่น ๆ จากไฟล์ OneNote เพียงไม่กี่ขั้นตอน.
linktitle: Get Image Dimensions Java from OneNote
second_title: Aspose.Note Java API
title: ดึงขนาดภาพ Java จาก OneNote
url: /th/java/onenote-hyperlinks-images/get-image-info/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# รับขนาดภาพ Java จาก OneNote

## บทนำ

หากคุณต้องการ **get image dimensions java** จากโน้ตบุ๊ก OneNote คุณมาถูกที่แล้ว ในหลายสถานการณ์การทำอัตโนมัติ—การสร้างรายงาน, การย้ายเนื้อหา, หรือการวิเคราะห์—คุณจะต้องการทราบความกว้าง, ความสูง, ขนาดต้นฉบับ, และชื่อไฟล์ของแต่ละรูปภาพโดยไม่ต้องเปิดโน้ตบุ๊กด้วยตนเอง บทเรียนนี้จะพาคุณผ่านการดึงข้อมูลดังกล่าวโดยใช้ Aspose.Note for Java.

## คำตอบอย่างรวดเร็ว
- **โค้ดทำอะไร?** ดึงรูปภาพทุกภาพในไฟล์ OneNote และพิมพ์ขนาด, ขนาดต้นฉบับ, ชื่อไฟล์และวันที่แก้ไข.  
- **ต้องใช้ไลบรารีอะไร?** Aspose.Note for Java.  
- **ต้องการไลเซนส์หรือไม่?** ไลเซนส์ชั่วคราวใช้ได้สำหรับการทดสอบ; ไลเซนส์เต็มจำเป็นสำหรับการใช้งานจริง.  
- **จำนวนบรรทัดของโค้ด?** ประมาณ 30 บรรทัด แบ่งเป็นขั้นตอนที่ชัดเจนและนำกลับใช้ได้.  
- **เวลาในการทำงานโดยทั่วไป?** เป็นมิลลิวินาทีสำหรับโน้ตบุ๊กมาตรฐานที่มีหลายสิบรูปภาพ.

## ข้อกำหนดเบื้องต้น

ก่อนที่เราจะลงลึกในขั้นตอนการทำงาน โปรดตรวจสอบว่าคุณมีข้อกำหนดต่อไปนี้พร้อมใช้งานแล้ว:

### 1. Java Development Kit (JDK)

ตรวจสอบให้แน่ใจว่าคุณได้ติดตั้ง Java Development Kit (JDK) บนระบบของคุณแล้ว คุณสามารถดาวน์โหลดและติดตั้ง JDK ล่าสุดจาก [Oracle website](https://www.oracle.com/java/technologies/javase-jdk15-downloads.html).

### 2. Aspose.Note for Java Library

ดาวน์โหลดและรวมไลบรารี Aspose.Note for Java ลงในโปรเจกต์ของคุณ คุณสามารถรับไลบรารีได้จาก [download page](https://releases.aspose.com/note/java/).

### 3. OneNote Document

เตรียมเอกสาร OneNote ตัวอย่างที่มีรูปภาพ เอกสารนี้จะใช้สำหรับดึงข้อมูลรูปภาพโดยอัตโนมัติ

## นำเข้าแพ็กเกจ

เพื่อเริ่มต้น ให้นำเข้าแพ็กเกจที่จำเป็นจาก Aspose.Note for Java:

```java
import java.io.IOException;
import java.util.List;
import com.aspose.note.Document;
import com.aspose.note.Image;
```

เราจะอธิบายโค้ดข้างต้นเป็นขั้นตอน‑ต่อ‑ขั้นตอน:

## วิธีการรับขนาดภาพ java จาก OneNote

### ขั้นตอนที่ 1: ตั้งค่าไดเรกทอรีเอกสาร

```java
String dataDir = "Your Document Directory";
```

แทนที่ `"Your Document Directory"` ด้วยพาธไปยังเอกสาร OneNote ของคุณ

### ขั้นตอนที่ 2: โหลดเอกสาร

```java
Document doc = new Document(dataDir + "Sample1.one");
```

โหลดเอกสาร OneNote ด้วยไลบรารี Aspose.Note for Java ตรวจสอบให้แน่ใจว่าคุณระบุพาธที่ถูกต้องไปยังเอกสารของคุณ

### ขั้นตอนที่ 3: ดึงรูปภาพทั้งหมด

```java
List<Image> list = doc.getChildNodes(Image.class);
```

ดึงรูปภาพทั้งหมดจากเอกสาร OneNote ที่โหลดแล้ว

### ขั้นตอนที่ 4: พิมพ์จำนวนรูปภาพทั้งหมด

```java
System.out.printf("Total Images: %s\n\n", list.size());
```

พิมพ์จำนวนรูปภาพทั้งหมดที่พบในเอกสาร

### ขั้นตอนที่ 5: วนลูปและพิมพ์ข้อมูลรูปภาพ

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

วนลูปผ่านรายการรูปภาพและพิมพ์รายละเอียดเช่น ความกว้าง, ความสูง, ขนาดต้นฉบับ, ชื่อไฟล์, และเวลาที่แก้ไขล่าสุดสำหรับแต่ละรูปภาพ

## ทำไมต้องดึงรูปภาพจาก OneNote ด้วย Java?

- **Automation:** กำจัดการตรวจสอบโน้ตบุ๊กด้วยมือ.  
- **Data Analytics:** ส่งข้อมูลเมตาดาต้าของรูปภาพเข้าสู่กระบวนการรายงาน.  
- **Migration:** รักษาคุณลักษณะของรูปภาพเมื่อย้ายเนื้อหาไปยังแพลตฟอร์มอื่น.  
- **Performance:** ดึงเมตาดาต้าที่ต้องการเท่านั้น หลีกเลี่ยงการพาร์สไฟล์ที่หนัก.

## ข้อผิดพลาดทั่วไปและเคล็ดลับ

- **Incorrect path:** ตรวจสอบให้แน่ใจว่า `dataDir` ลงท้ายด้วยตัวคั่นไฟล์ที่เหมาะสม (`/` หรือ `\`).  
- **License issues:** หากไม่มีไลเซนส์ที่ถูกต้อง Aspose.Note อาจแสดงคำเตือนการประเมินผล.  
- **Large notebooks:** สำหรับโน้ตบุ๊กที่มีรูปภาพหลายพันรูป ควรพิจารณาประมวลผลเป็นชุดเพื่อประหยัดหน่วยความจำ.

## คำถามที่พบบ่อย

### Q1: Aspose.Note for Java สามารถจัดการรูปแบบเอกสารอื่นนอกจาก OneNote ได้หรือไม่?

A1: ใช่, Aspose.Note for Java รองรับรูปแบบเอกสารต่าง ๆ รวมถึง OneNote, PDF, และ Microsoft Word.

### Q2: Aspose.Note for Java เหมาะสำหรับการใช้งานส่วนบุคคลและเชิงพาณิชย์หรือไม่?

A2: ใช่, คุณสามารถใช้ Aspose.Note for Java ได้ทั้งในงานส่วนบุคคลและเชิงพาณิชย์.

### Q3: Aspose.Note for Java มีการสนับสนุนทางเทคนิคหรือไม่?

A3: ใช่, การสนับสนุนทางเทคนิคพร้อมให้บริการผ่านฟอรั่มของ Aspose ที่ [here](https://forum.aspose.com/c/note/28).

### Q4: ฉันสามารถทดลองใช้ Aspose.Note for Java ก่อนตัดสินใจซื้อได้หรือไม่?

A4: ใช่, คุณสามารถสำรวจเวอร์ชันทดลองฟรีของ Aspose.Note for Java จาก [Aspose.Note for Java](https://releases.aspose.com/note/java/).

### Q5: ฉันจะขอรับไลเซนส์ชั่วคราวสำหรับ Aspose.Note for Java ได้อย่างไร?

A5: คุณสามารถรับไลเซนส์ชั่วคราวได้จาก [Temporary license/](https://purchase.aspose.com/temporary-license/).

## สรุป

โดยทำตามขั้นตอนที่อธิบายไว้ในบทเรียนนี้ คุณสามารถ **get image dimensions java** จากเอกสาร OneNote ได้อย่างมีประสิทธิภาพโดยใช้ Aspose.Note for Java การรวมฟังก์ชันนี้เข้าไปในแอปพลิเคชันของคุณจะช่วยทำงานอัตโนมัติเกี่ยวกับการประมวลผลเอกสาร เพิ่มประสิทธิภาพและผลผลิต

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Last Updated:** 2025-12-21  
**Tested With:** Aspose.Note for Java 23.12  
**Author:** Aspose