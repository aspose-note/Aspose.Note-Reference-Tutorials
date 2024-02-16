---
title: OneNote ドキュメントのテーブルから行テキストを抽出する - Aspose.Note
linktitle: OneNote ドキュメントのテーブルから行テキストを抽出する - Aspose.Note
second_title: Aspose.Note Java API
description: Aspose.Note for Java を使用して、OneNote テーブルから行テキストを簡単に抽出する方法を学びます。シームレスな統合については、ステップバイステップのガイドに従ってください。
type: docs
weight: 13
url: /ja/java/onenote-table-manipulation/extract-row-text-from-table/
---
## 導入
Aspose.Note for Java を使用して OneNote ドキュメントの表から行テキストを抽出するためのこの包括的なチュートリアルへようこそ。 Aspose.Note は、開発者が Microsoft OneNote ファイルをシームレスに操作できるようにする強力な Java ライブラリです。このチュートリアルでは、OneNote ドキュメント内の表から行テキストを効率的に抽出する方法を示しながら、プロセスを段階的に説明します。
## 前提条件
チュートリアルに入る前に、次の前提条件が満たされていることを確認してください。
-  Aspose.Note for Java ライブラリ: Aspose.Note for Java ライブラリがインストールされていることを確認します。からダウンロードできます。[ダウンロードリンク](https://releases.aspose.com/note/java/).
- Java 開発環境: マシン上に Java 開発環境がセットアップされていることを確認してください。
- OneNote ドキュメント: 行テキストを抽出するテーブルを含むサンプル OneNote ドキュメント (例: 「Sample1.one」) を準備します。
## パッケージのインポート
Java プロジェクトで、必要な Aspose.Note パッケージをインポートします。これにより、OneNote ドキュメントの操作に必要なクラスとメソッドに確実にアクセスできるようになります。
```java
import java.io.IOException;
import java.util.List;
import java.util.stream.Collectors;
import com.aspose.note.Document;
import com.aspose.note.LoadOptions;
import com.aspose.note.RichText;
import com.aspose.note.Table;
import com.aspose.note.TableRow;
```
## ステップ 1: ドキュメント ディレクトリを設定する
```java
//ドキュメントディレクトリへのパス。
String dataDir = "Your Document Directory";
```
## ステップ 2: OneNote ドキュメントをロードする
```java
//ドキュメントを Aspose.Note にロードします。
Document document = new Document(dataDir + "Sample1.one", new LoadOptions());
```
## ステップ 3: テーブル ノードを取得する
```java
//テーブルノードのリストを取得する
List<Table> nodes = (List<Table>) document.getChildNodes(Table.class);
```
## ステップ 4: テーブルと行を反復処理する
```java
//行数を設定する
int rowCount = 0;
for (Table table : nodes) {
    //テーブルの行を反復処理する
    for (TableRow row : table) {
        rowCount++;
        //テキストの取得
        List<RichText> textNodes = (List<RichText>) row.getChildNodes(RichText.class);
        StringBuilder text = new StringBuilder();
        for (RichText richText : textNodes) {
            text = text.append(richText.getText().toString());
        }
        //出力画面にテキストを印刷する
        System.out.println(text);
    }
}
```
OneNote ドキュメント内のテーブルごとにこれらの手順を繰り返すと、行テキストが正常に抽出されます。
## 結論
おめでとう！ Aspose.Note for Java を使用して、OneNote ドキュメントの表から行テキストを抽出する方法を学習しました。このチュートリアルは、Java アプリケーションで Aspose.Note の強力な機能を活用するための基礎を提供します。
## よくある質問
### Aspose.Note は Microsoft OneNote の最新バージョンと互換性がありますか?
 Aspose.Note は、最新のものを含むさまざまな OneNote バージョンをサポートしています。を参照してください。[ドキュメンテーション](https://reference.aspose.com/note/java/)互換性の詳細については。
### 購入する前に、Aspose.Note for Java を試してみることはできますか?
はい、Aspose.Note の無料トライアルを次の場所で試すことができます。[このリンク](https://releases.aspose.com/).
### 追加のサポートや支援はどこで入手できますか?
訪問[Aspose.Note フォーラム](https://forum.aspose.com/c/note/28)コミュニティのサポートとディスカッションのために。
### Aspose.Note の一時ライセンスを取得するにはどうすればよいですか?
から一時ライセンスを取得します[このリンク](https://purchase.aspose.com/temporary-license/).
### Aspose.Note for Java を使用するための特定のシステム要件はありますか?
詳細なシステム要件については、ドキュメントを参照してください。