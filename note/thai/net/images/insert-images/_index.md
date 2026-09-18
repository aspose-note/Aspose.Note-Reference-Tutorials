---
date: 2026-05-05
description: เรียนรู้วิธีแทรกรูปภาพลงในเอกสาร Aspose.Note ด้วย .NET คู่มือแบบขั้นตอนนี้จะแสดงวิธีจัดตำแหน่งรูปภาพ,
  เพิ่มรูปภาพลงในหน้า, และเสริมเนื้อหาภาพ
keywords:
- how to insert image
- how to align image
- append image to page
linktitle: แทรกรูปภาพในเอกสาร Aspose.Note
second_title: Aspose.Note .NET API
title: วิธีแทรกรูปภาพลงในเอกสาร Aspose.Note ด้วย .NET
url: /th/net/images/insert-images/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# วิธีแทรกรูปภาพลงในเอกสาร Aspose.Note ด้วย .NET

## บทนำ

หากคุณกำลังมองหาเพื่อทำให้ไฟล์ Aspose.Note ของคุณน่าสนใจยิ่งขึ้น, **how to insert image** คือทักษะแรกที่คุณต้องการเชี่ยวชาญ ในบทแนะนำนี้เราจะพาคุณผ่านขั้นตอนที่จำเป็นเพื่อเพิ่มรูปภาพ, ควบคุมขนาด, กำหนดตำแหน่งอย่างแม่นยำ, และแม้กระทั่งจัดแนวตามที่คุณต้องการ เมื่อเสร็จสิ้นคุณจะสามารถแทรกรูปภาพ, จัดแนว, และเพิ่มรูปภาพลงในหน้าได้อย่างสะดวก—ทั้งหมดด้วยโค้ด C# ที่อ่านง่ายและเป็นระเบียบ

## คำตอบสั้น
- **ต้องใช้ไลบรารีอะไร?** Aspose.Note for .NET  
- **ฉันสามารถตั้งขนาดรูปภาพโดยโปรแกรมได้หรือไม่?** Yes – use the Width and Height properties.  
- **ฉันจะกำหนดตำแหน่งรูปภาพอย่างไร?** Adjust HorizontalOffset, VerticalOffset or use alignment options.  
- **มีข้อจำกัดในรูปแบบไฟล์รูปภาพหรือไม่?** JPG, PNG, BMP, GIF and others are supported.  
- **ฉันต้องใช้ลิขสิทธิ์สำหรับการใช้งานจริงหรือไม่?** A valid Aspose.Note license is required for commercial use.

## การแทรกรูปภาพใน Aspose.Note คืออะไร?

การแทรกรูปภาพหมายถึงการสร้างวัตถุ Aspose.Note.Image, กำหนดคุณสมบัติการแสดงผล, และแนบไปยังหน้าของไฟล์ .one ที่เข้ากันได้กับ OneNote. สิ่งนี้ทำให้คุณสามารถเพิ่มเนื้อหาภาพเช่น ภาพหน้าจอ, แผนภาพ, หรือสื่อภาพอื่น ๆ ลงในโน้ตได้

## ทำไมต้องแทรกรูปภาพด้วย Aspose.Note?

- **การสื่อสารที่ดีกว่า:** Visuals clarify complex ideas faster than text alone.  
- **การจัดวางที่สอดคล้องกัน:** Programmatic control ensures every document follows the same design standards.  
- **เหมาะกับการทำอัตโนมัติ:** Ideal for generating reports, tutorials, or batch‑processed notebooks.

## ข้อกำหนดเบื้องต้น

1. Aspose.Note for .NET: Download and install Aspose.Note for .NET from [here](https://releases.aspose.com/note/net/).  
2. Image Files: Have the image files (JPG, PNG, etc.) you plan to embed ready on disk.

## นำเข้า Namespaces

เราจะเริ่มโดยการนำเข้า namespaces ที่ให้เราเข้าถึงการทำงานกับไฟล์ I/O และ API ของ Aspose.Note

```csharp
using System.IO;
using Aspose.Note;
using System.Collections.Generic;
using System.Drawing;
using System;
```

## ขั้นตอนที่ 1: โหลดเอกสารและดึงหน้าที่ต้องการ

ขั้นแรก, เปิดไฟล์ .one ที่มีอยู่และดึงหน้าที่รูปภาพจะถูกแทรก

```csharp
string dataDir = "Your Document Directory";
Document doc = new Document(dataDir + "YourDocument.one");
Aspose.Note.Page page = doc.FirstChild;
```

## วิธีจัดแนวรูปภาพ

ก่อนที่เราจะเพิ่มรูปภาพ, ให้กำหนดว่ามันควรจัดเรียงกับเนื้อหาอื่นอย่างไร Aspose.Note มีตัวเลือกการจัดแนวแนวนอน (ซ้าย, กลาง, ขวา). คุณยังสามารถปรับตำแหน่งอย่างละเอียดด้วยค่าการออฟเซ็ต

## ขั้นตอนที่ 2: โหลดรูปภาพและตั้งค่าคุณสมบัติ

สร้างวัตถุ Image, ชี้ไปที่ไฟล์ของคุณ, และกำหนดขนาด, การออฟเซ็ต, และการจัดแนว

```csharp
Aspose.Note.Image image = new Aspose.Note.Image(doc, dataDir + "image.jpg")
{
    Width = 100,                // Set image width
    Height = 100,               // Set image height
    HorizontalOffset = 100,     // Set horizontal offset
    VerticalOffset = 400,       // Set vertical offset
    Alignment = HorizontalAlignment.Right  // Set image alignment
};
```

## เพิ่มรูปภาพลงในหน้า

เมื่อรูปภาพได้รับการกำหนดค่าอย่างครบถ้วนแล้ว, ให้แนบมันเข้ากับโครงสร้างของหน้า

```csharp
page.AppendChildLast(image);
```

## ข้อผิดพลาดทั่วไปและเคล็ดลับ

- **การออฟเซ็ตไม่ถูกต้อง:** Remember that offsets are measured from the top‑left corner of the page. A large vertical offset may push the image off‑screen.  
- **รูปแบบที่ไม่รองรับ:** If you try a format that isn’t recognized, Aspose.Note will throw an exception—convert the file to JPG or PNG first.  
- **คำเตือนลิขสิทธิ์:** Running without a license adds a watermark to the generated document; always apply your license in production.

## สรุป

คุณได้เรียนรู้ **how to insert image** ลงในเอกสาร Aspose.Note, วิธี **how to align image**, และวิธี **append image to page** ด้วยบรรทัดโค้ด C# ที่ง่ายไม่กี่บรรทัด เทคนิคเหล่านี้ทำให้คุณสร้างโน้ตบุ๊กที่สมบูรณ์และเป็นมืออาชีพโดยอัตโนมัติ

## คำถามที่พบบ่อย

### Q1: ฉันสามารถแทรกรูปภาพในรูปแบบใดก็ได้ลงในเอกสาร Aspose.Note หรือไม่?

A1: ใช่, Aspose.Note รองรับรูปแบบภาพหลายประเภทรวมถึง JPG, PNG, BMP, GIF เป็นต้น.

### Q2: สามารถปรับขนาดรูปภาพที่แทรกโดยโปรแกรมได้หรือไม่?

A2: แน่นอน! คุณสามารถปรับความกว้างและความสูงของรูปภาพตามที่ต้องการในระหว่างการแทรก.

### Q3: Aspose.Note มีตัวเลือกในการแก้ไขการจัดแนวรูปภาพหรือไม่?

A3: ใช่, คุณสามารถจัดแนวรูปภาพไปทางซ้าย, ขวา หรือกลางภายในหน้าของเอกสารของคุณ.

### Q4: ฉันสามารถแทรกรูปภาพหลายรูปลงในหน้าเดียวของเอกสารได้หรือไม่?

A4: แน่นอน! คุณสามารถแทรกรูปภาพได้ตามจำนวนที่ต้องการในหน้าเดียวโดยใช้ Aspose.Note.

### Q5: มีขีดจำกัดขนาดไฟล์ของรูปภาพที่สามารถแทรกได้หรือไม่?

A5: Aspose.Note ไม่กำหนดข้อจำกัดที่เข้มงวดต่อขนาดไฟล์รูปภาพ, แต่แนะนำให้ทำการปรับขนาดรูปภาพเพื่อประสิทธิภาพที่ดียิ่งขึ้น.

## คำถามที่พบบ่อย

**Q: ฉันจะโหลดรูปภาพจากสตรีมแทนการใช้เส้นทางไฟล์ได้อย่างไร?**  
A: ใช้คอนสตรัคเตอร์ Image(Stream, Document) และส่ง MemoryStream ที่มีไบต์ของรูปภาพ

**Q: ฉันสามารถเปลี่ยนรูปภาพหลังจากที่ได้เพิ่มลงในหน้าแล้วได้หรือไม่?**  
A: ใช่, คุณสามารถแก้ไขคุณสมบัติ Width, Height, HorizontalOffset, VerticalOffset, และ Alignment ของวัตถุ Image ที่มีอยู่แล้วและจากนั้นเรียก page.Update().

**Q: สามารถเพิ่มคำบรรยายใต้รูปภาพได้หรือไม่?**  
A: แทรกองค์ประกอบ RichText หลังรูปภาพและตั้งค่าข้อความเป็นคำบรรยาย.

**Q: Aspose.Note รองรับ GIF แบบเคลื่อนไหวหรือไม่?**  
A: GIF แบบเคลื่อนไหวจะถูกจัดการเป็นภาพนิ่ง; จะทำการแสดงเฉพาะเฟรมแรกเท่านั้น.

**Q: ควรทำอย่างไรหากรูปภาพดูเบลอ?**  
A: ตรวจสอบให้แน่ใจว่ารูปภาพต้นฉบับมีความละเอียดเพียงพอและหลีกเลี่ยงการขยายขนาดเกินขนาดเดิม.

---

**อัปเดตล่าสุด:** 2026-05-05  
**ทดสอบกับ:** Aspose.Note 23.12 for .NET  
**ผู้เขียน:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}
{{< blocks/products/products-backtop-button >}}