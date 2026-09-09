---
date: 2026-02-28
description: เรียนรู้วิธีดึงแท็กจากไฟล์ OneNote ด้วย Aspose.Note สำหรับ Java บทแนะนำนี้แสดงวิธีโหลดไฟล์
  OneNote, ดึงแท็กของ OneNote, และแก้ไขแท็กของ OneNote อย่างมีประสิทธิภาพ
linktitle: How to Extract Tags from OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: วิธีดึงแท็กจาก OneNote ด้วย Aspose.Note
url: /th/java/onenote-tag-operations/get-node-tags/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# วิธีการดึงแท็กจาก OneNote ด้วย Aspose.Note

## บทนำ
หากคุณต้องการ **วิธีการดึงแท็ก** จากเอกสาร OneNote คุณมาถูกที่แล้ว ในคู่มือนี้เราจะอธิบายขั้นตอนทั้งหมดของการโหลดไฟล์ OneNote, การดึงแท็กของ OneNote, และแม้กระทั่งการแก้ไขแท็กเหล่านั้นโดยใช้ Aspose.Note สำหรับ Java เมื่อจบบทเรียนคุณจะสามารถผสานการดึงแท็กเข้าไปในแอปพลิเคชัน Java ใดก็ได้อย่างมั่นใจ

## คำตอบสั้น
- **คลาสหลักสำหรับเปิดไฟล์ OneNote คืออะไร?** `Document`
- **เมธอดใดที่คืนค่า RichText nodes ทั้งหมด?** `doc.getChildNodes(RichText.class)`
- **คุณสามารถอ่านเวลาสร้างของ NoteTag ได้หรือไม่?** ใช่, ผ่าน `noteTag.getCreationTime()`
- **ฉันต้องใช้ไลเซนส์สำหรับการใช้งานในผลิตภัณฑ์หรือไม่?** ใช่, จำเป็นต้องมีไลเซนส์ Aspose.Note ที่ถูกต้อง
- **API นี้เข้ากันได้กับ Java 8 และรุ่นต่อไปหรือไม่?** แน่นอน, รองรับเวอร์ชัน Java สมัยใหม่

## “วิธีการดึงแท็ก” ใน OneNote คืออะไร?
การดึงแท็กหมายถึงการอ่านเมตาดาต้า (เช่น สถานะ, ป้าย, ไอคอน, และเวลา) ที่ OneNote แนบไว้กับย่อหน้า, กล่องทำเครื่องหมาย, หรือองค์ประกอบเนื้อหาอื่น ๆ แท็กเหล่านี้จะถูกเก็บเป็นอ็อบเจ็กต์ `NoteTag` ภายในโหนด `RichText`

## ทำไมต้องใช้ Aspose.Note สำหรับการดึงแท็ก?
- **ไม่จำเป็นต้องติดตั้ง OneNote** – ทำงานโดยตรงกับไฟล์ .one
- **การควบคุมเต็มรูปแบบ** – ดึง, อ่าน, และแก้ไขคุณสมบัติของแท็กโดยโปรแกรม
- **ข้ามแพลตฟอร์ม** – ทำงานบนระบบปฏิบัติการใดก็ได้ที่รองรับ Java

## ข้อกำหนดเบื้องต้น
- สภาพแวดล้อมการพัฒนา Java (JDK 8+).
- ไลบรารี Aspose.Note ที่ดาวน์โหลดจาก [ที่นี่](https://releases.aspose.com/note/java/).
- เอกสาร OneNote ตัวอย่าง (เช่น `Sample1.one`) ที่วางไว้ในไดเรกทอรีที่รู้จัก.

## นำเข้าแพ็กเกจ
เริ่มต้นด้วยการนำเข้าคลาสที่คุณต้องการ การนำเข้าต่าง ๆ นี้จะให้คุณเข้าถึงการจัดการเอกสาร, อินเทอร์เฟซของแท็ก, และโหนด rich‑text

```java
import java.io.IOException;
import java.util.List;
import com.aspose.note.Document;
import com.aspose.note.ITag;
import com.aspose.note.NoteTag;
import com.aspose.note.RichText;
```

## วิธีการโหลดไฟล์ OneNote
ขั้นตอนแรกคือการโหลดไฟล์ OneNote เข้าไปในอ็อบเจ็กต์ `Document`

```java
// The path to the documents directory.
String dataDir = "Your Document Directory";
// Load the document into Aspose.Note
Document doc = new Document(dataDir + "Sample1.one");
// Get all RichText nodes
List<RichText> nodes = doc.getChildNodes(RichText.class);
// Load the document into Aspose.Note
Document doc = new Document(dataDir + "Sample1.one");
```

> **เคล็ดลับ:** ให้เก็บเส้นทาง `dataDir` เป็นแบบเต็มหรือใช้ `Paths.get(...)` เพื่อหลีกเลี่ยงข้อผิดพลาดที่เกี่ยวกับเส้นทาง

## วิธีการดึงแท็กของ OneNote
หลังจากโหลดเอกสารแล้ว ให้ดึงโหนด `RichText` ทั้งหมด โหนดแต่ละอันอาจมีหนึ่งหรือหลายแท็ก

```java
// Get all RichText nodes
List<RichText> nodes = doc.getChildNodes(RichText.class);
```

## วนลูปผ่านแต่ละโหนด
วนลูปผ่านโหนด `RichText` แต่ละอันเพื่อตรวจสอบแท็กของมัน

```java
// Iterate through each node
for (RichText richText : nodes) {
    // Process each node here
}
```

## ดึง Note Tags (วิธีการแก้ไขแท็กของ OneNote)
ภายในลูป ให้ตรวจสอบว่าแท็กเป็น `NoteTag` หรือไม่ หากเป็นคุณสามารถอ่านคุณสมบัติของมัน—หรือแก้ไขได้หากต้องการ

```java
for (ITag tag : richText.getTags()) {
    if (tag.getClass() == NoteTag.class) {
        NoteTag noteTag = (NoteTag) tag;
        // Retrieve properties
        System.out.println("Completed Time: " + noteTag.getCompletedTime());
        System.out.println("Create Time: " + noteTag.getCreationTime());
        System.out.println("Font Color: " + noteTag.getFontColor());
        System.out.println("Status: " + noteTag.getStatus());
        System.out.println("Label: " + noteTag.getLabel());
        System.out.println("Icon: " + noteTag.getIcon());
        System.out.println("High Light: " + noteTag.getHighlight());
        // Example of modifying a property
        // noteTag.setLabel("Updated Label");
    }
}
```

> **คำเตือน:** การแก้ไขแท็กจะทำให้เอกสารพื้นฐานเปลี่ยนแปลง จำไว้ว่าให้บันทึกเอกสารหลังจากทำการเปลี่ยนแปลง

## สรุป
ตอนนี้คุณรู้แล้วว่า **วิธีการดึงแท็ก**, วิธี **โหลดไฟล์ OneNote**, วิธี **ดึงแท็กของ OneNote**, และแม้กระทั่งวิธี **แก้ไขแท็กของ OneNote** ด้วย Aspose.Note สำหรับ Java ผสานโค้ดตัวอย่างเหล่านี้เข้ากับโปรเจกต์ของคุณเพื่อทำการวิเคราะห์โน้ต, รายงาน, หรืองานย้ายข้อมูลโดยอัตโนมัติ

## คำถามที่พบบ่อย
### Aspose.Note รองรับทุกเวอร์ชันของ OneNote หรือไม่?
Aspose.Note รองรับรูปแบบไฟล์ OneNote ต่าง ๆ เพื่อให้แน่ใจว่ามีความเข้ากันได้กับหลายเวอร์ชัน

### ฉันสามารถแก้ไขคุณสมบัติของ NoteTag ที่ดึงมาได้หรือไม่?
ได้, Aspose.Note อนุญาตให้คุณแก้ไขและอัปเดตคุณสมบัติของ NoteTag ผ่านโปรแกรม

### มีเวอร์ชันทดลองของ Aspose.Note หรือไม่?
แน่นอน! คุณสามารถเข้าถึงเวอร์ชันทดลองฟรีได้ที่ [ที่นี่](https://releases.aspose.com/).

### ฉันจะหาเอกสารประกอบที่ครอบคลุมสำหรับ Aspose.Note สำหรับ Java ได้จากที่ไหน?
สำรวจเอกสารรายละเอียดได้ที่ [ที่นี่](https://reference.aspose.com/note/java/).

### ฉันจะขอรับการสนับสนุนสำหรับปัญหาหรือคำถามใด ๆ ได้อย่างไร?
ไปที่ฟอรั่มสนับสนุนได้ที่ [ที่นี่](https://forum.aspose.com/c/note/28) เพื่อรับความช่วยเหลือจากชุมชน Aspose.

## คำถามที่พบบ่อย
**Q:** *ฉันสามารถดึงแท็กจากไฟล์ OneNote ที่ป้องกันด้วยรหัสผ่านได้หรือไม่?*  
**A:** ใช่, ให้ระบุรหัสผ่านเมื่อสร้างอ็อบเจ็กต์ `Document`.

**Q:** *ฉันต้องเรียกเมธอดบันทึกหลังจากแก้ไขแท็กหรือไม่?*  
**A:** แน่นอน. ใช้ `doc.save("UpdatedSample.one");` เพื่อบันทึกการเปลี่ยนแปลง

**Q:** *สามารถกรองแท็กตามสถานะได้หรือไม่?*  
**A:** คุณสามารถตรวจสอบ `noteTag.getStatus()` ภายในลูปและประมวลผลเฉพาะสถานะที่ต้องการ

**Q:** *จะเกิดอะไรขึ้นหากโหนด RichText ไม่มีแท็ก?*  
**A:** `richText.getTags()` จะคืนค่าคอลเลกชันว่าง; ลูปจะข้ามไปโดยอัตโนมัติ

**Q:** *ฉันสามารถประมวลผลหลายไฟล์ OneNote เป็นชุดได้หรือไม่?*  
**A:** ห่อหุ้มตรรกะข้างต้นในรูทีนการวนไฟล์และจัดการแต่ละเอกสารตามลำดับ

---

**อัปเดตล่าสุด:** 2026-02-28  
**ทดสอบด้วย:** Aspose.Note for Java 24.12  
**ผู้เขียน:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}