---
date: 2025-12-04
description: Aspose.Note を使用して、OneNote ファイルから画像を抽出し、Java で OneNote をテキストに変換する方法を学びましょう。コード例付きのステップバイステップガイド。
linktitle: Extract Images from OneNote using Document Visitor - Java
second_title: Aspose.Note Java API
title: Document Visitor を使用して OneNote から画像を抽出する - Java
url: /ja/java/onenote-document-loading/extract-content-using-document-visitor/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Document Visitor を使用した OneNote からの画像抽出 - Java

## 概要

Aspose.Note for Java を使用すると、OneNote ノートブックから画像を抽出したり、Java で基礎となる `.one` ファイルを読み取ったりすることが簡単になります。このチュートリアルでは、OneNote ファイルをロードし、カスタム `DocumentVisitor` で構造を走査し、画像とプレーンテキストの両方を取得する完全なハンズオン例をご紹介します。最後には、テキストコンテンツだけが必要な場合に **OneNote をテキストに変換** する方法もわかります。

## クイック回答
- **必要なライブラリは何ですか？** Aspose.Note for Java (以下のダウンロードリンク)。  
- **画像だけを抽出できますか？** はい – `DocumentVisitor` の `VisitImageStart` メソッドを実装します。  
- **Java で .one ファイルを読むには？** `new Document(path, new LoadOptions())` を使用します。  
- **本番環境でライセンスが必要ですか？** トライアル以外の使用には商用ライセンスが必要です。  
- **サポートされている Java バージョンは？** JDK 8 以上。

## 前提条件

開始する前に、以下が揃っていることを確認してください：

1. Java Development Kit (JDK) 8 以上がインストールされていること。  
2. Aspose.Note for Java ライブラリをダウンロードする。**[here](https://releases.aspose.com/note/java/)** からダウンロードできます。  
3. 画像を抽出したりテキストに変換したりしたい OneNote ドキュメント（`.one` ファイル）。

## パッケージのインポート

まず、Aspose.Note API から必要なクラスをインポートします。

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.DocumentVisitor;
import com.aspose.note.Image;
import com.aspose.note.LoadOptions;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.OutlineGroup;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.Title;
```

## ステップ 1: カスタム Document Visitor の設定

`DocumentVisitor` を継承したクラスを作成します。このクラスは OneNote ドキュメント内の各ノードに対して呼び出され、**OneNote から画像を抽出**し、必要に応じてテキストを収集できます。

```java
public class ExtractOneNoteContentUsingDocumentvisitor extends DocumentVisitor {
    
    final private StringBuilder mBuilder;
    final private boolean mIsSkipText;
    private int nodecount;

    public ExtractOneNoteContentUsingDocumentvisitor() {
        nodecount = 0;
        mIsSkipText = false;
        mBuilder = new StringBuilder();
    }
    
    // Other methods will be implemented here
}
```

## ステップ 2: Visitor メソッドの実装

対象とするノードタイプのオーバーライドを追加します。以下ではリッチテキスト、画像、タイトル、ページ、アウトライン、アウトライン要素を処理しています。画像抽出は `VisitImageStart` メソッドで行われます。

```java
// Visitor methods for different types of nodes

public /* override */ void VisitRichTextStart(RichText run) {
    ++nodecount;
    AppendText(run.getText());
}

public /* override */ void VisitDocumentStart(Document document) {
    ++nodecount;
}

public /* override */ void VisitPageStart(Page page) {
    ++nodecount;
}

public /* override */ void VisitTitleStart(Title title) {
    ++nodecount;
}

public /* override */ void VisitImageStart(Image image) {
    ++nodecount;
    // Here you could save the image to disk or process it further
    System.out.println("Found image with size: " + image.getData().length + " bytes");
}

public /* override */ void VisitOutlineGroupStart(OutlineGroup outlineGroup) {
    ++nodecount;
}

public void VisitOutlineStart(Outline outline) {
    ++nodecount;
}

public void VisitOutlineElementStart(OutlineElement outlineElement) {
    ++nodecount;
}
```

### これらのメソッドを実装する理由

- **OneNote から画像を抽出:** `VisitImageStart` は生の画像バイトに直接アクセスできます。  
- **OneNote をテキストに変換:** `VisitRichTextStart` はテキストコンテンツを収集し、シンプルな **OneNote をテキストに変換** 操作を可能にします。  
- **Java で .one ファイルを読む:** Visitor パターンにより基礎となる `.one` ファイル構造が抽象化され、バイナリ形式を自分で解析する必要がなくなります。

## ステップ 3: メインメソッドから Visitor を実行

`.one` ファイルをロードし、Visitor のインスタンスを作成して走査を開始します。

```java
public static void main(String[] args) throws IOException {
    // Open the document we want to convert.
    String dataDir = "Your Document Directory";
    Document doc = new Document(dataDir + "Sample1.one", new LoadOptions());
    
    // Create an object that inherits from the DocumentVisitor class.
    ExtractOneNoteContentUsingDocumentvisitor myConverter = new ExtractOneNoteContentUsingDocumentvisitor();
    
    // Accept the visitor to start the visiting process.
    doc.accept(myConverter);
    
    // Retrieve the result of the operation.
    System.out.println(myConverter.GetText());   // Text extracted from the notebook
    System.out.println(myConverter.NodeCount()); // Total nodes visited
}
```

## 一般的なユースケース

- **自動レポート:** OneNote の会議ノートブックから画像とテキストを取得し、PDF または HTML のサマリーを生成します。  
- **コンテンツ移行:** 旧式の OneNote アーカイブをプレーンテキストファイルに変換し、インデックス作成や検索エンジンへの取り込みに利用します。  
- **デジタル資産の抽出:** 埋め込まれたスクリーンショット、図、写真を収集し、他のアプリケーションで再利用します。

## トラブルシューティングとヒント

- **大規模ノートブック:** メモリ問題が発生した場合、`VisitPageStart` を確認し、必要なときにページレベルのリソースだけをロードしてページ単位で処理します。  
- **画像形式:** `Image` オブジェクトは生バイトを返すため、保存前に形式（PNG、JPEG など）を検出する必要があります。  
- **ライセンスエラー:** 本番環境でドキュメントをロードする前に、Aspose のライセンスを設定してください（`License license = new License(); license.setLicense("Aspose.Note.Java.lic");`）。

## よくある質問

**Q: OneNote ドキュメントから特定の種類のコンテンツを抽出できますか？**  
A: はい – 必要な Visitor メソッドだけをオーバーライドすれば可能です（例: 画像は `VisitImageStart`、テキストは `VisitRichTextStart`）。

**Q: Aspose.Note for Java はさまざまなバージョンの OneNote ドキュメントと互換性がありますか？**  
A: もちろんです。ライブラリは主要な OneNote ファイルバージョンすべてをサポートしているため、元の OneNote バージョンに関係なく **Java で .one ファイルを読む** プロジェクトを安全に使用できます。

**Q: この抽出プロセスを Java アプリケーションに統合できますか？**  
A: はい。Visitor パターンは任意の Java コードベースでシームレスに機能します。ライブラリ JAR を追加し、上記の例を呼び出すだけです。

**Q: Aspose.Note for Java は複雑な OneNote ドキュメントの処理をサポートしていますか？**  
A: サポートしています。入れ子になったアウトライン、埋め込みメディア、カスタムデータはすべて Visitor API で取得可能です。

**Q: 処理できる OneNote ドキュメントのサイズに制限はありますか？**  
A: 明確な上限はありませんが、非常に大きなノートブックはヒープメモリを多く必要とする可能性があります。ページ単位で処理することを検討してください。

**Q: 抽出したテキストをプレーンテキストファイルに変換するには？**  
A: `myConverter.GetText()` が `String` を返したら、標準的な Java I/O を使用してファイルに書き込みます（`Files.write(Paths.get("output.txt"), text.getBytes());`）。

---  

**最終更新日:** 2025-12-04  
**テスト環境:** Aspose.Note for Java 24.10  
**作者:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}