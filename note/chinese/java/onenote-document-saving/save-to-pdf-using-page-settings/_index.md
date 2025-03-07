---
title: 使用 OneNote 中的页面设置保存为 PDF - Aspose.Note
linktitle: 使用 OneNote 中的页面设置保存为 PDF - Aspose.Note
second_title: Aspose.Note Java API
description: 了解如何使用 Aspose.Note 库将 OneNote 文档保存为 Java 中的 PDF。包含不同页面设置的代码示例的分步指南。
weight: 19
url: /zh/java/onenote-document-saving/save-to-pdf-using-page-settings/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 使用 OneNote 中的页面设置保存为 PDF - Aspose.Note

## 介绍

在本教程中，我们将学习如何使用 Aspose.Note for Java 使用不同的页面设置将 OneNote 文档保存为 PDF 格式。我们将介绍两种方法：使用 Letter 页面设置保存和使用无高度限制的 A4 页面设置保存。

## 先决条件

在我们开始之前，请确保您具备以下先决条件：

1. 您的系统上安装了 Java 开发工具包 (JDK)。
2. Aspose.Note for Java 库已下载并包含在您的 Java 项目中。
3. 对 Java 编程语言有基本的了解。

## 导入包

确保您已导入在项目中使用 Aspose.Note for Java 所需的包。这是导入声明：

```java
import com.aspose.note.*;
import java.io.IOException;
import java.nio.file.Paths;
```

## 使用 Letter 页面设置保存为 PDF

### 第 1 步：加载文档

首先，将 OneNote 文档加载到 Aspose.Note 中：

```java
Document oneFile = new Document("path/to/your/OneNote.one");
```

### 第 2 步：定义目标路径

指定 PDF 文件的目标路径：

```java
String dst = "path/to/your/SaveToPdfUsingLetterPageSettings.pdf";
```

### 第 3 步：保存文档

使用 Letter 页面设置保存文档：

```java
PdfSaveOptions options = new PdfSaveOptions();
options.setPageSettings(PageSettings.getLetter());
oneFile.save(dst, options);
```

## 使用 A4 页面设置保存为 PDF，无高度限制

### 第 1 步：加载文档

同样，将 OneNote 文档加载到 Aspose.Note 中：

```java
Document oneFile = new Document("path/to/your/OneNote.one");
```

### 第 2 步：定义目标路径

指定 PDF 文件的目标路径：

```java
String dst = "path/to/your/SaveToPdfUsingA4PageSettingsWithoutHeightLimit.pdf";
```

### 第 3 步：保存文档

以A4页面设置保存文档，无高度限制：

```java
PdfSaveOptions options = new PdfSaveOptions();
options.setPageSettings(PageSettings.getA4NoHeightLimit());
oneFile.save(dst, options);
```

执行这些步骤后，您将使用不同的页面设置成功将 OneNote 文档保存为 PDF。

## 结论

在本教程中，我们探索了如何使用 Aspose.Note for Java 库将 OneNote 文档保存为 PDF 格式。通过遵循分步指南，您可以轻松地将此功能集成到您的 Java 应用程序中。

## 常见问题解答

### Q1：我可以进一步自定义页面设置吗？

A1：是的，您可以使用 Aspose.Note for Java 根据您的要求自定义页面设置。

### Q2：Aspose.Note 是否支持除 PDF 之外的其他输出格式？

A2：是的，Aspose.Note 支持各种输出格式，包括图像和 HTML。

### Q3：Aspose.Note 是否兼容不同版本的 OneNote 文件？

A3：是的，Aspose.Note 支持不同版本的 OneNote 文件，包括 .one 和 .onetoc2。

### Q4：我可以一次将多个 OneNote 文件转换为 PDF 吗？

A4：是的，您可以使用 Aspose.Note for Java 批量处理多个 OneNote 文件。

### Q5：有没有可供测试的试用版？

A5：是的，您可以从网站上获得 Aspose.Note for Java 的免费试用版。
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
