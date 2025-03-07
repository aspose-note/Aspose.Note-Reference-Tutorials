---
title: Aspose.Note でページ タイトルを含むドキュメントを作成する
linktitle: Aspose.Note でページ タイトルを含むドキュメントを作成する
second_title: Aspose.Note .NET API
description: Aspose.Note for .NET を使用して、タイトル付きのページを持つドキュメントを作成する方法を学びます。シームレスな統合については、ステップバイステップのガイドに従ってください。
weight: 13
url: /ja/net/loading-and-saving-operations/create-doc-with-page-title/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Note でページ タイトルを含むドキュメントを作成する

## 導入

このチュートリアルでは、Aspose.Note for .NET を使用してタイトル付きページを含むドキュメントを作成するプロセスを説明します。 Aspose.Note は、開発者が Microsoft OneNote ファイルをプログラムで操作できるようにする強力な API です。

## 前提条件

始める前に、次の前提条件がインストールおよび設定されていることを確認してください。

### Visual Studio のインストール

1. Visual Studio をダウンロードする: まだ行っていない場合は、Microsoft Web サイトから Visual Studio をダウンロードしてインストールします。

2. .NET 開発ワークロードをインストールする: インストール プロセス中に、必ず「.NET デスクトップ開発」ワークロードを選択して、.NET 開発に必要なコンポーネントがすべて揃っていることを確認してください。

3. 新しいプロジェクトを作成する: Visual Studio を開き、新しいプロジェクト (コンソール アプリケーションまたはその他の任意のタイプ) を作成します。

### Aspose.Note のインストール

1. Aspose.Note を入手: Aspose.Note for .NET ライブラリを次の場所からダウンロードします。[Webサイト](https://releases.aspose.com/note/net/).

2. NuGet 経由で Aspose.Note をインストールする: または、Visual Studio の NuGet パッケージ マネージャー経由で Aspose.Note for .NET をインストールすることもできます。 「Aspose.Note」を検索して最新バージョンをインストールするだけです。

## 名前空間のインポート

まず、プロジェクトで Aspose.Note を使用するために必要な名前空間をインポートする必要があります。

```csharp
using System.IO;
using Aspose.Note;
using Aspose.Note.Saving;
using System;
using System.Drawing;
using System.Globalization;
```

ここで、ページ タイトルを含むドキュメントを作成するプロセスを複数のステップに分けてみましょう。

## ステップ 1: ドキュメント オブジェクトを作成する

```csharp
//Documentクラスのオブジェクトを作成する
Document doc = new Aspose.Note.Document();
```

## ステップ 2: ページ クラス オブジェクトを初期化する

```csharp
// Pageクラスオブジェクトの初期化
Aspose.Note.Page page = new Aspose.Note.Page(doc);
```

## ステップ 3: テキストのデフォルトのスタイルを設定する

```csharp
//ドキュメント内のすべてのテキストのデフォルトのスタイル。
ParagraphStyle textStyle = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
```

## ステップ 4: ページ タイトルのプロパティを設定する

```csharp
//ページタイトルのプロパティを設定する
page.Title = new Title(doc)
{
    TitleText = new RichText(doc) { Text = "Title text.", ParagraphStyle = textStyle },
    TitleDate = new RichText(doc) { Text = new DateTime(2011, 11, 11).ToString("D", CultureInfo.InvariantCulture), ParagraphStyle = textStyle },
    TitleTime = new RichText(doc) { Text = "12:34", ParagraphStyle = textStyle }
};
```

## ステップ 5: ドキュメントにページ ノードを追加する

```csharp
//ドキュメントにページノードを追加
doc.AppendChildLast(page);
```

## ステップ 6: OneNote ドキュメントを保存する

```csharp
// OneNote ドキュメントを保存する
string dataDir = "Your Document Directory";
dataDir = dataDir + "CreateDocWithPageTitle_out.one";
doc.Save(dataDir);
```

## 結論

おめでとう！ Aspose.Note for .NET を使用して、タイトル付きのページを持つドキュメントが正常に作成されました。このチュートリアルでは、OneNote ファイルをプログラムで管理するために Aspose.Note を .NET アプリケーションに統合するのに役立つステップバイステップ ガイドを提供しました。

## よくある質問

### Q1: タイトルのテキストスタイルをカスタマイズできますか?

A1: はい、要件に応じてタイトル テキストのフォントの色、フォント名、フォント サイズをカスタマイズできます。

### Q2: Aspose.Note は .NET Core と互換性がありますか?

A2: はい、Aspose.Note は .NET Core をサポートしているため、クロスプラットフォーム アプリケーションを開発できます。

### Q3: ドキュメントに画像や添付ファイルを追加できますか?

A3：もちろんです！ Aspose.Note は、画像、添付ファイル、その他の要素を OneNote ドキュメントにシームレスに追加するための API を提供します。

### Q4: Aspose.Note は既存の OneNote ファイルの読み取りをサポートしていますか?

A4: はい、Aspose.Note を使用すると、既存の OneNote ファイルを簡単に読み取り、変更、操作できます。

### Q5: 問題が発生した場合、どこでサポートを受けられますか?

 A5: サポートと支援は次のサイトで見つけることができます。[Aspose.Note フォーラム](https://forum.aspose.com/c/note/28)では、専門家やコミュニティのメンバーが質問に答えてくれます。
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
