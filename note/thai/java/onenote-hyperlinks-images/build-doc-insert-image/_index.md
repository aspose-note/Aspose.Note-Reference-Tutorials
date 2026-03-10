---
date: 2025-12-20
description: เรียนรู้วิธีเพิ่มรูปภาพลงใน OneNote ด้วย Aspose.Note สำหรับ Java คู่มือแบบขั้นตอนต่อขั้นตอนในการสร้างเอกสาร
  OneNote และแทรกรูปภาพโดยอัตโนมัติ
linktitle: How to add picture to OneNote using Java – Build Document and Insert Image
second_title: Aspose.Note Java API
title: วิธีเพิ่มรูปภาพลงใน OneNote ด้วย Java – สร้างเอกสารและแทรกรูปภาพ
url: /th/java/onenote-hyperlinks-images/build-doc-insert-image/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# วิธีเพิ่มรูปภาพไปยัง OneNote ด้วย Java – สร้างเอกสารและแทรกรูปภาพ

## บทนำ

ในบทแนะนำนี้ คุณจะได้เรียนรู้ **วิธีเพิ่มรูปภาพไปยัง OneNote** ด้วย Aspose.Note Java API เราจะอธิบายขั้นตอนการสร้างเอกสาร OneNote ตั้งแต่ต้น การแทรกรูปภาพ และการบันทึกผลลัพธ์เป็น PDF ไม่ว่าคุณจะกำลังสร้างเครื่องมือรายงาน การทำงานอัตโนมัติในการบันทึกโน้ต หรือเพียงต้องการฝังกราฟิกด้วยโปรแกรม โค้ดนี้จะให้แนวทางที่ชัดเจนและเป็นมืออาชีพ

## คำตอบสั้น ๆ
- **ต้องใช้ไลบรารีอะไร?** Aspose.Note for Java  
- **สามารถแทรกรูปแบบภาพใดได้บ้าง?** รองรับ JPEG, PNG, BMP, GIF และรูปแบบอื่น ๆ  
- **มีรูปแบบไฟล์ผลลัพธ์อะไรบ้าง?** สามารถบันทึกเป็น OneNote, PDF, XPS, HTML ฯลฯ  
- **ต้องมีลิขสิทธิ์สำหรับการใช้งานจริงหรือไม่?** ใช่ ต้องมีลิขสิทธิ์เชิงพาณิชย์สำหรับการใช้งานที่ไม่ใช่ trial  
- **โค้ดนี้ทำงานข้ามแพลตฟอร์มหรือไม่?** แน่นอน – Java ทำงานบน Windows, Linux, และ macOS  

## “add picture to OneNote” คืออะไร?
การเพิ่มรูปภาพไปยัง OneNote หมายถึงการฝังไฟล์รูปภาพลงในหน้า OneNote ผ่านโปรแกรม เพื่อให้รูปปรากฏพร้อมกับข้อความ, โครงร่าง หรือองค์ประกอบอื่น ๆ Aspose.Note API ทำหน้าที่เป็นชั้นนามธรรมของรูปแบบไฟล์ OneNote ให้คุณโฟกัสที่เนื้อหาโดยไม่ต้องจัดการกับโครงสร้าง XML ภายใน

## ทำไมต้องเพิ่มรูปภาพไปยัง OneNote ด้วย Java?
- **Automation:** สร้างบันทึกการประชุมพร้อมภาพหน้าจอโดยอัตโนมัติ  
- **Consistency:** ทำให้ทุกหน้ามีรูปแบบและแบรนด์เดียวกัน  
- **Integration:** ผสานข้อมูลจากระบบอื่น (เช่น แผนภูมิ) เข้าไปในโน้ตบุ๊ก OneNote โดยตรง  
- **Cross‑platform:** Java ทำให้คุณรันโค้ดเดียวกันบนเซิร์ฟเวอร์หรือเดสก์ท็อปใดก็ได้  

## ข้อกำหนดเบื้องต้น

ก่อนเริ่มทำตามขั้นตอน โปรดตรวจสอบว่าคุณมีสิ่งต่อไปนี้พร้อมแล้ว:

1. **Java Development Kit (JDK)** – เวอร์ชันล่าสุด (8 หรือใหม่กว่า)  
2. **Aspose.Note for Java library** – ดาวน์โหลดจาก [website](https://releases.aspose.com/note/java/)  
3. **IDE** – IntelliJ IDEA, Eclipse หรือเครื่องมือแก้ไขโค้ด Java ที่คุณถนัด  

## นำเข้าแพ็กเกจ

เริ่มต้นด้วยการนำเข้าคลาสที่จำเป็นในไฟล์ซอร์สโค้ด Java ของคุณ:

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.HorizontalAlignment;
import com.aspose.note.Image;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.SaveFormat;
```

## คู่มือแบบขั้นตอน

### ขั้นตอนที่ 1: ตั้งค่าเอกสาร

สร้างเอกสาร OneNote ใหม่และคอนเทนเนอร์หน้า (page) ที่จะบรรจุเนื้อหา

```java
String dataDir = "Your Document Directory";
Document doc = new Document();
Page page = new Page();
```

### ขั้นตอนที่ 2: เริ่มต้น Outline

*Outline* ทำหน้าที่เป็นคอนเทนเนอร์สำหรับองค์ประกอบต่าง ๆ เช่น ข้อความและรูปภาพ เราตั้งค่า offset เป็นศูนย์เพื่อให้เนื้อหาเริ่มที่มุมซ้ายบน

```java
Outline outline = new Outline();
outline.setVerticalOffset(0);
outline.setHorizontalOffset(0);
```

### ขั้นตอนที่ 3: โหลดและจัดตำแหน่งรูปภาพ

โหลดรูปภาพที่ต้องการฝังและจัดตำแหน่งให้ชิดด้านขวาของหน้า นี่คือจุดที่เราจริง ๆ **เพิ่มรูปภาพไปยัง OneNote**

```java
Image image = new Image(null, dataDir + "Input.jpg");
image.setAlignment(HorizontalAlignment.Right);
```

### ขั้นตอนที่ 4: แนบรูปภาพเข้ากับ Outline Element

ห่อรูปภาพไว้ใน `OutlineElement` ขั้นตอนนี้เชื่อมวัตถุภาพกับโครงสร้าง outline ของเอกสาร

```java
OutlineElement outlineElem = new OutlineElement();
outlineElem.appendChildLast(image);
```

### ขั้นตอนที่ 5: ประกอบโครงสร้างเอกสาร

เพิ่ม `OutlineElement` เข้าไปใน `Outline` จากนั้นแนบ `Outline` ไปยังหน้า (page) และสุดท้ายเพิ่มหน้าเข้าไปในเอกสาร

```java
outline.appendChildLast(outlineElem);
page.appendChildLast(outline);
doc.appendChildLast(page);
```

### ขั้นตอนที่ 6: บันทึกเอกสาร OneNote

บันทึกเอกสารลงดิสก์ ตัวอย่างนี้ส่งออกเป็น PDF แต่คุณก็สามารถบันทึกเป็นไฟล์ OneNote ดั้งเดิม (`.one`) ได้โดยเปลี่ยนค่า `SaveFormat`

```java
try {
    doc.save(dataDir + "NewOneNotedocument_out", SaveFormat.Pdf);
} catch (IOException e) {
    e.printStackTrace();
}
```

## ปัญหาที่พบบ่อยและวิธีแก้

| ปัญหา | สาเหตุ | วิธีแก้ |
|-------|--------|--------|
| **รูปภาพไม่แสดง** | เส้นทางไฟล์ผิดหรือรูปแบบไม่รองรับ | ตรวจสอบให้ `dataDir` ชี้ไปยังโฟลเดอร์ที่ถูกต้องและใช้รูปแบบที่รองรับ (JPEG, PNG ฯลฯ) |
| **PDF บันทึกเป็นไฟล์เปล่า** | การตั้งค่า offset ของ outline ไม่ถูกต้อง | ตรวจสอบให้เรียก `setVerticalOffset(0)` และ `setHorizontalOffset(0)` หรือปรับ offset ให้อยู่ในขอบเขตของหน้า |
| **IOException ขณะบันทึก** | โฟลเดอร์ปลายทางไม่มีหรือไม่มีสิทธิ์เขียน | สร้างโฟลเดอร์ล่วงหน้าหรือรันโปรแกรมด้วยสิทธิ์ที่เหมาะสม |

## คำถามที่พบบ่อย

**Q1: จะหาเอกสารอ้างอิงของ Aspose.Note for Java ได้จากที่ไหน?**  
A1: คุณสามารถเข้าถึงเอกสารอ้างอิงได้ [ที่นี่](https://reference.aspose.com/note/java/)  

**Q2: จะดาวน์โหลด Aspose.Note for Java ได้อย่างไร?**  
A2: ดาวน์โหลด Aspose.Note for Java จาก [หน้าดาวน์โหลด](https://releases.aspose.com/note/java/)  

**Q3: มีรุ่นทดลองใช้งานฟรีสำหรับ Aspose.Note for Java หรือไม่?**  
A3: มี คุณสามารถรับรุ่นทดลองได้จาก [website](https://releases.aspose.com/)  

**Q4: จะขอรับการสนับสนุนสำหรับ Aspose.Note for Java ได้จากที่ไหน?**  
A4: สำหรับการสนับสนุน ให้เยี่ยมชม [Aspose.Note forum](https://forum.aspose.com/c/note/28)  

**Q5: สามารถขอรับลิขสิทธิ์ชั่วคราวสำหรับ Aspose.Note for Java ได้หรือไม่?**  
A5: ได้ คุณสามารถขอรับลิขสิทธิ์ชั่วคราวได้ [ที่นี่](https://purchase.aspose.com/temporary-license/)  

---

**อัปเดตล่าสุด:** 2025-12-20  
**ทดสอบกับ:** Aspose.Note for Java 24.12 (ล่าสุด)  
**ผู้เขียน:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}