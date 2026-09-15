---
date: 2026-03-29
description: 學習如何使用 Aspose.Note for Java 為 OneNote 文字設定語言。本分步指南將示範如何建立 OneNote 文件、變更文字語言，並有效儲存
  OneNote 檔案。
linktitle: Set Proofing Language for Text in OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: 如何在 OneNote 中設定文字語言 – Aspose.Note
url: /zh-hant/java/onenote-text-manipulation/set-proofing-language-for-text/
weight: 22
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何在 OneNote 中設定文字語言 – Aspose.Note

## 介紹
如果您需要在 OneNote 筆記本中為特定文字片段 **設定語言**，Aspose.Note for Java 讓這個過程變得簡單。在本教學中，您將學習如何建立 OneNote 文件、為單個字詞或片語變更文字語言，最後將 OneNote 檔案儲存為已套用正確校對語言的檔案。完成後，您將了解設定語言對拼寫檢查與在地化的重要性，並擁有可直接執行的程式碼範例。

## 快速解答
- **設定語言** 會影響什麼？它告訴 OneNote 使用哪個校對字典來進行拼寫檢查和文法校正。  
- **我可以在同一筆記中設定不同語言嗎？** 是的，您可以為每個文字段落指派語言。  
- **我需要 Aspose.Note 的授權嗎？** 免費試用版可用於測試；正式環境需購買商業授權。  
- **支援哪些 Java 版本？** Aspose.Note for Java 支援 Java 8 及以上版本。  
- **輸出檔案是 .one 格式嗎？** 是的，文件會儲存為 OneNote *.one* 檔案。

## 前置條件
在深入程式碼之前，請確保您已具備以下條件：

1. **Java 開發環境** – 已安裝並設定 JDK 8 或更高版本。  
2. **Aspose.Note for Java 函式庫** – 從 [download link](https://releases.aspose.com/note/java/) 下載並安裝函式庫。  
3. **文件目錄** – 在您的電腦上建立一個資料夾，用於儲存產生的 OneNote 檔案。

## 為何在 OneNote 中設定文字語言？
設定校對語言可確保拼寫檢查、文法建議與搜尋索引在多語言內容下正確運作。這在以下情況特別有用：

- **全球團隊** 在同一本筆記本上協作。  
- **在地化文件**，每個章節可能使用不同語言。  
- **資料驅動的應用程式**，可為全球使用者程式化產生筆記。

## 匯入套件
首先匯入必要的 Aspose.Note 類別與 Java 工具。

```java
import com.aspose.note.*;
import java.io.IOException;
import java.nio.file.Paths;
import java.util.Locale;
```

## 步驟 1：設定文件與頁面
建立一個全新的 OneNote 文件與用於放置內容的頁面。此步驟同時示範 **建立 OneNote 文件**。

```java
// The path to the documents directory.
String dataDir = "Your Document Directory";
Document document = new Document();
Page page = new Page();
```

## 步驟 2：建立大綱與大綱元素
大綱是筆記本內容的容器。此處我們建立結構，稍後將放入特定語言的文字。

```java
Outline outline = new Outline();
OutlineElement outlineElem = new OutlineElement();
```

## 步驟 3：加入具語言設定的豐富文字
現在我們透過將帶有特定 `Locale` 的 `TextStyle` 附加到每個文字段落，來 **變更文字語言**。此示範 **為文字設定語言**。

```java
RichText text = new RichText()
                        .append("United States", new TextStyle().setLanguage(Locale.forLanguageTag("en-US")))
                        .append(" Germany", new TextStyle().setLanguage(Locale.forLanguageTag("de-DE")))
                        .append(" China", new TextStyle().setLanguage(Locale.forLanguageTag("zh-CN")));
text.setParagraphStyle(ParagraphStyle.getDefault());
```

## 步驟 4：組織元素並儲存
組合大綱層級，將其附加至頁面，最後 **儲存 OneNote 檔案**，並套用語言設定。

```java
outlineElem.appendChildLast(text);
outline.appendChildLast(outlineElem);
page.appendChildLast(outline);
document.appendChildLast(page);
document.save(Paths.get(dataDir, "SetProofingLanguageForText.one").toString()); 
```

## 常見陷阱與技巧
- **Locale 格式** – 使用 IETF BCP‑47 標籤（例如 `en-US`、`de-DE`）。不正確的標籤會預設為文件的語言。  
- **檔案路徑** – 確保 `dataDir` 指向已存在的資料夾；否則 `document.save` 會拋出 `IOException`。  
- **專業提示：** 若需為整段文字設定語言，請將 `TextStyle` 套用至 `ParagraphStyle`，而非每次 `append` 呼叫。

## 結論
您剛剛學會如何使用 Aspose.Note for Java 為 OneNote 筆記本中的單個文字片段 **設定語言**。此功能讓您能以程式方式 **建立 OneNote 文件**、即時 **變更文字語言**，並 **儲存 OneNote 檔案**，附帶正確的校對中繼資料。

## 常見問答

**Q: 我可以為範例中未提及的其他語言設定校對語言嗎？**  
A: 當然可以！加入額外的 `append` 呼叫，使用所需的 `Locale.forLanguageTag("xx-XX")`。

**Q: Aspose.Note for Java 是否相容於最新的 Java 版本？**  
A: 是的，函式庫會定期更新以支援最新的 Java 發行版。

**Q: 如何在設定語言的過程中處理錯誤？**  
A: 將儲存操作包在 `try‑catch` 區塊中，以捕捉 `IOException` 或 `AsposeException`。

**Q: 我可以將此程式碼整合到 Web 應用程式中嗎？**  
A: 當然可以。只需將 Aspose.Note JAR 加入 Web 專案的 classpath，並確保伺服器對目標目錄具有寫入權限。

**Q: 我在哪裡可以找到 Aspose.Note for Java 的其他範例與文件？**  
A: 瀏覽 [documentation](https://reference.aspose.com/note/java/) 以取得完整的 API 列表與範例專案。

---

**最後更新：** 2026-03-29  
**測試環境：** Aspose.Note for Java 24.12  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}