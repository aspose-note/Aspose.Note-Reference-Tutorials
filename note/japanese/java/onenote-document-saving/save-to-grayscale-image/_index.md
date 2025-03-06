---
title: OneNote でグレースケール画像に保存 - Aspose.Note
linktitle: OneNote でグレースケール画像に保存 - Aspose.Note
second_title: Aspose.Note Java API
description: Aspose.Note for Java を使用して、OneNote でドキュメントをグレースケール イメージとして保存する方法を学習します。 Microsoft OneNote ドキュメントをプログラムで簡単に操作します。
weight: 17
url: /ja/java/onenote-document-saving/save-to-grayscale-image/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote でグレースケール画像に保存 - Aspose.Note

## 導入

このチュートリアルでは、Aspose.Note for Java を使用して、OneNote でドキュメントをグレースケール画像として保存する方法を説明します。グレースケール イメージは、色情報がグレーの階調だけで表されるモノクロ画像です。 Aspose.Note は、Microsoft OneNote ドキュメントをプログラムで操作できる強力な Java API です。

## 前提条件

始める前に、以下のものがあることを確認してください。

1. Java Development Kit (JDK) がシステムにインストールされています。
2.  Java ライブラリの Aspose.Note。からダウンロードできます[ここ](https://releases.aspose.com/note/java/).
3. Java プログラミングの基本的な理解。

## パッケージのインポート

まず、必要なパッケージをインポートします。

```java
import com.aspose.note.ColorMode;
import com.aspose.note.Document;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.SaveFormat;
import java.io.IOException;
```

## ステップ 1: ドキュメントをロードする

まず、ドキュメントを Aspose.Note にロードします。交換する`"Your Document Directory"`ドキュメントディレクトリへのパスと`"Aspose.one"`OneNote ドキュメントの名前に置き換えます。

```java
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Aspose.one");
```

## ステップ 2: 出力パスとオプションを設定する

グレースケール イメージの出力パスを定義し、保存オプションを指定します。カラーモードをグレースケールに設定します。

```java
dataDir = dataDir + "SaveAsGrayscaleImage_out.png";
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);
options.setColorMode(ColorMode.GrayScale);
```

## ステップ 3: ドキュメントを保存する

最後に、指定したオプションを使用してドキュメントをグレースケール画像として保存します。

```java
oneFile.save(dataDir, options);
```

## 結論

おめでとう！ Aspose.Note for Java を使用して、OneNote でドキュメントをグレースケール イメージとして保存する方法を学習しました。これは、グレースケール画像が必要なさまざまなアプリケーションで非常に役立ちます。

## よくある質問

### Q1: グレースケール画像を別の形式で保存できますか?

 A1: はい、可能です。単に変更するだけです`SaveFormat`のパラメータ`ImageSaveOptions`コンストラクターを希望の形式に変更します。

### Q2: Aspose.Note は、OneNote ドキュメントのすべてのバージョンと互換性がありますか?

A2: Aspose.Note は Microsoft OneNote 2010 以降をサポートしています。

### Q3: Aspose.Note を使用するにはライセンスが必要ですか?

A3: はい、運用環境で Aspose.Note を使用するには、有効なライセンスが必要です。ただし、テスト目的で一時ライセンスを取得することはできます。

### Q4: ドキュメントを画像として保存する前に、ドキュメントの他の部分を操作できますか?

A4：もちろんです！ Aspose.Note は、OneNote ドキュメントをプログラムで編集するための幅広い機能を提供します。

### Q5: 問題が発生した場合、どこでサポートを受けられますか?

A5: Aspose.Note フォーラムでサポートを見つけることができます。[ここ](https://forum.aspose.com/c/note/28).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
