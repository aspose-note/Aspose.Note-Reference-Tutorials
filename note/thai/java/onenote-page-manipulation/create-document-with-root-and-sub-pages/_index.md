---
date: 2026-04-30
description: เรียนรู้วิธี **บันทึก OneNote เป็น PDF** และเพิ่มหน้าย่อยใน OneNote ด้วย
  Aspose.Note สำหรับ Java. ติดตามคู่มือขั้นตอนต่อขั้นตอนนี้เพื่อจัดระเบียบโน้ตของคุณอย่างมีประสิทธิภาพ.
keywords:
- save onenote as pdf
- add sub pages onenote
- Aspose.Note Java
linktitle: วิธีบันทึก OneNote เป็น PDF และเพิ่มหน้าย่อย
second_title: Aspose.Note Java API
title: วิธีบันทึก OneNote เป็น PDF และเพิ่มหน้าย่อย
url: /th/java/onenote-page-manipulation/create-document-with-root-and-sub-pages/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# วิธีบันทึก OneNote เป็น PDF และเพิ่มหน้าย่อย

## บทนำ

ในบทแนะนำนี้ คุณจะค้นพบ **how to save onenote as pdf** ขณะสร้างเอกสารที่มีทั้งหน้า root และหน้าย่อยโดยใช้ Aspose.Note for Java การจัดระเบียบสมุดบันทึก OneNote ของคุณด้วยโครงสร้างชัดเจนทำให้การนำทางเป็นเรื่องง่าย และการส่งออกเป็น PDF ช่วยให้คุณสามารถแชร์บันทึกของคุณในรูปแบบที่ทุกคนสามารถอ่านได้ เราจะสาธิตวิธี **add sub pages onenote** style เพื่อให้คุณสร้างโครงสร้างหลายระดับได้อย่างง่ายดาย.

## คำตอบสั้น
- **“save onenote as pdf” หมายถึงอะไร?** หมายถึงการส่งออกสมุดบันทึก OneNote เป็นไฟล์ PDF โดยใช้ Aspose.Note for Java.  
- **ต้องการ API ใด?** Aspose.Note for Java มีคลาสและเมธอดที่จำเป็น.  
- **ฉันสามารถสร้างหน้าที่มีโครงสร้างลำดับชั้นได้หรือไม่?** ได้ – ตั้งค่าระดับของหน้าเพื่อสร้างหน้ารากและหน้าย่อย.  
- **ต้องการไลเซนส์สำหรับการใช้งานจริงหรือไม่?** มีรุ่นทดลองใช้งานฟรี แต่ต้องมีไลเซนส์เชิงพาณิชย์สำหรับการใช้งานจริง.  
- **ฉันสามารถส่งออกเป็นรูปแบบใดได้บ้าง?** นอกจาก PDF คุณยังสามารถส่งออกเป็น BMP, PNG, JPEG, DOCX และรูปแบบอื่น ๆ.

## วิธีบันทึก OneNote เป็น PDF

การบันทึก OneNote เป็น PDF จะเปลี่ยนแต่ละหน้าของสมุดบันทึกให้เป็นเอกสารแบบคงที่ที่รักษาการจัดรูปแบบ ภาพ และโครงสร้างของหน้าไว้ นี่เป็นวิธีที่เหมาะสำหรับการแชร์ เก็บถาวร หรือพิมพ์บันทึกในขณะที่ยังคงโครงสร้างต้นฉบับไว้ครบถ้วน.

## ทำไมต้องเพิ่มหน้าย่อยใน OneNote?

การเพิ่มหน้าย่อยช่วยให้คุณจัดกลุ่มเนื้อหาที่เกี่ยวข้องภายใต้หน้าพาเรนท์ ทำให้โครงสร้างคล้ายโฟลเดอร์ เพิ่มประสิทธิภาพการจัดระเบียบบันทึก เร่งการค้นหา และทำให้ประสบการณ์การอ่านดีขึ้นเมื่อสมุดบันทึกถูกส่งออกเป็น PDF.

## ข้อกำหนดเบื้องต้น

ก่อนเริ่มทำตามขั้นตอนต่อไปนี้ให้ตรวจสอบว่าคุณมีสิ่งต่อไปนี้แล้ว:

1. **Java Development Kit (JDK)** – ตรวจสอบว่าคุณได้ติดตั้ง JDK บนระบบของคุณแล้ว.  
2. **Aspose.Note for Java** – ดาวน์โหลดและติดตั้ง Aspose.Note for Java จาก [website](https://purchase.aspose.com/buy).  
3. **Integrated Development Environment (IDE)** – เลือก IDE สำหรับ Java เช่น IntelliJ IDEA, Eclipse หรือ NetBeans.

## นำเข้าแพ็กเกจ

เริ่มต้นด้วยการนำเข้าแพ็กเกจที่จำเป็นในโปรเจกต์ Java ของคุณ:

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

เริ่มต้นอ็อบเจ็กต์หน้าและตั้งค่าระดับของพวกมัน การตั้งค่าระดับจะกำหนดว่าหน้านั้นเป็นหน้ารากหรือหน้าย่อย:

```java
Page page1 = new Page();
page1.setLevel((byte) 1);

Page page2 = new Page();
page2.setLevel((byte) 2);

Page page3 = new Page();
page3.setLevel((byte) 1);
```

## ขั้นตอนที่ 4: เพิ่มโหนดลงในหน้า

### เพิ่มโหนดลงในหน้าแรก

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

### เพิ่มโหนดลงในหน้าที่สอง

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

### เพิ่มโหนดลงในหน้าที่สาม

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

## ขั้นตอนที่ 5: เพิ่มหน้าเข้าไปใน Document

```java
doc.appendChildLast(page1);
doc.appendChildLast(page2);
doc.appendChildLast(page3);
```

## ขั้นตอนที่ 6: บันทึก Document

บันทึกเอกสาร OneNote เป็น PDF (หรือ BMP ในตัวอย่างนี้) การเปลี่ยนค่า `SaveFormat` จะทำให้คุณส่งออกเป็น PDF ซึ่งตอบสนองความต้องการ “save onenote as pdf”:

```java
try {
    doc.save(dataDir + "GenerateRootAndSubLevelPagesInOneNote_out.bmp", SaveFormat.Bmp);
} catch (IOException e) {
    // Handle exception
}
```

> **เคล็ดลับ:** เพื่อส่งออกโดยตรงเป็น PDF ให้เปลี่ยน `SaveFormat.Bmp` เป็น `SaveFormat.Pdf`.

ยินดีด้วย! คุณได้สร้างเอกสาร OneNote ที่มีหน้ารากและหน้าย่อยสำเร็จแล้วและได้เรียนรู้ **how to save onenote as pdf** ด้วย Aspose.Note for Java.

## ทำไมเรื่องนี้ถึงสำคัญ

- **Hierarchical organization:** การจัดระเบียบแบบลำดับชั้นช่วยให้คุณจำลองโครงสร้างโฟลเดอร์ภายใน OneNote.  
- **Seamless PDF export:** เมื่อจัดระเบียบแล้ว การส่งออกเป็น PDF จะรักษาโครงสร้างลำดับชั้น ทำให้เอกสารสุดท้ายอ่านง่ายและแชร์ได้สะดวก.  
- **Automation:** โค้ดนี้สามารถรวมเข้ากับแอปพลิเคชัน Java ขนาดใหญ่ได้ ช่วยให้สร้างสมุดบันทึกที่มีโครงสร้างเป็นชุดได้อย่างอัตโนมัติ.

## ข้อผิดพลาดทั่วไปและวิธีหลีกเลี่ยง

| ปัญหา | สาเหตุ | วิธีแก้ |
|-------|-------|----------|
| หน้าปรากฏอยู่ในระดับเดียวกัน | ค่า `setLevel` ไม่ถูกต้อง | ใช้ `setLevel((byte) 1)` สำหรับหน้ารากและ `setLevel((byte) 2)` (หรือสูงกว่า) สำหรับหน้าย่อย. |
| ผลลัพธ์ PDF ปรากฏเป็นสีขาว | ขาด `SaveFormat.Pdf` หรือเส้นทางไฟล์ไม่ถูกต้อง | ตรวจสอบว่าไดเรกทอรีมีอยู่และใช้ `SaveFormat.Pdf`. |
| ฟอนต์ไม่ถูกนำไปใช้ | ชื่อฟอนต์ผิดหรือฟอนต์ไม่มีในระบบ | ตรวจสอบว่าฟอนต์ (เช่น “David Transparent”) ถูกติดตั้งบนเครื่องที่รันโค้ด. |

## คำถามที่พบบ่อย

**Q: ฉันสามารถสร้างหลายระดับของหน้าย่อยโดยใช้ Aspose.Note for Java ได้หรือไม่?**  
A: ได้ คุณสามารถสร้างโครงสร้างลึกขึ้นโดยตั้งค่าตัวเลขระดับที่สูงกว่า (เช่น `setLevel((byte) 3)` สำหรับหน้าย่อยระดับที่สาม).

**Q: Aspose.Note for Java รองรับ IDE ของ Java ต่าง ๆ หรือไม่?**  
A: แน่นอน มันทำงานได้กับ IntelliJ IDEA, Eclipse, NetBeans และ IDE ใด ๆ ที่รองรับการพัฒนา Java.

**Q: ฉันสามารถปรับแต่งการจัดรูปแบบข้อความในเอกสาร OneNote ของฉันได้หรือไม่?**  
A: ได้ ใช้ `ParagraphStyle` เพื่อตั้งค่าชื่อฟอนต์, ขนาด, สีและคุณลักษณะอื่น ๆ สำหรับแต่ละองค์ประกอบ `RichText`.

**Q: Aspose.Note for Java รองรับการบันทึกเอกสารในรูปแบบอื่น ๆ นอกจาก BMP หรือไม่?**  
A: ได้ รูปแบบที่รองรับรวมถึง PDF, PNG, JPEG, DOCX และอื่น ๆ เปลี่ยนค่า enum `SaveFormat` ตามต้องการ.

**Q: มีรุ่นทดลองใช้งานสำหรับ Aspose.Note for Java หรือไม่?**  
A: มี คุณสามารถดาวน์โหลดรุ่นทดลองฟรีจากเว็บไซต์ Aspose.

## สรุป

การจัดระเบียบสมุดบันทึก OneNote ของคุณด้วยโครงสร้างลำดับชั้นที่ชัดเจนและส่งออกเป็น PDF ทำให้บันทึกของคุณเข้าถึงและแชร์ได้ง่ายขึ้น โดยทำตามขั้นตอนข้างต้น คุณตอนนี้รู้แล้วว่า **how to save onenote as pdf** และ **add sub pages onenote** style อย่างโปรแกรมเมติกด้วย Aspose.Note for Java.

---

**อัปเดตล่าสุด:** 2026-04-30  
**ทดสอบกับ:** Aspose.Note for Java 24.11 (latest)  
**ผู้เขียน:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}