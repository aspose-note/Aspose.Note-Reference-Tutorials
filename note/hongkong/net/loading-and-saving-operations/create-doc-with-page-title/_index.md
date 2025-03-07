---
title: 在 Aspose.Note 中建立帶有頁面標題的文檔
linktitle: 在 Aspose.Note 中建立帶有頁面標題的文檔
second_title: Aspose.Note .NET API
description: 了解如何使用 Aspose.Note for .NET 建立具有標題頁面的文件。請按照我們的逐步指南進行無縫整合。
weight: 13
url: /zh-hant/net/loading-and-saving-operations/create-doc-with-page-title/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 在 Aspose.Note 中建立帶有頁面標題的文檔

## 介紹

在本教學中，我們將引導您完成使用 Aspose.Note for .NET 建立具有標題頁面的文件的過程。 Aspose.Note 是一個功能強大的 API，可讓開發人員以程式設計方式處理 Microsoft OneNote 檔案。

## 先決條件

在開始之前，請確保您已安裝並設定以下先決條件：

### 視覺工作室安裝

1. 下載 Visual Studio：如果尚未安裝，請從 Microsoft 網站下載並安裝 Visual Studio。

2. 安裝 .NET 開發工作負載：在安裝過程中，請務必選擇「.NET 桌面開發」工作負載，以確保您擁有 .NET 開發所需的所有元件。

3. 建立新專案：開啟 Visual Studio 並建立一個新專案（控制台應用程式或您喜歡的任何其他類型）。

### Aspose.Note安裝

1. 取得 Aspose.Note：從下列位置下載 Aspose.Note for .NET 函式庫[網站](https://releases.aspose.com/note/net/).

2. 透過 NuGet 安裝 Aspose.Note：或者，您可以透過 Visual Studio 中的 NuGet 套件管理器安裝 Aspose.Note for .NET。只需搜尋“Aspose.Note”並安裝最新版本。

## 導入命名空間

首先，您需要匯入必要的命名空間以在專案中使用 Aspose.Note。

```csharp
using System.IO;
using Aspose.Note;
using Aspose.Note.Saving;
using System;
using System.Drawing;
using System.Globalization;
```

現在，讓我們將建立具有頁面標題的文件的過程分解為多個步驟：

## 第 1 步：建立文檔對象

```csharp
//建立Document類別的對象
Document doc = new Aspose.Note.Document();
```

## 第2步：初始化頁面類別對象

```csharp
//初始化Page類別物件
Aspose.Note.Page page = new Aspose.Note.Page(doc);
```

## 第 3 步：設定文字的預設樣式

```csharp
//文件中所有文字的預設樣式。
ParagraphStyle textStyle = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
```

## 步驟 4：設定頁面標題屬性

```csharp
//設定頁面標題屬性
page.Title = new Title(doc)
{
    TitleText = new RichText(doc) { Text = "Title text.", ParagraphStyle = textStyle },
    TitleDate = new RichText(doc) { Text = new DateTime(2011, 11, 11).ToString("D", CultureInfo.InvariantCulture), ParagraphStyle = textStyle },
    TitleTime = new RichText(doc) { Text = "12:34", ParagraphStyle = textStyle }
};
```

## 步驟5：在文件中追加頁面節點

```csharp
//在文件中追加頁面節點
doc.AppendChildLast(page);
```

## 步驟 6：儲存 OneNote 文檔

```csharp
//儲存 OneNote 文檔
string dataDir = "Your Document Directory";
dataDir = dataDir + "CreateDocWithPageTitle_out.one";
doc.Save(dataDir);
```

## 結論

恭喜！您已使用 Aspose.Note for .NET 成功建立了具有標題頁面的文件。本教學提供了逐步指南，可協助您將 Aspose.Note 整合到 .NET 應用程式中，以便以程式設計方式管理 OneNote 檔案。

## 常見問題解答

### Q1：我可以自訂標題文字樣式嗎？

A1: 是的，您可以根據您的要求自訂標題文字的字體顏色、字體名稱和字體大小。

### Q2：Aspose.Note 與.NET Core 相容嗎？

A2：是的，Aspose.Note 支援.NET Core，讓您開發跨平台應用程式。

### Q3：我可以在文件中新增圖片和附件嗎？

A3：當然！ Aspose.Note 提供 API 來將圖像、附件和其他元素無縫添加到 OneNote 文件中。

### Q4：Aspose.Note支援讀取現有的OneNote檔案嗎？

A4：是的，您可以使用Aspose.Note輕鬆讀取、修改和操作現有的OneNote檔案。

### Q5：如果遇到任何問題，我可以在哪裡尋求支援？

A5：您可以在以下位置找到支援和協助：[Aspose.Note 論壇](https://forum.aspose.com/c/note/28)，專家和社群成員可以幫助您解答疑問。
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
