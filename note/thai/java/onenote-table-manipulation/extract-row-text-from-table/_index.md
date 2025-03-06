---
title: แยกข้อความแถวออกจากตารางในเอกสาร OneNote - Aspose.Note
linktitle: แยกข้อความแถวออกจากตารางในเอกสาร OneNote - Aspose.Note
second_title: Aspose.Note Java API
description: เรียนรู้การแยกข้อความแถวจากตาราง OneNote ได้อย่างง่ายดายด้วย Aspose.Note สำหรับ Java ปฏิบัติตามคำแนะนำทีละขั้นตอนของเราเพื่อการบูรณาการที่ราบรื่น
weight: 13
url: /th/java/onenote-table-manipulation/extract-row-text-from-table/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# แยกข้อความแถวออกจากตารางในเอกสาร OneNote - Aspose.Note

## การแนะนำ
ยินดีต้อนรับสู่บทช่วยสอนที่ครอบคลุมเกี่ยวกับการแยกข้อความแถวออกจากตารางในเอกสาร OneNote โดยใช้ Aspose.Note สำหรับ Java Aspose.Note เป็นไลบรารี Java อันทรงพลังที่ช่วยให้นักพัฒนาสามารถทำงานกับไฟล์ Microsoft OneNote ได้อย่างราบรื่น ในบทช่วยสอนนี้ เราจะแนะนำคุณตลอดกระบวนการทีละขั้นตอน ซึ่งสาธิตวิธีการแยกข้อความแถวจากตารางในเอกสาร OneNote ของคุณอย่างมีประสิทธิภาพ
## ข้อกำหนดเบื้องต้น
ก่อนที่เราจะเจาะลึกบทช่วยสอน ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:
-  Aspose.Note สำหรับไลบรารี Java: ตรวจสอบให้แน่ใจว่าคุณได้ติดตั้ง Aspose.Note สำหรับไลบรารี Java แล้ว คุณสามารถดาวน์โหลดได้จาก[ลิ้งค์ดาวน์โหลด](https://releases.aspose.com/note/java/).
- สภาพแวดล้อมการพัฒนา Java: ตรวจสอบให้แน่ใจว่าคุณได้ตั้งค่าสภาพแวดล้อมการพัฒนา Java บนเครื่องของคุณ
- เอกสาร OneNote: เตรียมเอกสาร OneNote ตัวอย่าง (เช่น "Sample1.one") ที่มีตารางที่คุณต้องการแยกข้อความแถว
## แพ็คเกจนำเข้า
ในโปรเจ็กต์ Java ของคุณ ให้นำเข้าแพ็คเกจ Aspose.Note ที่จำเป็น เพื่อให้แน่ใจว่าคุณจะสามารถเข้าถึงคลาสและวิธีการที่จำเป็นสำหรับการทำงานกับเอกสาร OneNote
```java
import java.io.IOException;
import java.util.List;
import java.util.stream.Collectors;
import com.aspose.note.Document;
import com.aspose.note.LoadOptions;
import com.aspose.note.RichText;
import com.aspose.note.Table;
import com.aspose.note.TableRow;
```
## ขั้นตอนที่ 1: ตั้งค่าไดเรกทอรีเอกสาร
```java
// เส้นทางไปยังไดเร็กทอรีเอกสาร
String dataDir = "Your Document Directory";
```
## ขั้นตอนที่ 2: โหลดเอกสาร OneNote
```java
// โหลดเอกสารลงใน Aspose.Note
Document document = new Document(dataDir + "Sample1.one", new LoadOptions());
```
## ขั้นตอนที่ 3: รับโหนดตาราง
```java
// รับรายการโหนดตาราง
List<Table> nodes = (List<Table>) document.getChildNodes(Table.class);
```
## ขั้นตอนที่ 4: วนซ้ำตารางและแถว
```java
// ตั้งค่าการนับแถว
int rowCount = 0;
for (Table table : nodes) {
    // วนซ้ำตามแถวของตาราง
    for (TableRow row : table) {
        rowCount++;
        // ดึงข้อความ
        List<RichText> textNodes = (List<RichText>) row.getChildNodes(RichText.class);
        StringBuilder text = new StringBuilder();
        for (RichText richText : textNodes) {
            text = text.append(richText.getText().toString());
        }
        // พิมพ์ข้อความบนหน้าจอเอาท์พุต
        System.out.println(text);
    }
}
```
ทำซ้ำขั้นตอนเหล่านี้สำหรับแต่ละตารางในเอกสาร OneNote ของคุณ และคุณจะแยกข้อความแถวได้สำเร็จ
## บทสรุป
ยินดีด้วย! คุณได้เรียนรู้วิธีแยกข้อความแถวออกจากตารางในเอกสาร OneNote โดยใช้ Aspose.Note สำหรับ Java บทช่วยสอนนี้เป็นพื้นฐานสำหรับการใช้ประโยชน์จากความสามารถอันทรงพลังของ Aspose.Note ในแอปพลิเคชัน Java ของคุณ
## คำถามที่พบบ่อย
### Aspose.Note เข้ากันได้กับ Microsoft OneNote เวอร์ชันล่าสุดหรือไม่
 Aspose.Note รองรับ OneNote เวอร์ชันต่างๆ รวมถึงเวอร์ชันล่าสุดด้วย อ้างถึง[เอกสารประกอบ](https://reference.aspose.com/note/java/) สำหรับรายละเอียดความเข้ากันได้
### ฉันสามารถลองใช้ Aspose.Note สำหรับ Java ก่อนซื้อได้หรือไม่
ใช่ คุณสามารถทดลองใช้ Aspose.Note เวอร์ชันทดลองใช้ฟรีได้ที่[ลิงค์นี้](https://releases.aspose.com/).
### ฉันจะรับการสนับสนุนและความช่วยเหลือเพิ่มเติมได้จากที่ไหน?
 เยี่ยมชม[ฟอรั่ม Aspose.Note](https://forum.aspose.com/c/note/28) สำหรับการสนับสนุนและการอภิปรายของชุมชน
### ฉันจะขอรับใบอนุญาตชั่วคราวสำหรับ Aspose.Note ได้อย่างไร
 รับใบอนุญาตชั่วคราวจาก[ลิงค์นี้](https://purchase.aspose.com/temporary-license/).
### มีข้อกำหนดระบบเฉพาะสำหรับการใช้ Aspose.Note สำหรับ Java หรือไม่
โปรดดูเอกสารประกอบสำหรับข้อกำหนดของระบบโดยละเอียด
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
