---
title: ตรวจสอบว่าเอกสาร OneNote ถูกเข้ารหัส - Java หรือไม่
linktitle: ตรวจสอบว่าเอกสาร OneNote ถูกเข้ารหัส - Java หรือไม่
second_title: Aspose.Note Java API
description: เรียนรู้วิธีตรวจสอบว่าเอกสาร OneNote ได้รับการเข้ารหัสใน Java โดยใช้ Aspose.Note หรือไม่ ปฏิบัติตามคำแนะนำทีละขั้นตอนของเราเพื่อการประมวลผลเอกสารที่มีประสิทธิภาพ
weight: 10
url: /th/java/onenote-document-loading/check-document-encrypted/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# ตรวจสอบว่าเอกสาร OneNote ถูกเข้ารหัส - Java หรือไม่

## การแนะนำ

เมื่อทำงานกับเอกสาร OneNote ใน Java จำเป็นอย่างยิ่งที่จะต้องแน่ใจว่าเอกสารนั้นไม่ได้เข้ารหัสก่อนที่จะประมวลผล การเข้ารหัสเอกสารสามารถเพิ่มระดับการรักษาความปลอดภัยเพิ่มเติมได้ แต่ก็อาจทำให้ขั้นตอนการประมวลผลยุ่งยากขึ้นได้หากไม่ได้รับการจัดการอย่างถูกต้อง ในบทช่วยสอนนี้ เราจะแนะนำคุณตลอดกระบวนการตรวจสอบว่าเอกสาร OneNote ได้รับการเข้ารหัสโดยใช้ Aspose.Note for Java หรือไม่

## ข้อกำหนดเบื้องต้น

ก่อนที่คุณจะเริ่มต้น ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:

1.  Java Development Kit (JDK): ตรวจสอบให้แน่ใจว่าคุณได้ติดตั้ง Java บนระบบของคุณ คุณสามารถดาวน์โหลดได้จาก[ที่นี่](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).

2.  Aspose.Note สำหรับไลบรารี Java: ดาวน์โหลดและตั้งค่า Aspose.Note สำหรับไลบรารี Java คุณสามารถค้นหาลิงค์ดาวน์โหลด[ที่นี่](https://releases.aspose.com/note/java/).

## แพ็คเกจนำเข้า

ในการเริ่มต้น ให้นำเข้าแพ็คเกจที่จำเป็นในโปรเจ็กต์ Java ของคุณ:

```java
import com.aspose.note.Document;
import com.aspose.note.LoadOptions;
import java.io.FileInputStream;
import java.io.IOException;
import java.nio.file.Paths;
```

แบ่งกระบวนการออกเป็นหลายขั้นตอน:

## ขั้นตอนที่ 1: ตรวจสอบว่าเอกสารจากสตรีมถูกเข้ารหัสหรือไม่

```java
public static void CheckIfDocumentFromStreamIsEncrypted() throws IOException {
    // ExStart:CheckIfDocumentFromStreamIsEncrypted
    String dataDir = "Your Document Directory";

    LoadOptions loadOptions = new LoadOptions();
    loadOptions.setDocumentPassword("password");

    FileInputStream stream = new FileInputStream(Paths.get(dataDir, "Sample1.one").toString());

    try {
        Document ref[] = { null };
        if (!Document.isEncrypted(stream, loadOptions, ref)) {
            System.out.println("The document is loaded and ready to be processed.");
        } else {
            System.out.println("The document is encrypted. Provide a password.");
        }
    } finally {
        stream.close();
    }
    // ExEnd:CheckIfDocumentFromStreamIsEncrypted
}
```

คำอธิบาย:

- วิธีนี้จะตรวจสอบว่าเอกสารที่โหลดจากสตรีมได้รับการเข้ารหัสหรือไม่
-  มันตั้งรหัสผ่านเอกสารโดยใช้`setDocumentPassword` วิธีการของ`LoadOptions` ระดับ.
-  ที่`Document.isEncrypted` วิธีการใช้เพื่อตรวจสอบว่าเอกสารถูกเข้ารหัสหรือไม่

## ขั้นตอนที่ 2: ตรวจสอบว่าเอกสารจากไฟล์ถูกเข้ารหัสหรือไม่

```java
public static void CheckIfDocumentFromFileIsEncrypted() throws IOException {
    // ExStart:CheckIfDocumentFromFileIsEncrypted
    String dataDir = "Your Document Directory";

    Document ref[] = { null };
    if (!Document.isEncrypted(Paths.get(dataDir, "Sample1.one").toString(), "VerySecretPassword", ref)) {
        if (ref[0] != null) {
            System.out.println("The document is decrypted. It is loaded and ready to be processed.");
        } else {
            System.out.println("The document is encrypted. Invalid password was provided.");
        }
    } else {
        System.out.println("The document is NOT encrypted. It is loaded and ready to be processed.");
    }
    // ExEnd:CheckIfDocumentFromFileIsEncrypted
}
```

คำอธิบาย:

- วิธีนี้จะตรวจสอบว่าเอกสารที่โหลดจากไฟล์ได้รับการเข้ารหัสหรือไม่
-  มันใช้`Document.isEncrypted` วิธีการคล้ายกับขั้นตอนก่อนหน้า แต่มีพารามิเตอร์เส้นทางไฟล์และรหัสผ่าน

## บทสรุป

ในบทช่วยสอนนี้ เราได้เรียนรู้วิธีตรวจสอบว่าเอกสาร OneNote ได้รับการเข้ารหัสใน Java โดยใช้ Aspose.Note หรือไม่ ด้วยการทำตามคำแนะนำทีละขั้นตอนและใช้ตัวอย่างโค้ดที่ให้มา คุณสามารถระบุสถานะการเข้ารหัสของเอกสารของคุณได้อย่างมีประสิทธิภาพ ช่วยให้มั่นใจได้ว่าการประมวลผลในแอปพลิเคชัน Java ของคุณจะราบรื่น

## คำถามที่พบบ่อย

### คำถามที่ 1: ฉันสามารถตรวจสอบสถานะการเข้ารหัสโดยไม่ต้องระบุรหัสผ่านได้หรือไม่

A1: ได้ คุณสามารถตรวจสอบสถานะการเข้ารหัสได้โดยไม่ต้องระบุรหัสผ่าน ที่`Document.isEncrypted` วิธีการช่วยให้คุณทำเช่นนั้นได้

### คำถามที่ 2: จะเกิดอะไรขึ้นหากฉันระบุรหัสผ่านไม่ถูกต้อง

 A2: หากคุณระบุรหัสผ่านไม่ถูกต้องเมื่อตรวจสอบสถานะการเข้ารหัส วิธีการนี้จะส่งคืน`true`แสดงว่าเอกสารถูกเข้ารหัส แต่รหัสผ่านที่ให้มาไม่ถูกต้อง

### คำถามที่ 3: เป็นไปได้ไหมที่จะถอดรหัสเอกสารที่เข้ารหัสโดยทางโปรแกรม

A3: ได้ คุณสามารถถอดรหัสเอกสารที่เข้ารหัสโดยทางโปรแกรมได้โดยระบุรหัสผ่านที่ถูกต้องระหว่างการโหลดเอกสาร

### คำถามที่ 4: ฉันสามารถใช้ Aspose.Note สำหรับรูปแบบเอกสารอื่นๆ นอกเหนือจาก OneNote ได้หรือไม่

A4: ไม่ Aspose.Note ได้รับการออกแบบมาโดยเฉพาะสำหรับการทำงานกับเอกสาร OneNote เท่านั้น

### คำถามที่ 5: ฉันจะค้นหาแหล่งข้อมูลเพิ่มเติมและการสนับสนุนสำหรับ Aspose.Note สำหรับ Java ได้ที่ไหน

 A5: คุณสามารถเยี่ยมชม[ฟอรั่ม Aspose.Note](https://forum.aspose.com/c/note/28) สำหรับการสนับสนุนชุมชนและเอกสารประกอบ
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
