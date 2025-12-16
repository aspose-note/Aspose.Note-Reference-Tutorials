---
date: 2025-12-09
description: 了解如何使用 Aspose.Note for Java 在 Java 中将 OneNote 保存为带格式的富文本 PDF。请遵循我们的分步指南，实现无缝的文档自动化。
linktitle: Save OneNote as PDF with Formatted Rich Text in Java
second_title: Aspose.Note Java API
title: 在 Java 中将 OneNote 保存为带格式的富文本 PDF
url: /zh/java/onenote-document-manipulation/create-onenote-document-formatted-rich-text/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 在 Java 中将 OneNote 保存为带格式的富文本 PDF

## 介绍

如果您需要 **将 OneNote 保存为 PDF** 并保留富文本格式，您来对地方了。在本教程中，我们将演示如何创建 OneNote 文档、应用自定义样式，并使用 Aspose.Note for Java 直接导出为 PDF。完成后，您将拥有一段可在任何 Java 项目中复用的代码片段，实现自动化的精美 OneNote‑转‑PDF 转换。

## 快速答案
- **本教程教什么？** 如何创建带样式文本的 OneNote 文档并将其保存为 PDF。  
- **需要哪个库？** Aspose.Note for Java（可从官方网站下载）。  
- **需要许可证吗？** 临时许可证可用于测试；生产环境需要正式许可证。  
- **可以使用哪种 IDE？** 任意 Java IDE——IntelliJ IDEA、Eclipse 或 NetBeans。  
- **可以更改输出格式吗？** 可以，Aspose.Note 支持 PDF、HTML、PNG 等多种格式。

## 什么是 “save onenote as pdf”？
将 OneNote 保存为 PDF 意味着将 OneNote 页面结构——包括文本、图像和格式——转换为静态 PDF 文件，任何平台都可查看，无需安装 OneNote。

## 为什么在 Java 中格式化富文本？
在 Java 中直接应用富文本格式（字体、颜色、样式），可以生成外观专业、符合品牌指南的文档，无需手动编辑。

## 前置条件

1. **Java Development Kit (JDK)** – 任意近期版本（8 或更高）。  
2. **Aspose.Note for Java JAR** – 从 [download link](https://releases.aspose.com/note/java/) 下载。  
3. **IDE** – IntelliJ IDEA、Eclipse 或您喜欢的任何编辑器。  

## 导入包

首先，需要将必要的包导入到您的 Java 项目中。将以下 import 语句添加到 Java 文件的开头：

```java
import java.awt.Color;
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.SaveFormat;
import com.aspose.note.TextStyle;
import com.aspose.note.ParagraphStyle;
import com.aspose.note.Title;
```

## 步骤 1：设置文档和页面

让我们从初始化 `Document` 和 `Page` 对象开始：

```java
String dataDir = "Your Document Directory";
Document doc = new Document();
Page page = new Page();
```

## 步骤 2：创建带格式的标题

现在，创建一个带格式的标题：

```java
Title title = new Title();
ParagraphStyle defaultTextStyle = new ParagraphStyle()
                                        .setFontColor(Color.black)
                                        .setFontName("Arial")
                                        .setFontSize(10);

RichText titleText = new RichText().append("Title!");
titleText.setParagraphStyle(defaultTextStyle);
title.setTitleText(titleText);
```

## 步骤 3：创建带格式的富文本

接下来，创建具有多种格式样式的富文本：

```java
Outline outline = new Outline();
OutlineElement outlineElem = new OutlineElement();

TextStyle textStyleForHelloWord = new TextStyle()
                                        .setFontColor(Color.red)
                                        .setFontName("Arial")
                                        .setFontSize(10);

TextStyle textStyleForOneNoteWord = new TextStyle()
                                        .setFontColor(Color.green)
                                        .setFontName("Calibri")
                                        .setFontSize(10)
                                        .setItalic(true);

TextStyle textStyleForTextWord = new TextStyle()
                                        .setFontColor(Color.blue)
                                        .setFontName("Arial")
                                        .setFontSize(15)
                                        .setBold(true)
                                        .setItalic(true);

RichText text = new RichText()
        .append("Hello", textStyleForHelloWord)
        .append(" OneNote", textStyleForOneNoteWord)
        .append(" text", textStyleForTextWord)
        .append("!", TextStyle.getDefault());
text.setParagraphStyle(defaultTextStyle);
```

## 步骤 4：将元素添加到页面和文档

现在，将标题和富文本添加到页面，并将元素加入大纲：

```java
outlineElem.appendChildLast(text);
outline.appendChildLast(outlineElem);
page.setTitle(title);
page.appendChildLast(outline);
doc.appendChildLast(page);
```

## 步骤 5：保存文档

最后，将创建的 OneNote 文档保存为 PDF：

```java
doc.save(dataDir + "CreateOneNoteDocument_out.pdf", SaveFormat.Pdf);
```

## 常见问题及解决方案

| 问题 | 解决方案 |
|-------|----------|
| **文件未找到** | 确认 `dataDir` 指向的文件夹存在且具有写入权限。 |
| **少字体** | 确保您引用的字体（例如 *Calibri*）已安装在主机机器上。 |
| **许可证未生效** | 在创建 `Document` 之前加载 Aspose 许可证，以避免出现评估水印。 |

## 常见问答

**问：我可以进一步自定义字体样式吗？**  
答：可以，您可以通过 `TextStyle` 和 `ParagraphStyle` 类调整下划线、删除线、文本对齐等额外属性。

**问：Aspose.Note for Java 是否兼容所有 Java IDE？**  
答：完全兼容。只要 IDE 支持标准的 Java 开发，您都可以将 Aspose.Note JAR 添加到项目的类路径中。

**问：我可以将此功能集成到 Web 应用程序中吗？**  
答：可以，同样的代码可在基于 Servlet 或 Spring Boot 的应用中使用，实现服务器端的动态 OneNote‑转‑PDF 生成。

**问：使用 Aspose.Note for Java 是否有许可证要求？**  
答：生产环境必须使用商业许可证。评估和测试阶段可使用临时许可证。

**问：Aspose.Note for Java 是否支持除 OneNote 之外的其他文档格式？**  
答：支持 PDF、HTML、PNG、JPEG 等多种导出格式，您可以灵活地将 OneNote 页面转换为所需的格式。

## 结论

本指南演示了如何使用 Aspose.Note for Java **将 OneNote 保存为 PDF** 并应用富文本格式。通过遵循逐步说明，您可以在任何基于 Java 的解决方案中自动化创建精美的 OneNote 文档并将其转换为 PDF。

---

**最后更新：** 2025-12-09  
**测试环境：** Aspose.Note for Java 24.11（撰写时的最新版本）  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}