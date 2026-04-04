---
date: 2026-03-05
description: เรียนรู้วิธีส่งออกเอกสาร OneNote เป็นภาพ BMP โดยใช้ Image Save Options
  ของ Aspose.Note for Java นอกจากนี้ยังดูวิธีแปลง OneNote เป็น PDF หรือบันทึก OneNote
  เป็น PNG.
linktitle: how to export onenote to BMP Image Using Image Save Options
second_title: Aspose.Note Java API
title: วิธีส่งออก OneNote เป็นภาพ BMP โดยใช้ตัวเลือกการบันทึกภาพ
url: /th/java/onenote-document-saving/save-to-bmp-image-using-image-save-options/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# วิธีส่งออก OneNote เป็นภาพ BMP ด้วย Image Save Options

## วิธีส่งออก OneNote เป็นภาพ BMP

## คำตอบอย่างรวดเร็ว
- **Image Save Options class ทำหน้าที่อะไร?** มันให้คุณระบุรูปแบบภาพที่ต้องการส่งออก (BMP, PNG, JPEG ฯลฯ) เมื่อแปลงหน้า OneNote.  
- **ฉันต้องมีลิขสิทธิ์เพื่อรันตัวอย่างหรือไม่?** การทดลองใช้ฟรีสามารถใช้เพื่อประเมินได้ แต่ต้องมีลิขสิทธิ์เชิงพาณิชย์สำหรับการใช้งานในผลิตภัณฑ์จริง.  
- **ฉันสามารถแปลงหน้า OneNote เป็น PDF หรือ PNG แทน BMP ได้หรือไม่?** ได้ – เพียงเปลี่ยนค่า enum `SaveFormat` (เช่น `SaveFormat.Pdf` หรือ `SaveFormat.Png`).  
- **รองรับเวอร์ชัน Java ใด?** รองรับ Java 8 และรุ่นต่อ ๆ ไปอย่างเต็มที่.  
- **มีการจัดการพิเศษสำหรับเอกสารขนาดใหญ่หรือไม่?** คุณสามารถสตรีมผลลัพธ์เพื่อหลีกเลี่ยงการใช้หน่วยความจำสูง.

## “Image Save Options” คืออะไรใน Aspose.Note?
`ImageSaveOptions` class ให้การควบคุมระดับละเอียดเกี่ยวกับการแปลงหน้า OneNote ให้เป็นภาพแรสเตอร์ คุณสามารถตั้งค่ารูปแบบภาพ, ความละเอียด, ความลึกของสี, และอื่น ๆ ความยืดหยุ่นนี้ทำให้การ **ส่งออกภาพหน้า OneNote** สำหรับระบบเก่า (BMP) หรือสถานการณ์เว็บสมัยใหม่ (PNG/JPEG) ง่ายขึ้น.

## ข้อกำหนดเบื้องต้น

1. ความรู้พื้นฐานของภาษาโปรแกรม Java.  
2. ติดตั้ง JDK (Java Development Kit) บนเครื่องของคุณ.  
3. IDE เช่น Eclipse หรือ IntelliJ IDEA.  
4. ไลบรารี Aspose.Note for Java – ดาวน์โหลดได้จาก [here](https://releases.aspose.com/note/java/).

## นำเข้าแพ็กเกจ

ก่อนแรก, ให้นำเข้าคลาส Aspose.Note ที่จำเป็นและยูทิลิตี้ I/O ของ Java มาตรฐาน:

```java
import com.aspose.note.*;
import java.io.IOException;
```

## ขั้นตอนที่ 1: โหลดเอกสาร OneNote

ที่นี่เราชี้ไปยังโฟลเดอร์ที่มีไฟล์ OneNote ต้นฉบับ (`Aspose.one`) และโหลดมันเข้าสู่วัตถุ `Document`. วัตถุนี้ให้คุณเข้าถึงหน้า, ส่วน, และองค์ประกอบอื่น ๆ ภายในโน้ตบุ๊กได้อย่างเต็มที่.

```java
// The path to the documents directory.
String dataDir = "Your Document Directory";

// Load the document into Aspose.Note.
Document oneFile = new Document(dataDir + "Aspose.one");
```

## ขั้นตอนที่ 2: บันทึกเอกสารเป็นภาพ BMP

เราจะต่อชื่อไฟล์ผลลัพธ์, จากนั้นเรียก `save` พร้อมกับอินสแตนซ์ `ImageSaveOptions` ที่ตั้งค่าไว้สำหรับ **BMP** (`SaveFormat.Bmp`).  
หากคุณต้องการ **บันทึกหน้า OneNote** เป็น PNG, เพียงเปลี่ยน `SaveFormat.Bmp` เป็น `SaveFormat.Png`. เช่นเดียวกัน, `SaveFormat.Pdf` จะทำให้คุณทำการแปลง **OneNote เป็น PDF**.

```java
dataDir = dataDir + "SaveToBmpImageUsingImageSaveOptions_out.bmp";

// Save the document.
oneFile.save(dataDir, new ImageSaveOptions(SaveFormat.Bmp));
```

## ทำไมต้องเลือก BMP?

- **คุณภาพแบบไม่มีการสูญเสีย** – BMP เก็บข้อมูลพิกเซลดิบ, รักษาลักษณะเดิมของหน้าต้นฉบับอย่างแม่นยำ.  
- **ความเข้ากันได้** – แอปพลิเคชัน Windows รุ่นเก่ามักต้องการไฟล์ BMP.  
- **ความเรียบง่าย** – ไม่มีศิลปะการบีบอัด, ทำให้เหมาะสำหรับการประมวลผลภาพต่อไป.

## ปัญหาทั่วไปและเคล็ดลับ

- **ข้อผิดพลาดของเส้นทางไฟล์** – ตรวจสอบให้ `dataDir` สิ้นสุดด้วยตัวคั่นไฟล์ที่เหมาะสม (`/` หรือ `\`).  
- **โน้ตบุ๊กขนาดใหญ่** – สำหรับไฟล์ OneNote ขนาดใหญ่มาก, พิจารณาบันทึกแต่ละหน้าแยกกันเพื่อรักษาการใช้หน่วยความจำให้ต่ำ.  
- **ข้อยกเว้นลิขสิทธิ์** – การรันโค้ดโดยไม่มีลิขสิทธิ์ที่ถูกต้องจะทำให้ภาพที่สร้างมีลายน้ำ.

## สรุป

ในคู่มือนี้เราได้สาธิต **วิธีส่งออกเอกสาร OneNote** เป็นภาพ BMP ด้วย `ImageSaveOptions` ของ Aspose.Note for Java. โดยการสลับค่า enum `SaveFormat` คุณสามารถสร้าง PNG, JPEG, PDF หรือรูปแบบอื่นที่รองรับได้, ทำให้คุณมีวิธีที่ยืดหยุ่นในการส่งออกเนื้อหา OneNote สำหรับสถานการณ์ใด ๆ ต่อไป.

## คำถามที่พบบ่อย

**Q1: ฉันสามารถบันทึกเอกสาร OneNote เป็นรูปภาพรูปแบบอื่นนอกจาก BMP ได้หรือไม่?**  
A: ได้, คุณสามารถใช้ `ImageSaveOptions` กับ `SaveFormat.Png`, `SaveFormat.Jpeg`, `SaveFormat.Gif`, หรือ `SaveFormat.Tiff` เพื่อส่งออกเป็นรูปแบบเหล่านั้น.

**Q2: Aspose.Note for Java รองรับการแปลงระหว่างรูปแบบเอกสารต่าง ๆ หรือไม่?**  
A: แน่นอน. นอกจากรูปแบบภาพ, คุณสามารถแปลงไฟล์ OneNote เป็น PDF, DOCX, HTML, และอื่น ๆ ด้วย `SaveFormat` ที่เหมาะสม.

**Q3: Aspose.Note for Java เข้ากันได้กับเวอร์ชันล่าสุดของ OneNote หรือไม่?**  
A: ใช่, ไลบรารีนี้ได้รับการอัปเดตอย่างสม่ำเสมอเพื่อให้สอดคล้องกับการปล่อยเวอร์ชันใหม่ของ OneNote.

**Q4: ฉันสามารถจัดการเนื้อหาเอกสาร OneNote ผ่านโปรแกรมได้หรือไม่?**  
A: ได้, คุณสามารถเพิ่ม, แก้ไข, หรือ ลบหน้า, ส่วน, และเนื้อหาที่หลากหลาย (ข้อความ, รูปภาพ, ตาราง) ผ่าน API.

**Q5: Aspose.Note for Java มีการสนับสนุนทางเทคนิคหรือไม่?**  
A: มี, Aspose มีการสนับสนุนทางเทคนิคและฟอรั่มเฉพาะ. เยี่ยมชม [Aspose.Note forum](https://forum.aspose.com/c/note/28) เพื่อขอความช่วยเหลือ.

---

**อัปเดตล่าสุด:** 2026-03-05  
**ทดสอบด้วย:** Aspose.Note for Java 24.12  
**ผู้เขียน:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}