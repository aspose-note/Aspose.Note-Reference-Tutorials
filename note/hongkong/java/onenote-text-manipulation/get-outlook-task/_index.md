---
title: 在 OneNote 中取得 Outlook 任務 - Aspose.Note
linktitle: 在 OneNote 中取得 Outlook 任務 - Aspose.Note
second_title: Aspose.Note Java API
description: 探索 Aspose.Note for Java 輕鬆從 OneNote 文件中提取 Outlook 任務詳細資訊的潛力。使用這個強大的函式庫提升您的 Java 開發。
weight: 10
url: /zh-hant/java/onenote-text-manipulation/get-outlook-task/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 在 OneNote 中取得 Outlook 任務 - Aspose.Note

## 介紹
歡迎來到 Aspose.Note for Java 的世界——這是一個強大的工具，使 Java 開發人員能夠無縫地使用 Microsoft OneNote 檔案。在本逐步指南中，我們將引導您完成使用 Aspose.Note for Java 從 OneNote 文件中提取 Outlook 任務資訊的過程。
## 先決條件
在深入學習本教程之前，請確保您具備以下先決條件：
- Java 開發工具包 (JDK)：確保您的系統上安裝了 Java。
-  Aspose.Note for Java：從下列位置下載並安裝 Aspose.Note 函式庫：[下載頁面](https://releases.aspose.com/note/java/).
## 導入包
首先將必要的套件匯入到您的 Java 專案中。在 Java 檔案的開頭新增以下行：
```java
import java.io.IOException;
import java.util.List;
import com.aspose.note.Document;
import com.aspose.note.ITag;
import com.aspose.note.NoteTask;
import com.aspose.note.RichText;
```
## 第 1 步：設定您的項目
建立一個新的 Java 專案並將 Aspose.Note 庫包含在專案的依賴項中。確保您的專案結構井井有條，並且您有一個專門的文件目錄。
## 步驟 2：載入 OneNote 文檔
使用以下程式碼將 OneNote 文件載入到 Aspose.Note：
```java
String dataDir = "Your Document Directory";
Document doc = new Document(dataDir + "Sample1.one");
```
確保將「您的文件目錄」替換為 OneNote 文件的路徑。
## 步驟 3：檢索 RichText 節點
使用以下程式碼從文件中提取所有 RichText 節點：
```java
List<RichText> nodes = (List<RichText>) doc.getChildNodes(RichText.class);
```
## 第 4 步：迭代每個節點
循環遍歷每個 RichText 節點並確定它是否包含 NoteTask 標記：
```java
for (RichText richText : nodes) {
    for (ITag tag : richText.getTags()) {
        if (tag.getClass() == NoteTask.class) {
            //您處理 NoteTask 的程式碼
        }
    }
}
```
## 第 5 步：檢索任務屬性
檢索並列印 NoteTask 的各種屬性，例如完成時間、建立時間、截止日期、狀態和圖示：
```java
NoteTask noteTask = (NoteTask) tag;
System.out.println("Completed Time: " + noteTask.getCompletedTime());
System.out.println("Create Time: " + noteTask.getCreationTime());
System.out.println("Due Date: " + noteTask.getDueDate());
System.out.println("Status: " + noteTask.getStatus());
System.out.println("Icon: " + noteTask.getIcon());
```
對文件中的所有 NoteTask 節點重複此程序。
## 結論
恭喜！您已成功學習如何使用 Aspose.Note for Java 從 OneNote 文件中提取 Outlook 任務資訊。這個強大的函式庫為 Java 開發人員使用 Microsoft OneNote 檔案開啟了一個充滿可能性的世界。
## 常見問題解答
### Q：我可以將 Aspose.Note for Java 與其他 Java 框架一起使用嗎？
答：是的，Aspose.Note for Java 與各種 Java 框架相容，提供了整合的靈活性。
### Q：Aspose.Note for Java 是否有免費試用版？
答：是的，您可以探索 Aspose.Note for Java 的免費試用版[這裡](https://releases.aspose.com/).
### Q：如何獲得 Aspose.Note for Java 支援？
答：訪問[Aspose.Note 論壇](https://forum.aspose.com/c/note/28)尋求社區支持或探索高級支援選項。
### Q：在哪裡可以找到 Aspose.Note for Java 的詳細文件？
答：請參閱[Aspose.Note Java 文檔](https://reference.aspose.com/note/java/)以獲得深入的資訊。
### Q：如何取得 Aspose.Note for Java 的臨時授權？
答：取得臨時駕照[這裡](https://purchase.aspose.com/temporary-license/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
