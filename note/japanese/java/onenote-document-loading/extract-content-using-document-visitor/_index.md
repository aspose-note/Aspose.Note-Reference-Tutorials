---
date: 2026-02-10
description: Aspose.Note for Java を使用して OneNote をテキストに変換し、画像を抽出する方法を学びましょう。このガイドでは、.one
  ファイルを Java で読み取り、OneNote のテキスト抽出を実行する手順を示します。
linktitle: Convert OneNote to Text and Extract Images using Document Visitor - Java
second_title: Aspose.Note Java API
title: Document Visitor を使用して OneNote をテキストに変換し、画像を抽出する - Java
url: /ja/java/onenote-document-loading/extract-content-using-document-visitor/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Document Visitor を使用した OneNote のテキスト変換と画像抽出 - Java

## はじめに

Aspose.Note for Java を使用すると、**OneNote をテキストに変換**しながら **OneNote ノートブックから画像を抽出**することが簡単になります。このチュートリアルでは、OneNote ファイルを読み込み、カスタム `DocumentVisitor` で構造を走査し、画像とプレーンテキストの両方を取得する完全なハンズオン例をご紹介します。最後まで読むと、**.one ファイルを Java で読み込む**方法と、このアプローチが自動コンテンツ移行やレポート作成に最適な理由が分かります。

## よくある質問
- **必要なライブラリは？** Aspose.Note for Java（ダウンロードリンクは下記参照）。
- **画像のみを抽出することはできますか？** はい。`DocumentVisitor` に `VisitImageStart` メソッドを実装してください。
- **Javaで.oneファイルを読み込むには？** `new Document(path, new LoadOptions())` を使用してください。
- **本番環境での使用にはライセンスが必要ですか？** 試用版以外の使用には商用ライセンスが必要です。
- **サポートされているJavaのバージョンは？** JDK8以降。

## OneNoteをテキストに変換するとは？

OneNote をテキストに変換するとは、`.one` ノートブックから生のテキストコンテンツを抽出し、プレーンな Unicode テキストとして保存することを指します。検索可能なアーカイブや軽量データフィード、元の OneNote 書式なしのシンプルな要約が必要な場合に便利です。

## OneNoteのテキスト抽出にAspose.Noteのドキュメントビジターを使用する理由

- **きめ細かな制御:** ビジターパターンを使用することで、処理対象とするノード（ページ、アウトライン、画像、リッチテキスト）を正確に指定できます。
- **パフォーマンス:** ドキュメント全体を単一のデータブロックとしてメモリに読み込む必要がなく、各ノードは必要に応じて処理されます。
- **汎用性:** 同じビジターを拡張して、画像、表、カスタムメタデータを抽出できるため、**OneNoteをテキストに変換する**タスクと**画像を抽出する**タスクの両方に対応するワンストップソリューションとなります。

## 前提条件

開始する前に、以下のものが必要です。

1. Java Development Kit (JDK) 8以降がインストールされていること。
2. Aspose.Note for Javaライブラリがダウンロードされていること。**[こちら](https://releases.aspose.com/note/java/)**からダウンロードできます。
3. 画像抽出またはテキスト変換を行うOneNoteドキュメント（`.one`ファイル）。

## パッケージのインポート

まず、Aspose.Note APIから必要なクラスをインポートします。

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

## ステップ 1: カスタムドキュメントビジターの設定

`DocumentVisitor` を継承するクラスを作成します。このクラスは OneNote ドキュメント内の各ノードに対して呼び出され、**OneNote 画像の抽出**と、必要に応じてテキストの収集を可能にします。

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

## ステップ 2: ビジターメソッドの実装

対象となるノードタイプに対応するオーバーライドメソッドを追加します。以下では、リッチテキスト、画像、タイトル、ページ、アウトライン、アウトライン要素を処理します。`VisitImageStart` メソッドは、画像の抽出処理を実行します。

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

- **OneNoteから画像を抽出する:** `VisitImageStart` を使用すると、生の画像バイトに直接アクセスできます。
- **OneNoteをテキストに変換する:** `VisitRichTextStart` はテキストコンテンツを収集し、**OneNoteをテキストに変換する**操作を簡単に実行できるようにします。
- **.oneファイルをJavaで読み込む:** ビジターパターンは、基となる`.one`ファイルの構造を抽象化するため、バイナリ形式を自分で解析する必要はありません。

## ステップ3: メインメソッドからビジターを実行する

`.one`ファイルを読み込み、ビジターをインスタンス化して、トラバーサルを開始します。

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

## 一般的な使用例

- **自動レポート作成:** OneNote 会議ノートブックから画像とテキストを抽出し、PDF または HTML 形式の要約を生成します。

- **コンテンツ移行:** 既存の OneNote アーカイブをプレーンテキストファイルに変換し、インデックス作成や検索エンジンへの取り込みに利用します。

- **デジタルアセットの抽出:** 埋め込まれたスクリーンショット、図、写真などを抽出し、他のアプリケーションで再利用します。

## トラブルシューティングとヒント

- **大容量ノートブック:** メモリの問題が発生した場合は、`VisitPageStart` をチェックしてページを個別に処理し、必要な場合にのみページレベルのリソースを読み込んでください。

- **画像形式:** `Image` オブジェクトは生のバイト列を返します。保存する前に、画像形式 (PNG、JPEG) を検出する必要がある場合があります。

- **ライセンスエラー:** 本番環境でドキュメントを読み込む前に、Aspose ライセンス (`License license = new License(); license.setLicense("Aspose.Note.Java.lic");`) が正しく設定されていることを確認してください。

- **画像を効率的に抽出する方法:** 特定の画像タイプのみが必要な場合は、`VisitImageStart` 内のノードをサイズまたはフォーマットでフィルタリングしてください。

## よくある質問

**Q: OneNote ドキュメントから特定の種類のコンテンツを抽出できますか？** A: はい。必要なビジターメソッドのみをオーバーライドすることで可能です（例: 画像の場合は `VisitImageStart`、テキストの場合は `VisitRichTextStart`）。

**Q: Aspose.Note for Java は、異なるバージョンの OneNote ドキュメントと互換性がありますか？** A: はい、もちろんです。このライブラリは主要な OneNote ファイルバージョンすべてをサポートしているため、元の OneNote バージョンに関係なく、** .one ファイル Java** プロジェクトを安全に読み込むことができます。

**Q: この抽出プロセスを Java アプリケーションに統合できますか？** A: はい。ビジターパターンは、あらゆる Java コードベース内でシームレスに動作します。ライブラリ JAR を追加し、上記の例を呼び出すだけです。


**Q: Aspose.Note for Java は複雑な OneNote ドキュメントの処理をサポートしていますか？** A: はい、サポートしています。ネストされたアウトライン、埋め込みメディア、カスタムデータはすべて、ビジター API を通じて公開されています。

**Q: 処理できる OneNote ドキュメントのサイズに制限はありますか？** A: 厳密な制限はありませんが、非常に大きなノートブックではより多くのヒープメモリが必要になる場合があります。ページごとに処理することを検討してください。

**Q: 抽出したテキストをプレーンテキストファイルに変換するにはどうすればよいですか？** A: `myConverter.GetText()` が `String` を返したら、標準の Java I/O を使用してファイルに書き込みます (`Files.write(Paths.get("output.txt"), text.getBytes());`)。

---
**Last Updated:** 2026-02-10  
**Tested With:** Aspose.Note for Java 24.10  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}