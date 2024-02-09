---
title: Aspose.Note で画像の情報を取得する
linktitle: Aspose.Note で画像の情報を取得する
second_title: Aspose.Note .NET API
description: Aspose.Note for .NET を使用して Microsoft OneNote ファイルから画像情報を抽出する方法を学習します。効率的な開発のために、ステップバイステップのガイドに従ってください。
type: docs
weight: 13
url: /ja/net/images/get-info-of-images/
---
## 導入

.NET 開発の世界では、Aspose.Note は Microsoft OneNote ファイルを操作するための強力なツール セットを提供します。開発者がよく直面する一般的なタスクの 1 つは、メモに埋め込まれた画像から情報を抽出することです。寸法、ファイル名、変更時刻の取得のいずれであっても、Aspose.Note はこのプロセスを簡素化します。

## 前提条件

Aspose.Note を使用して画像情報を抽出する前に、次のものがあることを確認してください。

1. C# の基本知識: コード例を理解するには、C# プログラミング言語に精通していることが不可欠です。
2.  Aspose.Note for .NET がインストールされている: Aspose.Note ライブラリが開発環境にインストールされていることを確認してください。ダウンロードできます[ここ](https://releases.aspose.com/note/net/).

## 名前空間のインポート

始める前に、必要な名前空間をインポートしましょう。

```csharp
using System.IO;
using Aspose.Note;
using System.Collections.Generic;
using System;
```

## ステップ 1: ドキュメントをロードする

まず、対象の OneNote ドキュメントを Aspose.Note に読み込みます。

```csharp
//ドキュメントディレクトリへのパス。
string dataDir = "Your Document Directory";

//ドキュメントを Aspose.Note にロードします。
Document oneFile = new Document(dataDir + "Aspose.one");
```

交換する`"Your Document Directory"`OneNote ファイルへのパスを置き換えます。

## ステップ 2: 画像情報を取得する

次に、ドキュメントからすべての画像ノードを取得します。

```csharp
//すべての画像ノードを取得する
IList<Aspose.Note.Image> images = oneFile.GetChildNodes<Aspose.Note.Image>();
```

このコード スニペットは、読み込まれた OneNote ドキュメント内のすべての画像ノードを取得します。

## ステップ 3: 画像を反復処理する

次に、各画像ノードを反復処理してメタデータを抽出しましょう。

```csharp
foreach (Aspose.Note.Image image in images)
{
    Console.WriteLine("Width: {0}", image.Width);
    Console.WriteLine("Height: {0}", image.Height);
    Console.WriteLine("OriginalWidth: {0}", image.OriginalWidth);
    Console.WriteLine("OriginalHeight: {0}", image.OriginalHeight);
    Console.WriteLine("FileName: {0}", image.FileName);
    Console.WriteLine("LastModifiedTime: {0}", image.LastModifiedTime);
    Console.WriteLine();
}
```

このループは、幅、高さ、元の寸法、ファイル名、最終変更時刻など、各画像のさまざまな属性を出力します。

## 結論

Aspose.Note for .NET を使用すると、OneNote ドキュメントから画像情報を抽出することがシームレスなプロセスになります。このチュートリアルで概説されている手順に従うことで、開発者は埋め込み画像からメタデータを効率的に取得でき、堅牢なアプリケーションを構築できるようになります。

## よくある質問

### Q1: Aspose.Note は Microsoft OneNote のすべてのバージョンと互換性がありますか?

A1: Aspose.Note は、.one、.onepkg、.onetoc2 などのさまざまな形式の OneNote ファイルをサポートし、異なるバージョン間の互換性を確保します。

### Q2: Aspose.Note を使用して画像のプロパティを変更できますか?

A2: はい、Aspose.Note を使用すると、寸法、ファイル名、変更時間などの画像プロパティをプログラムで操作できます。

### Q3: Aspose.Note は .NET Core のサポートを提供しますか?

A3: はい、Aspose.Note は .NET Core のサポートを提供し、アプリケーションのクロスプラットフォーム開発を可能にします。

### Q4: Aspose.Note に利用できる無料トライアルはありますか?

A4: はい、Aspose.Note の無料トライアルにアクセスして、購入する前にその機能を調べることができます。

### Q5: Aspose.Note に関する追加のサポートや支援はどこで入手できますか?

 A5: お問い合わせやサポートが必要な場合は、Aspose.Note フォーラムにアクセスしてください。[ここ](https://forum.aspose.com/c/note/28).