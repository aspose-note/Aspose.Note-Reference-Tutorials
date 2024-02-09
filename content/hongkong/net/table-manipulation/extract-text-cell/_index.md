---
title: 從 Aspose.Note 中的表格單元格中提取文本
linktitle: 從 Aspose.Note 中的表格單元格中提取文本
second_title: Aspose.Note .NET API
description: 了解如何從 Aspose.Note for .NET 中的表格儲存格中提取文字。輕鬆增強您的文件處理能力。
type: docs
weight: 13
url: /zh-hant/net/table-manipulation/extract-text-cell/
---
## 介紹

在本教程中，我們將深入研究使用 Aspose.Note for .NET 從表格單元格中提取文字的過程。表格通常在文件中用於組織訊息，並且能夠從特定單元格中提取文字對於各種應用程式非常有用。

## 先決條件

在我們繼續之前，請確保您具備以下條件：

- C# 程式語言的基礎知識。
- 安裝了 Visual Studio IDE。
- 已安裝 Aspose.Note for .NET 函式庫。
- 包含表格的範例文件（例如“Sample1.one”）。

## 導入命名空間

在開始編碼之前，讓我們匯入必要的命名空間來存取 Aspose.Note 提供的功能：

```csharp
using System.IO;
using Aspose.Note;
using System;
using System.Collections.Generic;
using System.Linq;
```

## 第 1 步：載入文檔

首先，我們需要載入包含要從中提取文字的表格的文件。確保更換`"Your Document Directory"`與文檔目錄的實際路徑。

```csharp
string dataDir = "Your Document Directory";
Document document = new Document(dataDir + "Sample1.one");
```

## 第二步：取得表節點

接下來，我們從載入的文檔中檢索表格節點清單。

```csharp
IList<Table> nodes = document.GetChildNodes<Table>();
```

## 第 3 步：迭代表、行和儲存格

現在，我們將循環遍歷每個表、行和單元格以提取文字。

```csharp
foreach (Table table in nodes)
{
    foreach (TableRow row in table)
    {
        foreach (TableCell cell in row)
        {
            //從每個單元格中檢索文本
            string text = string.Join(Environment.NewLine, cell.GetChildNodes<RichText>().Select(e => e.Text)) + Environment.NewLine;

            //列印提取的文本
            Console.WriteLine(text);
        }
    }
}
```

## 結論

在本教程中，我們探索了使用 Aspose.Note for .NET 從表格單元格中提取文字的過程。透過執行這些步驟，您可以有效地從文件中的表格中檢索文本，從而啟用資料提取和分析等各種應用程式。

## 常見問題解答

### Q1：Aspose.Note 可以處理有合併儲存格的表格嗎？

A1：是的，Aspose.Note 可以無縫處理帶有合併單元格的表格，讓您可以準確地提取文字。

### Q2：是否可以將文字格式與文字內容一起擷取？

A2：當然，Aspose.Note 提供了豐富的功能來在文字擷取過程中保留文字格式。

### Q3：Aspose.Note 是否支援除.one 之外的其他文件格式？

A3：是的，Aspose.Note 支援各種文件格式，包括 .one、.onenote、.onepkg 和 .pdf。

### Q4：我可以自訂提取過程以僅包含特定的表格單元格嗎？

A4：是的，您可以根據您的要求自訂提取過程，允許從特定單元格中選擇性地提取文字。

### Q5：Aspose.Note 適合個人和商業用途嗎？

A5：是的，Aspose.Note 提供適合個人和商業用途的授權選項，提供靈活性和可擴充性。