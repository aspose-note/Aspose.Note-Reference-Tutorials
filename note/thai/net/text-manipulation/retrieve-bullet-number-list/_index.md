---
title: เรียกข้อมูลสัญลักษณ์แสดงหัวข้อย่อยหรือรายการตัวเลขในข้อความ Aspose.Note
linktitle: เรียกข้อมูลสัญลักษณ์แสดงหัวข้อย่อยหรือรายการตัวเลขในข้อความ Aspose.Note
second_title: Aspose.Note .NET API
description: ปลดล็อกศักยภาพของ Aspose.Note สำหรับ .NET ด้วยคำแนะนำทีละขั้นตอนในการเรียกข้อมูลรายการสัญลักษณ์แสดงหัวข้อย่อยหรือตัวเลข ยกระดับทักษะการจัดการเอกสาร OneNote ของคุณ!
weight: 23
url: /th/net/text-manipulation/retrieve-bullet-number-list/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# เรียกข้อมูลสัญลักษณ์แสดงหัวข้อย่อยหรือรายการตัวเลขในข้อความ Aspose.Note

## การแนะนำ
ยินดีต้อนรับสู่โลกของ Aspose.Note สำหรับ .NET ไลบรารีที่แข็งแกร่งและอเนกประสงค์ที่ช่วยให้นักพัฒนาสามารถจัดการการจัดการเอกสาร OneNote ได้อย่างง่ายดาย ในบทช่วยสอนนี้ เราจะเจาะลึกขั้นตอนการดึงข้อมูลรายการสัญลักษณ์แสดงหัวข้อย่อยหรือตัวเลขโดยใช้ Aspose.Note สำหรับ .NET ไม่ว่าคุณจะเป็นนักพัฒนาที่มีประสบการณ์หรือผู้ที่ชื่นชอบการเขียนโค้ด คู่มือนี้จะช่วยให้คุณมีความรู้เพื่อสำรวจความซับซ้อนของการทำงานกับรายการใน Aspose.Note
## ข้อกำหนดเบื้องต้น
ก่อนที่เราจะเริ่มการเดินทางเขียนโค้ดนี้ ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:
-  Aspose.Note สำหรับ .NET: ตรวจสอบให้แน่ใจว่าคุณได้ติดตั้งไลบรารี Aspose.Note แล้ว ถ้าไม่เช่นนั้นคุณสามารถดาวน์โหลดได้จาก[Aspose.Note สำหรับเอกสาร .NET](https://reference.aspose.com/note/net/).
- สภาพแวดล้อมการพัฒนา: มีสภาพแวดล้อมการพัฒนาที่ใช้งานได้ โดยเฉพาะ Microsoft Visual Studio ที่ติดตั้งบนเครื่องของคุณ
- ความรู้พื้นฐานของ C#: ทำความคุ้นเคยกับ C# เนื่องจากบทช่วยสอนนี้เขียนด้วยภาษานี้
## นำเข้าเนมสเปซ
ในการโต้ตอบกับ Aspose.Note สำหรับ .NET คุณจะต้องนำเข้าเนมสเปซที่จำเป็นลงในโปรเจ็กต์ของคุณ รวมเนมสเปซต่อไปนี้ไว้ที่จุดเริ่มต้นของโค้ดของคุณ:
```csharp
using System;
using System.Globalization;
using System.IO;
using Aspose.Note;
using System.Collections.Generic;
```
ตอนนี้ เรามาแจกแจงขั้นตอนการดึงรายการสัญลักษณ์แสดงหัวข้อย่อยหรือตัวเลขทีละขั้นตอน:
## ขั้นตอนที่ 1: ตั้งค่าไดเร็กทอรีเอกสารของคุณ
```csharp
// เส้นทางไปยังไดเร็กทอรีเอกสาร
string dataDir = "Your Document Directory";
```
 แทนที่`"Your Document Directory"` ด้วยเส้นทางจริงที่มีเอกสาร Aspose.Note ของคุณอยู่
## ขั้นตอนที่ 2: โหลดเอกสาร
```csharp
// โหลดเอกสารลงใน Aspose.Note
Document oneFile = new Document(dataDir + "ApplyNumberingOnText.one");
```
 ตรวจสอบให้แน่ใจว่าคุณเปลี่ยน`"ApplyNumberingOnText.one"` ด้วยชื่อของเอกสาร OneNote เฉพาะของคุณ
## ขั้นตอนที่ 3: ดึงข้อมูลคอลเลกชันของโหนด
```csharp
// ดึงข้อมูลชุดโหนดขององค์ประกอบเค้าร่าง
IList<OutlineElement> nodes = oneFile.GetChildNodes<OutlineElement>();
```
ขั้นตอนนี้จะดึงชุดของโหนดเค้าร่างจากเอกสารที่โหลด
## ขั้นตอนที่ 4: วนซ้ำแต่ละโหนด
```csharp
// วนซ้ำผ่านแต่ละโหนด
foreach (OutlineElement node in nodes)
{
    if (node.NumberList != null)
    {
        NumberList list = node.NumberList;
        // ทำตามขั้นตอนต่อไป...
    }
}
```
การวนซ้ำนี้ทำให้แน่ใจว่าเรากำลังจัดการกับโหนดที่มีรายการตัวเลขเท่านั้น
## ขั้นตอนที่ 5: ดึงข้อมูลแบบอักษร
```csharp
// ดึงชื่อแบบอักษร
Console.WriteLine("Font Name: " + list.Font);
// ดึงความยาวตัวอักษร
Console.WriteLine("Font Length: " + list.Font.Length);
// ดึงขนาดตัวอักษร
Console.WriteLine("Font Size: " + list.FontSize);
// ดึงสีตัวอักษร
Console.WriteLine("Font Color: " + list.FontColor);
// ดึงข้อมูลรูปแบบ
Console.WriteLine("Font format: " + list.Format);
// ตรวจสอบตัวหนา
Console.WriteLine("Is bold: " + list.IsBold);
// ตรวจสอบตัวเอียง
Console.WriteLine("Is italic: " + list.IsItalic);
Console.WriteLine();
```
บรรทัดโค้ดเหล่านี้จะแยกข้อมูลที่เกี่ยวข้องกับแบบอักษรต่างๆ จากรายการตัวเลข
## บทสรุป
 ยินดีด้วย! คุณได้เรียนรู้วิธีดึงรายการสัญลักษณ์แสดงหัวข้อย่อยหรือตัวเลขโดยใช้ Aspose.Note สำหรับ .NET เรียบร้อยแล้ว ในขณะที่คุณดำเนินการสำรวจต่อไป โปรดดูที่[เอกสารประกอบ](https://reference.aspose.com/note/net/) เพื่อข้อมูลเชิงลึกและฟังก์ชันการทำงานที่เจาะลึกยิ่งขึ้น
## คำถามที่พบบ่อย
### ฉันสามารถใช้ Aspose.Note สำหรับ .NET กับภาษาการเขียนโปรแกรมอื่นได้หรือไม่
Aspose.Note รองรับ .NET เป็นหลัก แต่มีไลบรารีเวอร์ชันอื่นๆ ที่ปรับแต่งสำหรับแพลตฟอร์มและภาษาที่แตกต่างกัน
### Aspose.Note เข้ากันได้กับรูปแบบ OneNote ล่าสุดหรือไม่
ใช่ Aspose.Note รองรับรูปแบบ OneNote ที่หลากหลาย เพื่อให้มั่นใจว่าสามารถใช้งานร่วมกับเวอร์ชันล่าสุดได้
### ฉันจะขอรับใบอนุญาตชั่วคราวสำหรับ Aspose.Note ได้อย่างไร
 เยี่ยม[ลิงค์นี้](https://purchase.aspose.com/temporary-license/) เพื่อรับใบอนุญาตชั่วคราวเพื่อวัตถุประสงค์ในการประเมิน
### มีตัวเลือกการสนับสนุนใดบ้างสำหรับผู้ใช้ Aspose.Note
คุณสามารถสำรวจและขอความช่วยเหลือได้ใน[ฟอรั่ม Aspose.Note](https://forum.aspose.com/c/note/28) สำหรับข้อสงสัยหรือปัญหาใด ๆ ที่คุณอาจพบ
### มี Aspose.Note สำหรับ .NET เวอร์ชันทดลองใช้ฟรีหรือไม่
 ใช่ คุณสามารถเข้าถึง Aspose.Note สำหรับ .NET เวอร์ชันทดลองใช้ฟรีได้[ที่นี่](https://releases.aspose.com/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
