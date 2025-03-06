---
title: PDF Belgelerini Aspose.Note'a aktarın
linktitle: PDF Belgelerini Aspose.Note'a aktarın
second_title: Aspose.Note .NET API'si
description: Sorunsuz entegrasyon için çeşitli birleştirme seçeneklerini kullanarak PDF belgelerini Aspose.Note for .NET'e zahmetsizce nasıl aktaracağınızı öğrenin.
weight: 10
url: /tr/net/import/import-pdf-documents/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PDF Belgelerini Aspose.Note'a aktarın

## giriiş

Günümüzde mevcut olan çok sayıda dijital içerik göz önüne alındığında, PDF belgelerini projelerinize sorunsuz bir şekilde entegre etmek çok önemlidir. Aspose.Note for .NET, PDF belgelerini verimli bir şekilde içe aktarmak için güçlü işlevler sağlar. Bu eğitimde, Aspose.Note for .NET'i kullanarak PDF belgelerinin adım adım nasıl içe aktarılacağını inceleyeceğiz.

## Önkoşullar

Eğiticiye dalmadan önce aşağıdakilere sahip olduğunuzdan emin olun:

1.  Aspose.Note for .NET: Kitaplığı şuradan indirip yükleyin:[Burada](https://releases.aspose.com/note/net/).
2. Temel C# ve .NET Framework bilgisi: C# programlama dili ve .NET Framework'ün anlaşılması faydalı olacaktır.

## Ad Alanlarını İçe Aktar

PDF içe aktarma işlevi için gereken sınıflara ve yöntemlere erişmek için gerekli ad alanlarını içe aktardığınızdan emin olun:

```csharp
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;

using Aspose.Note.Importing;

```

## 1. Adım: Basit Birleştirmeyi kullanarak PDF Belgelerini içe aktarın

Basit Birleştirme yaklaşımı, birden fazla PDF belgesindeki tüm sayfaların sayfa sayfa içe aktarılmasına olanak tanır:

```csharp
public static void ImportSetOfFiles_SimpleMerge()
{
    string dataDir = "Your Document Directory";

    var d = new Document();

    d.Import(Path.Combine(dataDir, "sampleText.pdf"))
     .Import(Path.Combine(dataDir, "sampleImage.pdf"))
     .Import(Path.Combine(dataDir, "sampleTable.pdf"));

    d.Save(Path.Combine(dataDir, "sample_SimpleMerge.one"));

    Console.WriteLine("\nThe PDF documents are imported successfully.");
}
```

## 2. Adım: Yapılandırılmış Birleştirmeyi kullanarak PDF Belgelerini İçe Aktarın

Yapılandırılmış Birleştirme, her belgedeki sayfaları üst düzey OneNote sayfasının alt öğeleri olarak eklerken PDF belgelerindeki tüm sayfaları içe aktarır:

```csharp
public static void ImportSetOfFiles_StructuredMerge()
{
    string dataDir = "Your Document Directory";

    var d = new Document();

    foreach (var file in new[] { "sampleText.pdf", "sampleImage.pdf", "sampleTable.pdf" })
    {
        d.AppendChildLast(new Page()).Title = new Title() { TitleText = new RichText() { ParagraphStyle = ParagraphStyle.Default }.Append(file) };
        d.Import(Path.Combine(dataDir, file), new PdfImportOptions(), new MergeOptions() { InsertAt = int.MaxValue, InsertAsChild = true });
    }

    d.Save(Path.Combine(dataDir, "sample_StructuredMerge.one"));

    Console.WriteLine("\nThe PDF documents are imported successfully.");
}
```

## 3. Adım: Tek Sayfa Birleştirmeyi kullanarak PDF Belgelerini İçe Aktarın

Tek Sayfa Birleştirme, birden çok PDF belgesindeki içeriği tek bir OneNote sayfasında birleştirir:

```csharp
public static void ImportSetOfFiles_SinglePageMerge()
{
    string dataDir = "Your Document Directory";

    var d = new Document();

    var importOptions = new PdfImportOptions();
    var mergeOptions = new MergeOptions() { ImportAsSinglePage = true, PageSpacing = 100 };

    d.Import(Path.Combine(dataDir, "sampleText.pdf"), importOptions, mergeOptions)
     .Import(Path.Combine(dataDir, "sampleImage.pdf"), importOptions, mergeOptions)
     .Import(Path.Combine(dataDir, "sampleTable.pdf"), importOptions, mergeOptions);

    d.Save(Path.Combine(dataDir, "sample_SinglePageMerge.one"));

    Console.WriteLine("\nThe PDF documents are imported successfully.");
}
```

## 4. Adım: Özel Birleştirmeyi kullanarak PDF Belgelerini içe aktarın

Özel Birleştirme, PDF belgelerindeki sayfaların özel ölçütlere göre tek OneNote sayfalarında gruplanmasına olanak tanır:

```csharp
public static void ImportSetOfFiles_CustomMerge()
{
    string dataDir = "Your Document Directory";

    var d = new Document();

    var mergeOptions = new MergeOptions() { ImportAsSinglePage = true, PageSpacing = 100 };

    IEnumerable<Page> pages = PdfImporter.Import(Path.Combine(dataDir, "SampleGrouping.pdf"));
    while (pages.Any())
    {
        d.Merge(pages.Take(5), mergeOptions);
        pages = pages.Skip(5);
    }

    d.Save(Path.Combine(dataDir, "sample_CustomMerge.one"));

    Console.WriteLine("\nThe PDF documents are imported successfully.");
}
```

## Çözüm

Aspose.Note ile PDF belgelerini .NET uygulamalarınıza entegre etmek, projenizin gereksinimlerine göre uyarlanmış çeşitli birleştirme seçenekleri sunan basit bir süreçtir. İster birden fazla sayfayı içe aktarmanız, ister içeriği hiyerarşik olarak düzenlemeniz gerekiyorsa Aspose.Note kusursuz entegrasyon için gerekli araçları sağlar.

## SSS'ler

### S1: Şifrelenmiş PDF belgelerini içe aktarabilir miyim?

Cevap1: Evet, Aspose.Note şifrelenmiş PDF belgelerinin içe aktarılmasını destekler. Gerekli şifre çözme kimlik bilgilerini sağladığınızdan emin olun.

### S2: İçe aktarma için PDF dosya boyutunda herhangi bir sınırlama var mı?

Cevap2: Aspose.Note'un içe aktarma için PDF dosya boyutunda herhangi bir sınırlaması yoktur. Ancak büyük PDF dosyaları için sistem kaynaklarını ve performans sonuçlarını göz önünde bulundurun.

### S3: İçe aktarılan PDF içeriğinin görünümünü özelleştirebilir miyim?

Cevap3: Evet, Aspose.Note tarafından sağlanan yazı tipi stilleri, renkler ve düzen ayarları gibi çeşitli seçenekleri kullanarak içe aktarılan PDF içeriğinin görünümünü özelleştirebilirsiniz.

### S4: Aspose.Note .NET Core ile uyumlu mu?

Cevap4: Evet, Aspose.Note .NET Core ile uyumludur ve PDF içe aktarma işlevini platformlar arası uygulamalara entegre etmenize olanak tanır.

### S5: Ek desteği veya kaynakları nerede bulabilirim?

 Cevap5: Ek destek, dokümantasyon veya topluluk yardımı için şu adresi ziyaret edin:[Aspose.Note forumu](https://forum.aspose.com/c/note/28).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
