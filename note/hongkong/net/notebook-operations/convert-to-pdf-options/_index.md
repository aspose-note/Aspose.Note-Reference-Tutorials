---
title: 使用 Aspose Note .NET 中的選項將筆記本轉換為 PDF
linktitle: 使用 Aspose Note .NET 中的選項將筆記本轉換為 PDF
second_title: Aspose.Note .NET API
description: 了解如何使用具有可自訂選項的 Aspose.Note for .NET 程式庫將 Microsoft OneNote 筆記本轉換為 PDF 格式。
weight: 16
url: /zh-hant/net/notebook-operations/convert-to-pdf-options/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 使用 Aspose Note .NET 中的選項將筆記本轉換為 PDF

## 介紹

在本教學中，我們將逐步介紹使用 Aspose.Note for .NET 函式庫將筆記本轉換為 PDF 格式的過程。 Aspose.Note for .NET 提供了一組強大的功能來以程式設計方式處理 Microsoft OneNote 檔案。

## 先決條件

在我們開始之前，請確保您符合以下先決條件：

### 1..NET 函式庫的 Aspose.Note
確保您已下載並安裝 Aspose.Note for .NET 程式庫。您可以從[網站](https://releases.aspose.com/note/net/).

### 2. 開發環境
您應該設定一個開發環境，例如 Visual Studio，並安裝必要的 .NET 框架。

## 導入命名空間

在我們開始在專案中使用 Aspose.Note for .NET 之前，讓我們匯入所需的命名空間：

```csharp
using System.IO;
using Aspose.Note;
using Aspose.Note.Saving;
using System;
using System.Collections.Generic;
```

現在，讓我們將帶有選項的筆記本轉換為 PDF 的過程分解為多個步驟：

## 第 1 步：載入筆記本

首先，我們需要載入要轉換為 PDF 檔案的 OneNote 筆記本。

```csharp
//文檔目錄的路徑。
string dataDir = "Your Document Directory";

//載入 OneNote 筆記本
var notebook = new Notebook(dataDir + "Notizbuch �ffnen.onetoc2");
```

## 步驟 2：指定 PDF 儲存選項

接下來，我們將指定將筆記本儲存為 PDF 檔案的選項。我們可以自訂各種設置，例如頁面分割演算法、邊距和頁面大小。

```csharp
var notebookSaveOptions = new NotebookPdfSaveOptions();
var documentSaveOptions = notebookSaveOptions.DocumentSaveOptions;

documentSaveOptions.PageSplittingAlgorithm = new KeepSolidObjectsAlgorithm();
```

## 步驟 3：將筆記本儲存為 PDF

現在，我們將使用指定的選項將筆記本儲存為 PDF 檔案。

```csharp
dataDir = dataDir + "ConvertToPDF_out.pdf";

//儲存筆記本
notebook.Save(dataDir, notebookSaveOptions);
```

## 第 4 步：驗證轉換

最後，我們驗證轉換是否成功，並列印PDF文件的儲存位置。

```csharp
Console.WriteLine("\nNoteBook document converted to pdf successfully with save options.\nFile saved at " + dataDir);
```

## 結論

在本教學中，我們學習如何使用 Aspose.Note for .NET 函式庫將 OneNote 筆記本轉換為 PDF 格式。透過執行上述步驟，您可以輕鬆地將此功能整合到您的 .NET 應用程式中。

## 常見問題解答

### Q1：Aspose.Note for .NET 是否與所有版本的 Microsoft OneNote 相容？

A1：是的，Aspose.Note for .NET 支援各種版本的 Microsoft OneNote，包括 .one 和 .onetoc2 格式。

### Q2：我可以自訂 PDF 輸出的外觀嗎？

A2：是的，您可以指定頁面大小、邊距和頁面分割演算法等各種選項來自訂 PDF 輸出的外觀。

### Q3：Aspose.Note for .NET 是否提供對其他檔案格式的支援？

A3：是的，Aspose.Note for .NET 支援轉換為各種其他格式，例如映像、HTML 和 Microsoft Word 文件。

### 問題 4：Aspose.Note for .NET 是否有免費試用版？

A4：是的，您可以從網站下載 Aspose.Note for .NET 的免費試用版，以便在購買前評估其功能。

### Q5：如何獲得 Aspose.Note for .NET 的技術支援？

 A5：您可以透過造訪 Aspose.Note for .NET 獲得技術支持[Aspose.Note 論壇](https://forum.aspose.com/c/note/28)或直接聯絡 Aspose 支援團隊。
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
