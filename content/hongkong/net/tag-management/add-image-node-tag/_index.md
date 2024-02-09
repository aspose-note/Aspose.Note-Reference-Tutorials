---
title: 在Aspose.Note中新增帶有標籤的圖片節點
linktitle: 在Aspose.Note中新增帶有標籤的圖片節點
second_title: Aspose.Note .NET API
description: 了解如何使用 Aspose.Note for .NET 新增帶有自訂標籤的映像來增強 OneNote 文件。
type: docs
weight: 10
url: /zh-hant/net/tag-management/add-image-node-tag/
---
## 介紹

在本教學中，我們將探索如何使用 Aspose.Note for .NET 新增帶有標籤的圖片節點。此功能可讓您透過新增帶有自訂標籤的影像來增強 OneNote 文件。

## 先決條件

在開始之前，請確保您具備以下條件：

1. Visual Studio：在您的系統上安裝 Visual Studio IDE。
2.  Aspose.Note for .NET：從下列位置下載並安裝 Aspose.Note for .NET 函式庫：[下載連結](https://releases.aspose.com/note/net/).
3. 基礎知識：熟悉C#程式語言和.NET架構。

## 導入命名空間

首先，確保在 C# 程式碼中包含必要的命名空間：

```csharp
using System.Drawing;
using System.IO;
using Aspose.Note;
using System;
using System.Collections.Generic;
```

## 第 1 步：初始化文件和頁面對象

首先建立一個實例`Document`類別和一個`Page`目的：

```csharp
Document doc = new Document();
Aspose.Note.Page page = new Aspose.Note.Page(doc);
```

## 步驟 2：初始化 Outline 和 OutlineElement 對象

接下來，初始化`Outline`和`OutlineElement`對象：

```csharp
Outline outline = new Outline(doc);
OutlineElement outlineElem = new OutlineElement(doc);
```

## 第 3 步：載入並插入圖像

載入所需的圖像並將其插入到文件節點中：

```csharp
Aspose.Note.Image image = new Aspose.Note.Image(doc, "path_to_your_image.jpg");
outlineElem.AppendChildLast(image);
```

## 第 4 步：向圖像添加標籤

向圖像添加自訂標籤：

```csharp
image.Tags.Add(NoteTag.CreateYellowStar());
```

## 第 5 步：附加大綱元素和頁面節點

將大綱元素和大綱節點附加到頁面：

```csharp
outline.AppendChildLast(outlineElem);
page.AppendChildLast(outline);
```

## 第 6 步：儲存文檔

儲存修改後的 OneNote 文件：

```csharp
doc.AppendChildLast(page);
string outputFilePath = "output_path/AddImageNodeWithTag_out.one";
doc.Save(outputFilePath);
```

## 結論

透過執行這些步驟，您可以使用 Aspose.Note for .NET 無縫添加帶有自訂標籤的圖像節點，從而透過個人化視覺效果豐富您的 OneNote 文件。

## 常見問題解答

### Q1：我可以使用 Aspose.Note 在單一文件中新增多個具有不同標籤的圖片嗎？

A1：是的，您可以透過對每個影像執行類似的步驟來新增具有不同標籤的多個影像。

### Q2：Aspose.Note 是否相容於所有版本的 OneNote？

A2：Aspose.Note支援各種版本的OneNote，確保不同環境下的相容性。

### Q3：我可以自訂新增到圖像中的標籤的外觀嗎？

A3：是的，Aspose.Note 可以靈活地自訂標籤外觀以滿足您的喜好。

### Q4：Aspose.Note 是否支援從 URL 新增圖像？

A4：Aspose.Note 主要支援從本機目錄新增影像，但您可以先將外部影像下載到本機來合併它們。

### Q5：新增的圖片大小或格式有限制嗎？

A5：Aspose.Note支援多種影像格式，並且對影像大小沒有嚴格限制，允許您將不同的視覺效果合併到文件中。