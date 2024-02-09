---
title: 在 Aspose.Note 中對文字套用編號
linktitle: 在 Aspose.Note 中對文字套用編號
second_title: Aspose.Note .NET API
description: 透過這個綜合教程，了解如何在 Aspose.Note for .NET 中套用文字編號。輕鬆增強文件格式。
type: docs
weight: 12
url: /zh-hant/net/text-manipulation/apply-numbering-on-text/
---
## 介紹
Aspose.Note for .NET 為 C# 應用程式中的文件操作提供了強大的工具。在本教程中，我們將探索使用 Aspose.Note 在文字上套用編號的過程。請按照這些逐步說明輕鬆增強文件格式。
## 先決條件
在深入學習本教程之前，請確保您具備以下先決條件：
- 對 C# 程式語言有基本了解。
- 已安裝 Aspose.Note for .NET。你可以下載它[這裡](https://releases.aspose.com/note/net/).
- 整合開發環境 (IDE)，例如 Visual Studio。
## 導入命名空間
首先，請確保在 C# 專案中匯入必要的命名空間：
```csharp
using System;
using System.Globalization;
using System.IO;
using Aspose.Note;
using System.Drawing;
using System.Collections.Generic;
```
## 第 1 步：設定您的文檔
首先建立一個新文件並初始化所需的物件：
```csharp
//文檔目錄的路徑。
string dataDir = "Your Document Directory";
//建立Document類別的對象
Document doc = new Document();
//初始化Page類別物件
Aspose.Note.Page page = new Aspose.Note.Page(doc);
//初始化 Outline 類別對象
Outline outline = new Outline(doc);
```
## 第 2 步：定義預設樣式
使用 ParagraphStyle 類別設定文字的預設樣式：
```csharp
ParagraphStyle defaultStyle = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
```
## 第 3 步：應用編號
初始化 OutlineElement 類別物件並對每個元素套用編號：
```csharp
OutlineElement outlineElem1 = new OutlineElement(doc) { NumberList = new NumberList("{0})", NumberFormat.DecimalNumbers, "Arial", 10) };
RichText text1 = new RichText(doc) { Text = "First", ParagraphStyle = defaultStyle };
outlineElem1.AppendChildLast(text1);
OutlineElement outlineElem2 = new OutlineElement(doc) { NumberList = new NumberList("{0})", NumberFormat.DecimalNumbers, "Arial", 10) };
RichText text2 = new RichText(doc) { Text = "Second", ParagraphStyle = defaultStyle };
outlineElem2.AppendChildLast(text2);
OutlineElement outlineElem3 = new OutlineElement(doc) { NumberList = new NumberList("{0})", NumberFormat.DecimalNumbers, "Arial", 10) };
RichText text3 = new RichText(doc) { Text = "Third", ParagraphStyle = defaultStyle };
outlineElem3.AppendChildLast(text3);
```
## 第 4 步：新增輪廓元素
將大綱元素附加到大綱中：
```csharp
outline.AppendChildLast(outlineElem1);
outline.AppendChildLast(outlineElem2);
outline.AppendChildLast(outlineElem3);
```
## 第 5 步：儲存文檔
使用已套用的編號儲存 OneNote 文件：
```csharp
dataDir = dataDir + "ApplyNumberingOnText_out.one"; 
doc.Save(dataDir);
Console.WriteLine("\nNumbering applied successfully on a text.\nFile saved at " + dataDir); 
```
## 結論
恭喜！您已成功學習如何在 Aspose.Note for .NET 中對文字套用編號。嘗試不同的格式選項，輕鬆建立具有視覺吸引力的文件。
## 常見問題解答
### 1.我可以自訂編號格式嗎？
是的，NumberList 類別可讓您根據自己的喜好自訂編號格式。
### 2. 還有其他可用的格式選項嗎？
Aspose.Note 提供了廣泛的格式選項，包括字體樣式、顏色等。
### 3. Aspose.Note 與 Visual Studio 相容嗎？
絕對地！ Aspose.Note 與 Visual Studio 無縫集成，提供流暢的開發體驗。
### 4. 我可以在購買前試用Aspose.Note嗎？
當然！您可以探索免費試用[這裡](https://releases.aspose.com/).
### 5. 我可以在哪裡獲得Aspose.Note的支援？
如需任何協助或疑問，請訪問[Aspose.Note 論壇](https://forum.aspose.com/c/note/28).