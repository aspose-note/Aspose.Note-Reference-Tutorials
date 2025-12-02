---
date: 2025-12-02
description: 了解如何在使用 Aspose.Note for Java 将 OneNote 保存为 HTML 时导出字体。本指南展示了如何以编程方式创建
  OneNote 并嵌入字体、CSS 和图像。
language: zh
linktitle: How to Export Fonts When Saving OneNote as HTML – Java
second_title: Aspose.Note Java API
title: 在将 OneNote 保存为 HTML 时如何导出字体 – Java
url: /java/onenote-document-loading/create-onenote-save-to-html/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何在将 OneNote 保存为 HTML 时导出字体 – Java

## 介绍

在本教程中，您将了解 **如何在使用 Aspose.Note for Java 将 OneNote 保存为 HTML 时导出字体**。我们将演示如何以编程方式创建 OneNote 文档，配置 HTML 保存选项，并嵌入所需的字体文件，使生成的 HTML 与原始 OneNote 页面完全一致。此方法在需要以网页友好格式保留 OneNote 内容的视觉保真度时非常适用。

## 快速答案
- **处理导出的库是什么？** Aspose.Note for Java  
- **可以在 HTML 中嵌入字体吗？** 是 – 将 `ExportFonts` 设置为 `ExportEmbedded`  
- **生产环境需要许可证吗？** 商业使用需要有效的 Aspose.Note 许可证  
- **支持哪个 Java 版本？** Java 8 或更高  
- **是否可以将资源保存为单独的文件？** 当然可以 – 相应地配置 `ResourceExportType`  

## “导出字体”在 OneNote HTML 转换中的含义是什么？

当您将 OneNote 笔记本转换为 HTML 时，视觉外观取决于 CSS、图像，尤其是原始页面使用的字体。**导出字体**指的是将字体文件（例如 TTF）直接嵌入到 HTML 包中，使浏览器能够准确渲染文本，即使终端用户本地未安装这些字体。

## 为什么要以编程方式创建 OneNote 并保存为 HTML？

- **自动化：** 从 OneNote 生成报告、文档或知识库文章，无需手动复制粘贴。  
- **一致性：** 在不同设备间保持布局、样式和自定义字体。  
- **可移植性：** HTML 可在任何平台查看——无需 OneNote 客户端。  

## 前置条件

1. 已安装 Java Development Kit (JDK) 8 或更高版本。  
2. Aspose.Note for Java 库 – 从 [here](https://releases.aspose.com/note/java/) 下载。  
3. 用于加载的示例 OneNote 文件（`.one`），或可通过编程方式创建新文件。  

## 导入包

首先，将所需的类导入到您的 Java 项目中：

```java
import java.io.ByteArrayOutputStream;
import java.io.File;
import java.io.FileOutputStream;
import java.io.IOException;
import java.io.OutputStream;
import java.io.OutputStreamWriter;
import java.nio.file.Paths;
import com.aspose.note.CssSavingArgs;
import com.aspose.note.Document;
import com.aspose.note.FontFaceType;
import com.aspose.note.FontSavingArgs;
import com.aspose.note.HtmlSaveOptions;
import com.aspose.note.ICssSavingCallback;
import com.aspose.note.IFontSavingCallback;
import com.aspose.note.IImageSavingCallback;
import com.aspose.note.ImageSavingArgs;
import com.aspose.note.ResourceExportType;
```

## 如何在将 OneNote 保存为 HTML 时导出字体？

下面是一份逐步指南，展示 **如何导出字体** 以及其他资源。

### 步骤 1：以编程方式创建 OneNote 文档  

```java
Document document = new Document("Path_to_your_sample_one_file");
```

此行加载现有的 `.one` 文件。如果您需要**以编程方式创建 OneNote**，可以实例化一个新的 `Document` 对象，并通过 API 添加章节/页面（此处未展示，以保持重点在导出字体上）。

### 步骤 2：使用嵌入字体保存到内存流  

```java
HtmlSaveOptions options = new HtmlSaveOptions();
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);
options.setFontFaceTypes(FontFaceType.Ttf);

ByteArrayOutputStream outputStream = new ByteArrayOutputStream();
document.save(outputStream, options);
```

- `setExportFonts(ResourceExportType.ExportEmbedded)` 告诉 Aspose.Note **导出字体** 直接到 HTML 包中。  
- `setFontFaceTypes(FontFaceType.Ttf)` 确保使用 TrueType 字体，具有广泛的浏览器支持。

### 步骤 3：以分离资源文件保存为 HTML（仍然导出字体）  

```java
HtmlSaveOptions options = new HtmlSaveOptions();
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);

document.save("output_directory/document.html", options);
```

即使 CSS 和图像已嵌入，如果您希望使用单独的文件以便更易缓存，也可以将 `ResourceExportType` 更改为 `ExportExternal`。关键部分——**导出字体**——保持不变。

### 步骤 4：使用回调控制每个资源的存储位置  

```java
Document document = new Document("Path_to_your_sample_one_file");

UserSavingCallbacks savingCallbacks = new UserSavingCallbacks();
savingCallbacks.setRootFolder("documentFolder");
savingCallbacks.setCssFolder("css");
savingCallbacks.setKeepCssStreamOpened(true);
savingCallbacks.setImagesFolder("images");
savingCallbacks.setFontsFolder("fonts");

HtmlSaveOptions options = new HtmlSaveOptions();
options.setFontFaceTypes(FontFaceType.Ttf);
options.setCssSavingCallback(savingCallbacks);
options.setImageSavingCallback(savingCallbacks);
options.setFontSavingCallback(savingCallbacks);
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);

File dir = new File(savingCallbacks.getRootFolder());
if (!dir.exists()) {
    dir.mkdir();
}

document.save(Paths.get(savingCallbacks.getRootFolder(), "document.html").toString(), options);
```

`UserSavingCallbacks` 类（您需要实现 `ICssSavingCallback`、`IImageSavingCallback` 和 `IFontSavingCallback`）让您完全控制文件夹结构，能够将字体保存在专用的 `fonts` 目录中，同时仍然正确 **导出字体**。

## 常见问题与技巧

- **输出中缺少字体：** 确认已设置 `setExportFonts(ResourceExportType.ExportEmbedded)`，并且源 OneNote 文件实际使用了嵌入字体。  
- **HTML 文件过大：** 嵌入字体会增加体积。如果带宽是问题，可将 `ExportFonts` 切换为 `ExportExternal`，并将字体托管在 CDN 上。  
- **回调实现错误：** 确保回调类正确写入流并关闭资源，以避免文件损坏。  

## 常见问答

**Q: 我可以一次性将多个 OneNote 文档转换为 HTML 吗？**  
A: 可以，遍历每个 `Document` 实例并使用相同的 `HtmlSaveOptions`。

**Q: Aspose.Note for Java 是否支持除 HTML 之外的其他输出格式？**  
A: 当然。您可以使用相应的保存选项导出为 PDF、DOCX、PNG、JPEG 等。

**Q: 是否有 Aspose.Note for Java 的试用版？**  
A: 有，请从 [here](https://releases.aspose.com/) 下载免费试用版。

**Q: 在哪里可以获得 Aspose.Note for Java 的支持？**  
A: 请访问 [Aspose.Note forum](https://forum.aspose.com/c/note/28) 获取社区和官方帮助。

**Q: 如何购买 Aspose.Note for Java 的许可证？**  
A: 许可证可在 [Aspose website](https://purchase.aspose.com/buy) 购买。

## 结论

您现在已经了解 **如何在使用 Aspose.Note for Java 将 OneNote 保存为 HTML 时导出字体**。通过配置 `HtmlSaveOptions` 并可选使用回调，您可以在网页上呈现 OneNote 页面时保留其完整外观——包括自定义字体。欢迎尝试不同的 `ResourceExportType` 设置，以满足项目的性能和存储需求。

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**最后更新：** 2025-12-02  
**测试环境：** Aspose.Note for Java 24.12  
**作者：** Aspose  

---