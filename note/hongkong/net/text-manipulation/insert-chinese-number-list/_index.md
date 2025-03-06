---
title: 在Aspose.Note文字中插入中文數字列表
linktitle: 在Aspose.Note文字中插入中文數字列表
second_title: Aspose.Note .NET API
description: 了解如何在 Aspose.Note for .NET 文件中輕鬆插入中文數字清單。透過此逐步指南提升您的文件格式化技能。
weight: 20
url: /zh-hant/net/text-manipulation/insert-chinese-number-list/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 在Aspose.Note文字中插入中文數字列表

## 介紹
您是否希望透過將中文數字清單合併到文件中來增強您的 Aspose.Note for .NET 技能？如果是這樣，那麼您來對地方了！在本教學中，我們將引導您完成使用 Aspose.Note for .NET 插入中文數字清單的過程。這個強大的程式庫允許您無縫地操作 OneNote 文件。
## 先決條件
在我們深入學習本教程之前，請確保您具備以下先決條件：
- C# 程式設計基礎知識。
- 已安裝 Aspose.Note for .NET。你可以下載它[這裡](https://releases.aspose.com/note/net/).
## 導入命名空間
首先，將必要的命名空間匯入到您的專案中：
```csharp
using System;
using System.Globalization;
using System.IO;
using Aspose.Note;
using System.Drawing;
using System.Collections.Generic;
```
## 步驟1：初始化OneNote文檔
```csharp
string dataDir = "Your Document Directory";
Aspose.Note.Document doc = new Aspose.Note.Document();
```
## 步驟2：初始化OneNote頁面
```csharp
Aspose.Note.Page page = new Aspose.Note.Page(doc);
Outline outline = new Outline(doc);
```
## 第 3 步：套用文字樣式設定
```csharp
ParagraphStyle defaultStyle = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
```
## 第 4 步：建立輪廓元素
現在，讓我們用中文數字清單建立三個大綱元素：
### 步驟 4.1：第一個元素
```csharp
OutlineElement outlineElem1 = new OutlineElement(doc) { NumberList = new NumberList("{0})", NumberFormat.ChineseCounting, "Arial", 10) };
RichText text1 = new RichText(doc) { Text = "First", ParagraphStyle = defaultStyle };
outlineElem1.AppendChildLast(text1);
```
### 步驟 4.2：第二個元素
```csharp
OutlineElement outlineElem2 = new OutlineElement(doc) { NumberList = new NumberList("{0})", NumberFormat.ChineseCounting, "Arial", 10) };
RichText text2 = new RichText(doc) { Text = "Second", ParagraphStyle = defaultStyle };
outlineElem2.AppendChildLast(text2);
```
### 步驟 4.3：第三個元素
```csharp
OutlineElement outlineElem3 = new OutlineElement(doc) { NumberList = new NumberList("{0})", NumberFormat.ChineseCounting, "Arial", 10) };
RichText text3 = new RichText(doc) { Text = "Third", ParagraphStyle = defaultStyle };
outlineElem3.AppendChildLast(text3);
```
## 第 5 步：將元素附加到大綱中
```csharp
outline.AppendChildLast(outlineElem1);
outline.AppendChildLast(outlineElem2);
outline.AppendChildLast(outlineElem3);
```
## 第 6 步：將大綱附加到頁面
```csharp
page.AppendChildLast(outline);
```
## 第 7 步：將頁面附加到文檔
```csharp
doc.AppendChildLast(page);
```
## 步驟 8：儲存 OneNote 文檔
```csharp
dataDir = dataDir + "InsertChineseNumberList_out.one"; 
doc.Save(dataDir);
Console.WriteLine("\nChinese number list inserted successfully.\nFile saved at " + dataDir);
```
恭喜！您已使用 .NET 函式庫成功將中文數字清單插入 Aspose.Note 文件中。
## 結論
在本教程中，我們介紹了將中文數字清單合併到 Aspose.Note for .NET 文件中的逐步過程。增強您的文件格式化技能，並透過這些技術使您的內容更具吸引力。
## 常見問題解答
### Q：我可以自訂中文號碼清單的格式嗎？
答：是的，您可以透過調整參數中的參數來自訂格式`NumberList`構造函數。
### Q：Aspose.Note 與最新版本的.NET 相容嗎？
答：是的，Aspose.Note 會定期更新以支援最新版本的 .NET。
### Q：在哪裡可以找到其他範例和文件？
答：全面探索[Aspose.Note 文檔](https://reference.aspose.com/note/net/).
### Q：如何取得 Aspose.Note 的臨時許可證？
答：獲得臨時許可證[這裡](https://purchase.aspose.com/temporary-license/).
### Q：我可以在哪裡尋求協助或討論與 Aspose.Note 相關的問題？
答：訪問[Aspose.Note 支援論壇](https://forum.aspose.com/c/note/28)以獲得社區支持。
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
