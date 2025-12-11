---
date: 2025-12-08
description: 學習如何在 Java 中使用 Aspose.Note 設定段落樣式並新增大綱元素以建立 OneNote 文件。輕鬆將 OneNote 匯出為
  PDF 並產生 OneNote 檔案。
language: zh-hant
linktitle: Set Paragraph Style while Creating OneNote Document in Java
second_title: Aspose.Note Java API
title: 在 Java 中建立 OneNote 文件時設定段落樣式
url: /java/onenote-document-manipulation/create-onenote-document-simple-rich-text/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 在 Java 中建立 OneNote 文件時設定段落樣式

## 介紹

在當前快速變化的開發環境中，能以程式方式 **設定段落樣式** 對於產出精緻的 OneNote 檔案至關重要。本教學將一步步示範如何產生帶有簡易富文字的 OneNote 文件、套用自訂段落格式，最後使用 Aspose.Note for Java **將 OneNote 匯出為 PDF**。無論您是在建構報表引擎、自動筆記解決方案，或是文件轉換服務，本文所涵蓋的技巧都能協助您 **產生符合需求的 OneNote 檔案**。

## 快速問答
- **「設定段落樣式」是什麼意思？** 它會將字型、大小、顏色等格式套用到一段文字上。  
- **可以把結果匯出成 PDF 嗎？** 可以──教學最後會示範將 OneNote 檔案儲存為 PDF。  
- **使用 Aspose.Note 需要授權嗎？** 評估階段可使用免費試用版，正式上線則需購買授權。  
- **支援哪些 IDE？** 任何 Java IDE 都可──Eclipse、IntelliJ IDEA、NetBeans 等。  
- **實作大約需要多久？** 基本文件約 10‑15 分鐘即可完成。

## Aspose.Note 中的「設定段落樣式」是什麼？
設定段落樣式指的是建立並設定 `ParagraphStyle` 物件（字型名稱、大小、顏色等），再將其附加到 `RichText` 節點上。如此即可完整掌控 OneNote 頁面內文字的外觀。

## 為什麼在產生 OneNote 檔案時要設定段落樣式？
- **一致的品牌形象：** 自動套用公司字型與色彩。  
- **可讀性：** 較大的字型或特定顏色有助於提升可及性。  
- **匯出相容性：** 之後 **將 OneNote 轉換為 PDF** 時，樣式會被完整保留。  

## 前置作業

在開始之前，請先確認您已具備：

1. **Java Development Kit (JDK) 1.8+** ─ 任何近期版本皆可。  
2. **Aspose.Note for Java** ─ 從 [Aspose.Note 下載頁面](https://releases.aspose.com/note/java/) 取得最新 JAR。  
3. **IDE** (Eclipse、IntelliJ IDEA 或 NetBeans) 用於編譯與執行範例。  

> **小技巧：** 透過 Maven 或手動將 Aspose.Note JAR 加入專案 classpath，即可完成設定。

## 匯入套件

首先匯入所需的類別。此區塊保持不變。

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

> `ParagraphStyle` 類別是本教學稍後 **設定段落樣式** 的關鍵。

## 步驟說明

以下為每個操作的簡明流程。程式碼區塊與原始範例完全相同，我們僅補充說明文字。

### 步驟 1：設定文件目錄
指定產生檔案的儲存位置。

```java
String dataDir = "Your Document Directory";
```

將 `"Your Document Directory"` 替換為您機器上的絕對或相對路徑。

### 步驟 2：初始化 Document 物件
建立代表 OneNote 檔案的根 `Document`。

```java
Document doc = new Document();
```

### 步驟 3：初始化 Page 物件
OneNote 檔案由一或多個頁面組成，我們先建立單一頁面。

```java
Page page = new Page();
```

### 步驟 4：初始化 Outline 物件
Outline 為大綱元素的容器（可視為章節）。

```java
Outline outline = new Outline();
```

### 步驟 5：初始化 OutlineElement 物件
在此 **加入大綱元素**，用以容納富文字。

```java
OutlineElement outlineElem = new OutlineElement();
```

### 步驟 6：設定文字樣式（設定段落樣式）

```java
ParagraphStyle textStyle = new ParagraphStyle()
                                    .setFontColor(Color.black)
                                    .setFontName("Arial")
                                    .setFontSize(10);
```

`ParagraphStyle` 實例定義字型、大小與顏色──這裡即為即將加入的文字節點 **設定段落樣式** 的地方。

### 步驟 7：初始化 RichText 物件

```java
RichText text = new RichText().append("Hello OneNote text!");
text.setParagraphStyle(textStyle);
```

建立 `RichText` 節點、插入簡單字串，並套用先前定義的樣式。

### 步驟 8：將 RichText 節點加入 OutlineElement

```java
outlineElem.appendChildLast(text);
```

此時已將帶樣式的文字放入大綱元素內。

### 步驟 9：將 OutlineElement 節點加入 Outline

```java
outline.appendChildLast(outlineElem);
```

大綱現在包含了持有段落的元素。

### 步驟 10：將 Outline 節點加入 Page

```java
page.appendChildLast(outline);
```

將大綱放置於頁面上。

### 步驟 11：將 Page 節點加入 Document

```java
doc.appendChildLast(page);
```

文件現在只有一個頁面，內含已套用樣式的文字。

### 步驟 12：儲存文件（匯出 OneNote PDF）

```java
doc.save(dataDir + "CreateOneNoteDocumentWithSimpleRichText_out.pdf", SaveFormat.Pdf);
```

`save` 方法一次寫入 OneNote 檔案並 **匯出 OneNote PDF**。若需原生格式，只要使用 `SaveFormat.One` 即可儲存為 `.one`。

## 常見問題與解決方案

| 問題 | 原因 | 解決方式 |
|------|------|----------|
| **找不到檔案** | `dataDir` 指向不存在的資料夾。 | 確認目錄已建立，或以程式碼 `new File(dataDir).mkdirs();` 先建立。 |
| **PDF 為空白** | 儲存前未加入任何內容。 | 確認已將 `RichText` 節點加入，且樣式已設定。 |
| **不支援的字型** | 系統未安裝指定字型。 | 改用常見字型如 `"Arial"`，或將字型檔嵌入專案。 |

## 常見問答

**Q: Aspose.Note 能處理表格或圖片等複雜格式嗎？**  
A: 能，API 支援表格、圖片、超連結以及更進階的版面配置。

**Q: 能否 **將 OneNote PDF 轉回 OneNote 檔案**？**  
A: 目前未提供直接轉換，但可先解析 PDF 內容，再利用 API 重建 OneNote 文件。

**Q: 此函式庫能在 Linux/macOS 上執行嗎？**  
A: 能。Aspose.Note for Java 為跨平台套件，只要安裝 JDK 即可。

**Q: 如何加入多個頁面或大綱？**  
A: 建立額外的 `Page` 與 `Outline` 物件，然後像單頁範例一樣將它們加入 `Document`。

**Q: 哪裡可以找到更多範例？**  
A: 官方 Aspose.Note 文件與 [支援論壇](https://forum.aspose.com/c/note/28) 提供大量程式碼範例。

## 結論

您現在已了解如何 **設定段落樣式**、**加入大綱元素**，以及使用 Aspose.Note for Java **產生可匯出為 PDF 的 OneNote 檔案**。在建立文件時即套用樣式，可確保最終文件的專業外觀，且在之後的 **將 OneNote 轉換為 PDF** 操作中保持格式不變。歡迎在此基礎上加入圖片、表格或自訂中繼資料，以滿足您的專案需求。

---

**最後更新：** 2025-12-08  
**測試環境：** Aspose.Note for Java 24.11（最新發行版）  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}