---
title: เปลี่ยนสไตล์ชื่อหน้าใน Aspose.Note
linktitle: เปลี่ยนสไตล์ชื่อหน้าใน Aspose.Note
second_title: Aspose.Note .NET API
description: แปลงเอกสาร .NET ของคุณด้วย Aspose.Note! เรียนรู้การเปลี่ยนรูปแบบชื่อหน้าได้อย่างง่ายดาย ยกระดับความสวยงามด้วยขั้นตอนง่ายๆ ไม่กี่ขั้นตอน
weight: 13
url: /th/net/text-manipulation/change-page-title-style/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# เปลี่ยนสไตล์ชื่อหน้าใน Aspose.Note

## การแนะนำ
คุณกำลังมองหาที่จะยกระดับความดึงดูดสายตาให้กับเอกสาร .NET ของคุณด้วยการกำหนดสไตล์ชื่อหน้าแบบไดนามิกหรือไม่? Aspose.Note สำหรับ .NET นำเสนอโซลูชันที่ราบรื่น ช่วยให้คุณเปลี่ยนสไตล์ของชื่อเพจของคุณได้อย่างง่ายดาย ในบทช่วยสอนนี้ เราจะแนะนำคุณตลอดกระบวนการทีละขั้นตอน เพื่อให้มั่นใจว่าคุณสามารถเพิ่มความสวยงามให้กับเอกสารของคุณได้โดยไม่ต้องยุ่งยากใดๆ
## ข้อกำหนดเบื้องต้น
ก่อนที่จะเข้าสู่บทช่วยสอน ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:
-  Aspose.Note for .NET: ตรวจสอบให้แน่ใจว่าคุณได้ติดตั้ง Aspose.Note for .NET เวอร์ชันล่าสุดแล้ว ถ้าไม่คุณสามารถดาวน์โหลดได้[ที่นี่](https://releases.aspose.com/note/net/).
- Document Directory: มีไดเร็กทอรีที่กำหนดเพื่อจัดเก็บเอกสารของคุณ คุณจะต้องระบุไดเร็กทอรีนี้ในโค้ด
## นำเข้าเนมสเปซ
ในโปรเจ็กต์ .NET ของคุณ ให้นำเข้าเนมสเปซที่จำเป็นเพื่อเข้าถึงฟังก์ชันการทำงานของ Aspose.Note เพิ่มบรรทัดต่อไปนี้ที่จุดเริ่มต้นของโค้ดของคุณ:
```csharp
    using System;
    using System.IO;
    using System.Linq;
```
ตอนนี้ เรามาแบ่งโค้ดตัวอย่างออกเป็นหลายขั้นตอนเพื่อความเข้าใจที่ครอบคลุม:
## ขั้นตอนที่ 1: ระบุไดเร็กทอรีเอกสาร
```csharp
string dataDir = "Your Document Directory";
```
 แทนที่`"Your Document Directory"` พร้อมเส้นทางไปยังไดเร็กทอรีที่เก็บเอกสารของคุณ
## ขั้นตอนที่ 2: โหลดเอกสาร
```csharp
Document document = new Document(dataDir + "Aspose.one");
```
โหลดเอกสารของคุณลงใน Aspose.Note โดยใช้เส้นทางที่ระบุ
## ขั้นตอนที่ 3: วนซ้ำชื่อหน้า
```csharp
foreach (var title in document.Select(e => e.Title.TitleText))
{
    // ปรับเปลี่ยนรูปแบบย่อหน้าชื่อเรื่อง
    title.ParagraphStyle.FontSize = 24;
    title.ParagraphStyle.IsBold = true;
    // แก้ไขรูปแบบการเรียกใช้ข้อความภายในชื่อเรื่อง
    foreach (var run in title.TextRuns)
    {
        run.Style.FontSize = 24;
        run.Style.IsBold = true;
    }
}
```
วนซ้ำชื่อหน้าแต่ละหน้าในเอกสาร และปรับแต่งสไตล์การเรียกใช้ย่อหน้าและข้อความ
## ขั้นตอนที่ 4: บันทึกเอกสาร
```csharp
document.Save(Path.Combine(dataDir, "ChangePageTitleStyle.pdf"));
```
บันทึกเอกสารที่แก้ไขด้วยสไตล์หัวเรื่องที่อัปเดต
## ขั้นตอนที่ 5: แสดงข้อความแสดงความสำเร็จ
```csharp
Console.WriteLine("\nTitle's styles are changed successfully.");
```
พิมพ์ข้อความยืนยันเพื่อระบุว่าสไตล์ของชื่อเรื่องได้รับการอัปเดตเรียบร้อยแล้ว
## บทสรุป
ยินดีด้วย! คุณได้เรียนรู้วิธีการเปลี่ยนรูปแบบชื่อหน้าใน Aspose.Note สำหรับ .NET เรียบร้อยแล้ว คุณสมบัติที่เรียบง่ายแต่ทรงพลังนี้สามารถเพิ่มความดึงดูดสายตาให้กับเอกสารของคุณได้อย่างมาก
## คำถามที่พบบ่อย
### Aspose.Note เข้ากันได้กับเวอร์ชันเฟรมเวิร์ก .NET ล่าสุดหรือไม่
 Aspose.Note ได้รับการออกแบบมาให้เข้ากันได้กับเวอร์ชันเฟรมเวิร์ก .NET ที่หลากหลาย รวมถึงเวอร์ชันล่าสุดด้วย อ้างถึง[เอกสารประกอบ](https://reference.aspose.com/note/net/) สำหรับข้อมูลความเข้ากันได้โดยละเอียด
### ฉันสามารถลองใช้ Aspose.Note ก่อนซื้อได้หรือไม่
 ใช่ คุณสามารถสำรวจ Aspose.Note ได้ด้วยการดาวน์โหลดเวอร์ชันทดลองใช้ฟรี[ที่นี่](https://releases.aspose.com/).
### ฉันจะรับการสนับสนุนสำหรับ Aspose.Note ได้อย่างไร
 สำหรับคำถามที่เกี่ยวข้องกับการสนับสนุน โปรดไปที่[ฟอรั่ม Aspose.Note](https://forum.aspose.com/c/note/28).
### ฉันจะซื้อใบอนุญาตสำหรับ Aspose.Note ได้ที่ไหน
 คุณสามารถซื้อใบอนุญาตสำหรับ Aspose.Note[ที่นี่](https://purchase.aspose.com/buy).
### ฉันจำเป็นต้องมีใบอนุญาตชั่วคราวเพื่อการทดสอบหรือไม่?
 ได้ หากคุณกำลังทดสอบ Aspose.Note คุณสามารถขอรับใบอนุญาตชั่วคราวได้[ที่นี่](https://purchase.aspose.com/temporary-license/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
