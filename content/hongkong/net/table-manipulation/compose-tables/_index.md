---
title: 使用 Aspose.Note 撰寫表格
linktitle: 使用 Aspose.Note 撰寫表格
second_title: Aspose.Note .NET API
description: 了解如何使用 Aspose.Note for .NET 撰寫包含富文本內容的結構化表格。輕鬆增強文件的組織性和可讀性。
type: docs
weight: 11
url: /zh-hant/net/table-manipulation/compose-tables/
---
## 介紹

表格是文件的基本組成部分，可實現資訊的結構化呈現。 Aspose.Note for .NET 提供了強大的工具來輕鬆地編寫表格。在本教學中，我們將引導您完成使用 Aspose.Note 建立具有富文本內容的表格的過程。

## 先決條件

在使用 Aspose.Note for .NET 深入研究表組成之前，請確保您符合以下先決條件：

1. 環境設定：確保您擁有使用 .NET Framework 或 .NET Core 設定的合適的開發環境。
2. 安裝：從下列位置下載並安裝 Aspose.Note for .NET[網站](https://releases.aspose.com/note/net/).
3. 基礎知識：熟悉 C# 程式設計和文件操作的基本概念。

## 導入命名空間

在開始組合表之前，請確保匯入必要的命名空間：

```csharp
using System;
using System.Drawing;
using System.IO;
using System.Linq;
```

讓我們將提供的範例分解為可管理的步驟：

## 第 1 步：設定文檔目錄

在建立表格之前，定義儲存文件的目錄。

```csharp
string dataDir = "Your Document Directory";
```

## 第 2 步：建立標題文本

使用特定樣式定義標題文本，例如字體大小和粗體。

```csharp
var headerText = new RichText() { ParagraphStyle = new ParagraphStyle() { FontSize = 18, IsBold = true }, Alignment = HorizontalAlignment.Center }
					.Append("Super contest for suppliers.");
```

## 第 3 步：建立頁面和大綱

初始化頁面和大綱以建立內容。

```csharp
var page = new Page();
var outline = page.AppendChildLast(new Outline() { HorizontalOffset = 50 });
outline.AppendChildLast(new OutlineElement()).AppendChildLast(headerText);
```

## 第 4 步：新增摘要文本

在表格前面新增摘要文字。

```csharp
var bodyTextHeader = outline.AppendChildLast(new OutlineElement()).AppendChildLast(new RichText() { ParagraphStyle = ParagraphStyle.Default });
bodyTextHeader.Append("This is the final ranking of proposals got from our suppliers.");
```

## 第5步：建立表

初始化表以按行和列組織資料。

```csharp
var ranking = outline.AppendChildLast(new OutlineElement()).AppendChildLast(new Table());
```

## 第 6 步：新增標題行

使用包含列標題的標題行填入表格。

```csharp
var headerRow = ranking.AppendChildFirst(new TableRow());
foreach (var header in new[] { "Supplier", "Contacts", "Score A", "Score B", "Score C", "Final score", "Attached materials", "Comments" })
{
   ranking.Columns.Add(new TableColumn());
   headerRow.AppendChildLast(new TableCell() { BackgroundColor = backGroundColor })
			 .AppendChildLast(new OutlineElement())
			 .AppendChildLast(new RichText() { ParagraphStyle = headerStyle })
			 .Append(header);
}
```

## 步驟 7：新增空白行

插入空白行以準備資料插入。

```csharp
for (int i = 0; i < 5; i++)
{
   backGroundColor = backGroundColor.IsEmpty ? Color.LightGray : Color.Empty;
   var row = ranking.AppendChildLast(new TableRow());
   for (int j = 0; j < ranking.Columns.Count(); j++)
   {
	   row.AppendChildLast(new TableCell() { BackgroundColor = backGroundColor })
		  .AppendChildLast(new OutlineElement())
		  .AppendChildLast(new RichText() { ParagraphStyle = ParagraphStyle.Default });
   }
}
```

## 第 8 步：新增聯絡訊息

使用範本內容填入「聯絡人」列。

```csharp
foreach (var row in ranking.Skip(1))
{
   var contactsCell = row.ElementAt(1);
   contactsCell.AppendChildLast(new OutlineElement())
			   .AppendChildLast(new RichText() { ParagraphStyle = ParagraphStyle.Default })
			   .Append("Web: ").Append("link", new TextStyle() { HyperlinkAddress = "www.link.com", IsHyperlink = true });
   contactsCell.AppendChildLast(new OutlineElement())
			   .AppendChildLast(new RichText() { ParagraphStyle = ParagraphStyle.Default })
			   .Append("E-mail: ").Append("mail", new TextStyle() { HyperlinkAddress = "mailto:hi@link.com", IsHyperlink = true });
}
```

## 第9步：儲存文檔

儲存組成的表格文件。

```csharp
var d = new Document();
d.AppendChildLast(page);
d.Save(Path.Combine(dataDir, "ComposeTable_out.one"));
```

## 第10步：確認

確認文件撰寫成功。

```csharp
Console.WriteLine("\nThe document is composed successfully.");
```

## 結論

在本教學中，我們探討如何使用 Aspose.Note for .NET 撰寫具有富文本內容的表格。透過遵循這些逐步說明，您可以在文件中有效地建立結構化表格，從而增強可讀性和組織性。

## 常見問題解答

### Q1：我可以自訂表格元素的樣式嗎？
   
A1: 是的，您可以自訂各個方面，例如字體大小、顏色和對齊方式，以滿足您的要求。

### Q2：Aspose.Note 與其他.NET 函式庫相容嗎？
   
A2：Aspose.Note 與其他 .NET 函式庫無縫集成，為文件操作提供了廣泛的靈活性。

### Q3：Aspose.Note 支援將表格匯出為不同格式嗎？
   
A3：當然，Aspose.Note 允許您將表格匯出為各種格式，包括 PDF、DOCX 和 HTML。

### 問題 4：我可以使用外部來源的資料動態填入表嗎？
   
A4：是的，您可以透過從資料庫、API 或使用者輸入以取得資料來動態填入資料表。

### Q5：Aspose.Note 使用者可以獲得技術支援嗎？
   
A5：是的，Aspose 透過其論壇和專用支援管道提供全面的技術支援。