---
description: 了解如何使用 Aspose.Note for Java 将 OneNote 保存为 PDF 并在 OneNote 中添加子页面。请按照本分步指南高效组织您的笔记。
linktitle: How to Save OneNote PDF and Add Sub Pages
second_title: Aspose.Note Java API
title: 如何保存 OneNote PDF 并添加子页面
url: /zh/java/onenote-page-manipulation/create-document-with-root-and-sub-pages/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何保存 OneNote PDF 并添加子页面

## Introduction

在本教程中，您将了解 **如何使用 Aspose.Note for Java 将 OneNote 保存为 PDF**，同时创建包含根页面和子页面的文档。通过清晰的层次结构组织 OneNote 笔记本，可实现轻松导航，而导出为 PDF 则确保您可以以通用可读的格式共享笔记。我们还将展示如何以 onenote 风格添加子页面，从而轻松构建多层结构。

## Quick Answers
- **主要关键词是什么意思？** 它指的是使用 Aspose.Note 将 OneNote 笔记本导出为 PDF。  
- **使用的是哪个 API？** Aspose.Note for Java。  
- **我可以创建层级页面吗？** 可以——通过设置页面级别来构建根页面和子页面。  
- **需要许可证吗？** 提供免费试用；生产环境需要商业许可证。  
- **支持哪些输出格式？** BMP、PDF、PNG 等。

## What is “how to save OneNote PDF”?
将 OneNote 保存为 PDF 是将笔记本的页面转换为固定布局的文档，保留格式、图像和层次结构。这对于共享、归档或打印笔记非常理想。

## Why add sub pages onenote?
添加子页面可以将相关内容归类到父页面下，类似文件夹结构。它提升了笔记的组织性，加快搜索速度，并在笔记本导出为 PDF 时提升阅读体验。

## Prerequisites

在开始之前，请确保具备以下前提条件：

1. Java Development Kit (JDK)：确保系统已安装 JDK。  
2. Aspose.Note for Java：从[website](https://purchase.aspose.com/buy)下载并安装 Aspose.Note for Java。  
3. Integrated Development Environment (IDE)：选择如 IntelliJ IDEA、Eclipse 或 NetBeans 等 Java IDE。

## Import Packages

在 Java 项目中导入必要的包：

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

## Step 1: Set Up Document Directory

定义保存 OneNote 文档的目录：

```java
String dataDir = "Your Document Directory";
```

## Step 2: Create Document Object

实例化 `Document` 对象：

```java
Document doc = new Document();
```

## Step 3: Create Pages

初始化页面对象并设置其层级。设置层级决定页面是根页面还是子页面：

```java
Page page1 = new Page();
page1.setLevel((byte) 1);

Page page2 = new Page();
page2.setLevel((byte) 2);

Page page3 = new Page();
page3.setLevel((byte) 1);
```

## Step 4: Add Nodes to Pages

### Adding Nodes to First Page

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

### Adding Nodes to Second Page

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

### Adding Nodes to Third Page

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

## Step 5: Add Pages to the Document

```java
doc.appendChildLast(page1);
doc.appendChildLast(page2);
doc.appendChildLast(page3);
```

## Step 6: Save the Document

将 OneNote 文档保存为 PDF（本例中为 BMP）。更改 `SaveFormat` 即可导出为 PDF，满足 “如何保存 OneNote PDF” 的需求：

```java
try {
    doc.save(dataDir + "GenerateRootAndSubLevelPagesInOneNote_out.bmp", SaveFormat.Bmp);
} catch (IOException e) {
    // Handle exception
}
```

> **技巧提示：** 若要直接导出为 PDF，请将 `SaveFormat.Bmp` 替换为 `SaveFormat.Pdf`。

恭喜！您已成功创建包含根页面和子页面的 OneNote 文档，并学习了使用 Aspose.Note for Java **如何保存 OneNote PDF**。

## Why This Matters

- **层级组织：** 根页面和子页面让您在 OneNote 中模拟文件夹结构。  
- **无缝 PDF 导出：** 组织好后，导出为 PDF 能保留层级，使最终文档易于阅读和共享。  
- **自动化：** 代码可集成到更大的 Java 应用中，实现批量创建结构化笔记本。

## Common Pitfalls & How to Avoid Them

| Issue | Cause | Solution |
|-------|-------|----------|
| 页面显示在同一级别 | `setLevel` 值不正确 | 根页面使用 `setLevel((byte) 1)`，子页面使用 `setLevel((byte) 2)`（或更高） |
| PDF 输出为空白 | 缺少 `SaveFormat.Pdf` 或文件路径不正确 | 确认目录存在并使用 `SaveFormat.Pdf` |
| 字体未应用 | 字体名称错误或系统缺少该字体 | 确保在运行代码的机器上已安装该字体（例如 “David Transparent”） |

## Frequently Asked Questions

**问：我可以使用 Aspose.Note for Java 创建多层子页面吗？**  
答：可以，通过设置更高的层级数字来创建更深的层次结构（例如，`setLevel((byte) 3)` 表示第三级子页面）。

**问：Aspose.Note for Java 是否兼容不同的 Java IDE？**  
答：完全兼容。它可在 IntelliJ IDEA、Eclipse、NetBeans 以及任何支持 Java 开发的 IDE 中使用。

**问：我可以自定义 OneNote 文档中文本的格式吗？**  
答：可以。使用 `ParagraphStyle` 为每个 `RichText` 元素设置字体名称、大小、颜色等属性。

**问：Aspose.Note for Java 是否支持除 BMP 之外的其他保存格式？**  
答：支持。包括 PDF、PNG、JPEG、DOCX 等。相应地更改 `SaveFormat` 枚举即可。

**问：是否提供 Aspose.Note for Java 的试用版？**  
答：提供，可从 Aspose 官方网站下载免费试用版。

## Conclusion

通过清晰的层级结构组织 OneNote 笔记本并将其导出为 PDF，可使笔记更易访问和共享。按照上述步骤，您现在已经掌握了使用 Aspose.Note for Java **如何保存 OneNote PDF** 以及以 **onenote 风格添加子页面** 的编程方法。

---

**最后更新：** 2026-01-07  
**测试环境：** Aspose.Note for Java 24.11（最新）  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}