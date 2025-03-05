---
title: 在 OneNote 中指定儲存選項 - Aspose.Note
linktitle: 在 OneNote 中指定儲存選項 - Aspose.Note
second_title: Aspose.Note Java API
description: 了解如何使用 Aspose.Note for Java 在 OneNote 中指定儲存選項。輕鬆自訂頁面索引、計數和壓縮設定。
type: docs
weight: 24
url: /zh-hant/java/onenote-document-saving/specify-save-options/
---
## 介紹

在本教學中，我們將學習如何使用 Aspose.Note for Java 在 OneNote 中指定儲存選項。 Aspose.Note 是一個功能強大的 Java 程式庫，可讓開發人員以程式設計方式建立、操作和轉換 OneNote 文件。使用Aspose.Note，您可以輕鬆控制各種保存選項，以根據您的要求自訂輸出。

## 先決條件

在開始之前，請確保您具備以下先決條件：

1. Java 程式語言的基礎知識。
2. 系統上安裝了 JDK（Java 開發工具包）。
3. 安裝了 Java 函式庫的 Aspose.Note。您可以從以下位置下載：[這裡](https://releases.aspose.com/note/java/).

## 導入包

首先，在 Java 程式碼中匯入必要的套件：

```java
import com.aspose.note.Document;
import com.aspose.note.PdfImageCompression;
import com.aspose.note.PdfSaveOptions;
import java.io.IOException;
```

讓我們將該範例分解為多個步驟：

## 步驟1：載入OneNote文檔

```java
//文檔目錄的路徑。
String dataDir = "Your Document Directory";

//將文件載入到 Aspose.Note 中。
Document doc = new Document(dataDir + "Aspose.one");
```

在這一步驟中，我們指定 OneNote 文件的路徑並將其載入到`Document`目的。

## 步驟 2：初始化 PdfSaveOptions 對象

```java
//初始化 PdfSaveOptions 對象
PdfSaveOptions opts = new PdfSaveOptions();
```

在這裡，我們初始化一個`PdfSaveOptions`對象，用於指定將文件另存為 PDF 的選項。

## 步驟 3：設定頁面索引和計數

```java
//設定頁面索引
opts.setPageIndex(2);

//設定頁數
opts.setPageCount(3);
```

這些行設定要儲存的頁面的索引和計數。在此範例中，我們將從索引 2 開始儲存頁面，總共 3 個頁面。

## 步驟 4：指定壓縮設定

```java
//如果需要指定壓縮
opts.setImageCompression(PdfImageCompression.Jpeg);
opts.setJpegQuality(90);
```

在這裡，我們指定 PDF 的圖像壓縮設定。我們將壓縮設定為 JPEG 格式，並將 JPEG 品質指定為 90%。

## 第 5 步：使用選項儲存文檔

```java
dataDir = dataDir + "Document.SaveWithOptions_out.pdf";
doc.save(dataDir, opts);
```

最後，我們使用指定的選項來儲存文件。輸出的 PDF 將使用給定選項保存在指定位置。

## 結論

在本教學中，我們學習如何使用 Aspose.Note for Java 在 OneNote 中指定儲存選項。透過自訂儲存選項，您可以控制輸出文件的各個方面，例如頁面索引、計數和壓縮設定。

## 常見問題解答

### Q1：Aspose.Note 可以處理大型 OneNote 文件嗎？

A1：是的，Aspose.Note 旨在高效處理大型 OneNote 文件。

### Q2：Aspose.Note 與最新的 Java 版本相容嗎？

A2：是的，Aspose.Note 與最新的 Java 版本相容。

### Q3：我可以使用Aspose.Note 將OneNote 文件轉換為其他格式嗎？

A3：是的，Aspose.Note 支援將 OneNote 文件轉換為 PDF、DOCX 和 HTML 等各種格式。

### Q4：Aspose.Note是否支援OneNote文件的加密和解密？

A4：是的，Aspose.Note 提供了 OneNote 文件加密和解密的 API。

### Q5：Aspose.Note適合商業用途嗎？

A5：是的，Aspose.Note可以透過購買許可證用於商業目的。