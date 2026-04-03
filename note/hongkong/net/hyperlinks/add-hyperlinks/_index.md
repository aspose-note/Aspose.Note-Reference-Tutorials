---
date: 2026-04-03
description: 了解如何使用 Aspose.Note for .NET 在 Aspose.Note 文件中新增超連結、自訂超連結外觀，並插入多個超連結，以打造更豐富的
  OneNote 檔案。
keywords:
- how to add hyperlink
- insert multiple hyperlinks
- add hyperlink to onenote
- customize hyperlink appearance
- generate one file hyperlink
linktitle: 如何在 Aspose.Note 文件中加入超連結
second_title: Aspose.Note .NET API
title: 如何在 Aspose.Note 文件中加入超連結
url: /zh-hant/net/hyperlinks/add-hyperlinks/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何在 Aspose.Note 文件中新增超連結

## 介紹

在本教學中，您將學習 **如何新增超連結** 到 Aspose.Note 文件中的文字，使用 .NET API。加入超連結可將靜態筆記轉換為可互動、可點擊的內容——非常適合連結至網路資源、內部章節或外部檔案。我們將逐步說明每個步驟，示範如何 **自訂超連結外觀**，以及在需要更豐富的 OneNote 頁面時，說明如何 **插入多個超連結**。

## 快速解答
- **建立 OneNote 檔案的主要類別是什麼？** `Document` 來自 Aspose.Note.
- **哪個屬性會使文字呈現為超連結？** `TextStyle` 上的 `IsHyperlink = true`.
- **我可以連結至外部網站嗎？** 可以，將 `HyperlinkAddress` 設為類似 `https://www.google.com` 的 URL.
- **生產環境是否需要授權？** 非評估版建置必須使用有效的 Aspose.Note 授權.
- **支援哪些 .NET 版本？** .NET Framework 4.6 以上、.NET Core 3.1 以上、.NET 5/6 以上.

## 在 Aspose.Note 中「如何新增超連結」是什麼？
新增超連結是指將 URL 附加到文字上，讓使用者在 OneNote 中點擊時，會在瀏覽器或其他應用程式中開啟該資源。Aspose.Note 透過 `TextStyle.IsHyperlink` 標誌與 `HyperlinkAddress` 屬性，讓此功能可程式化實作。

## 為什麼要在 OneNote 文件中加入超連結？
- **提升導覽性：** 直接跳轉至相關的網頁或章節。
- **增強文件說明：** 提供參考資料、教學或原始檔案，無需離開筆記。
- **專業外觀：** 可自訂顏色與樣式，使超連結與文件設計融合。

## 前置條件

1. 具備 C# 與 Visual Studio 的基礎知識。
2. 已安裝 Aspose.Note for .NET 套件 – 可從 [此處](https://releases.aspose.com/note/net/) 下載。
3. 了解 Aspose.Note 文件結構（頁面、輪廓、大量文字）。

## 匯入命名空間

首先，匯入命名空間以取得核心 Aspose.Note 類別與基本 .NET 類型的存取權。

```csharp
using System;
using System.Drawing;
```

## 步驟指南

### 步驟 1：建立新 Document 物件

建立一個 `Document` 物件，用於保存所有頁面與內容。

```csharp
Document doc = new Document();
```

### 步驟 2：定義文字樣式（包含超連結樣式）

建立兩個 `TextStyle` 物件 – 一個用於普通文字，另一個用於超連結。  
此處我們亦透過設定字型顏色來 **自訂超連結外觀**。

```csharp
TextStyle textStyleRed = new TextStyle
{
    FontColor = Color.Red,
    FontName = "Arial",
    FontSize = 10,
};

TextStyle textStyleHyperlink = new TextStyle
{
    IsHyperlink = true,
    HyperlinkAddress = "www.google.com"
};
```

> **專業提示：** 若要插入 **多個超連結**，可定義額外的 `TextStyle` 物件，設定不同的 `HyperlinkAddress`，並在之後的 `RichText` 片段中重複使用。

### 步驟 3：建立 RichText 物件

建立混合普通文字與超連結的段落。`Append` 方法可讓您串接不同樣式的文字片段。

```csharp
RichText text = new RichText() { ParagraphStyle = ParagraphStyle.Default }
                    .Append("This is ", textStyleRed)
                    .Append("hyperlink", textStyleHyperlink)
                    .Append(". This text is not a hyperlink.", TextStyle.Default);
```

### 步驟 4：建立 Outline 與 Outline 元素

Outline 如同頁面上視覺元素的容器。依需求設定大小與位置。

```csharp
Outline outline = new Outline()
{
    MaxWidth = 200,
    MaxHeight = 200,
    VerticalOffset = 100,
    HorizontalOffset = 100
};

OutlineElement outlineElem = new OutlineElement();
outlineElem.AppendChildLast(text);
```

### 步驟 5：將元素加入頁面

每個 OneNote 檔案由多個頁面組成。我們建立 `Title` 與 `Page`，再將 Outline 附加上去。

```csharp
Title title = new Title() { TitleText = titleText };
Page page = new Note.Page() { Title = title };

page.AppendChildLast(outline);
doc.AppendChildLast(page);
```

### 步驟 6：儲存文件

選擇資料夾、組合完整檔名，然後呼叫 `Save`。輸出檔案將是一個有效的 OneNote `.one` 檔，內含您的超連結。

```csharp
string dataDir = "Your Document Directory";
string outputFilePath = Path.Combine(dataDir, "AddHyperlink_out.one");
doc.Save(outputFilePath);
```

## 常見問題與解決方案

| 問題 | 解決方案 |
|------|----------|
| 超連結無法開啟 | 確保 `HyperlinkAddress` 包含協定（`http://` 或 `https://`）。 |
| 文字顏色未套用 | 在用於超連結的 `TextStyle` 上設定 `FontColor`。 |
| 需要在同一頁面上放置多個連結 | 建立多個 `TextStyle` 物件，每個都有自己的 `HyperlinkAddress`，並將它們附加到相同或不同的 `RichText` 物件中。 |
| 文件在 OneNote 中無法載入 | 確認您使用的是受支援的 OneNote 版本（2010 以上）。 |

## 常見問答

**Q: 我可以在同一文件中使用 Aspose.Note 添加多個超連結嗎？**  
A: 可以，只需建立額外的 `TextStyle` 實例，設定不同的 `HyperlinkAddress`，並將它們附加到您的 `RichText` 物件中。

**Q: 我該如何自訂超連結的外觀？**  
A: 在 `IsHyperlink = true` 的 `TextStyle` 上使用 `FontColor`、`FontName`、`FontSize` 等屬性。這讓您能符合文件的品牌風格。

**Q: Aspose.Note 是否支援指向外部網站的超連結？**  
A: 當然支援。將 `HyperlinkAddress` 設為任何有效的 URL（包括 `http://` 或 `https://`），即可連結至 OneNote 檔案外部。

**Q: 是否能產生一個包含多個超連結的 OneNote 檔案？**  
A: 可以。透過不斷將不同超連結位址的樣式化 `RichText` 片段附加，您可以 **產生單一檔案的超連結集合**。

**Q: Aspose.Note 是否相容於最新的 OneNote 版本？**  
A: 此函式庫支援 OneNote 2010 及之後的版本，包括 Windows 10 UWP 版。

---

**最後更新：** 2026-04-03  
**測試環境：** Aspose.Note for .NET 24.11  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}