---
date: 2025-12-17
description: 学习如何使用 Aspose.Note for Java 将 OneNote 导出为灰度 PNG 图像。包括加载 OneNote 文档并创建灰度图像的步骤。
linktitle: How to Export OneNote as Grayscale Image – Aspose.Note
second_title: Aspose.Note Java API
title: 如何将 OneNote 导出为灰度图像 – Aspose.Note
url: /zh/java/onenote-document-saving/save-to-grayscale-image/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 在 OneNote 中保存为灰度图像 - Aspose.Note

## 介绍

在本教程中，我们将展示如何使用 Aspose.Note for Java 通过将文档保存为灰度图像来 **导出 onenote**。灰度图像是仅包含灰色阴影的单色图片，可用于打印、归档或减小文件大小。我们将演示加载 OneNote 文档、配置保存选项以 **创建灰度图像**，并最终 **将文档保存为 PNG**。

## 快速回答
- **“how to export onenote” 是什么意思？** 它指的是以编程方式将 OneNote 文件转换为其他格式，例如图像。  
- **哪种格式最适合灰度输出？** PNG 表现良好，因为它保持无损质量并支持灰度颜色模式。  
- **我需要许可证吗？** 生产环境需要有效的 Aspose.Note 许可证；测试时可使用临时试用许可证。  
- **需要哪个 Java 版本？** 建议使用 Java 8 或更高版本。  
- **我可以更改图像尺寸吗？** 可以，在保存之前调整 `ImageSaveOptions` 的属性，如 `Resolution` 或 `PageSize`。

## 什么是 “how to export onenote”？
导出 OneNote 是指以编程方式将 OneNote `.one` 文件转换为其他表示形式，例如 PDF、HTML 或图像。在本指南中，我们专注于导出为 **灰度 PNG** 图像，这在文档或打印工作流中是常见需求。

## 为什么要将 OneNote 导出为灰度图像？
- **文件大小减小** – 灰度 PNG 通常比全彩图像更小。  
- **可读性更好** – 对于打印报告，灰度通常提供更清晰的对比度。  
- **兼容性** – PNG 在浏览器、编辑器和移动设备上得到广泛支持。  

## 先决条件

在开始之前，请确保您具备以下条件：

1. 已在系统上安装 Java Development Kit (JDK)。  
2. Aspose.Note for Java 库。您可以从 [here](https://releases.aspose.com/note/java/) 下载。  
3. 对 Java 编程有基本了解。  

## 导入包

要开始，请导入必要的包：

```java
import com.aspose.note.ColorMode;
import com.aspose.note.Document;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.SaveFormat;
import java.io.IOException;
```

## 步骤 1：加载 OneNote 文档

首先，**加载 onenote 文档** 到 Aspose.Note。将 `"Your Document Directory"` 替换为本地文件夹路径，将 `"Aspose.one"` 替换为 OneNote 文件的名称。

```java
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Aspose.one");
```

## 步骤 2：设置输出路径和选项

为灰度图像定义输出路径并指定保存选项。我们将 `ColorMode` 设置为 `GrayScale`，并使用 **save document as png** 格式。

```java
dataDir = dataDir + "SaveAsGrayscaleImage_out.png";
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);
options.setColorMode(ColorMode.GrayScale);
```

## 步骤 3：保存文档

最后，使用配置好的选项将文档保存为灰度 PNG 图像。

```java
oneFile.save(dataDir, options);
```

## 常见问题及解决方案
- **FileNotFoundException** – 验证 `dataDir` 指向正确的文件夹且 `.one` 文件存在。  
- **LicenseException** – 在调用 `save` 之前确保已应用有效的 Aspose.Note 许可证。  
- **低分辨率输出** – 如有需要，调整 `options.setResolution(300)` 以提高 DPI。  

## 常见问答

**Q1：我可以将灰度图像保存为其他格式吗？**  
A1：可以，只需在 `ImageSaveOptions` 构造函数中将 `SaveFormat` 参数更改为 `Jpeg`、`Bmp` 等。

**Q2：Aspose.Note 是否兼容所有版本的 OneNote 文档？**  
A2：Aspose.Note 支持 Microsoft OneNote 2010 及更高版本。

**Q3：使用 Aspose.Note 是否需要许可证？**  
A3：生产使用需要有效许可证，但可获取临时试用许可证进行评估。

**Q4：在将文档保存为图像之前，我可以操作文档的其他方面吗？**  
A4：当然！Aspose.Note 提供了完整的 API，可在导出前编辑章节、页面和内容。

**Q5：如果遇到问题，我可以在哪里获得支持？**  
A5：您可以在 Aspose.Note 论坛 [here](https://forum.aspose.com/c/note/28) 获得支持。

## 结论

您现在已经学习了通过加载 OneNote 文件、配置保存选项以 **创建灰度图像**，以及 **将文档保存为 PNG** 的 **how to export onenote** 方法。此技术对于从 OneNote 笔记本生成轻量级、可直接打印的视觉内容非常实用。欢迎尝试其他 `ColorMode` 设置或图像格式，以满足项目需求。

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Last Updated:** 2025-12-17  
**Tested With:** Aspose.Note 24.12 for Java  
**Author:** Aspose  

---