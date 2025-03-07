---
title: Java を使用して OneNote にドキュメントを作成し画像を挿入する
linktitle: Java を使用して OneNote にドキュメントを作成し画像を挿入する
second_title: Aspose.Note Java API
description: Aspose.Note for Java を使用して OneNote ドキュメントを作成し、画像を挿入する方法を学びます。シームレスな統合のためのステップバイステップのチュートリアル。
weight: 12
url: /ja/java/onenote-hyperlinks-images/build-doc-insert-image/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java を使用して OneNote にドキュメントを作成し画像を挿入する

## 導入

このチュートリアルでは、Aspose.Note for Java を使用して OneNote ドキュメントを作成し、そこに画像を挿入する方法を説明します。 Aspose.Note は、開発者が Microsoft OneNote ファイルをプログラムで操作できるようにする強力な Java API です。プロセスをガイドするために、各ステップを詳しく説明します。

## 前提条件

始める前に、次の前提条件を満たしていることを確認してください。

1. Java Development Kit (JDK): システムに JDK がインストールされていることを確認してください。
2.  Aspose.Note for Java ライブラリ: Aspose.Note for Java ライブラリを次の場所からダウンロードしてインストールします。[Webサイト](https://releases.aspose.com/note/java/).
3. IDE (統合開発環境): コーディングには、IntelliJ IDEA や Eclipse などの Java サポートされている IDE を使用します。

## パッケージのインポート

まず、必要なパッケージを Java コードにインポートします。

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.HorizontalAlignment;
import com.aspose.note.Image;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.SaveFormat;
```

## ステップ 1: ドキュメントを設定する

まず、新しい OneNote ドキュメントを作成し、必要なオブジェクトを初期化します。

```java
String dataDir = "Your Document Directory";
Document doc = new Document();
Page page = new Page();
```

## ステップ 2: アウトラインを初期化する

ドキュメントのアウトラインを設定し、オフセット プロパティを指定します。

```java
Outline outline = new Outline();
outline.setVerticalOffset(0);
outline.setHorizontalOffset(0);
```

## ステップ 3: 画像を追加する

画像をロードし、その配置を指定します。

```java
Image image = new Image(null, dataDir + "Input.jpg");
image.setAlignment(HorizontalAlignment.Right);
```

## ステップ 4: アウトライン要素に画像を追加する

画像をアウトライン要素に添付します。

```java
OutlineElement outlineElem = new OutlineElement();
outlineElem.appendChildLast(image);
```

## ステップ 5: アウトライン ノードとページ ノードを追加する

アウトラインノードとページノードをドキュメントに追加します。

```java
outline.appendChildLast(outlineElem);
page.appendChildLast(outline);
doc.appendChildLast(page);
```

## ステップ 6: ドキュメントを保存する

最後に、OneNote ドキュメントを保存します。

```java
try {
    doc.save(dataDir + "NewOneNotedocument_out", SaveFormat.Pdf);
} catch (IOException e) {
    e.printStackTrace();
}
```

## 結論

おめでとう！ Aspose.Note for Java を使用して OneNote ドキュメントを作成し、そこに画像を挿入する方法を学習しました。これらの手順に従うことで、Java アプリケーションで OneNote ファイルを効率的に管理および操作できます。

## よくある質問

### Q1: Aspose.Note for Java のドキュメントはどこで見つけられますか?

 A1: ドキュメントにアクセスできます。[ここ](https://reference.aspose.com/note/java/).

### Q2: Aspose.Note for Java をダウンロードするにはどうすればよいですか?

 A2: Aspose.Note for Java は、次の場所からダウンロードできます。[ダウンロードページ](https://releases.aspose.com/note/java/).

### Q3: Aspose.Note for Java の無料トライアルはありますか?

 A3: はい、次のサイトから無料トライアルを利用できます。[Webサイト](https://releases.aspose.com/).

### Q4: Aspose.Note for Java のサポートはどこで入手できますか?

 A4: サポートについては、次のサイトにアクセスしてください。[Aspose.Note フォーラム](https://forum.aspose.com/c/note/28).

### Q5: Aspose.Note for Java の一時ライセンスを取得できますか?

 A5: はい、一時ライセンスをリクエストできます。[ここ](https://purchase.aspose.com/temporary-license/).

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
