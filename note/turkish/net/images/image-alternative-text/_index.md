---
date: 2026-04-09
description: Aspose.Note for .NET'te görüntülere alt metin eklemeyi kolayca öğrenin.
  Erişilebilirliği artırın ve bu adım adım kılavuzla kullanıcı deneyimini iyileştirin.
keywords:
- how to add alt text
- add alternative text image
- append image to page
linktitle: Aspose.Note'ta Görsellere Alternatif Metin Ekle
second_title: Aspose.Note .NET API
title: Aspose.Note'ta Görsellere Alt Metin Nasıl Eklenir
url: /tr/net/images/image-alternative-text/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Note'ta Görsellere Alt Metin Ekleme

## Giriş

OneNote‑stil belgelerinizde görsellere **alt metin ekleme** ihtiyacınız varsa, doğru yerdesiniz. Bu öğretici, Aspose.Note for .NET kullanarak bir görsele alternatif metin (hem başlık hem de açıklama) eklemek için gereken adımları size gösterir. Alt metin eklemek, sadece ekran okuyucu kullanıcıları için erişilebilirliği artırmakla kalmaz, aynı zamanda bu görselleri daha sonra gömen web‑yayınlanan içeriklerin SEO'sunu da iyileştirir.

## Hızlı Yanıtlar
- **“alt text” ne anlama gelir?** Görüntülenemediğinde bir resmi temsil eden metinsel açıklama.  
- **Neden alt metin için Aspose.Note kullanmalı?** Başlık ve açıklamayı programlı olarak ayarlamak için basit bir API sağlar.  
- **Ön koşullar nelerdir?** .NET geliştirme ortamı, Visual Studio ve Aspose.Note for .NET'in yüklü olması.  
- **Mevcut görsellere alt metin ekleyebilir miyim?** Evet – bir görüntü nesnesini yükleyebilir, özelliklerini ayarlayabilir ve belgeyi kaydedebilirsiniz.  
- **Çıktı nerede kaydedilir?** `document.Save(...)` ile belirttiğiniz yolda.

## Aspose.Note'ta “alt metin ekleme” nedir?

Alt metin eklemek, bir `Image` nesnesinin `AlternativeTextTitle` ve `AlternativeTextDescription` özelliklerini atamak anlamına gelir. Bu özellikler, ekran okuyucular ve diğer yardımcı teknolojiler tarafından resmin anlamını iletmek için okunur.

## Neden belgenize alternatif metin eklemelisiniz?

- **Erişilebilirlik uyumu** – WCAG ve Section 508 yönergelerini karşılar.  
- **Gelişmiş SEO** – arama motorları açıklayıcı metni indeksler.  
- **Daha iyi kullanıcı deneyimi** – görselleri devre dışı bırakılmış kullanıcılar bile içeriği anlayabilir.

## Ön Koşullar

Başlamadan önce, şunların olduğundan emin olun:

- C# ve .NET geliştirme konusunda temel bilgi.  
- Makinenizde Visual Studio yüklü.  
- Projenizde referans olarak eklenmiş Aspose.Note for .NET indirilmiş – bunu [buradan](https://releases.aspose.com/note/net/) alabilirsiniz.  
- Gömmek istediğiniz bir görüntü dosyası (ör. `image.jpg`).

## Ad Alanlarını İçe Aktarın

İlk olarak, dosya işlemleri ve Aspose.Note nesneleri için gerekli ad alanlarını ekleyin.

```csharp
using System.IO;
using Aspose.Note;
using System.Collections.Generic;
using System.Drawing;
using System;
```

## Adım 1: Belge ve Sayfayı Başlatma

Yeni bir `Document` örneği oluşturun ve görüntünün yer alacağı bir `Page` ekleyin.

```csharp
var document = new Document();
var page = new Page(document);
```

## Adım 2: Görüntüyü Yükleme

Resminizin bulunduğu klasöre işaret edin ve bir `Image` nesnesi oluşturun.

```csharp
string dataDir = "Your Document Directory";
var image = new Image(document, dataDir + "image.jpg");
```

## Adım 3: Alternatif Metni Ayarlama

Burada başlık ve açıklama alanlarını doldurarak **alternatif metin ekliyoruz**.

```csharp
image.AlternativeTextTitle = "This is an image's title!";
image.AlternativeTextDescription = "And this is an image's description!";
```

## Adım 4: Görüntüyü Sayfaya Ekleme

Şimdi `AppendChildLast` yöntemiyle **görseli sayfaya ekliyoruz**.

```csharp
page.AppendChildLast(image);
```

## Adım 5: Belgeyi Kaydetme

Çıktı dosya adını belirleyin ve OneNote belgesini kaydedin.

```csharp
dataDir = dataDir + "ImageAlternativeText_out.one";
document.Save(dataDir);
```

## Adım 6: Başarı Mesajını Görüntüleme

Basit bir konsol mesajı, işlemin başarılı olduğunu onaylar.

```csharp
Console.WriteLine("\nImage alternative text setup successfully.\nFile saved at " + dataDir); 
```

## Yaygın Sorunlar ve Çözümler

| Sorun | Neden | Çözüm |
|-------|-------|-------|
| **Alt metin görünmüyor** | `AlternativeTextTitle` veya `AlternativeTextDescription` boş bırakılmış | Kaydetmeden önce her iki özelliğin de ayarlandığından emin olun. |
| **Dosya bulunamadı** | Yanlış `dataDir` yolu | Mutlak bir yol kullanın veya göreli klasörün mevcut olduğunu doğrulayın. |
| **Kaydetme sırasında istisna** | Yetersiz yazma izinleri | Visual Studio'yu yönetici olarak çalıştırın veya yazılabilir bir klasör seçin. |

## Sıkça Sorulan Sorular

### S1: Görseller için alternatif metin neden önemlidir?

A1: Alternatif metin, görsellerin metinsel bir açıklamasını sağlar ve ekran okuyuculara güvenen ya da görselleri devre dışı bırakmış kullanıcılar için erişilebilir kılar.

### S2: Bir belgede mevcut görsellere alternatif metin ekleyebilir miyim?

A2: Evet, Aspose.Note for .NET kullanarak belgede zaten bulunan görsellere kolayca alternatif metin ekleyebilirsiniz.

### S3: Aspose.Note diğer .NET kütüphaneleriyle uyumlu mu?

A3: Aspose.Note, diğer .NET kütüphaneleriyle sorunsuz bir şekilde bütünleşir ve belge manipülasyonu için kapsamlı işlevsellik sunar.

### S4: Aspose.Note için nasıl destek alabilirim?

A4: Aspose.Note için destek alabilirsiniz; sorular sorabilir ve çözümler bulabilirsiniz. Bunun için [Aspose.Note forumunu](https://forum.aspose.com/c/note/28) ziyaret edin.

### S5: Aspose.Note için ücretsiz deneme mevcut mu?

A5: Evet, [buradan](https://releases.aspose.com/) ücretsiz bir deneme alabilirsiniz.

## Sonuç

Görsellere alt metin eklemek, erişilebilirlik, SEO ve genel kullanıcı deneyimi için büyük fark yaratan küçük bir adımdır. Aspose.Note for .NET ile süreç basittir—sadece `AlternativeTextTitle` ve `AlternativeTextDescription` özelliklerini ayarlayın, görseli ekleyin ve belgeyi kaydedin.

---

**Last Updated:** 2026-04-09  
**Tested With:** Aspose.Note 24.11 for .NET  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}