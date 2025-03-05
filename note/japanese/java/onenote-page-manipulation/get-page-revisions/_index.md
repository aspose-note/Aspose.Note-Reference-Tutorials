---
title: OneNote でページ リビジョンを取得する - Aspose.Note
linktitle: OneNote でページ リビジョンを取得する - Aspose.Note
second_title: Aspose.Note Java API
description: Aspose.Note for Java を使用して OneNote でページ リビジョンを取得する方法を学習します。変更を効率的に追跡するには、ステップバイステップのガイドに従ってください。
type: docs
weight: 14
url: /ja/java/onenote-page-manipulation/get-page-revisions/
---
## 導入

OneNote はメモを整理および管理するための強力なツールですが、ページに加えられた変更や改訂を追跡する必要がある場合があります。 Aspose.Note for Java を使用すると、ページ リビジョンをプログラムで簡単に取得できます。このチュートリアルでは、Aspose.Note for Java を使用して OneNote でページ リビジョンを取得するプロセスを説明します。

## 前提条件

始める前に、次の前提条件が満たされていることを確認してください。

### 1. Java 開発キット (JDK)

システムに Java Development Kit (JDK) がインストールされていることを確認してください。 JDK は Oracle Web サイトからダウンロードしてインストールできます。

### 2. Java 用 Aspose.Note

Aspose.Note for Java を次の場所からダウンロードしてインストールします。[ダウンロードリンク](https://releases.aspose.com/note/java/).

### 3. OneNote ドキュメントのサンプル

サンプルの OneNote ドキュメントを準備します (`Sample1.one`) リビジョンを取得するページが含まれています。

## パッケージのインポート

まず、Aspose.Note for Java から必要なパッケージをインポートする必要があります。

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.LoadOptions;
import com.aspose.note.Page;
```

ここで、提供された例を複数のステップに分解してみましょう。

## ステップ 1: ドキュメント ディレクトリを設定する

OneNote ドキュメントが配置されるディレクトリ パスを定義します。

```java
String dataDir = "Your Document Directory";
```

## ステップ 2: OneNote ドキュメントをロードする

次を使用して OneNote ドキュメントを読み込みます`LoadOptions`履歴の読み込みを有効にします。

```java
LoadOptions loadOptions = new LoadOptions();
loadOptions.setLoadHistory(true);
Document document = new Document(dataDir + "Sample1.one", loadOptions);
```

## ステップ 3: 最初のページを取得する

ロードされたドキュメントから最初のページを取得します。

```java
Page firstPage = document.getFirstChild();
```

## ステップ 4: ページの改訂を繰り返す

各ページのリビジョンを反復処理し、最終変更時刻、作成時刻、タイトル、レベル、作成者などの関連情報を取得します。

```java
for (Page pageRevision : document.getPageHistory(firstPage)) {
    System.out.println("LastModifiedTime: " + pageRevision.getLastModifiedTime());
    System.out.println("CreationTime: " + pageRevision.getCreationTime());
    System.out.println("Title: " + pageRevision.getTitle());
    System.out.println("Level: " + pageRevision.getLevel());
    System.out.println("Author: " + pageRevision.getAuthor());
    System.out.println();
}
```

## 結論

このチュートリアルでは、Aspose.Note for Java を使用して OneNote でページ リビジョンを取得する方法を学習しました。これらの手順に従うことで、OneNote ページに加えられた変更をプログラムで効率的に追跡できます。

## よくある質問

### Q1: Aspose.Note for Java を使用してページ リビジョンを変更できますか?

A1: いいえ、Aspose.Note for Java は現在、ページ リビジョンの取得をサポートしていますが、変更はサポートしていません。

### Q2: Aspose.Note for Java は、OneNote ドキュメントのさまざまなバージョンと互換性がありますか?

A2: はい、Aspose.Note for Java はさまざまなバージョンの OneNote ドキュメントをサポートしているため、さまざまなファイル形式をシームレスに操作できます。

### Q3: Aspose.Note for Java を使用するにはライセンスが必要ですか?

A3: はい、商用プロジェクトで Aspose.Note for Java を使用するにはライセンスを購入する必要があります。ただし、評価目的で一時ライセンスを取得することもできます。

### Q4: Aspose.Note for Java の使用中に問題が発生した場合、サポートを求めることはできますか?

 A4: はい、Aspose.Note フォーラムからサポートを求めることができます。[ここ](https://forum.aspose.com/c/note/28).

### Q5: Aspose.Note for Java の無料トライアルはありますか?

 A5: はい、Aspose.Note for Java の無料トライアルにアクセスできます。[Webサイト](https://releases.aspose.com/).