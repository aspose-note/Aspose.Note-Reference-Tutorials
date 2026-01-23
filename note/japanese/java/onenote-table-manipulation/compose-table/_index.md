---
date: 2026-01-23
description: Aspose.Note for Java を使用して、プログラムで OneNote に表を追加する方法を学びましょう。効率的なドキュメント作成のためのステップバイステップガイド。
linktitle: How to add table to OneNote with Aspose.Note for Java
second_title: Aspose.Note Java API
title: Aspose.Note for Java を使用して OneNote に表を追加する方法
url: /ja/java/onenote-table-manipulation/compose-table/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote にテーブルを追加する方法（Aspose.Note for Java）

## はじめに
このチュートリアルでは、Aspose.Note for Java を使用して **OneNote にテーブルを追加** する方法を学びます。これにより、プログラムからリッチで構造化されたドキュメントを作成し、コラボレーションやレポート作成を強化できます。Aspose.Note は、手動編集なしで OneNote ページ、アウトライン、テーブルを構築するための強力な API を提供します。

## クイック回答
- **このチュートリアルの内容は？** Aspose.Note for Java を使用して OneNote にテーブルを追加する方法です。  
- **所要時間は？** 基本的な実装で約 10‑15 分です。  
- **ライセンスは必要ですか？** 評価用の無料トライアルで動作しますが、製品環境では商用ライセンスが必要です。  
- **対応している Java バージョンは？** Java 8 以降。  
- **テーブルのスタイルをカスタマイズできますか？** はい – API を通じてフォント、色、セルの枠線などを変更できます。

## 前提条件
チュートリアルに入る前に、以下の前提条件を満たしていることを確認してください。
- Java プログラミングの基本知識。  
- Aspose.Note for Java ライブラリがインストールされていること。[こちら](https://releases.aspose.com/note/java/)からダウンロードできます。  
- Java 開発用の統合開発環境（IDE）が設定されていること。

## パッケージのインポート
プロジェクトを開始するために必要なパッケージをインポートしてください。以下のインポート文を Java クラスに追加します。

```java
import com.aspose.note.*;
import java.awt.*;
import java.io.IOException;
import java.nio.file.Paths;
import java.util.stream.StreamSupport;
```

## ステップ 1: ドキュメント ディレクトリの設定
```java
String dataDir = "Your Document Directory";
```
`"Your Document Directory"` を、OneNote ドキュメントを保存したい実際のパスに置き換えてください。

## ステップ 2: ヘッダーの作成
```java
RichText headerText = new RichText().append("Super contest for suppliers.");
headerText.setParagraphStyle(new ParagraphStyle().setFontSize(18).setBold(true));
headerText.setAlignment(HorizontalAlignment.Center);
```
ドキュメント用の目を引くヘッダーを作成します。フォントサイズ、太字、配置などを必要に応じて調整してください。

## ステップ 3: ページとアウトラインの作成
```java
Page page = new Page();
Outline outline = page.appendChildLast(new Outline());
outline.setHorizontalOffset(50);
outline.appendChildLast(new OutlineElement()).appendChildLast(headerText);
```
新しいページとアウトラインを設定し、先に作成したヘッダーをアウトラインに追加します。

## ステップ 4: 要約テキストの追加
```java
RichText bodyTextHeader = outline.appendChildLast(new OutlineElement()).appendChildLast(new RichText());
bodyTextHeader.setParagraphStyle(ParagraphStyle.getDefault());
bodyTextHeader.append("This is the final ranking of proposals got from our suppliers.");
```
テーブルのコンテキストを提供する簡潔な要約テキストを含めます。

## ステップ 5: OneNote にテーブルを追加
```java
Table ranking = outline.appendChildLast(new OutlineElement()).appendChildLast(new Table());
// Remaining steps are involved in setting up the table structure, header row, and adding empty rows.
// Refer to the provided code for detailed implementation.
```
テーブル構造を組み立て、関連情報で埋めます。コード例には列の追加、ヘッダー行、空行、そして「Contacts」列用のテンプレートコンテンツが含まれています。

## ステップ 6: ドキュメントの保存
```java
Document d = new Document();
d.appendChildLast(page);
d.save(Paths.get(dataDir, "ComposeTable_out.one").toString());
```
指定したファイル名とディレクトリパスで作成したドキュメントを保存します。

## 結論
おめでとうございます！Aspose.Note for Java を使用して **OneNote にテーブルを追加** することに成功しました。このチュートリアルは、ステップバイステップのプロセスを示し、プログラムからドキュメント作成機能を強化できるようにしました。

## よくある質問
### Q: Aspose.Note for Java のドキュメントはどこで見つけられますか？
ドキュメントは[こちら](https://reference.aspose.com/note/java/)をご参照ください。

### Q: Aspose.Note for Java はどこからダウンロードできますか？
[このリンク](https://releases.aspose.com/note/java/)からダウンロードできます。

### Q: 無料トライアルは利用できますか？
はい、無料トライアルは[こちら](https://releases.aspose.com/)から利用可能です。

### Q: Aspose.Note for Java のサポートはどこで受けられますか？
サポートフォーラムは[こちら](https://forum.aspose.com/c/note/28)です。

### Q: 一時ライセンスを取得できますか？
はい、一時ライセンスは[こちら](https://purchase.aspose.com/temporary-license/)から取得できます。

---

**Last Updated:** 2026-01-23  
**Tested With:** Aspose.Note for Java (latest release)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}