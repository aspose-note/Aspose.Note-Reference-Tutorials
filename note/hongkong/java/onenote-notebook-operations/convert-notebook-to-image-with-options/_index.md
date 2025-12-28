---
date: 2025-12-28
description: 了解如何使用 Aspose.Note 在 Java 中將 OneNote 轉換為圖像並設定圖像解析度。本逐步指南亦說明如何匯出 OneNote
  PNG 檔案。
linktitle: Convert OneNote to Image with Options - Aspose.Note
second_title: Aspose.Note Java API
title: 將 OneNote 轉換為圖片（含選項） - Aspose.Note
url: /zh-hant/java/onenote-notebook-operations/convert-notebook-to-image-with-options/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 將 OneNote 轉換為圖像（含選項） - Aspose.Note

## 簡介

在本教學中，您將學習如何使用 Aspose.Note for Java **將 OneNote 轉換為圖像**，並可使用各種選項。無論您需要用於報告的高解析度 PNG，或是快速的 JPEG 縮圖，以下步驟將精確說明如何完成並將此過程整合至您的 Java 應用程式中。

## 快速答案
- **什麼是「convert OneNote to image」的意思？** 它會將整個 OneNote 筆記本轉換為點陣圖檔案（PNG、JPEG 等）。
- **建議使用哪種格式以獲得無損品質？** PNG，因為它能在不產生壓縮雜訊的情況下保留所有細節。
- **如何在 Java 中設定圖像解析度？** 使用 `ImageSaveOptions.setResolution(int dpi)` 透過 `NotebookImageSaveOptions`。
- **能否一次性將 OneNote 筆記本匯出為 PNG？** 可以，Aspose.Note 提供單一的 `save` 呼叫，搭配相應的選項即可。
- **生產環境是否需要授權？** 生產環境需要商業授權；可使用免費試用版進行評估。

## 什麼是「convert OneNote to image」？
將 OneNote 筆記本轉換為圖像，即將筆記本的每一頁渲染為位圖檔案。此功能可用於建立靜態預覽、存檔內容，或在原始 OneNote 格式不受支援的報告中嵌入筆記本頁面。

## 為什麼要使用 Aspose.Note for Java？
- **完整控制** 輸出格式、解析度與色彩深度。  
- **無需 Microsoft Office 依賴** – 可在任何伺服器端 Java 環境中運行。  
- **支援複雜筆記本**，包括嵌入檔案、手寫墨跡與豐富文字。

## 先決條件

1. **Java Development Kit (JDK)** – 版本 8 或以上。  
2. **Aspose.Note for Java JAR 檔案** – 從 [here](https://releases.aspose.com/note/java/) 下載最新程式庫，並將其加入專案的 classpath。

## 匯入套件

首先，匯入我們在載入筆記本與設定圖像輸出時所需的類別。

```java
import java.io.IOException;

import com.aspose.note.ImageSaveOptions;
import com.aspose.note.Notebook;
import com.aspose.note.NotebookImageSaveOptions;
import com.aspose.note.SaveFormat;
```

## 步驟 1：載入筆記本

載入您想要轉換的 OneNote 筆記本。將路徑替換為您 `.onetoc2` 檔案的所在位置。

```java
String dataDir = "Your Document Directory";
// Load a OneNote Notebook
Notebook notebook = new Notebook(dataDir + "test.onetoc2");
```

## 步驟 2：設定儲存選項（如何 **set image resolution java**）

建立 `NotebookImageSaveOptions` 實例，選擇輸出格式，並指定所需的解析度。在此範例中，我們使用 PNG，解析度為 400 dpi。

```java
NotebookImageSaveOptions notebookSaveOptions = new NotebookImageSaveOptions(SaveFormat.Png);

ImageSaveOptions documentSaveOptions = notebookSaveOptions.getDocumentSaveOptions();

documentSaveOptions.setResolution(400);
```

> **專業提示：** 為了在大型筆記本上加快處理速度，可降低解析度（例如 150 dpi）。若需列印品質的圖形，則提高解析度。

## 步驟 3：將筆記本儲存為圖像（如何 **export OneNote PNG**）

定義輸出檔案名稱並呼叫 `save`。相同的選項會套用至筆記本的每一頁。

```java
dataDir = dataDir + "ExportNotebooktoImagewithOptions_out.png";

// Save the Notebook
notebook.save(dataDir, notebookSaveOptions);
```

上述程式碼會產生 PNG 檔案（或一系列 PNG 檔案，每頁一個），其解析度為您設定的值。

## 常見問題與解決方案

| 問題 | 解決方案 |
|------|----------|
| **OutOfMemoryError** 在大型筆記本上 | 增加 JVM 堆積大小（`-Xmx2g`）或降低解析度。 |
| **輸出空白頁面** | 確保筆記本未受密碼保護；如有需要，使用 `Notebook.load(path, password)`。 |
| **不支援的圖像格式** | 僅使用 `SaveFormat.Png`、`SaveFormat.Jpeg` 或 `SaveFormat.Bmp`——其他格式不支援筆記本匯出。 |

## 常見問答

**Q: Aspose.Note 能處理複雜的 OneNote 檔案嗎？**  
A: 是的，它能有效處理包含嵌入檔案、手寫墨跡與豐富格式的筆記本。

**Q: Aspose.Note for Java 容易整合到現有專案嗎？**  
A: 絕對可以。API 簡單明瞭，您只需將 JAR 加入 classpath 即可。

**Q: 在將筆記本轉換時，我可以自訂圖像輸出嗎？**  
A: 可以。您可以透過 `ImageSaveOptions` 設定解析度、格式，甚至色彩深度。

**Q: Aspose.Note 為開發者提供支援嗎？**  
A: 有。Aspose 提供豐富的文件、論壇與即時回應的支援管道。

**Q: Aspose.Note for Java 有免費試用版嗎？**  
A: 有，您可從 [here](https://releases.aspose.com/) 下載試用版。

---

**最後更新：** 2025-12-28  
**測試環境：** Aspose.Note 24.11 for Java  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}