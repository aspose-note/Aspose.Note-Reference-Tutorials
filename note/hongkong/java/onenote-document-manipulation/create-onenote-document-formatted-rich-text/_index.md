---
date: 2026-02-18
description: 學習如何使用 Aspose.Note 在 Java 中建立 OneNote 文件、格式化富文本，並儲存為 PDF。一步一步的指南，實現無縫自動化。
linktitle: Create OneNote document and save as PDF in Java
second_title: Aspose.Note Java API
title: 在 Java 中建立 OneNote 文件並另存為 PDF
url: /zh-hant/java/onenote-document-manipulation/create-onenote-document-formatted-rich-text/
weight: 11
---

 all shortcodes unchanged.

Now produce final output.{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 在 Java 中建立 OneNote 文件並儲存為 PDF

## 介紹

如果您需要 **建立 OneNote 文件** 並 **將 OneNote 儲存為 PDF** 同時保留豐富文字格式，您來對地方了。在本教學中，我們將逐步說明如何建立 OneNote 文件、套用自訂樣式，並使用 Aspose.Note for Java 直接匯出為 PDF。完成後，您將擁有可在任何 Java 專案中使用的可重複使用程式碼片段，以自動化精緻的 OneNote 轉 PDF 轉換。

## 快速解答
- **此教學教什麼？** 如何建立帶有樣式文字的 OneNote 文件並將其儲存為 PDF。  
- **需要哪個函式庫？** Aspose.Note for Java（可從官方網站下載）。  
- **需要授權嗎？** 測試可使用臨時授權；正式環境需購買完整授權。  
- **可使用哪種 IDE？** 任何 Java IDE，例如 IntelliJ IDEA、Eclipse 或 NetBeans。  
- **可以更改輸出格式嗎？** 可以，Aspose.Note 支援 PDF、HTML、PNG 等多種格式。

## 什麼是「save onenote pdf」？

將 OneNote 儲存為 PDF 意味著將 OneNote 頁面的結構——包括文字、影像與格式——轉換成靜態的 PDF 檔案，讓任何平台都能在不需要 OneNote 的情況下檢視。

## 為什麼在 Java 中格式化豐富文字？

在 Java 中直接 **格式化豐富文字** 可讓您產生外觀專業、符合品牌指引的文件，免除手動編輯的步驟。

## 前置條件

1. **Java Development Kit (JDK)** – 任意近期版本（8 或以上）。  
2. **Aspose.Note for Java JAR** – 從[下載連結](https://releases.aspose.com/note/java/)下載。  
3. **IDE** – IntelliJ IDEA、Eclipse，或您偏好的任何編輯器。  

## 匯入套件

在開始之前，請將必要的類別匯入您的 Java 檔案中：

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

## 如何建立 OneNote 文件 – 步驟說明

### 步驟 1：設定文件與頁面

初始化將容納所有內容的 `Document` 與 `Page` 物件：

```java
String dataDir = "Your Document Directory";
Document doc = new Document();
Page page = new Page();
```

### 步驟 2：建立帶格式的標題

加入標題元素，並使用 **set paragraph style** 來控制其外觀：

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

### 步驟 3：建立帶格式的豐富文字

在此使用多個 `TextStyle` 物件建立豐富文字內容，以示範 **rich text formatting**：

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

### 步驟 4：將元素加入頁面與文件

將標題與豐富文字組合至頁面層級：

```java
outlineElem.appendChildLast(text);
outline.appendChildLast(outlineElem);
page.setTitle(title);
page.appendChildLast(outline);
doc.appendChildLast(page);
```

### 步驟 5：儲存文件 – 匯出 OneNote PDF

最後，將 OneNote 文件匯出為 PDF 檔案：

```java
doc.save(dataDir + "CreateOneNoteDocument_out.pdf", SaveFormat.Pdf);
```

## 常見問題與解決方案

| 問題 | 解決方案 |
|-------|----------|
| **找不到檔案** | 確認 `dataDir` 指向已存在的資料夾且您具有寫入權限。 |
| **缺少字型** | 確保您引用的字型（例如 *Calibri*）已安裝於主機上。 |
| **授權未套用** | 在建立 `Document` 前先載入 Aspose 授權，以避免評估版浮水印。 |

## 常見問答

**問：我可以進一步自訂字型樣式嗎？**  
答：可以，您可以透過 `TextStyle` 與 `ParagraphStyle` 類別調整底線、刪除線、文字對齊等其他屬性。

**問：Aspose.Note for Java 是否相容所有 Java IDE？**  
答：絕對相容。只要 IDE 支援標準的 Java 開發，即可將 Aspose.Note JAR 加入專案的 classpath。

**問：我可以將此功能整合至 Web 應用程式嗎？**  
答：可以，同樣的程式碼可在基於 Servlet 或 Spring Boot 的應用程式中使用，實現在伺服器端動態產生 OneNote 轉 PDF。

**問：使用 Aspose.Note for Java 有授權需求嗎？**  
答：正式環境需購買商業授權。評估與測試可使用臨時授權。

**問：Aspose.Note for Java 是否支援除 OneNote 之外的其他文件格式？**  
答：它支援 PDF、HTML、PNG、JPEG 等多種匯出格式，讓您能彈性地將 OneNote 頁面轉換為所需格式。

## 結論

在本指南中，我們示範了如何 **建立 OneNote 文件**、套用 **豐富文字格式**，以及使用 Aspose.Note for Java **將 OneNote 儲存為 PDF**。依照步驟說明，您即可在任何基於 Java 的解決方案中自動化產生精緻的 OneNote 文件並轉換為 PDF。

---

**最後更新：** 2026-02-18  
**測試環境：** Aspose.Note for Java 24.11（撰寫時的最新版本）  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}