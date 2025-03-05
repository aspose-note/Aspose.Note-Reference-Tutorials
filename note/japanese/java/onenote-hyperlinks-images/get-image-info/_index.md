---
title: Java を使用して OneNote から画像情報を取得する
linktitle: Java を使用して OneNote から画像情報を取得する
second_title: Aspose.Note Java API
description: Java で OneNote ドキュメントから画像情報を抽出します。画像のサイズ、ファイル名などを取得します。簡単な手順とコード例が含まれています。 #OneNote #Java #Aspose
type: docs
weight: 15
url: /ja/java/onenote-hyperlinks-images/get-image-info/
---
## 導入

Java 開発の分野では、さまざまなドキュメント形式から情報を抽出するのが一般的なタスクです。メモを取るための人気のあるプラットフォームである OneNote には、多くの場合、テキストとともに画像が含まれています。 Java を使用して OneNote ファイルからプログラムで画像情報を取得すると、ドキュメント処理ワークフローを合理化できます。このチュートリアルでは、Aspose.Note for Java を使用して OneNote ドキュメントから画像の詳細を抽出する方法を詳しく説明します。

## 前提条件

実装に入る前に、次の前提条件が満たされていることを確認してください。

### 1. Java 開発キット (JDK)

システムに Java Development Kit (JDK) がインストールされていることを確認してください。最新の JDK を次の場所からダウンロードしてインストールできます。[オラクルのWebサイト](https://www.oracle.com/java/technologies/javase-jdk15-downloads.html).

### 2. Java ライブラリの Aspose.Note

 Aspose.Note for Java ライブラリをダウンロードしてプロジェクトに組み込みます。ライブラリは次から入手できます。[ダウンロードページ](https://releases.aspose.com/note/java/).

### 3. OneNote ドキュメント

画像を含むサンプル OneNote ドキュメントを準備します。このドキュメントは、プログラムによって画像情報を抽出するために使用されます。

## パッケージのインポート

まず、Aspose.Note for Java から必要なパッケージをインポートします。

```java
import java.io.IOException;
import java.util.List;
import com.aspose.note.Document;
import com.aspose.note.Image;
```

上記のコードを段階的な手順に分解してみましょう。

## ステップ 1: ドキュメント ディレクトリを設定する

```java
String dataDir = "Your Document Directory";
```

交換する`"Your Document Directory"`OneNote ドキュメントへのパスを置き換えます。

## ステップ 2: ドキュメントをロードする

```java
Document doc = new Document(dataDir + "Sample1.one");
```

Aspose.Note for Java ライブラリを使用して OneNote ドキュメントを読み込みます。ドキュメントへの正しいパスを指定していることを確認してください。

## ステップ 3: すべての画像を取得する

```java
List<Image> list = doc.getChildNodes(Image.class);
```

ロードされた OneNote ドキュメントからすべての画像を取得します。

## ステップ 4: 印刷総画像数

```java
System.out.printf("Total Images: %s\n\n", list.size());
```

文書内で見つかった画像の総数を印刷します。

## ステップ 5: 画像情報を走査して印刷する

```java
for (Image image : list) {
    System.out.println("Width: " + image.getWidth());
    System.out.println("Height: " + image.getHeight());
    System.out.println("OriginalWidth: " + image.getOriginalWidth());
    System.out.println("OriginalHeight: " + image.getOriginalHeight());
    System.out.println("FileName: " + image.getFileName());
    System.out.println("LastModifiedTime: " + image.getLastModifiedTime());
    System.out.println();
}
```

画像のリストを繰り返し処理し、各画像の幅、高さ、元の寸法、ファイル名、最終変更時刻などの詳細を印刷します。

## 結論

このチュートリアルで概説されている手順に従うと、Aspose.Note for Java ライブラリの支援を受けて、Java を使用して OneNote ドキュメントから画像情報を効果的に取得できます。この機能をアプリケーションに統合すると、ドキュメント処理に関連するタスクが自動化され、効率と生産性が向上します。

## よくある質問

### Q1: Aspose.Note for Java は、OneNote 以外の他のドキュメント形式を処理できますか?

A1: はい、Aspose.Note for Java は、OneNote、PDF、Microsoft Word などのさまざまなドキュメント形式をサポートしています。

### Q2: Aspose.Note for Java は個人使用と商用使用の両方に適していますか?

A2: はい、Aspose.Note for Java は個人目的でも商用目的でも利用できます。

### Q3: Aspose.Note for Java はテクニカル サポートを提供していますか?

 A3: はい、テクニカル サポートは、次の Aspose フォーラムを通じて利用できます。[ここ](https://forum.aspose.com/c/note/28).

### Q4: 購入する前に、Aspose.Note for Java を試してみることはできますか?

 A4: はい、Java 用 Aspose.Note の無料試用版を次のサイトから試すことができます。[Aspose.Note for Java](https://releases.aspose.com/note/java/).

### Q5: Aspose.Note for Java の一時ライセンスを取得するにはどうすればよいですか?
 
 A5: 一時ライセンスは以下から取得できます。[仮免許/](https://purchase.aspose.com/temporary-license/).