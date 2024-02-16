---
title: 使用 Java 從 OneNote 文件中提取圖像
linktitle: 使用 Java 從 OneNote 文件中提取圖像
second_title: Aspose.Note Java API
description: 了解如何使用 Java 和 Aspose.Note 庫從 OneNote 文件中提取圖像。請按照我們的逐步指南進行無縫影像擷取。
type: docs
weight: 14
url: /zh-hant/java/onenote-hyperlinks-images/extract-images/
---
## 介紹

在本教程中，我們將指導您在 Aspose.Note 庫的幫助下完成使用 Java 從 OneNote 文件中提取圖像的過程。

## 先決條件

在開始之前，請確保您具備以下條件：

1.  Java 開發工具包 (JDK)：確保您的系統上安裝了 Java。您可以從以下位置下載並安裝它[網站](https://www.oracle.com/java/technologies/javase-jdk15-downloads.html).

2. Aspose.Note 函式庫：下載 Aspose.Note 函式庫並包含在您的 Java 專案中。您可以從[下載連結](https://releases.aspose.com/note/java/).

## 導入包

首先，導入必要的套件：

```java
import java.io.IOException;
import java.nio.file.Files;
import java.nio.file.Paths;
import java.util.List;
import com.aspose.note.Document;
import com.aspose.note.Image;
```

## 第 1 步：載入文檔

首先，使用 Aspose.Note 載入 OneNote 文件：

```java
String dataDir = "Your Document Directory";
Document doc = new Document(dataDir + "Sample1.one");
```

## 步驟2：取得所有影像

接下來，從文件中檢索所有影像：

```java
List<Image> list = doc.getChildNodes(Image.class);
System.out.printf("Total Images: %s\n\n", list.size());
```

## 第三步：提取影像

遍歷圖像列表並將每個圖像保存到文件中：

```java
for (int i = 0; i < list.size(); i++) {
    Image image = list.get(i);
    String outputFile = "ExtractImages_out" + i + "_" + image.getFileName();
    byte[] buffer = image.getBytes();
    Files.write(Paths.get(dataDir + outputFile), buffer);
    System.out.printf("File saved: %s\n", dataDir);
}
```

## 結論

使用 Java 從 OneNote 文件中提取圖像可以透過 Aspose.Note 庫無縫實現。透過遵循本教學中概述的步驟，您可以輕鬆地從文件中檢索影像以進行進一步處理或分析。

## 常見問題解答

### Q1：我可以從密碼保護的 OneNote 文件中提取圖像嗎？

A1：是的，Aspose.Note 也支援從受密碼保護的文件中提取圖像。

### Q2：Aspose.Note 是否相容於不同版本的 Java？

A2：Aspose.Note相容於各個版本的Java，確保開發人員的靈活性。

### Q3：我可以在一次執行中從多個 OneNote 文件中提取映像嗎？

A3：當然，您可以使用 Aspose.Note 迭代多個文件並從每個文件中提取圖像。

### Q4：OneNote 文件有大小限制嗎？

A4：Aspose.Note可以有效率地處理各種尺寸的文檔，確保影像擷取時對文檔尺寸沒有限制。

### Q5：Aspose.Note 是否支援提取除圖像之外的其他類型的內容？

A5：是的，除了圖像之外，Aspose.Note 還允許從 OneNote 文件中提取文字、附件和其他內容類型。