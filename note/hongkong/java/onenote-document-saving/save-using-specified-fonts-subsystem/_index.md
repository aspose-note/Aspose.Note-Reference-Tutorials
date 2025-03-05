---
title: 在 OneNote 中使用指定字型子系統儲存
linktitle: 在 OneNote 中使用指定字型子系統儲存
second_title: Aspose.Note Java API
description: 了解如何透過 Aspose.Note 在 Java 中使用指定字型子系統儲存 OneNote 文件。輕鬆確保跨平台的字體表示一致。
type: docs
weight: 22
url: /zh-hant/java/onenote-document-saving/save-using-specified-fonts-subsystem/
---
## 介紹

Aspose.Note for Java 提供了處理 OneNote 文件的強大功能。處理此類文件時的常見要求是確保正確維護字體，尤其是當文件要匯出或儲存為不同格式（如 PDF）時。本教學將引導您完成儲存 OneNote 文件的流程，同時指定字型子系統，確保在不同平台上一致且準確地表示文字。

## 先決條件

在我們深入學習本教學之前，請確保您已設定以下先決條件：

### 1.Java開發工具包（JDK）

確保您的系統上安裝了 Java 開發工具包 (JDK)。您可以從以下位置下載：[這裡](https://www.oracle.com/java/technologies/javase-jdk15-downloads.html)如果你還沒有。

### 2.Java 函式庫的 Aspose.Note

下載並設定 Aspose.Note for Java 函式庫。您可以從[網站](https://releases.aspose.com/note/java/).

## 導入包

確保在您的 Java 專案中匯入必要的套件：

```java
import com.aspose.note.Document;
import com.aspose.note.PdfSaveOptions;
import com.aspose.note.fonts.DocumentFontsSubsystem;
import java.io.FileInputStream;
import java.io.IOException;
import java.io.InputStream;
import java.nio.file.Paths;
```

現在讓我們將每個範例分解為多個步驟，以便更好地理解該過程。

## 步驟 1：使用文件字型子系統和預設字型名稱儲存

此步驟示範如何使用指定的預設字型名稱將文件儲存為 PDF 格式。

```java
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontName() throws IOException
{
    //將文件載入到 Aspose.Note 中。
    Document oneFile = new Document("missing-font.one");

    //指定預設字體。
    PdfSaveOptions options = new PdfSaveOptions();
    options.setFontsSubsystem(DocumentFontsSubsystem.usingDefaultFont("Times New Roman"));

    //將文件另存為 PDF。
    oneFile.save("SaveUsingDocumentFontsSubsystemWithDefaultFontName_out.pdf", options);
}
```

在這一步中：
- OneNote 文件是使用 Aspose.Note 載入的。
- 預設字型指定為“Times New Roman”。
- 文件以指定字型儲存為 PDF 格式。

## 步驟 2：使用文檔字體子系統和文件中的預設字體進行儲存

此步驟示範如何使用從文件載入的預設字型以 PDF 格式儲存文件。

```java
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontFromFile() throws IOException
{
    //將文件載入到 Aspose.Note 中。
    Document oneFile = new Document("missing-font.one");

    //指定字型檔案的路徑。
    String fontFile = "geo_1.ttf";

    //指定檔案中的預設字體。
    PdfSaveOptions options = new PdfSaveOptions();
    options.setFontsSubsystem(DocumentFontsSubsystem.usingDefaultFontFromFile(fontFile));

    //將文件另存為 PDF。
    oneFile.save("SaveUsingDocumentFontsSubsystemWithDefaultFontFromFile_out.pdf", options);
}
```

在這一步中：
- 載入字體檔案“geo_1.ttf”。
- 預設字體是從已載入的字體檔案中指定的。
- 文件以指定字型儲存為 PDF 格式。

## 步驟 3：使用文檔字體子系統和流程中的預設字體進行儲存

此步驟示範如何使用從流程載入的預設字體以 PDF 格式儲存文件。

```java
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontFromStream() throws IOException
{
    //將文件載入到 Aspose.Note 中。
    Document oneFile = new Document("missing-font.one");

    //指定字型檔案的路徑。
    String fontFile = "geo_1.ttf";

    //將字體檔案作為流加載。
    InputStream stream = new FileInputStream(fontFile);

    try
    {
        //指定流中的預設字體。
        PdfSaveOptions options = new PdfSaveOptions();
        options.setFontsSubsystem(DocumentFontsSubsystem.usingDefaultFontFromStream(stream));

        //將文件另存為 PDF。
        oneFile.save("SaveUsingDocumentFontsSubsystemWithDefaultFontFromStream_out.pdf", options);
    }
    catch (Exception e)
    {
        stream.close();
    }
}
```

在這一步中：
- 字體檔案“geo_1.ttf”作為流加載。
- 預設字體是從載入的流中指定的。
- 文件以指定字型儲存為 PDF 格式。

## 結論

在本教學中，我們學習如何使用 Aspose.Note 在 Java 中使用指定字型子系統儲存 OneNote 文件。透過執行這些步驟，您可以在匯出或儲存文件時確保跨不同平台的字體表示一致。

## 常見問題解答

### Q1：我可以為文件的不同部分指定不同的字體嗎？

A1：是的，您可以使用 Aspose.Note for Java 為文件的不同部分指定不同的字型。

### Q2：Aspose.Note 是否相容於所有版本的 OneNote？

A2：Aspose.Note支援各種版本的OneNote，確保不同環境下的相容性。

### Q3：儲存文件時字體遺失如何處理？

A3：Aspose.Note提供了指定預設字體的選項，以便在文件保存過程中有效處理遺失的字體。

### Q4：我可以自訂字體屬性，例如大小和樣式嗎？

A4：是的，您可以使用 Aspose.Note for Java 自訂字體屬性，例如大小、樣式和顏色。

### Q5：Aspose.Note for Java 有試用版嗎？

A5：是的，您可以從網站上獲得 Aspose.Note for Java 的免費試用版。