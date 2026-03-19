---
date: 2026-03-19
description: Aspose.Note for Java を使用して Java で OneNote ドキュメントを作成し、ストリームから画像を挿入する方法を学びましょう。Java
  開発者向けのステップバイステップガイドです。
linktitle: How to create onenote document java – Build Doc and Insert Image with Stream
second_title: Aspose.Note Java API
title: JavaでOneNoteドキュメントを作成する方法 – ストリームを使用して文書を構築し画像を挿入
url: /ja/java/onenote-hyperlinks-images/build-doc-insert-image-stream/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# JavaでOneNoteドキュメントを作成する方法 – ドキュメントの構築とストリームで画像を挿入

## はじめに

ようこそ！このチュートリアルでは、**JavaでOneNoteドキュメントを作成**し、画像ストリームを使用して画像を挿入する方法を学びます。各ステップを順に解説し、各要素が重要な理由を説明し、実際のプロジェクトで技術を適用できる実用的なヒントを提供します。最後までで、プログラムからOneNoteページを生成し、必要な場所に画像を埋め込むことができるようになります。

## クイック回答
- **必要なライブラリは何ですか？** Aspose.Note for Java  
- **ストリームから画像を挿入できますか？** Yes – just pass an `InputStream` to the `Image` constructor.  
- **どの形式にエクスポートできますか？** Any format supported by Aspose.Note, e.g., PDF, DOCX, HTML.  
- **開発にライセンスは必要ですか？** A free temporary license works for evaluation; a full license is required for production.  
- **必要なJavaバージョンは何ですか？** Java 8 or higher.

## 「JavaでOneNoteドキュメントを作成」とは何ですか？

JavaでOneNoteドキュメントを作成することは、Aspose.Note API を使用して、OneNote デスクトップ クライアントを開かずにノートブック構造（ページ、アウトライン、要素）をプログラムで構築することを意味します。このアプローチは、レポートの自動生成、ノートのバッチ処理、またはOneNote コンテンツを大規模な Java アプリケーションに統合するのに最適です。

## なぜ Aspose.Note for Java を使用して JavaでOneNoteドキュメントを作成するのか？

- **完全な制御** ページレイアウト、アウトラインの位置、要素のスタイリングを完全に制御できます。  
- **COM 相互運用なし** – Java をサポートする任意の OS で動作します。  
- **豊富なエクスポートオプション** – 同じドキュメントを単一の呼び出しで PDF、DOCX、HTML などに変換できます。  
- **ストリームフレンドリー** – 画像をメモリ、ネットワーク、クラウドストレージから直接ロードできます。

## 前提条件

始める前に、以下が設定されていることを確認してください：

### Java Development Kit (JDK)

マシンにインストールされた最新の JDK（8 以降）。

### Aspose.Note for Java ライブラリ

公式 Aspose リリースページからライブラリをダウンロードしてください: [https://releases.aspose.com/note/java/](https://releases.aspose.com/note/java/)。

### IDE の設定

お気に入りの IDE（IntelliJ IDEA、Eclipse、VS Code）で、プロジェクトのクラスパスに Aspose.Note の JAR ファイルを含めるよう設定してください。

## パッケージのインポート

まず、必要な Java と Aspose.Note のクラスをインポートします。これらのインポートにより、ドキュメント作成、ページ処理、アウトライン管理、画像挿入が可能になります。

```java
import java.io.FileInputStream;
import java.io.FileNotFoundException;
import java.io.IOException;
import java.io.InputStream;
import com.aspose.note.Document;
import com.aspose.note.HorizontalAlignment;
import com.aspose.note.Image;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.SaveFormat;
```

## ステップ 1: ドキュメントディレクトリの設定

ソース画像が格納され、出力ファイルが保存されるフォルダーを定義します。プレースホルダーを実際のパスに置き換えてください。

```java
String dataDir = "Your Document Directory";
```

## ステップ 2: Document オブジェクトの作成

`Document` の新しいインスタンスを作成します。このオブジェクトは構築中の OneNote ノートブックを表します。

```java
Document doc = new Document();
```

## ステップ 3: Page オブジェクトの初期化

このノートブックページのすべてのアウトラインと要素を保持する `Page` を作成します。

```java
Page page = new Page();
```

## ステップ 4: Outline の作成

`Outline` は配置された要素のコンテナとして機能します。ここでは、アウトラインをページ上に配置するために垂直オフセットと水平オフセットを設定します。

```java
Outline outline1 = new Outline();
outline1.setVerticalOffset(600);
outline1.setHorizontalOffset(0);
```

## ステップ 5: Outline Element の作成

`OutlineElement` はこれから挿入する画像をホストします。

```java
OutlineElement outlineElem1 = new OutlineElement();
```

## ステップ 6: 画像ストリームのロード

画像ファイルをストリームとして開きます。ストリームを使用すると、画像をディスクに保存せずに任意のソース（ファイルシステム、ネットワーク、データベース）から読み取れます。

```java
InputStream fs = null;
try {
    fs = new FileInputStream(dataDir + "image.jpg");
} catch (FileNotFoundException e) {
    e.printStackTrace();
}
```

## ステップ 7: 画像の挿入

`Image` オブジェクトを作成します。後でストリームを提供する場合、最初の引数は `null` にできますが、簡単のためここではファイルパスを参照し、ページの右側に配置するように設定します。

```java
Image image = new Image(null, dataDir + "image1.jpg");
image.setAlignment(HorizontalAlignment.Right);
```

## ステップ 8: 画像を Outline Element に追加

画像をアウトライン要素に追加し、ページのビジュアル階層の一部にします。

```java
outlineElem1.appendChildLast(image);
```

## ステップ 9: Outline Element を Outline に追加

現在、画像を含むアウトライン要素をアウトラインコンテナに添付します。

```java
outline1.appendChildLast(outlineElem1);
```

## ステップ 10: Outline を Page に追加

アウトラインをページに配置します。

```java
page.appendChildLast(outline1);
```

## ステップ 11: Page を Document に追加

完全に構築されたページをドキュメントオブジェクトに追加します。

```java
doc.appendChildLast(page);
```

## ステップ 12: ドキュメントの保存

最後に、必要な形式で OneNote ドキュメントを保存します。この例では PDF にエクスポートしますが、Aspose.Note がサポートする任意の形式を選択できます。

```java
try {
    doc.save("D://Aspose_JavaProjects//OneNote//out3.pdf", SaveFormat.Pdf);
} catch (IOException e) {
    e.printStackTrace();
}
```

これらの手順に従うことで、**JavaでOneNoteドキュメントを作成**し、入力ストリームを使用して画像を埋め込むことに成功しました。

## よくある落とし穴とヒント

- **ストリームが閉じられていない** – 本番環境では、必ず `InputStream` を `finally` ブロックで閉じるか、try‑with‑resources を使用してください。  
- **ファイルパスが正しくない** – `dataDir` が適切なセパレーター（`/` または `\`）で終わっているか確認してください。  
- **画像の配置** – 画像が画面外に表示される場合、アウトラインの `VerticalOffset`/`HorizontalOffset` の値を調整してください。  
- **ライセンス例外** – 評価版を使用すると出力に透かしが付くことがあります。透かしを除去するには有効なライセンスを適用してください。

## よくある質問

### Q1: Aspose.Note for Java はすべてのバージョンの OneNote と互換性がありますか？

Aspose.Note for Java はさまざまな OneNote ファイル形式をサポートしており、デスクトップ、オンライン、モバイル版すべてでの互換性を確保しています。

### Q2: Aspose.Note for Java を使用して OneNote ドキュメントに挿入した画像の外観をカスタマイズできますか？

はい、`Image` オブジェクトの対応するプロパティを使用して、配置、サイズ、回転、さらにはクロッピングまで変更できます。

### Q3: Aspose.Note for Java は PDF 以外の他のドキュメント形式もサポートしていますか？

もちろんです。API は DOCX、HTML、XPS など複数の形式にエクスポートでき、ノートの共有やアーカイブ方法に柔軟性を提供します。

### Q4: Aspose.Note for Java の追加リソースやサポートはどこで見つけられますか？

公式 Aspose ウェブサイトでは、豊富なドキュメント、コード例、フォーラム、評価用の一時ライセンスが提供されています。

### Q5: Aspose.Note for Java のトライアル版はありますか？

はい、Aspose のリリースページから無料トライアルをダウンロードし、購入前にすべての機能を試すことができます。

## 結論

これで、**JavaでOneNoteドキュメントを作成**し、`InputStream` から直接画像を埋め込む完全なエンドツーエンドの例が手に入りました。テキスト、テーブル、図形などの追加要素を試してノートを充実させてください。準備ができたら、Aspose.Note が提供する多数のエクスポートオプションを活用し、OneNote コンテンツを PDF、DOCX、HTML などで共有しましょう。

---

**最終更新日:** 2026-03-19  
**テスト環境:** Aspose.Note for Java 24.12（執筆時点での最新）  
**作者:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}