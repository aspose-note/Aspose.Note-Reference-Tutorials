---
date: 2026-04-13
description: เรียนรู้วิธีเพิ่มรูปภาพลงในเอกสาร OneNote ด้วยการใช้สตรีมภาพใน .NET พร้อม
  Aspose.Note คู่มือขั้นตอนนี้ครอบคลุมการโหลดรูปภาพจากสตรีม การเพิ่มรูปภาพลงในโครงร่าง
  และการบันทึกไฟล์
keywords:
- add image to onenote
- how to insert image
- load image from stream
- append image to outline
- image stream .net
linktitle: เพิ่มรูปภาพลงใน OneNote ผ่านสตรีมภาพโดยใช้ Aspose.Note
second_title: Aspose.Note .NET API
title: เพิ่มรูปภาพไปยัง OneNote ผ่านสตรีมรูปภาพโดยใช้ Aspose.Note
url: /th/net/images/insert-image-using-image-stream/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# เพิ่มรูปภาพไปยัง OneNote ผ่าน Image Stream ด้วย Aspose.Note

## บทนำ

ในบทแนะนำนี้ คุณจะได้ค้นพบ **วิธีเพิ่มรูปภาพไปยัง OneNote** เอกสารโดยการโหลดรูปภาพจากสตรีมและเพิ่มลงในโครงร่างด้วย Aspose.Note สำหรับ .NET ไม่ว่าคุณจะกำลังสร้างเครื่องมือรายงาน แอปบันทึกโน้ต หรือทำงานอัตโนมัติด้านเอกสาร การแทรกรูปภาพโดยโปรแกรมทำให้ไฟล์ OneNote ของคุณน่าสนใจและมีประโยชน์มากยิ่งขึ้น.

## คำตอบด่วน
- **ต้องใช้ไลบรารีอะไร?** Aspose.Note สำหรับ .NET (มีรุ่นทดลองฟรี).  
- **รองรับเวอร์ชัน .NET ใดบ้าง?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6+.  
- **สามารถโหลดรูปภาพจากสตรีมได้หรือไม่?** ใช่ – ใช้ `FileStream` หรือการทำงานของ `Stream` ใด ๆ.  
- **จะควบคุมการจัดแนวรูปภาพอย่างไร?** ตั้งค่าคุณสมบัติ `Alignment` (เช่น `HorizontalAlignment.Right`).  
- **ไฟล์รูปแบบใดที่สร้างขึ้น?** ไฟล์ OneNote (`.one`) ที่สามารถเปิดได้ใน Microsoft OneNote.

## “เพิ่มรูปภาพไปยัง OneNote” คืออะไร

การเพิ่มรูปภาพไปยังไฟล์ OneNote หมายถึงการฝังองค์ประกอบภาพโดยตรงเข้าไปในโครงสร้างเนื้อหาของหน้า. ด้วย Aspose.Note คุณทำงานกับอ็อบเจ็กต์เช่น `Document`, `Page`, `Outline`, และ `OutlineElement`. โดยการแทรกอ็อบเจ็กต์ `Image` เข้าไปใน `OutlineElement` รูปภาพจะกลายเป็นส่วนหนึ่งของการจัดวางหน้า OneNote.

## ทำไมต้องใช้ Aspose.Note สำหรับการแทรกรูปภาพ

- **ไม่ต้องติดตั้ง Office** – สร้างหรือแก้ไขไฟล์ OneNote บนเซิร์ฟเวอร์.  
- **ควบคุมการจัดวางได้เต็มที่** – จัดแนว, ปรับขนาด, และกำหนดตำแหน่งรูปภาพได้ตามต้องการ.  
- **รองรับสตรีม** – ทำงานกับ `Stream` ใด ๆ เหมาะสำหรับการจัดเก็บบนคลาวด์หรือสถานการณ์ที่ใช้หน่วยความจำเท่านั้น.  
- **ข้ามแพลตฟอร์ม** – เข้ากันได้กับ .NET runtime บน Windows, Linux, และ macOS.

## ข้อกำหนดเบื้องต้น

1. **สภาพแวดล้อมการพัฒนา** – Visual Studio 2022 หรือ IDE ที่รองรับ .NET ใด ๆ.  
2. **ไลบรารี Aspose.Note** – ดาวน์โหลดจากเว็บไซต์อย่างเป็นทางการ [ที่นี่](https://releases.aspose.com/note/net/).  
3. **ไฟล์รูปภาพ** – อย่างน้อยหนึ่งรูป (JPG, PNG, BMP, GIF หรือ TIFF) ที่คุณต้องการฝัง.  
4. **ความรู้พื้นฐาน C#** – ความคุ้นเคยกับการจัดการไฟล์และโค้ดเชิงวัตถุ.

## นำเข้า Namespaces
ก่อนอื่น ให้นำเข้า namespaces ที่ให้เราเข้าถึงคลาสของ Aspose.Note และยูทิลิตี้ I/O ของ .NET มาตรฐาน.

```csharp
using System.IO;
using Aspose.Note;
using System.Collections.Generic;
using System.Drawing;
using System;
```

ตอนนี้เราจะเดินผ่านกระบวนการทีละขั้นตอน.

### ขั้นตอนที่ 1: เริ่มต้นอ็อบเจ็กต์ Document
เราเริ่มโดยการสร้างอินสแตนซ์ `Document` ใหม่ที่จะเก็บไฟล์ OneNote.

```csharp
// The path to the documents directory.
string dataDir = "Your Document Directory";
Document doc = new Document();
```

### ขั้นตอนที่ 2: สร้างอ็อบเจ็กต์ Page
ไฟล์ OneNote ประกอบด้วยหนึ่งหรือหลายหน้า ที่นี่เราจะสร้างหน้าใหม่เพื่อโฮสต์เนื้อหาของเรา.

```csharp
Aspose.Note.Page page = new Aspose.Note.Page(doc);
```

### ขั้นตอนที่ 3: เริ่มต้นอ็อบเจ็กต์ Outline และ OutlineElement
Outline เป็นคอนเทนเนอร์สำหรับเนื้อหาที่หลากหลาย (ข้อความ, รูปภาพ, ตาราง). `OutlineElement` เป็นลูกที่จริง ๆ แล้วเก็บรายการต่าง ๆ.

```csharp
Outline outline1 = new Outline(doc);
OutlineElement outlineElem1 = new OutlineElement(doc);
```

### ขั้นตอนที่ 4: โหลดรูปภาพจากสตรีม
โดยใช้ `FileStream` (หรือ `Stream` ใด ๆ) เราอ่านไฟล์รูปภาพและสร้างอ็อบเจ็กต์ `Image`. ที่นี่คือจุดที่คีย์เวิร์ด **load image from stream** ส่องแสง.

```csharp
using (FileStream fs = File.OpenRead(dataDir + "image.jpg"))
{
    Aspose.Note.Image image1 = new Aspose.Note.Image(doc, "Penguins.jpg", fs)
    {
        Alignment = HorizontalAlignment.Right
    };
    outlineElem1.AppendChildLast(image1);
}
```

### ขั้นตอนที่ 5: เพิ่มรูปภาพลงใน OutlineElement
รูปภาพตอนนี้เป็นส่วนหนึ่งของ `OutlineElement`. ขั้นตอนนี้แสดงฟังก์ชัน **append image to outline**.

```csharp
outlineElem1.AppendChildLast(image1);
```

### ขั้นตอนที่ 6: เพิ่ม OutlineElement ลงใน Outline
ตอนนี้เราจะผูกอิลิเมนต์ (พร้อมรูปภาพ) เข้ากับคอนเทนเนอร์ Outline.

```csharp
outline1.AppendChildLast(outlineElem1);
```

### ขั้นตอนที่ 7: เพิ่ม Outline ลงใน Page
Outline ที่มีรูปภาพจะถูกเพิ่มลงในหน้า.

```csharp
page.AppendChildLast(outline1);
```

### ขั้นตอนที่ 8: เพิ่ม Page ลงใน Document
เมื่อหน้าเตรียมพร้อม เราแทรกมันเข้าไปในโครงสร้างของเอกสาร.

```csharp
doc.AppendChildLast(page);
```

### ขั้นตอนที่ 9: บันทึก Document
สุดท้าย เราบันทึกไฟล์ OneNote ลงดิสก์ ไฟล์ที่ได้สามารถเปิดได้ใน Microsoft OneNote.

```csharp
doc.Save(dataDir + "BuildDocAndInsertImageUsingImageStream_out.one");
```

## ปัญหาทั่วไปและวิธีแก้

| ปัญหา | สาเหตุ | วิธีแก้ |
|-------|--------|----------|
| **รูปภาพไม่แสดง** | สตรีมถูกปิดก่อนที่รูปภาพจะถูกเพิ่ม. | คงบล็อก `using` ไว้รอบการเรียก `AppendChildLast` (ตามที่แสดง). |
| **การจัดแนวไม่ถูกต้อง** | คุณสมบัติ `Alignment` ไม่ได้ตั้งค่า หรือถูกเขียนทับภายหลัง. | ตั้งค่า `Alignment` เมื่อสร้าง `Image` หรือแก้ไข `image1.Alignment` ก่อนทำการเพิ่ม. |
| **รูปแบบรูปภาพที่ไม่รองรับ** | พยายามโหลดรูปแบบที่ Aspose.Note ไม่รู้จัก. | แปลงรูปภาพเป็น JPG, PNG, BMP, GIF หรือ TIFF ก่อน. |
| **ข้อผิดพลาดของเส้นทางไฟล์** | `dataDir` ชี้ไปยังโฟลเดอร์ที่ไม่มีอยู่. | ใช้ `Path.Combine` และตรวจสอบว่าโฟลเดอร์มีอยู่ก่อนรัน. |

## คำถามที่พบบ่อย

**ถาม: ฉันสามารถแทรกรูปภาพหลายรูปลงในเอกสารเดียวโดยใช้วิธีนี้ได้หรือไม่?**  
**ตอบ:** ใช่. เพียงทำซ้ำขั้นตอน *Load Image from Stream* และ *Append Image to OutlineElement* สำหรับแต่ละรูปภาพ.

**ถาม: Aspose.Note รองรับรูปแบบรูปภาพอื่น ๆ นอกจาก JPG หรือไม่?**  
**ตอบ:** แน่นอน. PNG, BMP, GIF, และ TIFF ทั้งหมดรองรับ.

**ถาม: ฉันสามารถปรับแต่งการจัดแนวและขนาดของรูปภาพที่แทรกได้หรือไม่?**  
**ตอบ:** ใช่. นอกจาก `Alignment` คุณสามารถตั้งค่าคุณสมบัติ `Width`, `Height`, และ `Scale` บนวัตถุ `Image`.

**ถาม: Aspose.Note เข้ากันได้กับทุกเวอร์ชันของ .NET หรือไม่?**  
**ตอบ:** ทำงานกับ .NET Framework 4.5+, .NET Core 3.1+, .NET 5, และ .NET 6+.

**ถาม: ฉันสามารถหาแหล่งข้อมูลและการสนับสนุนเพิ่มเติมสำหรับ Aspose.Note ได้ที่ไหน?**  
**ตอบ:** คุณสามารถค้นหาเอกสารที่ครอบคลุม, ฟอรั่ม, และการสนับสนุนได้ที่ [ฟอรั่ม Aspose](https://forum.aspose.com/c/note/28).

---

**อัปเดตล่าสุด:** 2026-04-13  
**ทดสอบกับ:** Aspose.Note 24.11 สำหรับ .NET  
**ผู้เขียน:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}