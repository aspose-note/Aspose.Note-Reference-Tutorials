---
title: รับงาน Outlook ใน OneNote - Aspose.Note
linktitle: รับงาน Outlook ใน OneNote - Aspose.Note
second_title: Aspose.Note Java API
description: สำรวจศักยภาพของ Aspose.Note สำหรับ Java ในการดึงรายละเอียดงาน Outlook ออกจากเอกสาร OneNote ได้อย่างง่ายดาย ยกระดับการพัฒนา Java ของคุณด้วยไลบรารีที่แข็งแกร่งนี้
type: docs
weight: 10
url: /th/java/onenote-text-manipulation/get-outlook-task/
---
## การแนะนำ
ยินดีต้อนรับสู่โลกของ Aspose.Note สำหรับ Java – เครื่องมืออันทรงพลังที่ช่วยให้นักพัฒนา Java สามารถทำงานกับไฟล์ Microsoft OneNote ได้อย่างราบรื่น ในคำแนะนำทีละขั้นตอนนี้ เราจะแนะนำคุณตลอดกระบวนการแยกข้อมูลงาน Outlook จากเอกสาร OneNote โดยใช้ Aspose.Note for Java
## ข้อกำหนดเบื้องต้น
ก่อนที่จะเข้าสู่บทช่วยสอน ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:
- Java Development Kit (JDK): ตรวจสอบให้แน่ใจว่าคุณได้ติดตั้ง Java บนระบบของคุณแล้ว
-  Aspose.Note สำหรับ Java: ดาวน์โหลดและติดตั้งไลบรารี Aspose.Note จาก[หน้าดาวน์โหลด](https://releases.aspose.com/note/java/).
## แพ็คเกจนำเข้า
เริ่มต้นด้วยการนำเข้าแพ็คเกจที่จำเป็นไปยังโปรเจ็กต์ Java ของคุณ เพิ่มบรรทัดต่อไปนี้ที่จุดเริ่มต้นของไฟล์ Java ของคุณ:
```java
import java.io.IOException;
import java.util.List;
import com.aspose.note.Document;
import com.aspose.note.ITag;
import com.aspose.note.NoteTask;
import com.aspose.note.RichText;
```
## ขั้นตอนที่ 1: ตั้งค่าโครงการของคุณ
สร้างโปรเจ็กต์ Java ใหม่และรวมไลบรารี Aspose.Note ในการขึ้นต่อกันของโปรเจ็กต์ของคุณ ตรวจสอบให้แน่ใจว่าโครงสร้างโครงการของคุณได้รับการจัดระเบียบ และคุณมีไดเร็กทอรีเฉพาะสำหรับเอกสารของคุณ
## ขั้นตอนที่ 2: โหลดเอกสาร OneNote
ใช้รหัสต่อไปนี้เพื่อโหลดเอกสาร OneNote ของคุณลงใน Aspose หมายเหตุ:
```java
String dataDir = "Your Document Directory";
Document doc = new Document(dataDir + "Sample1.one");
```
ตรวจสอบให้แน่ใจว่าได้แทนที่ "Your Document Directory" ด้วยเส้นทางไปยังเอกสาร OneNote ของคุณ
## ขั้นตอนที่ 3: ดึงข้อมูลโหนด RichText
แยกโหนด RichText ทั้งหมดออกจากเอกสารโดยใช้รหัสต่อไปนี้:
```java
List<RichText> nodes = (List<RichText>) doc.getChildNodes(RichText.class);
```
## ขั้นตอนที่ 4: วนซ้ำแต่ละโหนด
วนซ้ำแต่ละโหนด RichText และระบุว่ามีแท็ก NoteTask หรือไม่:
```java
for (RichText richText : nodes) {
    for (ITag tag : richText.getTags()) {
        if (tag.getClass() == NoteTask.class) {
            // รหัสของคุณเพื่อจัดการ NoteTask
        }
    }
}
```
## ขั้นตอนที่ 5: ดึงคุณสมบัติงาน
ดึงข้อมูลและพิมพ์คุณสมบัติต่างๆ ของ NoteTask เช่น เวลาที่เสร็จสมบูรณ์ เวลาการสร้าง วันที่ครบกำหนด สถานะ และไอคอน:
```java
NoteTask noteTask = (NoteTask) tag;
System.out.println("Completed Time: " + noteTask.getCompletedTime());
System.out.println("Create Time: " + noteTask.getCreationTime());
System.out.println("Due Date: " + noteTask.getDueDate());
System.out.println("Status: " + noteTask.getStatus());
System.out.println("Icon: " + noteTask.getIcon());
```
ทำซ้ำขั้นตอนนี้สำหรับโหนด NoteTask ทั้งหมดในเอกสาร
## บทสรุป
ยินดีด้วย! คุณได้เรียนรู้วิธีใช้ Aspose.Note สำหรับ Java เพื่อแยกข้อมูลงาน Outlook จากเอกสาร OneNote เรียบร้อยแล้ว ไลบรารีอันทรงพลังนี้เปิดโลกแห่งความเป็นไปได้สำหรับนักพัฒนา Java ที่ทำงานกับไฟล์ Microsoft OneNote
## คำถามที่พบบ่อย
### ถาม: ฉันสามารถใช้ Aspose.Note สำหรับ Java กับเฟรมเวิร์ก Java อื่นๆ ได้หรือไม่
ตอบ: ใช่ Aspose.Note สำหรับ Java เข้ากันได้กับเฟรมเวิร์ก Java ต่างๆ ซึ่งให้ความยืดหยุ่นในการบูรณาการ
### ถาม: Aspose.Note สำหรับ Java มีรุ่นทดลองใช้ฟรีหรือไม่
 ตอบ: ได้ คุณสามารถทดลองใช้ Aspose.Note สำหรับ Java ได้ฟรี[ที่นี่](https://releases.aspose.com/).
### ถาม: ฉันจะรับการสนับสนุน Aspose.Note สำหรับ Java ได้อย่างไร
 ตอบ: เยี่ยมชม[ฟอรั่ม Aspose.Note](https://forum.aspose.com/c/note/28) สำหรับการสนับสนุนจากชุมชนหรือสำรวจตัวเลือกการสนับสนุนระดับพรีเมียม
### ถาม: ฉันจะหาเอกสารโดยละเอียดสำหรับ Aspose.Note สำหรับ Java ได้ที่ไหน
 ตอบ: โปรดดูที่[Aspose.Note สำหรับเอกสารประกอบ Java](https://reference.aspose.com/note/java/) เพื่อข้อมูลเชิงลึก
### ถาม: ฉันจะขอรับใบอนุญาตชั่วคราวสำหรับ Aspose.Note สำหรับ Java ได้อย่างไร
 ตอบ: รับใบอนุญาตชั่วคราวของคุณ[ที่นี่](https://purchase.aspose.com/temporary-license/).