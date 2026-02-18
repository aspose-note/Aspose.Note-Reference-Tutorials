---
date: 2026-02-18
description: 學習如何在使用 Aspose.Note 的 Java 中建立 OneNote 文件時設定段落樣式與新增大綱元素。將 OneNote 匯出為
  PDF、將 OneNote 儲存為 PDF，並輕鬆產生 OneNote 檔案。
linktitle: Set Paragraph Style while Creating OneNote Document in Java
second_title: Aspose.Note Java API
title: 匯出 OneNote 為 PDF – 在 Java 中建立 OneNote 文件時設定段落樣式
url: /zh-hant/java/onenote-document-manipulation/create-onenote-document-simple-rich-text/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 在 Java 中建立 OneNote 文件時設定段落樣式

## Introduction

在當今快速變化的開發環境中，能夠以程式方式 **export OneNote to PDF** 是製作精緻、可分享文件的關鍵。本教學將帶領您建立 OneNote 檔案、套用自訂段落樣式，最後使用 Aspose.Note for Java **export OneNote to PDF**。無論您是構建報表引擎、自動筆記解決方案，或是文件轉換服務，本文所涵蓋的技術都能協助您 **save OneNote as PDF**，並精確控制格式。

## Quick Answers
- **「set paragraph style」是什麼意思？** 它會將字型、大小、顏色及其他格式套用到段落文字上。  
- **我可以將結果匯出為 PDF 嗎？** 可以——本教學最後會將 OneNote 檔案儲存為 PDF。  
- **使用 Aspose.Note 需要授權嗎？** 免費試用可用於評估；正式環境需購買授權。  
- **支援哪些 IDE？** 任何 Java IDE – Eclipse、IntelliJ IDEA、NetBeans 等。  
- **實作大約需要多久？** 基本文件約需 10‑15 分鐘。

## What is “set paragraph style” in Aspose.Note?
在 Aspose.Note 中，「set paragraph style」指的是設定 `ParagraphStyle` 物件（字型名稱、大小、顏色等），並將其附加至 `RichText` 節點。這讓您能完整掌控 OneNote 頁面內文字的顯示方式。

## How to Set Paragraph Style in OneNote?
套用樣式非常簡單，只需建立 `ParagraphStyle` 實例、客製化其屬性，然後指派給 `RichText` 元素。API 讓此操作在樣式物件準備好後只需一行程式碼即可完成。

## Why Export OneNote to PDF?
- **一致的品牌形象：** 在對外分享筆記時保留公司字型與顏色。  
- **可讀性：** PDF 保持精確版面，適合列印或存檔。  
- **跨平台存取：** 收件人可在任何裝置上開啟 PDF，無需安裝 OneNote。  

## Prerequisites

在開始之前，請確保您已具備以下條件：

1. **Java Development Kit (JDK) 1.8+** – 任何較新的 JDK 都可使用。  
2. **Aspose.Note for Java** – 從 [Aspose.Note 下載頁面](https://releases.aspose.com/note/java/) 取得最新 JAR。  
3. **IDE**（Eclipse、IntelliJ IDEA 或 NetBeans）用於編譯與執行範例。  

> **專業提示：** 透過 Maven 或在 IDE 中手動引用 JAR，將 Aspose.Note JAR 加入專案的 classpath。

## Import Packages

首先，匯入我們將使用的類別。此區塊保持不變。

```java
import java.awt.Color;
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.SaveFormat;
import com.aspose.note.ParagraphStyle;
```

> `ParagraphStyle` 類別是稍後 **set paragraph style** 的關鍵。

## Step‑by‑Step Guide

以下是每個步驟的簡要說明。程式碼區塊與原始範例完全相同，我們僅加入說明文字。

### Step 1: Set Document Directory
設定產生檔案的儲存目錄。

```java
String dataDir = "Your Document Directory";
```

將 `"Your Document Directory"` 替換為您機器上的絕對或相對路徑。

### Step 2: Initialize Document Object
建立代表 OneNote 檔案的根 `Document` 物件。

```java
Document doc = new Document();
```

### Step 3: Initialize Page Object
OneNote 檔案由一或多個頁面組成；此處先建立單一頁面。

```java
Page page = new Page();
```

### Step 4: Initialize Outline Object
Outline 為大綱元素的容器（可視為章節）。

```java
Outline outline = new Outline();
```

### Step 5: Initialize OutlineElement Object
在此 **add outline element**，用以容納我們的富文字。

```java
OutlineElement outlineElem = new OutlineElement();
```

### Step 6: Set Text Style (Set Paragraph Style)

```java
ParagraphStyle textStyle = new ParagraphStyle()
                                    .setFontColor(Color.black)
                                    .setFontName("Arial")
                                    .setFontSize(10);
```

`ParagraphStyle` 實例定義字型、大小與顏色——這裡就是為即將加入的文字節點 **set paragraph style** 的地方。

### Step 7: Initialize RichText Object

```java
RichText text = new RichText().append("Hello OneNote text!");
text.setParagraphStyle(textStyle);
```

我們建立 `RichText` 節點，插入簡單字串，並套用先前定義的樣式。

### Step 8: Add RichText Node to OutlineElement

```java
outlineElem.appendChildLast(text);
```

現在已將樣式化文字放入大綱元素中。

### Step 9: Add OutlineElement Node to Outline

```java
outline.appendChildLast(outlineElem);
```

大綱現在包含了持有段落的元素。

### Step 10: Add Outline Node to Page

```java
page.appendChildLast(outline);
```

我們將大綱放置於頁面上。

### Step 11: Add Page Node to Document

```java
doc.appendChildLast(page);
```

文件現在有一個包含樣式化文字的單一頁面。

### Step 12: Save the Document (Export OneNote PDF)

```java
doc.save(dataDir + "CreateOneNoteDocumentWithSimpleRichText_out.pdf", SaveFormat.Pdf);
```

`save` 方法一次寫入 OneNote 檔案並 **exports OneNote PDF**。若需原生格式，也可使用 `SaveFormat.One` 儲存為 `.one`。

## Common Issues & Solutions

| 問題 | 原因 | 解決方案 |
|-------|--------|-----|
| **File not found** | `dataDir` 指向不存在的資料夾。 | 確認目錄已存在，或以程式方式建立 (`new File(dataDir).mkdirs();`)。 |
| **Blank PDF** | 儲存前未加入任何內容。 | 檢查已將 `RichText` 節點加入，且已設定樣式。 |
| **Unsupported font** | 系統未安裝指定字型。 | 使用常見字型如 `"Arial"`，或將字型嵌入專案中。 |

## Frequently Asked Questions

**Q: Aspose.Note 能處理如表格或圖片等複雜格式嗎？**  
A: 能，API 支援表格、圖片、超連結以及更進階的版面配置功能。

**Q: 能否 **convert OneNote PDF** 回 OneNote 檔案？**  
A: 目前未提供直接轉換，但您可抽取 PDF 內容，並使用 API 重新建立 OneNote 文件。

**Q: 此函式庫能在 Linux/macOS 環境下運作嗎？**  
A: 當然可以。Aspose.Note for Java 與平台無關，只要安裝 JDK 即可。

**Q: 如何加入多個頁面或大綱？**  
A: 建立額外的 `Page` 與 `Outline` 物件，然後像單頁範例一樣將它們附加至 `Document`。

**Q: 哪裡可以找到更多範例？**  
A: 官方 Aspose.Note 文件與 [支援論壇](https://forum.aspose.com/c/note/28) 提供大量程式碼範例。

## Conclusion

您現在已了解如何 **set paragraph style**、**add outline element**，以及使用 Aspose.Note for Java **generate a OneNote file** 並 **export to PDF**。在建立文件時即套用樣式，可確保最終文件具備專業外觀，且任何後續的 **convert OneNote PDF** 動作都能保留格式。歡迎在此基礎上加入圖片、表格或自訂中繼資料，以滿足專案需求。

---

**最後更新：** 2026-02-18  
**測試環境：** Aspose.Note for Java 24.11（最新發行版）  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}