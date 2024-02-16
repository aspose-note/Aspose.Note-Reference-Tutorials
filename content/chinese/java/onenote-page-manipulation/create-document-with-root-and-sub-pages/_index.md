---
title: 在 OneNote 中创建包含根页面和子页面的文档
linktitle: 在 OneNote 中创建包含根页面和子页面的文档
second_title: Aspose.Note Java API
description: 使用 Aspose.Note for Java 在 OneNote 中创建包含根页面和子页面的文档。按照分步指南有效地组织您的笔记。
type: docs
weight: 11
url: /zh/java/onenote-page-manipulation/create-document-with-root-and-sub-pages/
---
## 介绍

在本教程中，我们将指导您完成使用 Aspose.Note for Java 在 OneNote 中创建包含根页面和子页面的文档的过程。通过执行这些步骤，您将能够以层次结构有效地组织 OneNote 文档。

## 先决条件

在开始之前，请确保您具备以下先决条件：

1. Java 开发工具包 (JDK)：确保您的系统上安装了 JDK。
2. Aspose.Note for Java：从以下位置下载并安装 Aspose.Note for Java：[网站](https://purchase.aspose.com/buy).
3. 集成开发环境 (IDE)：选择 Java IDE，例如 IntelliJ IDEA、Eclipse 或 NetBeans。

## 导入包

首先在 Java 项目中导入必要的包：

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.SaveFormat;
import com.aspose.note.ParagraphStyle;
```

## 第 1 步：设置文档目录

定义要保存 OneNote 文档的目录：

```java
String dataDir = "Your Document Directory";
```

## 第2步：创建文档对象

实例化一个`Document`目的：

```java
Document doc = new Document();
```

## 第 3 步：创建页面

初始化页面对象并设置其级别：

```java
Page page1 = new Page();
page1.setLevel((byte) 1);

Page page2 = new Page();
page2.setLevel((byte) 2);

Page page3 = new Page();
page3.setLevel((byte) 1);
```

## 第四步：向页面添加节点

### 将节点添加到首页

```java
Outline outline = new Outline();
OutlineElement outlineElem = new OutlineElement();
ParagraphStyle textStyle = new ParagraphStyle()
                                    .setFontColor(Color.black)
                                    .setFontName("David Transparent")
                                    .setFontSize(10);

RichText text = new RichText().append("First page.");
text.setParagraphStyle(textStyle);

outlineElem.appendChildLast(text);
outline.appendChildLast(outlineElem);
page1.appendChildLast(outline);
```

### 将节点添加到第二页

```java
Outline outline2 = new Outline();
OutlineElement outlineElem2 = new OutlineElement();
ParagraphStyle textStyle2 = new ParagraphStyle()
                                    .setFontColor(Color.black)
                                    .setFontName("David Transparent")
                                    .setFontSize(10);

RichText text2 = new RichText().append("Second page.");
text2.setParagraphStyle(textStyle2);

outlineElem2.appendChildLast(text2);
outline2.appendChildLast(outlineElem2);
page2.appendChildLast(outline2);
```

### 将节点添加到第三页

```java
Outline outline3 = new Outline();
OutlineElement outlineElem3 = new OutlineElement();
ParagraphStyle textStyle3 = new ParagraphStyle()
                                    .setFontColor(Color.black)
                                    .setFontName("Broadway")
                                    .setFontSize(10);

RichText text3 = new RichText().append("Third page.");
text3.setParagraphStyle(textStyle3);

outlineElem3.appendChildLast(text3);
outline3.appendChildLast(outlineElem3);
page3.appendChildLast(outline3);
```

## 步骤 5：将页面添加到文档

```java
doc.appendChildLast(page1);
doc.appendChildLast(page2);
doc.appendChildLast(page3);
```

## 第 6 步：保存文档

保存 OneNote 文档：

```java
try {
    doc.save(dataDir + "GenerateRootAndSubLevelPagesInOneNote_out.bmp", SaveFormat.Bmp);
} catch (IOException e) {
    //处理异常
}
```

恭喜！您已使用 Aspose.Note for Java 在 OneNote 中成功创建了包含根页面和子页面的文档。

## 结论

使用层次结构组织 OneNote 文档对于更好的管理和导航至关重要。使用 Aspose.Note for Java，您可以高效地创建具有根页面和子页面的文档，为您的笔记提供清晰且有组织的布局。

## 常见问题解答

### Q1：我可以使用Aspose.Note for Java 创建多个级别的子页面吗？

A1：是的，您可以通过为每个页面设置适当的级别来创建多个级别的子页面。

### Q2：Aspose.Note for Java 是否兼容不同的 Java IDE？

A2：是的，Aspose.Note for Java 与流行的 Java IDE 兼容，例如 IntelliJ IDEA、Eclipse 和 NetBeans。

### Q3：我可以自定义 OneNote 文档中的文本格式吗？

A3：是的，您可以使用 Aspose.Note for Java 的富文本功能自定义字体、颜色、大小和其他格式选项。

### Q4：Aspose.Note for Java支持保存不同格式的文档吗？

A4：是的，Aspose.Note for Java 支持以各种格式保存文档，包括 BMP、PDF、PNG 等。

### Q5：Aspose.Note for Java 有试用版吗？

A5：是的，您可以从网站下载 Aspose.Note for Java 的免费试用版。