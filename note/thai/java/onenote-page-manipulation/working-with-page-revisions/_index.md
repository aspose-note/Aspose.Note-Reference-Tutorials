---
title: การทำงานกับการแก้ไขหน้าใน OneNote - Aspose.Note
linktitle: การทำงานกับการแก้ไขหน้าใน OneNote - Aspose.Note
second_title: Aspose.Note Java API
description: เรียนรู้วิธีจัดการการแก้ไขหน้าในเอกสาร OneNote โดยใช้ Aspose.Note for Java ให้คำแนะนำทีละขั้นตอนเพื่อการติดตามการแก้ไขและการทำงานร่วมกันอย่างมีประสิทธิภาพ
type: docs
weight: 21
url: /th/java/onenote-page-manipulation/working-with-page-revisions/
---
## การแนะนำ

OneNote เป็นเครื่องมือที่ทรงพลังสำหรับการจัดระเบียบและจัดการบันทึกย่อ แต่บางครั้งคุณจำเป็นต้องแก้ไขเพื่อติดตามการเปลี่ยนแปลงและทำงานร่วมกันอย่างมีประสิทธิภาพ ด้วย Aspose.Note for Java คุณสามารถจัดการการแก้ไขหน้าในเอกสาร OneNote โดยทางโปรแกรมได้อย่างง่ายดาย บทช่วยสอนนี้จะแนะนำคุณตลอดกระบวนการทีละขั้นตอน

## ข้อกำหนดเบื้องต้น

ก่อนที่คุณจะเริ่มต้น ตรวจสอบให้แน่ใจว่าคุณมีสิ่งต่อไปนี้:

### สภาพแวดล้อมการพัฒนาจาวา

ตรวจสอบให้แน่ใจว่าคุณได้ติดตั้ง Java Development Kit (JDK) บนระบบของคุณ

### Aspose.Note สำหรับไลบรารี Java

ดาวน์โหลดและติดตั้ง Aspose.Note สำหรับไลบรารี Java จาก[ที่นี่](https://releases.aspose.com/note/java/).

### เอกสาร OneNote

เตรียมเอกสาร OneNote ตัวอย่างให้พร้อมสำหรับการทดสอบ

## แพ็คเกจนำเข้า

ในโปรเจ็กต์ Java ของคุณ ให้นำเข้าแพ็คเกจที่จำเป็นเพื่อทำงานกับ Aspose.Note สำหรับ Java

```java
import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.RevisionSummary;
import java.io.IOException;
import java.util.Calendar;
```

เราจะแบ่งตัวอย่างที่ให้ไว้ออกเป็นหลายขั้นตอนเพื่อความเข้าใจที่ชัดเจน

## ขั้นตอนที่ 1: โหลดเอกสาร OneNote

ขั้นแรก โหลดเอกสาร OneNote และรับเพจรองหน้าแรก

```java
String dataDir = "Your Document Directory";
Document document = new Document(dataDir + "Sample1.one");
Page page = document.getFirstChild();
```

## ขั้นตอนที่ 2: อ่านสรุปการแก้ไขหน้า

อ่านสรุปการแก้ไขเนื้อหาสำหรับหน้า

```java
RevisionSummary pageRevisionInfo = page.getPageContentRevisionSummary();
System.out.println(String.format("Author:\t%s\nModified:\t%s",
        pageRevisionInfo.getAuthorMostRecent(),
        pageRevisionInfo.getLastModifiedTime().toString()));
```

## ขั้นตอนที่ 3: อัปเดตสรุปการแก้ไขหน้า

อัปเดตสรุปการแก้ไขหน้าด้วยผู้เขียนใหม่และวันที่แก้ไข

```java
pageRevisionInfo.setAuthorMostRecent("New Author");
Calendar modifiedDate = Calendar.getInstance();
pageRevisionInfo.setLastModifiedTime(modifiedDate.getTime());
document.save(dataDir + "WorkingWithPageRevisions_out.one");
```

## บทสรุป

การจัดการการแก้ไขหน้าในเอกสาร OneNote โดยทางโปรแกรมสามารถทำให้ง่ายขึ้นด้วย Aspose.Note for Java เมื่อทำตามขั้นตอนที่ระบุไว้ในบทช่วยสอนนี้ คุณจะทำงานกับการแก้ไขหน้าได้อย่างมีประสิทธิภาพเพื่อติดตามการเปลี่ยนแปลงและทำงานร่วมกันได้อย่างราบรื่น

## คำถามที่พบบ่อย

### คำถามที่ 1: ฉันสามารถใช้ Aspose.Note สำหรับ Java กับไลบรารี Java อื่นได้หรือไม่

ตอบ: ได้ Aspose.Note สำหรับ Java สามารถรวมเข้ากับไลบรารี Java อื่น ๆ เพื่อปรับปรุงฟังก์ชันการทำงานได้

### คำถามที่ 2: Aspose.Note สำหรับ Java รองรับเอกสาร OneNote ทุกเวอร์ชันหรือไม่

ตอบ: Aspose.Note for Java รองรับเอกสาร OneNote เวอร์ชันต่างๆ รวมถึงเวอร์ชันเก่าด้วย

### คำถามที่ 3: Aspose.Note สำหรับ Java เหมาะสำหรับแอปพลิเคชันระดับองค์กรหรือไม่

ตอบ: แน่นอนว่า Aspose.Note สำหรับ Java ได้รับการออกแบบมาเพื่อตอบสนองความต้องการของแอปพลิเคชันระดับองค์กรด้วยคุณสมบัติที่แข็งแกร่งและความสามารถในการปรับขนาด

### คำถามที่ 4: ฉันสามารถปรับแต่งการแก้ไขหน้าด้วย Aspose.Note สำหรับ Java ได้หรือไม่

ตอบ: ได้ คุณสามารถปรับแต่งการแก้ไขหน้าได้ตามความต้องการของคุณโดยใช้ Aspose.Note for Java

### คำถามที่ 5: ฉันจะรับการสนับสนุนสำหรับ Aspose.Note สำหรับ Java ได้ที่ไหน

 ตอบ: คุณสามารถรับการสนับสนุนสำหรับ Aspose.Note สำหรับ Java ได้จาก[ฟอรั่ม Aspose.Note](https://forum.aspose.com/c/note/28).