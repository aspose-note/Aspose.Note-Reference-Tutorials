---
title: 在 OneNote 中使用保留實體物件演算法 - Aspose.Note
linktitle: 在 OneNote 中使用保留實體物件演算法 - Aspose.Note
second_title: Aspose.Note Java API
description: 了解如何在使用 Java 中的保留實體物件演算法轉換為 PDF 時保留 Aspose.Note 文件中的實體物件。
weight: 25
url: /zh-hant/java/onenote-document-saving/use-keep-solid-objects-algorithm/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 在 OneNote 中使用保留實體物件演算法 - Aspose.Note

## 介紹

在本教學中，我們將探討如何在 Aspose.Note for Java 中使用保留實體物件演算法。此演算法對於在將文件轉換為 PDF 格式時保持文件中實體物件的完整性非常重要。我們將逐步分解該過程，確保每個階段的清晰度和理解性。

## 先決條件

在我們開始之前，請確保您具備以下條件：

1. 您的系統上安裝了 Java 開發工具包 (JDK)。
2.  Java 函式庫的 Aspose.Note。您可以從以下位置下載：[這裡](https://releases.aspose.com/note/java/).

## 導入包

首先，讓我們導入必要的套件：

```java
import java.io.IOException;
import com.aspose.note.AlwaysSplitObjectsAlgorithm;
import com.aspose.note.Document;
import com.aspose.note.KeepPartAndCloneSolidObjectToNextPageAlgorithm;
import com.aspose.note.KeepSolidObjectsAlgorithm;
import com.aspose.note.PdfSaveOptions;
```

## 第 1 步：載入文檔

使用以下程式碼片段將文件載入到 Aspose.Note 中：

```java
String dataDir = "Your Document Directory";
Document doc = new Document(dataDir + "Aspose.one");
```

## 步驟 2：設定 PDF 儲存選項

定義 PdfSaveOptions 並將 PageSplittingAlgorithm 設定為 KeepSolidObjectsAlgorithm：

```java
PdfSaveOptions pdfSaveOptions = new PdfSaveOptions();
pdfSaveOptions.setPageSplittingAlgorithm(new KeepSolidObjectsAlgorithm());
```

## 步驟 3：調整高度限制（可選）

如有必要，您可以調整克隆零件的高度限制：

```java
float heightLimitOfClonedPart = 500;
pdfSaveOptions.setPageSplittingAlgorithm(new KeepSolidObjectsAlgorithm(heightLimitOfClonedPart));
```

## 步驟 4：儲存文檔

最後，使用指定的 PDF 儲存選項儲存文件：

```java
String outputDir = "Your Output Directory";
String outputFile = outputDir + "UsingKeepSolidObjectsAlgorithm_out.pdf";
doc.save(outputFile);
```

## 結論

在本教程中，我們學習如何在 Aspose.Note for Java 中使用保留實體物件演算法。此演算法可確保在將文件轉換為 PDF 格式時保留文件中的實體對象，從而保持文件的完整性。

## 常見問題解答

### Q1：克隆零件的高度限制可以調整嗎？

 A1: 是的，您可以根據您的要求使用調整克隆零件的高度限制`heightLimitOfClonedPart`範圍。

### Q2：在哪裡可以找到更多文件？

 A2：您可以在Aspose.Note for Java上找到詳細文檔[這裡](https://reference.aspose.com/note/java/).

### Q3：有免費試用嗎？

 A3：是的，您可以免費試用 Aspose.Note for Java[這裡](https://releases.aspose.com/).

### Q4：如果我遇到任何問題，我該如何獲得支援？

 A4：您可以從Aspose社群獲得支持[這裡](https://forum.aspose.com/c/note/28).

### Q5：哪裡可以購買許可證？

 A5：您可以購買 Aspose.Note for Java 的許可證[這裡](https://purchase.aspose.com/buy).

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
