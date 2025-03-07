---
title: 使用 OneNote 中的影像儲存選項儲存到 TIFF 影像
linktitle: 使用 OneNote 中的影像儲存選項儲存到 TIFF 影像
second_title: Aspose.Note Java API
description: 將 OneNote 文件轉換為 TIFF 並控製文件大小和品質！在 Java 中選擇 Jpeg、PackBits 或 Fax 壓縮。取得程式碼範例並了解如何操作！ #OneNote #Java #Aspose
weight: 21
url: /zh-hant/java/onenote-document-saving/save-to-tiff-image-using-image-save-options/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 使用 OneNote 中的影像儲存選項儲存到 TIFF 影像

## 介紹

在本教學中，您將學習如何在 Aspose.Note for Java 中使用不同的壓縮方法將文件儲存為 TIFF 影像格式。我們將介紹先決條件、匯入包，並為每種壓縮方法提供逐步指南。

## 先決條件

在開始之前，請確保您具備以下條件：

- 您的系統上安裝了 Java 開發工具包 (JDK)。
- 下載並配置了 Aspose.Note for Java 函式庫。
- 對 Java 程式語言有基本的了解。

## 導入包

首先，您需要將必要的套件匯入到您的 Java 檔案中：

```java
import com.aspose.note.*;
import java.io.IOException;
import java.nio.file.Paths;
```

## 第 1 步：使用 JPEG 壓縮儲存為 TIFF

```java
public static void SaveToTiffUsingJpegCompression() throws IOException {
    //文檔目錄的路徑。
    String dataDir = "Your Document Directory";

    //將文件載入到 Aspose.Note 中。
    Document oneFile = new Document(Paths.get(dataDir, "Aspose.one").toString());

    ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);
    options.setTiffCompression(TiffCompression.Jpeg);
    options.setQuality(93);

    oneFile.save(Paths.get(dataDir,"SaveToTiffUsingJpegCompression.tiff").toString(), options);
}
```

- 使用載入文檔`Document`班級。
- 建立一個實例`ImageSaveOptions`並將 TIFF 壓縮類型指定為 JPEG。
- 設定所需的品質（可選）。
- 使用指定選項將文件儲存為 TIFF 格式。

## 步驟 2：使用 PackBits 壓縮儲存為 TIFF

```java
public static void SaveToTiffUsingPackBitsCompression() throws IOException {
    //文檔目錄的路徑。
    String dataDir = "Your Document Directory";

    //將文件載入到 Aspose.Note 中。
    Document oneFile = new Document(Paths.get(dataDir, "Aspose.one").toString());

    ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);
    options.setTiffCompression(TiffCompression.PackBits);

    oneFile.save(Paths.get(dataDir, "SaveToTiffUsingPackBitsCompression.tiff").toString(), options);
}
```

- 使用載入文檔`Document`班級。
- 建立一個實例`ImageSaveOptions`並將 TIFF 壓縮類型指定為 PackBits。
- 使用指定選項將文件儲存為 TIFF 格式。

## 步驟 3：使用 CCITT Group 3 傳真壓縮保存為 TIFF

```java
public static void SaveToTiffUsingCcitt3Compression() throws IOException {
    //文檔目錄的路徑。
    String dataDir = "Your Document Directory";

    //將文件載入到 Aspose.Note 中。
    Document oneFile = new Document(Paths.get(dataDir, "Aspose.one").toString());

    ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);
    options.setColorMode(ColorMode.BlackAndWhite);
    options.setTiffCompression(TiffCompression.Ccitt3);

    oneFile.save(Paths.get(dataDir, "SaveToTiffUsingCcitt3Compression.tiff").toString(), options);
}
```

- 使用載入文檔`Document`班級。
- 建立一個實例`ImageSaveOptions`並將 TIFF 壓縮類型指定為 CCITT Group 3 Fax。
- 將顏色模式設定為黑白。
- 使用指定選項將文件儲存為 TIFF 格式。

## 結論

在本教學中，您學習如何在 Aspose.Note for Java 中使用不同的壓縮方法將文件儲存為 TIFF 影像格式。透過遵循逐步指南，您可以有效地利用 Aspose.Note 的功能來滿足您的要求。

## 常見問題解答

### Q1：我可以使用Aspose.Note for Java將其他文件格式轉換為TIFF嗎？

A1: 是的，Aspose.Note for Java 支援各種文件格式到 TIFF 的轉換，包括 OneNote 文件。

### Q2：儲存為TIFF時指定壓縮類型有何意義？

A2：指定壓縮類型可以控制影像品質和檔案大小。不同的壓縮方法在質量和壓縮比之間進行權衡。

### Q3：Aspose.Note for Java適合批次處理文件嗎？

A3：是的，Aspose.Note for Java 提供了用於批次的 API，使您能夠有效率地自動執行文件轉換任務。

### Q4：我可以進一步自訂壓縮設定嗎？

A4: 是的，您可以調整品質、解析度和壓縮方法等參數，以根據您的要求自訂輸出。

### Q5：Aspose.Note for Java 提供技術支援嗎？

A5：是的，Aspose 透過論壇和基於票證的系統提供全面的技術支援。
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
