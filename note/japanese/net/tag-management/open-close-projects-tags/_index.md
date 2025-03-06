---
title: Aspose.Note でタグ付きプロジェクトを開いたり閉じたりする
linktitle: Aspose.Note でタグ付きプロジェクトを開いたり閉じたりする
second_title: Aspose.Note .NET API
description: Aspose.Note for .NET を使用して Microsoft OneNote ファイルをプログラムで操作する方法を学びます。タグを使用してプロジェクトを開いたり閉じたりするのを効率的に行います。
weight: 15
url: /ja/net/tag-management/open-close-projects-tags/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Note でタグ付きプロジェクトを開いたり閉じたりする

## 導入

このチュートリアルでは、Aspose.Note for .NET を使用して、タグを含むプロジェクトを開いたり閉じたりする方法を学びます。 Aspose.Note は、開発者がプログラムで Microsoft OneNote ファイルを操作できるようにする強力な API で、ドキュメント内のテキスト、画像、タグの操作などのタスクを可能にします。

## 前提条件

始める前に、次の前提条件が設定されていることを確認してください。

## 名前空間のインポート

```csharp
using System.IO;
using System.Linq;
```

次に、各例を複数のステップに分けてみましょう。

## ステップ 1: ドキュメントをロードする

まず、ドキュメントを Aspose.Note にロードする必要があります。

```csharp
string dataDir = "Your Document Directory";
var oneFile = new Document(Path.Combine(dataDir, "ProjectNotes.one"));
```

## ステップ 2: プロジェクト C アイテムを閉じる

ここで、「プロジェクト C」に関連するすべてのチェックボックス項目を閉じましょう。

```csharp
foreach (var node in oneFile.GetChildNodes<ITaggable>())
{
    foreach (var checkBox in node.Tags.OfType<CheckBox>())
    {
        if (checkBox.Label.Contains("Project C") && !checkBox.Checked)
        {
            checkBox.SetCompleted();
        }
    }
}
```

## ステップ 3: 閉じたプロジェクト C のメモを保存する

閉じた「プロジェクト C」項目を含む変更されたドキュメントを保存します。

```csharp
oneFile.Save("Path to save the closed Project C notes");
```

## ステップ 4: プロジェクト C アイテムを開く

次に、「プロジェクト C」に関連するすべてのチェックボックス項目を開きます。

```csharp
var oneFile = new Document("Path to the closed Project C notes");

foreach (var node in oneFile.GetChildNodes<ITaggable>())
{
    foreach (var checkBox in node.Tags.OfType<CheckBox>())
    {
        if (checkBox.Label.Contains("Project C") && checkBox.Checked)
        {
            checkBox.SetOpen();
        }
    }
}
```

## ステップ 5: 開いているプロジェクト C のメモを保存する

開いた「プロジェクト C」項目を含む変更されたドキュメントを保存します。

```csharp
oneFile.Save(Path.Combine(dataDir, "ProjectNoteWithOpenProjectC.one"));
```

これで、.NET を使用して Aspose.Note でタグを含むプロジェクトを開いたり閉じたりする方法を学習しました。

## 結論

Aspose.Note for .NET は、OneNote ドキュメントをプログラムで操作する便利な方法を提供します。このチュートリアルに従うと、タグを使用して項目を開いたり閉じたりすることで、プロジェクトを効率的に管理できます。

## よくある質問

### Q1: Aspose.Note は OneNote のすべてのバージョンと互換性がありますか?

A1: Aspose.Note は Microsoft OneNote 2010 以降のバージョンをサポートしています。

### Q2: Aspose.Note を商用プロジェクトに使用できますか?

 A2: はい、Aspose.Note は個人プロジェクトと商用プロジェクトの両方に使用できます。訪問[ここ](https://purchase.aspose.com/buy)ライセンスを購入するため。

### Q3: Aspose.Note には無料トライアルがありますか?

 A3: はい、無料トライアルを利用できます。[ここ](https://releases.aspose.com/).

### Q4: Aspose.Note のドキュメントはどこで見つけられますか?

 A4: ドキュメントは見つかります。[ここ](https://reference.aspose.com/note/net/).

### Q5: Aspose.Note のサポートはどこで受けられますか?

 A5: サポートが必要な場合は、Aspose.Note にアクセスしてください。[フォーラム](https://forum.aspose.com/c/note/28).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
