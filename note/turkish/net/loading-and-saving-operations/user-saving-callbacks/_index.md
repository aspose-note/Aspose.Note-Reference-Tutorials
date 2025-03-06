---
title: Aspose.Note'ta Kullanıcıyı Kaydeden Geri Aramalar
linktitle: Aspose.Note'ta Kullanıcıyı Kaydeden Geri Aramalar
second_title: Aspose.Note .NET API'si
description: Yazı tiplerini, CSS'leri ve görüntüleri kaydetmeyi özelleştirmek için Aspose.Note for .NET'te kullanıcı tasarrufu sağlayan geri aramaları nasıl uygulayacağınızı öğrenin.
weight: 31
url: /tr/net/loading-and-saving-operations/user-saving-callbacks/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Note'ta Kullanıcıyı Kaydeden Geri Aramalar

## giriiş

Bu eğitimde, Aspose.Note for .NET'te kullanıcı tasarrufu sağlayan geri aramaların nasıl uygulanacağını inceleyeceğiz. Bu geri aramalar, yazı tiplerini, CSS stil sayfalarını ve görüntüleri kaydetme gibi farklı aşamalarda müdahale edecek kancalar sağlayarak kaydetme sürecini özelleştirmenize olanak tanır. Bu geri aramaları kullanarak, kaydetme davranışını özel gereksinimlerinize uyacak şekilde uyarlayabilir, çıktı üzerindeki esnekliği ve kontrolü artırabilirsiniz.

## Önkoşullar

Aspose.Note'ta kullanıcı tasarrufu sağlayan geri aramaların uygulanmasına dalmadan önce aşağıdaki önkoşulların yerine getirildiğinden emin olun:

1.  Aspose.Note for .NET SDK: Aspose.Note for .NET SDK'yı şu adresten indirip yükleyin:[indirme sayfası](https://releases.aspose.com/note/net/).
   
2. Geliştirme Ortamı: Visual Studio veya başka herhangi bir .NET geliştirme ortamı gibi uygun bir geliştirme ortamı kurun.

## Ad Alanlarını İçe Aktar

Başlamak için Aspose.Note kütüphanesinden gerekli sınıflara ve yöntemlere erişmek için gerekli ad alanlarını projenize aktardığınızdan emin olun:

```csharp
using Aspose.Note.Saving.Html;
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Text;
```

Şimdi kullanıcı tasarrufu sağlayan geri aramaların uygulanmasını birden çok adıma ayıralım:

## Adım 1: Geri Çağırma Özelliklerini Tanımlayın

```csharp
public string RootFolder { get; set; }
public bool KeepCssStreamOpened { get; set; }
public string CssFolder { get; set; }
public Stream CssStream { get; private set; }
public string FontsFolder { get; set; }
public string ImagesFolder { get; set; }
```

Burada kök klasörü, CSS klasörünü, yazı tipleri klasörünü, resimler klasörünü ve diğer ilgili ayarları belirtmek için çeşitli özellikler tanımlıyoruz.

## Adım 2: Yazı Tipi Tasarrufu Geri Aramasını Uygulayın

```csharp
public void FontSaving(FontSavingArgs args)
{
    string uri;
    Stream stream;
    this.CreateResourceInFolder(this.FontsFolder, args.FileName, out uri, out stream);
    args.Stream = stream;
    args.Uri = Path.Combine("..", uri).Replace("\\", "\\\\");
}
```

 Bu adımda şunları uyguluyoruz:`FontSaving` Yazı tiplerinin kaydedilmesini sağlayan geri çağırma yöntemi. Belirtilen yazı tipi klasöründe bir kaynak oluşturur ve akışı ve URI'yi buna göre atar.

## 3. Adım: CSS Kaydetme Geri Aramasını Uygulayın

```csharp
public void CssSaving(CssSavingArgs args)
{
    string uri;
    Stream stream;
    this.CreateResourceInFolder(this.CssFolder, args.FileName, out uri, out stream);
    args.Stream = this.CssStream = stream;
    args.KeepStreamOpen = this.KeepCssStreamOpened;
    args.Uri = uri;
}
```

 Burada şunu tanımlıyoruz:`CssSaving` CSS stil sayfalarının kaydedilmesini yönetmek için geri çağırma yöntemi. Belirtilen CSS klasöründe bir kaynak oluşturur ve akışı, URI'yi ve diğer özellikleri buna göre ayarlar.

## Adım 4: Görüntü Kaydederek Geri Aramayı Uygulayın

```csharp
public void ImageSaving(ImageSavingArgs args)
{
    string uri;
    Stream stream;
    this.CreateResourceInFolder(this.ImagesFolder, args.FileName, out uri, out stream);
    args.Stream = stream;
    args.Uri = uri;
}
```

 Son olarak şunları uyguluyoruz:`ImageSaving` görüntülerin kaydedilmesini işlemek için geri çağırma yöntemi. Önceki adımlara benzer şekilde, belirtilen resimler klasöründe bir kaynak oluşturur ve akışı ve URI'yi atar.

## Çözüm

Bu eğitimde, Aspose.Note for .NET'te kullanıcı tasarrufu sağlayan geri aramaların nasıl uygulanacağını öğrendik. Sağlanan adımları izleyerek yazı tipleri, CSS stil sayfaları ve görseller için kaydetme işlemini özelleştirerek çıktı üzerinde daha fazla esneklik ve kontrol sağlayabilirsiniz.

## SSS

### S1: Kaydetme sürecinin diğer yönlerini özelleştirmek için bu geri aramaları kullanabilir miyim?

C1: Evet, kaydetme sürecinin çeşitli yönlerini ihtiyaçlarınıza göre özelleştirmek için bu geri aramaları genişletebilir veya ek geri aramalar uygulayabilirsiniz.

### S2: Aspose.Note for .NET diğer .NET çerçeveleriyle uyumlu mudur?

C2: Evet, Aspose.Note for .NET, .NET Core ve .NET Standard dahil olmak üzere çeşitli .NET çerçeveleriyle uyumludur.

### S3: Kaydetme işlemi sırasında hataları veya istisnaları nasıl ele alabilirim?

Cevap 3: Oluşabilecek hataları veya istisnaları düzgün bir şekilde ele almak için her geri çağırma yöntemine hata işleme mekanizmalarını dahil edebilirsiniz.

### S4: Bu geri aramaları kullanırken herhangi bir performans hususu var mı?

Cevap4: Bu geri aramalar esneklik sunarken, özellikle büyük belgeler veya kaynaklarla uğraşırken herhangi bir performans yükünü önlemek için bunların verimli bir şekilde uygulanmasını sağlayın.

### S5: Kullanıcı girişine veya diğer koşullara göre kaydetme davranışını dinamik olarak değiştirebilir miyim?

C5: Evet, kaydetme davranışını çeşitli faktörlere göre dinamik olarak ayarlamak için geri çağırma yöntemlerine koşullu mantığı dahil edebilirsiniz.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
