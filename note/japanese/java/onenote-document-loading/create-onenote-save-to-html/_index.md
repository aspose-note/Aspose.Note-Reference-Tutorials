---
date: 2026-02-07
description: Aspose.Note for Java を使用して OneNote を HTML として保存する際にフォントをエクスポートする方法を学びましょう。このガイドでは、プログラムで
  OneNote を作成し、フォント、CSS、画像を埋め込む方法を示します。
linktitle: How to Export Fonts When Saving OneNote as HTML – Java
second_title: Aspose.Note Java API
title: OneNoteをHTMLとして保存するときにフォントをエクスポートする方法 – Java
url: /ja/java/onenote-document-loading/create-onenote-save-to-html/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote を HTML として保存する際のフォントエクスポート方法 – Java

## はじめに

このチュートリアルでは、Aspose.Note for Java を使用して **OneNote を HTML として保存する際にフォントをエクスポートする方法** をご紹介します。プログラムで OneNote ドキュメントを作成し、HTML 保存オプションを設定し、必要なフォントファイルを埋め込む手順を解説します。これにより、生成された HTML が元の OneNote ページとまったく同じ外観になるため、Web 向けに視覚的忠実度を保ちたい場合に最適です。

## クイック回答
- **エクスポートを処理するライブラリは？** Aspose.Note for Java  
- **HTML にフォントを埋め込めますか？** はい – `ExportFonts` を `ExportEmbedded` に設定します  
- **本番環境でライセンスは必要ですか？** 商用利用には有効な Aspose.Note ライセンスが必要です  
- **対応している Java バージョンは？** Java 8 以降  
- **リソースを別ファイルに保存できますか？** もちろん – `ResourceExportType` を適切に設定します  

## OneNote HTML 変換の文脈で「フォントをエクスポートする」とは何ですか？

OneNote ノートブックを HTML に変換する際、視覚的な外観は CSS、画像、そして特に元ページで使用されているフォントに依存します。**フォントをエクスポートする** とは、フォントファイル（例: TTF）を HTML パッケージに直接埋め込み、エンドユーザーがローカルにそのフォントをインストールしていなくても、ブラウザが OneNote と同じようにテキストをレンダリングできるようにすることです。

## なぜプログラムで OneNote を作成し、HTML として保存するのか？

- **自動化:** 手動のコピー＆ペーストなしで、レポートやドキュメント、ナレッジベース記事を OneNote から生成できます。  
- **一貫性:** デバイス間でレイアウト、スタイリング、カスタムフォントを保持します。  
- **ポータビリティ:** HTML は普遍的に閲覧可能 – OneNote クライアントは不要です。  

## 前提条件

1. Java Development Kit (JDK) 8 以降がインストールされていること。  
2. Aspose.Note for Java ライブラリ – [こちら](https://releases.aspose.com/note/java/) からダウンロード。  
3. サンプルの OneNote ファイル（`.one`）をロードするか、プログラムで新規作成できること。  

## パッケージのインポート

まず、必要なクラスを Java プロジェクトにインポートします：

```java
import java.io.ByteArrayOutputStream;
import java.io.File;
import java.io.FileOutputStream;
import java.io.IOException;
import java.io.OutputStream;
import java.io.OutputStreamWriter;
import java.nio.file.Paths;
import com.aspose.note.CssSavingArgs;
import com.aspose.note.Document;
import com.aspose.note.FontFaceType;
import com.aspose.note.FontSavingArgs;
import com.aspose.note.HtmlSaveOptions;
import com.aspose.note.ICssSavingCallback;
import com.aspose.note.IFontSavingCallback;
import com.aspose.note.IImageSavingCallback;
import com.aspose.note.ImageSavingArgs;
import com.aspose.note.ResourceExportType;
```

## OneNote を HTML として保存する際にフォントをエクスポートする方法は？

以下は、**フォントのエクスポート** とその他のリソースを示すステップバイステップガイドです。

### ステップ 1: プログラムで OneNote ドキュメントを作成する  

```java
Document document = new Document("Path_to_your_sample_one_file");
```

この行は既存の `.one` ファイルを読み込みます。**プログラムで OneNote を作成したい** 場合は、`Document` オブジェクトを新規にインスタンス化し、API を使ってセクションやページを追加できます（フォントのエクスポートに焦点を当てるため、ここでは省略しています）。

### ステップ 2: 埋め込みフォントでメモリストリームに保存する  

```java
HtmlSaveOptions options = new HtmlSaveOptions();
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);
options.setFontFaceTypes(FontFaceType.Ttf);

ByteArrayOutputStream outputStream = new ByteArrayOutputStream();
document.save(outputStream, options);
```

- `setExportFonts(ResourceExportType.ExportEmbedded)` は Aspose.Note に **フォントを直接 HTML パッケージにエクスポート** させます。  
- `setFontFaceTypes(FontFaceType.Ttf)` により、ブラウザ互換性の高い TrueType フォントが使用されます。

### ステップ 3: 別々のリソースファイルとして HTML を保存する（フォントは引き続きエクスポート）  

```java
HtmlSaveOptions options = new HtmlSaveOptions();
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);

document.save("output_directory/document.html", options);
```

CSS と画像は埋め込まれていますが、`ResourceExportType` を `ExportExternal` に変更すれば、キャッシュしやすい外部ファイルとして保存できます。重要なのは **フォントのエクスポート** が変わらないことです。

### ステップ 4: コールバックを使用して各リソースの保存場所を制御する  

```java
Document document = new Document("Path_to_your_sample_one_file");

UserSavingCallbacks savingCallbacks = new UserSavingCallbacks();
savingCallbacks.setRootFolder("documentFolder");
savingCallbacks.setCssFolder("css");
savingCallbacks.setKeepCssStreamOpened(true);
savingCallbacks.setImagesFolder("images");
savingCallbacks.setFontsFolder("fonts");

HtmlSaveOptions options = new HtmlSaveOptions();
options.setFontFaceTypes(FontFaceType.Ttf);
options.setCssSavingCallback(savingCallbacks);
options.setImageSavingCallback(savingCallbacks);
options.setFontSavingCallback(savingCallbacks);
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);

File dir = new File(savingCallbacks.getRootFolder());
if (!dir.exists()) {
    dir.mkdir();
}

document.save(Paths.get(savingCallbacks.getRootFolder(), "document.html").toString(), options);
```

`UserSavingCallbacks` クラス（`ICssSavingCallback`、`IImageSavingCallback`、`IFontSavingCallback` の実装が必要）を使うと、フォルダ構造を自由に決められます。たとえばフォントだけを `fonts` ディレクトリに保存しつつ、**フォントを正しくエクスポート** できます。

## OneNote を HTML に変換する際にカスタムフォントを埋め込む方法

カスタムフォントを埋め込むことで、HTML のレンダリングが元の OneNote レイアウトと一致します。`ExportEmbedded` と `FontFaceType.Ttf` を組み合わせると、TrueType ファイルが Base‑64 エンコードされ、生成された CSS に直接挿入されるため、外部フォントホスティングは不要です。

## ResourceExportType を使用したリソースエクスポートの制御

`ResourceExportType` は CSS、画像、フォントを **HTML 内部に埋め込む** (`ExportEmbedded`) か、**外部ファイルとして保存する** (`ExportExternal`) かを選択できる設定です。単一ファイルが欲しい場合は `ExportEmbedded`、大容量アセットのキャッシュを活用したい場合は `ExportExternal` を選びます。

## HTML エクスポート用にプログラムで OneNote を作成する

最初からコードで OneNote ドキュメントを構築し、セクション・ページ・リッチテキストを追加した後、上記と同じ `HtmlSaveOptions` を適用すれば、データ生成からカスタムフォント埋め込みまでのエンドツーエンド自動化が実現します。

## 一般的な問題とヒント

- **出力にフォントが欠けている:** `setExportFonts(ResourceExportType.ExportEmbedded)` が設定されているか、元の OneNote が埋め込みフォントを使用しているか確認してください。  
- **HTML ファイルが大きくなる:** フォント埋め込みはサイズ増加の要因です。帯域幅が懸念される場合は `ExportFonts` を `ExportExternal` に切り替え、CDN でフォントを配信しましょう。  
- **コールバック実装エラー:** コールバッククラスがストリームを書き込み、リソースを正しくクローズしているか確認し、ファイル破損を防ぎます。  

## よくある質問

**Q: 複数の OneNote ドキュメントを一括で HTML に変換できますか？**  
A: はい、各 `Document` インスタンスをループし、同じ `HtmlSaveOptions` を適用すれば可能です。  

**Q: Aspose.Note for Java は HTML 以外の出力形式もサポートしていますか？**  
A: もちろんです。PDF、DOCX、PNG、JPEG など、適切な保存オプションを使用してエクスポートできます。  

**Q: Aspose.Note for Java の試用版はありますか？**  
A: はい、[こちら](https://releases.aspose.com/) から無料トライアルをダウンロードできます。  

**Q: Aspose.Note for Java のサポートはどこで受けられますか？**  
A: コミュニティと公式サポートは [Aspose.Note フォーラム](https://forum.aspose.com/c/note/28) で提供されています。  

**Q: Aspose.Note for Java のライセンスはどうやって購入できますか？**  
A: ライセンスは [Aspose のウェブサイト](https://purchase.aspose.com/buy) で購入可能です。  

## 結論

これで、Aspose.Note for Java を使用して **OneNote を HTML として保存する際にフォントをエクスポートする方法** が分かりました。`HtmlSaveOptions` を設定し、必要に応じてコールバックを利用すれば、カスタムフォントを含む OneNote ページの外観を Web 上で正確に再現できます。プロジェクトのパフォーマンスやストレージ要件に合わせて、`ResourceExportType` の設定を調整してみてください。

---

**最終更新日:** 2026-02-07  
**テスト環境:** Aspose.Note for Java 24.12  
**作者:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}