---
date: 2026-04-13
description: 學習如何在 .NET 中使用 Aspose.Note 透過圖像串流將圖片加入 OneNote 文件。本分步指南涵蓋從串流載入圖片、將其附加至大綱，以及儲存檔案的操作。
keywords:
- add image to onenote
- how to insert image
- load image from stream
- append image to outline
- image stream .net
linktitle: 使用 Aspose.Note 透過圖像串流將圖片新增至 OneNote
second_title: Aspose.Note .NET API
title: 使用 Aspose.Note 透過影像串流將圖片新增至 OneNote
url: /zh-hant/net/images/insert-image-using-image-stream/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 使用 Aspose.Note 透過 Image Stream 將圖片加入 OneNote

## 簡介

在本教學中，您將發現 **如何將圖片加入 OneNote** 文件，方法是從串流載入圖片並將其附加到大綱，使用 Aspose.Note for .NET。無論您是建立報告工具、筆記應用程式，或自動化文件產生，程式化插入圖片都能讓您的 OneNote 檔案更具吸引力與實用性。

## 快速解答
- **需要哪個程式庫？** Aspose.Note for .NET（提供免費試用）。  
- **支援哪些 .NET 版本？** .NET Framework 4.5+、.NET Core 3.1+、.NET 5/6+。  
- **可以從串流載入圖片嗎？** 可以 – 使用 `FileStream` 或任何 `Stream` 實作。  
- **如何控制圖片對齊方式？** 設定 `Alignment` 屬性（例如 `HorizontalAlignment.Right`）。  
- **產生的檔案格式為何？** OneNote (`.one`) 檔案，可在 Microsoft OneNote 中開啟。

## 什麼是「將圖片加入 OneNote」？

將圖片加入 OneNote 檔案表示將視覺元素直接嵌入頁面的內容層級中。使用 Aspose.Note 時，您會操作如 `Document`、`Page`、`Outline`、`OutlineElement` 等物件。將 `Image` 物件插入 `OutlineElement` 後，圖片即成為 OneNote 頁面版面的組成部分。

## 為何使用 Aspose.Note 進行圖片插入？

- **不需安裝 Office** – 可在伺服器上產生或修改 OneNote 檔案。  
- **完整的版面控制** – 可精確對齊、調整大小與定位圖片。  
- **支援串流** – 可使用任何 `Stream`，非常適合雲端儲存或僅記憶體的情境。  
- **跨平台** – 相容於 Windows、Linux 與 macOS 的 .NET 執行環境。

## 先決條件

1. **開發環境** – Visual Studio 2022 或任何相容 .NET 的 IDE。  
2. **Aspose.Note 程式庫** – 從官方網站[此處](https://releases.aspose.com/note/net/)下載。  
3. **圖片檔案** – 至少一張您想嵌入的圖片（JPG、PNG、BMP、GIF 或 TIFF）。  
4. **基本 C# 知識** – 熟悉檔案處理與物件導向程式碼。

## 匯入命名空間
首先，匯入提供 Aspose.Note 類別與標準 .NET I/O 工具的命名空間。

```csharp
using System.IO;
using Aspose.Note;
using System.Collections.Generic;
using System.Drawing;
using System;
```

現在讓我們一步一步走過整個流程。

### 步驟 1：初始化 Document 物件
我們先建立一個全新的 `Document` 實例，用於保存 OneNote 檔案。

```csharp
// The path to the documents directory.
string dataDir = "Your Document Directory";
Document doc = new Document();
```

### 步驟 2：建立 Page 物件
OneNote 檔案由一或多個頁面組成。此處我們建立一個新頁面來放置內容。

```csharp
Aspose.Note.Page page = new Aspose.Note.Page(doc);
```

### 步驟 3：初始化 Outline 與 OutlineElement 物件
Outline 是用來容納豐富內容（文字、圖片、表格）的容器。`OutlineElement` 為其子項，實際保存這些項目。

```csharp
Outline outline1 = new Outline(doc);
OutlineElement outlineElem1 = new OutlineElement(doc);
```

### 步驟 4：從串流載入圖片
使用 `FileStream`（或任何 `Stream`）讀取圖片檔案並建立 `Image` 物件。這正是 **從串流載入圖片** 的關鍵所在。

```csharp
using (FileStream fs = File.OpenRead(dataDir + "image.jpg"))
{
    Aspose.Note.Image image1 = new Aspose.Note.Image(doc, "Penguins.jpg", fs)
    {
        Alignment = HorizontalAlignment.Right
    };
    outlineElem1.AppendChildLast(image1);
}
```

### 步驟 5：將圖片附加至 OutlineElement
圖片現在已成為 `OutlineElement` 的一部份。此步驟示範 **將圖片附加至大綱** 的功能。

```csharp
outlineElem1.AppendChildLast(image1);
```

### 步驟 6：將 OutlineElement 附加至 Outline
現在我們將包含圖片的元素附加至 Outline 容器。

```csharp
outline1.AppendChildLast(outlineElem1);
```

### 步驟 7：將 Outline 附加至 Page
包含圖片的 Outline 被加入至頁面。

```csharp
page.AppendChildLast(outline1);
```

### 步驟 8：將 Page 附加至 Document
頁面準備好後，我們將其插入至文件層級中。

```csharp
doc.AppendChildLast(page);
```

### 步驟 9：儲存 Document
最後，我們將 OneNote 檔案寫入磁碟。產生的檔案可在 Microsoft OneNote 中開啟。

```csharp
doc.Save(dataDir + "BuildDocAndInsertImageUsingImageStream_out.one");
```

## 常見問題與解決方案

| 問題 | 發生原因 | 解決方法 |
|-------|----------------|-----|
| **圖片未顯示** | 在加入圖片前，串流已被關閉。 | 在 `AppendChildLast` 呼叫周圍保留 `using` 區塊（如範例所示）。 |
| **對齊不正確** | `Alignment` 屬性未設定或之後被覆寫。 | 在建立 `Image` 時設定 `Alignment`，或在附加前修改 `image1.Alignment`。 |
| **不支援的圖片格式** | 嘗試載入 Aspose.Note 無法辨識的格式。 | 先將圖片轉換為 JPG、PNG、BMP、GIF 或 TIFF。 |
| **檔案路徑錯誤** | `dataDir` 指向不存在的資料夾。 | 使用 `Path.Combine`，並在執行前確認資料夾是否存在。 |

## 常見問答

**Q: 我可以使用此方法在單一文件中插入多張圖片嗎？**  
A: 可以。只需對每張圖片重複 *從串流載入圖片* 與 *將圖片附加至 OutlineElement* 的步驟。

**Q: Aspose.Note 是否支援除 JPG 之外的其他圖片格式？**  
A: 當然支援。PNG、BMP、GIF 與 TIFF 都可使用。

**Q: 我可以自訂插入圖片的對齊方式與尺寸嗎？**  
A: 可以。除了 `Alignment`，您還可以在 `Image` 物件上設定 `Width`、`Height` 與 `Scale` 屬性。

**Q: Aspose.Note 相容於所有 .NET 版本嗎？**  
A: 它支援 .NET Framework 4.5+、.NET Core 3.1+、.NET 5 以及 .NET 6+。

**Q: 我可以在哪裡找到 Aspose.Note 的其他資源與支援？**  
A: 您可在 [Aspose 論壇](https://forum.aspose.com/c/note/28) 找到完整文件、討論區與支援資訊。

---

**最後更新：** 2026-04-13  
**測試環境：** Aspose.Note 24.11 for .NET  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}