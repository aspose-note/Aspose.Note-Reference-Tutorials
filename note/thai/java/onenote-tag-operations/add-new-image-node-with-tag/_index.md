---
title: เพิ่มโหนดรูปภาพใหม่พร้อมแท็กใน OneNote - Aspose.Note
linktitle: เพิ่มโหนดรูปภาพใหม่พร้อมแท็กใน OneNote - Aspose.Note
second_title: Aspose.Note Java API
description: เรียนรู้วิธีเพิ่มโหนดรูปภาพใหม่ด้วยแท็กใน OneNote โดยใช้ Aspose.Note for Java ยกระดับทักษะการเขียนโปรแกรม Java ของคุณได้อย่างง่ายดาย
weight: 10
url: /th/java/onenote-tag-operations/add-new-image-node-with-tag/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# เพิ่มโหนดรูปภาพใหม่พร้อมแท็กใน OneNote - Aspose.Note

## การแนะนำ
ในขอบเขตของการเขียนโปรแกรม Java Aspose.Note โดดเด่นในฐานะเครื่องมืออันทรงพลังสำหรับการจัดการเอกสาร OneNote ได้อย่างง่ายดาย หากคุณต้องการพัฒนาทักษะของคุณและเรียนรู้วิธีเพิ่มโหนดรูปภาพใหม่ด้วยแท็กใน OneNote โดยใช้ Aspose.Note คุณมาถูกที่แล้ว คำแนะนำทีละขั้นตอนนี้จะแนะนำคุณตลอดกระบวนการ เพื่อให้มั่นใจว่าคุณจะเข้าใจแต่ละแนวคิดได้อย่างถี่ถ้วน
## ข้อกำหนดเบื้องต้น
ก่อนที่เราจะเจาะลึกบทช่วยสอน เรามาตรวจสอบให้แน่ใจว่าคุณมีทุกสิ่งที่คุณต้องการ:
1.  Aspose.Note สำหรับ Java: ตรวจสอบให้แน่ใจว่าคุณได้ติดตั้งไลบรารี Aspose.Note แล้ว ถ้าไม่คุณสามารถดาวน์โหลดได้[ที่นี่](https://releases.aspose.com/note/java/).
2. สภาพแวดล้อมการพัฒนา Java: ตรวจสอบให้แน่ใจว่าคุณได้ตั้งค่าสภาพแวดล้อมการพัฒนา Java ที่ใช้งานได้บนเครื่องของคุณ
ตอนนี้เรามีข้อกำหนดเบื้องต้นแล้ว มาดูขั้นตอนถัดไปกันดีกว่า
## แพ็คเกจนำเข้า
ในโปรเจ็กต์ Java ของคุณ ให้เริ่มด้วยการอิมพอร์ตแพ็คเกจที่จำเป็น:
```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.Image;
import com.aspose.note.NoteTag;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.SaveFormat;
import com.aspose.note.TagIcon;
```
## ขั้นตอนที่ 1: สร้างวัตถุเอกสาร
```java
// เส้นทางไปยังไดเร็กทอรีเอกสาร
String dataDir = "Your Document Directory";
// สร้างวัตถุของคลาสเอกสาร
Document doc = new Document();
```
## ขั้นตอนที่ 2: เริ่มต้นวัตถุคลาสหน้า
```java
// เริ่มต้นวัตถุคลาสหน้า
Page page = new Page();
```
## ขั้นตอนที่ 3: เริ่มต้นออบเจ็กต์ Outline Class
```java
// เริ่มต้นวัตถุคลาสเค้าร่าง
Outline outline = new Outline();
```
## ขั้นตอนที่ 4: เริ่มต้นวัตถุคลาส OutlineElement
```java
// เริ่มต้นวัตถุคลาส OutlineElement
OutlineElement outlineElem = new OutlineElement();
```
## ขั้นตอนที่ 5: โหลดและแทรกรูปภาพ
```java
// โหลดรูปภาพ
Image image = new Image(null, dataDir + "Input.jpg");
// แทรกรูปภาพในโหนดเอกสาร
outlineElem.appendChildLast(image);
```
## ขั้นตอนที่ 6: เพิ่มแท็กหมายเหตุลงในรูปภาพ
```java
// เพิ่มแท็กบันทึกรูปดาวสีเหลืองให้กับรูปภาพ
NoteTag noteTag = NoteTag.createYellowStar();
image.getTags().add(noteTag);
```
## ขั้นตอนที่ 7: เพิ่มโหนดองค์ประกอบโครงร่าง
```java
// เพิ่มโหนดองค์ประกอบเค้าร่าง
outline.appendChildLast(outlineElem);
```
## ขั้นตอนที่ 8: เพิ่มโหนดเค้าร่าง
```java
// เพิ่มโหนดเค้าร่าง
page.appendChildLast(outline);
```
## ขั้นตอนที่ 9: เพิ่มโหนดหน้า
```java
// เพิ่มโหนดหน้า
doc.appendChildLast(page);
```
## ขั้นตอนที่ 10: บันทึกเอกสาร OneNote
```java
// บันทึกเอกสาร OneNote เป็น PDF
doc.save(dataDir + "AddNewImageNodeWithTag_out.pdf", SaveFormat.Pdf);
```
ยินดีด้วย! คุณได้เพิ่มโหนดรูปภาพใหม่ด้วยแท็กใน OneNote เรียบร้อยแล้วโดยใช้ Aspose.Note สำหรับ Java
## บทสรุป
 Mastering Aspose.Note สำหรับ Java เปิดโอกาสที่น่าตื่นเต้นในการจัดการเอกสาร OneNote เมื่อทำตามบทช่วยสอนนี้ คุณจะได้รับทักษะเชิงปฏิบัติที่สามารถนำไปใช้กับโครงการต่างๆ ได้ สำรวจเอกสารประกอบของ Aspose.Note ต่อไป[ที่นี่](https://reference.aspose.com/note/java/)สำหรับคุณสมบัติและความเป็นไปได้ขั้นสูงเพิ่มเติม
## คำถามที่พบบ่อย
### ฉันจะหาเอกสารประกอบของ Aspose.Note ได้ที่ไหน
 คุณสามารถค้นหาเอกสาร[ที่นี่](https://reference.aspose.com/note/java/).
### ฉันจะดาวน์โหลด Aspose.Note สำหรับ Java ได้อย่างไร
 คุณสามารถดาวน์โหลดได้จากหน้าเผยแพร่[ที่นี่](https://releases.aspose.com/note/java/).
### มีการทดลองใช้ฟรีหรือไม่?
 ใช่ คุณสามารถเข้าถึงการทดลองใช้ฟรีได้[ที่นี่](https://releases.aspose.com/).
### ฉันจะรับการสนับสนุนสำหรับ Aspose.Note ได้ที่ไหน
 เยี่ยมชมฟอรั่มชุมชน[ที่นี่](https://forum.aspose.com/c/note/28) สำหรับการสนับสนุน
### ฉันจำเป็นต้องมีใบอนุญาตชั่วคราวหรือไม่?
 หากจำเป็น คุณสามารถขอรับใบอนุญาตชั่วคราวได้[ที่นี่](https://purchase.aspose.com/temporary-license/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
