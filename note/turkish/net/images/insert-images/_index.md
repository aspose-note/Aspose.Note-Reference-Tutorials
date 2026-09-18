---
date: 2026-05-05
description: Aspose.Note belgelerine .NET kullanarak nasıl resim ekleyeceğinizi öğrenin.
  Bu adım adım kılavuz, resmi nasıl hizalayacağınızı, sayfaya nasıl ekleyeceğinizi
  ve görsel içeriği nasıl geliştireceğinizi gösterir.
keywords:
- how to insert image
- how to align image
- append image to page
linktitle: Aspose.Note Belgelerine Görüntü Ekle
second_title: Aspose.Note .NET API
title: Aspose.Note Belgelerine .NET ile Resim Ekleme
url: /tr/net/images/insert-images/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# .NET ile Aspose.Note Belgelerine Görüntü Ekleme

## Giriş

Aspose.Note dosyalarınızı daha ilgi çekici hâle getirmek istiyorsanız, **görsel ekleme** ilk öğrenmeniz gereken beceridir. Bu öğreticide, resimleri eklemek, boyutlarını kontrol etmek, konumlarını hassas bir şekilde ayarlamak ve hatta istediğiniz gibi hizalamak için gereken adımları adım adım göstereceğiz. Sonunda, görüntü ekleme, hizalama ve sayfaya ekleme konularında rahat olacaksınız—hepsi temiz ve okunabilir C# kodu ile.

## Hızlı Yanıtlar
- **Gerekli kütüphane nedir?** Aspose.Note for .NET  
- **Görüntü boyutunu programlı olarak ayarlayabilir miyim?** Evet – Width ve Height özelliklerini kullanın.  
- **Bir görüntüyü nasıl konumlandırırım?** HorizontalOffset, VerticalOffset ayarlayın veya hizalama seçeneklerini kullanın.  
- **Görüntü formatları için bir sınırlama var mı?** JPG, PNG, BMP, GIF ve diğerleri desteklenir.  
- **Üretim için lisansa ihtiyacım var mı?** Ticari kullanım için geçerli bir Aspose.Note lisansı gereklidir.

## Aspose.Note'ta görüntü ekleme nedir?

Görüntü eklemek, bir Aspose.Note.Image nesnesi oluşturmak, görsel özelliklerini yapılandırmak ve OneNote uyumlu .one dosyasındaki bir sayfaya eklemek anlamına gelir. Bu sayede notlarınıza ekran görüntüleri, diyagramlar veya herhangi bir görsel öğe ekleyebilirsiniz.

## Aspose.Note ile neden görüntü eklemelisiniz?

- **Daha iyi iletişim:** Görseller, karmaşık fikirleri yalnızca metinden daha hızlı açıklığa kavuşturur.  
- **Tutarlı düzen:** Programlı kontrol, her belgenin aynı tasarım standartlarını izlemesini sağlar.  
- **Otomasyona uygun:** Rapor, öğretici veya toplu işlenmiş defterler oluşturmak için idealdir.

## Önkoşullar

1. Aspose.Note for .NET: Aspose.Note for .NET'i [buradan](https://releases.aspose.com/note/net/) indirip kurun.  
2. Görüntü Dosyaları: Gömmeyi planladığınız görüntü dosyalarını (JPG, PNG vb.) diskte hazır bulundurun.

## Ad Alanlarını İçe Aktarın

Dosya G/Ç ve Aspose.Note API'sine erişim sağlayan ad alanlarını içe aktararak başlıyoruz.

```csharp
using System.IO;
using Aspose.Note;
using System.Collections.Generic;
using System.Drawing;
using System;
```

## Adım 1: Belgeyi Yükleyin ve Sayfayı Alın

İlk olarak, mevcut .one belgesini açın ve resmin yer alacağı sayfayı alın.

```csharp
string dataDir = "Your Document Directory";
Document doc = new Document(dataDir + "YourDocument.one");
Aspose.Note.Page page = doc.FirstChild;
```

## Görüntüyü Nasıl Hizalarız

Resmi eklemeden önce, diğer içerikle nasıl hizalanması gerektiğine karar verin. Aspose.Note yatay hizalama seçenekleri (Sol, Ortala, Sağ) sunar. Ayrıca konumu offset değerleriyle ince ayarlayabilirsiniz.

## Adım 2: Görüntüyü Yükleyin ve Özelliklerini Ayarlayın

Image nesnesini oluşturun, dosyanıza yönlendirin ve boyutlarını, offsetlerini ve hizalamasını tanımlayın.

```csharp
Aspose.Note.Image image = new Aspose.Note.Image(doc, dataDir + "image.jpg")
{
    Width = 100,                // Set image width
    Height = 100,               // Set image height
    HorizontalOffset = 100,     // Set horizontal offset
    VerticalOffset = 400,       // Set vertical offset
    Alignment = HorizontalAlignment.Right  // Set image alignment
};
```

## Görüntüyü Sayfaya Ekle

Görüntü tamamen yapılandırıldıktan sonra, sayfanın öğe ağacına ekleyin.

```csharp
page.AppendChildLast(image);
```

## Yaygın Hatalar ve İpuçları

- **Yanlış offsetler:** Offsetlerin sayfanın sol‑üst köşesinden ölçüldüğünü unutmayın. Büyük bir dikey offset, görüntüyü ekran dışına itebilir.  
- **Desteklenmeyen format:** Tanınmayan bir format denerseniz, Aspose.Note bir istisna fırlatır—dosyayı önce JPG veya PNG'ye dönüştürün.  
- **Lisans uyarıları:** Lisans olmadan çalıştırmak, oluşturulan belgeye bir filigran ekler; üretimde her zaman lisansınızı uygulayın.

## Sonuç

Artık bir Aspose.Note belgesine **görsel ekleme**, **görsel hizalama** ve **görseli sayfaya ekleme** konularını birkaç basit C# satırıyla öğrendiniz. Bu teknikler, daha zengin ve profesyonel defterler oluşturmanızı otomatikleştirir.

## SSS

### Q1: Aspose.Note belgelerine herhangi bir formatta görüntü ekleyebilir miyim?

A1: Evet, Aspose.Note JPG, PNG, BMP, GIF vb. dahil olmak üzere çeşitli görüntü formatlarını destekler.

### Q2: Eklenen görüntüleri programlı olarak yeniden boyutlandırmak mümkün mü?

A2: Kesinlikle! Görüntüleri ekleme sırasında genişlik ve yüksekliğini tercihlerinize göre ayarlayabilirsiniz.

### Q3: Aspose.Note görüntü hizalamasını değiştirme seçenekleri sunuyor mu?

A3: Evet, görüntüleri belge sayfalarınızda sola, sağa veya ortaya hizalayabilirsiniz.

### Q4: Belgemdeki tek bir sayfaya birden fazla görüntü ekleyebilir miyim?

A4: Elbette! Aspose.Note kullanarak tek bir sayfaya ihtiyacınız kadar görüntü ekleyebilirsiniz.

### Q5: Eklenebilecek görüntü dosyalarının boyutu için bir sınırlama var mı?

A5: Aspose.Note görüntü dosya boyutları üzerinde katı bir sınırlama getirmez, ancak daha iyi performans için görüntüleri optimize etmeniz önerilir.

## Frequently Asked Questions

**S: Bir dosya yolu yerine bir akıştan görüntüyü nasıl yüklerim?**  
C: Image(Stream, Document) yapıcısını kullanın ve görüntü baytlarını içeren bir MemoryStream geçirin.

**S: Görüntü sayfaya eklendikten sonra değiştirilebilir mi?**  
C: Evet, mevcut Image nesnesinin Width, Height, HorizontalOffset, VerticalOffset ve Alignment özelliklerini değiştirebilir ve ardından page.Update() çağırabilirsiniz.

**S: Görselin altına bir başlık eklemek mümkün mü?**  
C: RichText öğesini görüntünün ardından ekleyin ve metnini başlık olarak ayarlayın.

**S: Aspose.Note animasyonlu GIF'leri destekliyor mu?**  
C: Animasyonlu GIF'ler statik görüntü olarak işlenir; yalnızca ilk çerçeve gösterilir.

**S: Görsel bulanık görünüyorsa ne yapmalıyım?**  
C: Kaynak görüntünün yeterli çözünürlüğe sahip olduğundan emin olun ve orijinal boyutunun üzerine ölçeklendirmekten kaçının.

---

**Last Updated:** 2026-05-05  
**Tested With:** Aspose.Note 23.12 for .NET  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}
{{< blocks/products/products-backtop-button >}}