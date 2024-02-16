---
title: เปิดและปิดโปรเจ็กต์ด้วยแท็กใน Aspose.Note
linktitle: เปิดและปิดโปรเจ็กต์ด้วยแท็กใน Aspose.Note
second_title: Aspose.Note .NET API
description: เรียนรู้วิธีจัดการไฟล์ Microsoft OneNote โดยทางโปรแกรมโดยใช้ Aspose.Note สำหรับ .NET เปิดและปิดโครงการด้วยแท็กได้อย่างมีประสิทธิภาพ
type: docs
weight: 15
url: /th/net/tag-management/open-close-projects-tags/
---
## การแนะนำ

ในบทช่วยสอนนี้ เราจะเรียนรู้วิธีใช้ Aspose.Note สำหรับ .NET เพื่อเปิดและปิดโปรเจ็กต์ด้วยแท็ก Aspose.Note เป็น API อันทรงประสิทธิภาพที่ช่วยให้นักพัฒนาสามารถทำงานกับไฟล์ Microsoft OneNote โดยทางโปรแกรม ช่วยให้ทำงานต่างๆ ได้ เช่น จัดการข้อความ รูปภาพ และแท็กภายในเอกสาร

## ข้อกำหนดเบื้องต้น

ก่อนที่เราจะเริ่มต้น ตรวจสอบให้แน่ใจว่าคุณได้ตั้งค่าข้อกำหนดเบื้องต้นต่อไปนี้:

## นำเข้าเนมสเปซ

```csharp
using System.IO;
using System.Linq;
```

ตอนนี้เรามาแบ่งแต่ละตัวอย่างออกเป็นหลายขั้นตอน:

## ขั้นตอนที่ 1: โหลดเอกสาร

ขั้นแรก เราต้องโหลดเอกสารลงใน Aspose.Note

```csharp
string dataDir = "Your Document Directory";
var oneFile = new Document(Path.Combine(dataDir, "ProjectNotes.one"));
```

## ขั้นตอนที่ 2: ปิดรายการโครงการ C

ตอนนี้เรามาปิดรายการช่องทำเครื่องหมายทั้งหมดที่เกี่ยวข้องกับ 'Project C'

```csharp
foreach (var node in oneFile.GetChildNodes<ITaggable>())
{
    foreach (var checkBox in node.Tags.OfType<CheckBox>())
    {
        if (checkBox.Label.Contains("Project C") && !checkBox.Checked)
        {
            checkBox.SetCompleted();
        }
    }
}
```

## ขั้นตอนที่ 3: บันทึกบันทึกโครงการ C ที่ปิด

บันทึกเอกสารที่แก้ไขด้วยรายการ 'Project C' ที่ปิด

```csharp
oneFile.Save("Path to save the closed Project C notes");
```

## ขั้นตอนที่ 4: เปิดรายการโครงการ C

ต่อไป เรามาเปิดรายการช่องทำเครื่องหมายทั้งหมดที่เกี่ยวข้องกับ 'Project C'

```csharp
var oneFile = new Document("Path to the closed Project C notes");

foreach (var node in oneFile.GetChildNodes<ITaggable>())
{
    foreach (var checkBox in node.Tags.OfType<CheckBox>())
    {
        if (checkBox.Label.Contains("Project C") && checkBox.Checked)
        {
            checkBox.SetOpen();
        }
    }
}
```

## ขั้นตอนที่ 5: บันทึก Open Project C Notes

บันทึกเอกสารที่แก้ไขด้วยรายการ 'Project C' ที่เปิดอยู่

```csharp
oneFile.Save(Path.Combine(dataDir, "ProjectNoteWithOpenProjectC.one"));
```

ตอนนี้ คุณได้เรียนรู้วิธีเปิดและปิดโปรเจ็กต์ด้วยแท็กใน Aspose.Note โดยใช้ .NET แล้ว

## บทสรุป

Aspose.Note สำหรับ .NET มอบวิธีที่สะดวกในการจัดการเอกสาร OneNote โดยทางโปรแกรม เมื่อทำตามบทช่วยสอนนี้ คุณสามารถจัดการโปรเจ็กต์ของคุณได้อย่างมีประสิทธิภาพด้วยการเปิดและปิดรายการโดยใช้แท็ก

## คำถามที่พบบ่อย

### คำถามที่ 1: Aspose.Note เข้ากันได้กับ OneNote ทุกเวอร์ชันหรือไม่

A1: Aspose.Note รองรับ Microsoft OneNote 2010 และเวอร์ชันที่ใหม่กว่า

### คำถามที่ 2: ฉันสามารถใช้ Aspose.Note สำหรับโครงการเชิงพาณิชย์ได้หรือไม่

 ตอบ 2: ได้ คุณสามารถใช้ Aspose.Note สำหรับทั้งโครงการส่วนตัวและเชิงพาณิชย์ เยี่ยม[ที่นี่](https://purchase.aspose.com/buy) เพื่อซื้อใบอนุญาต

### คำถามที่ 3: Aspose.Note ให้ทดลองใช้ฟรีหรือไม่

 A3: ใช่ คุณสามารถทดลองใช้ฟรีได้[ที่นี่](https://releases.aspose.com/).

### คำถามที่ 4: ฉันจะหาเอกสารสำหรับ Aspose.Note ได้ที่ไหน

 A4: คุณสามารถค้นหาเอกสารประกอบได้[ที่นี่](https://reference.aspose.com/note/net/).

### คำถามที่ 5: ฉันจะรับการสนับสนุนสำหรับ Aspose.Note ได้ที่ไหน

 A5: สำหรับการสนับสนุน คุณสามารถไปที่ Aspose.Note[ฟอรั่ม](https://forum.aspose.com/c/note/28).