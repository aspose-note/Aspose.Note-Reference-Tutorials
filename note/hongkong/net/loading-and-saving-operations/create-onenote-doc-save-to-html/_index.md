---
title: 在 Aspose.Note 中建立 OneNote 文件並儲存為 HTML
linktitle: 在 Aspose.Note 中建立 OneNote 文件並儲存為 HTML
second_title: Aspose.Note .NET API
description: 了解如何使用 Aspose.Note API 在 .NET 應用程式中建立 Microsoft OneNote 文件並將其儲存為 HTML 格式。請按照我們包含逐步範例的綜合教學進行操作。
weight: 14
url: /zh-hant/net/loading-and-saving-operations/create-onenote-doc-save-to-html/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 在 Aspose.Note 中建立 OneNote 文件並儲存為 HTML

## 介紹

Aspose.Note for .NET 是一個功能強大的 API，可讓開發人員在其 .NET 應用程式中以程式設計方式使用 Microsoft OneNote 文件。使用 Aspose.Note，您可以輕鬆建立、操作和轉換 OneNote 檔案。在本教程中，我們將探索如何使用 Aspose.Note for .NET API 提供的各種選項建立 OneNote 文件並將其儲存為 HTML 格式。

## 先決條件

在我們開始之前，請確保您符合以下先決條件：

- C# 程式語言的基礎知識。
- Visual Studio 安裝在您的系統上。
-  Aspose.Note for .NET API 安裝在您的專案中。您可以從以下位置下載：[這裡](https://releases.aspose.com/note/net/).
- 熟悉Microsoft OneNote文件的架構。

## 導入命名空間

在我們深入編碼部分之前，讓我們先導入必要的命名空間：

```csharp
using System;
using System.Drawing;
using System.Globalization;
using System.IO;

using Aspose.Note.Saving;
using Aspose.Note.Saving.Html;

```

現在，讓我們將每個範例分解為多個步驟，看看如何使用 Aspose.Note for .NET 建立 OneNote 文件並將其儲存為 HTML 格式。

## 步驟 1：使用預設選項建立 OneNote 文檔

```csharp
public static void CreateAndSaveToHTMLUsingDefaultOptions()
{
    //初始化 OneNote 文檔
    Document doc = new Document();
    Page page = doc.AppendChildLast(new Page());

    //文件中所有文字的預設樣式。
    ParagraphStyle textStyle = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
    page.Title = new Title()
    {
        TitleText = new RichText() { Text = "Title text.", ParagraphStyle = textStyle },
        TitleDate = new RichText() { Text = new DateTime(2011, 11, 11).ToString("D", CultureInfo.InvariantCulture), ParagraphStyle = textStyle },
        TitleTime = new RichText() { Text = "12:34", ParagraphStyle = textStyle }
    };

    //儲存為 HTML 格式
    string dataDir = "Your Document Directory";
    string outputPath = Path.Combine(dataDir, "CreateOneNoteDocAndSaveToHTML_out.html");
    doc.Save(outputPath);

    Console.WriteLine("\nOneNote document created successfully.\nFile saved at " + outputPath);
}
```

在此步驟中，我們初始化一個新的 OneNote 文檔，添加帶有標題的頁面，並使用預設選項將其儲存為 HTML 格式。

## 步驟 2：建立特定頁面範圍並將其儲存為 HTML

```csharp
public static void CreateAndSavePageRange()
{
    //初始化 OneNote 文檔
    Document doc = new Document();
    Page page = doc.AppendChildLast(new Page());

    //文件中所有文字的預設樣式。
    ParagraphStyle textStyle = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
    page.Title = new Title()
    {
        TitleText = new RichText() { Text = "Title text.", ParagraphStyle = textStyle },
        TitleDate = new RichText() { Text = new DateTime(2011, 11, 11).ToString("D", CultureInfo.InvariantCulture), ParagraphStyle = textStyle },
        TitleTime = new RichText() { Text = "12:34", ParagraphStyle = textStyle }
    };

    //儲存為 HTML 格式
    string dataDir = "Your Document Directory";
    string outputPath = Path.Combine(dataDir, "CreateAndSavePageRange_out.html");
    doc.Save(outputPath, new HtmlSaveOptions { PageCount = 1, PageIndex = 0 });

    Console.WriteLine("\nOneNote document created successfully and saved as page range.\nFile saved at " + outputPath);
}
```

在這裡，我們示範如何建立文件並將特定頁面範圍儲存為 HTML 格式。

## 步驟 3：將嵌入資源儲存為 HTML 到記憶體流

```csharp
public static void SaveAsHTMLToMemoryStreamWithEmbeddedResources()
{
    //載入 OneNote 文檔
    string dataDir = "Your Document Directory";
    var document = new Document(Path.Combine(dataDir, "Aspose.one"));

    //指定 HTML 儲存選項
    var options = new HtmlSaveOptions()
    {
        ExportCss = ResourceExportType.ExportEmbedded,
        ExportFonts = ResourceExportType.ExportEmbedded,
        ExportImages = ResourceExportType.ExportEmbedded,
        FontFaceTypes = FontFaceType.Ttf
    };

    //將文件儲存到記憶體流
    var memoryStream = new MemoryStream();
    document.Save(memoryStream, options);
}
```

此步驟說明如何將帶有嵌入資源（CSS、字體和圖像）的 OneNote 文件儲存為 HTML 格式到記憶體流中。

## 步驟 4：另存為 HTML 到文件，資源位於單獨的文件中

```csharp
public static void SaveAsHTMLToFileWithResourcesInSeparateFiles()
{
    //載入 OneNote 文檔
    string dataDir = "Your Document Directory";
    var document = new Document(Path.Combine(dataDir, "Aspose.one"));

    //指定 HTML 儲存選項
    var options = new HtmlSaveOptions()
    {
        ExportCss = ResourceExportType.ExportAsStream,
        ExportFonts = ResourceExportType.ExportAsStream,
        ExportImages = ResourceExportType.ExportAsStream,
        FontFaceTypes = FontFaceType.Ttf
    };

    //將文件儲存為 HTML 文件，資源儲存在單獨的文件中
    document.Save(Path.Combine(dataDir, "document_out.html"), options);
}
```

在此步驟中，我們將 OneNote 文件儲存為 HTML 格式，並將所有資源（CSS、字體和圖像）儲存在單獨的文件中。

## 步驟 5： 儲存為 HTML 到記憶體流，並透過回調來節省資源

```csharp
public static void SaveAsHTMLToMemoryStreamWithCallBacksToSaveResources()
{
    //指定儲存回呼配置
    var savingCallbacks = new UserSavingCallbacks()
    {
        RootFolder = "documentFolder",
        CssFolder = "css",
        KeepCssStreamOpened = true,
        ImagesFolder = "images",
        FontsFolder = "fonts"
    };

    //指定 HTML 儲存選項
    var options = new HtmlSaveOptions
    {
        FontFaceTypes = FontFaceType.Ttf,
        CssSavingCallback = savingCallbacks,
        FontSavingCallback = savingCallbacks,
        ImageSavingCallback = savingCallbacks
    };

    //載入 OneNote 文檔
    string dataDir = "Your Document Directory";
    var document = new Document(Path.Combine(dataDir, "Aspose.one"));

    //使用由使用者定義的回呼管理的資源將文件儲存為 HTML 格式
    using (var stream = File.Create(Path.Combine(savingCallbacks.RootFolder, "document.html")))
    {
        document.Save(stream, options);
    }

    //手動將資料附加到 CSS 串流
    using (var writer = new StreamWriter(savingCallbacks.CssStream))
    {
        writer.WriteLine();
        writer.WriteLine("/* This line is appended to stream manually by user */");
    }
}
```

在這裡，我們示範如何使用使用者定義的回呼管理的資源將 OneNote 文件儲存為 HTML 格式。

## 結論

在本文中，我們探討如何使用 Aspose.Note for .NET 處理 OneNote 文件並將其儲存為 HTML 格式。遵循逐步指南，您可以輕鬆地

 將此功能整合到您的 .NET 應用程式中，使您能夠有效率地操作 OneNote 檔案。

## 常見問題解答

### Q1：我可以自訂已儲存的 HTML 檔案的外觀嗎？

A1：是的，您可以透過修改轉換過程中產生的 CSS 樣式表來自訂外觀。

### Q2：Aspose.Note是否支援轉換為HTML以外的其他格式？

A2：是的，Aspose.Note 支援轉換為各種格式，例如 PDF、映像和 Microsoft Word 文件。

### Q3：Aspose.Note 與.NET Core 應用程式相容嗎？

A3：是的，Aspose.Note 與 .NET Framework 和 .NET Core 應用程式相容。

### Q4：我可以使用Aspose.Note從OneNote文件中提取文字和圖像嗎？

A4：是的，您可以使用 Aspose.Note API 提取文字和圖像以及執行各種其他操作。

### Q5：是否有試用版可用來測試Aspose.Note 功能？

 A5：是的，您可以從以下位置下載免費試用版：[這裡](https://releases.aspose.com/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
