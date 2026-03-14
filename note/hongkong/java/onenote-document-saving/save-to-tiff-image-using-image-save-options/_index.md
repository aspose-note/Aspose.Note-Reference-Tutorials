---
date: 2026-03-14
description: 了解如何在 Java 中使用 TIFF JPEG 壓縮、TIFF PackBits 壓縮或 CCITT Group 3 傳真壓縮，將 OneNote
  文件儲存為 TIFF 檔案。使用 Aspose.Note 控制影像品質、檔案大小與色彩模式。
linktitle: Save to TIFF Image Using TIFF JPEG Compression in OneNote
second_title: Aspose.Note Java API
title: 在 OneNote 中使用 TIFF JPEG 壓縮儲存為 TIFF 圖像
url: /zh-hant/java/onenote-document-saving/save-to-tiff-image-using-image-save-options/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 使用 TIFF JPEG 壓縮在 OneNote 中儲存為 TIFF 圖像

## 簡介

在本教學中，您將了解 **如何使用 TIFF JPEG 壓縮將 OneNote 文件儲存為 TIFF 檔案**，以及另外兩種常用的壓縮方法。我們將逐步說明所需的設定、匯入必要的 Java 套件，並提供每種壓縮選項的清晰逐步程式碼。完成後，您將能夠控制 **TIFF 圖像品質**、減少檔案大小，甚至產生適用於傳真式輸出的黑白 TIFF。

## 快速解答
- **什麼是 TIFF JPEG 壓縮？** 一種有損壓縮方法，可在保留視覺品質的同時減少 TIFF 檔案大小。  
- **哪個函式庫負責轉換？** Aspose.Note for Java。  
- **我需要授權嗎？** 免費試用可用於測試；正式環境需購買授權。  
- **我可以調整圖像品質嗎？** 可以，設定 `ImageSaveOptions` 的 `quality` 屬性。  
- **是否支援批次轉換？** 當然可以——遍歷文件並套用相同的選項。

## 什麼是 TIFF JPEG 壓縮？

TIFF JPEG 壓縮將影像資料存放於 TIFF 容器中，但使用 JPEG 的有損演算法來縮小檔案。當您需要在 **tiff 圖像品質** 與較小檔案大小之間取得平衡時，這是理想的選擇，尤其適用於網路或存檔情境。

## 為什麼要使用不同的 TIFF 壓縮類型？

- **JPEG** – 適合照片；提供可調整的品質。  
- **PackBits** – 簡單的無損行程長度編碼；適用於具有大面積均勻區域的圖形。  
- **CCITT Group 3 Fax** – 僅限黑白；非常適合掃描文件與傳真傳輸。  

選擇合適的壓縮方式可讓您在不犧牲應用所需視覺真實度的前提下，符合儲存空間限制。

## 使用 Aspose.Note 將 One 轉換為 TIFF

如果您的目標是 **將 OneNote 轉換為 TIFF**，以下三種方法涵蓋最常見的情境。每種方法都會載入 `.one` 檔案、設定 `ImageSaveOptions`，並將結果儲存為 `.tiff` 檔案。

## 先決條件

- 已安裝 Java Development Kit (JDK)。  
- 已將 Aspose.Note for Java 函式庫加入專案（Maven/Gradle 或手動 JAR）。  
- 具備基本的 Java 語法知識。

## 匯入套件

首先，將必要的 Aspose.Note 類別匯入您的 Java 檔案：

```java
import com.aspose.note.*;
import java.io.IOException;
import java.nio.file.Paths;
```

## 步驟 1：使用 TIFF JPEG 壓縮儲存為 TIFF

以下為完整的方法，載入 OneNote 檔案並以 JPEG 壓縮儲存為 TIFF。調整 `quality` 值（0‑100）即可控制 **tiff 圖像品質**。

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

- `ImageSaveOptions` 告訴 Aspose.Note 輸出 TIFF 檔案。  
- `setTiffCompression(TiffCompression.Jpeg)` 選擇 JPEG 壓縮。  
- `setQuality(93)`（可選）微調圖像品質；較低的數值會產生較小的檔案。

### 如何在 Java 中使用 JPEG 壓縮儲存 TIFF
1. 將 `dataDir` 指向包含 `.one` 檔案的資料夾。  
2. 從主方法或服務呼叫 `SaveToTiffUsingJpegCompression()`。  
3. 產生的 `.tiff` 檔案會出現在相同目錄下。

## TIFF PackBits 壓縮概述

PackBits 是一種無損壓縮演算法，最適合用於具有大面積純色區域的影像。文件中常稱其為 **tiff packbits compression**。

## 步驟 2：使用 PackBits 壓縮儲存為 TIFF

如果您需要無損選項，PackBits 是一種簡單的行程長度演算法，適用於具有純色的圖形。

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
- 不需要設定品質，因為 PackBits 為無損壓縮。

## 步驟 3：使用 CCITT Group 3 Fax 壓縮儲存為 TIFF（黑白 TIFF）

對於傳真式文件，您通常需要 **黑白 TIFF**。CCITT Group 3 為單色影像提供高壓縮率。

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
- `setTiffCompression(TiffCompression.Ccitt3)` 套用針對傳真的壓縮方式。

## 常見問題與技巧

| 問題 | 解決方案 |
|-------|----------|
| **輸出檔案比預期更大** | 嘗試降低 JPEG `quality` 值，或在接受無損的情況下改用 PackBits。 |
| **顏色看起來褪色** | 確保在需要全彩時未不小心設定 `ColorMode.BlackAndWhite`。 |
| **不支援的影像格式錯誤** | 確認您使用的是最新版本的 Aspose.Note；較舊的版本可能缺少某些壓縮列舉。 |
| **執行時 LicenseException** | 安裝有效的 Aspose.Note 授權 (`License license = new License(); license.setLicense("Aspose.Note.Java.lic");`)。 |

## 常見問與答

**Q: 我可以使用這些選項將其他文件類型（例如 PDF、DOCX）轉換為 TIFF 嗎？**  
A: 可以。雖然 Aspose.Note 主要針對 OneNote 檔案，Aspose.PDF、Aspose.Words 以及其他函式庫亦提供相似的 `ImageSaveOptions` 供其格式使用。

**Q: TIFF JPEG 壓縮與標準 JPEG 檔案有何不同？**  
A: JPEG 演算法相同，但影像資料存於 TIFF 容器中，該容器可容納多頁及更豐富的中繼資料。

**Q: 是否可以批次處理大量 `.one` 檔案？**  
A: 當然可以。遍歷目錄，對每個檔案呼叫任一三種方法，並收集產生的 TIFF。

**Q: 我可以控制輸出 TIFF 的 DPI/解析度嗎？**  
A: 可以。儲存前使用 `options.setResolution(int dpi)`。

**Q: Aspose.Note 支援非同步處理嗎？**  
A: API 本身是同步的，但您可以將呼叫包裝在 Java 的 `CompletableFuture` 或執行緒池中，以實現平行執行。

## 結論

您現在擁有完整的 **java tiff 轉換** 工具箱，可使用 JPEG、PackBits 或 CCITT Group 3 Fax 壓縮將 OneNote 文件儲存為 TIFF 檔案。調整品質、顏色模式與解析度，以符合您特定的 **tiff 圖像品質** 需求，並將這些方法整合至批次工作流程，以達到最高生產力。

---

**Last Updated:** 2026-03-14  
**Tested With:** Aspose.Note for Java 23.12 (latest at time of writing)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}