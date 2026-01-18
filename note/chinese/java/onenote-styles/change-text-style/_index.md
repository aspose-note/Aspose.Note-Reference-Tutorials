---
date: 2026-01-18
description: 学习如何使用 Aspose.Note 在 OneNote 中设置字体颜色、突出显示文本、修改字体大小，并将 OneNote 保存为 PDF。一步一步的代码指南。
linktitle: Change Text Style in OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: 在 OneNote 中使用 Java 设置字体颜色 – Aspose.Note
url: /zh/java/onenote-styles/change-text-style/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 在 OneNote 中使用 Java 设置字体颜色 – Aspose.Note

## 介绍

在本教程中，您将学习如何使用 Aspose.Note for Java API 为 OneNote 文档中的文本 **设置字体颜色 Java**。我们将演示如何加载 `.one` 文件、访问其 RichText 节点、应用颜色、突出显示以及字体大小的更改，最后 **将 OneNote 保存为 PDF**。无论您是需要 **在 OneNote 中突出显示文本**、**修改 OneNote 中的字体大小**，还是仅仅想更改整体文本样式，下面的步骤都提供了完整、可投入生产的解决方案。

## 快速答疑
- **可以更改特定单词的字体颜色吗？** 可以——遍历 `TextRun` 对象并调用 `setFontColor`。
- **Aspose.Note 能把 OneNote 保存为 PDF 吗？** 当然可以；使用 `document.save("output.pdf")`。
- **需要哪个 Java 版本？** Java 8 或更高。
- **支持突出显示吗？** 在 `TextStyle` 上使用 `setHighlight(Color)`。
- **可以一行代码将 OneNote 转换为 PDF 吗？** 不能直接，但 `save` 方法会完成转换。

## 什么是 “set font color java”？

该短语指的是使用 Java 代码在 OneNote 文件中以编程方式为文本元素分配新的字体颜色。借助 Aspose.Note，您可以在不打开 OneNote UI 的情况下完全控制字体颜色、突出显示和大小等样式属性。

## 为什么要更改 OneNote 文本样式？

- **提升可读性** – 彩色或高亮的文本能够突出关键要点。  
- **保持品牌一致性** – 在会议记录中统一使用公司配色。  
- **导出质量** – 当您 **将 OneNote 转换为 PDF** 进行共享时，带样式的笔记看起来更专业。

## 前置条件

在开始之前，请确保您具备以下条件：

1. 基本的 Java 编程知识。  
2. 已安装 JDK 8 或更高版本。  
3. 项目中已添加 Aspose.Note for Java 库（Maven/Gradle 或手动 JAR）。  
4. 一个用于实验的示例 OneNote 文件（`Sample1.one`）。  

## 导入包

首先，导入我们将要使用的类：

```java
import java.awt.Color;
import java.io.IOException;
import java.util.List;
import com.aspose.note.Document;
import com.aspose.note.RichText;
import com.aspose.note.TextRun;
import com.aspose.note.TextStyle;
```

## 步骤指南

### 步骤 1：加载文档

```java
// Load the document into Aspose.Note
Document document = new Document("Your Document Directory/Sample1.one");
```

我们加载 OneNote 文件（`Sample1.one`），以便 Aspose.Note 能够处理其内部结构。

### 步骤 2：访问 RichText 节点

```java
// Get a particular RichText node
List<RichText> richTextNodes = document.getChildNodes(RichText.class);
RichText richText = richTextNodes.get(0);
```

`RichText` 对象包含实际的段落。通过获取第一个节点，我们获得了要设置样式的文本句柄。

### 步骤 3：更改文本样式（set font color java）

```java
for (TextRun run : richText.getTextRuns()) {
    // Set font color
    run.getStyle().setFontColor(Color.yellow);
    // Set highlight color
    run.getStyle().setHighlight(Color.blue);
    // Set font size
    run.getStyle().setFontSize(20);
}
```

在循环中，我们 **将字体颜色 Java** 设置为黄色，应用蓝色突出显示（演示 **在 OneNote 中突出显示文本**），并将大小提升至 20 磅，展示 **在 OneNote 中修改字体大小**。

### 步骤 4：保存文档（save onenote as pdf）

```java
document.save("Your Document Directory/ChangeTextStyle_out.pdf");
System.out.printf("File saved: %s\n", "Your Document Directory/ChangeTextStyle_out.pdf");
```

使用 `.pdf` 扩展名调用 `save` 方法会自动 **将 OneNote 转换为 PDF**，生成可直接共享的文件。

## 常见问题与解决方案

| 问题 | 原因 | 解决办法 |
|------|------|----------|
| 颜色更改未生效 | 文档在保存前已在 OneNote 中打开 | 关闭 OneNote，或在 Java 进程结束后重新加载文件 |
| 突出显示未应用 | 使用的颜色与背景相同 | 选择对比度更高的 `Color`（例如 `Color.yellow`） |
| `document.save` 抛出 `IOException` | 输出路径无效 | 确认目录存在且具备写入权限 |

## 常见问答

**问：我可以仅对 OneNote 文件的某些章节应用这些样式更改吗？**  
答：可以——在遍历 `TextRun` 之前，根据其父级 `Section` 或 `Page` 对 `RichText` 节点进行过滤。

**问：除了颜色、突出显示和大小，Aspose.Note 还能处理哪些其他格式？**  
答：您可以更改字体族、粗体/斜体/下划线、对齐方式，甚至段落间距。

**问：是否可以批量处理多个 OneNote 文件？**  
答：完全可以。将加载和样式设置逻辑放入循环中，遍历文件夹中的每个 `.one` 文件。

**问：库是否支持直接保存为其他格式，如 DOCX？**  
答：支持——Aspose.Note 可导出为 PDF、DOCX、HTML 以及多种图像格式。

**问：在哪里可以找到更多示例和 API 参考？**  
答：访问官方 Aspose.Note 文档站点，查阅 API 参考，并下载免费试用版进行动手测试。

## 结论

现在，您已经掌握了使用 Aspose.Note **设置字体颜色 Java**、突出显示文本、调整字体大小，并 **将 OneNote 保存为 PDF** 的完整端到端示例。欢迎根据实际需求对代码进行改造，以针对特定页面、应用条件样式，或将其集成到更大的文档处理流水线中。

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**最后更新：** 2026-01-18  
**测试环境：** Aspose.Note 24.11 for Java  
**作者：** Aspose  

---