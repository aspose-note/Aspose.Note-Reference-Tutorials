---
title: 在 OneNote 中创建编号列表 - Aspose.Note
linktitle: 在 OneNote 中创建编号列表 - Aspose.Note
second_title: Aspose.Note Java API
description: 了解如何使用 Aspose.Note for Java 在 OneNote 中轻松创建编号列表。下载免费试用版并深入了解 Java 开发的世界！
weight: 14
url: /zh/java/onenote-text-manipulation/create-numbered-list/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 在 OneNote 中创建编号列表 - Aspose.Note

## 介绍
Aspose.Note for Java 使 Java 开发人员能够无缝地使用 Microsoft OneNote 文件。在本教程中，我们将引导您完成使用强大的 Aspose.Note for Java 库在 OneNote 中制作编号列表的过程。
## 先决条件
在深入学习本教程之前，请确保满足以下先决条件：
- 在您的计算机上安装了 Java 开发工具包 (JDK)。
-  Aspose.Note for Java 库下载自[这里](https://releases.aspose.com/note/java/).
## 导入包
首先，让我们在 Java 项目中导入必要的包，以充分利用 Aspose.Note 功能。在您的项目中包含以下代码：
```java
import java.awt.Color;
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.NumberFormat;
import com.aspose.note.NumberList;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.ParagraphStyle;
```
## 第 1 步：初始化文档、页面和大纲对象
```java
//您的文档目录
String dataDir = "Your Document Directory";
//创建文档、页面和大纲对象
Document doc = new Document();
Page page = new Page();
Outline outline = new Outline();
//设置默认文本样式
ParagraphStyle defaultStyle = new ParagraphStyle()
                                        .setFontColor(Color.black)
                                        .setFontName("Arial")
                                        .setFontSize(10);
Document doc = new Document();
Page page = new Page();
Outline outline = new Outline();
```
## 第2步：设置默认文本样式
```java
ParagraphStyle defaultStyle = new ParagraphStyle()
                                        .setFontColor(Color.black)
                                        .setFontName("Arial")
                                        .setFontSize(10);
```
## 第 3 步：创建轮廓元素
现在，让我们为编号列表创建元素。
```java
OutlineElement outlineElem1 = new OutlineElement();
outlineElem1.setNumberList(new NumberList("{0})", NumberFormat.DecimalNumbers, "Arial", 10));
RichText text1 = new RichText().append("First");
text1.setParagraphStyle(defaultStyle);
outlineElem1.appendChildLast(text1);
//对其他元素重复此操作（outlineElem2 和outlineElem3）
```
## 步骤 4：将大纲元素添加到大纲中
```java
outline.appendChildLast(outlineElem1);
outline.appendChildLast(outlineElem2);
outline.appendChildLast(outlineElem3);
```
## 第5步：向页面添加轮廓
```java
page.appendChildLast(outline);
```
## 第 6 步：保存文档
```java
doc.appendChildLast(page);
doc.save(dataDir + "CreateNumberedList_out.pdf");
System.out.printf("File saved: %s\n", dataDir + "CreateNumberedList_out.pdf");
```
严格按照这些步骤操作，您将可以使用 Aspose.Note for Java 轻松地在 OneNote 中创建编号列表。
## 结论
在本教程中，我们探索了使用 Aspose.Note for Java 在 OneNote 中创建编号列表的无缝过程。该库的强大功能使其成为使用 Microsoft OneNote 文件的 Java 开发人员的宝贵工具。
## 经常问的问题
### 问：我可以自定义 OneNote 列表中的编号格式吗？
答：当然！您可以使用 Aspose.Note for Java 提供的 NumberList 类自定义编号格式。
### 问：Aspose.Note for Java 有试用版吗？
答：是的，您可以下载免费试用版[这里](https://releases.aspose.com/).
### 问：如何获得 Aspose.Note for Java 支持？
答：访问[Aspose.Note for Java 论坛](https://forum.aspose.com/c/note/28)以获得社区支持。
### 问：在哪里可以找到 Aspose.Note for Java 的详细文档？
答：请参阅[文档](https://reference.aspose.com/note/java/)以获得全面的信息。
### 问：如何购买 Aspose.Note for Java 的许可证？
答：您可以购买许可证[这里](https://purchase.aspose.com/buy).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
