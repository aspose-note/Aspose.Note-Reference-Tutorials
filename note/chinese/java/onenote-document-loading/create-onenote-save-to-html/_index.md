---
title: 创建 OneNote 文档并保存为 HTML - Java
linktitle: 创建 OneNote 文档并保存为 HTML - Java
second_title: Aspose.Note Java API
description: 了解使用 Aspose.Note for Java 创建 OneNote 文档并将其保存为 HTML。集成到 Java 应用程序中以进行编程式 OneNote 文件处理。

weight: 18
url: /zh/java/onenote-document-loading/create-onenote-save-to-html/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 创建 OneNote 文档并保存为 HTML - Java

## 介绍

Aspose.Note for Java 是一个功能强大的库，允许开发人员以编程方式使用 Microsoft OneNote 文件。在本教程中，我们将探索如何使用 Aspose.Note for Java 创建 OneNote 文档并将其保存为 HTML 格式。

## 先决条件

在我们开始之前，请确保您具备以下条件：

1. 您的系统上安装了 Java 开发工具包 (JDK)。
2.  Java 库的 Aspose.Note。您可以从以下位置下载：[这里](https://releases.aspose.com/note/java/).
3. Java 编程的基础知识。

## 导入包

首先，将必要的包导入到您的 Java 项目中：

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

## 第 1 步：创建 OneNote 文档对象

```java
Document document = new Document("Path_to_your_sample_one_file");
```

这段代码初始化了一个`Document`通过加载示例 OneNote 文件来获取对象。

## 第 2 步：另存为 HTML 到内存流

```java
HtmlSaveOptions options = new HtmlSaveOptions();
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);
options.setFontFaceTypes(FontFaceType.Ttf);

ByteArrayOutputStream outputStream = new ByteArrayOutputStream();
document.save(outputStream, options);
```

在这里，我们设置 HTML 保存选项并将文档保存到内存流。

## 第 3 步：另存为 HTML，资源位于单独的文件中

```java
HtmlSaveOptions options = new HtmlSaveOptions();
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);

document.save("output_directory/document.html", options);
```

此步骤将文档另存为 HTML，并将 CSS、字体和图像等资源保存在单独的文件中。

## 第 4 步：保存为 HTML 到内存流，并通过回调来节省资源

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

在这里，我们使用回调将文档作为 HTML 保存到内存流中以处理资源节省。

## 结论

恭喜！您已经学习了如何使用 Aspose.Note for Java 创建 OneNote 文档并将其保存为 HTML 格式。现在，您可以将此功能集成到 Java 应用程序中，以编程方式处理 OneNote 文件。

## 常见问题解答

### Q1：我可以一次性将多个 OneNote 文档转换为 HTML 吗？

A1：是的，您可以循环遍历多个文档并迭代应用保存过程。

### Q2：Aspose.Note for Java 是否支持除 HTML 之外的其他输出格式？

A2：是的，Aspose.Note for Java 支持各种输出格式，包括 PDF、DOCX 和图像格式。

### Q3：Aspose.Note for Java 有试用版吗？

A3：是的，您可以从以下位置下载免费试用版：[这里](https://releases.aspose.com/).

### 问题 4：在哪里可以获得 Aspose.Note for Java 的支持？

 A4：您可以从以下机构获得支持[Aspose.Note 论坛](https://forum.aspose.com/c/note/28).

### Q5：如何购买 Aspose.Note for Java 的许可证？

 A5：您可以从以下位置购买许可证：[阿斯普斯网站](https://purchase.aspose.com/buy).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
