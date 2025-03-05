---
title: เปลี่ยนสไตล์ตารางใน OneNote - Aspose.Note
linktitle: เปลี่ยนสไตล์ตารางใน OneNote - Aspose.Note
second_title: Aspose.Note Java API
description: ปรับปรุงตาราง OneNote ของคุณอย่างง่ายดายด้วย Aspose.Note สำหรับ Java ปฏิบัติตามคำแนะนำทีละขั้นตอนของเราเพื่อเปลี่ยนสไตล์ตาราง ดาวน์โหลดห้องสมุดทันที!
type: docs
weight: 10
url: /th/java/onenote-table-manipulation/change-table-style/
---
## การแนะนำ
Aspose.Note for Java เป็นไลบรารีอันทรงพลังที่ช่วยให้นักพัฒนาจัดการไฟล์ OneNote ได้อย่างง่ายดาย ในบทช่วยสอนนี้ เราจะเน้นที่การเปลี่ยนสไตล์ตารางในเอกสาร OneNote โดยใช้ Aspose.Note สำหรับ Java ทำตามคำแนะนำทีละขั้นตอนเพื่อเพิ่มความสวยงามให้กับโต๊ะของคุณ
## ข้อกำหนดเบื้องต้น
ก่อนที่คุณจะเริ่มต้น ตรวจสอบให้แน่ใจว่าคุณมีสิ่งต่อไปนี้:
- สภาพแวดล้อมการพัฒนา Java: ตรวจสอบให้แน่ใจว่าคุณได้ตั้งค่าสภาพแวดล้อมการพัฒนา Java บนเครื่องของคุณ
-  Aspose.Note สำหรับไลบรารี Java: ดาวน์โหลดและติดตั้ง Aspose.Note สำหรับไลบรารี Java จาก[หน้าดาวน์โหลด](https://releases.aspose.com/note/java/).
- ไดเรกทอรีเอกสาร: เตรียมไดเรกทอรีเพื่อจัดเก็บเอกสาร OneNote ของคุณ
## แพ็คเกจนำเข้า
ในโปรเจ็กต์ Java ของคุณ ให้นำเข้าแพ็คเกจที่จำเป็นเพื่อทำงานกับ Aspose หมายเหตุ:
```java
import com.aspose.note.*;
import java.awt.Color;
import java.io.IOException;
import java.nio.file.Paths;
import java.util.List;
```
## ขั้นตอนที่ 1: ตั้งค่าเอกสาร
โหลดเอกสาร OneNote ลงใน Aspose.Note และเรียกข้อมูลรายการโหนดตาราง
```java
// ตั้งค่าเอกสารและรับรายการโหนดตาราง
String dataDir = "Your Document Directory";
Document document = new Document(dataDir + "ChangeTableStyleIn.one");
List<Table> nodes = document.getChildNodes(Table.class);
```
## ขั้นตอนที่ 2: ตั้งค่าสไตล์แถว
วนซ้ำแต่ละตาราง ตั้งค่าสไตล์สำหรับแต่ละแถว รวมถึงการไฮไลต์แถวแรกหลังส่วนหัว

```java
// กำหนดรูปแบบแถวให้กับแต่ละตารางในเอกสาร
for (Table table : nodes) {
    setRowStyle(table.getFirstChild(), Color.GRAY, true, true);
    // ไฮไลท์แถวแรกหลังส่วนหัว
    boolean flag = false;
    List<TableRow> rows = table.getChildren();
    for (int i = 1; i < rows.size(); ++i) {
        setRowStyle(rows.get(i), flag ? Color.lightGray : new java.awt.Color(-1, true), false, false);
        flag = !flag;
    }
}
```
## วิธีการ setRowStyle
```java
    private static void setRowStyle(TableRow row, Color highlightColor, boolean bold, boolean italic) {
        for (TableCell cell: row)
        {
            cell.setBackgroundColor(highlightColor);
            for (RichText node: cell.getChildNodes(RichText.class))
            {
                node.getParagraphStyle().setBold(bold);
                node.getParagraphStyle().setItalic(italic);
                for (TextRun run: node.getTextRuns())
                {
                    run.getStyle().setBold(bold);
                    run.getStyle().setItalic(italic);
                }
            }
        }
    }
```
## ขั้นตอนที่ 3: บันทึกเอกสาร
บันทึกเอกสารที่แก้ไขด้วยสไตล์ตารางใหม่
เมื่อทำตามขั้นตอนเหล่านี้ คุณจะสามารถเปลี่ยนสไตล์ตารางในเอกสาร OneNote ได้อย่างง่ายดายโดยใช้ Aspose.Note for Java

```java
// บันทึกเอกสารที่แก้ไข
document.save(Paths.get(dataDir, "ChangeTableStyleOut.one").toString());
```
## บทสรุป
Aspose.Note สำหรับ Java ช่วยให้กระบวนการจัดการไฟล์ OneNote ง่ายขึ้น ด้วยการใช้ประโยชน์จากความสามารถของไลบรารี คุณสามารถปรับปรุงการนำเสนอด้วยภาพตารางของคุณได้อย่างง่ายดาย

## คำถามที่พบบ่อย
### ฉันจะหาเอกสารสำหรับ Aspose.Note สำหรับ Java ได้ที่ไหน
 เยี่ยมชม[เอกสารประกอบ](https://reference.aspose.com/note/java/) เพื่อรับคำแนะนำอย่างครอบคลุม
### ฉันจะขอรับใบอนุญาตชั่วคราวสำหรับ Aspose.Note สำหรับ Java ได้อย่างไร
 ปฏิบัติตามนี้[ลิงค์](https://purchase.aspose.com/temporary-license/) เพื่อรับใบอนุญาตชั่วคราว
### มีการทดลองใช้ฟรีสำหรับ Aspose.Note สำหรับ Java หรือไม่
 ใช่ คุณสามารถดาวน์โหลดเวอร์ชันทดลองใช้ฟรีได้จาก[ที่นี่](https://releases.aspose.com/).
### ฉันจะรับการสนับสนุนสำหรับ Aspose.Note สำหรับ Java ได้ที่ไหน
 เข้าร่วม[ฟอรั่ม Aspose.Note](https://forum.aspose.com/c/note/28) เพื่อขอความช่วยเหลือจากชุมชน
### ฉันจะซื้อ Aspose.Note สำหรับ Java ได้อย่างไร
 คุณสามารถซื้อห้องสมุดได้[ที่นี่](https://purchase.aspose.com/buy).