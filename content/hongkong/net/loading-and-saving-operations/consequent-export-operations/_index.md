---
title: Aspose.Note 中的後續匯出操作
linktitle: Aspose.Note 中的後續匯出操作
second_title: Aspose.Note .NET API
description: 了解如何在 Aspose.Note for .NET 中執行後續匯出操作，以有效地以不同格式儲存 OneNote 文件。
type: docs
weight: 10
url: /zh-hant/net/loading-and-saving-operations/consequent-export-operations/
---
## 介紹

在本教程中，我們將深入研究使用 Aspose.Note for .NET 執行後續匯出操作。 Aspose.Note 是一個功能強大的函式庫，使開發人員能夠以程式設計方式處理 Microsoft OneNote 檔案。將文件匯出為不同的格式是常見的要求，Aspose.Note 有效地簡化了這項任務。讓我們逐步探索如何以各種格式儲存文件。

## 先決條件

在繼續本教學之前，請確保您具備以下條件：

1. 對 C# 程式語言有基本了解。
2. Visual Studio 安裝在您的系統上。
3. Aspose.Note for .NET 函式庫整合到您的專案中。

## 導入命名空間

首先，請確保在 C# 程式碼中匯入必要的命名空間：

```csharp
using System.IO;
using Aspose.Note;
using System;
using System.Drawing;
using System.Globalization;
```

## 步驟1：初始化文檔

首先，初始化一個新的`Document`停用自動佈局變更偵測的物件：

```csharp
Document doc = new Document() { AutomaticLayoutChangesDetectionEnabled = false };
```

## 第 2 步：初始化新頁面

創建一個新的`Page`物件並指定其屬性：

```csharp
Aspose.Note.Page page = new Aspose.Note.Page(doc);
```

## 第三步：設定頁面標題

定義頁面標題以及日期和時間資訊：

```csharp
ParagraphStyle textStyle = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
page.Title = new Title(doc)
{
    TitleText = new RichText(doc) { Text = "Title text.", ParagraphStyle = textStyle },
    TitleDate = new RichText(doc) { Text = new DateTime(2011, 11, 11).ToString("D", CultureInfo.InvariantCulture), ParagraphStyle = textStyle },
    TitleTime = new RichText(doc) { Text = "12:34", ParagraphStyle = textStyle }
};
```

## 第4步：追加頁面節點

將頁面節點新增至文件：

```csharp
doc.AppendChildLast(page);
```

## 步驟 5：以不同格式儲存文檔

現在，以各種格式儲存 OneNote 文件：

```csharp
string dataDir = "Your Document Directory";
doc.Save(dataDir + "ConsequentExportOperations_out.html");            
doc.Save(dataDir + "ConsequentExportOperations_out.pdf");            
doc.Save(dataDir + "ConsequentExportOperations_out.jpg");            
textStyle.FontSize = 11;           
doc.DetectLayoutChanges();            
doc.Save(dataDir + "ConsequentExportOperations_out.bmp");
```

## 結論

總之，我們學習如何使用 Aspose.Note for .NET 執行後續導出操作。透過遵循本教學中概述的步驟，您可以無縫地以各種格式儲存 OneNote 文檔，從而增強應用程式的多功能性。

## 常見問題解答

### Q1：我可以進一步自訂頁面標題嗎？

A1: 是的，您可以在儲存文件之前根據您的要求修改標題文字、日期和時間。

### Q2：如何處理佈局變更檢測？

 A2：如圖所示，您可以使用以下命令手動偵測佈局更改`DetectLayoutChanges()`Aspose.Note提供的方法。

### Q3：Aspose.Note 是否支援除上述格式之外的其他匯出格式？

A3：是的，Aspose.Note 支援多種匯出格式，包括 DOCX、PNG、TIFF 等。

### Q4：Aspose.Note 與.NET Core 相容嗎？

A4：是的，Aspose.Note 相容於 .NET Framework 和 .NET Core 環境。

### Q5：在哪裡可以找到更多 Aspose.Note 資源和支援？

A5：您可以造訪 Aspose.Note 文件和論壇以獲得全面的指南、教學和社群支援。