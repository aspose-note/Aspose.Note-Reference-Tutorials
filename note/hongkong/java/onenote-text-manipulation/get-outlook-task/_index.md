---
date: 2026-03-27
description: 學習如何使用 Aspose.Note for Java 從 OneNote Outlook 任務中提取任務詳情——為 Java 開發者提供快速且可靠的解決方案。
linktitle: Get Outlook Task in OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: 如何從 OneNote Outlook 任務中提取任務 – Aspose.Note
url: /zh-hant/java/onenote-text-manipulation/get-outlook-task/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何從 OneNote Outlook 任務中擷取 Task

## 介紹
如果你需要 **如何擷取任務** 資訊，且這些資訊位於 OneNote 頁面中——尤其是 Outlook 任務——Aspose.Note for Java 能讓這個過程變得輕鬆。在本實作教學中，我們將逐步說明如何從 OneNote 文件中取得任務屬性（狀態、到期日、建立時間等），並將它們輸出到主控台。完成後，你將擁有一段可在任何 Java 專案中使用的可重用程式碼片段，來處理 OneNote 檔案。

## 快速回答
- **本教學涵蓋什麼內容？** 從 OneNote 檔案中使用 Aspose.Note for Java 抽取 Outlook 任務細節。  
- **實作需要多久？** 基本設定約 10‑15 分鐘。  
- **前置條件？** Java JDK、Aspose.Note for Java 套件，以及包含任務的 OneNote 檔案。  
- **需要授權嗎？** 生產環境必須使用臨時或正式的 Aspose.Note 授權。  
- **可以在任何作業系統上執行嗎？** 可以——只要有 Java 執行環境，函式庫即平台無關。

## 什麼是從 OneNote 抽取任務？
抽取任務即是讀取 OneNote 為每個 Outlook 連結任務所儲存的 `NoteTask` 標籤。該標籤包含完成時間、到期日、狀態等中繼資料，你可以透過 Aspose.Note 的物件模型以程式方式存取。

## 為什麼要抽取任務資訊？
- **自動化：** 將任務同步至自家的任務管理系統。  
- **報表：** 產生跨多本筆記本的任務進度自訂報表。  
- **遷移：** 將任務從 OneNote 移轉至其他平台（例如 Microsoft Planner、Jira）。  

## 前置條件
在開始之前，請確保你已具備：

- **Java Development Kit (JDK)** – 任意近期版本（8 以上）。  
- **Aspose.Note for Java** – 從[下載頁面](https://releases.aspose.com/note/java/)取得。

## 匯入套件
在 Java 原始檔案中匯入必要的類別：

```java
import java.io.IOException;
import java.util.List;
import com.aspose.note.Document;
import com.aspose.note.ITag;
import com.aspose.note.NoteTask;
import com.aspose.note.RichText;
```

## 步驟 1：設定專案
建立新的 Java 專案（Maven、Gradle 或純 IDE），並將 Aspose.Note JAR 加入 classpath。將 OneNote 檔案放在專屬資料夾，例如 `data/`。

## 步驟 2：載入 OneNote 文件
載入你想檢查的 `.one` 檔案：

```java
String dataDir = "Your Document Directory";
Document doc = new Document(dataDir + "Sample1.one");
```

> **小技巧：** 若應用程式在不同環境執行，請使用絕對路徑或設定屬性。

## 步驟 3：取得 RichText 節點
所有文字元素皆以 `RichText` 節點表示。一次抓取全部：

```java
List<RichText> nodes = (List<RichText>) doc.getChildNodes(RichText.class);
```

## 步驟 4：遍歷每個節點
在每個 `RichText` 節點中搜尋 `NoteTask` 標籤：

```java
for (RichText richText : nodes) {
    for (ITag tag : richText.getTags()) {
        if (tag.getClass() == NoteTask.class) {
            // Your code to handle NoteTask
        }
    }
}
```

## 步驟 5：取得任務屬性
取得 `NoteTask` 實例後，即可讀取其屬性：

```java
NoteTask noteTask = (NoteTask) tag;
System.out.println("Completed Time: " + noteTask.getCompletedTime());
System.out.println("Create Time: " + noteTask.getCreationTime());
System.out.println("Due Date: " + noteTask.getDueDate());
System.out.println("Status: " + noteTask.getStatus());
System.out.println("Icon: " + noteTask.getIcon());
```

> **注意：** 必須對每個 `NoteTask` 節點執行迴圈，以抽取文件中所有任務的資訊。

## 常見問題與解決方案
| 問題 | 為何會發生 | 解決方式 |
|------|------------|----------|
| `NullPointerException` 發生於 `noteTask` | 標籤不是 `NoteTask`。 | 加入 null 檢查或確認 `tag instanceof NoteTask`。 |
| 日期未輸出 | OneNote 中的任務未設定到期日。 | 在列印前先檢查 `noteTask.getDueDate()` 是否為 `null`。 |
| 執行時找不到函式庫 | JAR 未在 classpath 中。 | 確認已在建置設定中加入 Aspose.Note JAR。 |

## 常見問答

**Q: 可以在其他 Java 框架中使用 Aspose.Note for Java 嗎？**  
A: 可以，Aspose.Note for Java 能順利整合至 Spring、Jakarta EE、Android 以及任何標準 Java 環境。

**Q: Aspose.Note for Java 有提供免費試用嗎？**  
A: 有，你可以在[此處](https://releases.aspose.com/)探索 Aspose.Note for Java 的免費試用。

**Q: 如何取得 Aspose.Note for Java 的支援？**  
A: 前往 [Aspose.Note 論壇](https://forum.aspose.com/c/note/28)取得社群協助，或購買高級支援方案。

**Q: 哪裡可以找到 Aspose.Note for Java 的詳細文件？**  
A: 請參考 [Aspose.Note for Java 文件](https://reference.aspose.com/note/java/) 以取得深入的 API 參考與範例。

**Q: 如何取得 Aspose.Note for Java 的臨時授權？**  
A: 前往[此處](https://purchase.aspose.com/temporary-license/)取得臨時授權。

## 結論
現在你已掌握 **如何從 OneNote 擷取任務** 的細節，並使用 Aspose.Note for Java 完成。此功能為自動化、報表與遷移等情境開啟了全新可能，過去手動且易出錯的流程得以自動化。歡迎自行擴充範例——將抽取的資料寫入資料庫、推送至外部服務，或與其他 OneNote 內容結合。

---

**最後更新：** 2026-03-27  
**測試環境：** Aspose.Note for Java 24.11（撰寫時的最新版本）  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}