---
title: Aspose.Note'ta Etiketli Görüntü Düğümü Ekleme
linktitle: Aspose.Note'ta Etiketli Görüntü Düğümü Ekleme
second_title: Aspose.Note .NET API'si
description: Aspose.Note for .NET'i kullanarak özel etiketlere sahip görüntüler ekleyerek OneNote belgelerinizi nasıl geliştireceğinizi öğrenin.
weight: 10
url: /tr/net/tag-management/add-image-node-tag/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Note'ta Etiketli Görüntü Düğümü Ekleme

## giriiş

Bu eğitimde Aspose.Note for .NET kullanarak etiketli bir görüntü düğümünün nasıl ekleneceğini inceleyeceğiz. Bu özellik, özel etiketlere sahip resimler ekleyerek OneNote belgelerinizi geliştirmenize olanak tanır.

## Önkoşullar

Başlamadan önce aşağıdakilere sahip olduğunuzdan emin olun:

1. Visual Studio: Sisteminize Visual Studio IDE'yi yükleyin.
2.  Aspose.Note for .NET: Aspose.Note for .NET kitaplığını indirip yükleyin.[İndirme: {link](https://releases.aspose.com/note/net/).
3. Temel Bilgi: C# programlama dili ve .NET çerçevesine aşina olun.

## Ad Alanlarını İçe Aktar

Öncelikle C# kodunuza gerekli ad alanlarını eklediğinizden emin olun:

```csharp
using System.Drawing;
using System.IO;
using Aspose.Note;
using System;
using System.Collections.Generic;
```

## Adım 1: Belge ve Sayfa Nesnelerini Başlatın

 Bir örneğini oluşturarak başlayın`Document` sınıf ve bir`Page` nesne:

```csharp
Document doc = new Document();
Aspose.Note.Page page = new Aspose.Note.Page(doc);
```

## Adım 2: Outline ve OutlineElement Nesnelerini Başlatın

 Sonra, başlat`Outline` Ve`OutlineElement` nesneler:

```csharp
Outline outline = new Outline(doc);
OutlineElement outlineElem = new OutlineElement(doc);
```

## 3. Adım: Görüntüyü Yükleyin ve Ekleyin

İstediğiniz görüntüyü yükleyin ve belge düğümüne ekleyin:

```csharp
Aspose.Note.Image image = new Aspose.Note.Image(doc, "path_to_your_image.jpg");
outlineElem.AppendChildLast(image);
```

## Adım 4: Resme Etiket Ekleme

Resme özel bir etiket ekleyin:

```csharp
image.Tags.Add(NoteTag.CreateYellowStar());
```

## Adım 5: Anahat Öğesini ve Sayfa Düğümlerini Ekleme

Anahat öğesini ve anahat düğümlerini sayfaya ekleyin:

```csharp
outline.AppendChildLast(outlineElem);
page.AppendChildLast(outline);
```

## Adım 6: Belgeyi Kaydedin

Değiştirilen OneNote belgesini kaydedin:

```csharp
doc.AppendChildLast(page);
string outputFilePath = "output_path/AddImageNodeWithTag_out.one";
doc.Save(outputFilePath);
```

## Çözüm

Bu adımları izleyerek Aspose.Note for .NET'i kullanarak özel etiketli bir görüntü düğümünü sorunsuz bir şekilde ekleyebilir, OneNote belgelerinizi kişiselleştirilmiş görsellerle zenginleştirebilirsiniz.

## SSS'ler

### S1: Aspose.Note'u kullanarak tek bir belgeye farklı etiketlere sahip birden fazla görsel ekleyebilir miyim?

Cevap1: Evet, her görsel için benzer adımları izleyerek farklı etiketlere sahip birden fazla görsel ekleyebilirsiniz.

### S2: Aspose.Note, OneNote'un tüm sürümleriyle uyumlu mudur?

Cevap2: Aspose.Note, OneNote'un çeşitli sürümlerini destekleyerek farklı ortamlar arasında uyumluluk sağlar.

### S3: Resme eklenen etiketin görünümünü özelleştirebilir miyim?

Cevap3: Evet, Aspose.Note, etiket görünümünü tercihlerinize uyacak şekilde özelleştirme konusunda esneklik sağlar.

### S4: Aspose.Note, URL'lerden görsel ekleme desteği sunuyor mu?

Cevap4: Aspose.Note öncelikle yerel dizinlerden görsel eklemeyi destekler, ancak harici görselleri önce yerel olarak indirerek dahil edebilirsiniz.

### S5: Eklenebilecek görsellerin boyutu veya formatıyla ilgili herhangi bir sınırlama var mı?

Cevap5: Aspose.Note çok çeşitli görüntü formatlarını destekler ve görüntü boyutuna katı sınırlamalar getirmez; bu da belgelerinize çeşitli görseller eklemenize olanak tanır.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
