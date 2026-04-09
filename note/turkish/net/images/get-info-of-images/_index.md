---
date: 2026-04-09
description: Aspose.Note for .NET ile OneNote dosyalarından görüntü meta verilerini
  çıkarmayı ve görüntü boyutlarını almayı öğrenin. C# geliştiricileri için adım adım
  rehber.
keywords:
- extract image metadata
- how to extract images
- get image dimensions
- load onenote document
- c# get image properties
linktitle: Aspose.Note kullanarak OneNote'tan görüntü meta verilerini nasıl çıkarabilirsiniz
second_title: Aspose.Note .NET API
title: Aspose.Note kullanarak OneNote'tan resim meta verilerini nasıl çıkarılır
url: /tr/net/images/get-info-of-images/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Note for .NET ile Görüntü Üst Verilerini Çıkarma

Bu uygulamalı öğreticide, Aspose.Note kütüphanesini C# için kullanarak Microsoft OneNote dosyalarından genişlik, yükseklik, orijinal boyut, dosya adı ve değiştirilme zamanı dahil olmak üzere **görüntü üst verilerini nasıl çıkaracağınızı** öğreneceksiniz. Görüntü küçük resimlerini göstermeniz, görüntü boyutlarını doğrulamanız veya gömülü varlıkların bir kataloğunu oluşturmanız gerekse, bu bilgileri programlı olarak çıkarmak sayısız manuel adımı tasarruf ettirir.

## Hızlı Yanıtlar
- **“görüntü üst verilerini çıkarma” ne anlama geliyor?** OneNote belgesi içinde depolanan görüntülerden boyutlar, dosya adı ve zaman damgaları gibi özellikleri almayı ifade eder.  
- **Bu işlemi hangi kütüphane gerçekleştirir?** Aspose.Note for .NET.  
- **Bir lisansa ihtiyacım var mı?** Geliştirme için ücretsiz deneme sürümü çalışır; üretim için ticari lisans gereklidir.  
- **Desteklenen platformlar?** .NET Framework 4.6+, .NET Core 3.1+, .NET 5/6+.  
- **Tipik çalışma süresi?** Standart bir .one dosyası için bir saniyeden az.

## Görüntü üst verilerini çıkarma nedir?
Görüntü üst verilerini çıkarmak, bir OneNote sayfasındaki her görüntü nesnesine eşlik eden açıklayıcı nitelikleri (genişlik, yükseklik, orijinal boyutlar, dosya adı, son‑değiştirilme zamanı vb.) programlı olarak okumak anlamına gelir. Bu veriler doğrulama, raporlama veya daha ileri görüntü işleme için faydalıdır.

## Neden OneNote'tan görüntü üst verilerini çıkaralım?
- **Otomasyon** – Görüntü envanterlerini otomatik olarak oluşturan araçlar geliştirin.  
- **Doğrulama** – Yayınlamadan önce görüntülerin boyut gereksinimlerini karşıladığından emin olun.  
- **Entegrasyon** – Görüntü detaylarına ihtiyaç duyan diğer sistemlerle (CMS, DAM vb.) OneNote içeriğini birleştirin.  
- **Performans** – Yalnızca boyutlar gerektiğinde tam görüntü ikili dosyalarını yüklemekten kaçının.

## Önkoşullar
1. **C# temelleri** – Temel C# kodu yazmada rahat olmalısınız.  
2. **Aspose.Note for .NET** – Kütüphaneyi resmi siteden [buradan](https://releases.aspose.com/note/net/) indirin ve kurun.  
3. **Bir OneNote (.one) dosyası** – Görüntü içeren mevcut herhangi bir OneNote belgesi.

## Ad Alanlarını İçe Aktarın
Başlamadan önce, gerekli ad alanlarını içe aktarın:

```csharp
using System.IO;
using Aspose.Note;
using System.Collections.Generic;
using System;
```

## Adım 1: OneNote belgesini yükleyin
İlk olarak, hedef OneNote dosyasını bir `Aspose.Note.Document` nesnesine yükleyin. Bu, API'yi sonraki sorgular için hazırlayan **OneNote belgesini yükle** adımıdır.

```csharp
// The path to the documents directory.
string dataDir = "Your Document Directory";

// Load the document into Aspose.Note.
Document oneFile = new Document(dataDir + "Aspose.one");
```

`"Your Document Directory"` ifadesini `.one` dosyanızı tutan gerçek klasörle değiştirin.

## Adım 2: Tüm görüntü düğümlerini alın
Şimdi, belgeden her `Image` düğümünü çekerek **görüntüleri nasıl çıkaracağımızı** göstereceğiz.

```csharp
// Get all Image nodes
IList<Aspose.Note.Image> images = oneFile.GetChildNodes<Aspose.Note.Image>();
```

`GetChildNodes<T>()` yöntemi tüm not defteri hiyerarşisini tarar ve bir görüntü nesnesi koleksiyonu döndürür.

## Her görüntü üzerinde döngü yapın ve **c# get image properties**
Koleksiyon üzerinde döngü kuracağız ve üst verileri, **görüntü boyutlarını al** ve **orijinal görüntü boyutunu çıkar** değerlerini içerecek şekilde yazdıracağız.

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

Çıktı, her görüntünün sayfada render edildiği mevcut genişlik/yüksekliğini, dosyada saklanan orijinal boyutlarını, dosya adını ve son değişiklik zaman damgasını gösterir.

## Yaygın Sorunlar ve Çözümler
| Sorun | Neden | Çözüm |
|-------|--------|-----|
| **NullReferenceException** `images` boş olduğunda | Belge hiçbir görüntü içermiyor | Kaynak `.one` dosyasının gömülü görüntüler içerdiğini doğrulayın. |
| **Incorrect dimensions** | Görüntüler OneNote'ta ölçeklendirilmiş | Gerçek boyutu elde etmek için `OriginalWidth`/`OriginalHeight` kullanın. |
| **FileName is empty** | Görüntü panodan yapıştırıldı | API bir dosya adı içermeyebilir; kodunuzda `null` veya boş stringleri işleyin. |

## Sıkça Sorulan Sorular

**Q: Aspose.Note, Microsoft OneNote'un tüm sürümleriyle uyumlu mu?**  
A: Aspose.Note .one, .onepkg ve .onetoc2 formatlarını destekler, 2007'den itibaren çoğu OneNote sürümünü kapsar.

**Q: Çıkarma işleminden sonra görüntü özelliklerini değiştirebilir miyim?**  
A: Evet, `Width`, `Height` veya `FileName` gibi özellikleri değiştirebilir ve ardından belgeyi kaydedebilirsiniz.

**Q: Aspose.Note .NET Core ile çalışıyor mu?**  
A: Kesinlikle. Kütüphane .NET Core, .NET 5 ve .NET 6 ile tam uyumludur.

**Q: Ücretsiz bir deneme sürümü mevcut mu?**  
A: Evet, tüm özellikleri keşfetmek için Aspose web sitesinden bir deneme sürümü indirebilirsiniz.

**Q: Ek yardım veya topluluk desteği nereden alabilirim?**  
A: İpuçları, örnek kod ve topluluktan yanıtlar için Aspose.Note forumunu [buradan](https://forum.aspose.com/c/note/28) ziyaret edin.

---

**Son Güncelleme:** 2026-04-09  
**Test Edilen:** Aspose.Note 24.11 for .NET  
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}