---
date: 2026-03-27
description: เรียนรู้วิธีดึงรายละเอียดงานจากงาน OneNote Outlook ด้วย Aspose.Note for
  Java – โซลูชันที่รวดเร็วและเชื่อถือได้สำหรับนักพัฒนา Java
linktitle: Get Outlook Task in OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: วิธีดึงงานจาก OneNote Outlook Tasks – Aspose.Note
url: /th/java/onenote-text-manipulation/get-outlook-task/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# วิธีการดึงข้อมูลงานจาก OneNote Outlook Tasks

## บทนำ
หากคุณต้องการ **วิธีการดึงข้อมูลงาน** ที่อยู่ในหน้า OneNote—โดยเฉพาะงาน Outlook—Aspose.Note for Java ทำให้ขั้นตอนนี้ง่ายดาย ในบทแนะนำเชิงปฏิบัตินี้เราจะเดินผ่านขั้นตอนที่แน่นอนเพื่อดึงคุณสมบัติงาน (สถานะ, วันกำหนด, เวลาสร้าง ฯลฯ) จากเอกสาร OneNote แล้วพิมพ์ออกที่คอนโซล เมื่อเสร็จคุณจะได้สคริปต์ที่นำกลับมาใช้ใหม่ได้ในโครงการ Java ใด ๆ ที่ทำงานกับไฟล์ OneNote

## คำตอบสั้น
- **บทเรียนนี้ครอบคลุมอะไร?** การดึงรายละเอียด Outlook Task จากไฟล์ OneNote ด้วย Aspose.Note for Java  
- **ใช้เวลาติดตั้งเท่าไหร่?** ประมาณ 10‑15 นาทีสำหรับการตั้งค่าเบื้องต้น  
- **ข้อกำหนดเบื้องต้น?** Java JDK, ไลบรารี Aspose.Note for Java, และไฟล์ OneNote ที่มีงานอยู่  
- **ต้องการไลเซนส์หรือไม่?** จำเป็นต้องมีไลเซนส์ Aspose.Note ชั่วคราวหรือเต็มสำหรับการใช้งานในผลิตภัณฑ์  
- **สามารถรันบนระบบปฏิบัติการใดก็ได้หรือไม่?** ได้ – ไลบรารีเป็นแบบ platform‑independent ตราบใดที่ Java ทำงานได้  

## การดึงงานจาก OneNote คืออะไร?
การดึงงานหมายถึงการอ่านแท็ก `NoteTask` ที่ OneNote เก็บไว้สำหรับแต่ละงานที่เชื่อมกับ Outlook แท็กนี้บรรจุเมตาดาต้าเช่น เวลาเสร็จสิ้น, วันกำหนด, และสถานะ ซึ่งคุณสามารถเข้าถึงได้ผ่านโมเดลอ็อบเจกต์ของ Aspose.Note

## ทำไมต้องดึงข้อมูลงาน?
- **Automation:** ซิงค์งานกับระบบจัดการงานของคุณเอง  
- **Reporting:** สร้างรายงานแบบกำหนดเองเกี่ยวกับความคืบหน้าของงานในหลาย ๆ โน้ตบุ๊ก  
- **Migration:** ย้ายงานจาก OneNote ไปยังแพลตฟอร์มอื่น (เช่น Microsoft Planner, Jira)  

## ข้อกำหนดเบื้องต้น
ก่อนเริ่มทำตามขั้นตอน ให้ตรวจสอบว่าคุณมี:

- **Java Development Kit (JDK)** – เวอร์ชันล่าสุด (8 หรือสูงกว่า)  
- **Aspose.Note for Java** – ดาวน์โหลดจาก [download page](https://releases.aspose.com/note/java/)  

## นำเข้าแพ็กเกจ
เริ่มต้นด้วยการนำเข้าคลาสที่จำเป็นในไฟล์ซอร์ส Java ของคุณ:

```java
import java.io.IOException;
import java.util.List;
import com.aspose.note.Document;
import com.aspose.note.ITag;
import com.aspose.note.NoteTask;
import com.aspose.note.RichText;
```

## ขั้นตอนที่ 1: ตั้งค่าโปรเจกต์ของคุณ
สร้างโปรเจกต์ Java ใหม่ (Maven, Gradle หรือ IDE ธรรมดา) แล้วเพิ่มไฟล์ JAR ของ Aspose.Note เข้าไปใน classpath เก็บไฟล์ OneNote ของคุณไว้ในโฟลเดอร์เฉพาะ เช่น `data/`

## ขั้นตอนที่ 2: โหลดเอกสาร OneNote
โหลดไฟล์ `.one` ที่คุณต้องการตรวจสอบ:

```java
String dataDir = "Your Document Directory";
Document doc = new Document(dataDir + "Sample1.one");
```

> **เคล็ดลับ:** ใช้พาธแบบเต็มหรือกำหนดค่าเป็น property หากแอปของคุณทำงานในสภาพแวดล้อมที่ต่างกัน

## ขั้นตอนที่ 3: ดึงโหนด RichText
องค์ประกอบข้อความทั้งหมดจะแสดงเป็นโหนด `RichText` ดึงทั้งหมดออกมา:

```java
List<RichText> nodes = (List<RichText>) doc.getChildNodes(RichText.class);
```

## ขั้นตอนที่ 4: วนลูปผ่านแต่ละโหนด
ค้นหาแท็ก `NoteTask` ในแต่ละโหนด `RichText`:

```java
for (RichText richText : nodes) {
    for (ITag tag : richText.getTags()) {
        if (tag.getClass() == NoteTask.class) {
            // Your code to handle NoteTask
        }
    }
}
```

## ขั้นตอนที่ 5: ดึงคุณสมบัติงาน
เมื่อคุณมีอินสแตนซ์ `NoteTask` แล้ว คุณสามารถอ่านคุณสมบัติต่าง ๆ ได้:

```java
NoteTask noteTask = (NoteTask) tag;
System.out.println("Completed Time: " + noteTask.getCompletedTime());
System.out.println("Create Time: " + noteTask.getCreationTime());
System.out.println("Due Date: " + noteTask.getDueDate());
System.out.println("Status: " + noteTask.getStatus());
System.out.println("Icon: " + noteTask.getIcon());
```

> **หมายเหตุ:** ให้รันลูปสำหรับทุกโหนด `NoteTask` เพื่อดึงข้อมูลจากงานทั้งหมดในเอกสาร

## ปัญหาที่พบบ่อยและวิธีแก้
| ปัญหา | สาเหตุ | วิธีแก้ |
|-------|--------|----------|
| `NullPointerException` บน `noteTask` | แท็กไม่ได้เป็น `NoteTask` | เพิ่มการตรวจสอบ null หรือยืนยันว่า `tag instanceof NoteTask` |
| ไม่มีผลลัพธ์สำหรับวันที่ | งานใน OneNote ไม่มีวันกำหนด | ตรวจสอบ `noteTask.getDueDate()` ว่าเป็น `null` ก่อนพิมพ์ |
| ไลบรารีไม่พบขณะรัน | JAR ไม่อยู่ใน classpath | ตรวจสอบให้แน่ใจว่าไฟล์ JAR ของ Aspose.Note ถูกใส่ในการตั้งค่า build ของคุณ |

## คำถามที่พบบ่อย

**Q: สามารถใช้ Aspose.Note for Java กับเฟรมเวิร์ก Java อื่น ๆ ได้หรือไม่?**  
A: ได้, Aspose.Note for Java ผสานรวมได้อย่างราบรื่นกับ Spring, Jakarta EE, Android และสภาพแวดล้อม Java มาตรฐานใด ๆ

**Q: มีรุ่นทดลองฟรีสำหรับ Aspose.Note for Java หรือไม่?**  
A: มี, คุณสามารถลองใช้รุ่นทดลองฟรีของ Aspose.Note for Java [ที่นี่](https://releases.aspose.com/)

**Q: จะขอรับการสนับสนุนสำหรับ Aspose.Note for Java ได้อย่างไร?**  
A: เยี่ยมชม [Aspose.Note Forum](https://forum.aspose.com/c/note/28) เพื่อรับความช่วยเหลือจากชุมชนหรือซื้อแผนสนับสนุนพรีเมียม

**Q: จะหาเอกสารรายละเอียดสำหรับ Aspose.Note for Java ได้ที่ไหน?**  
A: ดูที่ [Aspose.Note for Java documentation](https://reference.aspose.com/note/java/) สำหรับอ้างอิง API เชิงลึกและตัวอย่าง

**Q: จะขอรับไลเซนส์ชั่วคราวสำหรับ Aspose.Note for Java ได้อย่างไร?**  
A: รับไลเซนส์ชั่วคราวของคุณ [ที่นี่](https://purchase.aspose.com/temporary-license/)  

## สรุป
คุณได้เรียนรู้ **วิธีการดึงข้อมูลงาน** จาก OneNote ด้วย Aspose.Note for Java แล้ว ความสามารถนี้เปิดประตูสู่การอัตโนมัติ, การสร้างรายงาน, และการย้ายข้อมูลที่เคยทำด้วยมือและเสี่ยงต่อข้อผิดพลาดแล้ว อย่าลังเลที่จะต่อยอดตัวอย่างนี้—เก็บข้อมูลที่ดึงมาไว้ในฐานข้อมูล, ส่งต่อไปยังบริการภายนอก, หรือผสานกับเนื้อหา OneNote อื่น ๆ

---

**อัปเดตล่าสุด:** 2026-03-27  
**ทดสอบด้วย:** Aspose.Note for Java 24.11 (รุ่นล่าสุด ณ เวลาที่เขียน)  
**ผู้เขียน:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}