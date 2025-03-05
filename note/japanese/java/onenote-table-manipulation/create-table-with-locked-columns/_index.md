---
title: OneNote でロックされた列を含むテーブルを作成する - Aspose.Note
linktitle: OneNote でロックされた列を含むテーブルを作成する - Aspose.Note
second_title: Aspose.Note Java API
description: Aspose.Note for Java を使用して OneNote エクスペリエンスを強化します。ステップバイステップのガイドを使用して、ロックされた列を含むテーブルを作成する方法を学びます。今すぐ無料トライアルをダウンロードしてください!
type: docs
weight: 12
url: /ja/java/onenote-table-manipulation/create-table-with-locked-columns/
---
## 導入
OneNote は情報を整理するための強力なツールであり、Aspose.Note for Java はロックされた列を含むテーブルをシームレスに作成する方法を提供することでその機能を強化しています。このチュートリアルでは、Aspose.Note for Java を使用して、ロックされた列を含むテーブルを OneNote に作成するプロセスを説明します。
## 前提条件
始める前に、次の前提条件が満たされていることを確認してください。
- [Java 開発キット (JDK)](https://www.oracle.com/java/technologies/javase-downloads.html)あなたのマシンにインストールされています。
- [Java 用 Aspose.Note](https://downloads.aspose.com/note/java)ライブラリがダウンロードされ、プロジェクトに追加されます。
## パッケージのインポート
Java プロジェクトで、Aspose を使用するために必要なパッケージをインポートします。注:
```java
import com.aspose.note.*;
import java.io.IOException;
```
## ステップ 1: プロジェクトをセットアップする
まず、新しい Java プロジェクトを作成し、Aspose.Note ライブラリをクラスパスに追加します。プロジェクトが JDK を使用するように構成されていることを確認してください。
## ステップ 2: ドキュメントとページのオブジェクトを初期化する
```java
//ドキュメントディレクトリへのパス。
String dataDir = "Your Document Directory";
//Documentクラスのオブジェクトを作成する
Document doc = new Document();
// Pageクラスオブジェクトの初期化
Page page = new Page();
```
## ステップ 3: テーブルの行とセルを作成する
```java
//TableRowクラスオブジェクトを初期化する
TableRow row1 = new TableRow();
//TableCell クラス オブジェクトを初期化し、テキスト コンテンツを設定します。
TableCell cell11 = new TableCell();
cell11.appendChildLast(InsertTable.GetOutlineElementWithText("Small text"));
row1.appendChildLast(cell11);
//TableRowクラスオブジェクトを初期化する
TableRow row2 = new TableRow();
//TableCell クラス オブジェクトを初期化し、テキスト コンテンツを設定します。
TableCell cell21 = new TableCell();
cell21.appendChildLast(InsertTable.GetOutlineElementWithText("Long   text    with    several   words and    spaces."));
row2.appendChildLast(cell21);
```
## ステップ 4: テーブルの作成とカスタマイズ
```java
//Tableクラスオブジェクトの初期化
Table table = new Table();
table.setBordersVisible(true);
TableColumn col = new TableColumn();
col.setWidth(200);
col.setLockedWidth(true);
table.getColumns().addItem(col);
//行を追加する
table.appendChildLast(row1);
table.appendChildLast(row2);
```
## ステップ 5: アウトラインとページに表を追加する
```java
Outline outline = new Outline();
OutlineElement outlineElem = new OutlineElement();
//テーブルノードの追加
outlineElem.appendChildLast(table);
//アウトライン要素ノードの追加
outline.appendChildLast(outlineElem);
//アウトラインノードを追加
page.appendChildLast(outline);
//ページノードの追加
doc.appendChildLast(page);
```
## ステップ 6: ドキュメントを保存する
```java
dataDir = dataDir + "CreateTableWithLockedColumns_out.one";
doc.save(dataDir);
```
おめでとう！ Aspose.Note for Java を使用して、OneNote でロックされた列を含むテーブルを正常に作成できました。
## 結論
このチュートリアルでは、Aspose.Note for Java を利用して、ロックされた列を含むテーブルを作成することで OneNote エクスペリエンスを向上させるプロセスについて説明しました。この機能により、メモに組織と構造の新しい層が追加されます。
## よくある質問
### Aspose.Note for Java はすべての Java バージョンと互換性がありますか?
はい、Aspose.Note for Java は Java 6 以降のバージョンと互換性があります。
### テーブルの外観をさらにカスタマイズできますか?
絶対に！ Aspose.Note for Java には、境界線やセル間隔の調整など、テーブルをカスタマイズするための広範なオプションが用意されています。
### 購入前に利用できる試用版はありますか?
はい、できます[無料試用版をダウンロードする](https://releases.aspose.com/)Aspose.Note for Java の機能を探索します。
### 追加のサポートやコミュニティのディスカッションはどこで見つけられますか?
訪問[Aspose.Note フォーラム](https://forum.aspose.com/c/note/28)サポートとコミュニティのディスカッションのために。
### Aspose.Note for Java の一時ライセンスを取得するにはどうすればよいですか?
訪問[このリンク](https://purchase.aspose.com/temporary-license/)テスト目的で一時ライセンスを取得します。