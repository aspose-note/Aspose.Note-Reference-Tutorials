---
title: 使用 Java 建立具有格式化富文本的 OneNote 文檔
linktitle: 使用 Java 建立具有格式化富文本的 OneNote 文檔
second_title: Aspose.Note Java API
description: 了解如何使用 Aspose.Note for Java 以程式設計方式在 Java 中建立格式豐富的 OneNote 文件。請遵循我們的無縫文件自動化逐步指南。
weight: 11
url: /zh-hant/java/onenote-document-manipulation/create-onenote-document-formatted-rich-text/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 使用 Java 建立具有格式化富文本的 OneNote 文檔

## 介紹

對於希望在 Java 應用程式中自動執行文件生成任務的開發人員來說，以程式設計方式建立格式豐富的 OneNote 文件可能是一個強大的工具。 Aspose.Note for Java 提供了一套全面的特性和功能來無縫地實現這一點。在本教學中，我們將引導您完成使用 Aspose.Note for Java 建立具有格式化富文本的 OneNote 文件的過程。

## 先決條件

在我們開始之前，請確保您已設定以下先決條件：

1. Java 開發工具包 (JDK)：確保您的系統上安裝了 JDK。
2.  Aspose.Note for Java JAR：下載 Aspose.Note for Java JAR 檔案並將其包含在您的專案中。您可以從[下載連結](https://releases.aspose.com/note/java/).
3. 整合開發環境 (IDE)：使用您喜歡的 IDE，例如 IntelliJ IDEA 或 Eclipse。

## 導入包

首先，您需要將必要的套件匯入到您的 Java 專案中。將以下導入語句加入 Java 檔案的開頭：

```java
import java.awt.Color;
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.SaveFormat;
import com.aspose.note.TextStyle;
import com.aspose.note.ParagraphStyle;
import com.aspose.note.Title;
```

## 第 1 步：設定文件和頁面

讓我們先初始化 Document 和 Page 物件：

```java
String dataDir = "Your Document Directory";
Document doc = new Document();
Page page = new Page();
```

## 第 2 步：建立帶有格式的標題

現在，讓我們建立一個帶有格式化文字的標題：

```java
Title title = new Title();
ParagraphStyle defaultTextStyle = new ParagraphStyle()
                                        .setFontColor(Color.black)
                                        .setFontName("Arial")
                                        .setFontSize(10);

RichText titleText = new RichText().append("Title!");
titleText.setParagraphStyle(defaultTextStyle);
title.setTitleText(titleText);
```

## 第 3 步：建立帶有格式的富文本

接下來，讓我們建立具有各種格式樣式的富文本：

```java
Outline outline = new Outline();
OutlineElement outlineElem = new OutlineElement();

TextStyle textStyleForHelloWord = new TextStyle()
                                        .setFontColor(Color.red)
                                        .setFontName("Arial")
                                        .setFontSize(10);

TextStyle textStyleForOneNoteWord = new TextStyle()
                                        .setFontColor(Color.green)
                                        .setFontName("Calibri")
                                        .setFontSize(10)
                                        .setItalic(true);

TextStyle textStyleForTextWord = new TextStyle()
                                        .setFontColor(Color.blue)
                                        .setFontName("Arial")
                                        .setFontSize(15)
                                        .setBold(true)
                                        .setItalic(true);

RichText text = new RichText()
        .append("Hello", textStyleForHelloWord)
        .append(" OneNote", textStyleForOneNoteWord)
        .append(" text", textStyleForTextWord)
        .append("!", TextStyle.getDefault());
text.setParagraphStyle(defaultTextStyle);
```

## 步驟 4：在頁面和文件中新增元素

現在，讓我們將標題和富文本添加到頁面和大綱元素中：

```java
outlineElem.appendChildLast(text);
outline.appendChildLast(outlineElem);
page.setTitle(title);
page.appendChildLast(outline);
doc.appendChildLast(page);
```

## 第5步：儲存文檔

最後，儲存已建立的OneNote文件：

```java
doc.save(dataDir + "CreateOneNoteDocument_out.pdf", SaveFormat.Pdf);
```

## 結論

在本教學中，我們學習如何使用 Aspose.Note for Java 在 Java 中建立具有格式化富文本的 OneNote 文件。透過遵循這些逐步說明，您可以輕鬆地以程式設計方式產生自訂 OneNote 文檔，從而增強文檔自動化功能。

## 常見問題解答

### Q1：我可以進一步自訂字體樣式嗎？

A1: 是的，您可以調整各種屬性，例如字體顏色、大小、樣式等，以滿足您的要求。

### Q2：Aspose.Note for Java 是否與所有 Java IDE 相容？

A2：是的，您可以將 Aspose.Note for Java 與任何支援 Java 開發的 Java IDE 一起使用。

### Q3：我可以將此功能整合到 Web 應用程式中嗎？

A3：當然，Aspose.Note for Java 可以無縫整合到 Web 應用程式中以進行動態文件生成。

### Q4：使用 Aspose.Note for Java 有任何許可要求嗎？

A4：是的，您需要獲得許可證才能在商業專案中使用Aspose.Note for Java。但是，您也可以使用臨時許可證進行測試。

### Q5：Aspose.Note for Java 是否支援 OneNote 以外的其他文件格式？

A5：是的，Aspose.Note for Java 支援多種文件格式，包括 PDF、HTML 和影像格式。

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
