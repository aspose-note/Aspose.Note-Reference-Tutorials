---
title: 使用文件存取器提取 OneNote 內容 - Java
linktitle: 使用文件存取器提取 OneNote 內容 - Java
second_title: Aspose.Note Java API
description: 了解如何使用 Aspose.Note for Java 從 Java 中的 OneNote 文件中提取內容。提供了帶有程式碼範例的逐步教學。
type: docs
weight: 21
url: /zh-hant/java/onenote-document-loading/extract-content-using-document-visitor/
---
## 介紹

Aspose.Note for Java 提供了從 OneNote 文件中提取內容的強大功能。在本教學中，我們將引導您完成使用 Java 中的文件存取器從 OneNote 文件中提取內容的過程。

## 先決條件

在開始之前，請確保您具備以下條件：

1. 您的系統上安裝了 Java 開發工具包 (JDK)。
2. 下載了 Java 函式庫的 Aspose.Note。你可以下載它[這裡](https://releases.aspose.com/note/java/).
3. 要從中提取內容的 OneNote 文件（擴展名為 .one）。

## 導入包

首先，您需要匯入必要的套件才能使用 Aspose.Note for Java。

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

## 第 1 步：設定文件訪客類

建立一個類別來擴展`DocumentVisitor`Aspose.Note for Java 提供的類別。此類將處理存取文件的不同節點。

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
    
    //其他方法將在這裡實現
}
```

## 第 2 步：實現訪客方法

為文件中要處理的不同類型的節點實作訪客方法。在此範例中，我們將為 RichText、Document、Page、Title、Image、OutlineGroup、Outline 和 OutlineElement 節點實作方法。

```java
//不同類型節點的訪客方法

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

## 第三步：主要方法

在 main 方法中，載入 OneNote 文檔，建立自訂文檔訪客類別的實例，並接受訪客以啟動存取程序。

```java
public static void main(String[] args) throws IOException {
    //開啟我們要轉換的文檔。
    String dataDir = "Your Document Directory";
    Document doc = new Document(dataDir + "Sample1.one", new LoadOptions());
    
    //建立一個繼承自 DocumentVisitor 類別的物件。
    ExtractOneNoteContentUsingDocumentvisitor myConverter = new ExtractOneNoteContentUsingDocumentvisitor();
    
    //接受訪客以開始訪問流程。
    doc.accept(myConverter);
    
    //檢索操作結果。
    System.out.println(myConverter.GetText());
    System.out.println(myConverter.NodeCount());
}
```

## 結論

在本教學中，您學習如何使用 Aspose.Note for Java 從 OneNote 文件中提取內容。透過實現自訂文件訪客類別並存取文件的不同節點，您可以根據您的要求有效地提取和處理內容。

## 常見問題解答

### Q1：我可以從 OneNote 文件中提取特定類型的內容嗎？

A1：是的，透過為不同的節點類型實現特定的訪客方法，您可以選擇性地提取文字、圖像、標題等內容。

### Q2：Aspose.Note for Java 是否相容於不同版本的 OneNote 文件？

A2：Aspose.Note for Java支援各種版本的OneNote文檔，確保相容性和內容順利提取。

### Q3：我可以將此提取過程整合到我的 Java 應用程式中嗎？

A3：當然，您可以按照提供的教學輕鬆地將內容提取過程整合到您的 Java 應用程式中。

### Q4：Aspose.Note for Java 是否支援處理複雜的 OneNote 文件？

A4：是的，Aspose.Note for Java 為處理 OneNote 文件中的複雜結構和內容提供了全面的支援。

### Q5：使用 Aspose.Note for Java 處理的 OneNote 文件的大小有限制嗎？

A5：Aspose.Note for Java 旨在高效處理各種大小的 OneNote 文檔，即使處理大型文檔也能確保最佳效能。