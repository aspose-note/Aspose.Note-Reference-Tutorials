---
title: แยกรูปภาพจากเอกสาร OneNote โดยใช้ Java
linktitle: แยกรูปภาพจากเอกสาร OneNote โดยใช้ Java
second_title: Aspose.Note Java API
description: เรียนรู้วิธีแยกรูปภาพจากเอกสาร OneNote โดยใช้ Java พร้อมไลบรารี Aspose.Note ปฏิบัติตามคำแนะนำทีละขั้นตอนของเราเพื่อการแยกภาพที่ราบรื่น
weight: 14
url: /th/java/onenote-hyperlinks-images/extract-images/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# แยกรูปภาพจากเอกสาร OneNote โดยใช้ Java

## การแนะนำ

ในบทช่วยสอนนี้ เราจะแนะนำคุณตลอดกระบวนการแยกรูปภาพจากเอกสาร OneNote โดยใช้ Java ด้วยความช่วยเหลือของไลบรารี Aspose.Note

## ข้อกำหนดเบื้องต้น

ก่อนที่คุณจะเริ่มต้น ตรวจสอบให้แน่ใจว่าคุณมีสิ่งต่อไปนี้:

1.  Java Development Kit (JDK): ตรวจสอบให้แน่ใจว่าคุณได้ติดตั้ง Java บนระบบของคุณแล้ว คุณสามารถดาวน์โหลดและติดตั้งได้จาก[เว็บไซต์](https://www.oracle.com/java/technologies/javase-jdk15-downloads.html).

2.  ไลบรารี Aspose.Note: ดาวน์โหลดและรวมไลบรารี Aspose.Note ในโปรเจ็กต์ Java ของคุณ คุณสามารถรับได้จาก[ลิ้งค์ดาวน์โหลด](https://releases.aspose.com/note/java/).

## แพ็คเกจนำเข้า

ในการเริ่มต้น ให้นำเข้าแพ็คเกจที่จำเป็น:

```java
import java.io.IOException;
import java.nio.file.Files;
import java.nio.file.Paths;
import java.util.List;
import com.aspose.note.Document;
import com.aspose.note.Image;
```

## ขั้นตอนที่ 1: โหลดเอกสาร

ขั้นแรก โหลดเอกสาร OneNote โดยใช้ Aspose หมายเหตุ:

```java
String dataDir = "Your Document Directory";
Document doc = new Document(dataDir + "Sample1.one");
```

## ขั้นตอนที่ 2: รับรูปภาพทั้งหมด

จากนั้น ให้ดึงภาพทั้งหมดจากเอกสาร:

```java
List<Image> list = doc.getChildNodes(Image.class);
System.out.printf("Total Images: %s\n\n", list.size());
```

## ขั้นตอนที่ 3: แยกรูปภาพ

วนซ้ำรายการรูปภาพและบันทึกแต่ละรูปภาพลงในไฟล์:

```java
for (int i = 0; i < list.size(); i++) {
    Image image = list.get(i);
    String outputFile = "ExtractImages_out" + i + "_" + image.getFileName();
    byte[] buffer = image.getBytes();
    Files.write(Paths.get(dataDir + outputFile), buffer);
    System.out.printf("File saved: %s\n", dataDir);
}
```

## บทสรุป

การแยกรูปภาพออกจากเอกสาร OneNote โดยใช้ Java สามารถทำได้อย่างราบรื่นด้วยไลบรารี Aspose.Note ด้วยการทำตามขั้นตอนที่ระบุไว้ในบทช่วยสอนนี้ คุณสามารถดึงภาพจากเอกสารของคุณเพื่อการประมวลผลหรือการวิเคราะห์เพิ่มเติมได้อย่างง่ายดาย

## คำถามที่พบบ่อย

### คำถามที่ 1: ฉันสามารถแยกรูปภาพออกจากเอกสาร OneNote ที่มีการป้องกันด้วยรหัสผ่านได้หรือไม่

ตอบ 1: ใช่ Aspose.Note รองรับการแยกรูปภาพจากเอกสารที่มีการป้องกันด้วยรหัสผ่านเช่นกัน

### คำถามที่ 2: Aspose.Note เข้ากันได้กับ Java เวอร์ชันต่างๆ หรือไม่

คำตอบ 2: Aspose.Note เข้ากันได้กับ Java เวอร์ชันต่างๆ เพื่อให้เกิดความยืดหยุ่นสำหรับนักพัฒนา

### คำถามที่ 3: ฉันสามารถแยกรูปภาพจากเอกสาร OneNote หลายฉบับในการดำเนินการครั้งเดียวได้หรือไม่

คำตอบ 3: แน่นอน คุณสามารถวนซ้ำเอกสารหลายชุดและแยกรูปภาพจากแต่ละเอกสารได้โดยใช้ Aspose.Note

### คำถามที่ 4: มีข้อจำกัดด้านขนาดสำหรับเอกสาร OneNote หรือไม่

A4: Aspose.Note จัดการเอกสารขนาดต่างๆ ได้อย่างมีประสิทธิภาพ โดยไม่มีข้อจำกัดเกี่ยวกับขนาดเอกสารในการแยกรูปภาพ

### คำถามที่ 5: Aspose.Note รองรับการแยกเนื้อหาประเภทอื่นนอกเหนือจากรูปภาพหรือไม่

A5: ได้ นอกจากรูปภาพแล้ว Aspose.Note ยังอนุญาตให้แยกข้อความ สิ่งที่แนบมา และประเภทเนื้อหาอื่นๆ ออกจากเอกสาร OneNote
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
