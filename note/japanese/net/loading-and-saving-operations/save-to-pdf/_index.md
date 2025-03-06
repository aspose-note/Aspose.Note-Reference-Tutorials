---
title: Aspose.Note で PDF に保存
linktitle: Aspose.Note で PDF に保存
second_title: Aspose.Note .NET API
description: Aspose.Note for .NET を使用して Microsoft OneNote ドキュメントを PDF 形式で保存する方法を学びます。レターおよび A4 ページ レイアウトのコード例を含むステップバイステップのチュートリアル。
weight: 26
url: /ja/net/loading-and-saving-operations/save-to-pdf/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Note で PDF に保存

## 導入

このチュートリアルでは、Aspose.Note for .NET を使用してドキュメントを PDF 形式で保存する方法を説明します。 Aspose.Note は、開発者が Microsoft OneNote ファイルをプログラムで操作できるようにする強力なライブラリです。前提条件を説明し、名前空間をインポートし、さまざまなページ レイアウトでドキュメントを PDF に保存するためのステップバイステップのガイドを提供します。

## 前提条件

始める前に、以下のものがあることを確認してください。

- Visual Studio がシステムにインストールされている。
-  Aspose.Note for .NET ライブラリがダウンロードされ、インストールされます。からダウンロードできます[ここ](https://releases.aspose.com/note/net/).
- C# プログラミング言語の基本的な知識。

## 名前空間のインポート

まず、必要な名前空間を C# コードにインポートしましょう。

```csharp
using System;
using System.IO;

using Aspose.Note.Saving;
```

前提条件を満たし、名前空間をインポートしたので、さまざまなページ レイアウトでドキュメントを PDF に保存してみましょう。

## ステップ 1: レターページ設定を使用して PDF に保存する


```csharp
public static void SaveToPdfUsingLetterPageSettings()
{
    //ドキュメントディレクトリへのパス。
    string dataDir = "Your Document Directory";

    //ドキュメントを Aspose.Note にロードします。
    Document oneFile = new Document(dataDir + "OneNote.one");

    var dst = Path.Combine(dataDir, "SaveToPdfUsingLetterPageSettings.pdf");

    //文書を保存します。
    oneFile.Save(dst, new PdfSaveOptions() { PageSettings = PageSettings.Letter });

    Console.WriteLine("\nOneNote document saved successfully.\nFile saved at " + dst);
}
```

### 説明：

- OneNote ドキュメントを Aspose.Note に読み込みます。
- 保存する PDF ファイルの保存先パスを定義します。
- 次を使用してドキュメントを PDF に保存します`PdfSaveOptions`と`PageSettings`に設定`Letter`.

## ステップ 2: 高さ制限のない A4 ページ設定を使用して PDF に保存する

```csharp
public static void SaveToPdfUsingA4PageSettingsWithoutHeightLimit()
{
    //ドキュメントディレクトリへのパス。
    string dataDir = "Your Document Directory";

    //ドキュメントを Aspose.Note にロードします。
    Document oneFile = new Document(dataDir + "OneNote.one");

    var dst = Path.Combine(dataDir, "SaveToPdfUsingA4PageSettingsWithoutHeightLimit.pdf");

    //文書を保存します。
    oneFile.Save(dst, new PdfSaveOptions() { PageSettings = PageSettings.A4NoHeightLimit });

    Console.WriteLine("\nOneNote document saved successfully.\nFile saved at " + dst);
}
```

### 説明：

- 前の手順と同様に、OneNote ドキュメントを Aspose.Note に読み込みます。
- 保存する PDF ファイルの保存先パスを定義します。
- 次を使用してドキュメントを PDF に保存します`PdfSaveOptions`と`PageSettings`に設定`A4NoHeightLimit`.

## 結論

このチュートリアルでは、Aspose.Note for .NET を使用してドキュメントを PDF 形式で保存する方法を学びました。レターと高さ制限のない A4 の 2 つの異なるページ レイアウトを取り上げました。 Aspose.Note を使用すると、開発者は OneNote ファイルをプログラムで簡単に操作できるため、ドキュメント管理タスクの柔軟性と効率が向上します。

## よくある質問

### Q1: Aspose.Note は複雑な OneNote ファイルを処理できますか?

A1: はい、Aspose.Note は、複雑な OneNote ファイルを効果的に処理するためのさまざまな機能をサポートしています。

### Q2: Aspose.Note は商用プロジェクトに適していますか?

 A2: もちろん、Aspose.Note は商用プロジェクトでも簡単に使用できます。ライセンスを購入できます[ここ](https://purchase.aspose.com/buy).

### Q3: Aspose.Note には無料トライアルがありますか?

A3: はい、無料トライアルを利用して Aspose.Note を探索できます。[ここ](https://releases.aspose.com/).

### Q4: Aspose.Note のドキュメントはどこで見つけられますか?

 A4: 詳細なドキュメントを見つけることができます。[ここ](https://reference.aspose.com/note/net/).

### Q5: さらにサポートが必要ですか?

 A5: お気軽に質問したり、Aspose.Note フォーラムでサポートを求めたりしてください。[ここ](https://forum.aspose.com/c/note/28).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
