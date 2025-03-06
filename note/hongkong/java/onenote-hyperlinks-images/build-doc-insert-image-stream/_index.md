---
title: 在 OneNote 中使用流來建立文件並插入圖像 - Java
linktitle: 在 OneNote 中使用流來建立文件並插入圖像 - Java
second_title: Aspose.Note Java API
description: 了解如何使用 Aspose.Note for Java 輕鬆將圖像整合到 OneNote 文件中。面向 Java 開發人員的分步教程。
weight: 13
url: /zh-hant/java/onenote-hyperlinks-images/build-doc-insert-image-stream/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 在 OneNote 中使用流來建立文件並插入圖像 - Java

## 介紹

歡迎來到我們關於使用 Aspose.Note for Java 在 OneNote 中使用圖像流建立文件和插入圖像的綜合教學！在本教程中，我們將逐步引導您完成整個過程，確保您清楚地了解每個階段。最後，您將能夠使用 Java 輕鬆地將圖像整合到 OneNote 文件中。

## 先決條件

在我們深入學習本教程之前，請確保您具備以下先決條件：

### Java 開發工具包 (JDK)

確保您的系統上安裝了 Java 開發工具包 (JDK)。您可以從 Oracle 網站下載它。

### Java 函式庫的 Aspose.Note

從提供的下載並安裝 Aspose.Note for Java 庫[關聯](https://releases.aspose.com/note/java/).

### IDE設定

使用必要的配置設定整合開發環境 (IDE)，以處理 Java 專案。

## 導入包

首先，將所需的套件匯入到您的 Java 專案中。這些套件將提供處理 OneNote 文件和圖像所需的功能。

```java
import java.io.FileInputStream;
import java.io.FileNotFoundException;
import java.io.IOException;
import java.io.InputStream;
import com.aspose.note.Document;
import com.aspose.note.HorizontalAlignment;
import com.aspose.note.Image;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.SaveFormat;
```

## 第 1 步：設定文檔目錄

定義文件和圖像所在的目錄。代替`"Your Document Directory"`與您的目錄的路徑。

```java
String dataDir = "Your Document Directory";
```

## 步驟2：建立文檔對象

初始化一個實例`Document`類別開始使用您的 OneNote 文件。

```java
Document doc = new Document();
```

## 第三步：初始化頁面對象

創建一個`Page`物件來表示文檔中的頁面。

```java
Page page = new Page();
```

## 第 4 步：建立大綱

初始化一個`Outline`物件來建構頁面內的內容。

```java
Outline outline1 = new Outline();
outline1.setVerticalOffset(600);
outline1.setHorizontalOffset(0);
```

## 第5步：建立輪廓元素

創建一個`OutlineElement`儲存影像並指定其位置。

```java
OutlineElement outlineElem1 = new OutlineElement();
```

## 第6步：載入圖像流

使用載入圖像流`FileInputStream`以獲得所需的圖像。

```java
InputStream fs = null;
try {
    fs = new FileInputStream(dataDir + "image.jpg");
} catch (FileNotFoundException e) {
    e.printStackTrace();
}
```

## 第7步：插入圖片

透過建立一個將圖像插入到文件中`Image`對象並設定其對齊方式。

```java
Image image = new Image(null, dataDir + "image1.jpg");
image.setAlignment(HorizontalAlignment.Right);
```

## 第 8 步：將影像附加到輪廓元素

將影像附加到輪廓元素。

```java
outlineElem1.appendChildLast(image);
```

## 第 9 步：將大綱元素附加到大綱

將輪廓元素加入輪廓。

```java
outline1.appendChildLast(outlineElem1);
```

## 第 10 步：將大綱附加到頁面

將輪廓新增至頁面。

```java
page.appendChildLast(outline1);
```

## 第 11 步：將頁面附加到文檔

最後，將頁面附加到文件中。

```java
doc.appendChildLast(page);
```

## 第12步：儲存文檔

儲存修改後的文檔，指定所需的格式（例如 PDF）。

```java
try {
    doc.save("D://Aspose_JavaProjects//OneNote//out3.pdf", SaveFormat.Pdf);
} catch (IOException e) {
    e.printStackTrace();
}
```

透過執行這些步驟，您可以使用 Aspose.Note for Java 在 OneNote 中輕鬆建立文件並使用圖像流插入圖像。

## 結論

總之，掌握使用 Java 將影像整合到 OneNote 文件中可以顯著增強文件建立過程。透過 Aspose.Note for Java，您可以使用一個強大的工具來無縫地完成此任務。

## 常見問題解答

### Q1：Aspose.Note for Java 是否相容於所有版本的 OneNote？

A1：Aspose.Note for Java支援各種版本的OneNote，確保不同環境下的相容性。

### Q2：我可以使用 Aspose.Note for Java 自訂 OneNote 文件中插入影像的外觀嗎？

A2：是的，您可以自訂插入影像的各個方面，例如對齊方式、大小和方向，以滿足您的特定要求。

### Q3：Aspose.Note for Java 是否提供 PDF 以外的其他文件格式的支援？

A3：是的，Aspose.Note for Java 支援多種文件格式，包括 DOCX、HTML 等，為您的文件管理任務提供彈性。

### 問題 4：在哪裡可以找到 Aspose.Note for Java 的其他資源和支援？

A4：您可以透過提供的連結存取 Aspose.Note for Java 的文件、下載連結、支援論壇和臨時授權。

### Q5：Aspose.Note for Java 有試用版嗎？

A5：是的，您可以在做出購買決定之前獲得 Aspose.Note for Java 的免費試用版，以探索其功能和功能。

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
