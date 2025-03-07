---
title: Aspose.Note ドキュメントのページ リビジョンを調べる
linktitle: Aspose.Note ドキュメントのページ リビジョンを調べる
second_title: Aspose.Note .NET API
description: .NET Framework を使用して Aspose.Note ドキュメントのページ リビジョンを調査する方法を、ステップバイステップのガイダンスとともに学びます。
weight: 14
url: /ja/net/note-manipulation/page-revisions-exploration/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Note ドキュメントのページ リビジョンを調べる

## 導入

このチュートリアルでは、.NET Framework を使用した Aspose.Note ドキュメントのページ リビジョンの探索について詳しく説明します。 Aspose.Note は、開発者が Microsoft OneNote ファイルをプログラムで操作できるようにする強力なライブラリであり、これらのファイルからデータを操作および抽出するためのさまざまな機能を提供します。

## 前提条件

始める前に、次の前提条件が設定されていることを確認してください。

### 1. Aspose.Note for .NET をダウンロードしてインストールします

訪問[ダウンロードページ](https://releases.aspose.com/note/net/)Aspose.Note for .NET ライブラリをダウンロードします。提供されるインストール手順に従って、開発環境にライブラリをセットアップします。

### 2. 必要な名前空間をロードする

Aspose.Note の機能にシームレスにアクセスするには、.NET プロジェクトに必要な名前空間を必ずインポートしてください。

```csharp
using System.IO;
using Aspose.Note;
using System;
using System.Collections.Generic;
```

ここで、ページ リビジョンを調査するプロセスを段階的な手順に分けて説明します。

## ステップ 1: ドキュメントをロードする

まず、Aspose.Note ドキュメントをロードし、ドキュメント履歴のロードを有効にする必要があります。

```csharp
string dataDir = "Your Document Directory";
Document document = new Document(dataDir + "Aspose.one", new LoadOptions { LoadHistory = true });
```

## ステップ 2: ページのリビジョンを取得する

ドキュメントがロードされると、特定のページのリビジョンを取得できます。この例では、最初のページのリビジョンを取得します。

```csharp
Page firstPage = document.FirstChild;
foreach (Page pageRevision in document.GetPageHistory(firstPage))
{
    /*Use pageRevision like a regular page.*/
    Console.WriteLine("LastModifiedTime: {0}", pageRevision.LastModifiedTime);
    Console.WriteLine("CreationTime: {0}", pageRevision.CreationTime);
    Console.WriteLine("Title: {0}", pageRevision.Title);
    Console.WriteLine("Level: {0}", pageRevision.Level);
    Console.WriteLine("Author: {0}", pageRevision.Author);
    Console.WriteLine();
}
```

## ステップ 3: リビジョンを反復処理する

ループ内で、ページの各リビジョンを反復処理し、最終変更時刻、作成時刻、タイトル、レベル、作成者などのプロパティにアクセスします。

## 結論

.NET を使用して Aspose.Note ドキュメントのページ リビジョンを調査するのは簡単なプロセスです。このチュートリアルで概説されている手順に従うことで、OneNote ファイルの改訂履歴をプログラム的に効果的に取得して分析できます。

## よくある質問

### Q1: Aspose.Note for .NET を使用して新しい OneNote ドキュメントを作成できますか?

A1: はい、Aspose.Note for .NET を使用すると、OneNote ドキュメントをプログラムで作成、編集、操作できます。

### Q2: Aspose.Note は、あらゆる種類の OneNote ファイルの読み込み履歴をサポートしていますか?

A2: Aspose.Note は、.one と .onepkg の両方のファイル形式の読み込み履歴をサポートしています。

### Q3: Aspose.Note for .NET に利用できる無料トライアルはありますか?

A3: はい、Aspose.Note for .NET の無料トライアル版を次のサイトからダウンロードできます。[ここ](https://releases.aspose.com/).

### Q4: Aspose.Note for .NET の一時ライセンスを取得するにはどうすればよいですか?

 A4: 一時ライセンスは以下からリクエストできます。[このリンク](https://purchase.aspose.com/temporary-license/).

### Q5: Aspose.Note for .NET のサポートはどこで見つけられますか?

 A5: サポートとリソースは次のサイトで見つけることができます。[Aspose.Note フォーラム](https://forum.aspose.com/c/note/28).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
