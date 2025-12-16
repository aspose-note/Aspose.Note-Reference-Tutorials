---
date: 2025-12-09
description: 學習如何使用 Aspose.Note for Java 在 Java 中將 OneNote 另存為帶有格式化富文本的 PDF。遵循我們的逐步指南，實現無縫的文件自動化。
linktitle: Save OneNote as PDF with Formatted Rich Text in Java
second_title: Aspose.Note Java API
title: 使用 Java 將 OneNote 另存為 PDF 並保留格式化的富文本
url: /zh-hant/java/onenote-document-manipulation/create-onenote-document-formatted-rich-text/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 在 Java 中將 OneNote 另存為 PDF 並保留格式化的豐富文字

## 簡介

如果您需要 **將 OneNote 另存為 PDF** 並保留豐富文字的格式化，您來對地方了。在本教學中，我們將示範如何建立 OneNote、套用自訂樣式，並使用 Aspose.Note for Java 直接匯出為 PDF。完成後，您將擁有一段可重複使用的程式碼片段，能夠在任何 Java 專案中自動化產出精緻的 OneNote 轉 PDF。

## 快速答案
- **本教學教什麼？** 如何建立帶樣式文字的 OneNote 文件並將其儲存為 PDF。  
- **需要哪個函式庫？** Aspose.Note for Java（可從官方網站下載）。  
- **需要授權嗎？** 測試可使用臨時授權；正式上線必須購買正式授權。  
- **可以使用哪種 IDE？** 任何 Java IDE——IntelliJ IDEA、Eclipse 或 NetBeans 都可。  
- **可以更換輸出格式嗎？** 可以，Aspose.Note 支援 PDF、HTML、PNG 等多種格式。

## 什麼是「將 OneNote 另存為 PDF」？
將 OneNote 另存為 PDF 意指將 OneNote 頁面的結構（包括文字、圖片與格式）轉換為靜態的 PDF 檔案，讓任何平台都能在不安裝 OneNote 的情況下檢視。

## 為什麼在 Java 中格式化豐富文字？
在 Java 中直接套用豐富文字格式（字型、顏色、樣式）可讓您產生符合品牌指引、外觀專業的文件，免除手動編輯的麻煩。

## 先決條件

1. **Java Development Kit (JDK)** – 任意近期版本（8 或以上）。  
2. **Aspose.Note for Java JAR** – 從 [download link](https://releases.aspose.com/note/java/) 下載。  
3. **IDE** – IntelliJ IDEA、Eclipse，或您慣用的任何編輯器。  

## 匯入套件

首先，您需要將必要的套件匯入至 Java 專案。將以下 import 陳述式加入 Java 檔案的開頭：

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

## 步驟 1：設定文件與頁面

讓我們先初始化 `Document` 與 `Page` 物件：

```java
String dataDir = "Your Document Directory";
Document doc = new Document();
Page page = new Page();
```

## 步驟 2：建立帶格式的標題

現在，建立一個帶格式的標題：

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

## 步驟 3：建立帶格式的豐富文字

接著，建立具有各種格式樣式的豐富文字：

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

## 步驟 4：將元素加入頁面與文件

現在，將標題與豐富文字加入頁面，並建立大綱元素：

```java
outlineElem.appendChildLast(text);
outline.appendChildLast(outlineElem);
page.setTitle(title);
page.appendChildLast(outline);
doc.appendChildLast(page);
```

## 步驟 5：儲存文件

最後，將建立好的 OneNote 文件儲存為 PDF：

```java
doc.save(dataDir + "CreateOneNoteDocument_out.pdf", SaveFormat.Pdf);
```

## 常見問題與解決方案

| 問題 | 解決方案 |
|-------|----------|
| **找不到檔案** | 確認 `dataDir` 指向已存在的資料夾，且您具有寫入權限。 |
| **缺少字型** | 確認您所引用的字型（例如 *Calibri*）已安裝在主機上。 |
| **授權未套用** | 在建立 `Document` 前先載入 Aspose 授權，以避免評估版浮水印。 |

## 常見問答

**Q: 我可以進一步自訂字型樣式嗎？**  
A: 可以，您可以透過 `TextStyle` 與 `ParagraphStyle` 類別調整底線、刪除線、文字對齊等屬性。

**Q: Aspose.Note for Java 是否相容所有 Java IDE？**  
A: 完全相容。只要 IDE 支援標準的 Java 開發，即可將 Aspose.Note JAR 加入專案的 classpath。

**Q: 我可以將此功能整合到 Web 應用程式嗎？**  
A: 可以，同樣的程式碼可在 Servlet 或 Spring Boot 應用程式中使用，實現在伺服器端動態產生 OneNote 轉 PDF。

**Q: 使用 Aspose.Note for Java 有哪些授權需求？**  
A: 正式環境必須購買商業授權。測試與評估可使用臨時授權。

**Q: Aspose.Note for Java 支援除 OneNote 之外的其他文件格式嗎？**  
A: 支援 PDF、HTML、PNG、JPEG 等多種匯出格式，讓您能將 OneNote 頁面轉換成所需的任意格式。

## 結論

本指南示範了如何使用 Aspose.Note for Java **將 OneNote 另存為 PDF** 並套用豐富文字格式。依循逐步說明，您即可在任何基於 Java 的解決方案中自動化產生精緻的 OneNote 文件並轉換為 PDF。

---

**最後更新：** 2025-12-09  
**測試環境：** Aspose.Note for Java 24.11（撰寫時的最新版本）  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}