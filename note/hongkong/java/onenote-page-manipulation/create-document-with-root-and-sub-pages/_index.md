---
description: 學習如何使用 Aspose.Note for Java 將 OneNote 另存為 PDF 並在 OneNote 中新增子頁面。跟隨此一步一步的指南，有效組織您的筆記。
linktitle: How to Save OneNote PDF and Add Sub Pages
second_title: Aspose.Note Java API
title: 如何儲存 OneNote PDF 並新增子頁面
url: /zh-hant/java/onenote-page-manipulation/create-document-with-root-and-sub-pages/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何儲存 OneNote PDF 並新增子頁面

## 簡介

在本教學中，您將了解 **如何儲存 OneNote PDF**，同時使用 Aspose.Note for Java 建立包含根頁面與子頁面的文件。將 OneNote 筆記本以清晰的層級結構組織，可讓導航變得輕鬆，而匯出為 PDF 則確保您能以通用可讀的格式分享筆記。我們也會示範 **新增子頁面 onenote** 風格，讓您輕鬆構建多層結構。

## 快速回答
- **主要關鍵字的含義是什麼？** 它指的是使用 Aspose.Note 將 OneNote 筆記本匯出為 PDF。  
- **使用哪個 API？** Aspose.Note for Java。  
- **我可以建立階層頁面嗎？** 可以 – 設定頁面層級即可建立根頁面與子頁面。  
- **需要授權嗎？** 提供免費試用版；正式環境需購買商業授權。  
- **支援哪些輸出格式？** BMP、PDF、PNG 等。

## 什麼是「如何儲存 OneNote PDF」？
將 OneNote 儲存為 PDF 會將筆記本的頁面轉換為固定版面的文件，保留格式、圖像與層級結構。這非常適合分享、存檔或列印筆記。

## 為什麼要新增子頁面 onenote？
新增子頁面可讓您將相關內容歸於父頁面之下，類似資料夾的結構。它提升筆記的組織性、加快搜尋速度，並在匯出為 PDF 時增強閱讀體驗。

## 先決條件

在開始之前，請確保您具備以下條件：

1. **Java Development Kit (JDK)**：確保系統已安裝 JDK。  
2. **Aspose.Note for Java**：從[網站](https://purchase.aspose.com/buy)下載並安裝 Aspose.Note for Java。  
3. **整合開發環境 (IDE)**：選擇如 IntelliJ IDEA、Eclipse 或 NetBeans 等 Java IDE。

## 匯入套件

在您的 Java 專案中匯入必要的套件：

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.SaveFormat;
import com.aspose.note.ParagraphStyle;
```

## 步驟 1：設定文件目錄

定義您想要儲存 OneNote 文件的目錄：

```java
String dataDir = "Your Document Directory";
```

## 步驟 2：建立 Document 物件

實例化一個 `Document` 物件：

```java
Document doc = new Document();
```

## 步驟 3：建立頁面

初始化頁面物件並設定其層級。設定層級可決定頁面是根頁面還是子頁面：

```java
Page page1 = new Page();
page1.setLevel((byte) 1);

Page page2 = new Page();
page2.setLevel((byte) 2);

Page page3 = new Page();
page3.setLevel((byte) 1);
```

## 步驟 4：向頁面新增節點

### 新增節點至第一頁

```java
Outline outline = new Outline();
OutlineElement outlineElem = new OutlineElement();
ParagraphStyle textStyle = new ParagraphStyle()
                                    .setFontColor(Color.black)
                                    .setFontName("David Transparent")
                                    .setFontSize(10);

RichText text = new RichText().append("First page.");
text.setParagraphStyle(textStyle);

outlineElem.appendChildLast(text);
outline.appendChildLast(outlineElem);
page1.appendChildLast(outline);
```

### 新增節點至第二頁

```java
Outline outline2 = new Outline();
OutlineElement outlineElem2 = new OutlineElement();
ParagraphStyle textStyle2 = new ParagraphStyle()
                                    .setFontColor(Color.black)
                                    .setFontName("David Transparent")
                                    .setFontSize(10);

RichText text2 = new RichText().append("Second page.");
text2.setParagraphStyle(textStyle2);

outlineElem2.appendChildLast(text2);
outline2.appendChildLast(outlineElem2);
page2.appendChildLast(outline2);
```

### 新增節點至第三頁

```java
Outline outline3 = new Outline();
OutlineElement outlineElem3 = new OutlineElement();
ParagraphStyle textStyle3 = new ParagraphStyle()
                                    .setFontColor(Color.black)
                                    .setFontName("Broadway")
                                    .setFontSize(10);

RichText text3 = new RichText().append("Third page.");
text3.setParagraphStyle(textStyle3);

outlineElem3.appendChildLast(text3);
outline3.appendChildLast(outlineElem3);
page3.appendChildLast(outline3);
```

## 步驟 5：將頁面加入文件

```java
doc.appendChildLast(page1);
doc.appendChildLast(page2);
doc.appendChildLast(page3);
```

## 步驟 6：儲存文件

將 OneNote 文件儲存為 PDF（此範例為 BMP）。變更 `SaveFormat` 即可匯出為 PDF，滿足「如何儲存 OneNote PDF」的需求：

```java
try {
    doc.save(dataDir + "GenerateRootAndSubLevelPagesInOneNote_out.bmp", SaveFormat.Bmp);
} catch (IOException e) {
    // Handle exception
}
```

> **專業提示：** 若要直接匯出為 PDF，請將 `SaveFormat.Bmp` 改為 `SaveFormat.Pdf`。

恭喜！您已成功建立包含根頁面與子頁面的 OneNote 文件，並學會使用 Aspose.Note for Java **如何儲存 OneNote PDF**。

## 為什麼這很重要

- **階層組織：** 根頁面與子頁面可在 OneNote 中模擬資料夾結構。  
- **無縫 PDF 匯出：** 組織完成後，匯出為 PDF 可保留層級，使最終文件易於閱讀與分享。  
- **自動化：** 此程式碼可整合至更大型的 Java 應用程式，實現批次建立結構化筆記本。

## 常見陷阱與避免方法

| 問題 | 原因 | 解決方案 |
|-------|-------|----------|
| 頁面顯示在相同層級 | `setLevel` 值設定錯誤 | 根頁面使用 `setLevel((byte) 1)`，子頁面使用 `setLevel((byte) 2)`（或更高）。 |
| PDF 輸出為空白 | 缺少 `SaveFormat.Pdf` 或檔案路徑不正確 | 確認目錄存在，並使用 `SaveFormat.Pdf`。 |
| 字型未套用 | 字型名稱錯誤或系統未安裝該字型 | 確保字型（例如 “David Transparent”）已安裝於執行程式的機器上。 |

## 常見問答

**Q: 我可以使用 Aspose.Note for Java 建立多層子頁面嗎？**  
A: 可以，透過設定較高的層級數字即可建立更深的層級（例如 `setLevel((byte) 3)` 代表第三層子頁面）。

**Q: Aspose.Note for Java 是否相容於不同的 Java IDE？**  
A: 完全相容。它支援 IntelliJ IDEA、Eclipse、NetBeans 以及任何支援 Java 開發的 IDE。

**Q: 我可以自訂 OneNote 文件中文本的格式嗎？**  
A: 可以。使用 `ParagraphStyle` 為每個 `RichText` 元素設定字型名稱、大小、顏色等屬性。

**Q: Aspose.Note for Java 是否支援除 BMP 之外的其他格式儲存？**  
A: 支援。可匯出為 PDF、PNG、JPEG、DOCX 等格式，只需相應調整 `SaveFormat` 列舉值。

**Q: 是否有 Aspose.Note for Java 的試用版？**  
A: 有，您可從 Aspose 官方網站下載免費試用版。

## 結論

將 OneNote 筆記本以清晰的階層結構組織並匯出為 PDF，可讓您的筆記更易於存取與分享。透過上述步驟，您現在已掌握 **如何儲存 OneNote PDF** 以及 **新增子頁面 onenote** 風格的程式化方法，並可在 Aspose.Note for Java 中實踐。

---

**最後更新：** 2026-01-07  
**測試環境：** Aspose.Note for Java 24.11（最新）  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}