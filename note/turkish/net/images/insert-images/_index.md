---
title: Aspose.Note Belgelerine Görüntü Ekleme
linktitle: Aspose.Note Belgelerine Görüntü Ekleme
second_title: Aspose.Note .NET API'si
description: Gelişmiş görsel içerik için .NET'i kullanarak görüntüleri Aspose.Note belgelerine sorunsuz bir şekilde nasıl ekleyeceğinizi öğrenin. Kolay entegrasyon için adım adım kılavuzumuzu izleyin.
weight: 16
url: /tr/net/images/insert-images/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Note Belgelerine Görüntü Ekleme

## giriiş

Aspose.Note belgelerinize görsel eklemek, görsel çekiciliğini ve kullanışlılığını büyük ölçüde artırabilir. İster notlar, sunumlar, ister başka bir belge oluşturuyor olun, resimleri entegre etmek içeriğinize bağlam ve netlik sağlayabilir. Bu eğitimde, .NET kullanarak Aspose.Note belgelerinize resim ekleme sürecinde size rehberlik edeceğiz.

## Önkoşullar

Başlamadan önce aşağıdaki önkoşulların mevcut olduğundan emin olun:

1.  Aspose.Note for .NET: Aspose.Note for .NET'i şu adresten indirip yükleyin:[Burada](https://releases.aspose.com/note/net/).
   
2. Görüntü Dosyaları: Aspose.Note belgelerinize eklemeyi düşündüğünüz görüntü dosyalarını hazırlayın.

## Ad Alanlarını İçe Aktar

Öncelikle .NET projenizde Aspose.Note ile çalışmak için gerekli ad alanlarını içe aktarmanız gerekir. Bunu nasıl yapabileceğiniz aşağıda açıklanmıştır:

```csharp
using System.IO;
using Aspose.Note;
using System.Collections.Generic;
using System.Drawing;
using System;
```

## 1. Adım: Belgeyi Yükleyin ve Sayfayı Alın

Mevcut Aspose.Note belgenizi yükleyerek ve görüntüyü eklemek istediğiniz sayfaya erişerek başlayın.

```csharp
string dataDir = "Your Document Directory";
Document doc = new Document(dataDir + "YourDocument.one");
Aspose.Note.Page page = doc.FirstChild;
```

## 2. Adım: Görüntüyü Yükleyin ve Özellikleri Ayarlayın

Daha sonra eklemek istediğiniz görüntüyü yükleyin ve gereksinimlerinize göre genişlik, yükseklik, uzaklıklar ve hizalama gibi özelliklerini belirtin.

```csharp
Aspose.Note.Image image = new Aspose.Note.Image(doc, dataDir + "image.jpg")
{
    Width = 100,                // Resim genişliğini ayarla
    Height = 100,               // Görüntü yüksekliğini ayarla
    HorizontalOffset = 100,     // Yatay ofseti ayarla
    VerticalOffset = 400,       // Dikey ofseti ayarla
    Alignment = HorizontalAlignment.Right  // Görüntü hizalamasını ayarlayın
};
```

## 3. Adım: Sayfaya Resim Ekleme

Görüntü özelliklerini yapılandırdıktan sonra görüntüyü Aspose.Note belgenizin istediğiniz sayfasına ekleyin.

```csharp
page.AppendChildLast(image);
```

## Çözüm

Tebrikler! Aspose.Note belgenize .NET'i kullanarak başarıyla bir görüntü eklediniz. Resimler, belgelerinizin görsel sunumunu önemli ölçüde iyileştirerek onları daha ilgi çekici ve bilgilendirici hale getirebilir.

## SSS'ler

### S1: Aspose.Note belgelerine herhangi bir formattaki görselleri ekleyebilir miyim?

Cevap1: Evet, Aspose.Note JPG, PNG, BMP, GIF vb. gibi çeşitli görüntü formatlarını destekler.

### S2: Eklenen görüntüleri programlı olarak yeniden boyutlandırmak mümkün mü?

A2: Kesinlikle! Ekleme sırasında görsellerin genişliğini ve yüksekliğini tercihlerinize göre ayarlayabilirsiniz.

### S3: Aspose.Note görüntü hizalamasını değiştirme seçenekleri sunuyor mu?

C3: Evet, belge sayfalarınızda görüntüleri sola, sağa veya ortaya hizalayabilirsiniz.

### S4: Belgemin tek bir sayfasına birden fazla resim ekleyebilir miyim?

A4: Kesinlikle! Aspose.Note'u kullanarak tek bir sayfaya istediğiniz kadar görsel ekleyebilirsiniz.

### S5: Eklenebilecek görsellerin dosya boyutunda bir sınır var mı?

Cevap5: Aspose.Note, görüntü dosyası boyutlarına katı sınırlamalar getirmez ancak daha iyi performans için görüntülerin optimize edilmesi önerilir.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
