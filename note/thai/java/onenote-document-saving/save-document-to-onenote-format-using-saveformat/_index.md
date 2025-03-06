---
title: บันทึกเอกสารลงใน OneNote โดยใช้ SaveFormat - Aspose.Note
linktitle: บันทึกเอกสารลงใน OneNote โดยใช้ SaveFormat - Aspose.Note
second_title: Aspose.Note Java API
description: เรียนรู้วิธีบันทึกเอกสารเป็นรูปแบบ OneNote โดยใช้ Aspose.Note สำหรับ Java ปฏิบัติตามบทช่วยสอนทีละขั้นตอนนี้เพื่อการผสานรวมเข้ากับแอปพลิเคชัน Java ของคุณได้อย่างราบรื่น
weight: 12
url: /th/java/onenote-document-saving/save-document-to-onenote-format-using-saveformat/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# บันทึกเอกสารลงใน OneNote โดยใช้ SaveFormat - Aspose.Note

## การแนะนำ

Aspose.Note for Java เป็นไลบรารีอันทรงพลังที่ช่วยให้นักพัฒนาสามารถทำงานกับไฟล์ Microsoft OneNote โดยทางโปรแกรม การบันทึกเอกสารเป็นรูปแบบ OneNote โดยใช้ SaveFormat เป็นกระบวนการที่ไม่ซับซ้อน ในบทช่วยสอนนี้ เราจะอธิบายขั้นตอนที่จำเป็นเพื่อให้งานนี้สำเร็จ

## ข้อกำหนดเบื้องต้น

ก่อนที่เราจะเริ่ม ตรวจสอบให้แน่ใจว่าคุณมีสิ่งต่อไปนี้:

1. ติดตั้ง Java Development Kit (JDK) บนระบบของคุณ
2.  Aspose.Note สำหรับไลบรารี Java ที่ดาวน์โหลด คุณสามารถรับได้จาก[ที่นี่](https://releases.aspose.com/note/java/).
3. ความเข้าใจพื้นฐานเกี่ยวกับภาษาการเขียนโปรแกรม Java

## แพ็คเกจนำเข้า

 ขั้นแรก คุณต้องนำเข้าแพ็คเกจที่จำเป็นลงในโปรเจ็กต์ Java ของคุณ ซึ่งรวมถึงการนำเข้าไฟล์`com.aspose.note` แพ็คเกจสำหรับการทำงานกับฟังก์ชัน Aspose.Note

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.SaveFormat;
```

## ขั้นตอนที่ 1: ตั้งค่าไดเร็กทอรีเอกสาร

กำหนดไดเร็กทอรีที่มีเอกสารของคุณอยู่ และตำแหน่งที่คุณต้องการบันทึกไฟล์เอาต์พุต

```java
String dataDir = "Your Document Directory";
```

## ขั้นตอนที่ 2: โหลดเอกสาร

 โหลดเอกสารลงในแอปพลิเคชัน Java ของคุณโดยใช้`Document` คลาสจัดทำโดย Aspose.Note

```java
Document document = new Document(dataDir + "Sample1.one");
```

## ขั้นตอนที่ 3: บันทึกเอกสารเป็นรูปแบบ OneNote

บันทึกเอกสารที่โหลดเป็นรูปแบบ OneNote โดยใช้`save` และระบุรูปแบบไฟล์เอาต์พุตที่ต้องการเป็น`SaveFormat.One`.

```java
document.save(dataDir + "SaveDocToOneNoteFormatUsingSaveformat_out.one", SaveFormat.One);
```

## บทสรุป

ในบทช่วยสอนนี้ เราได้เรียนรู้วิธีบันทึกเอกสารเป็นรูปแบบ OneNote โดยใช้ SaveFormat ใน Aspose.Note สำหรับ Java ด้วยการทำตามขั้นตอนง่ายๆ เหล่านี้ คุณสามารถรวมฟังก์ชันการทำงานนี้เข้ากับแอปพลิเคชัน Java ของคุณได้อย่างราบรื่น

## คำถามที่พบบ่อย

### คำถามที่ 1: Aspose.Note สำหรับ Java เข้ากันได้กับ Microsoft OneNote ทุกเวอร์ชันหรือไม่

ตอบ 1: Aspose.Note for Java รองรับ Microsoft OneNote เวอร์ชันต่างๆ เพื่อให้มั่นใจถึงความเข้ากันได้ในสภาพแวดล้อมที่แตกต่างกัน

### คำถามที่ 2: ฉันสามารถลองใช้ Aspose.Note สำหรับ Java ก่อนที่จะซื้อได้หรือไม่

 ตอบ 2: ได้ คุณสามารถดาวน์โหลด Aspose.Note สำหรับ Java เวอร์ชันทดลองใช้ฟรีได้จาก[ที่นี่](https://releases.aspose.com/).

### คำถามที่ 3: ฉันจะหาเอกสารสำหรับ Aspose.Note สำหรับ Java ได้ที่ไหน

 A3: สามารถดูเอกสารประกอบโดยละเอียดสำหรับ Aspose.Note สำหรับ Java ได้[ที่นี่](https://reference.aspose.com/note/java/).

### คำถามที่ 4: ฉันจะได้รับการสนับสนุนด้านเทคนิคสำหรับ Aspose.Note สำหรับ Java ได้อย่างไร

 A4: สำหรับความช่วยเหลือและการสนับสนุนด้านเทคนิค คุณสามารถไปที่ฟอรัม Aspose.Note[ที่นี่](https://forum.aspose.com/c/note/28).

### คำถามที่ 5: มีตัวเลือกสิทธิ์การใช้งานชั่วคราวสำหรับ Aspose.Note สำหรับ Java หรือไม่

 A5: ได้ คุณสามารถขอรับใบอนุญาตชั่วคราวสำหรับ Aspose.Note สำหรับ Java ได้[ที่นี่](https://purchase.aspose.com/temporary-license/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
