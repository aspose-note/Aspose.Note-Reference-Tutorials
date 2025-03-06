---
title: OneNote にタグ付きの新しい画像ノードを追加する - Aspose.Note
linktitle: OneNote にタグ付きの新しい画像ノードを追加する - Aspose.Note
second_title: Aspose.Note Java API
description: Aspose.Note for Java を使用して、OneNote にタグ付きの新しい画像ノードを追加する方法を学習します。 Java プログラミング スキルを簡単に向上させます。
weight: 10
url: /ja/java/onenote-tag-operations/add-new-image-node-with-tag/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote にタグ付きの新しい画像ノードを追加する - Aspose.Note

## 導入
Java プログラミングの分野では、Aspose.Note は OneNote ドキュメントを簡単に処理するための強力なツールとして際立っています。スキルを向上させ、Aspose.Note を使用して OneNote にタグ付きの新しい画像ノードを追加する方法を学びたい場合は、ここが正しい場所です。このステップバイステップのガイドではプロセスを順を追って説明し、各概念を完全に理解できるようにします。
## 前提条件
チュートリアルに入る前に、必要なものがすべて揃っていることを確認してください。
1.  Aspose.Note for Java: Aspose.Note ライブラリがインストールされていることを確認してください。そうでない場合は、ダウンロードできます[ここ](https://releases.aspose.com/note/java/).
2. Java 開発環境: マシン上に動作する Java 開発環境がセットアップされていることを確認してください。
前提条件が整ったので、次のステップに進みましょう。
## パッケージのインポート
Java プロジェクトで、必要なパッケージをインポートすることから始めます。
```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.Image;
import com.aspose.note.NoteTag;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.SaveFormat;
import com.aspose.note.TagIcon;
```
## ステップ 1: ドキュメント オブジェクトを作成する
```java
//ドキュメントディレクトリへのパス。
String dataDir = "Your Document Directory";
//Documentクラスのオブジェクトを作成します。
Document doc = new Document();
```
## ステップ 2: ページ クラス オブジェクトを初期化する
```java
//Pageクラスオブジェクトを初期化する
Page page = new Page();
```
## ステップ 3: アウトライン クラス オブジェクトを初期化する
```java
//アウトラインクラスオブジェクトを初期化する
Outline outline = new Outline();
```
## ステップ 4:OutlineElement クラス オブジェクトを初期化する
```java
//OutlineElementクラスオブジェクトを初期化する
OutlineElement outlineElem = new OutlineElement();
```
## ステップ 5: 画像をロードして挿入する
```java
//画像をロードする
Image image = new Image(null, dataDir + "Input.jpg");
//ドキュメントノードに画像を挿入する
outlineElem.appendChildLast(image);
```
## ステップ 6: 画像にメモタグを追加する
```java
//画像に黄色の星メモタグを追加します
NoteTag noteTag = NoteTag.createYellowStar();
image.getTags().add(noteTag);
```
## ステップ 7: アウトライン要素ノードを追加する
```java
//アウトライン要素ノードを追加
outline.appendChildLast(outlineElem);
```
## ステップ 8: アウトライン ノードを追加する
```java
//アウトラインノードを追加
page.appendChildLast(outline);
```
## ステップ 9: ページノードの追加
```java
//ページノードを追加
doc.appendChildLast(page);
```
## ステップ 10: OneNote ドキュメントを保存する
```java
//OneNote ドキュメントを PDF として保存する
doc.save(dataDir + "AddNewImageNodeWithTag_out.pdf", SaveFormat.Pdf);
```
おめでとう！ Aspose.Note for Java を使用して、OneNote にタグ付きの新しい画像ノードが正常に追加されました。
## 結論
 Aspose.Note for Java をマスターすると、OneNote ドキュメント操作の素晴らしい可能性が広がります。このチュートリアルに従うことで、さまざまなプロジェクトに適用できる実践的なスキルを習得できます。 Aspose.Note ドキュメントを引き続き探索してください[ここ](https://reference.aspose.com/note/java/)より高度な機能と可能性を実現します。
## よくある質問
### Aspose.Note のドキュメントはどこで見つけられますか?
ドキュメントを見つけることができます[ここ](https://reference.aspose.com/note/java/).
### Aspose.Note for Java をダウンロードするにはどうすればよいですか?
リリースページからダウンロードできます[ここ](https://releases.aspose.com/note/java/).
### 無料トライアルはありますか?
はい、無料トライアルにアクセスできます[ここ](https://releases.aspose.com/).
### Aspose.Note のサポートはどこで入手できますか?
コミュニティフォーラムにアクセスしてください[ここ](https://forum.aspose.com/c/note/28)サポートのための。
### 仮免許は必要ですか?
必要に応じて、一時ライセンスを取得できます[ここ](https://purchase.aspose.com/temporary-license/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
