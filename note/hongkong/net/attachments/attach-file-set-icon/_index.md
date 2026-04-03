---
date: 2026-04-03
description: 了解如何在 Aspose.Note for .NET 中設定自訂圖示與附加檔案，包括儲存 OneNote 檔案以及使用圖片作為圖示。
keywords:
- set custom icon
- attach multiple files
- use image as icon
- save onenote file
- embed text file
linktitle: 在 Aspose.Note 中附加檔案並設定圖示
second_title: Aspose.Note .NET API
title: 在 Aspose.Note 中設定自訂圖示並附加檔案
url: /zh-hant/net/attachments/attach-file-set-icon/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 設定自訂圖示並在 Aspose.Note 中附加檔案

## 介紹

如果您需要在 OneNote 頁面為附件 **設定自訂圖示**，Aspose.Note for .NET 讓此操作變得簡單。透過附加檔案並指定圖像作為其圖示，您可以建立更豐富、更具資訊性的筆記，外觀完全符合您的需求。在本教學中，我們將完整示範整個流程——從建立全新文件、加入附件、套用自訂 JPEG 圖示，最後儲存 OneNote 檔案。

## 快速解答
- **「設定自訂圖示」是什麼意思？** 它讓您可以將預設的附件縮圖替換為您提供的圖像。  
- **我可以附加多個檔案嗎？** 可以，對每個檔案重複附件步驟即可。  
- **支援哪些圖像格式作為圖示？** 任何 .NET 相容的格式，例如 JPEG、PNG、BMP 或 GIF。  
- **我需要授權嗎？** 正式使用時需要有效的 Aspose.Note 授權；免費試用版可用於評估。  
- **如何儲存 OneNote 檔案？** 使用 `Document.Save()` 並指定 *.one* 檔案路徑。

## 在 Aspose.Note 中「設定自訂圖示」是什麼？
設定自訂圖示是指為 OneNote 頁面中的附件指定特定圖像（例如 JPEG），以此來代表該檔案。這可提升使用者的視覺提示，亦可用於顯示檔案類型標誌或品牌圖像。

## 為何要為附件設定自訂圖示？
- **更佳的視覺情境：** 使用者能立即辨識附件的類型或用途。  
- **品牌一致性：** 使用公司標誌作為所有相關文件的圖示。  
- **提升使用者體驗：** 讓筆記看起來更精緻、專業，特別是在共享筆記本中。

## 前置條件

- 具備 C# 程式設計的基本知識。  
- 已安裝 Aspose.Note for .NET 程式庫。  
- Visual Studio（或任何 .NET 相容的 IDE）已就緒以進行開發。

## 匯入命名空間

首先，將所需的命名空間匯入範圍，以便操作檔案、圖像與 OneNote 物件。

```csharp
using System.IO;
using Aspose.Note;
using System;
using System.Collections.Generic;
using System.Drawing.Imaging;
```

## 步驟說明：附加檔案並設定其圖示

### 步驟 1：建立 Document 物件
全新的 `Document` 實例代表您即將建立的 OneNote 檔案。

```csharp
Document doc = new Document();
```

### 步驟 2：初始化 Page 物件
每個 OneNote 檔案包含一個或多個頁面。此處我們建立第一個頁面。

```csharp
Aspose.Note.Page page = new Aspose.Note.Page(doc);
```

### 步驟 3：初始化 Outline 物件
Outline 作為頁面上內容區塊的容器。

```csharp
Outline outline = new Outline(doc);
```

### 步驟 4：初始化 OutlineElement 物件
此元素將保存附加的檔案及其自訂圖示。

```csharp
OutlineElement outlineElem = new OutlineElement(doc);
```

### 步驟 5：讀取圖示影像並初始化 AttachedFile 物件
我們開啟圖像串流（自訂圖示），並指向要嵌入的檔案。

```csharp
string dataDir = "Your Document Directory";
using (var stream = File.OpenRead(dataDir + "icon.jpg"))
{
    AttachedFile attachedFile = new AttachedFile(doc, dataDir + "attachment.txt", stream, ImageFormat.Jpeg);
}
```

> **小技巧：** 若想使用 PNG 圖示，請將 `ImageFormat.Jpeg` 改為 `ImageFormat.Png`。

### 步驟 6：將附加檔案加入 OutlineElement
現在檔案（含圖示）成為 OutlineElement 的子項目。

```csharp
outlineElem.AppendChildLast(attachedFile);
```

### 步驟 7：將 OutlineElement 加入 Outline
此動作將元素嵌入 Outline 容器內。

```csharp
outline.AppendChildLast(outlineElem);
```

### 步驟 8：將 Outline 加入 Page
將整個 Outline 階層附加至頁面。

```csharp
page.AppendChildLast(outline);
```

### 步驟 9：將 Page 加入 Document
將完成的頁面加入文件結構。

```csharp
doc.AppendChildLast(page);
```

### 步驟 10：儲存 OneNote 文件
最後，將文件寫入磁碟，儲存為 *.one* 檔案。

```csharp
dataDir = dataDir + "AttachFileAndSetIcon_out.one";
doc.Save(dataDir);
```

## 常見使用情境
- **嵌入合約：** 附加 PDF 並使用合約標誌圖示。  
- **分享程式碼片段：** 附加 `.txt` 檔案並使用自訂的「程式碼」圖示。  
- **專案文件：** 附加設計檔案，並設定與檔案類型相符的縮圖。

## 常見問題與解決方案

| 問題 | 解決方案 |
|------|----------|
| **圖示未顯示** | 確認圖像格式與您傳入的 `ImageFormat` 相符（例如 JPEG 與 PNG）。 |
| **檔案路徑錯誤** | 使用 `Path.Combine(dataDir, "file.ext")` 以避免缺少斜線的問題。 |
| **大型附件導致效能延遲** | 先壓縮檔案或將其分割成多個較小的附件。 |

## 常見問與答

**Q: 我可以使用 Aspose.Note for .NET 在單一筆記中附加多個檔案嗎？**  
A: 可以。只需對每個檔案重複「讀取圖示影像並初始化 AttachedFile 物件」的區塊，並將每個 `AttachedFile` 附加至相同的 `OutlineElement`，或建立獨立的元素。

**Q: 是否可以為檔案附件設定自訂圖示？**  
A: 當然可以。`AttachedFile` 建構函式允許您傳入圖像串流並指定圖像格式，讓您完全掌控圖示。

**Q: Aspose.Note 是否支援其他圖像格式作為圖示？**  
A: 支援。除了 JPEG，您也可以使用 PNG、BMP、GIF，或任何 `System.Drawing.Imaging.ImageFormat` 支援的格式。

**Q: 我可以從外部 URL 附加檔案嗎？**  
A: 雖然 Aspose.Note 主要使用本機串流，但您可以透過 `HttpClient` 下載檔案，將其存入 `MemoryStream`，再將該串流傳給 `AttachedFile`。

**Q: 檔案附件有大小限制嗎？**  
A: Aspose.Note 本身沒有硬性限制，但極大檔案可能影響記憶體使用與效能。建議壓縮大型附件。

---

**Last Updated:** 2026-04-03  
**Tested With:** Aspose.Note 24.11 for .NET  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}