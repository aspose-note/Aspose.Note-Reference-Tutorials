---
title: OneNote ドキュメントを作成し、Aspose.Note で HTML に保存する
linktitle: OneNote ドキュメントを作成し、Aspose.Note で HTML に保存する
second_title: Aspose.Note .NET API
description: Aspose.Note API を使用して、.NET アプリケーションで Microsoft OneNote ドキュメントを作成し、HTML 形式で保存する方法を学びます。ステップバイステップの例を含む包括的なチュートリアルに従ってください。
weight: 14
url: /ja/net/loading-and-saving-operations/create-onenote-doc-save-to-html/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote ドキュメントを作成し、Aspose.Note で HTML に保存する

## 導入

Aspose.Note for .NET は、開発者が .NET アプリケーションで Microsoft OneNote ドキュメントをプログラム的に操作できるようにする強力な API です。 Aspose.Note を使用すると、OneNote ファイルを簡単に作成、操作、変換できます。このチュートリアルでは、Aspose.Note for .NET API が提供するさまざまなオプションを使用して、OneNote ドキュメントを作成し、それを HTML 形式で保存する方法を説明します。

## 前提条件

始める前に、次の前提条件を満たしていることを確認してください。

- C# プログラミング言語の基本的な知識。
- Visual Studio がシステムにインストールされている。
- プロジェクトにインストールされている .NET API 用の Aspose.Note。からダウンロードできます[ここ](https://releases.aspose.com/note/net/).
- Microsoft OneNote ドキュメントの構造に精通していること。

## 名前空間のインポート

コーディング部分に入る前に、必要な名前空間をインポートしましょう。

```csharp
using System;
using System.Drawing;
using System.Globalization;
using System.IO;

using Aspose.Note.Saving;
using Aspose.Note.Saving.Html;

```

ここで、各例を複数の手順に分けて、Aspose.Note for .NET を使用して OneNote ドキュメントを作成し、HTML 形式で保存する方法を見てみましょう。

## ステップ 1: デフォルトのオプションを使用して OneNote ドキュメントを作成する

```csharp
public static void CreateAndSaveToHTMLUsingDefaultOptions()
{
    //OneNote ドキュメントを初期化する
    Document doc = new Document();
    Page page = doc.AppendChildLast(new Page());

    //ドキュメント内のすべてのテキストのデフォルトのスタイル。
    ParagraphStyle textStyle = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
    page.Title = new Title()
    {
        TitleText = new RichText() { Text = "Title text.", ParagraphStyle = textStyle },
        TitleDate = new RichText() { Text = new DateTime(2011, 11, 11).ToString("D", CultureInfo.InvariantCulture), ParagraphStyle = textStyle },
        TitleTime = new RichText() { Text = "12:34", ParagraphStyle = textStyle }
    };

    //HTML形式で保存
    string dataDir = "Your Document Directory";
    string outputPath = Path.Combine(dataDir, "CreateOneNoteDocAndSaveToHTML_out.html");
    doc.Save(outputPath);

    Console.WriteLine("\nOneNote document created successfully.\nFile saved at " + outputPath);
}
```

この手順では、新しい OneNote ドキュメントを初期化し、タイトル付きのページを追加し、既定のオプションを使用して HTML 形式で保存します。

## ステップ 2: 特定のページ範囲を作成して HTML に保存する

```csharp
public static void CreateAndSavePageRange()
{
    //OneNote ドキュメントを初期化する
    Document doc = new Document();
    Page page = doc.AppendChildLast(new Page());

    //ドキュメント内のすべてのテキストのデフォルトのスタイル。
    ParagraphStyle textStyle = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
    page.Title = new Title()
    {
        TitleText = new RichText() { Text = "Title text.", ParagraphStyle = textStyle },
        TitleDate = new RichText() { Text = new DateTime(2011, 11, 11).ToString("D", CultureInfo.InvariantCulture), ParagraphStyle = textStyle },
        TitleTime = new RichText() { Text = "12:34", ParagraphStyle = textStyle }
    };

    //HTML形式で保存
    string dataDir = "Your Document Directory";
    string outputPath = Path.Combine(dataDir, "CreateAndSavePageRange_out.html");
    doc.Save(outputPath, new HtmlSaveOptions { PageCount = 1, PageIndex = 0 });

    Console.WriteLine("\nOneNote document created successfully and saved as page range.\nFile saved at " + outputPath);
}
```

ここでは、ドキュメントを作成し、特定のページ範囲を HTML 形式で保存する方法を示します。

## ステップ 3: 埋め込みリソースを含む Memory Stream に HTML として保存する

```csharp
public static void SaveAsHTMLToMemoryStreamWithEmbeddedResources()
{
    //OneNote ドキュメントをロードする
    string dataDir = "Your Document Directory";
    var document = new Document(Path.Combine(dataDir, "Aspose.one"));

    //HTML 保存オプションを指定する
    var options = new HtmlSaveOptions()
    {
        ExportCss = ResourceExportType.ExportEmbedded,
        ExportFonts = ResourceExportType.ExportEmbedded,
        ExportImages = ResourceExportType.ExportEmbedded,
        FontFaceTypes = FontFaceType.Ttf
    };

    //ドキュメントをメモリ ストリームに保存する
    var memoryStream = new MemoryStream();
    document.Save(memoryStream, options);
}
```

この手順では、OneNote ドキュメントをメモリ ストリームに埋め込まれたリソース (CSS、フォント、画像) とともに HTML 形式で保存する方法を示します。

## ステップ 4: リソースを別のファイルに含めて HTML としてファイルに保存する

```csharp
public static void SaveAsHTMLToFileWithResourcesInSeparateFiles()
{
    //OneNote ドキュメントをロードする
    string dataDir = "Your Document Directory";
    var document = new Document(Path.Combine(dataDir, "Aspose.one"));

    //HTML 保存オプションを指定する
    var options = new HtmlSaveOptions()
    {
        ExportCss = ResourceExportType.ExportAsStream,
        ExportFonts = ResourceExportType.ExportAsStream,
        ExportImages = ResourceExportType.ExportAsStream,
        FontFaceTypes = FontFaceType.Ttf
    };

    //ドキュメントを HTML ファイルに保存し、リソースを別のファイルに保存します
    document.Save(Path.Combine(dataDir, "document_out.html"), options);
}
```

この手順では、OneNote ドキュメントを HTML 形式で保存し、すべてのリソース (CSS、フォント、画像) を別のファイルに保存します。

## ステップ 5: リソースを保存するためのコールバックを使用して、HTML として Memory Stream に保存する

```csharp
public static void SaveAsHTMLToMemoryStreamWithCallBacksToSaveResources()
{
    //保存コールバック構成を指定する
    var savingCallbacks = new UserSavingCallbacks()
    {
        RootFolder = "documentFolder",
        CssFolder = "css",
        KeepCssStreamOpened = true,
        ImagesFolder = "images",
        FontsFolder = "fonts"
    };

    //HTML 保存オプションを指定する
    var options = new HtmlSaveOptions
    {
        FontFaceTypes = FontFaceType.Ttf,
        CssSavingCallback = savingCallbacks,
        FontSavingCallback = savingCallbacks,
        ImageSavingCallback = savingCallbacks
    };

    //OneNote ドキュメントをロードする
    string dataDir = "Your Document Directory";
    var document = new Document(Path.Combine(dataDir, "Aspose.one"));

    //ユーザー定義のコールバックによって管理されるリソースを使用して、ドキュメントを HTML 形式で保存します。
    using (var stream = File.Create(Path.Combine(savingCallbacks.RootFolder, "document.html")))
    {
        document.Save(stream, options);
    }

    // CSS ストリームにデータを手動で追加する
    using (var writer = new StreamWriter(savingCallbacks.CssStream))
    {
        writer.WriteLine();
        writer.WriteLine("/* This line is appended to stream manually by user */");
    }
}
```

ここでは、ユーザー定義のコールバックによって管理されるリソースを使用して、OneNote ドキュメントを HTML 形式で保存する方法を示します。

## 結論

この記事では、Aspose.Note for .NET を使用して OneNote ドキュメントを操作し、HTML 形式で保存する方法を説明しました。ステップバイステップのガイドに従うことで、簡単に

 この機能を .NET アプリケーションに統合すると、OneNote ファイルを効率的に操作できるようになります。

## よくある質問

### Q1: 保存した HTML ファイルの外観をカスタマイズできますか?

A1: はい、変換プロセス中に生成された CSS スタイルシートを変更することで、外観をカスタマイズできます。

### Q2: Aspose.Note は HTML 以外の形式への変換をサポートしていますか?

A2: はい、Aspose.Note は PDF、画像、Microsoft Word ドキュメントなどのさまざまな形式への変換をサポートしています。

### Q3: Aspose.Note は .NET Core アプリケーションと互換性がありますか?

A3: はい、Aspose.Note は .NET Framework アプリケーションと .NET Core アプリケーションの両方と互換性があります。

### Q4: Aspose.Note を使用して OneNote ドキュメントからテキストや画像を抽出できますか?

A4: はい、Aspose.Note API を使用して、テキストや画像を抽出したり、その他のさまざまな操作を実行したりできます。

### Q5: Aspose.Note の機能をテストするために利用できる試用版はありますか?

 A5: はい、以下から無料試用版をダウンロードできます。[ここ](https://releases.aspose.com/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
