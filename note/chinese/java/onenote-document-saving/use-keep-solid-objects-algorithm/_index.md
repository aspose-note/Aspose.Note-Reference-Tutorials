---
title: 在 OneNote 中使用保留实体对象算法 - Aspose.Note
linktitle: 在 OneNote 中使用保留实体对象算法 - Aspose.Note
second_title: Aspose.Note Java API
description: 了解如何在使用 Java 中的保留实体对象算法转换为 PDF 时保留 Aspose.Note 文档中的实体对象。
weight: 25
url: /zh/java/onenote-document-saving/use-keep-solid-objects-algorithm/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 在 OneNote 中使用保留实体对象算法 - Aspose.Note

## 介绍

在本教程中，我们将探讨如何在 Aspose.Note for Java 中使用保留实体对象算法。该算法对于在将文档转换为 PDF 格式时保持文档中实体对象的完整性非常重要。我们将逐步分解该过程，确保每个阶段的清晰度和理解性。

## 先决条件

在我们开始之前，请确保您具备以下条件：

1. 您的系统上安装了 Java 开发工具包 (JDK)。
2.  Java 库的 Aspose.Note。您可以从以下位置下载：[这里](https://releases.aspose.com/note/java/).

## 导入包

首先，让我们导入必要的包：

```java
import java.io.IOException;
import com.aspose.note.AlwaysSplitObjectsAlgorithm;
import com.aspose.note.Document;
import com.aspose.note.KeepPartAndCloneSolidObjectToNextPageAlgorithm;
import com.aspose.note.KeepSolidObjectsAlgorithm;
import com.aspose.note.PdfSaveOptions;
```

## 第 1 步：加载文档

使用以下代码片段将文档加载到 Aspose.Note 中：

```java
String dataDir = "Your Document Directory";
Document doc = new Document(dataDir + "Aspose.one");
```

## 步骤 2：配置 PDF 保存选项

定义 PdfSaveOptions 并将 PageSplittingAlgorithm 设置为 KeepSolidObjectsAlgorithm：

```java
PdfSaveOptions pdfSaveOptions = new PdfSaveOptions();
pdfSaveOptions.setPageSplittingAlgorithm(new KeepSolidObjectsAlgorithm());
```

## 步骤 3：调整高度限制（可选）

如有必要，您可以调整克隆零件的高度限制：

```java
float heightLimitOfClonedPart = 500;
pdfSaveOptions.setPageSplittingAlgorithm(new KeepSolidObjectsAlgorithm(heightLimitOfClonedPart));
```

## 步骤 4：保存文档

最后，使用指定的 PDF 保存选项保存文档：

```java
String outputDir = "Your Output Directory";
String outputFile = outputDir + "UsingKeepSolidObjectsAlgorithm_out.pdf";
doc.save(outputFile);
```

## 结论

在本教程中，我们学习了如何在 Aspose.Note for Java 中使用保留实体对象算法。该算法可确保在将文档转换为 PDF 格式时保留文档中的实体对象，从而保持文档的完整性。

## 常见问题解答

### Q1：克隆零件的高度限制可以调整吗？

 A1: 是的，您可以根据您的要求使用调整克隆零件的高度限制`heightLimitOfClonedPart`范围。

### Q2：在哪里可以找到更多文档？

 A2：您可以在Aspose.Note for Java上找到详细文档[这里](https://reference.aspose.com/note/java/).

### Q3：有免费试用吗？

 A3：是的，您可以免费试用 Aspose.Note for Java[这里](https://releases.aspose.com/).

### Q4：如果我遇到任何问题，如何获得支持？

 A4：您可以从Aspose社区获得支持[这里](https://forum.aspose.com/c/note/28).

### Q5：在哪里可以购买许可证？

 A5：您可以购买 Aspose.Note for Java 的许可证[这里](https://purchase.aspose.com/buy).

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
