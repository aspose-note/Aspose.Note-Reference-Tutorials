---
date: 2025-12-16
description: 了解如何使用 Aspose.Note for Java 的图像保存选项将 OneNote 文档保存为 BMP 图像。还可以查看如何将 OneNote
  保存为 PDF 或 PNG。
linktitle: how to save onenote to BMP Image Using Image Save Options
second_title: Aspose.Note Java API
title: 如何使用图像保存选项将 OneNote 保存为 BMP 图像
url: /zh/java/onenote-document-saving/save-to-bmp-image-using-image-save-options/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何使用图像保存选项将 OneNote 保存为 BMP 图像

## 介绍

Aspose.Note for Java 是一个强大的库，使 Java 开发者能够以编程方式处理 Microsoft OneNote 文件。**在本教程中，您将学习如何使用 Aspose.Note for Java 的图像保存选项功能将 OneNote 文档保存为 BMP 图像**。我们将逐步演示每个步骤，解释为何可能会选择 BMP 而非其他格式，并展示如何将此功能集成到您自己的应用程序中。

## 快速答案
- **Image Save Options 类的作用是什么？** 它允许您在将 OneNote 页面转换为图像时指定输出图像格式（BMP、PNG、JPEG 等）。  
- **运行示例是否需要许可证？** 免费试用可用于评估，但生产环境需要商业许可证。  
- **我可以将 OneNote 页面转换为 PDF 或 PNG 而不是 BMP 吗？** 可以——只需更改 `SaveFormat` 枚举（例如 `SaveFormat.Pdf` 或 `SaveFormat.Png`）。  
- **支持哪个 Java 版本？** 完全支持 Java 8 及更高版本。  
- **对于大型文档是否有特殊处理？** 您可以流式输出以避免高内存消耗。

## Aspose.Note 中的 “Image Save Options” 是什么？

`ImageSaveOptions` 类提供了对 OneNote 页面渲染为光栅图像的细粒度控制。您可以设置图像格式、分辨率、色深等。此灵活性使得能够轻松生成用于遗留系统的 BMP 文件或用于 Web 的 PNG/JPEG 文件。

## 前置条件

1. 对 Java 编程语言的基本了解。  
2. 在机器上已安装 JDK（Java Development Kit）。  
3. 如 Eclipse 或 IntelliJ IDEA 等 IDE。  
4. Aspose.Note for Java 库——从 [here](https://releases.aspose.com/note/java/) 下载。

## 导入包

首先，导入必要的 Aspose.Note 类和标准的 Java I/O 实用工具：

```java
import com.aspose.note.*;
import java.io.IOException;
```

## 步骤 1：加载 OneNote 文档

```java
// The path to the documents directory.
String dataDir = "Your Document Directory";

// Load the document into Aspose.Note.
Document oneFile = new Document(dataDir + "Aspose.one");
```

这里我们指向包含源 OneNote 文件（`Aspose.one`）的文件夹，并将其加载到 `Document` 对象中。该对象让您可以完整访问笔记本中的页面、章节以及其他元素。

## 步骤 2：将文档保存为 BMP 图像

```java
dataDir = dataDir + "SaveToBmpImageUsingImageSaveOptions_out.bmp";

// Save the document.
oneFile.save(dataDir, new ImageSaveOptions(SaveFormat.Bmp));
```

我们拼接输出文件名，然后使用配置为 **BMP**（`SaveFormat.Bmp`）的 `ImageSaveOptions` 实例调用 `save`。  
如果您想将 **OneNote 页面** 保存为 PNG，只需将 `SaveFormat.Bmp` 替换为 `SaveFormat.Png`。同样，`SaveFormat.Pdf` 可用于执行 **OneNote 转 PDF** 的转换。

## 为什么选择 BMP？

- **无损质量** – BMP 存储原始像素数据，保留原始页面的精确外观。  
- **兼容性** – 许多旧的 Windows 应用程序常常需要 BMP 文件。  
- **简洁性** – 没有压缩伪影，适合进一步的图像处理。

## 常见问题与技巧

- **文件路径错误** – 确保 `dataDir` 以适当的文件分隔符（`/` 或 `\`）结尾。  
- **大型笔记本** – 对于非常大的 OneNote 文件，考虑逐页保存以降低内存使用。  
- **许可证异常** – 在没有有效许可证的情况下运行代码会在生成的图像上添加水印。

## 结论

在本指南中，我们演示了使用 Aspose.Note for Java 的 `ImageSaveOptions` **将 OneNote 文档保存为 BMP 图像** 的方法。通过切换 `SaveFormat` 枚举，您还可以生成 PNG、JPEG、PDF 或其他受支持的格式，为导出 OneNote 内容以满足任何后续场景提供了灵活的方式。

## 常见问题

**Q1: 我可以将 OneNote 文档保存为除 BMP 之外的其他图像格式吗？**  
A: 可以，您可以使用 `ImageSaveOptions` 并配合 `SaveFormat.Png`、`SaveFormat.Jpeg`、`SaveFormat.Gif` 或 `SaveFormat.Tiff` 导出为相应格式。

**Q2: Aspose.Note for Java 是否支持不同文档格式之间的转换？**  
A: 当然。除了图像格式外，您还可以使用相应的 `SaveFormat` 将 OneNote 文件转换为 PDF、DOCX、HTML 等。

**Q3: Aspose.Note for Java 是否兼容最新版本的 OneNote？**  
A: 是的，该库会定期更新，以保持与最新 OneNote 版本同步。

**Q4: 我可以以编程方式操作 OneNote 文档的内容吗？**  
A: 可以，您可以通过 API 添加、编辑或删除页面、章节以及丰富内容（文本、图像、表格）。

**Q5: Aspose.Note for Java 是否提供技术支持？**  
A: 是的，Aspose 提供技术支持和专门的论坛。访问 [Aspose.Note forum](https://forum.aspose.com/c/note/28) 获取帮助。

---

**最后更新：** 2025-12-16  
**测试环境：** Aspose.Note for Java 24.12  
**作者：** Aspose

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
