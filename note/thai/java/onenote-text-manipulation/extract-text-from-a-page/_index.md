---
title: แยกข้อความจากหน้าใน OneNote - Aspose.Note
linktitle: แยกข้อความจากหน้าใน OneNote - Aspose.Note
second_title: Aspose.Note Java API
description: ค้นพบวิธีแยกข้อความจากหน้า OneNote ได้อย่างง่ายดายโดยใช้ Aspose.Note for Java ปรับปรุงกระบวนการของคุณด้วยคำแนะนำทีละขั้นตอนที่ครอบคลุมนี้
weight: 16
url: /th/java/onenote-text-manipulation/extract-text-from-a-page/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# แยกข้อความจากหน้าใน OneNote - Aspose.Note

## การแนะนำ
หากคุณต้องการปลดล็อกศักยภาพในการแยกข้อความจากหน้า OneNote อย่างมีประสิทธิภาพโดยใช้ Java คุณมาถูกที่แล้ว คำแนะนำทีละขั้นตอนนี้จะแนะนำคุณตลอดกระบวนการโดยใช้ Aspose.Note สำหรับ Java Aspose.Note เป็น API อันทรงพลังที่ทำให้การทำงานกับเอกสาร OneNote ง่ายขึ้น ช่วยให้คุณสามารถแยกข้อความจากหน้าต่างๆ ได้อย่างราบรื่น
## ข้อกำหนดเบื้องต้น
ก่อนที่จะเข้าสู่บทช่วยสอน ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:
- ความเข้าใจพื้นฐานเกี่ยวกับการเขียนโปรแกรม Java
-  ติดตั้ง Aspose.Note สำหรับ Java แล้ว คุณสามารถดาวน์โหลดได้[ที่นี่](https://releases.aspose.com/note/java/).
## แพ็คเกจนำเข้า
เริ่มต้นด้วยการนำเข้าแพ็คเกจที่จำเป็นในโปรเจ็กต์ Java ของคุณเพื่อใช้ประโยชน์จากฟังก์ชัน Aspose.Note:
```java
import com.aspose.note.Document;
import com.aspose.note.Node;
import com.aspose.note.NodeType;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import java.util.List;
import java.util.stream.Collectors;
```
ตอนนี้เรามาดูรายละเอียดแต่ละขั้นตอนกัน
## ขั้นตอนที่ 1: ตั้งค่าไดเรกทอรีเอกสาร
 ตรวจสอบให้แน่ใจว่าคุณมีไดเร็กทอรีเอกสารที่กำหนดซึ่งเก็บไฟล์ OneNote ของคุณ แทนที่`"Your Document Directory"` กับเส้นทางที่แท้จริง
```java
// เส้นทางไปยังไดเร็กทอรีเอกสาร
String dataDir = "Your Document Directory";
```
## ขั้นตอนที่ 2: โหลดเอกสาร OneNote
 ใช้`Document` คลาสจาก Aspose.Note เพื่อโหลดเอกสาร OneNote ของคุณ:
```java
Document oneFile = new Document(dataDir + "Sample1.one");
```
 แทนที่`"Sample1.one"` ด้วยชื่อไฟล์ OneNote ของคุณ
## ขั้นตอนที่ 3: ดึงโหนดหน้า
รับรายการโหนดหน้าจากเอกสารที่โหลด:
```java
List<Node> nodes = oneFile.getChildNodes(Node.class);
```
เพื่อให้แน่ใจว่าคุณจะสามารถเข้าถึงหน้าต่างๆ ภายในเอกสาร OneNote ได้
## ขั้นตอนที่ 4: ตรวจสอบและแยกข้อความ
ตรวจสอบว่าเอกสารมีหน้าหรือไม่ และหากมี ให้ดึงข้อความ:
```java
if (nodes.size() > 0 && nodes.get(0).getNodeType() == NodeType.Page)
{
    Page page = (Page)nodes.get(0);
    // ดึงข้อความ
    List<RichText> textNodes = (List<RichText>) page.getChildNodes(RichText.class);
    StringBuilder text = new StringBuilder();
    for (RichText richText : textNodes) {
        text = text.append(richText.getText().toString());
    }
    
    // พิมพ์ข้อความบนหน้าจอเอาท์พุต
    System.out.println(text);
}
```
ตัวอย่างนี้จะตรวจสอบว่าโหนดแรกเป็นหน้าหรือไม่ จากนั้นแยกและพิมพ์ข้อความ
ทำตามขั้นตอนเหล่านี้เพื่อปรับปรุงความสามารถของแอปพลิเคชัน Java ของคุณในการแยกข้อความจากหน้า OneNote โดยใช้ Aspose.Note สำหรับ Java
## บทสรุป
ยินดีด้วย! คุณได้เรียนรู้วิธีแยกข้อความจากหน้า OneNote โดยใช้ Aspose.Note for Java เรียบร้อยแล้ว รวมความรู้นี้เข้ากับโครงการของคุณและปรับปรุงกระบวนการแยกข้อความของคุณได้อย่างง่ายดาย
## คำถามที่พบบ่อย
### ฉันสามารถใช้ Aspose.Note สำหรับ Java กับภาษาการเขียนโปรแกรมอื่นได้หรือไม่
Aspose.Note รองรับ Java เป็นหลัก แต่มีเวอร์ชันสำหรับภาษาอื่น เช่น .NET ตรวจสอบเอกสารประกอบสำหรับความเข้ากันได้ของภาษา
### มีเวอร์ชันทดลองใช้สำหรับ Aspose.Note สำหรับ Java หรือไม่
 ใช่ คุณสามารถสำรวจเวอร์ชันทดลองใช้ฟรีได้[ที่นี่](https://releases.aspose.com/).
### ฉันจะรับการสนับสนุนสำหรับ Aspose.Note สำหรับ Java ได้ที่ไหน
 เยี่ยมชม Aspose.Note[ฟอรั่ม](https://forum.aspose.com/c/note/28) สำหรับการสนับสนุนและการอภิปรายของชุมชน
### ฉันจะซื้อ Aspose.Note สำหรับ Java ได้อย่างไร
 ท่านสามารถซื้อสินค้าได้[ที่นี่](https://purchase.aspose.com/buy).
### ฉันจำเป็นต้องมีใบอนุญาตชั่วคราวสำหรับ Aspose.Note สำหรับ Java หรือไม่
 หากคุณต้องการใบอนุญาตชั่วคราว คุณสามารถขอรับได้[ที่นี่](https://purchase.aspose.com/temporary-license/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
