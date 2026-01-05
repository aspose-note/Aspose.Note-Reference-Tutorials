---
date: 2026-01-05
description: 學習如何設定預設語系、載入 OneNote 文件、設定 Aspose 授權、將 OneNote 轉換為 PNG，並使用 Aspose.Note
  for Java 將 OneNote 儲存為影像。
linktitle: Working with Locales in OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: 在 OneNote 中設定預設語系 – Aspose.Note Java
url: /zh-hant/java/onenote-notebook-operations/working-with-locales/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 在 OneNote 中設定預設語系 – Aspose.Note Java

## 簡介

如果您在處理 OneNote 檔案時需要**設定預設語系**，Aspose.Note for Java 讓這變得輕而易舉。在本教學中，我們將逐步說明您需要的全部內容——從授權產品、載入 OneNote 文件、變更語系，到最後將檔案轉換為 PNG 圖像。完成後，您只需幾行程式碼即可自訂語言設定，產生符合特定語系的輸出。

## 快速解答
- **「設定預設語系」的作用是什麼？** 它定義了 Aspose.Note 在讀寫 OneNote 檔案時所使用的語言與區域格式。  
- **我需要授權嗎？** 需要——設定 Aspose 授權即可解鎖全部功能。  
- **需要哪個版本的 Java？** 支援任何 JDK 8 以上的版本。  
- **我可以將 OneNote 轉換為 PNG 嗎？** 當然可以；API 允許您將頁面儲存為圖像。  
- **此程序是執行緒安全的嗎？** 設定預設語系是全域性的，因此只需在應用程式啟動時設定一次。

## 什麼是 Aspose.Note 中的「設定預設語系」？

設定預設語系可告訴 Aspose.Note 在解析日期、數字與文字時應套用哪種語言與文化慣例。對於需要在不同使用者語系間保持一致格式的多區域應用程式而言，這是必不可少的。

## 為何在使用 OneNote 時要設定預設語系？

- **準確的資料呈現：** 日期與數字會正確顯示給目標受眾。  
- **一致的 UI 文字：** 從 OneNote 抽取的文字會遵守語系設定。  
- **簡化的轉換：** 當您之後將 OneNote 檔案轉換為 PNG 或其他格式時，視覺版面會符合預期的語系。

## 先決條件

- **Java 開發環：** 已安裝 JDK 並設定 `JAVA_HOME`。  
- **Aspose.Note 程式庫：** 從[下載連結](https://releases.aspose.com/note/java/)下載最新的 JAR。  
- **有效的 Aspose 授權檔案**（免費試用版亦可用於測試）。

## 匯入套件

在撰寫任何程式碼之前，先匯入提供所需功能的類別。

```java
import java.io.IOException;
import java.nio.file.Path;
import java.util.Locale;
import com.aspose.note.Document;
import com.aspose.note.License;
import com.aspose.note.LocaleOptions;
```

## 步驟 1：設定 Aspose 授權

```java
License license = new License();
license.setLicense("licenseFile");
```

設定 Aspose 授權可解鎖所有功能，包括語系處理與圖像轉換。

## 步驟 2：設定預設語系

```java
java.util.Locale.setDefault(new java.util.Locale("en", "rs"));
```

此處我們將**預設語系**設定為英文 (`en`) 並使用國家代碼 `rs`。請依目標區域調整語言與國家代碼。

## 步驟 3：載入 OneNote 文件

```java
String inputFile = "Sample1.one";
Path inputPath = Paths.get(inputFile);

Document oneFile = new Document(inputPath.toString());
```

此步驟會**載入 OneNote 文件**至 `Document` 物件，以便您操作其內容。

## 步驟 4：將 OneNote 轉換為 PNG（OneNote 檔案轉換）

```java
oneFile.save("sample.png");
```

`save` 方法執行**OneNote 檔案轉換**，將筆記本（或特定頁面）匯出為 PNG 圖像——實際上是**將 OneNote 轉換為 PNG**以及**將 OneNote 儲存為圖像**。

## 常見問題與技巧

- **找不到授權檔案：** 請確認 `licenseFile` 的路徑正確且檔案具備讀取權限。  
- **語系未套用：** 請在載入文件之前呼叫 `Locale.setDefault`。  
- **缺少圖像輸出：** 請確認 OneNote 檔案實際包含可渲染的頁面；空的筆記本會產生空白 PNG。

## 常見問與答

**Q: Aspose.Note 是否相容於不同版本的 Java？**  
A: 是的，Aspose.Note 支援 Java 8 及更高版本，確保在各種開發環境中具有廣泛相容性。

**Q: 我可以將 Aspose.Note 與其他 Java 函式庫整合嗎？**  
A: 當然可以。API 可與 Apache POI、Jackson、Spring 等流行函式庫無縫協作。

**Q: Aspose.Note 是否支援不同的檔案格式？**  
A: 雖然其核心聚焦於 OneNote 檔案，但該程式庫亦可匯出為 PNG、JPEG、PDF 以及其他影像格式。

**Q: 是否有 Aspose.Note 使用者社群論壇可供求助與分享知識？**  
A: 有，Aspose 社群論壇提供平台讓使用者與專家互動、提問並共同解決問題。請前往[支援論壇](https://forum.aspose.com/c/note/28)取得協助。

**Q: 我可以在購買前試用 Aspose.Note 嗎？**  
A: 當然可以，您可透過網站提供的免費試用版來體驗 Aspose.Note 的功能。

## 結論

透過上述步驟，您已學會如何使用 Aspose.Note for Java **設定預設語系**、**載入 OneNote 文件**、**設定 Aspose 授權**，以及 **將 OneNote 轉換為 PNG**。此工作流程讓您能產生具語系感知的報告與圖像，滿足全球受眾的需求。

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**最後更新：** 2026-01-05  
**測試環境：** Aspose.Note 24.11 for Java  
**作者：** Aspose