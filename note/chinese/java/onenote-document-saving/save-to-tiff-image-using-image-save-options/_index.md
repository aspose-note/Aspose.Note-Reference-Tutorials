---
date: 2025-12-17
description: 学习如何在 Java 中使用 TIFF JPEG 压缩、PackBits 或 CCITT Group 3 传真将 OneNote 文档保存为
  TIFF 文件。使用 Aspose.Note 控制图像质量、文件大小和颜色模式。
linktitle: Save to TIFF Image Using TIFF JPEG Compression in OneNote
second_title: Aspose.Note Java API
title: 在 OneNote 中使用 TIFF JPEG 压缩保存为 TIFF 图像
url: /zh/java/onenote-document-saving/save-to-tiff-image-using-image-save-options/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 在 OneNote 中使用 TIFF JPEG 压缩保存为 TIFF 图像

## 介绍

在本教程中，您将了解 **如何使用 TIFF JPEG 压缩将 OneNote 文档保存为 TIFF 文件**，以及另外两种流行的压缩方法。我们将逐步演示所需的设置，导入必要的 Java 包，并为每种压缩选项提供清晰的逐步代码。完成后，您将能够控制 **TIFF 图像质量**，减小文件大小，甚至生成用于传真风格输出的黑白 TIFF。

## 快速答案
- **TIFF JPEG 压缩是什么？** 一种有损压缩方法，可在保持视觉质量的同时减小 TIFF 文件大小。  
- **哪个库负责转换？** Aspose.Note for Java。  
- **我需要许可证吗？** 免费试用可用于测试；生产环境需要许可证。  
- **我可以更改图像质量吗？** 可以，在 `ImageSaveOptions` 上设置 `quality` 属性。  
- **批量转换是否可行？** 完全可以——遍历文档并应用相同的选项。

## 什么是 TIFF JPEG 压缩？

TIFF JPEG 压缩将图像数据存储在 TIFF 容器中，但使用 JPEG 的有损算法来压缩文件。当您需要在 **tiff 图像质量** 与更小文件大小之间取得平衡时，它是理想选择，尤其适用于网络或归档场景。

## 为什么使用不同的 TIFF 压缩类型？

- **JPEG** – 适合照片；提供可调节的质量。  
- **PackBits** – 简单的无损行程长度编码；适用于具有大面积均匀区域的图形。  
- **CCITT Group 3 Fax** – 仅黑白；非常适合扫描文档和传真传输。  

选择合适的压缩方式可让您在满足存储限制的同时，不牺牲应用所需的视觉保真度。

## 先决条件

- 已安装 Java Development Kit (JDK)。  
- 已将 Aspose.Note for Java 库添加到项目中（Maven/Gradle 或手动 JAR）。  
- 对 Java 语法有基本了解。

## 导入包

首先，将必要的 Aspose.Note 类导入到您的 Java 文件中：

```java
import com.aspose.note.*;
import java.io.IOException;
import java.nio.file.Paths;
```

## 步骤 1：使用 TIFF JPEG 压缩保存为 TIFF

下面是完整的方法，它加载 OneNote 文件并使用 JPEG 压缩将其保存为 TIFF。调整 `quality` 值（0‑100）以控制 **tiff 图像质量**。

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

**解释**

- `ImageSaveOptions` 告诉 Aspose.Note 输出为 TIFF 文件。  
- `setTiffCompression(TiffCompression.Jpeg)` 选择 JPEG 压缩。  
- `setQuality(93)`（可选）微调图像质量；较低的值会生成更小的文件。

### 如何在 Java 中使用 JPEG 压缩保存 TIFF
1. 将 `dataDir` 指向包含 `.one` 文件的文件夹。  
2. 从主方法或服务中调用 `SaveToTiffUsingJpegCompression()`。  
3. 生成的 `.tiff` 文件将出现在同一目录中。

## 步骤 2：使用 PackBits 压缩保存为 TIFF

如果您需要无损选项，PackBits 是一种简单的行程长度算法，适用于具有纯色的图形。

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

**解释**

- `setTiffCompression(TiffCompression.PackBits)` 切换压缩方式。  
- 无需质量设置，因为 PackBits 是无损的。

## 步骤 3：使用 CCITT Group 3 Fax 压缩（黑白 TIFF）保存为 TIFF

对于传真风格的文档，您通常需要 **黑白 TIFF**。CCITT Group 3 为单色图像提供高压缩率。

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

**解释**

- `setColorMode(ColorMode.BlackAndWhite)` 强制输出为单色。  
- `setTiffCompression(TiffCompression.Ccitt3)` 应用针对传真优化的压缩。

## 常见问题与技巧

| 问题 | 解决方案 |
|-------|----------|
| **输出文件比预期更大** | 尝试降低 JPEG `quality` 值，或在可接受无损的情况下切换到 PackBits。 |
| **颜色显得褪色** | 确保在需要全彩时未意外设置 `ColorMode.BlackAndWhite`。 |
| **不支持的图像格式错误** | 确认您使用的是最新版本的 Aspose.Note；旧版本可能缺少某些压缩枚举。 |
| **运行时 LicenseException** | 安装有效的 Aspose.Note 许可证（`License license = new License(); license.setLicense("Aspose.Note.Java.lic");`）。 |

## 常见问题

**Q: 我可以使用这些选项将其他文档类型（例如 PDF、DOCX）转换为 TIFF 吗？**  
A: 可以。Aspose.Note 专注于 OneNote 文件，但 Aspose 的其他库（PDF、Words）为各自的格式提供类似的 `ImageSaveOptions`。

**Q: TIFF JPEG 压缩与标准 JPEG 文件有何不同？**  
A: 图像数据存储在 TIFF 容器中，保留元数据并支持多页，而压缩算法仍然是 JPEG。

**Q: 是否可以批量处理大量 `.one` 文件？**  
A: 完全可以。遍历文件夹，对每个文件调用任意三种方法之一，并收集生成的 TIFF。

**Q: 我可以控制输出 TIFF 的 DPI/分辨率吗？**  
A: 可以。保存前使用 `options.setResolution(int dpi)`。

**Q: Aspose.Note 支持异步处理吗？**  
A: API 本身是同步的，但您可以将调用包装在 Java 的 `CompletableFuture` 或线程池中，以实现并行执行。

## 结论

现在您拥有完整的 **java tiff 转换** 工具包，可使用 JPEG、PackBits 或 CCITT Group 3 Fax 压缩将 OneNote 文档保存为 TIFF 文件。调整质量、颜色模式和分辨率，以满足您特定的 **tiff 图像质量** 要求，并将这些方法集成到批量工作流中，以实现最高生产力。

---

**Last Updated:** 2025-12-17  
**Tested With:** Aspose.Note for Java 23.12 (latest at time of writing)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}