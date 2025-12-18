---
date: 2025-12-18
description: Aspose.Note for Java を使用して OneNote ページを PDF にエクスポートする方法を学びましょう。分割アルゴリズムを選択し、ページ分割を設定して、簡単に
  PDF ファイルを生成できます。
linktitle: Export OneNote Pages with Splitting Algorithm Method – Aspose.Note
second_title: Aspose.Note Java API
title: 分割アルゴリズム手法によるOneNoteページのエクスポート – Aspose.Note
url: /ja/java/onenote-document-saving/use-splitting-algorithm-method/
weight: 26
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Splitting Algorithm メソッドで OneNote ページをエクスポート – Aspose.Note

## はじめに

プログラムで OneNote ページを PDF ドキュメントに **エクスポート** する必要がある場合、Aspose.Note for Java を使用すれば簡単に実現できます。このチュートリアルでは Splitting Algorithm メソッドを順に解説し、ページ間でコンテンツがどのように分割されるかを制御して、きれいで読みやすい PDF 出力を実現します。PDF 保存オプションの設定方法、適切なページ分割アルゴリズムの選択方法、そして最終的に PDF ファイルを生成する手順を、数行の Java コードで示します。

## クイック回答
- **Splitting Algorithm は何をするものですか？** OneNote ページを PDF にエクスポートする際、ページ境界をまたぐオブジェクトの処理方法を決定します。  
- **必要なライブラリは何ですか？** Aspose.Note for Java（公式 Aspose サイトからダウンロード）。  
- **ライセンスは必要ですか？** 本番環境で使用するには一時ライセンスまたはフルライセンスが必要です。無料トライアルも利用可能です。  
- **大規模な OneNote ノートブックをエクスポートできますか？** はい。ライブラリは大きなファイルを効率的に処理し、ページ分割ルールを設定できます。  
- **サポートされている出力形式は何ですか？** PDF、JPEG、PNG、XPS など。本ガイドは PDF エクスポートに焦点を当てています。

## **export onenote pages** とは何ですか？

OneNote ページのエクスポートとは、ネイティブの `.one` ファイル形式を PDF などのより汎用的な形式に変換することです。これにより、OneNote アプリケーションが不要な状態でコンテンツを共有、アーカイブ、印刷することが可能になります。

## **export onenote pages** に Splitting Algorithm を使用する理由

このアルゴリズムは、テーブル、画像、図形などの複雑なオブジェクトがページ区切りでどのように処理されるかを細かく制御できます。適切なアルゴリズムを選択することで、以下が可能です。

* 各ページのビジュアルレイアウトを保持する。  
* 切り取られる可能性のあるコンテンツの切れ端を防止する。  
* オブジェクトを次ページへきれいに移動できる場合、生成されるページ数を削減する。  

## 前提条件

開始する前に、以下の前提条件が揃っていることをご確認ください。

1. Java Development Kit (JDK)：システムに JDK がインストールされていることを確認してください。[website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) からダウンロードできます。  
2. Aspose.Note for Java ライブラリ： [download link](https://releases.aspose.com/note/java/) から Aspose.Note for Java ライブラリをダウンロードしてインストールしてください。

## パッケージのインポート

Java プロジェクトで、Aspose.Note の機能を利用するために必要なパッケージをインポートします。

```java
import java.io.IOException;
import com.aspose.note.AlwaysSplitObjectsAlgorithm;
import com.aspose.note.Document;
import com.aspose.note.KeepPartAndCloneSolidObjectToNextPageAlgorithm;
import com.aspose.note.KeepSolidObjectsAlgorithm;
import com.aspose.note.PdfSaveOptions;
```

## 手順 1: ドキュメントディレクトリの定義

OneNote ドキュメントが格納されているディレクトリを設定します。

```java
String dataDir = "Your Document Directory";
```

## 手順 2: OneNote ドキュメントのロード

Aspose.Note の `Document` クラスを使用して OneNote ドキュメントをロードします。

```java
Document doc = new Document(dataDir + "Sample1.one");
```

## 手順 3: PDF 保存オプションの設定

`PdfSaveOptions` のインスタンスを作成し、ドキュメントを PDF として保存するオプションを指定します。ここで **ページ分割** の動作やその他の PDF 関連設定を行います。

```java
PdfSaveOptions pdfSaveOptions = new PdfSaveOptions();
```

## 手順 4: ページ分割アルゴリズムの設定

要件に合わせて適切な分割アルゴリズムを選択します。ここでは `KeepPartAndCloneSolidObjectToNextPageAlgorithm` を使用しています。このアルゴリズムはオブジェクトの一部を現在のページに残し、残りを次のページにクローンします。

```java
pdfSaveOptions.setPageSplittingAlgorithm(new KeepPartAndCloneSolidObjectToNextPageAlgorithm(100));
```

## 手順 5: ドキュメントの保存

指定した PDF 保存オプションでドキュメントを保存します。この手順で **PDF onenote** 出力が生成され、開いたり共有したり印刷したりできます。

```java
try {
    doc.save(dataDir + "UsingSplittingAlgorithmMethod_out.Jpeg", pdfSaveOptions);
} catch (Exception ex) {
    System.out.println("Exception: " + ex.getMessage());
}
```

## よくある問題と解決策

| 問題 | 解決策 |
|------|--------|
| **オブジェクトがページ境界で切り取られる** | `AlwaysSplitObjectsAlgorithm` などの別のアルゴリズムを試すか、`KeepPartAndCloneSolidObjectToNextPageAlgorithm` のしきい値を増やしてください。 |
| **出力 PDF が空白** | ソースの `.one` ファイルが破損していないか、`dataDir` パスが正しいかを確認してください。 |
| **大規模ノートブックでパフォーマンスが低下** | `pdfSaveOptions.setCompressImages(true)` を使用してメモリ使用量を削減し、ノートブックを小さなセクションに分割して処理することを検討してください。 |

## よくある質問

**Q: Aspose.Note for Java を他のプログラミング言語でも使用できますか？**  
A: はい、Aspose.Note は .NET、C++、Python でも利用可能です。

**Q: 大規模な OneNote ファイルの処理に Aspose.Note は適していますか？**  
A: はい。ライブラリは大規模ノートブックを効率的に処理できるよう最適化されています。

**Q: Aspose.Note の追加リソースやサポートはどこで見つけられますか？**  
A: サポートやガイダンスについては、[documentation](https://reference.aspose.com/note/java/) と [forum](https://forum.aspose.com/c/note/28) を参照してください。

**Q: 購入前に Aspose.Note を試すことはできますか？**  
A: はい、[free trial](https://releases.aspose.com/) を利用して機能を確認できます。

**Q: Aspose.Note の一時ライセンスはどのように取得できますか？**  
A: [temporary license](https://purchase.aspose.com/temporary-license/) をリクエストして、試用期間中に製品を評価できます。

**最終更新日:** 2025-12-18  
**テスト環境:** Aspose.Note 24.12 for Java  
**作者:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}