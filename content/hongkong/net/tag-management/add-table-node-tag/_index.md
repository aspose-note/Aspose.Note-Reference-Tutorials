---
title: 在Aspose.Note中新增帶有標籤的表節點
linktitle: 在Aspose.Note中新增帶有標籤的表節點
second_title: Aspose.Note .NET API
description: 了解如何在 Aspose.Note for .NET 中新增帶有標籤的表格。以程式設計方式增強您的文件操作技能。
type: docs
weight: 11
url: /zh-hant/net/tag-management/add-table-node-tag/
---
## 介紹

在本教學中，我們將引導您完成使用 Aspose.Note for .NET 新增帶有標籤的表格節點的過程。請按照以下步驟來實現此目的。

## 導入命名空間

在開始之前，請確保匯入必要的命名空間以使用 Aspose.Note：

```csharp
using System.Drawing;
using System.IO;
using Aspose.Note;
using System;
using System.Collections.Generic;
using Aspose.Note.Examples.CSharp.Tables;
```

## 先決條件

在繼續之前，請確保您已設定以下先決條件：

1. 安裝：下載並安裝 Aspose.Note for .NET 函式庫[這裡](https://releases.aspose.com/note/net/).
2. 許可證：取得許可證或使用[臨時執照](https://purchase.aspose.com/temporary-license/)使用圖書館。
3. 開發環境：設定相容的開發環境，例如 Visual Studio。

## 第 1 步：初始化文件和頁面對象

首先建立一個實例`Document`類別並初始化`Page`目的：

```csharp
Document doc = new Document();
Aspose.Note.Page page = new Aspose.Note.Page(doc);
```

## 第 2 步：建立表格、行和單元格對象

初始化`Table`, `TableRow`， 和`TableCell`對象：

```csharp
TableRow row = new TableRow(doc);
TableCell cell = new TableCell(doc);
```

## 第 3 步：將內容插入儲存格

使用以下命令將內容新增至儲存格`AppendChildLast`方法：

```csharp
cell.AppendChildLast(InsertTable.GetOutlineElementWithText(doc, "Single cell."));
```

## 第四步：初始化表節點

初始化`Table`具有指定屬性的物件：

```csharp
Table table = new Table(doc)
{
    IsBordersVisible = true,
    Columns = { new TableColumn { Width = 70 } }
};
```

## 第 5 步：將行加入表中

將行節點加入表中：

```csharp
table.AppendChildLast(row);
```

## 第六步：為表節點新增標籤

包括表節點的標籤：

```csharp
table.Tags.Add(NoteTag.CreateQuestionMark());
```

## 步驟7：將表格節點加入大綱元素

創建一個`Outline`和`OutlineElement`新增表節點：

```csharp
Outline outline = new Outline(doc);
OutlineElement outlineElem = new OutlineElement(doc);
outlineElem.AppendChildLast(table);
outline.AppendChildLast(outlineElem);
page.AppendChildLast(outline);
doc.AppendChildLast(page);
```

## 第 8 步：儲存文檔

儲存 OneNote 文件：

```csharp
string dataDir = "Your Document Directory";
dataDir = dataDir + "AddTableNodeWithTag_out.one";
doc.Save(dataDir);
Console.WriteLine("\nTable node with tag added successfully.\nFile saved at " + dataDir);
```

執行這些步驟後，您應該已經使用 Aspose.Note for .NET 成功新增了帶有標籤的表節點。

## 結論

在本教學中，我們介紹了在 Aspose.Note for .NET 中新增帶有標籤的表格節點的過程。透過執行以下步驟，您可以以程式設計方式有效地操作 OneNote 文檔，從而增強您的文檔管理能力。

## 常見問題解答

### Q1：Aspose.Note 是否相容於所有版本的.NET？

A1：Aspose.Note for .NET 支援 .NET Framework 2.0 以上版本，包括 .NET Core 和 .NET Standard。

### Q2：我可以在購買許可證之前試用 Aspose.Note 嗎？

 A2：是的，您可以獲得 Aspose.Note 的免費試用版[這裡](https://releases.aspose.com/).

### Q3：如何取得 Aspose.Note 的臨時授權？

 A3：您可以從以下地點獲得臨時許可證：[這個連結](https://purchase.aspose.com/temporary-license/)，有效期限為 30 天。

### Q4：Aspose.Note支援文檔加密嗎？

A4：是的，Aspose.Note提供了對OneNote文件加密的支持，以確保資料安全。

### Q5：Aspose.Note 使用者可以獲得技術支援嗎？

 A5：是的，透過 Aspose 論壇提供技術支持[這裡](https://forum.aspose.com/c/note/28)，您可以在這裡尋求專家的協助。