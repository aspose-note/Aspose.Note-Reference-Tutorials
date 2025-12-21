---
date: 2025-12-21
description: Aspose.Note for Java を使用して Java で OneNote ドキュメントに画像を追加する方法を学びましょう。画像の挿入手順と、必要に応じて
  OneNote を PDF として保存する方法をステップバイステップでご案内します。
linktitle: Insert an Image in OneNote Document with Java
second_title: Aspose.Note Java API
title: Java を使用して OneNote に画像を追加する方法
url: /ja/java/onenote-hyperlinks-images/insert-image/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# JavaでOneNoteドキュメントに画像を挿入する

## Introduction

このチュートリアルでは、Aspose.Note for Java を使用して Java で OneNote ドキュメントに画像を挿入する方法を解説します。Aspose.Note for Java は、Microsoft OneNote ファイルをプログラムから操作できる強力なライブラリで、作成・読み取り・編集などさまざまな操作が可能です。

## Quick Answers
- **What is the easiest way to add image to OneNote using Java?**  
  Aspose.Note for Java の `Image` クラスを使用し、ページに追加します。
- **Do I need a license for production use?**  
  はい、商用環境で使用する場合は商用ライセンスが必要です。
- **Can I set custom dimensions for the image?**  
  もちろんです。`Image` オブジェクトの `setWidth()` と `setHeight()` を呼び出します。
- **Is it possible to save the OneNote file as PDF after adding the image?**  
  はい、`save(..., SaveFormat.Pdf)` を呼び出すことで **OneNote を PDF として保存** できます。
- **Which Java version is supported?**  
  Aspose.Note for Java は JDK 8 以降で動作します。

## How to add image to OneNote using Java?

コードに入る前に、なぜプログラムで OneNote に画像を埋め込む必要があるのかを簡単に説明します。会議の議事録作成、レポートの自動生成、ドキュメントパイプラインの構築など、画像を挿入することでテキストだけでは伝えきれない視覚的コンテキストを提供できます。Aspose.Note for Java を使えば、OneNote の UI を開くことなくコードだけでこれらを実現できます。

## Prerequisites

開始する前に、以下の前提条件が整っていることを確認してください。

### 1. Java Development Kit (JDK)
システムに Java Development Kit (JDK) がインストールされていることを確認します。Oracle のウェブサイトから JDK をダウンロードしてインストールできます。

### 2. Aspose.Note for Java Library
[Aspose.Note for Java のドキュメント](https://reference.aspose.com/note/java/) に従ってライブラリをダウンロードし、設定してください。

## Import Packages

まず、Java プロジェクトに必要なパッケージをインポートします。これらには Aspose.Note ライブラリとその他の依存関係が含まれます。

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.HorizontalAlignment;
import com.aspose.note.Image;
import com.aspose.note.LoadOptions;
import com.aspose.note.Page;
import com.aspose.note.SaveFormat;
```

画像を OneNote ドキュメントに挿入する手順を複数のステップに分けて解説します。

## Step 1: Load the OneNote Document

画像を挿入したい OneNote ドキュメントを読み込みます。

```java
LoadOptions options = new LoadOptions();
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Sample1.one", options);
```

## Step 2: Get the Page

画像を挿入したいページを取得します。

```java
Page page = oneFile.getFirstChild();
```

## Step 3: Load the Image

OneNote に挿入する画像を読み込みます。

```java
Image image = new Image(oneFile, dataDir + "Input.jpg");
```

## Step 4: Customize Image Attributes (Optional)

必要に応じて画像のサイズ、位置、配置をカスタマイズできます。ここで **Java スタイルで画像の寸法を設定** します。

```java
image.setWidth(100);
image.setHeight(100);
image.setVerticalOffset(400);
image.setHorizontalOffset(100);
image.setAlignment(HorizontalAlignment.Right);
```

## Step 5: Add Image to the Page

ページに画像を追加します。

```java
page.appendChildLast(image);
```

## Step 6: Save the Document

画像を挿入したドキュメントを保存します。この段階で **OneNote を PDF として保存** することも可能です。

```java
try {
    oneFile.save(dataDir + "InsertanImage_out.pdf", SaveFormat.Pdf);
} catch (IOException e) {
    e.printStackTrace();
}
```

## Conclusion

本チュートリアルでは、Aspose.Note for Java ライブラリを活用して Java で OneNote ドキュメントに画像を挿入する方法を学びました。ステップバイステップの手順に従うだけで、プログラムから簡単に画像を組み込むことができます。

## FAQ's

### Q1: Can I insert multiple images into a single OneNote document using this method?

A1: はい、各画像ごとに本チュートリアルの手順を繰り返すことで、1つの OneNote ドキュメントに複数の画像を挿入できます。

### Q2: Is Aspose.Note for Java compatible with all versions of OneNote?

A2: Aspose.Note for Java は Microsoft OneNote 2010 以降で作成された OneNote ファイルの操作をサポートしています。

### Q3: Can I insert images of different formats, such as PNG or GIF, into a OneNote document?

A3: はい、PNG、JPEG、GIF などさまざまな形式の画像を Aspose.Note for Java で挿入できます。

### Q4: Is there a trial version of Aspose.Note for Java available for testing purposes?

A4: はい、評価用に Aspose.Note for Java の無料トライアル版をウェブサイトからダウンロードできます。

### Q5: How can I get technical support for Aspose.Note for Java?

A5: Aspose.Note 製品専用の [フォーラム](https://forum.aspose.com/c/note/28) から技術サポートを受けられます。

---

**Last Updated:** 2025-12-21  
**Tested With:** Aspose.Note for Java 24.10  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}