---
title: OneNote でノートブックをフラット化されたイメージに変換する - Aspose.Note
linktitle: OneNote でノートブックをフラット化されたイメージに変換する - Aspose.Note
second_title: Aspose.Note Java API
description: Aspose.Note for Java を使用して、OneNote でノートブックをフラット化された画像に変換する方法を学習します。すべての要素を 1 つの画像ファイルに簡単に保存できます。
weight: 13
url: /ja/java/onenote-notebook-operations/convert-notebook-to-flattened-image/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote でノートブックをフラット化されたイメージに変換する - Aspose.Note

## 導入

このチュートリアルでは、Aspose.Note for Java を使用して、OneNote でノートブックをフラット化されたイメージに変換するプロセスを説明します。これにより、ノートブックを画像ファイルとして保存でき、すべての要素が単一の画像形式で保存されるようになります。

## 前提条件

始める前に、以下のものがあることを確認してください。

1. Java Development Kit (JDK) がシステムにインストールされています。
2.  Aspose.Note for Java ライブラリがダウンロードされ、Java プロジェクトにセットアップされます。ライブラリはからダウンロードできます[ここ](https://releases.aspose.com/note/java/).
3. Java プログラミングの基本的な知識。

## パッケージのインポート

まず、Aspose.Note for Java から必要なパッケージをインポートする必要があります。

```java
import java.io.IOException;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.Notebook;
import com.aspose.note.NotebookImageSaveOptions;
import com.aspose.note.SaveFormat;
```

## ステップ 1: ドキュメント ディレクトリを設定する

まず、ノートブック ファイルが配置されるディレクトリを定義します。

```java
String dataDir = "Your Document Directory";
```

交換する`"Your Document Directory"`ノートブック ファイルへのパスを含めます。

## ステップ 2: ノートブックをロードする

次に、ノートブック ファイルをロードします。`Notebook`クラス：

```java
Notebook notebook = new Notebook(dataDir + "test.onetoc2");
```

必ず交換してください`"test.onetoc2"`ノートブック ファイルの名前を付けます。

## ステップ 3: 画像保存オプションを設定する

次に、ノートブックを画像として保存するためのオプションを設定します。保存形式を PNG として指定し、解像度を 400 DPI に設定します。

```java
NotebookImageSaveOptions saveOptions = new NotebookImageSaveOptions(SaveFormat.Png);
ImageSaveOptions documentSaveOptions = saveOptions.getDocumentSaveOptions();
documentSaveOptions.setResolution(400);
```

要件に応じて解像度を調整できます。

## ステップ 4: ノートブックを平らにする

すべての要素が 1 つの画像にフラット化されるようにするには、`flatten`というオプション`true`:

```java
saveOptions.setFlatten(true);
```

これにより、結果として得られる画像がノートブックのレイアウトを維持することが保証されます。

## ステップ 5: 画像を保存する

最後に、ノートブックをフラット化された画像として保存します。

```java
notebook.save(dataDir + "ExportImageasFlattenedNotebook_out.png", saveOptions);
```

交換する`"ExportImageasFlattenedNotebook_out.png"`希望の出力ファイル名を付けます。

## 結論

結論として、Aspose.Note for Java を使用すると、ノートブックを OneNote のフラット化された画像に簡単に変換できます。このプロセスにより、すべての要素が単一の画像形式で保存され、共有や表示が容易になります。

## よくある質問

### Q1: 出力画像の解像度を調整できますか?

 A1: はい、要件に応じて解像度を調整するには、`setResolution`メソッドのパラメータ。

### Q2: Aspose.Note は他の画像形式のエクスポートをサポートしていますか?

A2: はい、Aspose.Note はノートブックをエクスポートするために、PNG、JPEG、BMP などのさまざまな画像形式をサポートしています。

### Q3: 出力画像をさらにカスタマイズできますか?

A3: はい、Aspose.Note には、ページ サイズ、向き、品質設定など、出力画像をカスタマイズするための広範なオプションが用意されています。

### Q4: Aspose.Note for Java の試用版はありますか?

 A4: はい、以下から無料試用版を入手できます。[ここ](https://releases.aspose.com/).

### Q5: Aspose.Note for Java のサポートはどこで見つけられますか?

 A5: Aspose.Note フォーラムでサポートとリソースを見つけることができます。[ここ](https://forum.aspose.com/c/note/28).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
