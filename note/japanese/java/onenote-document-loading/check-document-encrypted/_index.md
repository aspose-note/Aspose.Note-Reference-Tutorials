---
title: OneNote ドキュメントが暗号化されているかどうかを確認する - Java
linktitle: OneNote ドキュメントが暗号化されているかどうかを確認する - Java
second_title: Aspose.Note Java API
description: Aspose.Note を使用して Java で OneNote ドキュメントが暗号化されているかどうかを確認する方法を学習します。効率的に文書を処理するには、ステップバイステップのガイドに従ってください。
type: docs
weight: 10
url: /ja/java/onenote-document-loading/check-document-encrypted/
---
## 導入

Java で OneNote ドキュメントを操作する場合、処理前にドキュメントが暗号化されていないことを確認することが重要です。ドキュメントを暗号化すると、セキュリティ層がさらに強化されますが、正しく処理されないと処理手順が複雑になる可能性もあります。このチュートリアルでは、Aspose.Note for Java を使用して OneNote ドキュメントが暗号化されているかどうかを確認するプロセスを説明します。

## 前提条件

始める前に、次の前提条件が満たされていることを確認してください。

1.  Java Development Kit (JDK): システムに Java がインストールされていることを確認してください。からダウンロードできます[ここ](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).

2. Aspose.Note for Java ライブラリ: Aspose.Note for Java ライブラリをダウンロードしてセットアップします。ダウンロードリンクが見つかります[ここ](https://releases.aspose.com/note/java/).

## パッケージのインポート

まず、必要なパッケージを Java プロジェクトにインポートします。

```java
import com.aspose.note.Document;
import com.aspose.note.LoadOptions;
import java.io.FileInputStream;
import java.io.IOException;
import java.nio.file.Paths;
```

プロセスを複数のステップに分けてみましょう。

## ステップ 1: ストリームからのドキュメントが暗号化されているかどうかを確認する

```java
public static void CheckIfDocumentFromStreamIsEncrypted() throws IOException {
    //ExStart:CheckIfDocumentFromStreamIsEncrypted
    String dataDir = "Your Document Directory";

    LoadOptions loadOptions = new LoadOptions();
    loadOptions.setDocumentPassword("password");

    FileInputStream stream = new FileInputStream(Paths.get(dataDir, "Sample1.one").toString());

    try {
        Document ref[] = { null };
        if (!Document.isEncrypted(stream, loadOptions, ref)) {
            System.out.println("The document is loaded and ready to be processed.");
        } else {
            System.out.println("The document is encrypted. Provide a password.");
        }
    } finally {
        stream.close();
    }
    // ExEnd:CheckIfDocumentFromStreamIsEncrypted
}
```

説明：

- このメソッドは、ストリームからロードされたドキュメントが暗号化されているかどうかを確認します。
- 次を使用してドキュメントのパスワードを設定します`setDocumentPassword`の方法`LoadOptions`クラス。
- の`Document.isEncrypted`メソッドは、ドキュメントが暗号化されているかどうかを判断するために使用されます。

## ステップ 2: ファイルからのドキュメントが暗号化されているかどうかを確認する

```java
public static void CheckIfDocumentFromFileIsEncrypted() throws IOException {
    //ExStart:CheckIfDocumentFromFileIsEncrypted
    String dataDir = "Your Document Directory";

    Document ref[] = { null };
    if (!Document.isEncrypted(Paths.get(dataDir, "Sample1.one").toString(), "VerySecretPassword", ref)) {
        if (ref[0] != null) {
            System.out.println("The document is decrypted. It is loaded and ready to be processed.");
        } else {
            System.out.println("The document is encrypted. Invalid password was provided.");
        }
    } else {
        System.out.println("The document is NOT encrypted. It is loaded and ready to be processed.");
    }
    // ExEnd:CheckIfDocumentFromFileIsEncrypted
}
```

説明：

- このメソッドは、ファイルからロードされたドキュメントが暗号化されているかどうかを確認します。
- それは、`Document.isEncrypted`このメソッドは前のステップと同様ですが、ファイル パスとパスワード パラメーターを使用します。

## 結論

このチュートリアルでは、Aspose.Note を使用して Java で OneNote ドキュメントが暗号化されているかどうかを確認する方法を学習しました。ステップバイステップのガイドに従い、提供されているコード例を利用することで、ドキュメントの暗号化ステータスを効率的に判断し、Java アプリケーションでのスムーズな処理を確保できます。

## よくある質問

### Q1: パスワードを入力せずに暗号化ステータスを確認できますか?

A1: はい、パスワードを入力しなくても暗号化ステータスを確認できます。の`Document.isEncrypted`メソッドを使用するとそれが可能になります。

### Q2: 間違ったパスワードを入力するとどうなりますか?

 A2: 暗号化ステータスを確認するときに間違ったパスワードを入力すると、メソッドは次のエラーを返します。`true`、文書は暗号化されているが、指定されたパスワードが間違っていることを示します。

### Q3: 暗号化されたドキュメントをプログラムで復号化することは可能ですか?

A3: はい、ドキュメントの読み込み時に正しいパスワードを入力することで、暗号化されたドキュメントをプログラムで復号化できます。

### Q4: Aspose.Note を OneNote 以外のドキュメント形式に使用できますか?

A4: いいえ、Aspose.Note は OneNote ドキュメントのみを操作するために特別に設計されています。

### Q5: Aspose.Note for Java のその他のリソースとサポートはどこで入手できますか?

 A5: をご覧いただけます。[Aspose.Note フォーラム](https://forum.aspose.com/c/note/28)コミュニティのサポートとドキュメントのために。