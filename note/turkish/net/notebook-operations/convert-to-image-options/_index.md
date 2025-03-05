---
title: Aspose Note .NET'teki Seçeneklerle Not Defterlerini Görüntüye Dönüştürün
linktitle: Aspose Note .NET'teki Seçeneklerle Not Defterlerini Görüntüye Dönüştürün
second_title: Aspose.Note .NET API'si
description: Aspose.Note for .NET'i kullanarak not defterlerini özelleştirilebilir seçeneklerle görüntülere nasıl dönüştüreceğinizi öğrenin.
type: docs
weight: 13
url: /tr/net/notebook-operations/convert-to-image-options/
---
## giriiş

Bu eğitimde Aspose.Note for .NET kitaplığını kullanarak not defterlerini çeşitli seçeneklerle görüntülere dönüştürmeyi ele alacağız. Aspose.Note, geliştiricilerin Microsoft OneNote dosyalarıyla programlı olarak çalışmasına olanak tanıyan güçlü bir .NET API'sidir. Bu kılavuzda özetlenen adımları izleyerek, çıktıyı gereksinimlerinize göre özelleştirirken not defterlerini zahmetsizce görüntülere nasıl dönüştüreceğinizi öğreneceksiniz.

## Önkoşullar

Başlamadan önce aşağıdaki önkoşullara sahip olduğunuzdan emin olun:

1. Temel C# Bilgisi: Sağlanan kod parçacıklarını anlamak ve uygulamak için C# programlama diline aşina olmak çok önemlidir.

2.  Aspose.Note for .NET: Aspose.Note for .NET'i şu adresten indirip yükleyin:[İnternet sitesi](https://releases.aspose.com/note/net/). İhtiyaçlarınıza göre ücretsiz deneme sürümü alabilir veya lisans satın alabilirsiniz.

3. Geliştirme Ortamı: Tercih ettiğiniz geliştirme ortamını Visual Studio veya .NET geliştirmeyi destekleyen başka bir IDE ile kurun.

## Ad Alanlarını İçe Aktar

Başlamak için Aspose.Note for .NET ile çalışmak üzere gerekli ad alanlarını içe aktaralım.

```csharp
using System.IO;
using Aspose.Note;
using Aspose.Note.Saving;
using System;
using System.Collections.Generic;
```

Şimdi not defterlerini görüntülere dönüştürme işlemini seçeneklerle birden fazla adıma ayıralım.

## 1. Adım: Dizüstü Bilgisayarı Yükleyin

Öncelikle görüntüye dönüştürmek istediğiniz not defteri dosyasını yükleyin.

```csharp
// Belgeler dizininin yolu.
string dataDir = "Your Document Directory";

// OneNote Not Defteri Yükleme
var notebook = new Notebook(dataDir + "Notizbuch �ffnen.onetoc2");
```

## 2. Adım: Görüntü Kaydetme Seçeneklerini Ayarlayın

Not defterini resim olarak kaydetme seçeneklerini belirtin. Burada görüntü formatını PNG olarak ayarlayacağız ve çözünürlüğü özelleştireceğiz.

```csharp
var notebookSaveOptions = new NotebookImageSaveOptions(SaveFormat.Png);

var documentSaveOptions = notebookSaveOptions.DocumentSaveOptions;

documentSaveOptions.Resolution = 400;
```

## 3. Adım: Not Defterini Görüntü Olarak Kaydetme

Belirtilen seçenekleri kullanarak not defterini resim olarak kaydedin.

```csharp
dataDir = dataDir + "ConvertToImageWithOptions_out.png";

// Not Defterini Kaydet
notebook.Save(dataDir, notebookSaveOptions);
```

## Çözüm

Sonuç olarak, Aspose.Note for .NET kullanarak not defterlerini çeşitli seçeneklerle görüntülere nasıl dönüştürebileceğimizi araştırdık. Bu öğreticide özetlenen adımları izleyerek, bu işlevselliği .NET uygulamalarınıza sorunsuz bir şekilde entegre edebilir ve Microsoft OneNote dosyalarının verimli şekilde işlenmesini sağlayabilirsiniz.

## SSS'ler

### S1: Aspose.Note for .NET kullanarak birden fazla not defterini aynı anda dönüştürebilir miyim?

C1: Evet, birden çok not defteri dosyasını yineleyebilir ve bu eğitimde gösterilen benzer yöntemleri kullanarak bunları görüntülere dönüştürebilirsiniz.

### S2: Aspose.Note for .NET, .NET Core ile uyumlu mu?

C2: Evet, Aspose.Note for .NET, hem .NET Framework hem de .NET Core ortamlarıyla uyumludur.

### S3: Resimlere dönüştürülebilecek not defterlerinin boyutunda herhangi bir sınırlama var mı?

Cevap3: Aspose.Note for .NET, dönüştürülebilecek dizüstü bilgisayarların boyutuna özel sınırlamalar getirmez ancak performans, dizüstü bilgisayarın boyutuna ve karmaşıklığına bağlı olarak değişebilir.

### S4: Görüntü çıkışını çözünürlük ayarlarının ötesinde özelleştirebilir miyim?

Cevap4: Evet, Aspose.Note for .NET görüntü çıktısını özelleştirmek için kenar boşluklarını, renkleri ve sıkıştırma düzeylerini ayarlamak gibi çeşitli seçenekler sunar.

### S5: Aspose.Note for .NET PNG'nin yanı sıra diğer görüntü formatlarını da destekliyor mu?

C5: Evet, Aspose.Note for .NET, JPEG, BMP, GIF ve TIFF dahil çeşitli görüntü formatlarını destekler.