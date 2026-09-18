---
date: 2026-05-05
description: 學習如何使用 .NET 將圖片插入 Aspose.Note 文件。本分步指南將向您展示如何對齊圖片、將圖片附加至頁面，以及增強視覺內容。
keywords:
- how to insert image
- how to align image
- append image to page
linktitle: 在 Aspose.Note 文件中插入圖片
second_title: Aspose.Note .NET API
title: 如何使用 .NET 在 Aspose.Note 文件中插入圖片
url: /zh-hant/net/images/insert-images/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何在 Aspose.Note 文件中使用 .NET 插入圖片

## 簡介

如果您想讓 Aspose.Note 檔案更具吸引力，**如何插入圖片** 是您首先需要掌握的技能。在本教學中，我們將逐步說明添加圖片、控制其大小、精確定位以及按照需求對齊的具體步驟。完成後，您將能輕鬆插入圖片、對齊圖片，並將圖片附加至頁面——全部使用乾淨、易讀的 C# 程式碼。

## 快速答覆
- **需要哪個函式庫？** Aspose.Note for .NET  
- **可以程式化設定圖片大小嗎？** 可以 – 使用 Width 和 Height 屬性。  
- **如何定位圖片？** 調整 HorizontalOffset、VerticalOffset 或使用對齊選項。  
- **圖片格式有沒有限制？** 支援 JPG、PNG、BMP、GIF 等格式。  
- **商業使用需要授權嗎？** 商業使用需擁有有效的 Aspose.Note 授權。

## 什麼是 Aspose.Note 中的圖片插入？

插入圖片是指建立一個 Aspose.Note.Image 物件，設定其視覺屬性，並將其附加到 OneNote 相容的 .one 檔案中的頁面。這讓您能以螢幕截圖、圖表或任何視覺輔助素材豐富筆記。

## 為什麼要使用 Aspose.Note 插入圖片？

- **更佳的溝通效果：** 視覺圖像比純文字更快說明複雜概念。  
- **版面一致性：** 程式化控制確保每份文件遵循相同的設計標準。  
- **自動化友好：** 非常適合產生報告、教學或批次處理的筆記本。

## 先決條件

1. Aspose.Note for .NET：從 [here](https://releases.aspose.com/note/net/) 下載並安裝 Aspose.Note for .NET。  
2. 圖片檔案：將您打算嵌入的圖片檔案（JPG、PNG 等）事先準備好於磁碟上。

## 匯入命名空間

我們首先匯入提供檔案 I/O 與 Aspose.Note API 存取的命名空間。

```csharp
using System.IO;
using Aspose.Note;
using System.Collections.Generic;
using System.Drawing;
using System;
```

## 步驟 1：載入文件並取得頁面

首先，開啟現有的 .one 文件，並取得圖片將要放置的頁面。

```csharp
string dataDir = "Your Document Directory";
Document doc = new Document(dataDir + "YourDocument.one");
Aspose.Note.Page page = doc.FirstChild;
```

## 如何對齊圖片

在加入圖片之前，先決定它與其他內容的對齊方式。Aspose.Note 提供水平對齊選項（左、置中、右）。您亦可使用偏移值微調位置。

## 步驟 2：載入圖片並設定屬性

建立 Image 物件，指向您的檔案，並定義其尺寸、偏移與對齊方式。

```csharp
Aspose.Note.Image image = new Aspose.Note.Image(doc, dataDir + "image.jpg")
{
    Width = 100,                // Set image width
    Height = 100,               // Set image height
    HorizontalOffset = 100,     // Set horizontal offset
    VerticalOffset = 400,       // Set vertical offset
    Alignment = HorizontalAlignment.Right  // Set image alignment
};
```

## 將圖片附加至頁面

現在圖片已完整設定，將其附加至頁面的元素樹中。

```csharp
page.AppendChildLast(image);
```

## 常見陷阱與技巧

- **偏移值不正確：** 請記得偏移是以頁面左上角為基準。過大的垂直偏移可能會使圖片超出畫面。  
- **不支援的格式：** 若使用未被識別的格式，Aspose.Note 會拋出例外——請先將檔案轉為 JPG 或 PNG。  
- **授權警告：** 未使用授權執行會在產生的文件上加上浮水印；在正式環境務必套用授權。

## 結論

您現在已學會 **如何在 Aspose.Note 文件中插入圖片**、**如何對齊圖片**，以及 **如何將圖片附加至頁面**，只需幾行簡潔的 C# 程式碼。這些技巧讓您能自動建立更豐富、更專業的筆記本。

## 常見問答

### Q1：我可以在 Aspose.Note 文件中插入任何格式的圖片嗎？

A1：是的，Aspose.Note 支援多種圖片格式，包括 JPG、PNG、BMP、GIF 等。

### Q2：能否以程式方式調整插入圖片的大小？

A2：當然可以！在插入時您可以依需求調整圖片的寬度與高度。

### Q3：Aspose.Note 是否提供修改圖片對齊的選項？

A3：是的，您可以將圖片對齊至文件頁面的左側、右側或置中。

### Q4：我可以在文件的單一頁面插入多張圖片嗎？

A4：當然可以！使用 Aspose.Note 您可以在單一頁面插入任意多張圖片。

### Q5：插入的圖片檔案大小有沒有上限？

A5：Aspose.Note 對圖片檔案大小沒有嚴格限制，但建議對圖片進行最佳化以提升效能。

## 常見問題

**Q: 如何從串流而非檔案路徑載入圖片？**  
A: 使用 Image(Stream, Document) 建構函式，並傳入包含圖片位元組的 MemoryStream。

**Q: 圖片加入頁面後，我可以更改它嗎？**  
A: 可以，您可以修改現有 Image 物件的 Width、Height、HorizontalOffset、VerticalOffset 與 Alignment 屬性，然後呼叫 page.Update()。

**Q: 能否在圖片下方加入說明文字？**  
A: 在圖片之後插入 RichText 元素，並設定其文字作為說明。

**Q: Aspose.Note 支援動畫 GIF 嗎？**  
A: 動畫 GIF 會被視為靜態圖片，只顯示第一幀。

**Q: 若圖片顯示模糊，我該怎麼辦？**  
A: 確保來源圖片解析度足夠，且避免將其放大超過原始尺寸。

---

**最後更新：** 2026-05-05  
**測試環境：** Aspose.Note 23.12 for .NET  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}
{{< blocks/products/products-backtop-button >}}