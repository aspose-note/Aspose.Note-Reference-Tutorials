---
date: 2026-01-15
description: เรียนรู้วิธีติดตามการเปลี่ยนแปลงใน OneNote และจัดการการแก้ไขหน้าในเอกสาร
  OneNote ด้วย Aspose.Note สำหรับ Java รวมตัวอย่างสรุปการแก้ไขและวิธีการแก้ไขวันที่ของการแก้ไข
linktitle: Working with Page Revisions in OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: ติดตามการเปลี่ยนแปลง OneNote – จัดการการแก้ไขหน้าโดยใช้ Aspose.Note
url: /th/java/onenote-page-manipulation/working-with-page-revisions/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# ทำงานกับการแก้ไขหน้าใน OneNote - Aspose.Note

## Introduction

OneNote เป็นเครื่องมือที่มีประสิทธิภาพสำหรับการจัดระเบียบโน้ต และเมื่อคุณต้องการ **track changes onenote** การจัดการการแก้ไขหน้าเป็นสิ่งสำคัญสำหรับการทำงานร่วมกันอย่างมีประสิทธิภาพ ด้วย Aspose.Note for Java คุณสามารถจัดการการแก้ไขได้โดยโปรแกรม ดูว่าใครแก้ไขหน้า และแม้กระทั่งปรับแต่งเวลาประทับ นี่คือบทแนะนำที่พาคุณผ่านแต่ละขั้นตอน ตั้งแต่การโหลดเอกสารจนถึงการอัปเดตสรุปการแก้ไข

## Quick Answers
- **“track changes onenote” หมายถึงอะไร?** หมายถึงการตรวจสอบว่าใครแก้ไขหน้า OneNote และเมื่อใด
- **ต้องใช้ไลบรารีอะไร?** Aspose.Note for Java.
- **ฉันสามารถเปลี่ยนผู้เขียนหรือวันที่ของการแก้ไขได้หรือไม่?** ใช่, โดยใช้ RevisionSummary API (`modify revision date`).
- **ฉันต้องมีไฟล์ OneNote ล่วงหน้าหรือไม่?** ใช่, จำเป็นต้องมีไฟล์ `.one` ตัวอย่าง
- **ต้องการใบอนุญาตสำหรับการใช้งานจริงหรือไม่?** จำเป็นต้องมีใบอนุญาต Aspose.Note ที่ถูกต้องสำหรับการใช้งานเชิงพาณิชย์

## What is a revision summary example?
A *revision summary* ให้ข้อมูลเมตาเกี่ยวกับการเปลี่ยนแปลงล่าสุดบนหน้า—ชื่อผู้เขียน, เวลาแก้ไขล่าสุด, และรายละเอียดอื่น ๆ ในคู่มือนี้เราจะดึงและแสดงข้อมูลนั้น, จากนั้นจะแสดงวิธี **modify revision date**.

## Why track changes onenote with Aspose.Note?
- **Collaboration:** ดูว่าใครทำการแก้ไขล่าสุดอย่างรวดเร็ว
- **Auditing:** เก็บประวัติการเปลี่ยนแปลงที่เชื่อถือได้เพื่อการปฏิบัติตามข้อกำหนด
- **Automation:** ผสานการจัดการการแก้ไขเข้ากับบริการ back‑end หรือเครื่องมือการย้ายข้อมูล

## Prerequisites

### สภาพแวดล้อมการพัฒนา Java
ตรวจสอบว่าคุณได้ติดตั้ง Java Development Kit (JDK) บนระบบของคุณแล้ว

### ไลบรารี Aspose.Note for Java
ดาวน์โหลดและติดตั้งไลบรารี Aspose.Note for Java จาก [here](https://releases.aspose.com/note/java/).

### เอกสาร OneNote
เตรียมเอกสาร OneNote ตัวอย่างสำหรับการทดสอบ

## Import Packages

In your Java project, import the necessary packages to work with Aspose.Note for Java.

```java
import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.RevisionSummary;
import java.io.IOException;
import java.util.Calendar;
```

เรามาแยกตัวอย่างที่ให้มาออกเป็นหลายขั้นตอนเพื่อความเข้าใจที่ชัดเจน

## Step 1: Load OneNote Document

First, load the OneNote document and get the first child page.

```java
String dataDir = "Your Document Directory";
Document document = new Document(dataDir + "Sample1.one");
Page page = document.getFirstChild();
```

## Step 2: Read Page Revision Summary

Read the content revision summary for the page. This is the **revision summary example** that shows who edited the page last.

```java
RevisionSummary pageRevisionInfo = page.getPageContentRevisionSummary();
System.out.println(String.format("Author:\t%s\nModified:\t%s",
        pageRevisionInfo.getAuthorMostRecent(),
        pageRevisionInfo.getLastModifiedTime().toString()));
```

## Step 3: Update Page Revision Summary

Update the page revision summary with a new author and a new modified date. This demonstrates how to **modify revision date** programmatically.

```java
pageRevisionInfo.setAuthorMostRecent("New Author");
Calendar modifiedDate = Calendar.getInstance();
pageRevisionInfo.setLastModifiedTime(modifiedDate.getTime());
document.save(dataDir + "WorkingWithPageRevisions_out.one");
```

## Conclusion

การจัดการการแก้ไขหน้าในเอกสาร OneNote ด้วยโปรแกรมสามารถทำได้ง่ายขึ้นด้วย Aspose.Note for Java โดยการทำตามขั้นตอนในบทแนะนำนี้ คุณจะสามารถ **track changes onenote** ได้อย่างมีประสิทธิภาพ, ดูรายละเอียดการแก้ไข, และแม้กระทั่ง **modify revision date** ให้สอดคล้องกับกระบวนการทำงานของคุณ

## FAQ's

### Q1: ฉันสามารถใช้ Aspose.Note for Java กับไลบรารี Java อื่นได้หรือไม่?
A: ใช่, Aspose.Note for Java สามารถผสานรวมกับไลบรารี Java อื่นเพื่อเพิ่มฟังก์ชันการทำงาน

### Q2: Aspose.Note for Java รองรับเวอร์ชันทั้งหมดของเอกสาร OneNote หรือไม่?
A: Aspose.Note for Java รองรับหลายเวอร์ชันของเอกสาร OneNote รวมถึงเวอร์ชันเก่า

### Q3: Aspose.Note for Java เหมาะกับแอปพลิเคชันระดับองค์กรหรือไม่?
A: แน่นอน, Aspose.Note for Java ถูกออกแบบมาเพื่อรองรับความต้องการของแอปพลิเคชันระดับองค์กรด้วยคุณสมบัติที่แข็งแกร่งและความสามารถในการขยาย

### Q4: ฉันสามารถปรับแต่งการแก้ไขหน้าโดยใช้ Aspose.Note for Java ได้หรือไม่?
A: ใช่, คุณสามารถปรับแต่งการแก้ไขหน้าให้ตรงตามความต้องการของคุณโดยใช้ Aspose.Note for Java

### Q5: ฉันจะหาแหล่งสนับสนุนสำหรับ Aspose.Note for Java ได้จากที่ไหน?
A: คุณสามารถรับการสนับสนุนสำหรับ Aspose.Note for Java ได้จาก [Aspose.Note forum](https://forum.aspose.com/c/note/28).

---

**Last Updated:** 2026-01-15  
**Tested With:** Aspose.Note for Java 24.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}