---
date: 2025-12-04
description: 學習如何從 OneNote 檔案中提取圖片，並使用 Aspose.Note 在 Java 中將 OneNote 轉換為文字。逐步指南，附有程式碼範例。
language: zh-hant
linktitle: Extract Images from OneNote using Document Visitor - Java
second_title: Aspose.Note Java API
title: 使用 Document Visitor 從 OneNote 提取圖片 - Java
url: /java/onenote-document-loading/extract-content-using-document-visitor/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 從 OneNote 使用 Document Visitor 提取圖像 - Java

## Introduction

Aspose.Note for Java 讓您輕鬆 **從 OneNote** 筆記本提取圖像，並在 Java 中讀取底層的 `.one` 檔案。 在本教學中，我們將帶您完成一個完整的實作範例，示範如何載入 OneNote 檔案、自訂的 `DocumentVisitor` 遍歷其結構，並提取圖像與純文字。 完成後，若只需要文字內容，您也會知道如何 **將 OneNote 轉換為文字**。

## Quick Answers
- **我需要哪個函式庫？** Aspose.Note for Java（下載連結如下）。  
- **我只能提取圖像嗎？** 是 – 在 `DocumentVisitor` 中實作 `VisitImageStart` 方法。  
- **如何在 Java 中讀取 .one 檔案？** 使用 `new Document(path, new LoadOptions())`。  
- **正式環境需要授權嗎？** 非試用時需購買商業授權。  
- **支援哪個 Java 版本？** JDK 8 或以上。

## Prerequisites

在開始之前，請確保您已具備：

1. 已安裝 Java Development Kit (JDK) 8 或更新版本。  
2. 已下載 Aspose.Note for Java 函式庫。您可於 **[此處](https://releases.aspose.com/note/java/)** 下載。  
3. 一個您想要提取圖像或轉換為文字的 OneNote 文件（`.one` 檔案）。

## Import Packages

首先，從 Aspose.Note API 匯入必要的類別。

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.DocumentVisitor;
import com.aspose.note.Image;
import com.aspose.note.LoadOptions;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.OutlineGroup;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.Title;
```

## Step 1: Set Up a Custom Document Visitor

建立一個繼承自 `DocumentVisitor` 的類別。此類別會在 OneNote 文件的每個節點被呼叫，讓您 **從 OneNote 提取圖像**，並可選擇性收集文字。

```java
public class ExtractOneNoteContentUsingDocumentvisitor extends DocumentVisitor {
    
    final private StringBuilder mBuilder;
    final private boolean mIsSkipText;
    private int nodecount;

    public ExtractOneNoteContentUsingDocumentvisitor() {
        nodecount = 0;
        mIsSkipText = false;
        mBuilder = new StringBuilder();
    }
    
    // Other methods will be implemented here
}
```

## Step 2: Implement Visitor Methods

為您關心的節點類型新增覆寫。以下示範處理富文字、圖像、標題、頁面、大綱及大綱元素。`VisitImageStart` 方法即負責圖像提取。

```java
// Visitor methods for different types of nodes

public /* override */ void VisitRichTextStart(RichText run) {
    ++nodecount;
    AppendText(run.getText());
}

public /* override */ void VisitDocumentStart(Document document) {
    ++nodecount;
}

public /* override */ void VisitPageStart(Page page) {
    ++nodecount;
}

public /* override */ void VisitTitleStart(Title title) {
    ++nodecount;
}

public /* override */ void VisitImageStart(Image image) {
    ++nodecount;
    // Here you could save the image to disk or process it further
    System.out.println("Found image with size: " + image.getData().length + " bytes");
}

public /* override */ void VisitOutlineGroupStart(OutlineGroup outlineGroup) {
    ++nodecount;
}

public void VisitOutlineStart(Outline outline) {
    ++nodecount;
}

public void VisitOutlineElementStart(OutlineElement outlineElement) {
    ++nodecount;
}
```

### Why implement these methods?

- **從 OneNote 提取圖像：** `VisitImageStart` 直接提供原始圖像位元組。  
- **將 OneNote 轉換為文字：** `VisitRichTextStart` 收集文字內容，讓您能簡單執行 **將 OneNote 轉換為文字** 的操作。  
- **在 Java 中讀取 .one 檔案：** Visitor 模式抽象底層 `.one` 檔案結構，您無需自行解析二進位格式。

## Step 3: Run the Visitor from Your Main Method

載入 `.one` 檔案，建立 Visitor 實例，然後開始遍歷。

```java
public static void main(String[] args) throws IOException {
    // Open the document we want to convert.
    String dataDir = "Your Document Directory";
    Document doc = new Document(dataDir + "Sample1.one", new LoadOptions());
    
    // Create an object that inherits from the DocumentVisitor class.
    ExtractOneNoteContentUsingDocumentvisitor myConverter = new ExtractOneNoteContentUsingDocumentvisitor();
    
    // Accept the visitor to start the visiting process.
    doc.accept(myConverter);
    
    // Retrieve the result of the operation.
    System.out.println(myConverter.GetText());   // Text extracted from the notebook
    System.out.println(myConverter.NodeCount()); // Total nodes visited
}
```

## Common Use Cases

- **自動化報告：** 從 OneNote 會議筆記本提取圖像與文字，生成 PDF 或 HTML 摘要。  
- **內容遷移：** 將舊版 OneNote 檔案轉換為純文字檔，以供索引或搜尋引擎匯入。  
- **數位資產提取：** 收集嵌入的螢幕截圖、圖表或照片，以便在其他應用程式中重複使用。

## Troubleshooting & Tips

- **大型筆記本：** 若遇記憶體問題，可逐頁處理，透過檢查 `VisitPageStart` 並僅在需要時載入頁面層級資源。  
- **圖像格式：** `Image` 物件回傳原始位元組，儲存前可能需要偵測格式（PNG、JPEG）。  
- **授權錯誤：** 在正式環境載入文件前，確保已設定 Aspose 授權 (`License license = new License(); license.setLicense("Aspose.Note.Java.lic");`)。

## Frequently Asked Questions

**Q: 我可以只提取 OneNote 文件中特定類型的內容嗎？**  
A: 可以 – 只覆寫您需要的 Visitor 方法（例如，`VisitImageStart` 用於圖像，`VisitRichTextStart` 用於文字）。

**Q: Aspose.Note for Java 是否相容於不同版本的 OneNote 文件？**  
A: 絕對相容。此函式庫支援所有主要的 OneNote 檔案版本，您可以安全地 **在 Java 中讀取 .one 檔案**，不論原始 OneNote 版本為何。

**Q: 我可以將此提取流程整合到我的 Java 應用程式中嗎？**  
A: 可以。Visitor 模式可無縫運作於任何 Java 程式碼中，只需加入函式庫 JAR 並呼叫上述範例即可。

**Q: Aspose.Note for Java 是否支援處理複雜的 OneNote 文件？**  
A: 支援。巢狀大綱、嵌入媒體與自訂資料皆可透過 Visitor API 取得。

**Q: 可處理的 OneNote 文件大小是否有限制？**  
A: 沒有硬性上限，但極大型筆記本可能需要更多堆疊記憶體；建議逐頁處理。

**Q: 如何將提取的文字轉換為純文字檔？**  
A: 在 `myConverter.GetText()` 回傳 `String` 後，使用標準 Java I/O 寫入檔案，例如 (`Files.write(Paths.get("output.txt"), text.getBytes());`)。

---  

**Last Updated:** 2025-12-04  
**Tested With:** Aspose.Note for Java 24.10  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}