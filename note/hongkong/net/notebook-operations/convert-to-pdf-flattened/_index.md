---
title: 在 Aspose Note .NET 中將筆記本轉換為 PDF（扁平化）
linktitle: 在 Aspose Note .NET 中將筆記本轉換為 PDF（扁平化）
second_title: Aspose.Note .NET API
description: 了解如何使用 Aspose.Note for .NET 輕鬆將 OneNote 筆記本轉換為扁平 PDF。無縫保存您的內容。
weight: 15
url: /zh-hant/net/notebook-operations/convert-to-pdf-flattened/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 在 Aspose Note .NET 中將筆記本轉換為 PDF（扁平化）

## 介紹

您是否希望使用 Aspose Note .NET 將 OneNote 筆記本轉換為扁平 PDF？您來對地方了！在本教程中，我們將逐步演示該過程。

## 先決條件

在我們開始之前，請確保您具備以下條件：

1.  Aspose.Note for .NET：確保您已下載並安裝 Aspose.Note for .NET。如果沒有，您可以從[這裡](https://releases.aspose.com/note/net/).
2. Visual Studio：您需要在系統上安裝 Visual Studio 來進行編碼和編譯。
3. OneNote 筆記本：準備轉換為 PDF 的 OneNote 筆記本。

## 導入命名空間

首先，我們在 C# 程式碼中導入必要的命名空間：

```csharp
using System.IO;
using Aspose.Note;
using Aspose.Note.Saving;
using System;
using System.Collections.Generic;
```

## 第 1 步：載入 OneNote 筆記本

```csharp
//文檔目錄的路徑。
string dataDir = "Your Document Directory";

//載入 OneNote 筆記本
var notebook = new Notebook(dataDir + "Notizbuch �ffnen.onetoc2");
```

在此步驟中，我們使用以下命令載入 OneNote 筆記本`Notebook`Aspose.Note 提供的類別。

## 第 2 步：透過拼合轉換為 PDF

```csharp
//透過拼合將筆記本另存為 PDF
dataDir = dataDir + "ConvertToPDFAsFlattened_out.pdf";
notebook.Save(
    dataDir,
    new NotebookPdfSaveOptions
    {
        Flatten = true
    }); 
```

在這裡，我們將加載的筆記本另存為 PDF，其中包含`Flatten`屬性設定為`true`。此屬性將所有內容（包括註釋和圖像）合併到 PDF 中。

## 步驟3：列印成功訊息

```csharp
Console.WriteLine("\nNoteBook document converted to PDF as flattened successfully.\nFile saved at " + dataDir);
```

最後，我們列印一條成功訊息以及 PDF 的儲存路徑。

## 結論

恭喜！您已使用 Aspose.Note for .NET 成功將 OneNote 筆記本轉換為拼合 PDF。此流程可確保您的所有內容以 PDF 格式準確保存，從而更輕鬆地分享和分發。

## 常見問題解答

### Q1：我可以保留PDF中的互動元素嗎？

A1：Aspose.Note 將內容（包括複選框或表單欄位等互動元素）扁平化到 PDF 中，使它們成為靜態的。

### Q2：Aspose.Note支援將筆記本轉換為其他格式嗎？

A2：是的，Aspose.Note 支援將筆記本轉換為各種格式，例如 PDF、HTML、圖像等。

### Q3：我可以自訂轉換選項嗎？

A3：當然！ Aspose.Note 在轉換過程中提供了廣泛的自訂選項，可讓您根據您的要求自訂輸出。

### Q4：有試用版嗎？

 A4：是的，您可以免費試用 Aspose.Note[這裡](https://releases.aspose.com/).

### Q5：如果遇到任何問題，我可以在哪裡獲得支援？

 A5：您可以透過以下地址尋求 Aspose 社群的支持：[Aspose.Note 論壇](https://forum.aspose.com/c/note/28).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
