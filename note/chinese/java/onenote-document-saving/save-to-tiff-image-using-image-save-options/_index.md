---
date: 2026-11-05
description: 了解如何在 Java 中使用 Aspose.Note 将 OneNote 笔记本转换为 TIFF 时减小 TIFF 文件大小。包括 JPEG、PackBits
  和 black‑white TIFF 选项。
keywords:
- reduce tiff file size
- black white tiff
- tiff jpeg compression
- aspose note java
lastmod: 2026-11-05
linktitle: 如何在 Java 中将 OneNote 转换为 TIFF 时减小 TIFF 文件大小
og_description: 了解如何在 Java 中使用 Aspose.Note 将 OneNote 笔记本转换为 TIFF 时减小 TIFF 文件大小。包括
  JPEG、PackBits 和 black‑white TIFF 选项。
og_image_alt: Developer guide showing OneNote to TIFF conversion with compression
  options in Java
og_title: 如何在 Java 中将 OneNote 转换为 TIFF 时减小 TIFF 文件大小
schemas:
- author: Aspose
  dateModified: '2026-11-05'
  description: Learn how to reduce TIFF file size when converting OneNote notebooks
    to TIFF in Java using Aspose.Note. Includes JPEG, PackBits and black‑white TIFF
    options.
  headline: How to reduce TIFF file size when converting OneNote in Java
  type: TechArticle
- description: Learn how to reduce TIFF file size when converting OneNote notebooks
    to TIFF in Java using Aspose.Note. Includes JPEG, PackBits and black‑white TIFF
    options.
  name: How to reduce TIFF file size when converting OneNote in Java
  steps:
  - name: Point `dataDir` to the folder containing your `.one` file.
    text: Point `dataDir` to the folder containing your `.one` file.
  - name: Call `SaveToTiffUsingJpegCompression()` from your main method or service.
    text: Call `SaveToTiffUsingJpegCompression()` from your main method or service.
  - name: The resulting `.tiff` file will appear in the same directory.
    text: The resulting `.tiff` file will appear in the same directory.
  type: HowTo
- questions:
  - answer: Yes. While Aspose.Note focuses on OneNote files, Aspose.PDF, Aspose.Words,
      and other libraries provide similar `ImageSaveOptions` for their formats.
    question: Can I convert other document types (e.g., PDF, DOCX) to TIFF with these
      options?
  - answer: The JPEG algorithm is the same, but the image data lives inside a TIFF
      container, which can hold multiple pages and richer metadata.
    question: How does TIFF JPEG compression differ from a standard JPEG file?
  - answer: Absolutely. Iterate over a directory, call any of the three methods for
      each file, and collect the resulting TIFFs.
    question: Is it possible to batch‑process many `.one` files?
  - answer: Yes. Use `options.setResolution(int dpi)` before saving.
    question: Can I control the DPI/resolution of the output TIFF?
  - answer: The API itself is synchronous, but you can wrap calls in Java’s `CompletableFuture`
      or a thread pool for parallel execution.
    question: Does Aspose.Note support asynchronous processing?
  type: FAQPage
second_title: Aspose.Note Java API
tags:
- reduce tiff file size
- aspose.note
- java tiff conversion
- black white tiff
- image compression
title: 如何在 Java 中将 OneNote 转换为 TIFF 时减小 TIFF 文件大小
url: /zh/java/onenote-document-saving/save-to-tiff-image-using-image-save-options/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何在 Java 中将 OneNote 转换为 TIFF 时减小 TIFF 文件大小

## 介绍

在本教程中，您将了解如何在使用 Aspose.Note for Java 将 OneNote 笔记本转换为 TIFF 图像时**减小 TIFF 文件大小**。我们将介绍三种压缩方法——TIFF JPEG、PackBits 和 CCITT Group 3（黑白 TIFF）——并展示如何调整图像质量、控制颜色模式，以使文件大小在 Web、归档或传真类场景中保持最佳。

## 快速答案
- **TIFF JPEG 压缩是什么？** 一种有损压缩方法，可在保持视觉质量的同时减小 TIFF 文件大小。  
- **哪个库负责转换？** Aspose.Note for Java。  
- **我需要许可证吗？** 免费试用可用于测试；生产环境需要许可证。  
- **我可以更改图像质量吗？** 可以，在 `ImageSaveOptions` 上设置 `quality` 属性。  
- **是否支持批量转换？** 当然——遍历文档并应用相同的选项即可。

## TIFF JPEG 压缩概述

TIFF JPEG 压缩将图像数据存储在 TIFF 容器中，但使用 JPEG 的有损算法来缩小文件。它在需要在 **tiff 图像质量** 与更小文件大小之间取得平衡时非常适用，尤其适用于 Web 或归档场景。

## 为什么使用不同的 TIFF 压缩类型？

您可以根据内容和存储需求选择压缩类型：JPEG 最适合照片，PackBits 为具有大面积均匀区域的图形提供无损压缩，CCITT Group 3 为单色传真式文档提供高比率压缩。选择合适的方法可让您**减小 TIFF 文件大小**，而不会影响应用所需的视觉保真度。

## 选择合适的压缩方式

- **JPEG** – 可调节质量（0‑100），可在大小与细节之间权衡，适用于彩色丰富的页面。  
- **PackBits** – 无损的行程长度编码；在必须保持每个像素精确时理想。  
- **CCITT Group 3** – 仅限单色；为扫描文本或传真文档提供最大压缩。

## 使用 Aspose.Note 将 OneNote 转换为 TIFF

如果您的目标是**将 OneNote 转换为 TIFF**，下面的三种方法涵盖了最常见的场景。每种方法都会加载 `.one` 文件，配置 `ImageSaveOptions`，并将结果保存为 `.tiff` 文件。

## 先决条件

- 已安装 Java Development Kit（JDK）。  
- 已在项目中添加 Aspose.Note for Java 库（Maven/Gradle 或手动 JAR）。  
- 具备基本的 Java 语法知识。

## 导入包

`ImageSaveOptions`、`TiffCompression` 和 `ColorMode` 类是转换 API 的核心。

`ImageSaveOptions` 定义了保存图像的选项，例如格式和压缩方式。  
`TiffCompression` 列举了支持的 TIFF 压缩算法。  
`ColorMode` 指定颜色深度，例如彩色或黑白。

```java
// Placeholder for import statements – keep your imports here
```

```java
import com.aspose.note.*;
import java.io.IOException;
import java.nio.file.Paths;
```

## 步骤 1：使用 TIFF JPEG 压缩保存为 TIFF

### 在 Java 中使用 JPEG 压缩保存 TIFF

加载 OneNote 文件，使用 JPEG 压缩配置 `ImageSaveOptions`，可选地设置 `quality` 值，然后调用保存方法。这种两步模式让您完全控制输出大小和视觉保真度。

1. 将 `dataDir` 指向包含 `.one` 文件的文件夹。  
2. 在主方法或服务中调用 `SaveToTiffUsingJpegCompression()`。  
3. 生成的 `.tiff` 文件将出现在同一目录中。

```java
// Placeholder for the JPEG compression method implementation
```

```java
public static void SaveToTiffUsingJpegCompression() throws IOException {
    // The path to the documents directory.
    String dataDir = "Your Document Directory";

    // Load the document into Aspose.Note.
    Document oneFile = new Document(Paths.get(dataDir, "Aspose.one").toString());

    ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);
    options.setTiffCompression(TiffCompression.Jpeg);
    options.setQuality(93);

    oneFile.save(Paths.get(dataDir,"SaveToTiffUsingJpegCompression.tiff").toString(), options);
}
```

**说明**

- `ImageSaveOptions` 告诉 Aspose.Note 输出 TIFF 文件。  
- `setTiffCompression(TiffCompression.Jpeg)` 选择 JPEG 压缩。  
- `setQuality(93)`（可选）微调图像质量；较低的值会生成更小的文件。

## TIFF PackBits 压缩概述

PackBits 是一种无损压缩算法，最适用于具有大面积纯色区域的图像。文档中常将其称为 **tiff packbits compression**。

## 在 Java 中使用 PackBits 压缩保存 TIFF

如果需要无损选项，PackBits 是一种简单的行程长度算法，适用于具有纯色的图形。使用 `TiffCompression.PackBits` 配置 `ImageSaveOptions` 并保存文档。

```java
// Placeholder for the PackBits compression method implementation
```

```java
public static void SaveToTiffUsingPackBitsCompression() throws IOException {
    // The path to the documents directory.
    String dataDir = "Your Document Directory";

    // Load the document into Aspose.Note.
    Document oneFile = new Document(Paths.get(dataDir, "Aspose.one").toString());

    ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);
    options.setTiffCompression(TiffCompression.PackBits);

    oneFile.save(Paths.get(dataDir, "SaveToTiffUsingPackBitsCompression.tiff").toString(), options);
}
```

**说明**

- `setTiffCompression(TiffCompression.PackBits)` 切换压缩方式。  
- 不需要质量设置，因为 PackBits 是无损的。

## 在 Java 中使用 CCITT Group 3 压缩保存 TIFF

对于传真式文档，您通常需要 **黑白 TIFF**。CCITT Group 3 为单色图像提供高压缩率。将颜色模式设置为黑白，并选择 CCITT 3 压缩枚举。

```java
// Placeholder for the CCITT Group 3 compression method implementation
```

```java
public static void SaveToTiffUsingCcitt3Compression() throws IOException {
    // The path to the documents directory.
    String dataDir = "Your Document Directory";

    // Load the document into Aspose.Note.
    Document oneFile = new Document(Paths.get(dataDir, "Aspose.one").toString());

    ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);
    options.setColorMode(ColorMode.BlackAndWhite);
    options.setTiffCompression(TiffCompression.Ccitt3);

    oneFile.save(Paths.get(dataDir, "SaveToTiffUsingCcitt3Compression.tiff").toString(), options);
}
```

**说明**

- `setColorMode(ColorMode.BlackAndWhite)` 强制输出为单色。  
- `setTiffCompression(TiffCompression.Ccitt3)` 应用针对传真优化的压缩。

## 常见问题与技巧

| 问题 | 解决方案 |
|-------|----------|
| **输出文件大于预期** | 尝试降低 JPEG `quality` 值，或在可接受无损的情况下切换到 PackBits。 |
| **颜色显得苍白** | 确保在需要全彩时未意外设置 `ColorMode.BlackAndWhite`。 |
| **不支持的图像格式错误** | 确认您使用的是最新版本的 Aspose.Note；旧版本可能缺少某些压缩枚举。 |
| **运行时 LicenseException** | 安装有效的 Aspose.Note 许可证 (`License license = new License(); license.setLicense("Aspose.Note.Java.lic");`). |

## 常见问题

**Q: 我可以使用这些选项将其他文档类型（例如 PDF、DOCX）转换为 TIFF 吗？**  
A: 可以。虽然 Aspose.Note 主要针对 OneNote 文件，但 Aspose.PDF、Aspose.Words 等库也为其各自的格式提供类似的 `ImageSaveOptions`。

**Q: TIFF JPEG 压缩与标准 JPEG 文件有何不同？**  
A: JPEG 算法相同，但图像数据位于 TIFF 容器中，后者可以容纳多页并拥有更丰富的元数据。

**Q: 是否可以批量处理大量 `.one` 文件？**  
A: 当然。遍历目录，对每个文件调用任意一种方法，并收集生成的 TIFF。

**Q: 我可以控制输出 TIFF 的 DPI/分辨率吗？**  
A: 可以。在保存之前使用 `options.setResolution(int dpi)`。

**Q: Aspose.Note 支持异步处理吗？**  
A: API 本身是同步的，但您可以将调用包装在 Java 的 `CompletableFuture` 或线程池中以实现并行执行。

## 结论

现在，您拥有完整的 **Java TIFF 转换** 工具包，可在使用 JPEG、PackBits 或 CCITT Group 3 传真压缩将 OneNote 文档保存为 TIFF 文件时**减小 TIFF 文件大小**。通过调整质量、颜色模式和分辨率以满足特定需求，并将这些方法集成到批量工作流中，以实现最高生产力。

---

**最后更新：** 2026-11-05  
**测试环境：** Aspose.Note for Java 26.4（撰写时的最新版本）  
**作者：** Aspose

## 相关教程

- [如何使用保存格式将 OneNote 页面图像（JPEG）渲染为 Aspose.Note for Java](/note/java/onenote-document-saving/save-to-jpeg-image-using-save-format/)
- [使用 Aspose.Note for Java 将 OneNote 保存为 PNG（带选项）——将笔记本转换为图像](/note/java/onenote-notebook-operations/convert-notebook-to-image-with-options/)
- [如何将 OneNote 导出为灰度图像 – Aspose.Note](/note/java/onenote-document-saving/save-to-grayscale-image/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}