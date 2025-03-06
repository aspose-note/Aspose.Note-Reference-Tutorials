---
title: Aspose.Note'ta Sayfa Başlığıyla Belge Oluşturma
linktitle: Aspose.Note'ta Sayfa Başlığıyla Belge Oluşturma
second_title: Aspose.Note .NET API'si
description: Aspose.Note for .NET'i kullanarak başlıklı sayfalara sahip belgeler oluşturmayı öğrenin. Sorunsuz entegrasyon için adım adım kılavuzumuzu izleyin.
weight: 13
url: /tr/net/loading-and-saving-operations/create-doc-with-page-title/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Note'ta Sayfa Başlığıyla Belge Oluşturma

## giriiş

Bu eğitimde, Aspose.Note for .NET'i kullanarak başlıklı sayfaya sahip bir belge oluşturma sürecinde size rehberlik edeceğiz. Aspose.Note, geliştiricilerin Microsoft OneNote dosyalarıyla programlı olarak çalışmasına olanak tanıyan güçlü bir API'dir.

## Önkoşullar

Başlamadan önce aşağıdaki önkoşulların yüklendiğinden ve ayarlandığından emin olun:

### Visual Studio Kurulumu

1. Visual Studio'yu İndirin: Henüz yapmadıysanız, Microsoft web sitesinden Visual Studio'yu indirip yükleyin.

2. .NET Geliştirme İş Yükünü Yükleme: Yükleme işlemi sırasında, .NET geliştirme için gerekli tüm bileşenlere sahip olduğunuzdan emin olmak için ".NET masaüstü geliştirme" iş yükünü seçtiğinizden emin olun.

3. Yeni Bir Proje Oluşturun: Visual Studio'yu açın ve yeni bir proje oluşturun (Konsol Uygulaması veya tercih ettiğiniz başka bir tür).

### Aspose.Note Kurulumu

1.  Aspose.Note'u edinin: Aspose.Note for .NET kitaplığını şu adresten indirin:[İnternet sitesi](https://releases.aspose.com/note/net/).

2. Aspose.Note'u NuGet aracılığıyla yükleyin: Alternatif olarak Aspose.Note for .NET'i Visual Studio'daki NuGet Paket Yöneticisi aracılığıyla da yükleyebilirsiniz. Basitçe "Aspose.Note"u arayın ve en son sürümü yükleyin.

## Ad Alanlarını İçe Aktarma

Aspose.Note'u projenizde kullanmak için öncelikle gerekli ad alanlarını içe aktarmanız gerekir.

```csharp
using System.IO;
using Aspose.Note;
using Aspose.Note.Saving;
using System;
using System.Drawing;
using System.Globalization;
```

Şimdi sayfa başlığına sahip bir belge oluşturma sürecini birden çok adıma ayıralım:

## Adım 1: Belge Nesnesi Oluşturun

```csharp
//Document sınıfının bir nesnesini oluşturun
Document doc = new Aspose.Note.Document();
```

## Adım 2: Sayfa Sınıfı Nesnesini Başlatın

```csharp
// Sayfa sınıfı nesnesini başlat
Aspose.Note.Page page = new Aspose.Note.Page(doc);
```

## 3. Adım: Metin için Varsayılan Stili Ayarlayın

```csharp
// Belgedeki tüm metinler için varsayılan stil.
ParagraphStyle textStyle = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
```

## Adım 4: Sayfa Başlığı Özelliklerini Ayarlayın

```csharp
// Sayfa başlığı özelliklerini ayarlama
page.Title = new Title(doc)
{
    TitleText = new RichText(doc) { Text = "Title text.", ParagraphStyle = textStyle },
    TitleDate = new RichText(doc) { Text = new DateTime(2011, 11, 11).ToString("D", CultureInfo.InvariantCulture), ParagraphStyle = textStyle },
    TitleTime = new RichText(doc) { Text = "12:34", ParagraphStyle = textStyle }
};
```

## Adım 5: Belgeye Sayfa Düğümü Ekleme

```csharp
// Belgeye Sayfa düğümü ekle
doc.AppendChildLast(page);
```

## Adım 6: OneNote Belgesini Kaydetme

```csharp
// OneNote belgesini kaydet
string dataDir = "Your Document Directory";
dataDir = dataDir + "CreateDocWithPageTitle_out.one";
doc.Save(dataDir);
```

## Çözüm

Tebrikler! Aspose.Note for .NET'i kullanarak başlıklı sayfaya sahip bir belgeyi başarıyla oluşturdunuz. Bu eğitimde, OneNote dosyalarını programlı olarak yönetmek için Aspose.Note'u .NET uygulamalarınıza entegre etmenize yardımcı olacak adım adım bir kılavuz sağlanmıştır.

## SSS'ler

### S1: Başlık metni stilini özelleştirebilir miyim?

Cevap1: Evet, başlık metninin yazı tipi rengini, yazı tipi adını ve yazı tipi boyutunu gereksinimlerinize göre özelleştirebilirsiniz.

### S2: Aspose.Note .NET Core ile uyumlu mu?

C2: Evet, Aspose.Note .NET Core'u destekleyerek platformlar arası uygulamalar geliştirmenize olanak tanır.

### S3: Belgeye resim ve ekler ekleyebilir miyim?

A3: Kesinlikle! Aspose.Note, OneNote belgelerinize sorunsuz bir şekilde resim, eklenti ve diğer öğeleri eklemenizi sağlayan API'ler sağlar.

### S4: Aspose.Note mevcut OneNote dosyalarının okunmasını destekliyor mu?

Cevap4: Evet, mevcut OneNote dosyalarını kolaylıkla okumak, değiştirmek ve işlemek için Aspose.Note'u kullanabilirsiniz.

### S5: Herhangi bir sorunla karşılaşırsam nereden destek bulabilirim?

 Cevap5: Destek ve yardımı şu adreste bulabilirsiniz:[Aspose.Note forumu](https://forum.aspose.com/c/note/28)Uzmanların ve topluluk üyelerinin sorularınız konusunda size yardımcı olabileceği yer.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
