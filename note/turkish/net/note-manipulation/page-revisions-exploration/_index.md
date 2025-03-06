---
title: Aspose.Note Belgelerindeki Sayfa Revizyonlarını Keşfedin
linktitle: Aspose.Note Belgelerindeki Sayfa Revizyonlarını Keşfedin
second_title: Aspose.Note .NET API'si
description: Adım adım rehberlikle .NET çerçevesini kullanarak Aspose.Note belgelerindeki sayfa revizyonlarını nasıl keşfedeceğinizi öğrenin.
weight: 14
url: /tr/net/note-manipulation/page-revisions-exploration/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Note Belgelerindeki Sayfa Revizyonlarını Keşfedin

## giriiş

Bu eğitimde, .NET çerçevesini kullanarak Aspose.Note belgelerindeki sayfa revizyonlarını incelemeye devam edeceğiz. Aspose.Note, geliştiricilerin Microsoft OneNote dosyalarıyla programlı olarak çalışmasına olanak tanıyan, bu dosyalardan veri işlemek ve çıkarmak için çeşitli özellikler sunan güçlü bir kitaplıktır.

## Önkoşullar

Başlamadan önce aşağıdaki önkoşulları oluşturduğunuzdan emin olun:

### 1. Aspose.Note for .NET'i indirip yükleyin

 Ziyaret edin[indirme sayfası](https://releases.aspose.com/note/net/) ve Aspose.Note for .NET kitaplığını indirin. Kitaplığı geliştirme ortamınıza kurmak için sağlanan kurulum talimatlarını izleyin.

### 2. Gerekli Ad Alanlarını Yükleyin

Aspose.Note işlevlerine sorunsuz bir şekilde erişmek için gerekli ad alanlarını .NET projenize aktardığınızdan emin olun.

```csharp
using System.IO;
using Aspose.Note;
using System;
using System.Collections.Generic;
```

Şimdi sayfa revizyonlarını keşfetme sürecini adım adım talimatlara ayıralım:

## 1. Adım: Belgeyi Yükleyin

Öncelikle Aspose.Note belgesini yüklememiz ve belge geçmişinin yüklenmesini sağlamamız gerekiyor.

```csharp
string dataDir = "Your Document Directory";
Document document = new Document(dataDir + "Aspose.one", new LoadOptions { LoadHistory = true });
```

## 2. Adım: Sayfa Düzeltmelerini Alın

Belge yüklendikten sonra belirli bir sayfaya ilişkin revizyonları alabiliriz. Bu örnekte ilk sayfanın revizyonlarını alacağız.

```csharp
Page firstPage = document.FirstChild;
foreach (Page pageRevision in document.GetPageHistory(firstPage))
{
    /*Use pageRevision like a regular page.*/
    Console.WriteLine("LastModifiedTime: {0}", pageRevision.LastModifiedTime);
    Console.WriteLine("CreationTime: {0}", pageRevision.CreationTime);
    Console.WriteLine("Title: {0}", pageRevision.Title);
    Console.WriteLine("Level: {0}", pageRevision.Level);
    Console.WriteLine("Author: {0}", pageRevision.Author);
    Console.WriteLine();
}
```

## Adım 3: Revizyonları Yineleyin

Döngü içinde, sayfanın her revizyonunu yineleyin ve son değiştirilme zamanı, oluşturulma zamanı, başlık, seviye ve yazar gibi özelliklerine erişin.

## Çözüm

Aspose.Note belgelerindeki sayfa revizyonlarını .NET kullanarak keşfetmek basit bir işlemdir. Bu öğreticide özetlenen adımları izleyerek OneNote dosyalarınızın düzeltme geçmişini programlı olarak etkili bir şekilde alıp analiz edebilirsiniz.

## SSS'ler

### S1: Aspose.Note for .NET'i yeni OneNote belgeleri oluşturmak için kullanabilir miyim?

C1: Evet, Aspose.Note for .NET, OneNote belgelerini programlı olarak oluşturmanıza, düzenlemenize ve değiştirmenize olanak tanır.

### S2: Aspose.Note tüm OneNote dosyası türleri için yükleme geçmişini destekliyor mu?

Cevap2: Aspose.Note, hem .one hem de .onepkg dosya formatları için yükleme geçmişini destekler.

### S3: Aspose.Note for .NET'in ücretsiz deneme sürümü mevcut mu?

Cevap3: Evet, Aspose.Note for .NET'in ücretsiz deneme sürümünü şu adresten indirebilirsiniz:[Burada](https://releases.aspose.com/).

### S4: Aspose.Note for .NET için nasıl geçici lisans alabilirim?

 Cevap4: Şu adresten geçici bir lisans talep edebilirsiniz:[bu bağlantı](https://purchase.aspose.com/temporary-license/).

### S5: Aspose.Note for .NET desteğini nerede bulabilirim?

 Cevap5: Destek ve kaynakları şurada bulabilirsiniz:[Aspose.Note forumu](https://forum.aspose.com/c/note/28).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
