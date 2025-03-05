---
title: OneNote の固定しきい値を使用してバイナリ イメージに保存する
linktitle: OneNote の固定しきい値を使用してバイナリ イメージに保存する
second_title: Aspose.Note Java API
description: Aspose.Note Java の固定しきい値を使用して、Microsoft OneNote ドキュメントをバイナリ イメージとして簡単に保存します。 OneNote のファイル操作機能を強化します。
type: docs
weight: 14
url: /ja/java/onenote-document-saving/save-to-binary-image-using-fixed-threshold/
---
## 導入

Aspose.Note for Java は、開発者がプログラムで Microsoft OneNote ファイルを操作できるようにする強力な API です。このチュートリアルでは、固定しきい値を使用してドキュメントをバイナリ イメージとして保存する方法を検討します。これを実現するには、以下の手順に従ってください。

## 前提条件

始める前に、次のものが揃っていることを確認してください。

1. Java Development Kit (JDK) がシステムにインストールされています。
2.  Java ライブラリ用の Aspose.Note がダウンロードされました。からダウンロードできます[ここ](https://releases.aspose.com/note/java/).
3. Java プログラミングの基本的な知識。

## パッケージのインポート

まず、必要なパッケージを Java ファイルにインポートします。

```java
import com.aspose.note.*;
import java.io.IOException;
```

## ステップ 1: ドキュメントをロードする

Aspose.Note API を使用して OneNote ドキュメントを読み込みます。

```java
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Aspose.one");
```

## ステップ 2: 2 値化オプションを設定する

ドキュメントをバイナリ イメージとして保存するための 2 値化オプションを定義します。

```java
dataDir = dataDir + "SaveToBinaryImageUsingFixedThreshold_out.png";
ImageBinarizationOptions binarizationOptions = new ImageBinarizationOptions();
binarizationOptions.setBinarizationMethod(BinarizationMethod.FixedThreshold);
binarizationOptions.setBinarizationThreshold(123);
```

## ステップ 3: 画像保存オプションを設定する

カラーモードや二値化オプションなどの画像保存オプションを設定します。

```java
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);
options.setColorMode(ColorMode.BlackAndWhite);
options.setBinarizationOptions(binarizationOptions);
```

## ステップ 4: ドキュメントを保存する

指定されたオプションを使用して、ドキュメントをバイナリ イメージとして保存します。

```java
oneFile.save(dataDir, options);
```

## 結論

このチュートリアルでは、Aspose.Note for Java の固定しきい値を使用してドキュメントをバイナリ イメージとして保存する方法を学びました。次の手順に従うと、OneNote ファイルをプログラムで簡単に操作できます。

## よくある質問

### Q1: 2値化の閾値を調整できますか?

 A1: はい、要件に応じてしきい値を調整するには、`setBinarizationThreshold()`メソッドのパラメータ。

### Q2: Aspose.Note for Java は、Microsoft OneNote のすべてのバージョンと互換性がありますか?

A2: Aspose.Note for Java は、2010、2013、2016 などのさまざまなバージョンの Microsoft OneNote をサポートしています。

### Q3: 処理できる書類のサイズに制限はありますか?

A3: Aspose.Note for Java には処理できるドキュメントのサイズに制限がないため、大きなファイルを効率的に処理できます。

### Q4: 複数の OneNote ドキュメントを同時に変換できますか?

A4: はい、各ファイルを反復処理して必要な操作を適用することで、複数の OneNote ドキュメントをバッチ処理できます。

### Q5: Aspose.Note for Java のテクニカル サポートは利用できますか?

 A5: はい、テクニカル サポートは次のサイトから利用できます。[Aspose.Note フォーラム](https://forum.aspose.com/c/note/28)、ここで質問したり、専門家に支援を求めることができます。