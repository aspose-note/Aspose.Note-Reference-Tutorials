---
title: 在 Aspose.Note 中儲存為 PDF
linktitle: 在 Aspose.Note 中儲存為 PDF
second_title: Aspose.Note .NET API
description: 了解如何使用 Aspose.Note for .NET 將 Microsoft OneNote 文件儲存為 PDF 格式。包含 Letter 和 A4 頁面佈局程式碼範例的逐步教學。
type: docs
weight: 26
url: /zh-hant/net/loading-and-saving-operations/save-to-pdf/
---
## 介紹

在本教學中，我們將探討如何使用 Aspose.Note for .NET 將文件儲存為 PDF 格式。 Aspose.Note 是一個功能強大的函式庫，使開發人員能夠以程式設計方式處理 Microsoft OneNote 檔案。我們將介紹先決條件、匯入命名空間，並提供將文件儲存為各種頁面佈局的 PDF 的逐步指南。

## 先決條件

在我們開始之前，請確保您具備以下條件：

- Visual Studio 安裝在您的系統上。
- 下載並安裝了 Aspose.Note for .NET 函式庫。您可以從以下位置下載：[這裡](https://releases.aspose.com/note/net/).
- C# 程式語言的基礎知識。

## 導入命名空間

首先，讓我們將必要的命名空間匯入到我們的 C# 程式碼中：

```csharp
using System;
using System.IO;

using Aspose.Note.Saving;
```

現在我們已經滿足了先決條件並匯入了命名空間，讓我們繼續以不同的頁面佈局將文件儲存為 PDF。

## 第 1 步：使用 Letter 頁面設定儲存為 PDF


```csharp
public static void SaveToPdfUsingLetterPageSettings()
{
    //文檔目錄的路徑。
    string dataDir = "Your Document Directory";

    //將文件載入到 Aspose.Note 中。
    Document oneFile = new Document(dataDir + "OneNote.one");

    var dst = Path.Combine(dataDir, "SaveToPdfUsingLetterPageSettings.pdf");

    //儲存文檔。
    oneFile.Save(dst, new PdfSaveOptions() { PageSettings = PageSettings.Letter });

    Console.WriteLine("\nOneNote document saved successfully.\nFile saved at " + dst);
}
```

### 解釋：

- 我們將 OneNote 文件載入到 Aspose.Note 中。
- 定義已儲存的 PDF 檔案的目標路徑。
- 使用以下命令將文件儲存為 PDF`PdfSaveOptions`和`PageSettings`設定`Letter`.

## 步驟 2：使用無高度限制的 A4 頁面設定儲存為 PDF

```csharp
public static void SaveToPdfUsingA4PageSettingsWithoutHeightLimit()
{
    //文檔目錄的路徑。
    string dataDir = "Your Document Directory";

    //將文件載入到 Aspose.Note 中。
    Document oneFile = new Document(dataDir + "OneNote.one");

    var dst = Path.Combine(dataDir, "SaveToPdfUsingA4PageSettingsWithoutHeightLimit.pdf");

    //儲存文檔。
    oneFile.Save(dst, new PdfSaveOptions() { PageSettings = PageSettings.A4NoHeightLimit });

    Console.WriteLine("\nOneNote document saved successfully.\nFile saved at " + dst);
}
```

### 解釋：

- 與上一步類似，我們將 OneNote 文件載入到 Aspose.Note 中。
- 定義已儲存的 PDF 檔案的目標路徑。
- 使用以下命令將文件儲存為 PDF`PdfSaveOptions`和`PageSettings`設定`A4NoHeightLimit`.

## 結論

在本教學中，我們學習如何使用 Aspose.Note for .NET 將文件儲存為 PDF 格式。我們介紹了兩種不同的頁面佈局：Letter 和 A4，沒有高度限制。借助 Aspose.Note，開發人員可以輕鬆地以程式設計方式操作 OneNote 文件，從而為文件管理任務提供靈活性和效率。

## 常見問題解答

### Q1：Aspose.Note 可以處理複雜的 OneNote 檔案嗎？

A1：是的，Aspose.Note 支援各種特性和功能來有效處理複雜的 OneNote 檔案。

### Q2：Aspose.Note適合商業項目嗎？

 A2：當然可以，Aspose.Note 可以輕鬆地用於商業項目。您可以購買許可證[這裡](https://purchase.aspose.com/buy).

### Q3：Aspose.Note 提供免費試用嗎？

A3：是的，您可以透過免費試用版探索 Aspose.Note[這裡](https://releases.aspose.com/).

### Q4：在哪裡可以找到 Aspose.Note 的文檔？

 A4：你可以找到詳細的文檔[這裡](https://reference.aspose.com/note/net/).

### Q5: 需要進一步幫忙嗎？

 A5：請隨時在 Aspose.Note 論壇上提出任何問題或尋求支持[這裡](https://forum.aspose.com/c/note/28).