---
date: 2026-11-05
description: 了解如何在 Java 中使用 Aspose.Note 將 OneNote 筆記本轉換為 TIFF 時減少 TIFF 檔案大小。包括 JPEG、PackBits
  以及黑白 TIFF 選項。
keywords:
- reduce tiff file size
- black white tiff
- tiff jpeg compression
- aspose note java
lastmod: 2026-11-05
linktitle: 在 Java 中將 OneNote 轉換為 TIFF 時，如何減少 TIFF 檔案大小
og_description: 了解如何在 Java 中使用 Aspose.Note 將 OneNote 筆記本轉換為 TIFF 時減少 TIFF 檔案大小。包括
  JPEG、PackBits 以及黑白 TIFF 選項。
og_image_alt: Developer guide showing OneNote to TIFF conversion with compression
  options in Java
og_title: 在 Java 中將 OneNote 轉換為 TIFF 時，如何減少 TIFF 檔案大小
schemas:
- author: Aspose
  dateModified: '2026-11-05'
  description: Learn how to reduce TIFF file size when converting OneNote notebooks
    to TIFF in Java using Aspose.Note. Includes JPEG, PackBits and black‑white TIFF
    options.
  headline: How to reduce TIFF file size when converting OneNote in Java
  type: TechArticle
- description: Learn how to reduce TIFF file size when converting OneNote notebooks
    to TIFF in Java using Aspose.Note. Includes JPEG, PackBits and black‑white TIFF
    options.
  name: How to reduce TIFF file size when converting OneNote in Java
  steps:
  - name: Point `dataDir` to the folder containing your `.one` file.
    text: Point `dataDir` to the folder containing your `.one` file.
  - name: Call `SaveToTiffUsingJpegCompression()` from your main method or service.
    text: Call `SaveToTiffUsingJpegCompression()` from your main method or service.
  - name: The resulting `.tiff` file will appear in the same directory.
    text: The resulting `.tiff` file will appear in the same directory.
  type: HowTo
- questions:
  - answer: Yes. While Aspose.Note focuses on OneNote files, Aspose.PDF, Aspose.Words,
      and other libraries provide similar `ImageSaveOptions` for their formats.
    question: Can I convert other document types (e.g., PDF, DOCX) to TIFF with these
      options?
  - answer: The JPEG algorithm is the same, but the image data lives inside a TIFF
      container, which can hold multiple pages and richer metadata.
    question: How does TIFF JPEG compression differ from a standard JPEG file?
  - answer: Absolutely. Iterate over a directory, call any of the three methods for
      each file, and collect the resulting TIFFs.
    question: Is it possible to batch‑process many `.one` files?
  - answer: Yes. Use `options.setResolution(int dpi)` before saving.
    question: Can I control the DPI/resolution of the output TIFF?
  - answer: The API itself is synchronous, but you can wrap calls in Java’s `CompletableFuture`
      or a thread pool for parallel execution.
    question: Does Aspose.Note support asynchronous processing?
  type: FAQPage
second_title: Aspose.Note Java API
tags:
- reduce tiff file size
- aspose.note
- java tiff conversion
- black white tiff
- image compression
title: 在 Java 中將 OneNote 轉換為 TIFF 時，如何減少 TIFF 檔案大小
url: /zh-hant/java/onenote-document-saving/save-to-tiff-image-using-image-save-options/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 在 Java 中將 OneNote 轉換為 TIFF 時減少檔案大小

## 介紹

在本教學中，您將學會在使用 Aspose.Note for Java 將 OneNote 筆記本轉換為 TIFF 圖像時，**減少 TIFF 檔案大小**。我們將介紹三種壓縮方法——TIFF JPEG、PackBits 與 CCITT Group 3（黑白 TIFF），並說明如何調整影像品質、控制色彩模式，讓檔案大小在網路、歸檔或傳真等情境下保持最佳。

## 快速回答
- **什麼是 TIFF JPEG 壓縮？** 一種有損壓縮方法，可在保留視覺品質的同時減少 TIFF 檔案大小。  
- **哪個函式庫負責轉換？** Aspose.Note for Java。  
- **需要授權嗎？** 免費試用可用於測試；正式環境需購買授權。  
- **可以調整影像品質嗎？** 可以，設定 `ImageSaveOptions` 的 `quality` 屬性。  
- **支援批次轉換嗎？** 完全支援，只要在迴圈中對每個文件套用相同的選項即可。

## TIFF JPEG 壓縮概述

TIFF JPEG 壓縮將影像資料存放於 TIFF 容器中，但使用 JPEG 的有損演算法來縮小檔案。當您需要在 **tiff 影像品質** 與較小檔案大小之間取得平衡，尤其是用於網路或歸檔情境時，這是理想的選擇。

## 為何使用不同的 TIFF 壓縮類型？

您可以根據內容與儲存需求選擇壓縮類型：JPEG 最適合照片，PackBits 為圖形提供無損壓縮（適合大面積單色區域），CCITT Group 3 則為單色傳真式文件提供高比例壓縮。選對方法即可 **減少 TIFF 檔案大小**，同時不影響應用程式所需的視覺忠實度。

## 選擇合適的壓縮方式

- **JPEG** – 可調整品質（0‑100），讓您在檔案大小與細節之間取得平衡，適合彩色豐富的頁面。  
- **PackBits** – 無損的跑長編碼；當必須保留每個像素時的理想選擇。  
- **CCITT Group 3** – 僅限單色；為掃描文字或傳真文件提供最大壓縮率。  

## 使用 Aspose.Note 將 OneNote 轉換為 TIFF

如果您的目標是 **將 OneNote 轉換為 TIFF**，以下三種方法涵蓋最常見的情境。每種方法皆會載入 `.one` 檔案、設定 `ImageSaveOptions`，並將結果儲存為 `.tiff` 檔案。

## 前置條件

- 已安裝 Java Development Kit（JDK）。  
- 已將 Aspose.Note for Java 套件加入專案（Maven/Gradle 或手動 JAR）。  
- 具備基本的 Java 語法概念。

## 匯入套件

`ImageSaveOptions`、`TiffCompression` 與 `ColorMode` 類別是轉換 API 的核心。

`ImageSaveOptions` 定義了儲存影像的選項，例如格式與壓縮方式。  
`TiffCompression` 列舉了支援的 TIFF 壓縮演算法。  
`ColorMode` 指定色彩深度，例如彩色或黑白。

```java
// Placeholder for import statements – keep your imports here
```

```java
import com.aspose.note.*;
import java.io.IOException;
import java.nio.file.Paths;
```

## 步驟 1：使用 TIFF JPEG 壓縮儲存為 TIFF

### 在 Java 中使用 JPEG 壓縮儲存 TIFF

載入 OneNote 檔案、以 JPEG 壓縮設定 `ImageSaveOptions`，可選擇設定 `quality` 值，最後呼叫儲存方法。這個兩步驟模式讓您完整掌控輸出大小與視覺忠實度。

1. 將 `dataDir` 指向存放 `.one` 檔案的資料夾。  
2. 從主程式或服務呼叫 `SaveToTiffUsingJpegCompression()`。  
3. 產生的 `.tiff` 檔案會出現在相同目錄下。

```java
// Placeholder for the JPEG compression method implementation
```

```java
public static void SaveToTiffUsingJpegCompression() throws IOException {
    // The path to the documents directory.
    String dataDir = "Your Document Directory";

    // Load the document into Aspose.Note.
    Document oneFile = new Document(Paths.get(dataDir, "Aspose.one").toString());

    ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);
    options.setTiffCompression(TiffCompression.Jpeg);
    options.setQuality(93);

    oneFile.save(Paths.get(dataDir,"SaveToTiffUsingJpegCompression.tiff").toString(), options);
}
```

**說明**

- `ImageSaveOptions` 告訴 Aspose.Note 輸出為 TIFF 檔案。  
- `setTiffCompression(TiffCompression.Jpeg)` 選擇 JPEG 壓縮。  
- `setQuality(93)`（可選）微調影像品質；數值越低檔案越小。

## TIFF PackBits 壓縮概述

PackBits 是一種無損壓縮演算法，最適合大面積單色區塊的影像。文件中常將其稱為 **tiff packbits compression**。

## 在 Java 中使用 PackBits 壓縮儲存 TIFF

若需要無損選項，PackBits 是簡單的跑長編碼，適合純色圖形。只要將 `ImageSaveOptions` 設為 `TiffCompression.PackBits` 後儲存文件即可。

```java
// Placeholder for the PackBits compression method implementation
```

```java
public static void SaveToTiffUsingPackBitsCompression() throws IOException {
    // The path to the documents directory.
    String dataDir = "Your Document Directory";

    // Load the document into Aspose.Note.
    Document oneFile = new Document(Paths.get(dataDir, "Aspose.one").toString());

    ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);
    options.setTiffCompression(TiffCompression.PackBits);

    oneFile.save(Paths.get(dataDir, "SaveToTiffUsingPackBitsCompression.tiff").toString(), options);
}
```

**說明**

- `setTiffCompression(TiffCompression.PackBits)` 變更壓縮方式。  
- 無需設定品質，因為 PackBits 為無損壓縮。

## 在 Java 中使用 CCITT Group 3 壓縮儲存 TIFF

對於傳真式文件，您通常需要 **黑白 TIFF**。CCITT Group 3 為單色影像提供高壓縮率。將色彩模式設定為黑白，並選擇 CCITT 3 壓縮列舉。

```java
// Placeholder for the CCITT Group 3 compression method implementation
```

```java
public static void SaveToTiffUsingCcitt3Compression() throws IOException {
    // The path to the documents directory.
    String dataDir = "Your Document Directory";

    // Load the document into Aspose.Note.
    Document oneFile = new Document(Paths.get(dataDir, "Aspose.one").toString());

    ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);
    options.setColorMode(ColorMode.BlackAndWhite);
    options.setTiffCompression(TiffCompression.Ccitt3);

    oneFile.save(Paths.get(dataDir, "SaveToTiffUsingCcitt3Compression.tiff").toString(), options);
}
```

**說明**

- `setColorMode(ColorMode.BlackAndWhite)` 強制輸出為單色。  
- `setTiffCompression(TiffCompression.Ccitt3)` 套用傳真導向的壓縮。

## 常見問題與技巧

| 問題 | 解決方案 |
|------|----------|
| **輸出檔案比預期大** | 嘗試降低 JPEG 的 `quality` 值，或在可接受無損的情況下改用 PackBits。 |
| **顏色看起來黯淡** | 確認未在需要全彩時誤設定 `ColorMode.BlackAndWhite`。 |
| **不支援的影像格式錯誤** | 確認使用的是最新版本的 Aspose.Note；舊版可能缺少某些壓縮列舉。 |
| **執行時出現 LicenseException** | 安裝有效的 Aspose.Note 授權 (`License license = new License(); license.setLicense("Aspose.Note.Java.lic");`)。 |

## 常見問答

**Q: 可以使用這些選項將其他文件類型（例如 PDF、DOCX）轉換為 TIFF 嗎？**  
A: 可以。雖然 Aspose.Note 主要針對 OneNote 檔案，Aspose.PDF、Aspose.Words 等套件亦提供類似的 `ImageSaveOptions` 供其格式使用。

**Q: TIFF JPEG 壓縮與一般 JPEG 檔案有何不同？**  
A: 演算法相同，但影像資料存放於 TIFF 容器中，容器可容納多頁與更豐富的中繼資料。

**Q: 能否批次處理大量 `.one` 檔案？**  
A: 完全可以。遍歷目錄，對每個檔案呼叫任一方法，並收集產生的 TIFF。

**Q: 能否控制輸出 TIFF 的 DPI/解析度？**  
A: 可以。在儲存前使用 `options.setResolution(int dpi)` 設定。

**Q: Aspose.Note 支援非同步處理嗎？**  
A: API 本身是同步的，但您可以將呼叫包裝在 Java 的 `CompletableFuture` 或執行緒池中，以實現平行執行。

## 結論

現在您已掌握完整的 **Java TIFF 轉換** 工具組，能在使用 JPEG、PackBits 或 CCITT Group 3 傳真壓縮將 OneNote 文件儲存為 TIFF 時 **減少 TIFF 檔案大小**。依需求調整品質、色彩模式與解析度，並將這些方法整合至批次工作流程，以達到最高生產力。

---

**最後更新：** 2026-11-05  
**測試環境：** Aspose.Note for Java 26.4（撰寫時的最新版本）  
**作者：** Aspose

## 相關教學

- [How to Render OneNote Page Image (JPEG) Using Save Format with Aspose.Note for Java](/note/java/onenote-document-saving/save-to-jpeg-image-using-save-format/)
- [Use Aspose.Note for Java to Save OneNote as PNG with Options – Convert Notebook to Image](/note/java/onenote-notebook-operations/convert-notebook-to-image-with-options/)
- [How to Export OneNote as Grayscale Image – Aspose.Note](/note/java/onenote-document-saving/save-to-grayscale-image/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}