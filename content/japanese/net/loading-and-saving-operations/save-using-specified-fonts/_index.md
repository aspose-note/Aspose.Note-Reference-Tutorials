---
title: Aspose.Note で指定したフォントを使用して保存する
linktitle: Aspose.Note で指定したフォントを使用して保存する
second_title: Aspose.Note .NET API
description: Aspose.Note for .NET で指定したフォントを使用してドキュメントを保存する方法を学びます。フォント設定を簡単にカスタマイズして、一貫したドキュメントの書式設定を実現します。
type: docs
weight: 28
url: /ja/net/loading-and-saving-operations/save-using-specified-fonts/
---
## 導入

このチュートリアルでは、Aspose.Note for .NET で指定したフォントを使用してドキュメントを保存する方法を学習します。これを達成するためのさまざまな方法を段階的に検討していきます。

## 前提条件

始める前に、以下のものがあることを確認してください。

1.  Aspose.Note for .NET: Aspose.Note for .NET がインストールされていることを確認してください。からダウンロードできます[ここ](https://releases.aspose.com/note/net/).

2. 開発環境: .NET 開発用にセットアップされた開発環境が必要です。

## 名前空間のインポート

まず、必要な名前空間をインポートしましょう。

```csharp
using System;
using System.IO;

using Aspose.Note.Fonts;
using Aspose.Note.Saving;

```

## ステップ 1: デフォルトのフォント名で保存する

このステップでは、指定したデフォルトのフォント名を使用してドキュメントを保存します。

```csharp
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontName()
{
    //ドキュメントディレクトリへのパス。
    string dataDir = "Your Document Directory";

    //ドキュメントを Aspose.Note にロードします。
    Document oneFile = new Document(Path.Combine(dataDir, "missing-font.one"));

    //指定したデフォルトのフォントを使用してドキュメントを PDF として保存します。
    dataDir = dataDir + "SaveUsingDocumentFontsSubsystemWithDefaultFontName_out.pdf";
    oneFile.Save(dataDir, new PdfSaveOptions()
                          {
                              FontsSubsystem = DocumentFontsSubsystem.UsingDefaultFont("Times New Roman")
                          });
}
```

## ステップ 2: デフォルトのフォントを使用してファイルから保存する

次に、ファイルから読み込んだデフォルトのフォントを使用してドキュメントを保存しましょう。

```csharp
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontFromFile()
{
    //ドキュメントディレクトリへのパス。
    string dataDir = "Your Document Directory";

    string fontFile = Path.Combine(dataDir, "geo_1.ttf");

    //ドキュメントを Aspose.Note にロードします。
    Document oneFile = new Document(Path.Combine(dataDir, "missing-font.one"));

    //ファイルから読み込まれたデフォルトのフォントを使用してドキュメントを PDF として保存します。
    dataDir = dataDir + "SaveUsingDocumentFontsSubsystemWithDefaultFontFromFile_out.pdf";
    oneFile.Save(dataDir, new PdfSaveOptions()
                          {
                              FontsSubsystem = DocumentFontsSubsystem.UsingDefaultFontFromFile(fontFile)
                          });
}
```

## ステップ 3: ストリームからデフォルトのフォントを使用して保存する

最後に、ストリームからロードされたデフォルトのフォントを使用してドキュメントを保存しましょう。

```csharp
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontFromStream()
{
    //ドキュメントディレクトリへのパス。
    string dataDir = "Your Document Directory";

    string fontFile = Path.Combine(dataDir, "geo_1.ttf");

    //ドキュメントを Aspose.Note にロードします。
    Document oneFile = new Document(Path.Combine(dataDir, "missing-font.one"));

    //ストリームから読み込まれたデフォルトのフォントを使用してドキュメントを PDF として保存します。
    dataDir = dataDir + "SaveUsingDocumentFontsSubsystemWithDefaultFontFromStream_out.pdf";

    using (var stream = File.Open(fontFile, FileMode.Open, FileAccess.Read, FileShare.Read))
    {
        oneFile.Save(dataDir, new PdfSaveOptions()
                              {
                                  FontsSubsystem = DocumentFontsSubsystem.UsingDefaultFontFromStream(stream)
                              });
    }
}
```

## 結論

このチュートリアルでは、Aspose.Note for .NET で指定したフォントを使用してドキュメントを保存する方法を検討しました。これらの手順に従うことで、要件に応じてフォント設定をカスタマイズし、ドキュメントが希望どおりにフォーマットされるようにすることができます。

## よくある質問

### Q1: Aspose.Note でドキュメントを保存するために任意のフォントを使用できますか?

A1: はい、ドキュメントを保存するために任意のフォントを指定できます。フォント ファイルがアクセス可能であり、正しくロードされていることを確認してください。

### Q2: Aspose.Note はさまざまなドキュメント形式と互換性がありますか?

A2: Aspose.Note は主に OneNote ドキュメントで動作しますが、PDF を含むさまざまな形式で保存するオプションも提供しています。

### Q3: ドキュメントを保存するときにフォントが見つからない場合はどうすればよいですか?

A3: Aspose.Note には、指定されたフォントが見つからない場合にデフォルトのフォントを使用するオプションが用意されており、一貫したドキュメントの書式設定が保証されます。

### Q4: Aspose.Note は出力ドキュメントへのフォント埋め込みをサポートしていますか?

A4: はい、Aspose.Note ではフォントを埋め込むことができ、ドキュメントの移植性と、さまざまなプラットフォーム間での一貫したレンダリングを確保できます。

### Q5: Aspose.Note に関するさらなるサポートはどこで受けられますか?

 A5: さらに支援や技術サポートが必要な場合は、次のサイトにアクセスしてください。[Aspose.Note フォーラム](https://forum.aspose.com/c/note/28).