---
date: 2025-12-20
description: 學習如何使用 Java 與 Aspose.Note 函式庫將 OneNote 儲存為 PDF 並在 OneNote 中加入超連結。輕鬆從
  OneNote 產生 PDF。
linktitle: Save OneNote as PDF and Add Hyperlink in OneNote with Java
second_title: Aspose.Note Java API
title: 使用 Java 將 OneNote 儲存為 PDF 並在 OneNote 中加入超連結
url: /zh-hant/java/onenote-hyperlinks-images/add-hyperlink/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 將 OneNote 儲存為 PDF 並在 OneNote 中加入超連結（使用 Java）

## 簡介

在 OneNote 文件中加入超連結，同時將其儲存為 PDF，能顯著提升筆記的互動性並讓分享更方便。在本教學中，您將學習 **如何將 OneNote 儲存為 PDF**，以及使用 Java 與 Aspose.Note 函式庫嵌入可點擊的連結。讓我們一起逐步完成吧！

## 快速解答
- **我可以使用 Java 將 OneNote 儲存為 PDF 嗎？** 是的，Aspose.Note for Java 提供單一的 `save` 呼叫即可產生 PDF。
- **如何嵌入超連結？** 在 `RichText` 片段上使用 `TextStyle.setHyperlinkAddress`。
- **前置條件是什麼？** JDK 8 以上以及 Aspose.Note for Java 函式庫。
- **支援哪些輸出格式？** PDF、DOCX、XPS 等。
- **正式環境是否需要授權？** 是的，非評估使用需購買商業授權。

## 什麼是「將 OneNote 儲存為 PDF」？

將 OneNote 筆記本儲存為 PDF 會產生一個可攜帶、唯讀的筆記版本，無需 OneNote 應用程式即可在任何裝置上開啟。這對於歸檔、列印或與沒有 OneNote 的使用者分享特別有用。

## 為什麼要使用 Aspose.Note Java 從 OneNote 產生 PDF？

- **完整保真度：** 保留格式、影像與超連結。
- **程式化控制：** 在後端服務中自動化批次轉換。
- **跨平台：** 可在 Windows、Linux 與 macOS 上執行。
- **豐富 API：** 可輕鬆在儲存前新增或修改內容。

## 前置條件

在開始之前，請確保您的系統已安裝並設定以下前置條件：

### Java Development Kit (JDK)

請確認您的系統已安裝 Java Development Kit (JDK)。您可以從 [Oracle 網站](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) 下載並安裝 JDK。

### Aspose.Note for Java 函式庫

下載並安裝 Aspose.Note for Java 函式庫。您可於 [此處](https://reference.aspose.com/note/java/) 找到文件與下載連結。

## 匯入套件

首先，匯入使用 Aspose.Note for Java 所需的相關套件。

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.TextStyle;
import com.aspose.note.ParagraphStyle;
import com.aspose.note.Title;
```

現在，讓我們將提供的範例分解為多個步驟：

## 步驟 1：設定文件結構

首先，建立一個新文件與一個頁面，以放置內容。

```java
String dataDir = "Your Document Directory";
Document doc = new Document();
Page page = new Page();
Title title = new Title();
```

## 步驟 2：定義預設文字樣式

定義一個預設段落樣式，將套用於大多數文字元素。

```java
ParagraphStyle defaultTextStyle = new ParagraphStyle()
                                            .setFontName("Arial")
                                            .setFontSize(10)
                                            .setFontColor(java.awt.Color.GRAY);
```

## 步驟 3：設定標題文字

為頁面建立標題並套用預設樣式。

```java
RichText titleText = new RichText().append("Title");
titleText.setParagraphStyle(defaultTextStyle);
title.setTitleText(titleText);
page.setTitle(title);
```

## 步驟 4：建立大綱與大綱元素

大綱充當段落及其他元素的容器。

```java
Outline outline = new Outline();
OutlineElement outlineElem = new OutlineElement();
```

## 步驟 5：定義超連結文字樣式

此處定義一個紅色樣式，用於可點擊的部分。

```java
TextStyle textStyleRed = new TextStyle()
                                    .setFontName("Arial")
                                    .setFontSize(10)
                                    .setFontColor(java.awt.Color.red);
```

## 步驟 6：加入帶有超連結的文字

現在我們建立一個 `RichText` 物件，混合普通文字與超連結。  
`setHyperlinkAddress` 方法告訴 Aspose.Note 此片段應可點擊。

```java
RichText text = new RichText()
                            .append("This is ", textStyleRed)
                            .append("hyperlink", new TextStyle().setHyperlinkAddress("www.google.com"))
                            .append(". This text is not a hyperlink.", TextStyle.getDefault());
text.setParagraphStyle(defaultTextStyle);
outlineElem.appendChildLast(text);
```

## 步驟 7：將大綱加入頁面，並將頁面加入文件

將大綱元素附加至大綱，將大綱附加至頁面，最後將頁面附加至文件。

```java
outline.appendChildLast(outlineElem);
page.appendChildLast(outline);
doc.appendChildLast(page);
```

## 步驟 8：將文件儲存為 PDF

最後一步是將 OneNote 文件儲存為 PDF 檔案。此處即會使用主要關鍵字 **save onenote as pdf**。

```java
doc.save(dataDir + "AddHyperlink_out.pdf");
System.out.printf("File saved: %s\n", dataDir + "AddHyperlink_out.pdf");
```

## 結論

恭喜！您已成功 **將 OneNote 儲存為 PDF**，並使用 Java 與 Aspose.Note 函式庫在文件中加入超連結。此功能讓您能直接從 OneNote 內容產生可互動、可分享的 PDF。

## 常見問答

### Q1：Aspose.Note 是否相容所有 Java 版本？

A1：是的，Aspose.Note for Java 支援所有主要的 Java 版本，包括 JDK 8 以上。

### Q2：我可以在單一文件中使用 Aspose.Note 加入多個超連結嗎？

A2：當然可以！您可在 OneNote 文件中使用 Aspose.Note for Java 加入任意數量的超連結。

### Q3：Aspose.Note 是否提供其他程式語言的支援？

A3：是的，Aspose.Note 提供多種程式語言的函式庫，包括 .NET、Python 與 Android。

### Q4：Aspose.Note 容易整合到現有的 Java 專案嗎？

A4：是的，將 Aspose.Note 整合到 Java 專案相當簡單，且文件完善，讓您輕鬆上手。

### Q5：我可以在哪裡找到更多使用 Aspose.Note 的協助與資源？

A5：您可於 [Aspose.Note 論壇](https://forum.aspose.com/c/note/28) 找到豐富的文件、教學與社群支援。

## 常見問題

**問：如何自訂超連結的外觀？**  
答：在呼叫 `setHyperlinkAddress` 前，使用 `TextStyle` 的屬性，如 `setFontColor`、`setUnderline` 或 `setFontName`。

**問：我可以將文件儲存為 PDF 以外的格式嗎？**  
答：可以，Aspose.Note 支援 DOCX、XPS、HTML 等多種匯出格式。

**問：如果需要在現有的 OneNote 檔案中加入超連結該怎麼做？**  
答：使用 `new Document("input.one")` 載入現有檔案，依照示範修改內容，然後以所需格式呼叫 `save`。

**問：PDF 產生後，是否有辦法以程式方式開啟超連結？**  
答：PDF 閱讀器會自動處理可點擊的連結，無需額外程式碼。

**問：開發使用需要授權嗎？**  
答：暫時的評估授權足以用於開發與測試，但正式上線需購買完整授權。

---

**最後更新：** 2025-12-20  
**測試環境：** Aspose.Note for Java 23.12  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}