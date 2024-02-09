---
title: โหลดเอกสาร OneNote ใน Aspose.Note
linktitle: โหลดเอกสาร OneNote ใน Aspose.Note
second_title: Aspose.Note .NET API
description: เรียนรู้วิธีโหลด เข้ารหัส และถอดรหัสเอกสาร OneNote โดยทางโปรแกรมใน .NET โดยใช้ Aspose.Note
type: docs
weight: 16
url: /th/net/loading-and-saving-operations/load-onenote-document/
---
## การแนะนำ

Aspose.Note สำหรับ .NET เป็น API อันทรงพลังที่ช่วยให้นักพัฒนาสามารถทำงานกับไฟล์ Microsoft OneNote โดยทางโปรแกรมในแอปพลิเคชัน .NET ของตน ไม่ว่าคุณจะต้องโหลด จัดการ หรือแปลงเอกสาร OneNote Aspose.Note สำหรับ .NET ก็มีฟังก์ชันการทำงานที่ครอบคลุมเพื่อปรับปรุงเวิร์กโฟลว์ของคุณ

## ข้อกำหนดเบื้องต้น

ก่อนที่จะเข้าสู่บทช่วยสอน ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:

1. Visual Studio: ติดตั้ง Visual Studio ซึ่งเป็นสภาพแวดล้อมการพัฒนาแบบรวม (IDE) ที่ครอบคลุมสำหรับการพัฒนา .NET
2.  Aspose.Note สำหรับ .NET: ดาวน์โหลดและติดตั้ง Aspose.Note สำหรับ .NET จาก[หน้าดาวน์โหลด](https://releases.aspose.com/note/net/).
3. ความรู้พื้นฐาน C#: ความคุ้นเคยกับพื้นฐานภาษาการเขียนโปรแกรม C# เป็นสิ่งจำเป็นในการทำความเข้าใจและนำตัวอย่างที่ให้ไว้ในบทช่วยสอนนี้ไปใช้

## นำเข้าเนมสเปซ

ก่อนที่คุณจะเริ่มทำงานกับ Aspose.Note สำหรับ .NET ตรวจสอบให้แน่ใจว่าได้นำเข้าเนมสเปซที่จำเป็นลงในโปรเจ็กต์ C# ของคุณ:

```csharp
using System;
using System.IO;
```

เราจะแบ่งแต่ละตัวอย่างออกเป็นหลายขั้นตอน:

## โหลดเอกสาร OneNote ใน Aspose.Note

### ขั้นตอนที่ 1: โหลดสมุดบันทึกอย่างง่าย:
   -  เริ่มต้นด้วยการสร้างอินสแตนซ์ใหม่ของ`Notebook` คลาสผ่านเส้นทางไปยังเอกสาร OneNote
   - วนซ้ำโหนดย่อยของโน้ตบุ๊กโดยใช้ลูป foreach
   - แสดงชื่อที่แสดงของแต่ละโหนดย่อย
   - ดำเนินการเฉพาะโดยพิจารณาว่าโหนดลูกเป็นเอกสารหรือสมุดบันทึกอื่น

```csharp
public static void SimpleLoadNotebook()
{
    // เส้นทางไปยังไดเร็กทอรีเอกสาร
    string dataDir = "Your Document Directory";
    string fileName = "Open Notebook.onetoc2";
    try
    {
        var notebook = new Notebook(Path.Combine(dataDir, fileName));
        foreach (var notebookChildNode in notebook)
        {
            Console.WriteLine(notebookChildNode.DisplayName);
            if (notebookChildNode is Document)
            {
                // ทำบางสิ่งกับเอกสารลูก
            }
            else if (notebookChildNode is Notebook)
            {
                // ทำอะไรสักอย่างกับสมุดบันทึกสำหรับเด็ก
            }
        }
    }
    catch (Exception ex)
    {
        Console.WriteLine(ex.Message);
    }
}
```

### ขั้นตอนที่ 2: ตรวจสอบว่าเอกสารถูกเข้ารหัสและโหลดหรือไม่:
   - ตรวจสอบว่าเอกสาร OneNote ได้รับการเข้ารหัสหรือไม่โดยการเรียก`Document.IsEncrypted` วิธีการส่งชื่อไฟล์
   - หากไม่ได้เข้ารหัส ให้ดำเนินการประมวลผลเอกสารต่อไป
   - หากมีการเข้ารหัส ให้แจ้งให้ผู้ใช้ระบุรหัสผ่านสำหรับการถอดรหัส

```csharp
public static void Document_CheckIfEncryptedAndLoad()
{
    // เส้นทางไปยังไดเร็กทอรีเอกสาร
    string dataDir = "Your Document Directory";
    string fileName = Path.Combine(dataDir, "Aspose.one");

    Document document;
    if (!Document.IsEncrypted(fileName, out document))
    {
        Console.WriteLine("The document is loaded and ready to be processed.");
    }
    else
    {
        Console.WriteLine("The document is encrypted. Provide a password.");
    }
}
```

### ขั้นตอนที่ 3: ตรวจสอบว่าเอกสารถูกเข้ารหัสด้วยรหัสผ่านและโหลดหรือไม่:
   - เช่นเดียวกับขั้นตอนก่อนหน้า ให้ตรวจสอบว่าเอกสารได้รับการเข้ารหัสด้วยรหัสผ่านเฉพาะหรือไม่
   - หากมีการเข้ารหัสและมีรหัสผ่านที่ถูกต้อง ให้ดำเนินการประมวลผลเอกสารต่อไป
   - หากมีการเข้ารหัสแต่ให้รหัสผ่านไม่ถูกต้อง ให้แจ้งให้ผู้ใช้ทราบเกี่ยวกับรหัสผ่านที่ไม่ถูกต้อง

```csharp
public static void Document_CheckIfEncryptedByPasswordAndLoad()
{
    // เส้นทางไปยังไดเร็กทอรีเอกสาร
    string dataDir = "Your Document Directory";
    string fileName = Path.Combine(dataDir, "Aspose.one");

    Document document;
    if (Document.IsEncrypted(fileName, "VerySecretPassword", out document))
    {
        if (document != null)
        {
            Console.WriteLine("The document is decrypted. It is loaded and ready to be processed.");
        }
        else
        {
            Console.WriteLine("The document is encrypted. Invalid password was provided.");
        }
    }
    else
    {
        Console.WriteLine("The document is NOT encrypted. It is loaded and ready to be processed.");
    }
}
```

### ขั้นตอนที่ 4: จัดการรูปแบบ OneNote 2007 ที่ไม่รองรับ:
   - พยายามโหลดเอกสาร OneNote ในรูปแบบ 2007
   -  หากรูปแบบไม่รองรับ ให้จับไฟล์`UnsupportedFileFormatException` และจัดการอย่างเหมาะสมโดยแจ้งให้ผู้ใช้ทราบเกี่ยวกับรูปแบบที่ไม่รองรับ

```csharp
public static void Document_OneNote2007_Is_NotSupported()
{
    // เส้นทางไปยังไดเร็กทอรีเอกสาร
    string dataDir = "Your Document Directory";
    string fileName = Path.Combine(dataDir, "OneNote2007.one");

    try
    {
        new Document(fileName);
    }
    catch (UnsupportedFileFormatException e)
    {
        if (e.FileFormat == FileFormat.OneNote2007)
        {
            Console.WriteLine("It looks like the provided file is in OneNote 2007 format that is not supported.");
        }
        else
            throw;
    }
}
```

## บทสรุป

ในบทช่วยสอนนี้ เราได้สำรวจวิธีการโหลดเอกสาร OneNote ใน Aspose.Note สำหรับ .NET โดยใช้วิธีต่างๆ ด้วยการทำตามคำแนะนำทีละขั้นตอนเหล่านี้ คุณสามารถรวมความสามารถในการประมวลผลเอกสาร OneNote เข้ากับแอปพลิเคชัน .NET ของคุณได้อย่างราบรื่น

## คำถามที่พบบ่อย

### คำถามที่ 1: Aspose.Note สำหรับ .NET เข้ากันได้กับ Microsoft OneNote ทุกเวอร์ชันหรือไม่

A1: Aspose.Note สำหรับ .NET รองรับ OneNote เวอร์ชันต่างๆ อย่างไรก็ตาม อาจมีข้อจำกัดสำหรับรูปแบบที่เก่ากว่า เช่น OneNote 2007

### คำถามที่ 2: ฉันสามารถเข้ารหัสและถอดรหัสเอกสาร OneNote โดยทางโปรแกรมด้วย Aspose.Note for .NET ได้หรือไม่

ตอบ 2: ได้ คุณสามารถตรวจสอบว่าเอกสารถูกเข้ารหัสหรือไม่ และถอดรหัสโดยใช้ Aspose.Note สำหรับ .NET

### คำถามที่ 3: ฉันจะค้นหาแหล่งข้อมูลเพิ่มเติมและการสนับสนุนสำหรับ Aspose.Note สำหรับ .NET ได้ที่ไหน

 A3: คุณสามารถเยี่ยมชม[Aspose.Note สำหรับเอกสาร .NET](https://reference.aspose.com/note/net/) สำหรับคำแนะนำและตัวอย่างที่ครอบคลุม นอกจากนี้คุณยังสามารถขอความช่วยเหลือจาก[Aspose.Note สำหรับฟอรัม .NET](https://forum.aspose.com/c/note/28).

### คำถามที่ 4: Aspose.Note สำหรับ .NET มีรุ่นทดลองใช้ฟรีหรือไม่

 A4: ได้ คุณสามารถดาวน์โหลดรุ่นทดลองใช้ฟรีได้จาก[เว็บไซต์กำหนด](https://releases.aspose.com/).

### คำถามที่ 5: ฉันจะขอรับใบอนุญาตชั่วคราวสำหรับ Aspose.Note สำหรับ .NET ได้อย่างไร

 A5: คุณสามารถขอใบอนุญาตชั่วคราวได้จาก[กำหนดหน้าการซื้อ](https://purchase.aspose.com/temporary-license/).