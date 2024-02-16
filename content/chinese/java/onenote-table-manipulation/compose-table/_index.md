---
title: 在 OneNote 中撰写表格 - Aspose.Note
linktitle: 在 OneNote 中撰写表格 - Aspose.Note
second_title: Aspose.Note Java API
description: 了解如何使用 Aspose.Note for Java 以编程方式在 OneNote 中撰写表格。高效文档创建的分步指南。
type: docs
weight: 11
url: /zh/java/onenote-table-manipulation/compose-table/
---
## 介绍
在当今竞争激烈的商业环境中，有效的沟通和协作是取得成功的关键因素。 Aspose.Note for Java 提供了一个强大的解决方案，用于以编程方式创建和操作 OneNote 文档。在本教程中，我们将探讨如何使用 Aspose.Note for Java 在 OneNote 中编写表格。请按照下面的分步指南来增强您的文档创建过程。
## 先决条件
在深入学习本教程之前，请确保您满足以下先决条件：
- Java 编程的基础知识。
- 安装了 Java 库的 Aspose.Note。您可以从以下位置下载：[这里](https://releases.aspose.com/note/java/).
- 为 Java 开发而设置的集成开发环境 (IDE)。
## 导入包
确保导入必要的包来启动您的项目。将以下导入语句添加到您的 Java 类中：
```java
import com.aspose.note.*;
import java.awt.*;
import java.io.IOException;
import java.nio.file.Paths;
import java.util.stream.StreamSupport;
```
## 第1步：设置文档目录
```java
String dataDir = "Your Document Directory";
```
确保将“您的文档目录”替换为您要保存 OneNote 文档的实际路径。
## 第 2 步：撰写标题
```java
RichText headerText = new RichText().append("Super contest for suppliers.");
headerText.setParagraphStyle(new ParagraphStyle().setFontSize(18).setBold(true));
headerText.setAlignment(HorizontalAlignment.Center);
```
为您的文档创建引人注目的标题。根据需要调整字体大小、粗细和对齐方式。
## 第 3 步：创建页面和大纲
```java
Page page = new Page();
Outline outline = page.appendChildLast(new Outline());
outline.setHorizontalOffset(50);
outline.appendChildLast(new OutlineElement()).appendChildLast(headerText);
```
设置新页面和大纲，然后将之前创建的标题添加到大纲中。
## 第 4 步：添加摘要文本
```java
RichText bodyTextHeader = outline.appendChildLast(new OutlineElement()).appendChildLast(new RichText());
bodyTextHeader.setParagraphStyle(ParagraphStyle.getDefault());
bodyTextHeader.append("This is the final ranking of proposals got from our suppliers.");
```
包括简短的摘要文本以提供表格的上下文。
## 第5步：撰写表格
```java
Table ranking = outline.appendChildLast(new OutlineElement()).appendChildLast(new Table());
//其余步骤涉及设置表结构、标题行和添加空行。
//具体实现请参考提供的代码。
```
构建表结构并填充相关信息。提供的代码包括为“联系人”列添加列、标题行、空行和模板内容。
## 第 6 步：保存文档
```java
Document d = new Document();
d.appendChildLast(page);
d.save(Paths.get(dataDir, "ComposeTable_out.one").toString());
```
使用指定的文件名和目录路径保存撰写的文档。
## 结论
恭喜！您已使用 Aspose.Note for Java 在 OneNote 中成功编写了一个表格。本教程演示了分步过程，使您能够以编程方式增强文档创建功能。
## 经常问的问题
### 问：在哪里可以找到 Aspose.Note for Java 文档？
你可以参考文档[这里](https://reference.aspose.com/note/java/).
### 问：如何下载 Aspose.Note for Java？
您可以从以下位置下载：[这个链接](https://releases.aspose.com/note/java/).
### 问：有免费试用吗？
是的，您可以免费试用[这里](https://releases.aspose.com/).
### 问：在哪里可以获得 Aspose.Note for Java 的支持？
访问支持论坛[这里](https://forum.aspose.com/c/note/28).
### 问：我可以获得临时许可证吗？
是的，您可以获得临时许可证[这里](https://purchase.aspose.com/temporary-license/).