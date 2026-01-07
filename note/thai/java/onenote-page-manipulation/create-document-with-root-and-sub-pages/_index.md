---
description: เรียนรู้วิธีบันทึกไฟล์ PDF ของ OneNote และเพิ่มหน้าย่อยใน OneNote โดยใช้
  Aspose.Note สำหรับ Java. ปฏิบัติตามคู่มือขั้นตอนต่อขั้นตอนนี้เพื่อจัดระเบียบบันทึกของคุณอย่างมีประสิทธิภาพ.
linktitle: How to Save OneNote PDF and Add Sub Pages
second_title: Aspose.Note Java API
title: วิธีบันทึก PDF ของ OneNote และเพิ่มหน้าย่อย
url: /th/java/onenote-page-manipulation/create-document-with-root-and-sub-pages/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# วิธีบันทึก OneNote PDF และเพิ่มหน้าย่อย

## บทนำ

ในบทเรียนนี้ คุณจะได้ค้นพบ **วิธีบันทึก OneNote PDF** พร้อมกับสร้างเอกสารที่มีทั้งหน้ารากและหน้าย่อยโดยใช้ Aspose.Note for Java การจัดระเบียบสมุดบันทึก OneNote ของคุณด้วยโครงสร้างชัดเจนทำให้การนำทางเป็นเรื่องง่าย และความสามารถในการส่งออกเป็น PDF ช่วยให้คุณสามารถแชร์บันทึกของคุณในรูปแบบที่ทุกคนอ่านได้อย่างทั่วถึง เราจะสาธิตวิธี **เพิ่มหน้าย่อยแบบ onenote** เพื่อให้คุณสร้างโครงสร้างหลายระดับได้อย่างง่ายดาย

## คำตอบอย่างรวดเร็ว
- **คีย์เวิร์ดหลักหมายถึงอะไร?** หมายถึงการส่งออกสมุด OneNote เป็น PDF ด้วย Aspose.Note  
- **ใช้ API ใด?** Aspose.Note for Java  
- **ฉันสามารถสร้างหน้าที่มีลำดับชั้นได้หรือไม่?** ได้ – ตั้งค่าระดับของหน้าเพื่อสร้างหน้ารากและหน้าย่อย  
- **ต้องมีลิขสิทธิ์หรือไม่?** มีรุ่นทดลองฟรี; ต้องมีลิขสิทธิ์เชิงพาณิชย์สำหรับการใช้งานจริง  
- **รูปแบบผลลัพธ์ที่รองรับคืออะไร?** BMP, PDF, PNG และอื่น ๆ  

## “วิธีบันทึก OneNote PDF” คืออะไร?
การบันทึก OneNote เป็น PDF จะเปลี่ยนหน้าของสมุดบันทึกให้เป็นเอกสารแบบจัดรูปแบบคงที่ที่คงรักษาการจัดรูปแบบ, รูปภาพ, และโครงสร้างลำดับชั้นไว้ เหมาะสำหรับการแชร์, เก็บถาวร, หรือพิมพ์บันทึก

## ทำไมต้องเพิ่มหน้าย่อยใน OneNote?
การเพิ่มหน้าย่อยช่วยให้คุณจัดกลุ่มเนื้อหาที่เกี่ยวข้องภายใต้หน้าพ่อแม่ เหมือนโครงสร้างโฟลเดอร์ ทำให้การจัดระเบียบบันทึกดีขึ้น, การค้นหาเร็วขึ้น, และประสบการณ์การอ่านดีขึ้นเมื่อสมุดบันทึกถูกส่งออกเป็น PDF

## ข้อกำหนดเบื้องต้น

ก่อนเริ่มทำงาน โปรดตรวจสอบว่าคุณมีสิ่งต่อไปนี้:

1. Java Development Kit (JDK): ตรวจสอบว่าคุณได้ติดตั้ง JDK ไว้บนระบบของคุณ  
2. Aspose.Note for Java: ดาวน์โหลดและติดตั้ง Aspose.Note for Java จาก [website](https://purchase.aspose.com/buy)  
3. Integrated Development Environment (IDE): เลือก IDE สำหรับ Java เช่น IntelliJ IDEA, Eclipse, หรือ NetBeans  

## นำเข้าแพ็กเกจ

เริ่มต้นโดยนำเข้าแพ็กเกจที่จำเป็นในโปรเจกต์ Java ของคุณ:

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.SaveFormat;
import com.aspose.note.ParagraphStyle;
```

## ขั้นตอนที่ 1: ตั้งค่าไดเรกทอรีเอกสาร

กำหนดไดเรกทอรีที่คุณต้องการบันทึกเอกสาร OneNote ของคุณ:

```java
String dataDir = "Your Document Directory";
```

## ขั้นตอนที่ 2: สร้างอ็อบเจ็กต์ Document

สร้างอ็อบเจ็กต์ `Document`:

```java
Document doc = new Document();
```

## ขั้นตอนที่ 3: สร้างหน้า

เริ่มต้นอ็อบเจ็กต์หน้าและตั้งค่าระดับของมัน การตั้งค่าระดับจะกำหนดว่าหน้านั้นเป็นหน้ารากหรือหน้าย่อย:

```java
Page page1 = new Page();
page1.setLevel((byte) 1);

Page page2 = new Page();
page2.setLevel((byte) 2);

Page page3 = new Page();
page3.setLevel((byte) 1);
```

## ขั้นตอนที่ 4: เพิ่มโหนดลงในหน้า

### เพิ่มโหนดในหน้าที่หนึ่ง

```java
Outline outline = new Outline();
OutlineElement outlineElem = new OutlineElement();
ParagraphStyle textStyle = new ParagraphStyle()
                                    .setFontColor(Color.black)
                                    .setFontName("David Transparent")
                                    .setFontSize(10);

RichText text = new RichText().append("First page.");
text.setParagraphStyle(textStyle);

outlineElem.appendChildLast(text);
outline.appendChildLast(outlineElem);
page1.appendChildLast(outline);
```

### เพิ่มโหนดในหน้าที่สอง

```java
Outline outline2 = new Outline();
OutlineElement outlineElem2 = new OutlineElement();
ParagraphStyle textStyle2 = new ParagraphStyle()
                                    .setFontColor(Color.black)
                                    .setFontName("David Transparent")
                                    .setFontSize(10);

RichText text2 = new RichText().append("Second page.");
text2.setParagraphStyle(textStyle2);

outlineElem2.appendChildLast(text2);
outline2.appendChildLast(outlineElem2);
page2.appendChildLast(outline2);
```

### เพิ่มโหนดในหน้าที่สาม

```java
Outline outline3 = new Outline();
OutlineElement outlineElem3 = new OutlineElement();
ParagraphStyle textStyle3 = new ParagraphStyle()
                                    .setFontColor(Color.black)
                                    .setFontName("Broadway")
                                    .setFontSize(10);

RichText text3 = new RichText().append("Third page.");
text3.setParagraphStyle(textStyle3);

outlineElem3.appendChildLast(text3);
outline3.appendChildLast(outlineElem3);
page3.appendChildLast(outline3);
```

## ขั้นตอนที่ 5: เพิ่มหน้าเข้าไปในเอกสาร

```java
doc.appendChildLast(page1);
doc.appendChildLast(page2);
doc.appendChildLast(page3);
```

## ขั้นตอนที่ 6: บันทึกเอกสาร

บันทึกเอกสาร OneNote เป็น PDF (หรือ BMP ในตัวอย่างนี้) การเปลี่ยนค่า `SaveFormat` จะทำให้คุณส่งออกเป็น PDF ซึ่งตอบสนองต่อความต้องการ “วิธีบันทึก OneNote PDF”:

```java
try {
    doc.save(dataDir + "GenerateRootAndSubLevelPagesInOneNote_out.bmp", SaveFormat.Bmp);
} catch (IOException e) {
    // Handle exception
}
```

> **เคล็ดลับ:** เพื่อส่งออกเป็น PDF โดยตรง ให้เปลี่ยน `SaveFormat.Bmp` เป็น `SaveFormat.Pdf`.

ยินดีด้วย! คุณได้สร้างเอกสาร OneNote ที่มีหน้ารากและหน้าย่อยสำเร็จแล้วและได้เรียนรู้ **วิธีบันทึก OneNote PDF** ด้วย Aspose.Note for Java

## ทำไมเรื่องนี้ถึงสำคัญ

- **การจัดระเบียบแบบลำดับชั้น:** หน้ารากและหน้าย่อยช่วยให้คุณจำลองโครงสร้างโฟลเดอร์ภายใน OneNote  
- **การส่งออก PDF อย่างราบรื่น:** เมื่อจัดระเบียบแล้ว การส่งออกเป็น PDF จะคงรักษาโครงสร้างลำดับชั้น ทำให้เอกสารสุดท้ายอ่านง่ายและแชร์ได้สะดวก  
- **การอัตโนมัติ:** โค้ดนี้สามารถรวมเข้าไปในแอปพลิเคชัน Java ขนาดใหญ่ได้ ช่วยสร้างสมุดบันทึกที่มีโครงสร้างเป็นชุดได้อย่างอัตโนมัติ  

## ข้อผิดพลาดทั่วไปและวิธีหลีกเลี่ยง

| ปัญหา | สาเหตุ | วิธีแก้ |
|-------|-------|----------|
| หน้าปรากฏในระดับเดียวกัน | ค่า `setLevel` ไม่ถูกต้อง | ใช้ `setLevel((byte) 1)` สำหรับหน้ารากและ `setLevel((byte) 2)` (หรือสูงกว่า) สำหรับหน้าย่อย |
| ผลลัพธ์ PDF เป็นสีขาวเปล่า | ขาด `SaveFormat.Pdf` หรือเส้นทางไฟล์ไม่ถูกต้อง | ตรวจสอบว่าไดเรกทอรีมีอยู่และใช้ `SaveFormat.Pdf` |
| ฟอนต์ไม่ถูกนำไปใช้ | ชื่อฟอนต์ผิดหรือไม่มีฟอนต์บนระบบ | ตรวจสอบว่าฟอนต์ (เช่น “David Transparent”) ถูกติดตั้งบนเครื่องที่รันโค้ด |

## คำถามที่พบบ่อย

**ถาม: ฉันสามารถสร้างหลายระดับของหน้าย่อยโดยใช้ Aspose.Note for Java ได้หรือไม่?**  
ตอบ: ได้ คุณสามารถสร้างโครงสร้างลึกขึ้นโดยตั้งค่าตัวเลขระดับที่สูงกว่า (เช่น `setLevel((byte) 3)` สำหรับหน้าย่อยระดับที่สาม)

**ถาม: Aspose.Note for Java รองรับ IDE ของ Java ต่าง ๆ หรือไม่?**  
ตอบ: แน่นอน มันทำงานได้กับ IntelliJ IDEA, Eclipse, NetBeans และ IDE ใด ๆ ที่สนับสนุนการพัฒนา Java

**ถาม: ฉันสามารถปรับแต่งรูปแบบข้อความในเอกสาร OneNote ของฉันได้หรือไม่?**  
ตอบ: ได้ ใช้ `ParagraphStyle` เพื่อตั้งค่าชื่อฟอนต์, ขนาด, สี, และคุณลักษณะอื่น ๆ สำหรับแต่ละองค์ประกอบ `RichText`

**ถาม: Aspose.Note for Java รองรับการบันทึกเอกสารในรูปแบบอื่น ๆ นอกจาก BMP หรือไม่?**  
ตอบ: ได้ รูปแบบที่รองรับรวมถึง PDF, PNG, JPEG, DOCX และอื่น ๆ ปรับค่า enum `SaveFormat` ตามต้องการ

**ถาม: มีรุ่นทดลองของ Aspose.Note for Java หรือไม่?**  
ตอบ: มี คุณสามารถดาวน์โหลดรุ่นทดลองฟรีจากเว็บไซต์ Aspose

## สรุป

การจัดระเบียบสมุดบันทึก OneNote ของคุณด้วยโครงสร้างลำดับชั้นที่ชัดเจนและการส่งออกเป็น PDF ทำให้บันทึกของคุณเข้าถึงและแชร์ได้ง่ายขึ้น ด้วยการทำตามขั้นตอนข้างต้น คุณจึงรู้ **วิธีบันทึก OneNote PDF** และ **เพิ่มหน้าย่อยแบบ onenote** อย่างเป็นโปรแกรมโดยใช้ Aspose.Note for Java

---

**อัปเดตล่าสุด:** 2026-01-07  
**ทดสอบด้วย:** Aspose.Note for Java 24.11 (latest)  
**ผู้เขียน:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}