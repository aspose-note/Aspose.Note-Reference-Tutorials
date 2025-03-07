---
title: สร้างเอกสารจากเทมเพลตใน OneNote - Aspose.Note
linktitle: สร้างเอกสารจากเทมเพลตใน OneNote - Aspose.Note
second_title: Aspose.Note Java API
description: สร้างเอกสารไดนามิกอย่างง่ายดายโดยใช้ Aspose.Note สำหรับ Java ปฏิบัติตามคำแนะนำทีละขั้นตอนของเราเพื่อสร้างเอกสารอย่างมีประสิทธิภาพจากเทมเพลต
weight: 18
url: /th/java/onenote-text-manipulation/generate-document-from-template/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# สร้างเอกสารจากเทมเพลตใน OneNote - Aspose.Note

## การแนะนำ
คุณกำลังมองหาวิธีปรับปรุงการสร้างเอกสารในแอปพลิเคชัน Java ของคุณหรือไม่? Aspose.Note สำหรับ Java มอบโซลูชันอันทรงพลัง ในบทช่วยสอนนี้ เราจะแนะนำคุณตลอดขั้นตอนการสร้างเอกสารจากเทมเพลตโดยใช้ Aspose.Note สำหรับ Java ซึ่งทำให้กระบวนการทั้งหมดง่ายและมีประสิทธิภาพ
## ข้อกำหนดเบื้องต้น
ก่อนที่จะเข้าสู่บทช่วยสอน ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:
- ความเข้าใจพื้นฐานเกี่ยวกับการเขียนโปรแกรม Java
-  Aspose.Note สำหรับไลบรารี Java หากไม่ได้ติดตั้ง ให้ดาวน์โหลดจาก[ที่นี่](https://releases.aspose.com/note/java/).
- เอกสารเทมเพลต (เช่น "JobOffer.one") สำหรับการสร้างเอกสาร
## แพ็คเกจนำเข้า
เริ่มต้นด้วยการนำเข้าแพ็คเกจที่จำเป็นไปยังโปรเจ็กต์ Java ของคุณ ขั้นตอนนี้ช่วยให้แน่ใจว่าคุณสามารถเข้าถึงฟังก์ชันการทำงานทั้งหมดที่มีให้โดย Aspose.Note สำหรับ Java
```java
import com.aspose.note.*;
import java.io.IOException;
import java.nio.file.Paths;
import java.util.HashMap;
import java.util.Map;
import com.aspose.note.RichText
```
## ขั้นตอนที่ 1: กำหนดข้อมูลเทมเพลต
ที่นี่เรากำหนดแฮชแมป (`D`) โดยมีคู่คีย์-ค่าที่แสดงถึงข้อมูลเทมเพลต ค่าเหล่านี้จะแทนที่ตัวยึดตำแหน่งในเอกสารเทมเพลต
```java
// เส้นทางไปยังไดเร็กทอรีเอกสาร
String dataDir = "Your Document Directory";
HashMap<String, String> D = new HashMap<>();
D.put("Company", "Atlas Shrugged Ltd");
D.put("CandidateName", "John Galt");
D.put("JobTitle", "Chief Entrepreneur Officer");
D.put("Department", "Sales");
D.put("Salary", "123456 USD");
D.put("Vacation", "30");
D.put("StartDate", "29 Feb 2024");
D.put("YourName", "Ayn Rand");
```
ตรวจสอบให้แน่ใจว่าคุณแทนที่ "Your Document Directory" ด้วยเส้นทางไดเรกทอรีจริง
## ขั้นตอนที่ 2: โหลดเอกสารเทมเพลต
 ตอนนี้ เราโหลดเอกสารเทมเพลต ("JobOffer.one") โดยใช้`Document`คลาสจาก Aspose.Note สำหรับ Java
```java
// โหลดเอกสารเทมเพลตลงใน Aspose.Note
Document d = new Document(Paths.get(dataDir, "JobOffer.one").toString());
```
## ขั้นตอนที่ 3: แทนที่คำเทมเพลต
ในขั้นตอนนี้ เราจะวนซ้ำโหนดย่อยของเอกสารเพื่อแทนที่คำเทมเพลตด้วยค่าที่เกี่ยวข้องจากแฮชแมป
```java
// มาแทนที่คำเทมเพลตทั้งหมด
for (RichText e : d.getChildNodes(RichText.class)) {
    for (Map.Entry<String, String> replace : D.entrySet()) {
        e.replace(String.format("${%s}", replace.getKey()), replace.getValue());
    }
}
```
เพื่อให้แน่ใจว่าแต่ละตัวยึดตำแหน่งในเอกสารจะถูกแทนที่ด้วยข้อมูลที่เกี่ยวข้อง
## ขั้นตอนที่ 4: บันทึกเอกสารที่สร้างขึ้น
หลังจากแทนที่คำเทมเพลต เราจะบันทึกเอกสารที่แก้ไขด้วยชื่อใหม่ (เช่น "JobOffer_out.one") ลงในไดเร็กทอรีที่ระบุ
```java
// บันทึกเอกสารที่แก้ไขด้วยชื่อใหม่ (เช่น "JobOffer_out.one") ไปยังไดเร็กทอรีที่คุณระบุ
d.save(Paths.get(dataDir, "JobOffer_out.one").toString());
```
## ขั้นตอนที่ 5: ยืนยันการสร้างที่ประสบความสำเร็จ
สุดท้ายนี้ เราจะแสดงข้อความยืนยันเพื่อระบุว่าสร้างเอกสารสำเร็จแล้ว
```java
// แสดงข้อความยืนยัน
System.out.println("\nThe document is generated successfully.");
```
ด้วยขั้นตอนโดยละเอียดเหล่านี้และข้อมูลโค้ดที่เกี่ยวข้อง คุณสามารถสร้างเอกสารจากเทมเพลตโดยใช้ Aspose.Note สำหรับ Java ได้อย่างราบรื่น หากคุณมีคำถามเพิ่มเติม อย่าลังเลที่จะถาม!
ขณะนี้ เมื่อรวมข้อมูลโค้ดเหล่านี้แล้ว คุณจะมีคำแนะนำทีละขั้นตอนที่ครอบคลุมพร้อมโค้ดสำหรับสร้างเอกสารโดยใช้ Aspose.Note สำหรับ Java โปรดติดต่อเราหากคุณมีคำถามเพิ่มเติม
## บทสรุป
ยินดีด้วย! คุณได้เรียนรู้วิธีสร้างเอกสารจากเทมเพลตโดยใช้ Aspose.Note สำหรับ Java เรียบร้อยแล้ว กระบวนการที่ได้รับการปรับปรุงนี้สามารถปรับปรุงเวิร์กโฟลว์การสร้างเอกสารของคุณได้อย่างมาก
## คำถามที่พบบ่อย
### ฉันสามารถใช้ Aspose.Note สำหรับ Java กับภาษาการเขียนโปรแกรมอื่นได้หรือไม่
Aspose.Note รองรับ Java เป็นหลัก แต่มีเวอร์ชันสำหรับภาษาอื่น เช่น .NET
### Aspose.Note สำหรับ Java เข้ากันได้กับรูปแบบเอกสารที่แตกต่างกันหรือไม่
ใช่ Aspose.Note รองรับรูปแบบต่างๆ รวมถึง OneNote, PDF และรูปภาพ
### ฉันจะหาตัวอย่างและเอกสารประกอบเพิ่มเติมได้ที่ไหน
 อ้างถึง[เอกสารประกอบ](https://reference.aspose.com/note/java/) สำหรับคำแนะนำและตัวอย่างที่ครอบคลุม
### ฉันจะรับการสนับสนุนสำหรับ Aspose.Note สำหรับ Java ได้อย่างไร
 เยี่ยมชม[ฟอรั่ม Aspose.Note](https://forum.aspose.com/c/note/28)เพื่อขอความช่วยเหลือจากชุมชนและสนับสนุน
### มีการทดลองใช้ฟรีหรือไม่?
 ใช่ คุณสามารถเข้าถึง[ทดลองฟรี](https://releases.aspose.com/) เพื่อสำรวจคุณสมบัติก่อนตัดสินใจซื้อ
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
