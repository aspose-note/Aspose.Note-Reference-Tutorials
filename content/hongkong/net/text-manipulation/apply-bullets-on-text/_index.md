---
title: 在 Aspose.Note 中的文字上套用項目符號
linktitle: 在 Aspose.Note 中的文字上套用項目符號
second_title: Aspose.Note .NET API
description: 了解如何在 Aspose.Note for .NET 中的文字上套用項目符號以增強您的 OneNote 文件。請按照此逐步指南進行有效的格式化。
type: docs
weight: 10
url: /zh-hant/net/text-manipulation/apply-bullets-on-text/
---
## 介紹
歡迎閱讀本逐步指南，以了解如何使用 Aspose.Note for .NET 將項目符號應用於文字。 Aspose.Note 是一個功能強大的程式庫，可讓開發人員在其 .NET 應用程式中無縫使用 Microsoft OneNote 檔案。在本教程中，我們將引導您完成將項目符號應用於文字的過程，從而增強 OneNote 文件的視覺吸引力。
## 先決條件
在我們深入學習本教程之前，請確保您符合以下先決條件：
- C# 和 .NET 程式設計的基礎知識。
- 已安裝 Aspose.Note for .NET 函式庫。你可以下載它[這裡](https://releases.aspose.com/note/net/).
## 導入命名空間
在您的 C# 程式碼中，確保包含必要的命名空間：
```csharp
using System;
using System.Globalization;
using System.IO;
using Aspose.Note;
using System.Drawing;
using System.Collections.Generic;
```
## 第 1 步：設定您的文檔
```csharp
//文檔目錄的路徑。
string dataDir = "Your Document Directory";
//建立Document類別的對象
Aspose.Note.Document doc = new Aspose.Note.Document();
```
## 步驟2：初始化頁面和大綱
```csharp
//初始化Page類別物件
Aspose.Note.Page page = new Aspose.Note.Page(doc);
//初始化 Outline 類別對象
Outline outline = new Outline(doc);
```
## 步驟 3：設定預設文字樣式
```csharp
//初始化 TextStyle 類別物件並設定格式屬性
ParagraphStyle defaultStyle = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
```
## 第 4 步：使用項目符號建立大綱元素
```csharp
//初始化 OutlineElement 類別物件並套用項目符號
OutlineElement outlineElem1 = new OutlineElement(doc) { NumberList = new NumberList("*", "Arial", 10) };
RichText text1 = new RichText(doc) { Text = "First", ParagraphStyle = defaultStyle };
outlineElem1.AppendChildLast(text1);
//對其他輪廓元素重複此操作
```
## 步驟5：將大綱元素加入大綱中
```csharp
//添加輪廓元素
outline.AppendChildLast(outlineElem1);
//對其他輪廓元素重複此操作
```
## 第 6 步：向頁面新增輪廓
```csharp
//新增輪廓節點
page.AppendChildLast(outline);
```
## 步驟 7：將頁面新增至文檔
```csharp
//新增頁面節點
doc.AppendChildLast(page);
```
## 步驟 8：儲存 OneNote 文檔
```csharp
//儲存 OneNote 文檔
dataDir = dataDir + "ApplyBulletsOnText_out.one"; 
doc.Save(dataDir);
Console.WriteLine("\nBullets applied successfully on a text.\nFile saved at " + dataDir); 
```
## 結論
恭喜！您已成功學習如何使用 Aspose.Note for .NET 將項目符號套用至文字。此功能可顯著增強 OneNote 文件的格式，使它們在視覺上更具吸引力。
## 常見問題解答
### 我可以對清單中的每個項目套用不同的項目符號樣式嗎？
是的，您可以透過修改來自訂項目符號樣式`NumberList`每個屬性`OutlineElement`.
### Aspose.Note 與最新版本的 Microsoft OneNote 相容嗎？
Aspose.Note支援各種版本的Microsoft OneNote，確保與舊版和新版本的兼容性。
### 我可以將 Aspose.Note 用於商業目的嗎？
是的，您可以在商業專案中使用 Aspose.Note for .NET。要獲得許可證，請訪問[這裡](https://purchase.aspose.com/buy).
### Aspose.Note for .NET 有試用版嗎？
是的，您可以下載免費試用版[這裡](https://releases.aspose.com/).
### 我可以在哪裡找到額外的支援和資源？
您可以造訪 Aspose.Note 社群論壇[這裡](https://forum.aspose.com/c/note/28)以尋求支持和討論。