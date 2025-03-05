---
title: OneNote のページに関する情報を取得する - Aspose.Note
linktitle: OneNote のページに関する情報を取得する - Aspose.Note
second_title: Aspose.Note Java API
description: OneNote ドキュメント内のページの秘密を明らかにしましょう。 Aspose.Note を使用して、リビジョン、作成時刻などを抽出します。ステップバイステップのガイドとコードが含まれています。 #OneNote #Java #Aspose
type: docs
weight: 12
url: /ja/java/onenote-page-manipulation/get-information-about-pages/
---
## 導入

このチュートリアルでは、Aspose.Note for Java を使用して OneNote のページに関する情報を抽出するプロセスを説明します。 Aspose.Note は、Microsoft OneNote ドキュメントをプログラムで操作できるようにする強力な API です。ページのリビジョン、作成時刻、タイトル、作成者にアクセスする必要がある場合でも、Aspose.Note の直感的なインターフェイスによりタスクが簡素化されます。

## 前提条件

始める前に、以下のものがあることを確認してください。

1. Java Development Kit (JDK): システムに JDK がインストールされていることを確認してください。
2.  Aspose.Note for Java: Aspose.Note for Java ライブラリをダウンロードしてインストールします。から入手できます。[Webサイト](https://purchase.aspose.com/buy).
3. サンプル OneNote ドキュメント: 情報の取得に使用するサンプル OneNote ドキュメントを準備します。

## パッケージのインポート

まず、Java プロジェクトで Aspose.Note を操作するために必要なパッケージをインポートする必要があります。

```java
import java.io.IOException;
import java.util.List;

import com.aspose.note.Document;
import com.aspose.note.LoadOptions;
import com.aspose.note.Page;
```

## ステップ 1: OneNote ドキュメントをロードする

まず、Aspose.Note を使用して OneNote ドキュメントを読み込みます。

```java
String dataDir = "Your Document Directory";
//ドキュメントを Aspose.Note にロードします。
LoadOptions options = new LoadOptions();
Document doc = new Document(dataDir + "Sample1.one", options);
```

交換する`"Your Document Directory"`OneNote ドキュメントへのパスを置き換えます。

## ステップ 2: ページ情報を取得する

次に、OneNote ドキュメント内のページに関する情報を取得します。

```java
//ページのリビジョンを取得する
List<Page> pages = doc.getChildNodes(Page.class);

//ページのリストを横断する
for (Page pageRevision : pages) {
    System.out.println("LastModifiedTime: " + pageRevision.getLastModifiedTime());
    System.out.println("CreationTime: " + pageRevision.getCreationTime());
    System.out.println("Title: " + pageRevision.getTitle());
    System.out.println("Level: " + pageRevision.getLevel());
    System.out.println("Author: " + pageRevision.getAuthor());
}
```

このコード スニペットはドキュメント内の各ページを反復処理し、各ページの最終変更時刻、作成時刻、タイトル、レベル、作成者などの情報を出力します。

## 結論

このチュートリアルでは、Aspose.Note for Java を使用して OneNote のページに関する情報を取得する方法を学習しました。上記の手順に従うことで、Aspose.Note を Java アプリケーションにシームレスに統合して、OneNote ドキュメントから貴重なデータを抽出できます。

## よくある質問

### Q1: Aspose.Note for Java を使用して OneNote ドキュメントを編集できますか?

A1: はい、Aspose.Note は、OneNote ドキュメントをプログラムで編集および操作するための包括的な機能セットを提供します。

### Q2: Aspose.Note は OneNote のすべてのバージョンと互換性がありますか?

A2: Aspose.Note はさまざまなバージョンの OneNote をサポートし、さまざまな環境間での互換性を確保します。

### Q3: Aspose.Note を使用して OneNote ドキュメントを他の形式に変換できますか?

A3: もちろん、Aspose.Note を使用すると、OneNote ドキュメントを PDF、HTML、画像などの形式に簡単に変換できます。

### Q4: Aspose.Note は開発者に技術サポートを提供しますか?

A4: はい、Aspose は、Aspose.Note の使用中に発生した問題について開発者を支援する専用のテクニカル サポートを提供しています。

### Q5: Aspose.Note for Java の試用版はありますか?

 A5: はい、Aspose.Note for Java の無料試用版を次のサイトからダウンロードできます。[ここ](https://releases.aspose.com/).