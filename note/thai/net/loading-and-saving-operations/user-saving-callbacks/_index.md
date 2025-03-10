---
title: การโทรกลับแบบประหยัดผู้ใช้ใน Aspose.Note
linktitle: การโทรกลับแบบประหยัดผู้ใช้ใน Aspose.Note
second_title: Aspose.Note .NET API
description: เรียนรู้วิธีใช้การโทรกลับแบบประหยัดผู้ใช้ใน Aspose.Note สำหรับ .NET เพื่อปรับแต่งแบบอักษรสำหรับการบันทึก, CSS และรูปภาพ
weight: 31
url: /th/net/loading-and-saving-operations/user-saving-callbacks/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# การโทรกลับแบบประหยัดผู้ใช้ใน Aspose.Note

## การแนะนำ

ในบทช่วยสอนนี้ เราจะสำรวจวิธีการใช้การโทรกลับแบบประหยัดผู้ใช้ใน Aspose.Note สำหรับ .NET การเรียกกลับเหล่านี้ช่วยให้คุณปรับแต่งกระบวนการบันทึกโดยจัดให้มี hooks เพื่อแทรกแซงในขั้นตอนต่างๆ เช่น การบันทึกแบบอักษร สไตล์ชีต CSS และรูปภาพ ด้วยการใช้การเรียกกลับเหล่านี้ คุณสามารถปรับแต่งพฤติกรรมการบันทึกให้เหมาะกับความต้องการเฉพาะของคุณ เพิ่มความยืดหยุ่นและการควบคุมเอาต์พุต

## ข้อกำหนดเบื้องต้น

ก่อนที่จะเจาะลึกการใช้งานการโทรกลับแบบประหยัดผู้ใช้ใน Aspose.Note ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:

1.  Aspose.Note สำหรับ .NET SDK: ดาวน์โหลดและติดตั้ง Aspose.Note สำหรับ .NET SDK จาก[หน้าดาวน์โหลด](https://releases.aspose.com/note/net/).
   
2. สภาพแวดล้อมการพัฒนา: ตั้งค่าสภาพแวดล้อมการพัฒนาที่เหมาะสม เช่น Visual Studio หรือสภาพแวดล้อมการพัฒนา .NET อื่นๆ

## นำเข้าเนมสเปซ

ในการเริ่มต้น ตรวจสอบให้แน่ใจว่าได้นำเข้าเนมสเปซที่จำเป็นลงในโปรเจ็กต์ของคุณเพื่อเข้าถึงคลาสและวิธีการที่จำเป็นจากไลบรารี Aspose.Note:

```csharp
using Aspose.Note.Saving.Html;
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Text;
```

ตอนนี้ เราจะแบ่งการใช้งานการโทรกลับแบบประหยัดผู้ใช้ออกเป็นหลายขั้นตอน:

## ขั้นตอนที่ 1: กำหนดคุณสมบัติการโทรกลับ

```csharp
public string RootFolder { get; set; }
public bool KeepCssStreamOpened { get; set; }
public string CssFolder { get; set; }
public Stream CssStream { get; private set; }
public string FontsFolder { get; set; }
public string ImagesFolder { get; set; }
```

ที่นี่ เรากำหนดคุณสมบัติต่างๆ เพื่อระบุโฟลเดอร์รูท โฟลเดอร์ CSS โฟลเดอร์แบบอักษร โฟลเดอร์รูปภาพ และการตั้งค่าอื่นๆ ที่เกี่ยวข้อง

## ขั้นตอนที่ 2: ใช้การโทรกลับเพื่อบันทึกแบบอักษร

```csharp
public void FontSaving(FontSavingArgs args)
{
    string uri;
    Stream stream;
    this.CreateResourceInFolder(this.FontsFolder, args.FileName, out uri, out stream);
    args.Stream = stream;
    args.Uri = Path.Combine("..", uri).Replace("\\", "\\\\");
}
```

 ในขั้นตอนนี้ เราดำเนินการ`FontSaving` วิธีการโทรกลับเพื่อจัดการการบันทึกแบบอักษร โดยจะสร้างทรัพยากรในโฟลเดอร์แบบอักษรที่ระบุ และกำหนดสตรีมและ URI ตามนั้น

## ขั้นตอนที่ 3: ใช้ CSS Saving Callback

```csharp
public void CssSaving(CssSavingArgs args)
{
    string uri;
    Stream stream;
    this.CreateResourceInFolder(this.CssFolder, args.FileName, out uri, out stream);
    args.Stream = this.CssStream = stream;
    args.KeepStreamOpen = this.KeepCssStreamOpened;
    args.Uri = uri;
}
```

 ในที่นี้เรากำหนด`CssSaving` วิธีการโทรกลับเพื่อจัดการการบันทึกสไตล์ชีต CSS โดยจะสร้างทรัพยากรในโฟลเดอร์ CSS ที่ระบุและตั้งค่าสตรีม, URI และคุณสมบัติอื่นๆ ตามนั้น

## ขั้นตอนที่ 4: ใช้การโทรกลับการบันทึกรูปภาพ

```csharp
public void ImageSaving(ImageSavingArgs args)
{
    string uri;
    Stream stream;
    this.CreateResourceInFolder(this.ImagesFolder, args.FileName, out uri, out stream);
    args.Stream = stream;
    args.Uri = uri;
}
```

 สุดท้ายนี้ เราดำเนินการ`ImageSaving` วิธีการโทรกลับเพื่อจัดการการบันทึกภาพ เช่นเดียวกับขั้นตอนก่อนหน้านี้ สร้างทรัพยากรในโฟลเดอร์รูปภาพที่ระบุ และกำหนดสตรีมและ URI

## บทสรุป

ในบทช่วยสอนนี้ เราได้เรียนรู้วิธีการใช้งานการโทรกลับแบบประหยัดผู้ใช้ใน Aspose.Note สำหรับ .NET ด้วยการทำตามขั้นตอนที่ให้ไว้ คุณสามารถปรับแต่งกระบวนการบันทึกสำหรับแบบอักษร สไตล์ชีต CSS และรูปภาพได้ ทำให้มีความยืดหยุ่นและควบคุมเอาต์พุตได้มากขึ้น

## คำถามที่พบบ่อย

### คำถามที่ 1: ฉันสามารถใช้การเรียกกลับเหล่านี้เพื่อปรับแต่งด้านอื่นๆ ของกระบวนการบันทึกได้หรือไม่

ตอบ 1: ได้ คุณสามารถขยายการโทรกลับเหล่านี้หรือใช้งานเพิ่มเติมเพื่อปรับแต่งแง่มุมต่างๆ ของกระบวนการบันทึกได้ตามความต้องการของคุณ

### คำถามที่ 2: Aspose.Note สำหรับ .NET เข้ากันได้กับเฟรมเวิร์ก .NET อื่นๆ หรือไม่

ตอบ 2: ใช่ Aspose.Note สำหรับ .NET เข้ากันได้กับ .NET Frameworks ต่างๆ รวมถึง .NET Core และ .NET Standard

### คำถามที่ 3: ฉันจะจัดการกับข้อผิดพลาดหรือข้อยกเว้นระหว่างขั้นตอนการบันทึกได้อย่างไร

A3: คุณสามารถรวมกลไกการจัดการข้อผิดพลาดภายในวิธีการโทรกลับแต่ละวิธีเพื่อจัดการกับข้อผิดพลาดหรือข้อยกเว้นที่อาจเกิดขึ้นได้อย่างงดงาม

### คำถามที่ 4: มีข้อควรพิจารณาด้านประสิทธิภาพเมื่อใช้การเรียกกลับเหล่านี้หรือไม่

A4: แม้ว่าการเรียกกลับเหล่านี้จะให้ความยืดหยุ่น แต่ต้องแน่ใจว่ามีการนำไปใช้อย่างมีประสิทธิภาพเพื่อหลีกเลี่ยงค่าใช้จ่ายด้านประสิทธิภาพ โดยเฉพาะอย่างยิ่งเมื่อต้องจัดการกับเอกสารหรือทรัพยากรขนาดใหญ่

### คำถามที่ 5: ฉันสามารถเปลี่ยนพฤติกรรมการบันทึกแบบไดนามิกตามการป้อนข้อมูลของผู้ใช้หรือเงื่อนไขอื่น ๆ ได้หรือไม่

A5: ได้ คุณสามารถรวมตรรกะแบบมีเงื่อนไขภายในวิธีการโทรกลับเพื่อปรับพฤติกรรมการบันทึกแบบไดนามิกตามปัจจัยต่างๆ
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
