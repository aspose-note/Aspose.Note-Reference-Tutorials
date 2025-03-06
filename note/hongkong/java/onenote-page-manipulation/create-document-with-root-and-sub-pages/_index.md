---
title: 在 OneNote 中建立包含根頁面和子頁面的文檔
linktitle: 在 OneNote 中建立包含根頁面和子頁面的文檔
second_title: Aspose.Note Java API
description: 使用 Aspose.Note for Java 在 OneNote 中建立包含根頁面和子頁面的文件。按照逐步指南有效地組織您的筆記。
weight: 11
url: /zh-hant/java/onenote-page-manipulation/create-document-with-root-and-sub-pages/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 在 OneNote 中建立包含根頁面和子頁面的文檔

## 介紹

在本教學中，我們將引導您完成使用 Aspose.Note for Java 在 OneNote 中建立包含根頁面和子頁面的文件的過程。透過執行這些步驟，您將能夠以層次結構有效地組織 OneNote 文件。

## 先決條件

在開始之前，請確保您具備以下先決條件：

1. Java 開發工具包 (JDK)：確保您的系統上安裝了 JDK。
2. Aspose.Note for Java：從下列位置下載並安裝 Aspose.Note for Java：[網站](https://purchase.aspose.com/buy).
3. 整合開發環境 (IDE)：選擇 Java IDE，例如 IntelliJ IDEA、Eclipse 或 NetBeans。

## 導入包

首先在 Java 專案中匯入必要的套件：

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.SaveFormat;
import com.aspose.note.ParagraphStyle;
```

## 第 1 步：設定文檔目錄

定義要儲存 OneNote 文件的目錄：

```java
String dataDir = "Your Document Directory";
```

## 步驟2：建立文檔對象

實例化一個`Document`目的：

```java
Document doc = new Document();
```

## 第 3 步：建立頁面

初始化頁面物件並設定其層級：

```java
Page page1 = new Page();
page1.setLevel((byte) 1);

Page page2 = new Page();
page2.setLevel((byte) 2);

Page page3 = new Page();
page3.setLevel((byte) 1);
```

## 第四步：為頁面新增節點

### 將節點加入首頁

```java
Outline outline = new Outline();
OutlineElement outlineElem = new OutlineElement();
ParagraphStyle textStyle = new ParagraphStyle()
                                    .setFontColor(Color.black)
                                    .setFontName("David Transparent")
                                    .setFontSize(10);

RichText text = new RichText().append("First page.");
text.setParagraphStyle(textStyle);

outlineElem.appendChildLast(text);
outline.appendChildLast(outlineElem);
page1.appendChildLast(outline);
```

### 將節點加入第二頁

```java
Outline outline2 = new Outline();
OutlineElement outlineElem2 = new OutlineElement();
ParagraphStyle textStyle2 = new ParagraphStyle()
                                    .setFontColor(Color.black)
                                    .setFontName("David Transparent")
                                    .setFontSize(10);

RichText text2 = new RichText().append("Second page.");
text2.setParagraphStyle(textStyle2);

outlineElem2.appendChildLast(text2);
outline2.appendChildLast(outlineElem2);
page2.appendChildLast(outline2);
```

### 將節點加入第三頁

```java
Outline outline3 = new Outline();
OutlineElement outlineElem3 = new OutlineElement();
ParagraphStyle textStyle3 = new ParagraphStyle()
                                    .setFontColor(Color.black)
                                    .setFontName("Broadway")
                                    .setFontSize(10);

RichText text3 = new RichText().append("Third page.");
text3.setParagraphStyle(textStyle3);

outlineElem3.appendChildLast(text3);
outline3.appendChildLast(outlineElem3);
page3.appendChildLast(outline3);
```

## 步驟 5：將頁面新增至文檔

```java
doc.appendChildLast(page1);
doc.appendChildLast(page2);
doc.appendChildLast(page3);
```

## 第 6 步：儲存文檔

儲存 OneNote 文件：

```java
try {
    doc.save(dataDir + "GenerateRootAndSubLevelPagesInOneNote_out.bmp", SaveFormat.Bmp);
} catch (IOException e) {
    //處理例外
}
```

恭喜！您已使用 Aspose.Note for Java 在 OneNote 中成功建立了包含根頁面和子頁面的文件。

## 結論

使用層次結構組織 OneNote 文件對於更好的管理和導航至關重要。使用 Aspose.Note for Java，您可以有效率地建立具有根頁面和子頁面的文檔，為您的筆記提供清晰且有組織的佈局。

## 常見問題解答

### Q1：我可以使用Aspose.Note for Java 建立多個層級的子頁面嗎？

A1：是的，您可以透過為每個頁面設定適當的層級來建立多個層級的子頁面。

### Q2：Aspose.Note for Java 是否相容於不同的 Java IDE？

A2：是的，Aspose.Note for Java 與流行的 Java IDE 相容，例如 IntelliJ IDEA、Eclipse 和 NetBeans。

### Q3：我可以自訂 OneNote 文件中的文字格式嗎？

A3：是的，您可以使用 Aspose.Note for Java 的富文本功能自訂字體、顏色、大小和其他格式選項。

### Q4：Aspose.Note for Java支援保存不同格式的文件嗎？

A4：是的，Aspose.Note for Java 支援以各種格式儲存文檔，包括 BMP、PDF、PNG 等。

### Q5：Aspose.Note for Java 有試用版嗎？

A5：是的，您可以從網站下載 Aspose.Note for Java 的免費試用版。
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
