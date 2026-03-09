---
date: 2025-12-17
description: 學習如何在 Java 中使用 TIFF JPEG 壓縮、PackBits 或 CCITT Group 3 傳真，將 OneNote 文件儲存為
  TIFF 檔案。使用 Aspose.Note 控制影像品質、檔案大小與色彩模式。
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

## 介紹

在本教學中，您將學會 **如何使用 TIFF JPEG 壓縮將 OneNote 文件儲存為 TIFF 檔案**，以及另外兩種常用的壓縮方式。我們會一步步說明所需的設定、匯入必要的 Java 套件，並提供每種壓縮選項的完整程式碼範例。完成後，您即可自行控制 **TIFF 圖像品質**、減少檔案大小，甚至產生適合傳真的黑白 TIFF。

## 快速回答
- **什麼是 TIFF JPEG 壓縮？** 一種有損壓縮方法，可在降低 TIFF 檔案大小的同時保留視覺品質。  
- **哪個函式庫負責轉換？** Aspose.Note for Java。  
- **需要授權嗎？** 免費試用可用於測試；正式環境需購買授權。  
- **可以調整圖像品質嗎？** 可以，於 `ImageSaveOptions` 設定 `quality` 屬性。  
- **支援批次轉換嗎？** 完全支援，只要在迴圈中套用相同的選項即可。

## 什麼是 TIFF JPEG 壓縮？
TIFF JPEG 壓縮將影像資料存放於 TIFF 容器中，同時使用 JPEG 的有損演算法來縮小檔案。當您需要在 **tiff 圖像品質** 與較小檔案大小之間取得平衡，尤其是用於網站或歸檔情境時，這是一個理想的選擇。

## 為什麼要使用不同的 TIFF 壓縮類型？
- **JPEG** – 適合照片，提供可調整的品質。  
- **PackBits** – 簡單的無損行程長度編碼，適用於具有大面積單色區塊的圖形。  
- **CCITT Group 3 Fax** – 僅限黑白，完美適用於掃描文件與傳真傳輸。  

選擇合適的壓縮方式，可在不犧牲應用所需的視覺忠實度下，滿足儲存空間的限制。

## 前置條件

- 已安裝 Java Development Kit (JDK)。  
- 已將 Aspose.Note for Java 套件加入專案（Maven/Gradle 或手動 JAR）。  
- 具備基本的 Java 語法知識。

## 匯入套件

首先，將必要的 Aspose.Note 類別匯入您的 Java 檔案：

```java
import com.aspose.note.*;
import java.io.IOException;
import java.nio.file.Paths;
```

## 步驟 1：使用 TIFF JPEG 壓縮儲存為 TIFF

以下為完整方法，會載入 OneNote 檔案並以 JPEG 壓縮儲存為 TIFF。調整 `quality` 值 (0‑100) 以控制 **tiff 圖像品質**。

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
- `setQuality(93)`（可選）微調圖像品質；數值越低檔案越小。

### 如何在 Java 中使用 JPEG 壓縮儲存 TIFF
1. 將 `dataDir` 指向包含 `.one` 檔案的資料夾。  
2. 從主程式或服務呼叫 `SaveToTiffUsingJpegCompression()`。  
3. 產生的 `.tiff` 檔案會出現在同一目錄下。

## 步驟 2：使用 PackBits 壓縮儲存為 TIFF

如果需要無損選項，PackBits 是一種簡單的行程長度演算法，適合單色或純色圖形。

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

## 步驟 3：使用 CCITT Group 3 Fax 壓縮（黑白 TIFF）

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
|------|----------|
| **輸出檔案比預期大** | 嘗試降低 JPEG `quality` 值，或在可接受無損的情況下改用 PackBits。 |
| **顏色看起來淡化** | 確認未不小心設定 `ColorMode.BlackAndWhite`，若需要全彩請移除該設定。 |
| **不支援的影像格式錯誤** | 確認使用的是最新版本的 Aspose.Note；舊版可能缺少某些壓縮列舉。 |
| **執行時出現 LicenseException** | 安裝有效的 Aspose.Note 授權 (`License license = new License(); license.setLicense("Aspose.Note.Java.lic");`)。 |

## 常見問答

**Q: 我可以將其他文件類型（例如 PDF、DOCX）轉換為 TIFF 並使用這些選項嗎？**  
A: 可以。Aspose.Note 主要針對 OneNote 檔案，但 Aspose 其他套件（PDF、Words）亦提供類似的 `ImageSaveOptions` 供各自格式使用。

**Q: TIFF JPEG 壓縮與一般 JPEG 檔案有何不同？**  
A: 圖像資料存放在 TIFF 容器內，保留更多中繼資料且支援多頁，而壓縮演算法仍為 JPEG。

**Q: 能否批次處理大量 `.one` 檔案？**  
A: 完全可以。遍歷資料夾，對每個檔案呼叫任一方法，最後收集產生的 TIFF 即可。

**Q: 我可以控制輸出 TIFF 的 DPI/解析度嗎？**  
A: 可以。在儲存前使用 `options.setResolution(int dpi)` 設定。

**Q: Aspose.Note 支援非同步處理嗎？**  
A: API 本身為同步，但您可將呼叫包裝於 Java 的 `CompletableFuture` 或執行緒池，以實現平行處理。

## 結論

現在您已擁有完整的 **java tiff 轉換** 工具箱，能以 JPEG、PackBits 或 CCITT Group 3 Fax 壓縮方式將 OneNote 文件儲存為 TIFF。依需求調整品質、色彩模式與解析度，以符合特定的 **tiff 圖像品質** 要求，並將這些方法整合至批次工作流程中，提升生產力。

---

**最後更新日期：** 2025-12-17  
**測試環境：** Aspose.Note for Java 23.12（撰寫時的最新版本）  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}