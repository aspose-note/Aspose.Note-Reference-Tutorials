---
title: 反白顯示 Aspose.Note 文字中的所有最新更改
linktitle: 反白顯示 Aspose.Note 文字中的所有最新更改
second_title: Aspose.Note .NET API
description: 使用 Aspose.Note for .NET 增強您的 Note 文件！透過此逐步教程，了解如何突出顯示文字中最近的變更。
weight: 19
url: /zh-hant/net/text-manipulation/highlight-recent-changes/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 反白顯示 Aspose.Note 文字中的所有最新更改

## 介紹
您是否希望使用 .NET 為您的 Note 文件添加動態且具有視覺吸引力的功能？ Aspose.Note for .NET 是一個功能強大的解決方案，可讓您無縫地操作並增強您的 Note 檔案。在本教程中，我們將深入研究一個特定方面：突出顯示 Aspose.Note 文字中的所有最新變更。
## 先決條件
在我們開始這趟旅程之前，請確保您具備以下先決條件：
-  Aspose.Note for .NET：確保您已安裝 Aspose.Note 函式庫。您可以從[.NET 文件的 Aspose.Note](https://reference.aspose.com/note/net/).
- 開發環境：設定.NET開發環境，包括Visual Studio等IDE。
- 範例文件：準備一個包含要反白的文字的註解文件（在本例中為「Aspose.one」）。
## 導入命名空間
首先，在 .NET 專案中導入必要的命名空間：
```csharp
    using System;
    using System.Drawing;
    using System.IO;
    using System.Linq;
```
## 第 1 步：載入文檔
首先將 Note 文件載入到 Aspose.Note 中：
```csharp
string dataDir = "Your Document Directory";
Document document = new Document(dataDir + "Aspose.one");
```
## 第 2 步：確定最近的變化
接下來，識別上週修改的 RichText 節點：
```csharp
var richTextNodes = document.GetChildNodes<RichText>().Where(e => e.LastModifiedTime >= DateTime.Today.Subtract(TimeSpan.FromDays(7)));
```
## 第 3 步：設定突出顯示顏色
現在，設定已識別節點和文字運行的突出顯示顏色：
```csharp
foreach (var node in richTextNodes)
{
    //設定段落的突出顯示顏色
    node.ParagraphStyle.Highlight = Color.DarkGreen;
    //為每個文字運行設定突出顯示顏色
    foreach (var run in node.TextRuns)
    {
        run.Style.Highlight = Color.DarkSeaGreen;
    }
}
```
## 第四步：儲存修改後的文檔
儲存突出顯示的最近更改的文件：
```csharp
document.Save(Path.Combine(dataDir, "HighlightAllRecentChanges.pdf"));
```
## 步驟5：顯示成功訊息
最後，顯示成功訊息以通知用戶：
```csharp
Console.WriteLine("\nText's recent changes are highlighted successfully.");
```
## 結論
在本教學中，我們探討如何使用 Aspose.Note for .NET 來反白 Note 文件中文字中的所有最新變更。此功能增強了文件可見性，並且是處理 Note 文件的工具包的寶貴補充。
## 常見問題解答
### 我可以在不同的時間段應用不同的突出顯示顏色嗎？
是的，您可以根據您的特定要求自訂程式碼以設定不同的突出顯示顏色。
### Aspose.Note 與最新的.NET 框架相容嗎？
Aspose.Note 會定期更新其程式庫，以確保與最新的 .NET 框架相容。
### 實現此功能時如何處理錯誤？
您可以合併 try-catch 區塊來處理異常並提供流暢的使用者體驗。
### Aspose.Note 是否支援其他文字格式化功能？
絕對地！ Aspose.Note 提供了廣泛的文字格式化功能，包括字體樣式、大小等。
### 我可以將此解決方案整合到 Web 應用程式中嗎？
是的，您可以將 Aspose.Note for .NET 整合到 Web 應用程式中以增強文件處理能力。
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
