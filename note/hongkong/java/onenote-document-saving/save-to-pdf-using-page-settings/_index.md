---
title: 使用 OneNote 中的頁面設定儲存為 PDF - Aspose.Note
linktitle: 使用 OneNote 中的頁面設定儲存為 PDF - Aspose.Note
second_title: Aspose.Note Java API
description: 了解如何使用 Aspose.Note 函式庫將 OneNote 文件儲存為 Java 中的 PDF。包含不同頁面設定的程式碼範例的逐步指南。
weight: 19
url: /zh-hant/java/onenote-document-saving/save-to-pdf-using-page-settings/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 使用 OneNote 中的頁面設定儲存為 PDF - Aspose.Note

## 介紹

在本教學中，我們將學習如何使用 Aspose.Note for Java 使用不同的頁面設定將 OneNote 文件儲存為 PDF 格式。我們將介紹兩種方法：使用 Letter 頁面設定儲存和使用無高度限制的 A4 頁面設定儲存。

## 先決條件

在我們開始之前，請確保您具備以下先決條件：

1. 您的系統上安裝了 Java 開發工具包 (JDK)。
2. Aspose.Note for Java 程式庫已下載並包含在您的 Java 專案中。
3. 對 Java 程式語言有基本的了解。

## 導入包

確保您已匯入在專案中使用 Aspose.Note for Java 所需的套件。這是導入聲明：

```java
import com.aspose.note.*;
import java.io.IOException;
import java.nio.file.Paths;
```

## 使用 Letter 頁面設定儲存為 PDF

### 第 1 步：載入文檔

首先，將 OneNote 文件載入到 Aspose.Note 中：

```java
Document oneFile = new Document("path/to/your/OneNote.one");
```

### 第 2 步：定義目標路徑

指定 PDF 檔案的目標路徑：

```java
String dst = "path/to/your/SaveToPdfUsingLetterPageSettings.pdf";
```

### 第 3 步：儲存文檔

使用 Letter 頁面設定儲存文件：

```java
PdfSaveOptions options = new PdfSaveOptions();
options.setPageSettings(PageSettings.getLetter());
oneFile.save(dst, options);
```

## 使用 A4 頁面設定儲存為 PDF，無高度限制

### 第 1 步：載入文檔

同樣，將 OneNote 文件載入到 Aspose.Note 中：

```java
Document oneFile = new Document("path/to/your/OneNote.one");
```

### 第 2 步：定義目標路徑

指定 PDF 檔案的目標路徑：

```java
String dst = "path/to/your/SaveToPdfUsingA4PageSettingsWithoutHeightLimit.pdf";
```

### 第 3 步：儲存文檔

以A4頁面設定儲存文檔，無高度限制：

```java
PdfSaveOptions options = new PdfSaveOptions();
options.setPageSettings(PageSettings.getA4NoHeightLimit());
oneFile.save(dst, options);
```

執行這些步驟後，您將使用不同的頁面設定成功將 OneNote 文件儲存為 PDF。

## 結論

在本教學中，我們探索如何使用 Aspose.Note for Java 函式庫將 OneNote 文件儲存為 PDF 格式。透過遵循逐步指南，您可以輕鬆地將此功能整合到您的 Java 應用程式中。

## 常見問題解答

### Q1：我可以進一步自訂頁面設定嗎？

A1：是的，您可以使用 Aspose.Note for Java 根據您的要求自訂頁面設定。

### Q2：Aspose.Note 是否支援 PDF 以外的其他輸出格式？

A2：是的，Aspose.Note 支援各種輸出格式，包括圖片和 HTML。

### Q3：Aspose.Note 是否相容於不同版本的 OneNote 檔案？

A3：是的，Aspose.Note 支援不同版本的 OneNote 文件，包括 .one 和 .onetoc2。

### Q4：我可以一次將多個 OneNote 檔案轉換為 PDF 嗎？

A4：是的，您可以使用 Aspose.Note for Java 批次處理多個 OneNote 檔案。

### Q5：有沒有可供測試的試用版？

A5：是的，您可以從網站上獲得 Aspose.Note for Java 的免費試用版。
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
