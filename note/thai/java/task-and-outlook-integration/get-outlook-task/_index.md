---
date: 2026-04-01
description: เรียนรู้วิธีดึงงานจาก Outlook ไปยัง OneNote ด้วย Aspose.Note สำหรับ Java.
  ทำตามคู่มือขั้นตอนต่อขั้นตอนนี้เพื่อดึงรายละเอียดงานอย่างรวดเร็ว.
keywords:
- how to extract tasks
- Aspose.Note Java
- Outlook task extraction
linktitle: รับงาน Outlook ใน OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: วิธีดึงงาน Outlook ใน OneNote ด้วย Aspose.Note
url: /th/java/task-and-outlook-integration/get-outlook-task/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# ดึงงาน Outlook ใน OneNote - Aspose.Note

## บทนำ
ยินดีต้อนรับสู่คู่มือเชิงลึกของเราว่า **วิธีดึงงาน** จาก Outlook ในสมุดบันทึก OneNote ด้วย Aspose.Note สำหรับ Java ไม่ว่าคุณจะกำลังสร้างเครื่องมือการย้ายข้อมูล, สร้างรายงาน, หรือเพียงแค่ต้องการซิงค์ข้อมูลงาน, บทแนะนำนี้จะพาคุณผ่านทุกขั้นตอน—ตั้งแต่การโหลดไฟล์ OneNote ไปจนถึงการอ่านคุณสมบัติของแต่ละงาน Outlook. เมื่อเสร็จสิ้นคุณจะมีโค้ดสแนปช็อตที่พร้อมใช้งานซึ่งสามารถปรับใช้กับโครงการของคุณได้.

## คำตอบอย่างรวดเร็ว
- **บทแนะนำนี้ครอบคลุมอะไร?** การสกัดรายละเอียดงาน Outlook จากเอกสาร OneNote ด้วย Aspose.Note สำหรับ Java.  
- **ใช้ API ใด?** ไลบรารี Aspose.Note สำหรับ Java.  
- **ต้องการใบอนุญาตหรือไม่?** การทดลองใช้ฟรีทำงานได้สำหรับการพัฒนา; จำเป็นต้องมีใบอนุญาตเชิงพาณิชย์สำหรับการใช้งานจริง.  
- **ใช้เวลานานเท่าไหร่ในการทำงาน?** ประมาณ 10‑15 นาทีหลังจากตั้งค่าสภาพแวดล้อมเรียบร้อย.  
- **สามารถประมวลผลหลายสมุดบันทึกได้หรือไม่?** ได้—เพียงวนลูปไฟล์และใช้ตรรกะเดียวกัน.

## การสกัดงานคืออะไร
การสกัดงานหมายถึงการอ่านข้อมูลงานที่มีโครงสร้าง (เช่น วันที่ครบกำหนด, สถานะ, และไอคอน) ที่ Outlook เก็บไว้ภายในหน้าของ OneNote เป็นแท็ก `NoteTask`. สิ่งนี้ทำให้สามารถเข้าถึงเมตาดาต้าของงานโดยอัตโนมัติโดยไม่ต้องคัดลอกด้วยมือ.

## ทำไมต้องใช้ Aspose.Note สำหรับ Java
- **ไม่ต้องการ Microsoft Office** – ทำงานบนแพลตฟอร์มใดก็ได้ที่มี Java runtime.  
- **ความสมบูรณ์เต็มรูปแบบ** – รักษาองค์ประกอบทั้งหมดของ OneNote ขณะเดียวกันให้คุณเข้าถึงแท็กโดยตรง.  
- **ประสิทธิภาพสูง** – ปรับให้เหมาะกับสมุดบันทึกขนาดใหญ่และการประมวลผลเป็นชุด.  

## ข้อกำหนดเบื้องต้น
ก่อนที่เราจะเริ่ม, โปรดตรวจสอบว่าคุณมีสิ่งต่อไปนี้พร้อมใช้งาน:

- **สภาพแวดล้อมการพัฒนา Java** – JDK 8 หรือใหม่กว่า ติดตั้งและกำหนดค่าแล้ว.  
- **ไลบรารี Aspose.Note** – ดาวน์โหลดแพ็กเกจ Java ล่าสุดจากเว็บไซต์อย่างเป็นทางการ [here](https://releases.aspose.com/note/java/).  
- **ไฟล์ OneNote ตัวอย่าง** – บทแนะนำใช้ `Sample1.one`; คุณสามารถเปลี่ยนเป็นสมุดบันทึกใดก็ได้ที่มีงาน Outlook.

## นำเข้าแพ็กเกจ
เพิ่มการนำเข้าที่จำเป็นลงในคลาส Java ของคุณ. คลาสเหล่านี้ให้คุณเข้าถึงโมเดลเอกสารและแท็ก `NoteTask` ที่เฉพาะของ Outlook.

```java
import java.io.IOException;
import java.util.List;
import com.aspose.note.Document;
import com.aspose.note.ITag;
import com.aspose.note.NoteTask;
import com.aspose.note.RichText;
```

## คู่มือขั้นตอนต่อขั้นตอน

### ขั้นตอนที่ 1: ตั้งค่าไดเรกทอรีเอกสารของคุณ
กำหนดโฟลเดอร์ที่เก็บไฟล์ OneNote ของคุณ. การใช้เส้นทางแบบ absolute หรือ relative ก็ได้, แต่ควรทำให้สตริงเส้นทางเป็นระเบียบเพื่อความอ่านง่าย.

```java
String dataDir = "Your Document Directory";
```

### ขั้นตอนที่ 2: โหลดเอกสาร OneNote
สร้างอินสแตนซ์ `Document` โดยชี้ไปที่ไฟล์ `.one`. Aspose.Note จะวิเคราะห์ไฟล์เป็นโครงสร้างคล้าย DOM ที่คุณสามารถเดินสำรวจได้.

```java
Document doc = new Document(dataDir + "Sample1.one");
```

### ขั้นตอนที่ 3: ดึงโหนด RichText ทั้งหมด
งาน Outlook ถูกเก็บไว้ภายในองค์ประกอบ `RichText`. ดึงโหนด `RichText` ทั้งหมดเพื่อให้คุณสามารถตรวจสอบแท็กของมันได้.

```java
List<RichText> nodes = (List<RichText>) doc.getChildNodes(RichText.class);
```

### ขั้นตอนที่ 4: วนลูปผ่านแต่ละโหนด
วนลูปผ่านแต่ละโหนด `RichText`, ตรวจสอบแท็กของมัน, และทำการเมื่อพบ `NoteTask`. โค้ดด้านล่างจะแสดงคุณสมบัติที่เป็นประโยชน์ที่สุดสำหรับแต่ละงาน.

```java
for (RichText richText : nodes) {
    for (ITag tag : richText.getTags()) {
        if (tag.getClass() == NoteTask.class) {
            NoteTask noteTask = (NoteTask) tag;
            
            // Retrieve properties
            System.out.println("Completed Time: " + noteTask.getCompletedTime());
            System.out.println("Create Time: " + noteTask.getCreationTime());
            System.out.println("Due Date: " + noteTask.getDueDate());
            System.out.println("Status: " + noteTask.getStatus());
            System.out.println("Icon: " + noteTask.getIcon());
        }
    }
}
```

**เคล็ดลับ:** หากคุณต้องการเพียงส่วนย่อยของคุณสมบัติ, คุณสามารถข้ามส่วนที่เหลือเพื่อเพิ่มประสิทธิภาพเมื่อประมวลผลสมุดบันทึกขนาดใหญ่.

### ปัญหาทั่วไปและวิธีแก้
- **ไม่พบงาน:** ตรวจสอบให้แน่ใจว่าหน้า OneNote มีงาน Outlook จริง ๆ. งานจะแสดงเป็นช่องทำเครื่องหมายพร้อมไอคอน Outlook ขนาดเล็ก.  
- **ค่า null:** ฟิลด์งานบางอย่าง (เช่น `CompletedTime`) อาจเป็น `null` หากงานยังไม่เสร็จสิ้น. ป้องกัน `NullPointerException` ด้วยการตรวจสอบ `null` ก่อนพิมพ์.  
- **ไฟล์ไม่พบ:** ตรวจสอบว่า `dataDir` ลงท้ายด้วยตัวคั่นเส้นทางที่เหมาะสม (`/` หรือ `\\`) สำหรับ OS ของคุณ.

## สรุป
ขอแสดงความยินดี! คุณได้เรียนรู้ **วิธีดึงงาน** จาก Outlook ใน OneNote ด้วย Aspose.Note Java API. วิธีนี้ให้คุณควบคุมข้อมูลงานได้อย่างเต็มรูปแบบผ่านโปรแกรม, ทำให้สามารถผสานรวมกับเครื่องมือรายงานแบบกำหนดเอง, ฐานข้อมูล, หรือกระบวนการธุรกิจอื่น ๆ.

## คำถามที่พบบ่อย

**Q: Aspose.Note รองรับทุกเวอร์ชันของ OneNote หรือไม่?**  
A: Aspose.Note รองรับ Microsoft OneNote 2010 และเวอร์ชันต่อ ๆ ไป.

**Q: ฉันสามารถใช้ Aspose.Note สำหรับโครงการส่วนบุคคลและเชิงพาณิชย์ได้หรือไม่?**  
A: ใช่, Aspose.Note สามารถใช้ได้ทั้งในโครงการส่วนบุคคลและเชิงพาณิชย์. เยี่ยมชม [here](https://purchase.aspose.com/buy) เพื่อสำรวจตัวเลือกการให้สิทธิ์.

**Q: มีการทดลองใช้ฟรีสำหรับ Aspose.Note หรือไม่?**  
A: มี, คุณสามารถเข้าถึงการทดลองใช้ฟรีได้ที่ [here](https://releases.aspose.com/).

**Q: ฉันจะรับการสนับสนุนสำหรับ Aspose.Note อย่างไร?**  
A: เยี่ยมชม [Aspose.Note Forum](https://forum.aspose.com/c/note/28) เพื่อรับการสนับสนุนจากชุมชน. หากต้องการความช่วยเหลือเพิ่มเติม, พิจารณาซื้อ [temporary license](https://purchase.aspose.com/temporary-license/).

**Q: มีเอกสาร OneNote ตัวอย่างสำหรับการทดสอบหรือไม่?**  
A: คุณสามารถค้นหาเอกสารตัวอย่างได้ในเอกสาร Aspose.Note [here](https://reference.aspose.com/note/java/).

---

**Last Updated:** 2026-04-01  
**ทดสอบกับ:** Aspose.Note for Java 24.12 (ล่าสุด ณ เวลาที่เขียน)  
**ผู้เขียน:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}