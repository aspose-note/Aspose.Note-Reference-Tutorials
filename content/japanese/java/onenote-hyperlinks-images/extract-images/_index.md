---
title: Java を使用して OneNote ドキュメントから画像を抽出する
linktitle: Java を使用して OneNote ドキュメントから画像を抽出する
second_title: Aspose.Note Java API
description: Java と Aspose.Note ライブラリを使用して OneNote ドキュメントから画像を抽出する方法を学びます。シームレスな画像抽出については、ステップバイステップのガイドに従ってください。
type: docs
weight: 14
url: /ja/java/onenote-hyperlinks-images/extract-images/
---
## 導入

このチュートリアルでは、Aspose.Note ライブラリを利用して Java を使用して OneNote ドキュメントから画像を抽出するプロセスを説明します。

## 前提条件

始める前に、次のものが揃っていることを確認してください。

1.  Java 開発キット (JDK): システムに Java がインストールされていることを確認してください。からダウンロードしてインストールできます。[Webサイト](https://www.oracle.com/java/technologies/javase-jdk15-downloads.html).

2.  Aspose.Note ライブラリ: Aspose.Note ライブラリをダウンロードして、Java プロジェクトに組み込みます。から入手できます。[ダウンロードリンク](https://releases.aspose.com/note/java/).

## パッケージのインポート

まず、必要なパッケージをインポートします。

```java
import java.io.IOException;
import java.nio.file.Files;
import java.nio.file.Paths;
import java.util.List;
import com.aspose.note.Document;
import com.aspose.note.Image;
```

## ステップ 1: ドキュメントをロードする

まず、Aspose.Note を使用して OneNote ドキュメントを読み込みます。

```java
String dataDir = "Your Document Directory";
Document doc = new Document(dataDir + "Sample1.one");
```

## ステップ 2: すべての画像を取得する

次に、ドキュメントからすべての画像を取得します。

```java
List<Image> list = doc.getChildNodes(Image.class);
System.out.printf("Total Images: %s\n\n", list.size());
```

## ステップ 3: 画像を抽出する

画像のリストを繰り返し処理し、各画像をファイルに保存します。

```java
for (int i = 0; i < list.size(); i++) {
    Image image = list.get(i);
    String outputFile = "ExtractImages_out" + i + "_" + image.getFileName();
    byte[] buffer = image.getBytes();
    Files.write(Paths.get(dataDir + outputFile), buffer);
    System.out.printf("File saved: %s\n", dataDir);
}
```

## 結論

Java を使用して OneNote ドキュメントから画像を抽出することは、Aspose.Note ライブラリを使用してシームレスに実現できます。このチュートリアルで概説されている手順に従うことで、ドキュメントから画像を簡単に取得して、さらなる処理や分析を行うことができます。

## よくある質問

### Q1: パスワードで保護された OneNote ドキュメントから画像を抽出できますか?

A1: はい、Aspose.Note はパスワードで保護されたドキュメントからの画像の抽出もサポートしています。

### Q2: Aspose.Note は Java のさまざまなバージョンと互換性がありますか?

A2: Aspose.Note はさまざまなバージョンの Java と互換性があり、開発者にとって柔軟性が確保されています。

### Q3: 1 回の実行で複数の OneNote ドキュメントから画像を抽出できますか?

A3: もちろん、Aspose.Note を使用して複数のドキュメントを反復処理し、それぞれのドキュメントから画像を抽出することができます。

### Q4: OneNote ドキュメントのサイズ制限はありますか?

A4: Aspose.Note はさまざまなサイズのドキュメントを効率的に処理し、画像抽出のドキュメント サイズに制限がありません。

### Q5: Aspose.Note は、画像以外の他の種類のコンテンツの抽出をサポートしていますか?

A5: はい。Aspose.Note では、画像のほかに、OneNote ドキュメントからテキスト、添付ファイル、その他のコンテンツ タイプを抽出できます。