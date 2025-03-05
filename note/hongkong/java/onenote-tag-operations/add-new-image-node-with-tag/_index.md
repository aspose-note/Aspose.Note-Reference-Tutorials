---
title: 在 OneNote 中新增帶有標籤的新圖片節點 - Aspose.Note
linktitle: 在 OneNote 中新增帶有標籤的新圖片節點 - Aspose.Note
second_title: Aspose.Note Java API
description: 了解如何使用 Aspose.Note for Java 在 OneNote 中新增帶有標籤的新映像節點。輕鬆提升您的 Java 程式設計技能。
type: docs
weight: 10
url: /zh-hant/java/onenote-tag-operations/add-new-image-node-with-tag/
---
## 介紹
在 Java 程式設計領域，Aspose.Note 作為輕鬆處理 OneNote 文件的強大工具而脫穎而出。如果您希望提高自己的技能並了解如何使用 Aspose.Note 在 OneNote 中添加帶有標籤的新圖像節點，那麼您來對地方了。本逐步指南將引導您完成整個過程，確保您徹底掌握每個概念。
## 先決條件
在我們深入學習本教程之前，讓我們確保您擁有所需的一切：
1.  Aspose.Note for Java：確保您已安裝 Aspose.Note 函式庫。如果沒有的話可以下載[這裡](https://releases.aspose.com/note/java/).
2. Java 開發環境：確保您的電腦上設定了有效的 Java 開發環境。
現在我們已經具備了先決條件，讓我們繼續下一步。
## 導入包
在您的 Java 專案中，首先匯入必要的套件：
```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.Image;
import com.aspose.note.NoteTag;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.SaveFormat;
import com.aspose.note.TagIcon;
```
## 第 1 步：建立文檔對象
```java
//文檔目錄的路徑。
String dataDir = "Your Document Directory";
//建立 Document 類別的對象
Document doc = new Document();
```
## 第2步：初始化頁面類別對象
```java
//初始化Page類別物件
Page page = new Page();
```
## 步驟3：初始化Outline類別對象
```java
//初始化 Outline 類別對象
Outline outline = new Outline();
```
## 步驟 4：初始化 OutlineElement 類別對象
```java
//初始化 OutlineElement 類別對象
OutlineElement outlineElem = new OutlineElement();
```
## 第 5 步：載入並插入圖像
```java
//載入圖片
Image image = new Image(null, dataDir + "Input.jpg");
//在文件節點中插入影像
outlineElem.appendChildLast(image);
```
## 第 6 步：在圖像上新增註釋標籤
```java
//向圖像添加黃色星形註釋標籤
NoteTag noteTag = NoteTag.createYellowStar();
image.getTags().add(noteTag);
```
## 第7步：新增輪廓元素節點
```java
//新增輪廓元素節點
outline.appendChildLast(outlineElem);
```
## 步驟8：新增輪廓節點
```java
//新增輪廓節點
page.appendChildLast(outline);
```
## 第9步：新增頁面節點
```java
//新增頁面節點
doc.appendChildLast(page);
```
## 步驟10：儲存OneNote文檔
```java
//將 OneNote 文件另存為 PDF
doc.save(dataDir + "AddNewImageNodeWithTag_out.pdf", SaveFormat.Pdf);
```
恭喜！您已使用 Aspose.Note for Java 在 OneNote 中成功新增了帶有標籤的新圖像節點。
## 結論
掌握 Aspose.Note for Java 為 OneNote 文件操作帶來了令人興奮的可能性。透過學習本教程，您將獲得可應用於各種專案的實用技能。繼續探索 Aspose.Note 文檔[這裡](https://reference.aspose.com/note/java/)以獲得更高級的功能和可能性。
## 常見問題解答
### 在哪裡可以找到 Aspose.Note 文件？
你可以找到文檔[這裡](https://reference.aspose.com/note/java/).
### 如何下載 Java 版 Aspose.Note？
您可以從發布頁面下載它[這裡](https://releases.aspose.com/note/java/).
### 有免費試用嗎？
是的，您可以免費試用[這裡](https://releases.aspose.com/).
### 在哪裡可以獲得 Aspose.Note 的支援？
訪問社區論壇[這裡](https://forum.aspose.com/c/note/28)為了支持。
### 我需要臨時許可證嗎？
如果需要，您可以獲得臨時許可證[這裡](https://purchase.aspose.com/temporary-license/).