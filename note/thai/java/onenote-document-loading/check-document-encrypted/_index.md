---
date: 2026-07-05
description: เรียนรู้วิธีตรวจสอบการเข้ารหัส OneNote ด้วย Aspose.Note for Java. ตรวจจับไฟล์
  OneNote ที่เข้ารหัสก่อนโหลดเพื่อหลีกเลี่ยงข้อผิดพลาดและปรับปรุงประสบการณ์ผู้ใช้.
keywords:
- check onenote encryption
- Aspose.Note encryption detection
- Java OneNote password check
linktitle: ตรวจสอบว่าเอกสาร OneNote ถูกเข้ารหัสหรือไม่ - Java
second_title: Aspose.Note Java API
title: ตรวจสอบการเข้ารหัส OneNote – ยืนยันการเข้ารหัสเอกสาร OneNote ด้วย Java
url: /th/java/onenote-document-loading/check-document-encrypted/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}  
{{< blocks/products/pf/main-container >}}  
{{< blocks/products/pf/tutorial-page-section >}}  

# ตรวจสอบว่าเอกสาร OneNote ถูกเข้ารหัสหรือไม่ – Java  

## บทนำ  

เมื่อคุณทำงานกับไฟล์ OneNote ในแอปพลิเคชัน Java สิ่งแรกที่คุณต้องรู้คือ **ว่าเอกสารถูกเข้ารหัสหรือไม่** การพยายามโหลดไฟล์ที่เข้ารหัสโดยไม่มีรหัสผ่านที่ถูกต้องจะทำให้เกิดข้อยกเว้นและขัดจังหวะการทำงานของคุณ ในบทเรียนนี้เราจะอธิบาย **วิธีตรวจสอบการเข้ารหัสของ OneNote** ด้วย Aspose.Note สำหรับ Java เพื่อให้คุณสามารถตัดสินใจได้อย่างปลอดภัยว่าจะให้ผู้ใช้ป้อนรหัสผ่านหรือดำเนินการประมวลผลไฟล์ต่อไป  

## คำตอบสั้น  

- **วิธีใดกำหนดการเข้ารหัส?** `Document.isEncrypted`  
- **ฉันต้องใช้รหัสผ่านเพื่อทำการตรวจสอบหรือไม่?** ไม่ คุณสามารถสอบถามสถานะได้โดยไม่ต้องใช้รหัสผ่าน.  
- **เวอร์ชัน API ใดทำงานได้?** เวอร์ชันล่าสุดของ Aspise.Note สำหรับ Java (ทดสอบกับ 26.4).  
- **ฉันสามารถตรวจสอบทั้งสตรีมและเส้นทางไฟล์ได้หรือไม่?** ใช่ – API รองรับทั้งสอง.  
- **เกิดอะไรขึ้นหากรหัสผ่านผิด?** เมธอดจะคืนค่า `true` ซึ่งบ่งบอกว่าไฟล์ยังคงถูกเข้ารหัส.  

## การตรวจสอบการเข้ารหัส OneNote คืออะไร?  

การตรวจสอบการเข้ารหัส OneNote หมายถึงการกำหนดโดยโปรแกรมว่าฟไฟล์ OneNote (`.one`) ถูกป้องกันด้วยรหัสผ่านหรือไม่ ก่อนที่จะพยายามอ่านเนื้อหา การตรวจสอบสถานะอย่างรวดเร็วนี้ช่วยป้องกันข้อยกเว้นขณะรันไทม์ ทำให้คุณสามารถขอให้ผู้ใช้ป้อนรหัสผ่านเมื่อจำเป็นเท่านั้น และช่วยให้คุณปฏิบัติตามนโยบายความปลอดภัยได้  

## ทำไมต้องตรวจสอบการเข้ารหัส OneNote ก่อนโหลด?  

การโหลดไฟล์ OneNote ที่เข้ารหัสโดยไม่ได้ให้รหัสผ่านที่ถูกต้องจะทำให้เกิดข้อยกเว้นซึ่งอาจทำให้บริการของคุณล่มหรือแสดงข้อผิดพลาดที่ทำให้ผู้ใช้สับสน โดยการตรวจสอบแฟล็กการเข้ารหัสก่อน คุณสามารถแสดงหน้าต่างขอรหัสผ่านเมื่อจำเป็นเท่านั้น ลดการทำ I/O ที่ไม่จำเป็น และรับรองว่าข้อมูลที่ได้รับการป้องกันจะถูกจัดการตามกฎระเบียบขององค์กร  

## ข้อกำหนดเบื้องต้น  

1. **Java Development Kit (JDK)** – จำเป็นต้องใช้ Java 11 หรือใหม่กว่า ดาวน์โหลดได้จาก [here](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).  
2. **Aspose.Note for Java** – รับไลบรารีจากหน้าดาวน์โหลดอย่างเป็นทางการ [here](https://releases.aspose.com/note/java/).  

## นำเข้าแพ็กเกจ  

คลาส `Document` แทนไฟล์ OneNote และให้เมธอดสำหรับการโหลดและตรวจสอบเนื้อหา  

```java
import com.aspose.note.Document;
import com.aspose.note.LoadOptions;
import java.io.FileInputStream;
import java.io.IOException;
import java.nio.file.Paths;
```  

```java
import com.aspose.note.Document;
import com.aspose.note.LoadOptions;
import java.io.FileInputStream;
import java.io.IOException;
import java.nio.file.Paths;
```  

## ฉันจะตรวจสอบสถานะการเข้ารหัสสำหรับเอกสารที่โหลดจากสตรีมได้อย่างไร?  

`Document.isEncrypted` เป็นเมธอดแบบ static ที่คืนค่า boolean บ่งบอกว่าไฟล์ OneNote ถูกเข้ารหัสหรือไม่ โหลดสตรีม OneNote แบบ PDF‑style ของคุณและเรียกเมธอด static `Document.isEncrypted` เมธอดจะคืนค่า boolean ที่บ่งบอกการเข้ารหัส และเมื่อไฟล์ไม่ถูกเข้ารหัส จะเติมอาร์เรย์อ้างอิงด้วยอินสแตนซ์ `Document` ที่โหลดแล้ว sehingga คุณไม่ต้องเรียกโหลดอีกครั้ง  

**คำตอบโดยตรง (40‑70 คำ):**  
เรียก `Document.isEncrypted(inputStream, loadOptions, ref)` – จะบอกทันทีว่าสตรีมถูกป้องกันด้วยรหัสผ่านหรือไม่ หากผลลัพธ์เป็น `false` `ref[0]` จะมีอ็อบเจกต์ `Document` พร้อมใช้งาน ทำให้คุณสามารถดำเนินการต่อได้โดยไม่ต้องทำ I/O เพิ่มเติม หากผลลัพธ์เป็น `true` สตรีมถูกเข้ารหัสและคุณต้องขอรหัสผ่านก่อนดำเนินการต่อ  

**คำอธิบาย**  

- `LoadOptions` ให้คุณระบุรหัสผ่านได้ตามต้องการ (`setDocumentPassword`).  
- `Document.isEncrypted(stream, loadOptions, ref)` ตรวจสอบสถานะการเข้ารหัสของสตรีม.  
- อาร์เรย์ `ref` จะได้รับอ้างอิงไปยัง `Document` ที่โหลดเมื่อไฟล์ **ไม่** ถูกเข้ารหัส ทำให้คุณสามารถดำเนินการต่อโดยไม่ต้องโหลดอีกครั้ง.  

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

## ฉันจะตรวจสอบสถานะการเข้ารหัสสำหรับเอกสารที่โหลดจากเส้นทางไฟล์ได้อย่างไร?  

`Document.isEncrypted` ยังมี overload ที่ทำงานโดยตรงกับเส้นทางไฟล์และสตริงรหัสผ่าน overload นี้ทำตามรูปแบบการคืนค่า boolean เดียวกัน โดยจะเติมอาร์เรย์อ้างอิงเฉพาะเมื่อไฟล์ไม่ถูกเข้ารหัส.  

**คำตอบโดยตรง (40‑70 คำ):**  
เรียก `Document.isEncrypted(filePath, password, ref)` – การเรียกนี้จะคืนค่า `true` หากไฟล์ถูกเข้ารหัส (หรือรหัสผ่านผิด) และคืนค่า `false` ในกรณีอื่น เมื่อเป็น `false` `ref[0]` จะมี `Document` ที่โหลดเต็มรูปแบบพร้อมใช้งาน วิธีนี้หลีกเลี่ยงขั้นตอนการโหลดแยกและทำให้โค้ดของคุณกระชับ  

**คำอธิบาย**  

- overload นี้ทำงานโดยตรงกับเส้นทางไฟล์และสตริงรหัสผ่าน.  
- หากไฟล์ **ไม่** ถูกเข้ารหัส `isEncrypted` จะคืนค่า `false` และอ้างอิง `ref[0]` จะมีเอกสารที่โหลดแล้ว.  
- หากรหัสผ่านผิด เมธอดยังคงคืนค่า `true` ซึ่งบ่งบอกว่าไฟล์ยังคงถูกเข้ารหัส.  

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

## ข้อผิดพลาดทั่วไปและเคล็ดลับ  

- **ห้ามเขียนรหัสผ่านแบบ hard‑code** ในโค้ดการผลิต; ดึงรหัสผ่านอย่างปลอดภัย (เช่น จาก vault).  
- ควรปิดสตรีมเสมอในบล็อก `finally` หรือใช้ try‑with‑resources เพื่อหลีกเลี่ยงการรั่วของทรัพยากร.  
- หากคุณได้รับค่า `true` จาก `isEncrypted` และ `ref[0]` เป็น `null` ไฟล์อาจถูกเข้ารหัส **หรือ** รหัสผ่านที่ให้ไม่ถูกต้อง ให้ขอรหัสผ่านที่ถูกต้องจากผู้ใช้และลองใหม่.  

## คำถามที่พบบ่อย  

**Q: ฉันสามารถตรวจสอบสถานะการเข้ารหัสโดยไม่ต้องให้รหัสผ่านได้หรือไม่?**  
A: ได้. เรียก `Document.isEncrypted` พร้อมอินสแตนซ์ `LoadOptions` ที่ไม่ได้ตั้งรหัสผ่าน; เมธอดจะรายงานว่าไฟล์ถูกเข้ารหัสหรือไม่.  

**Q: จะเกิดอะไรขึ้นหากฉันให้รหัสผ่านที่ไม่ถูกต้อง?**  
A: เมธอดจะคืนค่า `true` ซึ่งบ่งบอกว่าเอกสารยังคงถูกเข้ารหัสและ `ref[0]` จะเป็น `null`.  

**Q: มีวิธีการถอดรหัสเอกสารโดยโปรแกรมได้หรือไม่?**  
A: มี. เมื่อคุณรู้รหัสผ่านที่ถูกต้อง ให้ส่งรหัสผ่านนั้นไปยัง `LoadOptions` (หรือ overload ที่รับรหัสผ่าน) แล้วโหลดเอกสาร; API จะถอดรหัสให้โดยอัตโนมัติ.  

**Q: Aspose.Note ทำงานกับรูปแบบ Microsoft อื่น ๆ หรือไม่?**  
A: Aspose.Note ถูกออกแบบมาเฉพาะสำหรับไฟล์ OneNote (`.one`) เท่านั้น สำหรับ Word, Excel, PowerPoint ฯลฯ ให้พิจารณาใช้ Aspose.Words, Aspose.Cells, Aspose.Slides ตามลำดับ.  

**Q: ฉันจะหา ตัวอย่างและการสนับสนุนเพิ่มเติมได้จากที่ไหน?**  
A: เยี่ยมชม [Aspose.Note forum](https://forum.aspose.com/c/note/28) เพื่อรับความช่วยเหลือจากชุมชน และตรวจสอบเอกสารอย่างเป็นทางการสำหรับตัวอย่างโค้ดเพิ่มเติม.  

## สรุป  

ในคู่มือนี้เราได้สาธิต **วิธีตรวจสอบการเข้ารหัส OneNote** ด้วย Aspose.Note สำหรับ Java ครอบคลุมทั้งสถานการณ์ที่ใช้สตรีมและไฟล์ การรวมการตรวจสอบเหล่านี้เข้าในแอปพลิเคชันของคุณจะช่วยจัดการไฟล์ OneNote ที่เข้ารหัสได้อย่างราบรื่น ปรับปรุงประสบการณ์ผู้ใช้ และทำให้กระบวนการประมวลผลของคุณมั่นคง  

---  

**อัปเดตล่าสุด:** 2026-07-05  
**ทดสอบด้วย:** Aspose.Note 26.4 for Java  
**ผู้เขียน:** Aspose  

{{< blocks/products/products-backtop-button >}}

## บทเรียนที่เกี่ยวข้อง

- [สร้างเอกสาร OneNote – โหลด Notebook ด้วย Aspose.Note](/note/java/onenote-notebook-operations/loading-notebook/)
- [ป้องกัน OneNote ด้วยรหัสผ่านด้วย Aspose.Note สำหรับ Java](/note/java/onenote-notebook-operations/write-password-protected-document/)
- [รับข้อมูลรูปแบบไฟล์ Aspose Note จาก OneNote ด้วย Java](/note/java/onenote-document-loading/get-file-format-info/)


{{< /blocks/products/pf/tutorial-page-section >}}  
{{< /blocks/products/pf/main-container >}}  
{{< /blocks/products/pf/main-wrap-class >}}