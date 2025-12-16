---
date: 2025-12-16
description: 學習如何使用 Aspose.Note for Java 的圖像儲存選項，將 OneNote 文件儲存為 BMP 圖像。另請參閱如何將 OneNote
  儲存為 PDF 或 PNG。
linktitle: how to save onenote to BMP Image Using Image Save Options
second_title: Aspose.Note Java API
title: 如何使用圖像儲存選項將 OneNote 儲存為 BMP 圖像
url: /zh-hant/java/onenote-document-saving/save-to-bmp-image-using-image-save-options/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何使用 Image Save Options 將 OneNote 儲存為 BMP 圖像

## 介紹

Aspose.Note for Java 是一個功能強大的函式庫，讓 Java 開發人員能以程式方式操作 Microsoft OneNote 檔案。**在本教學中，您將學會如何使用 Aspose.Note for Java 的 Image Save Options 功能，將 OneNote 文件儲存為 BMP 圖像**。我們將逐步說明每個步驟，解釋為何會選擇 BMP 而非其他格式，並示範如何將此功能整合到自己的應用程式中。

## 快速答覆
- **Image Save Options 類別的作用是什麼？** 它讓您在將 OneNote 頁面轉換為圖像時，指定輸出圖像格式（BMP、PNG、JPEG 等）。  
- **執行範例是否需要授權？** 免費試用可用於評估，但正式上線需購買商業授權。  
- **我可以將 OneNote 頁面轉換為 PDF 或 PNG 而不是 BMP 嗎？** 可以，只需更改 `SaveFormat` 列舉（例如 `SaveFormat.Pdf` 或 `SaveFormat.Png`）。  
- **支援哪個 Java 版本？** 完全支援 Java 8 及以上版本。  
- **大型文件有特別處理方式嗎？** 您可以將輸出以串流方式寫入，以避免記憶體使用過高。

## Aspose.Note 中的「Image Save Options」是什麼？
`ImageSaveOptions` 類別提供了對 OneNote 頁面渲染為點陣圖的精細控制。您可以設定圖像格式、解析度、色深等。此彈性讓您能輕鬆產生適用於舊版系統的 BMP 檔，或適合網路使用的 PNG/JPEG 檔。

## 前置條件

在開始之前，請確保您已具備以下條件：

1. 具備基本的 Java 程式語言知識。  
2. 已在電腦上安裝 JDK（Java Development Kit）。  
3. 有 Eclipse、IntelliJ IDEA 等開發環境。  
4. 取得 Aspose.Note for Java 函式庫——可從 [此處](https://releases.aspose.com/note/java/) 下載。

## 匯入套件

首先，匯入必要的 Aspose.Note 類別與標準 Java I/O 工具：

```java
import com.aspose.note.*;
import java.io.IOException;
```

## 步驟 1：載入 OneNote 文件

```java
// The path to the documents directory.
String dataDir = "Your Document Directory";

// Load the document into Aspose.Note.
Document oneFile = new Document(dataDir + "Aspose.one");
```

此處我們指向包含來源 OneNote 檔案（`Aspose.one`）的資料夾，並將其載入為 `Document` 物件。此物件讓您完整存取筆記本中的頁面、分區與其他元素。

## 步驟 2：將文件儲存為 BMP 圖像

```java
dataDir = dataDir + "SaveToBmpImageUsingImageSaveOptions_out.bmp";

// Save the document.
oneFile.save(dataDir, new ImageSaveOptions(SaveFormat.Bmp));
```

我們先組合輸出檔名，然後使用已設定為 **BMP**（`SaveFormat.Bmp`）的 `ImageSaveOptions` 實例呼叫 `save`。  
若要 **將 OneNote 頁面儲存為 PNG**，只需將 `SaveFormat.Bmp` 改為 `SaveFormat.Png`。同理，`SaveFormat.Pdf` 可執行 **OneNote 轉 PDF** 的轉換。

## 為何選擇 BMP？
- **無損品質** – BMP 直接儲存原始像素資料，完整保留原始頁面的外觀。  
- **相容性** – 許多舊版 Windows 應用程式仍要求使用 BMP 檔案。  
- **簡單易用** – 無壓縮雜訊，適合後續的影像處理工作。

## 常見問題與小技巧

- **檔案路徑錯誤** – 確認 `dataDir` 以正確的檔案分隔符（`/` 或 `\`）結尾。  
- **大型筆記本** – 對於非常大的 OneNote 檔案，建議逐頁儲存，以降低記憶體使用量。  
- **授權例外** – 未使用有效授權執行程式碼時，產生的圖像會加上浮水印。

## 結論

本指南示範了如何使用 Aspose.Note for Java 的 `ImageSaveOptions` **將 OneNote 文件儲存為 BMP 圖像**。只要切換 `SaveFormat` 列舉，您同樣可以產生 PNG、JPEG、PDF 或其他支援的格式，為 OneNote 內容的下游應用提供彈性匯出方式。

## 常見問答

**Q1：我可以將 OneNote 文件儲存為 BMP 以外的其他圖像格式嗎？**  
A：可以，使用 `ImageSaveOptions` 搭配 `SaveFormat.Png`、`SaveFormat.Jpeg`、`SaveFormat.Gif` 或 `SaveFormat.Tiff` 即可匯出相應格式。

**Q2：Aspose.Note for Java 是否支援不同文件格式之間的轉換？**  
A：當然支援。除了圖像格式外，您還可以使用相應的 `SaveFormat` 將 OneNote 檔案轉換為 PDF、DOCX、HTML 等。

**Q3：Aspose.Note for Java 是否與最新版本的 OneNote 相容？**  
A：是的，函式庫會定期更新，以保持與最新 OneNote 版本的相容性。

**Q4：我可以以程式方式操作 OneNote 文件的內容嗎？**  
A：可以，您可以透過 API 新增、編輯或刪除頁面、分區以及富內容（文字、圖像、表格）等。

**Q5：Aspose.Note for Java 是否提供技術支援？**  
A：提供。Aspose 有技術支援與專屬論壇。請前往 [Aspose.Note forum](https://forum.aspose.com/c/note/28) 取得協助。

---

**最後更新：** 2025-12-16  
**測試環境：** Aspose.Note for Java 24.12  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
