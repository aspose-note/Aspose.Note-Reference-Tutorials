---
date: 2026-01-05
description: เรียนรู้วิธีตั้งค่า locale เริ่มต้น, โหลดเอกสาร OneNote, ตั้งค่าใบอนุญาต
  Aspose, แปลง OneNote เป็น PNG และบันทึก OneNote เป็นภาพโดยใช้ Aspose.Note สำหรับ
  Java.
linktitle: Working with Locales in OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: ตั้งค่าภูมิภาคเริ่มต้นใน OneNote – Aspose.Note Java
url: /th/java/onenote-notebook-operations/working-with-locales/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# ตั้งค่า Locale เริ่มต้นใน OneNote – Aspose.Note Java

## บทนำ

หากคุณต้องการ **ตั้งค่า locale เริ่มต้น** ขณะประมวลผลไฟล์ OneNote, Aspose.Note สำหรับ Java ทำให้เรื่องนี้ง่ายดายมาก ในบทแนะนำนี้เราจะพาคุณผ่านทุกขั้นตอนที่จำเป็น—from การเปิดใช้งานใบอนุญาตผลิตภัณฑ์ไปจนถึงการโหลดเอกสาร OneNote, การเปลี่ยน locale, และสุดท้ายการแปลงไฟล์เป็นภาพ PNG. เมื่อเสร็จสิ้นคุณจะสามารถปรับแต่งการตั้งค่าภาษาและสร้างผลลัพธ์ที่เฉพาะเจาะจงตาม locale ได้ด้วยเพียงไม่กี่บรรทัดของโค้ด.

## คำตอบอย่างรวดเร็ว
- **“set default locale” ทำอะไร?** มันกำหนดภาษและรูปแบบการจัดรูปแบบตามภูมิภาคที่ Aspose.Note ใช้เมื่ออ่านหรือเขียนไฟล์ OneNote.  
- **ต้องมีใบอนุญาตหรือไม่?** ต้อง—ตั้งค่าใบอนุญาต Aspose เพื่อเปิดใช้งานฟังก์ชันทั้งหมด.  
- **ต้องใช้ Java เวอร์ชันใด?** รองรับ JDK 8 ขึ้นไปทั้งหมด.  
- **สามารถแปลง OneNote เป็น PNG ได้หรือไม่?** แน่นอน; API ให้คุณบันทึกหน้าเป็นภาพ.  
- **กระบวนการนี้ปลอดภัยต่อเธรดหรือไม่?** การตั้งค่า locale เริ่มต้นเป็นการตั้งค่าทั่วโลก, ดังนั้นให้กำหนดค่าเพียงครั้งเดียวเมื่อตัวแอปพลิเคชันเริ่มทำงาน.

## “set default locale” คืออะไรใน Aspose.Note?
การตั้งค่า locale เริ่มต้นบอก Aspose.Note ว่าจะใช้ภาษาและขนบธรรมเนียมทางวัฒนธรรมใดเมื่อทำการแยกวิเคราะห์วันที่, ตัวเลข, และข้อความ. สิ่งนี้สำคัญสำหรับแอปพลิเคชันหลายภูมิภาคที่ต้องการการจัดรูปแบบที่สอดคล้องกันในแต่ละ locale ของผู้ใช้.

## ทำไมต้องตั้งค่า locale เริ่มต้นเมื่อทำงานกับ OneNote?
- **การแสดงข้อมูลที่แม่นยำ:** วันที่และตัวเลขจะแสดงอย่างถูกต้องตามกลุ่มเป้าหมาย.  
- **สตริง UI ที่สอดคล้อง:** ข้อความที่ดึงจาก OneNote จะเคารพการตั้งค่าภาษา.  
- **การแปลงที่ง่ายขึ้น:** เมื่อคุณแปลงไฟล์ OneNote เป็น PNG หรือรูปแบบอื่น ๆ ภาพที่ได้จะสอดคล้องกับ locale ที่คาดหวัง.

## ข้อกำหนดเบื้องต้น

- **Java Development Environment:** ติดตั้ง JDK และกำหนดค่า `JAVA_HOME` แล้ว.  
- **Aspose.Note Library:** ดาวน์โหลด JAR เวอร์ชันล่าสุดจาก [download link](https://releases.aspose.com/note/java/).  
- **ไฟล์ใบอนุญาต Aspose ที่ถูกต้อง** (เวอร์ชันทดลองฟรีใช้สำหรับการทดสอบได้).

## นำเข้าแพ็กเกจ

ก่อนเขียนโค้ดใด ๆ ให้ทำการนำเข้าคลาสที่ให้ฟังก์ชันที่จำเป็น.

```java
import java.io.IOException;
import java.nio.file.Path;
import java.util.Locale;
import com.aspose.note.Document;
import com.aspose.note.License;
import com.aspose.note.LocaleOptions;
```

## ขั้นตอนที่ 1: ตั้งค่าใบอนุญาต Aspose

```java
License license = new License();
license.setLicense("licenseFile");
```

การตั้งค่าใบอนุญาต Aspose จะปลดล็อกฟีเจอร์ทั้งหมด, รวมถึงการจัดการ locale และการแปลงภาพ.

## ขั้นตอนที่ 2: ตั้งค่า Locale เริ่มต้น

```java
java.util.Locale.setDefault(new java.util.Locale("en", "rs"));
```

ที่นี่เราจะ **ตั้งค่า locale เริ่มต้น** เป็นภาษาอังกฤษ (`en`) พร้อมรหัสประเทศ `rs`. ปรับรหัสภาษาและประเทศให้ตรงกับภูมิภาคเป้าหมายของคุณ.

## ขั้นตอนที่ 3: โหลดเอกสาร OneNote

```java
String inputFile = "Sample1.one";
Path inputPath = Paths.get(inputFile);

Document oneFile = new Document(inputPath.toString());
```

ขั้นตอนนี้ **โหลดเอกสาร OneNote** เข้าไปในอ็อบเจ็กต์ `Document` เพื่อให้คุณสามารถทำงานกับเนื้อหาภายในได้.

## ขั้นตอนที่ 4: แปลง OneNote เป็น PNG (การแปลงไฟล์ OneNote)

```java
oneFile.save("sample.png");
```

เมธอด `save` ทำการ **การแปลงไฟล์ onenote**, ส่งออกสมุดบันทึก (หรือหน้าที่ระบุ) เป็นภาพ PNG—โดยตรงคือ **convert onenote to png** และ **save onenote as image**.

## ปัญหาที่พบบ่อยและเคล็ดลับ

- **ไม่พบใบอนุญาต:** ตรวจสอบให้แน่ใจว่าเส้นทางไปยัง `licenseFile` ถูกต้องและไฟล์มีสิทธิ์อ่าน.  
- **Locale ไม่ถูกนำไปใช้:** เรียก `Locale.setDefault` **ก่อน** โหลดเอกสาร.  
- **ไม่มีผลลัพธ์ภาพ:** ตรวจสอบว่าไฟล์ OneNote มีหน้าที่สามารถเรนเดอร์ได้; สมุดบันทึกที่ว่างเปล่าจะสร้าง PNG ที่ว่างเปล่า.

## คำถามที่พบบ่อย

**Q: Aspose.Note รองรับเวอร์ชัน Java ต่าง ๆ หรือไม่?**  
A: ใช่, Aspose.Note รองรับ Java 8 และรุ่นต่อ ๆ ไป, ทำให้เข้ากันได้กับสภาพแวดล้อมการพัฒนาต่าง ๆ อย่างกว้างขวาง.

**Q: สามารถผสาน Aspose.Note กับไลบรารี Java อื่นได้หรือไม่?**  
A: แน่นอน. API ทำงานร่วมกับไลบรารียอดนิยมเช่น Apache POI, Jackson, และ Spring อย่างไร้รอยต่อ.

**Q: Aspose.Note มีการสนับสนุนรูปแบบไฟล์ต่าง ๆ หรือไม่?**  
A: แม้ว่าจุดเด่นหลักจะเป็นไฟล์ OneNote, ไลบรารีนี้สามารถส่งออกเป็น PNG, JPEG, PDF, และรูปแบบภาพอื่น ๆ ได้.

**Q: มีฟอรั่มชุมชนสำหรับผู้ใช้ Aspose.Note เพื่อขอความช่วยเหลือและแบ่งปันความรู้หรือไม่?**  
A: มี, ฟอรั่มชุมชนของ Aspose ให้แพลตฟอร์มสำหรับผู้ใช้ในการติดต่อผู้เชี่ยวชาญ, ถามคำถาม, และร่วมมือแก้ปัญหา. เยี่ยมชม [support forum](https://forum.aspose.com/c/note/28) เพื่อรับความช่วยเหลือ.

**Q: สามารถทดลองใช้ Aspose.Note ก่อนซื้อได้หรือไม่?**  
A: ได้เลย, คุณสามารถสำรวจความสามารถของ Aspose.Note ได้โดยใช้เวอร์ชันทดลองฟรีที่เว็บไซต์ให้บริการ.

## สรุป

โดยทำตามขั้นตอนเหล่านี้คุณได้เรียนรู้วิธี **ตั้งค่า locale เริ่มต้น**, **โหลดเอกสาร OneNote**, **ตั้งค่าใบอนุญาต Aspose**, และ **แปลง OneNote เป็น PNG** ด้วย Aspose.Note สำหรับ Java. กระบวนการนี้ช่วยให้คุณสร้างรายงานและภาพที่รับรู้ locale ได้อย่างเหมาะสมสำหรับผู้ชมทั่วโลก.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**อัปเดตล่าสุด:** 2026-01-05  
**ทดสอบด้วย:** Aspose.Note 24.11 for Java  
**ผู้เขียน:** Aspose