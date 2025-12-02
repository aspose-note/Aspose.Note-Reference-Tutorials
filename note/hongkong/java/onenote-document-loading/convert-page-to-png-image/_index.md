---
date: 2025-11-29
description: 學習如何使用 Aspose.Note for Java 將 OneNote 頁面匯出為 PNG。按照步驟說明設定頁面索引、轉換頁面並儲存圖片。
language: zh-hant
linktitle: Export OneNote Page to PNG Image in Java
second_title: Aspose.Note Java API
title: 使用 Aspose.Note 在 Java 中將 OneNote 頁面匯出為 PNG 圖片
url: /java/onenote-document-loading/convert-page-to-png-image/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 使用 Aspose.Note 在 Java 中將 OneNote 頁面匯出為 PNG 圖像

## 介紹

在本教學中，您將了解 **如何使用 Aspose.Note for Java 函式庫將 OneNote 頁面匯出為 PNG 圖像**。我們將一步步說明從環境設定、設定頁面索引，到最終將頁面儲存為高品質 PNG 檔案的全部過程。完成後，您即可在任何處理 OneNote 文件的 Java 應用程式中加入此功能。

## 快速回答
- **需要的函式庫是什麼？** Aspose.Note for Java.  
- **可以只匯出單一頁面嗎？** 可以—使用 `setPageIndex` 來指定特定頁面。  
- **支援的影像格式？** PNG、JPEG、GIF、BMP、TIFF（此處示範 PNG）。  
- **需要授權嗎？** 提供免費試用版；正式環境需購買授權。  
- **實作需要多長時間？** 基本轉換通常在 10 分鐘以內完成。

## 什麼是「匯出 OneNote 頁面」？
將 OneNote 頁面匯出指的是將 `.one` 文件中的特定頁面轉換為獨立的影像檔案（此處為 PNG）。當您需要在 OneNote 環境之外分享、嵌入或處理 OneNote 內容時，此功能非常有用。

## 為什麼使用 Aspose.Note for Java 來轉換 OneNote 為 PNG？
- **無需 Microsoft Office 相依** – 可在任何支援 Java 的平台上執行。  
- **細緻的控制** – 可透過 `setPageIndex` 選取任意頁面。  
- **高品質輸出** – PNG 能保留向量圖形與文字清晰度。  
- **支援批次處理** – 可輕鬆迴圈頁面進行大量轉換。

## 前置條件

在開始之前，請確保您已具備以下條件：

1. **Java Development Kit (JDK)** – 版本 8 或以上。  
2. **Aspose.Note for Java** – 從 [Aspose 官方網站](https://releases.aspose.com/note/java/) 下載最新 JAR。  
3. **OneNote 文件**（`.one`）其中包含您想匯出的頁面。

## 匯入套件

首先，匯入必要的 Java 類別：

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.LoadOptions;
import com.aspose.note.SaveFormat;
```

## 步驟說明

### 步驟 1：載入 OneNote 文件

```java
// Load the document into Aspose.Note.
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Sample1.one", new LoadOptions());
```

我們使用 `Document` 類別從磁碟讀取 OneNote 檔案。`LoadOptions` 物件可讓您在需要時自訂載入行為。

### 步驟 2：初始化 ImageSaveOptions

```java
// Initialize ImageSaveOptions object
ImageSaveOptions opts = new ImageSaveOptions(SaveFormat.Png);
```

`ImageSaveOptions` 告訴 Aspose.Note 我們希望輸出為 **PNG** 格式。您也可以透過變更 `SaveFormat` 改為 JPEG、BMP 等。

### 步驟 3：設定頁面索引（如何轉換 OneNote 頁面）

```java
// set page index
opts.setPageIndex(0);
```

`setPageIndex` 方法用來選擇要匯出的頁面。頁碼從 **0** 開始計算，`0` 代表第一頁。調整此值即可匯出其他頁面。

### 步驟 4：將文件儲存為 PNG（將 OneNote 儲存為 PNG）

```java
// Save the document as PNG.
oneFile.save(dataDir + "ConvertSpecificPageToPngImage_out.png", opts);
```

呼叫 `save` 方法即可將選取的頁面寫入磁碟為 PNG 檔案。檔名 `ConvertSpecificPageToPngImage_out.png` 只是示範，您可以自行命名。

## 常見問題與提示

- **頁碼錯誤** – 請記得索引從 0 開始。如果得到空白影像，請檢查索引值。  
- **缺少 Aspose.Note JAR** – 確認 JAR 已加入 classpath，否則會出現 `ClassNotFoundException`。  
- **頁面過大** – 對於非常大的頁面，建議增加 JVM 堆積大小（`-Xmx`）以避免 `OutOfMemoryError`。

## 常見問答

### Q1: 我可以一次將多個頁面轉換為 PNG 圖像嗎？
A1: 可以，您可以迴圈文件的每個頁面，更新 `opts.setPageIndex(i)`，然後對每次迭代呼叫 `save`。

### Q2: Aspose.Note for Java 是否支援除 PNG 之外的其他影像格式？
A2: 當然可以。您可以在 `ImageSaveOptions` 中設定 `SaveFormat.Jpeg`、`SaveFormat.Gif`、`SaveFormat.Bmp` 或 `SaveFormat.Tiff`。

### Q3: 是否提供 Aspose.Note for Java 的免費試用？
A3: 有，您可以從 [網站](https://releases.aspose.com/) 下載免費試用版。

### Q4: 若遇到 Aspose.Note for Java 的問題，我可以獲得技術支援嗎？
A4: 可以，您可前往 Aspose 社群論壇 [此處](https://forum.aspose.com/c/note/28) 取得協助。

### Q5: 我該從哪裡購買 Aspose.Note for Java 的授權？
A5: 您可在 [購買頁面](https://purchase.aspose.com/buy) 購買授權。

### Q6: 若頁面內含嵌入圖像，我該如何匯出？
A6: 嵌入的圖像會自動在 PNG 輸出中呈現，無需額外程式碼。

### Q7: 我可以設定 DPI 或影像解析度嗎？
A7: 可以，在呼叫 `save` 前使用 `opts.setResolution(int dpi)` 來控制輸出品質。

---

**最後更新：** 2025-11-29  
**測試環境：** Aspose.Note for Java 24.11（最新）  
**作者：** Aspose

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
