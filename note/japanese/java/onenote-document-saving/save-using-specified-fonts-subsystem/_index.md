---
title: OneNote で指定したフォント サブシステムを使用して保存する
linktitle: OneNote で指定したフォント サブシステムを使用して保存する
second_title: Aspose.Note Java API
description: Aspose.Note を使用して Java の指定されたフォント サブシステムを使用して OneNote ドキュメントを保存する方法を学習します。プラットフォーム間で一貫したフォント表現を簡単に確保できます。
weight: 22
url: /ja/java/onenote-document-saving/save-using-specified-fonts-subsystem/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote で指定したフォント サブシステムを使用して保存する

## 導入

Aspose.Note for Java は、OneNote ドキュメントを操作するための堅牢な機能を提供します。このようなドキュメントを扱うときの一般的な要件の 1 つは、特にドキュメントを PDF などのさまざまな形式でエクスポートまたは保存する場合、フォントが適切に維持されていることを確認することです。このチュートリアルでは、フォント サブシステムを指定しながら OneNote ドキュメントを保存するプロセスを説明し、さまざまなプラットフォーム間で一貫した正確なテキスト表現を保証します。

## 前提条件

チュートリアルに入る前に、次の前提条件が設定されていることを確認してください。

### 1. Java 開発キット (JDK)

システムに Java Development Kit (JDK) がインストールされていることを確認してください。からダウンロードできます[ここ](https://www.oracle.com/java/technologies/javase-jdk15-downloads.html)まだ行っていない場合は。

### 2. Java ライブラリの Aspose.Note

Aspose.Note for Java ライブラリをダウンロードしてセットアップします。からダウンロードできます。[Webサイト](https://releases.aspose.com/note/java/).

## パッケージのインポート

必要なパッケージを Java プロジェクトにインポートしてください。

```java
import com.aspose.note.Document;
import com.aspose.note.PdfSaveOptions;
import com.aspose.note.fonts.DocumentFontsSubsystem;
import java.io.FileInputStream;
import java.io.IOException;
import java.io.InputStream;
import java.nio.file.Paths;
```

ここで、プロセスをよりよく理解するために、各例を複数のステップに分けてみましょう。

## ステップ 1: ドキュメント フォント サブシステムを使用してデフォルトのフォント名で保存する

この手順では、指定したデフォルトのフォント名を使用してドキュメントを PDF 形式で保存する方法を示します。

```java
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontName() throws IOException
{
    //ドキュメントを Aspose.Note にロードします。
    Document oneFile = new Document("missing-font.one");

    //デフォルトのフォントを指定します。
    PdfSaveOptions options = new PdfSaveOptions();
    options.setFontsSubsystem(DocumentFontsSubsystem.usingDefaultFont("Times New Roman"));

    //ドキュメントを PDF として保存します。
    oneFile.save("SaveUsingDocumentFontsSubsystemWithDefaultFontName_out.pdf", options);
}
```

このステップでは:
- OneNote ドキュメントは Aspose.Note を使用して読み込まれます。
- デフォルトのフォントは「Times New Roman」に指定されています。
- ドキュメントは、指定したフォントを使用して PDF 形式で保存されます。

## ステップ 2: ドキュメント フォント サブシステムを使用してファイルからのデフォルト フォントを保存する

このステップでは、ファイルからロードされたデフォルトのフォントを使用してドキュメントを PDF 形式で保存する方法を示します。

```java
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontFromFile() throws IOException
{
    //ドキュメントを Aspose.Note にロードします。
    Document oneFile = new Document("missing-font.one");

    //フォントファイルへのパスを指定します。
    String fontFile = "geo_1.ttf";

    //ファイルからデフォルトのフォントを指定します。
    PdfSaveOptions options = new PdfSaveOptions();
    options.setFontsSubsystem(DocumentFontsSubsystem.usingDefaultFontFromFile(fontFile));

    //ドキュメントを PDF として保存します。
    oneFile.save("SaveUsingDocumentFontsSubsystemWithDefaultFontFromFile_out.pdf", options);
}
```

このステップでは:
- フォントファイル「geo_1.ttf」が読み込まれます。
- デフォルトのフォントは読み込まれたフォントファイルから指定されます。
- ドキュメントは、指定したフォントを使用して PDF 形式で保存されます。

## ステップ 3: ストリームからのデフォルトのフォントを使用してドキュメント フォント サブシステムを使用して保存する

このステップでは、ストリームからロードされたデフォルトのフォントを使用してドキュメントを PDF 形式で保存する方法を示します。

```java
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontFromStream() throws IOException
{
    //ドキュメントを Aspose.Note にロードします。
    Document oneFile = new Document("missing-font.one");

    //フォントファイルへのパスを指定します。
    String fontFile = "geo_1.ttf";

    //フォント ファイルをストリームとして読み込みます。
    InputStream stream = new FileInputStream(fontFile);

    try
    {
        //ストリームからデフォルトのフォントを指定します。
        PdfSaveOptions options = new PdfSaveOptions();
        options.setFontsSubsystem(DocumentFontsSubsystem.usingDefaultFontFromStream(stream));

        //ドキュメントを PDF として保存します。
        oneFile.save("SaveUsingDocumentFontsSubsystemWithDefaultFontFromStream_out.pdf", options);
    }
    catch (Exception e)
    {
        stream.close();
    }
}
```

このステップでは:
- フォントファイル「geo_1.ttf」がストリームとして読み込まれます。
- デフォルトのフォントは、ロードされたストリームから指定されます。
- ドキュメントは、指定したフォントを使用して PDF 形式で保存されます。

## 結論

このチュートリアルでは、Aspose.Note を使用して Java で指定されたフォント サブシステムを使用して OneNote ドキュメントを保存する方法を学習しました。これらの手順に従うことで、ドキュメントをエクスポートまたは保存するときに、さまざまなプラットフォーム間で一貫したフォント表現を確保できます。

## よくある質問

### Q1: ドキュメントの異なる部分に異なるフォントを指定できますか?

A1: はい、Aspose.Note for Java を使用して、ドキュメントのさまざまな部分に異なるフォントを指定できます。

### Q2: Aspose.Note は OneNote のすべてのバージョンと互換性がありますか?

A2: Aspose.Note はさまざまなバージョンの OneNote をサポートし、さまざまな環境間での互換性を確保します。

### Q3: ドキュメントを保存するときにフォントが見つからない場合はどうすればよいですか?

A3: Aspose.Note には、ドキュメントの保存中に不足しているフォントを効果的に処理するためにデフォルトのフォントを指定するオプションが用意されています。

### Q4: サイズやスタイルなどのフォントのプロパティをカスタマイズできますか?

A4: はい、Aspose.Note for Java を使用して、サイズ、スタイル、色などのフォント プロパティをカスタマイズできます。

### Q5: Aspose.Note for Java の試用版はありますか?

A5: はい、Web サイトから Aspose.Note for Java の無料トライアルを入手できます。
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
