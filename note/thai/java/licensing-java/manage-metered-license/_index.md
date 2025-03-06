---
title: จัดการใบอนุญาตแบบมิเตอร์สำหรับ OneNote ใน Java
linktitle: จัดการใบอนุญาตแบบมิเตอร์สำหรับ OneNote ใน Java
second_title: Aspose.Note Java API
description: เรียนรู้วิธีจัดการใบอนุญาตแบบคิดค่าบริการตามปริมาณข้อมูลสำหรับ OneNote ใน Java โดยใช้ไลบรารี Aspose.Note ควบคุมการใช้งาน ติดตามเครดิต และปรับต้นทุนให้เหมาะสมอย่างมีประสิทธิภาพ
weight: 10
url: /th/java/licensing-java/manage-metered-license/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# จัดการใบอนุญาตแบบมิเตอร์สำหรับ OneNote ใน Java

## การแนะนำ

ในบทช่วยสอนนี้ เราจะเรียนรู้วิธีจัดการสิทธิ์ใช้งานแบบคิดค่าบริการตามปริมาณข้อมูลสำหรับ OneNote โดยใช้ Aspose.Note สำหรับ Java ใบอนุญาตแบบคิดค่าบริการตามปริมาณข้อมูลช่วยให้คุณสามารถตรวจสอบและควบคุมการใช้งานของคุณตามเครดิต ซึ่งเป็นโซลูชันที่ยืดหยุ่นและคุ้มต้นทุน

## ข้อกำหนดเบื้องต้น

ก่อนที่เราจะเริ่มต้น ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นดังต่อไปนี้:

1.  Java Development Kit (JDK): ตรวจสอบให้แน่ใจว่าคุณได้ติดตั้ง JDK บนระบบของคุณแล้ว คุณสามารถดาวน์โหลดได้จาก[ที่นี่](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).
   
2. Aspose.Note สำหรับไลบรารี Java: คุณต้องมี Aspose.Note สำหรับไลบรารี Java คุณสามารถดาวน์โหลดได้จาก[เว็บไซต์](https://releases.aspose.com/note/java/).

## แพ็คเกจนำเข้า

ขั้นแรก นำเข้าแพ็คเกจที่จำเป็นไปยังโปรเจ็กต์ Java ของคุณ:

```java
import com.aspose.note.Document;
import com.aspose.note.Metered;



import java.nio.file.Paths;
```

## ขั้นตอนที่ 1: ตั้งค่าใบอนุญาตแบบมิเตอร์

```java
Metered metered = new Metered();
metered.setMeteredKey("MyPublicKey", "MyPrivateKey");
```

 ในขั้นตอนนี้ เราจะเริ่มต้นไฟล์`Metered` และตั้งค่าคีย์แบบมิเตอร์ด้วยคีย์สาธารณะและคีย์ส่วนตัวของคุณที่ Aspose มอบให้

## ขั้นตอนที่ 2: โหลดเอกสารและดำเนินการ

```java
String dataDir = "Your Document Directory";
Document doc = new Document(Paths.get(dataDir,"Sample1.one").toString());
doc.save(Paths.get(dataDir,"MeteredLicense.pdf").toString());
```

 ที่นี่ เราโหลดเอกสาร OneNote จากไดเร็กทอรีที่ระบุและบันทึกเป็นไฟล์ PDF ให้แน่ใจว่าจะเปลี่ยน`"Your Document Directory"` ด้วยเส้นทางไดเรกทอรีจริงของคุณ

## ขั้นตอนที่ 3: ตรวจสอบการบริโภค

```java
System.out.println(String.format("Credit before operation: %.02f", Metered.getConsumptionCredit()));
System.out.println(String.format("Consumption quantity before operation: %.02f", Metered.getConsumptionQuantity()));
```

ขั้นตอนนี้จะดึงข้อมูลและพิมพ์ปริมาณเครดิตและปริมาณการใช้ก่อนและหลังการดำเนินการ

## บทสรุป

ในบทช่วยสอนนี้ เราได้เรียนรู้วิธีจัดการสิทธิ์ใช้งานแบบคิดค่าบริการตามปริมาณข้อมูลสำหรับ OneNote ใน Java โดยใช้ไลบรารี Aspose.Note การออกใบอนุญาตแบบคิดค่าบริการตามปริมาณข้อมูลให้ความยืดหยุ่นและควบคุมการใช้งานของคุณ ทำให้มั่นใจได้ถึงความคุ้มค่าและการจัดการทรัพยากรที่มีประสิทธิภาพ

## คำถามที่พบบ่อย

### คำถามที่ 1: ใบอนุญาตแบบคิดค่าบริการตามปริมาณข้อมูลคืออะไร

ตอบ 1: ใบอนุญาตแบบมิเตอร์ช่วยให้คุณสามารถติดตามและควบคุมการใช้งาน API หรือบริการของคุณตามเครดิต
   
### คำถามที่ 2: ฉันจะรับคีย์แบบมิเตอร์สำหรับผลิตภัณฑ์ Aspose ได้อย่างไร

ตอบ 2: คุณสามารถขอรับคีย์แบบมิเตอร์ได้โดยการซื้อใบอนุญาตจากเว็บไซต์ Aspose หรือขอใบอนุญาตชั่วคราวเพื่อวัตถุประสงค์ในการประเมิน
   
### คำถามที่ 3: ฉันสามารถใช้สิทธิ์ใช้งานแบบคิดค่าบริการตามปริมาณข้อมูลกับหลายแอปพลิเคชันได้หรือไม่

A3: ได้ สิทธิ์ใช้งานแบบมิเตอร์สามารถใช้ได้กับหลายแอปพลิเคชัน แต่ปริมาณการใช้จะถูกรวมเข้าด้วยกัน
   
### คำถามที่ 4: Aspose.Note สำหรับ Java มีรุ่นทดลองใช้ฟรีหรือไม่

 A4: ได้ คุณสามารถดาวน์โหลดรุ่นทดลองใช้ฟรีได้จาก[ที่นี่](https://releases.aspose.com/).
   
### คำถามที่ 5: ฉันจะรับการสนับสนุนสำหรับ Aspose.Note สำหรับ Java ได้ที่ไหน

 A5: คุณสามารถรับการสนับสนุนจากฟอรัมชุมชน Aspose[ที่นี่](https://forum.aspose.com/c/note/28).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
