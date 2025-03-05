---
title: 使用 Aspose Note .NET 中的選項將筆記本轉換為映像
linktitle: 使用 Aspose Note .NET 中的選項將筆記本轉換為映像
second_title: Aspose.Note .NET API
description: 了解如何使用 Aspose.Note for .NET 將筆記本轉換為具有可自訂選項的映像。
type: docs
weight: 13
url: /zh-hant/net/notebook-operations/convert-to-image-options/
---
## 介紹

在本教程中，我們將深入研究使用 Aspose.Note for .NET 庫將筆記本轉換為具有各種選項的圖像。 Aspose.Note 是一個功能強大的 .NET API，允許開發人員以程式設計方式使用 Microsoft OneNote 檔案。透過遵循本指南中概述的步驟，您將了解如何輕鬆地將筆記本轉換為影像，同時根據您的要求自訂輸出。

## 先決條件

在我們開始之前，請確保您符合以下先決條件：

1. C# 基礎知識：熟悉 C# 程式語言對於理解和實作所提供的程式碼片段至關重要。

2.  Aspose.Note for .NET：從下列位置下載並安裝 Aspose.Note for .NET[網站](https://releases.aspose.com/note/net/)。您可以根據需要取得免費試用版或購買授權。

3. 開發環境：使用 Visual Studio 或任何其他支援 .NET 開發的 IDE 設定您的首選開發環境。

## 導入命名空間

首先，讓我們匯入必要的命名空間以使用 Aspose.Note for .NET。

```csharp
using System.IO;
using Aspose.Note;
using Aspose.Note.Saving;
using System;
using System.Collections.Generic;
```

現在，讓我們將帶有選項的筆記本轉換為圖像的過程分解為多個步驟。

## 第 1 步：載入筆記本

首先，載入要轉換為圖像的筆記本檔案。

```csharp
//文檔目錄的路徑。
string dataDir = "Your Document Directory";

//載入 OneNote 筆記本
var notebook = new Notebook(dataDir + "Notizbuch �ffnen.onetoc2");
```

## 第 2 步：設定影像儲存選項

指定將筆記本儲存為影像的選項。在這裡，我們將圖像格式設為 PNG 並自訂解析度。

```csharp
var notebookSaveOptions = new NotebookImageSaveOptions(SaveFormat.Png);

var documentSaveOptions = notebookSaveOptions.DocumentSaveOptions;

documentSaveOptions.Resolution = 400;
```

## 步驟 3：將筆記本另存為影像

使用指定的選項將筆記本儲存為影像。

```csharp
dataDir = dataDir + "ConvertToImageWithOptions_out.png";

//儲存筆記本
notebook.Save(dataDir, notebookSaveOptions);
```

## 結論

總之，我們探索如何使用 Aspose.Note for .NET 將筆記本轉換為具有各種選項的圖像。透過遵循本教學中概述的步驟，您可以將此功能無縫整合到您的 .NET 應用程式中，從而實現 Microsoft OneNote 檔案的高效操作。

## 常見問題解答

### Q1：我可以使用 Aspose.Note for .NET 同時轉換多本筆記本嗎？

A1：是的，您可以迭代多個筆記本文件，並使用本教程中演示的類似方法將它們轉換為圖像。

### Q2：Aspose.Note for .NET 與 .NET Core 相容嗎？

A2：是的，Aspose.Note for .NET 與 .NET Framework 和 .NET Core 環境相容。

### Q3：轉換為影像的筆記本的尺寸有限制嗎？

A3：Aspose.Note for .NET 不會對可轉換的筆記本的大小施加具體限制，但效能可能會根據筆記本的大小和複雜程度而有所不同。

### Q4：除了解析度設定之外，我還可以進一步自訂影像輸出嗎？

A4：是的，Aspose.Note for .NET 提供了各種自訂影像輸出的選項，例如調整邊距、色彩和壓縮等級。

### Q5：Aspose.Note for .NET 是否支援 PNG 以外的其他圖片格式？

A5：是的，Aspose.Note for .NET 支援多種影像格式，包括 JPEG、BMP、GIF 和 TIFF。