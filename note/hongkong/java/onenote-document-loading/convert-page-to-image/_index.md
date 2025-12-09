---
date: 2025-11-29
description: 學習如何使用 Java 將 OneNote 頁面匯出為圖像，並了解如何使用 Aspose.Note 轉換 OneNote 頁面圖像。請遵循我們的逐步指南，快速整合。
linktitle: How to Export OneNote Page to Image Using Java
second_title: Aspose.Note Java API
title: 使用 Java 將 OneNote 頁面匯出為圖像
url: /zh-hant/java/onenote-document-loading/convert-page-to-image/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何使用 Java 將 OneNote 頁面匯出為圖像

## 介紹

在本教學中，您將學習 **如何匯出 OneNote** 頁面為圖像檔案，使用 Java 搭配 Aspose.Note。將 OneNote 頁面轉換為圖像非常方便，無論是要將筆記本內容嵌入報告、與非 OneNote 使用者分享快照，或是為文件管理系統產生縮圖。我們將逐步說明每一行程式碼的意義，並示範如何自訂輸出結果。

## 快速答覆
- **需要的函式庫是什麼？** Aspose.Note for Java  
- **可以選擇圖像格式嗎？** 可以 – 透過 `ImageSaveOptions` 支援 JPEG、PNG、BMP 等格式  
- **商業使用需要授權嗎？** 商業用途必須使用有效的 Aspose.Note 授權  
- **可以匯出哪一頁？** 只要設定 `PageIndex`（從 0 開始）即可匯出任意頁面  
- **轉換需要多長時間？** 標準頁面通常在一秒內完成

## 什麼是將 OneNote 頁面匯出為圖像？

將 OneNote 頁面匯出為圖像是指將頁面中的豐富內容——文字、手寫、圖表——渲染成靜態圖像檔（例如 JPEG）。此過程會產生可攜帶的視覺表示，無論是否安裝 OneNote 客戶端，都能在任何地方顯示。

## 為什麼使用 Aspose.Note 轉換 OneNote 頁面？

- **完整保真** – 保留版面配置、字型與墨跡  
- **無需 Microsoft Office 依賴** – 可在任何支援 Java 的平台上執行  
- **精細控制** – 可自行選擇圖像格式、品質與特定頁面索引  
- **可擴充** – 適合大量批次處理多頁文件  

## 前置條件

在開始之前，請確保已具備以下條件：

1. **Java Development Kit (JDK)** – 安裝 JDK 11 或更新版本。若尚未安裝，可從 [Oracle 的官方網站](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) 下載。  
2. **Aspose.Note for Java** – 從 [Aspose.Note 下載頁面](https://releases.aspose.com/note/java/) 取得最新程式庫，並將 JAR 加入專案的 classpath。

## 匯入套件

首先，我們匯入必要的套件，以取得文件處理與圖像儲存選項的功能。

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.SaveFormat;
```

## 步驟 1：載入 OneNote 文件

我們先將 `.one` 檔案載入為 `Aspose.Note` 的 `Document` 物件。

```java
String dataDir = "Your Document Directory";
// Load the document into Aspose.Note
Document oneFile = new Document(dataDir + "Sample1.one");
```

> **專業提示：** 若檔案位於 JAR 內，請使用絕對路徑或資源串流載入。

## 步驟 2：初始化圖像儲存選項

建立 `ImageSaveOptions` 實例以定義輸出格式（此範例使用 JPEG）。您也可以透過變更 `SaveFormat` 改為 PNG、BMP 或 GIF。

```java
// Initialize ImageSaveOptions object
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Jpeg);
```

## 步驟 3：指定頁面索引

頁面索引採零基制，`1` 代表 **第二** 頁。依需求調整此值即可匯出任意頁面。

```java
// Specify second page for conversion
options.setPageIndex(1);
```

## 步驟 4：將文件儲存為圖像

呼叫 `Document` 物件的 `save` 方法，傳入目標檔名與先前設定的選項。

```java
// Save the document
oneFile.save(dataDir + "ConvertSpecificPageToImage_out.jpg", options);
```

## 步驟 5：列印確認訊息

簡單的主控台訊息會顯示圖像已成功產生。

```java
// Print confirmation message
System.out.println("File saved: " + dataDir + "ConvertSpecificPageToImage_out.jpg");
```

## 如何轉換 OneNote 頁面為圖像（替代情境）

若需 **批次轉換 OneNote 頁面圖像**，只要將上述程式碼放入迴圈，遍歷 `Document.getPages()`。在每次迭代中呼叫 `options.setPageIndex(i)`，並可自行調整 `options.setQuality(90)` 以控制 JPEG 壓縮品質。

## 常見問題與解決方案

| 問題 | 原因 | 解決方式 |
|------|------|----------|
| **圖像為空白** | 頁面索引超出範圍或文件未正確載入。 | 確認 `options.setPageIndex` 位於 `0 .. document.getPages().size() - 1` 之間。 |
| **不支援的格式** | 使用較舊的 Aspose.Note 版本，缺少某些格式支援。 | 更新至最新的 Aspose.Note for Java 版本。 |
| **OutOfMemoryError** | 在記憶體不足的 JVM 上轉換過大頁面。 | 增加堆積大小 (`-Xmx2g`) 或一次只處理單一頁面。 |

## 常見問答

**Q1：可以使用此方法一次轉換多個頁面為圖像嗎？**  
A：可以。將儲存邏輯包在迴圈中，並在每次迭代時變更 `options.setPageIndex(i)` 即可匯出多頁。

**Q2：Aspose.Note 是否相容於不同版本的 OneNote 檔案？**  
A：完全相容。Aspose.Note 支援 OneNote 2007、2010、2013 以及之後版本的 `.one` 檔案。

**Q3：在轉換過程中可以自訂圖像格式與品質嗎？**  
A：可以。使用 `SaveFormat.Png`、`SaveFormat.Bmp` 等設定格式，並透過 `options.setQuality(int)` 調整 JPEG 品質（0‑100）。

**Q4：Aspose.Note 是否提供其他程式語言的支援？**  
A：有提供。除了 Java，亦有 .NET、Python、C++ 等語言的函式庫。

**Q5：在哪裡可以取得更多支援或協助？**  
A：請前往 [Aspose.Note 論壇](https://forum.aspose.com/c/note/28) 或參考官方文件 [此處](https://reference.aspose.com/note/java/)。

---

**最後更新：** 2025-11-29  
**測試環境：** Aspose.Note for Java 24.12  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}