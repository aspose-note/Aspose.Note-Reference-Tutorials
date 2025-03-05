---
title: Aspose.Note のテンプレートからドキュメントを生成
linktitle: Aspose.Note のテンプレートからドキュメントを生成
second_title: Aspose.Note .NET API
description: Aspose.Note for .NET を使用すると、動的なドキュメントを簡単に生成できます。パーソナライズされたデータ主導のドキュメント作成については、ステップバイステップのガイドに従ってください。
type: docs
weight: 18
url: /ja/net/text-manipulation/generate-document-from-template/
---
## 導入
進化し続けるドキュメント作成環境において、Aspose.Note for .NET は、動的なドキュメントを簡単に生成するための強力なツールとして際立っています。レポート、請求書、または個人用ドキュメントを扱う場合でも、このチュートリアルでは、Aspose.Note for .NET を使用してテンプレートからドキュメントを生成するプロセスを説明します。
## 前提条件
ステップバイステップ ガイドに進む前に、次の前提条件が満たされていることを確認してください。
1.  Aspose.Note for .NET ライブラリ: からライブラリをダウンロードしてインストールします。[Aspose.Note for .NET ドキュメント](https://reference.aspose.com/note/net/).
2. ドキュメント テンプレート: OneNote 形式 (拡張子 .one) のテンプレート ドキュメントを準備します。これは、動的に生成されるドキュメントの基礎として機能します。
## 名前空間のインポート
必要な名前空間をプロジェクトに必ず含めてください。
```csharp
    using System;
    using System.Collections.Generic;
    using System.IO;
```
ここで、ガイドの各ステップを詳しく見てみましょう。
## ステップ 1: ドキュメント ディレクトリを定義する
```csharp
string dataDir = "Your Document Directory";
```
「Your Document Directory」を、生成されたドキュメントを保存するパスに置き換えます。
## ステップ 2: 置換値を含む辞書を作成する
```csharp
var templateData = new Dictionary<string, string>
{
    { "Company", "Atlas Shrugged Ltd" },
    { "CandidateName", "John Galt" },
    { "JobTitle", "Chief Entrepreneur Officer" },
    { "Department", "Sales" },
    { "Salary", "123456 USD" },
    { "Vacation", "30" },
    { "StartDate", "29 Feb 2024" },
    { "YourName", "Ayn Rand" }
};
```
キーがテンプレート内のプレースホルダーであり、値がそれらを置き換えるデータであるディクショナリを定義します。

## ステップ 3: テンプレート ドキュメントをロードする
```csharp
var templateDocument = new Document(Path.Combine(dataDir, "JobOffer.one"));
```
OneNote テンプレート ドキュメントを Aspose.Note に読み込みます。

## ステップ 4: テンプレートの単語を動的データに置き換える
```csharp
foreach (var paragraph in templateDocument.GetChildNodes<RichText>())
{
    foreach (var replacement in templateData)
    {
        paragraph.Replace($"${{{replacement.Key}}}", replacement.Value);
    }
}
```
テンプレート内の各段落を反復処理して、プレースホルダーを動的データに置き換えます。

## ステップ 5: 生成されたドキュメントを保存する
```csharp
templateDocument.Save(Path.Combine(dataDir, "JobOffer_out.one"));
```
動的に生成されたドキュメントを指定したディレクトリに保存します。

## 結論
おめでとう！ Aspose.Note for .NET を使用して動的ドキュメントを生成することに成功しました。このプロセスにより、パーソナライズされたデータ駆動型のドキュメントをシームレスに作成する可能性が広がります。

## よくある質問
### Aspose.Note for .NET を他のドキュメント形式で使用できますか?
はい、Aspose.Note for .NET は主に OneNote ドキュメントを扱いますが、Aspose はさまざまな形式に対応するさまざまなライブラリを提供します。
### Aspose.Note for .NET に利用できる無料トライアルはありますか?
はい、無料トライアルで Aspose.Note for .NET の機能を試すことができます。訪問[ここ](https://releases.aspose.com/)詳細については。
### Aspose.Note for .NET のサポートを受けるにはどうすればよいですか?
訪問[Aspose.Note for .NET フォーラム](https://forum.aspose.com/c/note/28)コミュニティや専門家からの支援が得られます。
### Aspose.Note for .NET の一時ライセンスは利用できますか?
はい、一時ライセンスを取得できます[ここ](https://purchase.aspose.com/temporary-license/)テストと評価の目的で。
### Aspose.Note for .NET の包括的なドキュメントはどこで見つけられますか?
を参照してください。[ドキュメンテーション](https://reference.aspose.com/note/net/) Aspose.Note for .NET の使用に関する詳細については、「Aspose.Note for .NET」を参照してください。