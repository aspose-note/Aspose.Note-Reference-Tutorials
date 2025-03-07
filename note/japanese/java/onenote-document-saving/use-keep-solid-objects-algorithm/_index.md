---
title: OneNote でソリッド オブジェクト保持アルゴリズムを使用する - Aspose.Note
linktitle: OneNote でソリッド オブジェクト保持アルゴリズムを使用する - Aspose.Note
second_title: Aspose.Note Java API
description: Java のソリッド オブジェクト保持アルゴリズムを使用して PDF に変換するときに、Aspose.Note ドキュメント内のソリッド オブジェクトを保持する方法を学びます。
weight: 25
url: /ja/java/onenote-document-saving/use-keep-solid-objects-algorithm/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote でソリッド オブジェクト保持アルゴリズムを使用する - Aspose.Note

## 導入

このチュートリアルでは、Aspose.Note for Java の Keep Solid Objects アルゴリズムを利用する方法を検討します。このアルゴリズムは、ドキュメント内のソリッド オブジェクトを PDF 形式に変換する際にその整合性を維持するのに非常に役立ちます。プロセスを段階的に分けて、各段階での明確さと理解を確保します。

## 前提条件

始める前に、以下のものがあることを確認してください。

1. Java Development Kit (JDK) がシステムにインストールされています。
2.  Java ライブラリの Aspose.Note。からダウンロードできます[ここ](https://releases.aspose.com/note/java/).

## パッケージのインポート

まず、必要なパッケージをインポートしましょう。

```java
import java.io.IOException;
import com.aspose.note.AlwaysSplitObjectsAlgorithm;
import com.aspose.note.Document;
import com.aspose.note.KeepPartAndCloneSolidObjectToNextPageAlgorithm;
import com.aspose.note.KeepSolidObjectsAlgorithm;
import com.aspose.note.PdfSaveOptions;
```

## ステップ 1: ドキュメントをロードする

次のコード スニペットを使用して、ドキュメントを Aspose.Note に読み込みます。

```java
String dataDir = "Your Document Directory";
Document doc = new Document(dataDir + "Aspose.one");
```

## ステップ 2: PDF 保存オプションを構成する

PdfSaveOptions を定義し、PageSplittingAlgorithm を KeepSolidObjectsAlgorithm に設定します。

```java
PdfSaveOptions pdfSaveOptions = new PdfSaveOptions();
pdfSaveOptions.setPageSplittingAlgorithm(new KeepSolidObjectsAlgorithm());
```

## ステップ 3: 高さ制限を調整する (オプション)

必要に応じて、クローン化されたパーツの高さ制限を調整できます。

```java
float heightLimitOfClonedPart = 500;
pdfSaveOptions.setPageSplittingAlgorithm(new KeepSolidObjectsAlgorithm(heightLimitOfClonedPart));
```

## ステップ 4: ドキュメントを保存する

最後に、指定した PDF 保存オプションを使用してドキュメントを保存します。

```java
String outputDir = "Your Output Directory";
String outputFile = outputDir + "UsingKeepSolidObjectsAlgorithm_out.pdf";
doc.save(outputFile);
```

## 結論

このチュートリアルでは、Aspose.Note for Java の Keep Solid Objects アルゴリズムを利用する方法を学びました。このアルゴリズムにより、ドキュメント内のソリッド オブジェクトが PDF 形式に変換されるときに確実に保持され、ドキュメントの整合性が維持されます。

## よくある質問

### Q1: クローンパーツの高さ制限を調整できますか?

 A1: はい、要件に応じてクローン パーツの高さ制限を調整できます。`heightLimitOfClonedPart`パラメータ。

### Q2: 詳しいドキュメントはどこで入手できますか?

 A2: Aspose.Note for Java で詳細なドキュメントを見つけることができます。[ここ](https://reference.aspose.com/note/java/).

### Q3: 無料トライアルはありますか?

 A3: はい、Aspose.Note for Java の無料トライアルを入手できます。[ここ](https://releases.aspose.com/).

### Q4: 問題が発生した場合、どうすればサポートを受けられますか?

 A4: Aspose コミュニティからサポートを受けることができます。[ここ](https://forum.aspose.com/c/note/28).

### Q5: ライセンスはどこで購入できますか?

 A5: Aspose.Note for Java のライセンスを購入できます。[ここ](https://purchase.aspose.com/buy).

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
