---
date: 2026-01-15
description: เรียนรู้วิธีติดตามการเปลี่ยนแปลงใน OneNote และจัดการการแก้ไขหน้าในเอกสาร
  OneNote ด้วย Aspose.Note สำหรับ Java รวมตัวอย่างสรุปการแก้ไขและวิธีการแก้ไขวันที่ของการแก้ไข
linktitle: Working with Page Revisions in OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: ติดตามการเปลี่ยนแปลง OneNote – จัดการการแก้ไขหน้าโดยใช้ Aspose.Note
url: /th/java/onenote-page-manipulation/working-with-page-revisions/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# ทำงานกับการแก้ไขหน้าใน OneNote - Aspose.Note

## การแนะนำ

OneNote การเปลี่ยนแปลงโครงสร้างสำหรับโน้ตและเมื่อจำเป็น **track การเปลี่ยนแปลง onenote** จะทำให้หน้ามีความสำคัญสำหรับการควบคุมอย่างมีประสิทธิภาพด้วย Aspose.Note สำหรับ Java คุณจะเข้าใจถึงประสิทธิภาพของโปรแกรมว่าใครแก้ไขหน้า และปรับแต่งเวลาได้อย่างเต็มที่แนะนำบทที่พาคุณผ่านแต่ละขั้นตอนในการพิจารณาเอกสารจนกว่าจะสรุปได้ทั้งหมด

## คำตอบด่วน
- **“ติดตามการเปลี่ยนแปลง onenote” สำหรับอะไร?** ตรวจสอบว่าใครแก้ไขหน้า OneNote และเมื่อใด
- **ต้องใช้ไลบรารีอะไร?** Aspose.Note สำหรับ Java
- **ฉันมักจะต้องติดตามหรือวันที่ของผลิตภัณฑ์ใดบ้าง?** ต้องอาศัย RevisionSummary API (`แก้ไขวันที่แก้ไข`)
- **ฉันต้องมีไฟล์ OneNote ล่วงหน้าหรือไม่** สามารถตรวจสอบไฟล์ `.one` อธิบายได้
- **ต้องการและจำเป็นต้องมีจริงหรือไม่?** จำเป็นต้องมีอีกครั้งหมายเหตุสำหรับเรื่องนี้

## ตัวอย่างสรุปการแก้ไขคืออะไร?
A *สรุปการแก้ไข* ข้อมูลเพิ่มเติมเมตาเกี่ยวกับการเปลี่ยนแปลงล่าสุดบนหน้า—ชื่อดังกล่าว, เวลาแก้ไขล่าสุด, และรายละเอียดอื่นๆ ในคู่มือนี้เราจะดึงและแสดงข้อมูลนั้น, จะต้องทราบวิธี **แก้ไขวันที่แก้ไข**.

## เหตุใดจึงติดตามการเปลี่ยนแปลง onenote ด้วย Aspose.Note
- **การทำงานร่วมกัน:** ว่าใครทำอย่างรวดเร็วอย่างรวดเร็ว
- **การตรวจสอบ:** บันทึกประวัติการเปลี่ยนแปลงเพื่อตรวจสอบข้อกำหนด
- **ระบบอัตโนมัติ:** การจัดการกับบริการแบ็กเอนด์หรือเครื่องมือนั้นจะเป็นข้อมูล

## ข้อกำหนดเบื้องต้น

### และยังคงมีการพัฒนา Java
เรียนรู้การติดตั้ง Java Development Kit (JDK) บนระบบของคุณแล้ว

### ไลบรารี Aspose.Note สำหรับ Java
ดาวน์โหลดรวมไลบรารี Aspose.Note for Java จาก [ที่นี่](https://releases.aspose.com/note/java/)

### เอกสาร OneNote
เอกสาร OneNote อธิบายสำหรับการทดสอบ

## แพคเกจนำเข้า

ในโปรเจ็กต์ Java ของคุณ ให้นำเข้าแพ็คเกจที่จำเป็นเพื่อทำงานกับ Aspose.Note สำหรับ Java

```java
import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.RevisionSummary;
import java.io.IOException;
import java.util.Calendar;
```

เรามาแยกตัวอย่างที่ให้มาออกเป็นหลายขั้นตอนเพื่อความเข้าใจที่ชัดเจน

## ขั้นตอนที่ 1: โหลดเอกสาร OneNote

ขั้นแรก โหลดเอกสาร OneNote และดึงหน้าย่อยแรกออกมา

```java
String dataDir = "Your Document Directory";
Document document = new Document(dataDir + "Sample1.one");
Page page = document.getFirstChild();
```

## ขั้นตอนที่ 2: อ่านสรุปการแก้ไขหน้า

อ่านสรุปการแก้ไขเนื้อหาของหน้า นี่คือ **ตัวอย่างสรุปการแก้ไข** ที่แสดงว่าใครเป็นผู้แก้ไขหน้าล่าสุด

```java
RevisionSummary pageRevisionInfo = page.getPageContentRevisionSummary();
System.out.println(String.format("Author:\t%s\nModified:\t%s",
        pageRevisionInfo.getAuthorMostRecent(),
        pageRevisionInfo.getLastModifiedTime().toString()));
```

## ขั้นตอนที่ 3: อัปเดตสรุปการแก้ไขหน้า

อัปเดตสรุปการแก้ไขหน้าด้วยผู้เขียนใหม่และวันที่แก้ไขใหม่ ตัวอย่างนี้แสดงวิธีการ **แก้ไขวันที่แก้ไข** โดยใช้โปรแกรม

```java
pageRevisionInfo.setAuthorMostRecent("New Author");
Calendar modifiedDate = Calendar.getInstance();
pageRevisionInfo.setLastModifiedTime(modifiedDate.getTime());
document.save(dataDir + "WorkingWithPageRevisions_out.one");
```

## บทสรุป

ต้องที่หน้าในเอกสาร OneNote ด้วยโปรแกรมที่ต้องใช้ด้วย Aspose.Note for Java ต้องใช้ขั้นตอนในบทแนะนำนี้ทำอะไร **ติดตามการเปลี่ยนแปลง onenote** ได้อย่างมีประสิทธิภาพ, เจาะลึก, และอย่างเป็นทางการ **แก้ไขวันที่แก้ไข** ช่วยให้คุณสามารถทำงานของคุณได้

## คำถามที่พบบ่อย

### Q1: ฉันสามารถใช้ Aspose.Note for Java กับไลบรารี Java อย่างอื่นได้หรือไม่?
ตอบ: ทดสอบ, Aspose.Note สำหรับ Java ความสามารถของไลบรารี Java อื่นๆ เพื่อเพิ่มฟังก์ชั่นการทำงาน

### Q2: Aspose.Note for Java รองรับการตรวจสอบเอกสาร OneNote ได้หรือไม่?
ตอบ: Aspose.Note สำหรับ Java รองรับหลายบันทึกของเอกสาร OneNote และบันทึกเก่า

### Q3: Aspose.Note for Java รองรับระดับองค์กรหรือไม่?
ตอบ: แน่นอน, Aspose.Note สำหรับ Java ความต้องการของรองรับแอปพลิเคชันระดับองค์กรด้วยคุณสมบัติและการขยายการขยาย

### คำถามที่ 4: ฉันต้องทำตามความต้องการของหน้า Aspose.Note สำหรับ Java สามารถทำได้หรือไม่
ตอบ: พิสูจน์ได้ว่าเราสามารถปรับแต่งหน้าให้ตรงตามความต้องการของคุณ Aspose.Note สำหรับ Java

### Q5: ฉันหาแหล่งสนับสนุนสำหรับ Aspose.Note สำหรับ Java จากที่ไหน?
ตอบ: เรายินดีรับสำหรับ Aspose.Note for Java จาก [ฟอรัม Aspose.Note](https://forum.aspose.com/c/note/28)

---

**อัปเดตล่าสุด:** 15-01-2026
**ทดสอบกับ:** Aspose.Note สำหรับ Java 24.12
**ผู้เขียน:** สมมติ  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}