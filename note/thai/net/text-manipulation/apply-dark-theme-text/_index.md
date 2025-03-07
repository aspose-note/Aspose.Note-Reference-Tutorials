---
title: การแปลงธีมสีเข้มด้วย Aspose.Note สำหรับ .NET
linktitle: ใช้ธีมสีเข้มกับข้อความใน Aspose.Note
second_title: Aspose.Note .NET API
description: แปลงเอกสาร OneNote ของคุณด้วย Aspose.Note สำหรับ .NET! ใช้ธีมสีเข้มที่ทันสมัยได้อย่างง่ายดาย ดาวน์โหลดตอนนี้และปรับปรุงประสบการณ์การจดบันทึกของคุณ
weight: 11
url: /th/net/text-manipulation/apply-dark-theme-text/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# การแปลงธีมสีเข้มด้วย Aspose.Note สำหรับ .NET

## การแนะนำ
ยินดีต้อนรับสู่คำแนะนำทีละขั้นตอนของเราเกี่ยวกับการใช้ธีมสีเข้มกับข้อความใน Aspose.Note สำหรับ .NET Aspose.Note เป็น .NET API อันทรงพลังที่ช่วยให้นักพัฒนาสามารถทำงานกับไฟล์ Microsoft OneNote โดยทางโปรแกรม ในบทช่วยสอนนี้ เราจะสำรวจวิธีทำให้เอกสาร OneNote ของคุณมีรูปลักษณ์ที่ทันสมัยและทันสมัยโดยการใช้ธีมสีเข้มกับข้อความ
## ข้อกำหนดเบื้องต้น
ก่อนที่เราจะเจาะลึกบทช่วยสอน ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:
-  Aspose.Note for .NET: ตรวจสอบให้แน่ใจว่าคุณได้ติดตั้ง Aspose.Note for .NET แล้ว ถ้าไม่เช่นนั้นคุณสามารถดาวน์โหลดได้จาก[เอกสาร Aspose.Note](https://reference.aspose.com/note/net/).
- สภาพแวดล้อมการพัฒนา: ตั้งค่าสภาพแวดล้อมการพัฒนา .NET ที่คุณต้องการ เช่น Visual Studio
- ไดเร็กทอรีเอกสาร: เตรียมไดเร็กทอรีที่มีเอกสาร OneNote ของคุณ
## นำเข้าเนมสเปซ
ในโปรเจ็กต์ .NET ของคุณ ให้นำเข้าเนมสเปซที่จำเป็นเพื่อทำงานกับ Aspose หมายเหตุ:
```csharp
    using System;
    using System.Drawing;
    using System.IO;
```
## ขั้นตอนที่ 1: โหลดเอกสาร OneNote
โหลดเอกสาร OneNote ของคุณลงใน Aspose.Note โดยใช้รหัสต่อไปนี้:
```csharp
// เส้นทางไปยังไดเร็กทอรีเอกสาร
string dataDir = "Your Document Directory";
// โหลดเอกสารลงใน Aspose.Note
Document doc = new Document(Path.Combine(dataDir, "Aspose.one"));
```
## ขั้นตอนที่ 2: ตั้งค่าสีพื้นหลัง
ตั้งค่าสีพื้นหลังของแต่ละหน้าเป็นสีดำ:
```csharp
foreach (var page in doc)
{
    page.BackgroundColor = Color.Black;
}
```
## ขั้นตอนที่ 3: ปรับสีข้อความ
ปรับสีแบบอักษรของข้อความเป็นสีขาวเพื่อให้มองเห็นได้ดีขึ้น:
```csharp
foreach (var node in doc.GetChildNodes<RichText>())
{
    var c = node.ParagraphStyle.FontColor;
    if (c.IsEmpty || Math.Abs(c.R - Color.Black.R) + Math.Abs(c.G - Color.Black.G) + Math.Abs(c.B - Color.Black.B) <= 30)
    {
        node.ParagraphStyle.FontColor = Color.White;
    }
}
```
## ขั้นตอนที่ 4: บันทึกเอกสาร
บันทึกเอกสาร OneNote ที่แก้ไขเป็น PDF:
```csharp
doc.Save(Path.Combine(dataDir, "AsposeDarkTheme.pdf"));
```
## บทสรุป
ยินดีด้วย! คุณใช้ธีมสีเข้มกับข้อความในเอกสาร Aspose.Note สำเร็จแล้ว การปรับปรุงที่เรียบง่ายแต่มีประสิทธิภาพนี้จะทำให้ไฟล์ OneNote ของคุณมีรูปลักษณ์ที่ซับซ้อนยิ่งขึ้น
## คำถามที่พบบ่อย
### ฉันสามารถใช้ธีมสีเข้มกับส่วนเฉพาะของเอกสาร OneNote ของฉันได้หรือไม่
ใช่ คุณสามารถปรับแต่งโค้ดเพื่อกำหนดเป้าหมายหน้าหรือส่วนเฉพาะภายในเอกสารของคุณได้
### Aspose.Note รองรับรูปแบบการส่งออกอื่นๆ นอกเหนือจาก PDF หรือไม่
อย่างแน่นอน! Aspose.Note รองรับรูปแบบการส่งออกที่หลากหลาย รวมถึงรูปภาพและ Microsoft Word
### มีการจำกัดขนาดเอกสารที่ Aspose.Note สามารถรองรับได้หรือไม่
Aspose.Note สามารถจัดการเอกสารที่มีขนาดแตกต่างกันได้ และประสิทธิภาพของมันได้รับการปรับให้มีประสิทธิภาพสูงสุด
### ฉันสามารถเปลี่ยนกลับเป็นธีมดั้งเดิมหลังจากใช้ธีมสีเข้มได้หรือไม่
ใช่ คุณสามารถแก้ไขโค้ดเพื่อสลับระหว่างธีมต่างๆ ตามความต้องการของคุณได้
### ฉันจะรับการสนับสนุนสำหรับการสืบค้นที่เกี่ยวข้องกับ Aspose.Note ได้ที่ไหน
 หากต้องการความช่วยเหลือใด ๆ โปรดไปที่[ฟอรั่ม Aspose.Note](https://forum.aspose.com/c/note/28) หรือสำรวจ[เอกสารประกอบ](https://reference.aspose.com/note/net/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
