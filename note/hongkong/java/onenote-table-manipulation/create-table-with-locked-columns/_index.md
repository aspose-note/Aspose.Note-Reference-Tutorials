---
title: 在 OneNote 中建立具有鎖定列的表 - Aspose.Note
linktitle: 在 OneNote 中建立具有鎖定列的表 - Aspose.Note
second_title: Aspose.Note Java API
description: 使用 Aspose.Note for Java 增強您的 OneNote 體驗。了解如何使用逐步指南建立具有鎖定列的表。立即下載免費試用版！
weight: 12
url: /zh-hant/java/onenote-table-manipulation/create-table-with-locked-columns/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 在 OneNote 中建立具有鎖定列的表 - Aspose.Note

## 介紹
OneNote 是用於組織資訊的強大工具，Aspose.Note for Java 透過提供無縫方式建立具有鎖定列的表來增強其功能。在本教學中，我們將引導您完成使用 Aspose.Note for Java 在 OneNote 中建立具有鎖定列的表的過程。
## 先決條件
在開始之前，請確保您具備以下先決條件：
- [Java 開發工具包 (JDK)](https://www.oracle.com/java/technologies/javase-downloads.html)安裝在您的機器上。
- [用於 Java 的 Aspose.Note](https://downloads.aspose.com/note/java)庫已下載並新增至您的專案。
## 導入包
在您的 Java 專案中，匯入使用 Aspose.Note 所需的套件：
```java
import com.aspose.note.*;
import java.io.IOException;
```
## 第 1 步：設定您的項目
首先建立一個新的 Java 專案並將 Aspose.Note 庫新增到類別路徑中。確保您的專案配置為使用 JDK。
## 第 2 步：初始化文件和頁面對象
```java
//文檔目錄的路徑。
String dataDir = "Your Document Directory";
//建立Document類別的對象
Document doc = new Document();
//初始化Page類別物件
Page page = new Page();
```
## 第 3 步：建立表格行和儲存格
```java
//初始化TableRow類別對象
TableRow row1 = new TableRow();
//初始化TableCell類別物件並設定文字內容
TableCell cell11 = new TableCell();
cell11.appendChildLast(InsertTable.GetOutlineElementWithText("Small text"));
row1.appendChildLast(cell11);
//初始化TableRow類別對象
TableRow row2 = new TableRow();
//初始化TableCell類別物件並設定文字內容
TableCell cell21 = new TableCell();
cell21.appendChildLast(InsertTable.GetOutlineElementWithText("Long   text    with    several   words and    spaces."));
row2.appendChildLast(cell21);
```
## 第 4 步：建立並自訂表格
```java
//初始化Table類別物件
Table table = new Table();
table.setBordersVisible(true);
TableColumn col = new TableColumn();
col.setWidth(200);
col.setLockedWidth(true);
table.getColumns().addItem(col);
//新增行
table.appendChildLast(row1);
table.appendChildLast(row2);
```
## 步驟5：將表格加入大綱和頁面
```java
Outline outline = new Outline();
OutlineElement outlineElem = new OutlineElement();
//新增表節點
outlineElem.appendChildLast(table);
//新增輪廓元素節點
outline.appendChildLast(outlineElem);
//新增輪廓節點
page.appendChildLast(outline);
//新增頁面節點
doc.appendChildLast(page);
```
## 第 6 步：儲存文檔
```java
dataDir = dataDir + "CreateTableWithLockedColumns_out.one";
doc.save(dataDir);
```
恭喜！您已使用 Aspose.Note for Java 在 OneNote 中成功建立了帶有鎖定列的表。
## 結論
在本教程中，我們探索了利用 Aspose.Note for Java 透過建立具有鎖定列的表來增強 OneNote 體驗的過程。此功能為您的筆記添加了新的組織和結構層。
## 常見問題解答
### Aspose.Note for Java 是否與所有 Java 版本相容？
是的，Aspose.Note for Java 與 Java 6 及更高版本相容。
### 我可以進一步自訂表格的外觀嗎？
絕對地！ Aspose.Note for Java 提供了廣泛的自訂表格選項，例如調整邊框、儲存格間距等。
### 購買前是否有試用版？
是的你可以[下載免費試用版](https://releases.aspose.com/)探索 Aspose.Note for Java 的功能。
### 我可以在哪裡找到其他支持或社區討論？
參觀[Aspose.Note 論壇](https://forum.aspose.com/c/note/28)用於支持和社區討論。
### 如何取得 Aspose.Note for Java 的臨時授權？
訪問[這個連結](https://purchase.aspose.com/temporary-license/)取得用於測試目的的臨時許可證。
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
