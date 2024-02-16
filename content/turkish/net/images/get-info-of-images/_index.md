---
title: Aspose.Note'taki Görsellerin Bilgisini Alın
linktitle: Aspose.Note'taki Görsellerin Bilgisini Alın
second_title: Aspose.Note .NET API'si
description: Aspose.Note for .NET'i kullanarak Microsoft OneNote dosyalarından görüntü bilgilerini nasıl çıkaracağınızı öğrenin. Verimli geliştirme için adım adım kılavuzumuzu izleyin.
type: docs
weight: 13
url: /tr/net/images/get-info-of-images/
---
## giriiş

.NET geliştirme dünyasında Aspose.Note, Microsoft OneNote dosyalarıyla çalışmak için güçlü bir araç seti sağlar. Geliştiricilerin sıklıkla karşılaştığı ortak görevlerden biri, bu notların içine yerleştirilmiş görsellerden bilgi çıkarmaktır. Aspose.Note, boyutların, dosya adlarının veya değişiklik zamanlarının elde edilmesi bu süreci basitleştirir.

## Önkoşullar

Aspose.Note ile görüntü bilgilerini çıkarmaya başlamadan önce aşağıdakilere sahip olduğunuzdan emin olun:

1. Temel C# bilgisi: C# programlama diline aşina olmak, kod örneklerini anlamak için çok önemlidir.
2.  Aspose.Note for .NET kurulu: Geliştirme ortamınızda Aspose.Note kütüphanesinin kurulu olduğundan emin olun. İndirebilirsin[Burada](https://releases.aspose.com/note/net/).

## Ad Alanlarını İçe Aktar

Başlamadan önce gerekli ad alanlarını içe aktaralım:

```csharp
using System.IO;
using Aspose.Note;
using System.Collections.Generic;
using System;
```

## 1. Adım: Belgeyi Yükleyin

Öncelikle hedef OneNote belgesini Aspose.Note'a yükleyin:

```csharp
// Belgeler dizininin yolu.
string dataDir = "Your Document Directory";

// Belgeyi Aspose.Note'a yükleyin.
Document oneFile = new Document(dataDir + "Aspose.one");
```

 Yer değiştirmek`"Your Document Directory"` OneNote dosyanızın yolu ile birlikte.

## 2. Adım: Görüntü Bilgilerini Alın

Daha sonra belgedeki tüm görüntü düğümlerini alın:

```csharp
// Tüm Görüntü düğümlerini al
IList<Aspose.Note.Image> images = oneFile.GetChildNodes<Aspose.Note.Image>();
```

Bu kod parçacığı, yüklenen OneNote belgesindeki tüm görüntü düğümlerini getirir.

## Adım 3: Görselleri Yineleyin

Şimdi meta verilerini çıkarmak için her görüntü düğümünü tekrarlayalım:

```csharp
foreach (Aspose.Note.Image image in images)
{
    Console.WriteLine("Width: {0}", image.Width);
    Console.WriteLine("Height: {0}", image.Height);
    Console.WriteLine("OriginalWidth: {0}", image.OriginalWidth);
    Console.WriteLine("OriginalHeight: {0}", image.OriginalHeight);
    Console.WriteLine("FileName: {0}", image.FileName);
    Console.WriteLine("LastModifiedTime: {0}", image.LastModifiedTime);
    Console.WriteLine();
}
```

Bu döngü, her görüntünün genişlik, yükseklik, orijinal boyutlar, dosya adı ve son değiştirilme zamanı gibi çeşitli özelliklerini yazdırır.

## Çözüm

Aspose.Note for .NET ile OneNote belgelerinden görüntü bilgilerinin çıkarılması sorunsuz bir süreç haline gelir. Geliştiriciler, bu eğitimde özetlenen adımları izleyerek, gömülü görüntülerden meta verileri verimli bir şekilde alabilir ve böylece güçlü uygulamalar oluşturmalarını sağlayabilirler.

## SSS'ler

### S1: Aspose.Note, Microsoft OneNote'un tüm sürümleriyle uyumlu mudur?

Cevap1: Aspose.Note, .one, .onepkg ve .onetoc2 dahil olmak üzere çeşitli OneNote dosya formatlarını destekleyerek farklı sürümler arasında uyumluluk sağlar.

### S2: Aspose.Note'u kullanarak görüntü özelliklerini değiştirebilir miyim?

Cevap2: Evet, Aspose.Note boyutlar, dosya adları ve değişiklik süreleri gibi görüntü özelliklerini programlı olarak değiştirmenize olanak tanır.

### S3: Aspose.Note .NET Core desteği sunuyor mu?

C3: Evet, Aspose.Note, .NET Core desteği sağlayarak uygulamalarınız için platformlar arası geliştirme olanağı sağlar.

### S4: Aspose.Note'un ücretsiz deneme sürümü mevcut mu?

Cevap4: Evet, satın alma işlemi yapmadan önce özelliklerini keşfetmek için Aspose.Note'un ücretsiz deneme sürümüne erişebilirsiniz.

### S5: Aspose.Note ile ilgili ek desteği veya yardımı nerede bulabilirim?

Cevap5: Sorularınız veya yardımlarınız için Aspose.Note forumunu ziyaret edebilirsiniz.[Burada](https://forum.aspose.com/c/note/28).