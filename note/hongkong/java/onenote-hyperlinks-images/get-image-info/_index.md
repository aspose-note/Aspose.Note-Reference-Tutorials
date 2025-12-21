---
date: 2025-12-21
description: 學習如何使用 Aspose.Note 在 Java 中取得圖像尺寸。只需幾個步驟，即可從 OneNote 檔案中提取寬度、高度、檔名等資訊。
linktitle: Get Image Dimensions Java from OneNote
second_title: Aspose.Note Java API
title: 從 OneNote 取得圖像尺寸（Java）
url: /zh-hant/java/onenote-hyperlinks-images/get-image-info/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 從 OneNote 取得 Image Dimensions Java

## 介紹

如果您需要 **從 OneNote 筆記本取得 image dimensions java**，您來對地方了。在許多自動化情境——報告產生、內容遷移或分析——中，您會想在不手動開啟筆記本的情況下，取得每張圖片的寬度、高度、原始大小以及檔名。本教學將帶您使用 Aspose.Note for Java 以程式方式擷取這些資訊。

## 快速回答
- **程式碼的功能是什麼？** 取得 OneNote 檔案中的所有圖片，並列印其尺寸、原始大小、檔名與修改日期。  
- **需要哪個函式庫？** Aspose.Note for Java。  
- **需要授權嗎？** 測試可使用臨時授權；正式上線需購買完整授權。  
- **程式碼行數多少？** 約 30 行，分為清晰且可重用的步驟。  
- **一般執行時間？** 對於含數十張圖片的標準筆記本，執行時間為毫秒級。

## 前置條件

在開始實作之前，請先確保您已具備以下前置條件：

### 1. Java Development Kit (JDK)

請確認您的系統已安裝 Java Development Kit (JDK)。您可以從 [Oracle website](https://www.oracle.com/java/technologies/javase-jdk15-downloads.html) 下載並安裝最新的 JDK。

### 2. Aspose.Note for Java 函式庫

下載並將 Aspose.Note for Java 函式庫加入您的專案。您可以從 [download page](https://releases.aspose.com/note/java/) 取得此函式庫。

### 3. OneNote 文件

準備一份包含圖片的範例 OneNote 文件，該文件將用於程式化擷取圖片資訊。

## 匯入套件

首先，從 Aspose.Note for Java 匯入必要的套件：

```java
import java.io.IOException;
import java.util.List;
import com.aspose.note.Document;
import com.aspose.note.Image;
```

以下將上述程式碼逐步說明：

## 如何從 OneNote 取得 image dimensions java

### 步驟 1：設定文件目錄

```java
String dataDir = "Your Document Directory";
```

將 `"Your Document Directory"` 替換為您 OneNote 文件的路徑。

### 步驟 2：載入文件

```java
Document doc = new Document(dataDir + "Sample1.one");
```

使用 Aspose.Note for Java 函式庫載入 OneNote 文件。請確保提供正確的文件路徑。

### 步驟 3：取得所有圖片

```java
List<Image> list = doc.getChildNodes(Image.class);
```

從已載入的 OneNote 文件中取得全部圖片。

### 步驟 4：列印圖片總數

```java
System.out.printf("Total Images: %s\n\n", list.size());
```

列印文件中找到的圖片總數。

### 步驟 5：遍歷並列印圖片資訊

```java
for (Image image : list) {
    System.out.println("Width: " + image.getWidth());
    System.out.println("Height: " + image.getHeight());
    System.out.println("OriginalWidth: " + image.getOriginalWidth());
    System.out.println("OriginalHeight: " + image.getOriginalHeight());
    System.out.println("FileName: " + image.getFileName());
    System.out.println("LastModifiedTime: " + image.getLastModifiedTime());
    System.out.println();
}
```

遍歷圖片清單，為每張圖片列印寬度、高度、原始尺寸、檔名以及最後修改時間等詳細資訊。

## 為什麼要使用 Java 從 OneNote 抽取圖片？

- **自動化：** 消除手動檢查筆記本的需求。  
- **資料分析：** 將圖片中繼資料輸入報告管線。  
- **遷移：** 在將內容搬移至其他平台時保留圖片屬性。  
- **效能：** 僅取得所需的中繼資料，避免繁重的檔案解析。

## 常見問題與技巧

- **路徑錯誤：** 請再次確認 `dataDir` 以正確的檔案分隔符（`/` 或 `\`）結尾。  
- **授權問題：** 若未使用有效授權，Aspose.Note 可能會拋出評估警告。  
- **大型筆記本：** 若筆記本包含數千張圖片，建議分批處理以降低記憶體使用。

## 常見問答

### Q1：Aspose.Note for Java 能處理除 OneNote 之外的其他文件格式嗎？

A1：是的，Aspose.Note for Java 支援多種文件格式，包括 OneNote、PDF 以及 Microsoft Word。

### Q2：Aspose.Note for Java 可同時用於個人與商業用途嗎？

A2：是的，您可以將 Aspose.Note for Java 用於個人或商業目的。

### Q3：Aspose.Note for Java 提供技術支援嗎？

A3：是的，可透過 Aspose 論壇的 [here](https://forum.aspose.com/c/note/28) 取得技術支援。

### Q4：我可以在購買前試用 Aspose.Note for Java 嗎？

A4：可以，您可從 [Aspose.Note for Java](https://releases.aspose.com/note/java/) 下載免費試用版。

### Q5：如何取得 Aspose.Note for Java 的臨時授權？

A5：您可從 [Temporary license/](https://purchase.aspose.com/temporary-license/) 取得臨時授權。

## 結論

依循本教學所列步驟，您即可使用 Aspose.Note for Java 從 OneNote 文件中有效地 **取得 image dimensions java**。將此功能整合至您的應用程式，可自動化文件處理相關任務，提升效率與生產力。

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**最後更新：** 2025-12-21  
**測試環境：** Aspose.Note for Java 23.12  
**作者：** Aspose  

---