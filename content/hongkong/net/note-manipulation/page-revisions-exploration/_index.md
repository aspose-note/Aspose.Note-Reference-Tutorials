---
title: 探索 Aspose.Note 文件中的頁面修訂
linktitle: 探索 Aspose.Note 文件中的頁面修訂
second_title: Aspose.Note .NET API
description: 了解如何使用 .NET 框架在逐步指導下探索 Aspose.Note 文件中的頁面修訂。
type: docs
weight: 14
url: /zh-hant/net/note-manipulation/page-revisions-exploration/
---
## 介紹

在本教學中，我們將深入探索使用 .NET 框架的 Aspose.Note 文件中的頁面修訂。 Aspose.Note 是一個功能強大的函式庫，使開發人員能夠以程式設計方式處理 Microsoft OneNote 文件，並提供各種功能來操作這些文件並從中提取資料。

## 先決條件

在我們開始之前，請確保您已設定以下先決條件：

### 1. 下載並安裝 Aspose.Note for .NET

參觀[下載頁面](https://releases.aspose.com/note/net/)並下載 Aspose.Note for .NET 函式庫。按照提供的安裝說明在您的開發環境中設定該庫。

### 2. 載入必要的命名空間

請確保在 .NET 專案中匯入所需的命名空間，以無縫存取 Aspose.Note 功能。

```csharp
using System.IO;
using Aspose.Note;
using System;
using System.Collections.Generic;
```

現在，讓我們將探索頁面修訂的過程分解為逐步說明：

## 第 1 步：載入文檔

首先，我們需要載入Aspose.Note文檔，確保啟用文檔歷史記錄的載入。

```csharp
string dataDir = "Your Document Directory";
Document document = new Document(dataDir + "Aspose.one", new LoadOptions { LoadHistory = true });
```

## 第 2 步：檢索頁面修訂

載入文件後，我們可以檢索特定頁面的修訂版本。在此範例中，我們將獲得第一頁的修訂版。

```csharp
Page firstPage = document.FirstChild;
foreach (Page pageRevision in document.GetPageHistory(firstPage))
{
    /*Use pageRevision like a regular page.*/
    Console.WriteLine("LastModifiedTime: {0}", pageRevision.LastModifiedTime);
    Console.WriteLine("CreationTime: {0}", pageRevision.CreationTime);
    Console.WriteLine("Title: {0}", pageRevision.Title);
    Console.WriteLine("Level: {0}", pageRevision.Level);
    Console.WriteLine("Author: {0}", pageRevision.Author);
    Console.WriteLine();
}
```

## 第 3 步：迭代修訂

在循環中，迭代頁面的每個修訂版本並存取其屬性，例如上次修改時間、建立時間、標題、層級和作者。

## 結論

使用 .NET 探索 Aspose.Note 文件中的頁面修訂是一個簡單的過程。透過遵循本教學中概述的步驟，您可以以程式設計方式有效地檢索和分析 OneNote 檔案的修訂歷史記錄。

## 常見問題解答

### Q1：我可以使用 Aspose.Note for .NET 建立新的 OneNote 文件嗎？

A1：是的，Aspose.Note for .NET 可讓您以程式設計方式建立、編輯和操作 OneNote 文件。

### Q2：Aspose.Note 是否支援所有類型的 OneNote 檔案的載入歷史記錄？

A2：Aspose.Note 支援.one 和.onepkg 檔案格式的載入歷史記錄。

### 問題 3：Aspose.Note for .NET 是否有免費試用版？

A3：是的，您可以從以下位置下載 Aspose.Note for .NET 的免費試用版：[這裡](https://releases.aspose.com/).

### Q4：如何取得 Aspose.Note for .NET 的臨時授權？

 A4：您可以向以下機構申請臨時許可證：[這個連結](https://purchase.aspose.com/temporary-license/).

### Q5：在哪裡可以找到 Aspose.Note for .NET 支援？

 A5：您可以在以下位置找到支援和資源：[Aspose.Note 論壇](https://forum.aspose.com/c/note/28).