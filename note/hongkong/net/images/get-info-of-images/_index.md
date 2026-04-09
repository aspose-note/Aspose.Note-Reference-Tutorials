---
date: 2026-04-09
description: 學習如何使用 Aspose.Note for .NET 從 OneNote 檔案中提取圖像中繼資料並取得圖像尺寸。為 C# 開發人員提供的逐步指南。
keywords:
- extract image metadata
- how to extract images
- get image dimensions
- load onenote document
- c# get image properties
linktitle: 如何使用 Aspose.Note 從 OneNote 提取圖像元資料
second_title: Aspose.Note .NET API
title: 如何使用 Aspose.Note 從 OneNote 提取圖片元資料
url: /zh-hant/net/images/get-info-of-images/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 使用 Aspose.Note for .NET 提取圖像中繼資料

在本實作教學中，您將學習 **如何提取圖像中繼資料**——包括寬度、高度、原始大小、檔案名稱和修改時間——從 Microsoft OneNote 檔案中使用 Aspose.Note 程式庫（C#）進行提取。無論您是需要顯示圖像縮圖、驗證圖像尺寸，或是建立嵌入資產目錄，程式化提取此資訊都能為您節省大量手動步驟。

## 快速解答
- **「提取圖像中繼資料」是什麼意思？** 從 OneNote 文件中儲存的圖像中檢索尺寸、檔案名稱和時間戳記等屬性。  
- **哪個程式庫負責此操作？** Aspose.Note for .NET。  
- **我需要授權嗎？** 開發階段可使用免費試用版；正式上線需購買商業授權。  
- **支援的平台？** .NET Framework 4.6+、.NET Core 3.1+、.NET 5/6+。  
- **典型執行時間？** 標準 .one 檔案的執行時間少於一秒。

## 什麼是提取圖像中繼資料？
提取圖像中繼資料是指以程式方式讀取附加於 OneNote 頁面中每個圖像物件的描述性屬性（寬度、高度、原始尺寸、檔案名稱、最後修改時間等）。此資料可用於驗證、報告或進一步的圖像處理。

## 為何要從 OneNote 提取圖像中繼資料？
- **自動化** – 建立自動產生圖像清單的工具。  
- **驗證** – 確保圖像在發佈前符合尺寸要求。  
- **整合** – 將 OneNote 內容與其他需要圖像細節的系統（CMS、DAM 等）結合。  
- **效能** – 僅需尺寸時避免載入完整圖像檔案。

## 先決條件
1. **C# 基礎** – 您應該能熟練撰寫基本的 C# 程式碼。  
2. **Aspose.Note for .NET** – 從官方網站[此處](https://releases.aspose.com/note/net/)下載並安裝程式庫。  
3. **OneNote (.one) 檔案** – 任何包含圖像的現有 OneNote 文件。

## 匯入命名空間
在開始之前，先匯入所需的命名空間：

```csharp
using System.IO;
using Aspose.Note;
using System.Collections.Generic;
using System;
```

## 步驟 1：載入 OneNote 文件
首先，將目標 OneNote 檔案載入至 `Aspose.Note.Document` 物件。這是 **載入 OneNote 文件** 的步驟，為後續查詢做好 API 準備。

```csharp
// The path to the documents directory.
string dataDir = "Your Document Directory";

// Load the document into Aspose.Note.
Document oneFile = new Document(dataDir + "Aspose.one");
```

將 `"Your Document Directory"` 替換為實際存放 `.one` 檔案的資料夾路徑。

## 步驟 2：取得所有圖像節點
現在我們將 **如何提取圖像**，透過從文件中抓取每個 `Image` 節點來完成。

```csharp
// Get all Image nodes
IList<Aspose.Note.Image> images = oneFile.GetChildNodes<Aspose.Note.Image>();
```

`GetChildNodes<T>()` 方法會掃描整個筆記本層級，並回傳圖像物件的集合。

## 步驟 3：遍歷每個圖像並 **c# 取得圖像屬性**
我們將遍歷該集合，並列印出中繼資料，包括 **取得圖像尺寸** 與 **提取原始圖像大小** 的值。

```csharp
foreach (Aspose.Note.Image image in images)
{
    Console.WriteLine("Width: {0}", image.Width);
    Console.WriteLine("Height: {0}", image.Height);
    Console.WriteLine("OriginalWidth: {0}", image.OriginalWidth);
    Console.WriteLine("OriginalHeight: {0}", image.OriginalHeight);
    Console.WriteLine("FileName: {0}", image.FileName);
    Console.WriteLine("LastModifiedTime: {0}", image.LastModifiedTime);
    Console.WriteLine();
}
```

輸出會顯示每張圖像在頁面上呈現的當前寬度/高度、檔案中儲存的原始尺寸、檔名，以及最後修改的時間戳記。

## 常見問題與解決方案
| 問題 | 原因 | 解決方案 |
|-------|--------|-----|
| **NullReferenceException** 當 `images` 為空時 | 文件未包含圖像 | 確認來源 `.one` 檔案確實嵌入了圖像。 |
| **尺寸不正確** | 圖像在 OneNote 中被縮放 | 使用 `OriginalWidth`/`OriginalHeight` 取得實際尺寸。 |
| **FileName 為空** | 圖像是從剪貼簿貼上 | API 可能沒有檔名；請在程式碼中處理 `null` 或空字串。 |

## 常見問答

**Q: Aspose.Note 是否相容於所有版本的 Microsoft OneNote？**  
A: Aspose.Note 支援 .one、.onepkg 與 .onetoc2 格式，涵蓋自 2007 起的大多數 OneNote 版本。

**Q: 提取後我可以修改圖像屬性嗎？**  
A: 可以，您可以變更 `Width`、`Height` 或 `FileName` 等屬性，然後儲存文件。

**Q: Aspose.Note 能在 .NET Core 上運作嗎？**  
A: 當然可以。此程式庫完全相容於 .NET Core、.NET 5 與 .NET 6。

**Q: 是否提供免費試用版？**  
A: 有，您可從 Aspose 官方網站下載試用版以體驗全部功能。

**Q: 我可以在哪裡取得額外協助或社群支援？**  
A: 請前往 Aspose.Note 論壇[此處](https://forum.aspose.com/c/note/28)取得技巧、範例程式碼與社群的解答。

---

**最後更新：** 2026-04-09  
**測試環境：** Aspose.Note 24.11 for .NET  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}