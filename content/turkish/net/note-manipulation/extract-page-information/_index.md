---
title: Aspose.Note for .NET ile Sayfa Bilgilerini Çıkarın
linktitle: Aspose.Note for .NET ile Sayfa Bilgilerini Çıkarın
second_title: Aspose.Note .NET API'si
description: Aspose.Note for .NET'i kullanarak Microsoft OneNote dosyalarından sayfa bilgilerini nasıl çıkaracağınızı öğrenin. Bu kapsamlı eğitim, süreç boyunca size adım adım rehberlik eder.
type: docs
weight: 13
url: /tr/net/note-manipulation/extract-page-information/
---
## giriiş

Aspose.Note for .NET, geliştiricilerin Microsoft OneNote dosyalarıyla programlı olarak çalışmasına olanak tanıyan güçlü bir kitaplıktır. Bu dosyalardan sayfa bilgilerinin çıkarılması, veri analizinden belge yönetimine kadar çeşitli uygulamalar için çok önemli olabilir. Bu eğitimde, Aspose.Note for .NET'i kullanarak sayfa bilgilerini adım adım çıkarma sürecinde size rehberlik edeceğiz.

## Önkoşullar

Başlamadan önce aşağıdaki önkoşulların mevcut olduğundan emin olun:

1. Aspose.Note for .NET Library: Aspose.Note for .NET kütüphanesini indirip yüklediğinizden emin olun. Şuradan indirebilirsiniz[Burada](https://releases.aspose.com/note/net/).

2. Geliştirme Ortamı: Geliştirme ortamınızı Visual Studio veya tercih edilen herhangi bir başka .NET geliştirme aracıyla kurun.

## Ad Alanlarını İçe Aktar

Aspose.Note for .NET ile çalışmak için gereken sınıflara ve yöntemlere erişmek için öncelikle gerekli ad alanlarını içe aktarmanız gerekir.

```csharp
using System.IO;
using Aspose.Note;
using System;
using System.Collections.Generic;
```

Sayfa bilgilerini çıkarma sürecini birden çok adıma ayıralım:

## 1. Adım: Belgeyi Yükleyin

OneNote belgesini Aspose.Note for .NET'e yükleyin.

```csharp
// Belgeler dizininin yolu.
string dataDir = "Your Document Directory";

// Belgeyi Aspose.Note'a yükleyin.
Document oneFile = new Document(dataDir + "Aspose.one");
```

## Adım 2: Sayfalar Arasında Yineleme Yapın

Bilgiyi çıkarmak için belgedeki her sayfayı yineleyin.

```csharp
foreach (Page page in oneFile)
{
    // Sayfa bilgilerini çıkarın ve görüntüleyin.
    Console.WriteLine("LastModifiedTime: {0}", page.LastModifiedTime);
    Console.WriteLine("CreationTime: {0}", page.CreationTime);
    Console.WriteLine("Title: {0}", page.Title);
    Console.WriteLine("Level: {0}", page.Level);
    Console.WriteLine("Author: {0}", page.Author);
    Console.WriteLine();
}
```

## 3. Adım: Sayfa Bilgilerini Alın

Her sayfa hakkında son değiştirilme zamanı, oluşturulma zamanı, başlık, seviye ve yazar gibi belirli bilgileri alın.

```csharp
foreach (Page page in oneFile)
{
    // Sayfa bilgilerini çıkarın ve görüntüleyin.
    Console.WriteLine("LastModifiedTime: {0}", page.LastModifiedTime);
    Console.WriteLine("CreationTime: {0}", page.CreationTime);
    Console.WriteLine("Title: {0}", page.Title);
    Console.WriteLine("Level: {0}", page.Level);
    Console.WriteLine("Author: {0}", page.Author);
    Console.WriteLine();
}
```

## Çözüm

Bu eğitimde Aspose.Note for .NET kullanarak Microsoft OneNote dosyalarından sayfa bilgilerinin nasıl çıkarılacağını öğrendik. Adım adım kılavuzu takip ederek bu işlevselliği .NET uygulamalarınıza kolayca entegre edebilir, OneNote belgelerini daha etkili bir şekilde analiz etmenize ve yönetmenize olanak tanıyabilirsiniz.

## SSS'ler

### S1: Şifrelenmiş OneNote dosyalarından sayfa bilgilerini çıkarabilir miyim?

Cevap1: Evet, Aspose.Note for .NET hem şifrelenmiş hem de şifrelenmemiş OneNote dosyalarından bilgi çıkarmayı destekler.

### S2: Aspose.Note for .NET'in deneme sürümü mevcut mu?

 C2: Evet, ücretsiz deneme sürümünü şuradan indirebilirsiniz:[Burada](https://releases.aspose.com/).

### S3: Çıkarılan sayfa bilgilerini değiştirip belgeye geri kaydedebilir miyim?

Cevap3: Aspose.Note for .NET kesinlikle sayfa bilgilerini değiştirmek ve değişiklikleri orijinal belgeye kaydetmek için kapsamlı yetenekler sağlar.

### S4: Aspose.Note for .NET, OneNote dosyalarındaki eklerle çalışmayı destekliyor mu?

Cevap4: Evet, Aspose.Note for .NET'i kullanarak ekleri çıkarabilir, değiştirebilir ve ekleyebilirsiniz.

### S5: Aspose.Note for .NET için daha fazla desteği ve kaynağı nerede bulabilirim?

 Cevap5: Aspose.Note for .NET forumunu ziyaret edebilirsiniz.[Burada](https://forum.aspose.com/c/note/28) Her türlü yardım veya sorularınız için.