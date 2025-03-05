---
title: 在 Aspose.Note 中创建 OneNote 文档并保存为 HTML
linktitle: 在 Aspose.Note 中创建 OneNote 文档并保存为 HTML
second_title: Aspose.Note .NET API
description: 了解如何使用 Aspose.Note API 在 .NET 应用程序中创建 Microsoft OneNote 文档并将其保存为 HTML 格式。请按照我们包含分步示例的综合教程进行操作。
type: docs
weight: 14
url: /zh/net/loading-and-saving-operations/create-onenote-doc-save-to-html/
---
## 介绍

Aspose.Note for .NET 是一个功能强大的 API，允许开发人员在其 .NET 应用程序中以编程方式使用 Microsoft OneNote 文档。使用 Aspose.Note，您可以轻松创建、操作和转换 OneNote 文件。在本教程中，我们将探索如何使用 Aspose.Note for .NET API 提供的各种选项创建 OneNote 文档并将其保存为 HTML 格式。

## 先决条件

在我们开始之前，请确保您满足以下先决条件：

- C# 编程语言的基础知识。
- Visual Studio 安装在您的系统上。
-  Aspose.Note for .NET API 安装在您的项目中。您可以从以下位置下载：[这里](https://releases.aspose.com/note/net/).
- 熟悉Microsoft OneNote文档的结构。

## 导入命名空间

在我们深入编码部分之前，让我们导入必要的命名空间：

```csharp
using System;
using System.Drawing;
using System.Globalization;
using System.IO;

using Aspose.Note.Saving;
using Aspose.Note.Saving.Html;

```

现在，让我们将每个示例分解为多个步骤，看看如何使用 Aspose.Note for .NET 创建 OneNote 文档并将其保存为 HTML 格式。

## 步骤 1：使用默认选项创建 OneNote 文档

```csharp
public static void CreateAndSaveToHTMLUsingDefaultOptions()
{
    //初始化 OneNote 文档
    Document doc = new Document();
    Page page = doc.AppendChildLast(new Page());

    //文档中所有文本的默认样式。
    ParagraphStyle textStyle = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
    page.Title = new Title()
    {
        TitleText = new RichText() { Text = "Title text.", ParagraphStyle = textStyle },
        TitleDate = new RichText() { Text = new DateTime(2011, 11, 11).ToString("D", CultureInfo.InvariantCulture), ParagraphStyle = textStyle },
        TitleTime = new RichText() { Text = "12:34", ParagraphStyle = textStyle }
    };

    //保存为 HTML 格式
    string dataDir = "Your Document Directory";
    string outputPath = Path.Combine(dataDir, "CreateOneNoteDocAndSaveToHTML_out.html");
    doc.Save(outputPath);

    Console.WriteLine("\nOneNote document created successfully.\nFile saved at " + outputPath);
}
```

在此步骤中，我们初始化一个新的 OneNote 文档，添加带有标题的页面，并使用默认选项将其保存为 HTML 格式。

## 步骤 2：创建特定页面范围并将其保存为 HTML

```csharp
public static void CreateAndSavePageRange()
{
    //初始化 OneNote 文档
    Document doc = new Document();
    Page page = doc.AppendChildLast(new Page());

    //文档中所有文本的默认样式。
    ParagraphStyle textStyle = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
    page.Title = new Title()
    {
        TitleText = new RichText() { Text = "Title text.", ParagraphStyle = textStyle },
        TitleDate = new RichText() { Text = new DateTime(2011, 11, 11).ToString("D", CultureInfo.InvariantCulture), ParagraphStyle = textStyle },
        TitleTime = new RichText() { Text = "12:34", ParagraphStyle = textStyle }
    };

    //保存为 HTML 格式
    string dataDir = "Your Document Directory";
    string outputPath = Path.Combine(dataDir, "CreateAndSavePageRange_out.html");
    doc.Save(outputPath, new HtmlSaveOptions { PageCount = 1, PageIndex = 0 });

    Console.WriteLine("\nOneNote document created successfully and saved as page range.\nFile saved at " + outputPath);
}
```

在这里，我们演示如何创建文档并将特定页面范围保存为 HTML 格式。

## 步骤 3：将嵌入资源另存为 HTML 到内存流

```csharp
public static void SaveAsHTMLToMemoryStreamWithEmbeddedResources()
{
    //加载 OneNote 文档
    string dataDir = "Your Document Directory";
    var document = new Document(Path.Combine(dataDir, "Aspose.one"));

    //指定 HTML 保存选项
    var options = new HtmlSaveOptions()
    {
        ExportCss = ResourceExportType.ExportEmbedded,
        ExportFonts = ResourceExportType.ExportEmbedded,
        ExportImages = ResourceExportType.ExportEmbedded,
        FontFaceTypes = FontFaceType.Ttf
    };

    //将文档保存到内存流
    var memoryStream = new MemoryStream();
    document.Save(memoryStream, options);
}
```

此步骤说明如何将带有嵌入资源（CSS、字体和图像）的 OneNote 文档保存为 HTML 格式到内存流中。

## 步骤 4：另存为 HTML 到文件，资源位于单独的文件中

```csharp
public static void SaveAsHTMLToFileWithResourcesInSeparateFiles()
{
    //加载 OneNote 文档
    string dataDir = "Your Document Directory";
    var document = new Document(Path.Combine(dataDir, "Aspose.one"));

    //指定 HTML 保存选项
    var options = new HtmlSaveOptions()
    {
        ExportCss = ResourceExportType.ExportAsStream,
        ExportFonts = ResourceExportType.ExportAsStream,
        ExportImages = ResourceExportType.ExportAsStream,
        FontFaceTypes = FontFaceType.Ttf
    };

    //将文档保存为 HTML 文件，资源存储在单独的文件中
    document.Save(Path.Combine(dataDir, "document_out.html"), options);
}
```

在此步骤中，我们将 OneNote 文档保存为 HTML 格式，并将所有资源（CSS、字体和图像）存储在单独的文件中。

## 第 5 步：保存为 HTML 到内存流，并通过回调来节省资源

```csharp
public static void SaveAsHTMLToMemoryStreamWithCallBacksToSaveResources()
{
    //指定保存回调配置
    var savingCallbacks = new UserSavingCallbacks()
    {
        RootFolder = "documentFolder",
        CssFolder = "css",
        KeepCssStreamOpened = true,
        ImagesFolder = "images",
        FontsFolder = "fonts"
    };

    //指定 HTML 保存选项
    var options = new HtmlSaveOptions
    {
        FontFaceTypes = FontFaceType.Ttf,
        CssSavingCallback = savingCallbacks,
        FontSavingCallback = savingCallbacks,
        ImageSavingCallback = savingCallbacks
    };

    //加载 OneNote 文档
    string dataDir = "Your Document Directory";
    var document = new Document(Path.Combine(dataDir, "Aspose.one"));

    //使用由用户定义的回调管理的资源将文档保存为 HTML 格式
    using (var stream = File.Create(Path.Combine(savingCallbacks.RootFolder, "document.html")))
    {
        document.Save(stream, options);
    }

    //手动将数据附加到 CSS 流
    using (var writer = new StreamWriter(savingCallbacks.CssStream))
    {
        writer.WriteLine();
        writer.WriteLine("/* This line is appended to stream manually by user */");
    }
}
```

在这里，我们演示如何使用用户定义的回调管理的资源将 OneNote 文档保存为 HTML 格式。

## 结论

在本文中，我们探讨了如何使用 Aspose.Note for .NET 处理 OneNote 文档并将其保存为 HTML 格式。通过遵循分步指南，您可以轻松地

 将此功能集成到您的 .NET 应用程序中，使您能够高效地操作 OneNote 文件。

## 常见问题解答

### Q1：我可以自定义保存的 HTML 文件的外观吗？

A1：是的，您可以通过修改转换过程中生成的 CSS 样式表来自定义外观。

### Q2：Aspose.Note是否支持转换为HTML以外的其他格式？

A2：是的，Aspose.Note 支持转换为各种格式，例如 PDF、图像和 Microsoft Word 文档。

### Q3：Aspose.Note 与.NET Core 应用程序兼容吗？

A3：是的，Aspose.Note 与 .NET Framework 和 .NET Core 应用程序兼容。

### Q4：我可以使用Aspose.Note从OneNote文档中提取文本和图像吗？

A4：是的，您可以使用 Aspose.Note API 提取文本和图像以及执行各种其他操作。

### Q5：是否有试用版可用于测试Aspose.Note 功能？

 A5：是的，您可以从以下位置下载免费试用版：[这里](https://releases.aspose.com/).