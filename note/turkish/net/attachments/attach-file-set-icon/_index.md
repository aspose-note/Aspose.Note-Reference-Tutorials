---
date: 2026-04-03
description: Aspose.Note for .NET'te özel simge ayarlamayı ve dosya eklemeyi öğrenin;
  OneNote dosyalarını kaydetme ve resimleri simge olarak kullanma da dahil.
keywords:
- set custom icon
- attach multiple files
- use image as icon
- save onenote file
- embed text file
linktitle: Aspose.Note'ta Dosya Ekle ve Simge Ayarla
second_title: Aspose.Note .NET API
title: Aspose.Note'ta Özel Simge Ayarla ve Dosya Ekle
url: /tr/net/attachments/attach-file-set-icon/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Note'ta Özel Simge Ayarlama ve Dosya Ekleme

## Giriş

If you need to **set custom icon** for an attachment in a OneNote page, Aspose.Note for .NET makes it straightforward. By attaching a file and assigning an image as its icon, you can create richer, more informative notes that look exactly the way you want. In this tutorial we’ll walk through the complete process—starting from a fresh document, adding an attachment, applying a custom JPEG icon, and finally saving the OneNote file.

## Hızlı Yanıtlar
- **“set custom icon” ne anlama geliyor?** Varsayılan ek dosya küçük resmini sağladığınız bir görüntüyle değiştirmenizi sağlar.  
- **Birden fazla dosya ekleyebilir miyim?** Evet, her dosya için ekleme adımlarını tekrarlayın.  
- **Simgeler için hangi görüntü formatları destekleniyor?** JPEG, PNG, BMP veya GIF gibi .NET uyumlu herhangi bir format.  
- **Bir lisansa ihtiyacım var mı?** Üretim kullanımı için geçerli bir Aspose.Note lisansı gerekir; ücretsiz deneme sürümü değerlendirme için çalışır.  
- **OneNote dosyasını nasıl kaydederim?** `Document.Save()` metodunu kullanın ve *.one* dosya yolunu belirtin.

## Aspose.Note'ta “set custom icon” nedir?
Özel bir simge ayarlamak, ekli bir dosyayı OneNote sayfasında temsil etmek için belirli bir görüntü (ör. JPEG) atamak anlamına gelir. Bu, kullanıcılar için görsel ipuçlarını geliştirir ve dosya türü logolarını veya marka görsellerini göstermek için kullanılabilir.

## Ek dosyalar için neden özel bir simge ayarlamalıyız?
- **Daha iyi görsel bağlam:** Kullanıcılar ekli dosyanın türünü veya amacını anında tanır.  
- **Marka tutarlılığı:** Şirketinizin logosunu ilgili tüm belgeler için simge olarak kullanın.  
- **Geliştirilmiş kullanıcı deneyimi:** Notların özellikle paylaşılan defterlerde daha şık ve profesyonel görünmesini sağlar.

## Önkoşullar
- C# programlama temelleri hakkında bilgi.  
- Aspose.Note for .NET kütüphanesi yüklü.  
- Visual Studio (veya herhangi bir .NET uyumlu IDE) geliştirme için hazır.

## Ad Alanlarını İçe Aktarma
İlk olarak, dosyalar, görüntüler ve OneNote nesneleriyle çalışabilmek için gerekli ad alanlarını kapsam içine alın.

```csharp
using System.IO;
using Aspose.Note;
using System;
using System.Collections.Generic;
using System.Drawing.Imaging;
```

## Dosya Ekleme ve Simge Ayarlama İçin Adım Adım Kılavuz

### Adım 1: Document Nesnesi Oluşturma
Yeni bir `Document` örneği, oluşturacağınız OneNote dosyasını temsil eder.

```csharp
Document doc = new Document();
```

### Adım 2: Page Nesnesini Başlatma
Her OneNote dosyası bir veya daha fazla sayfa içerir. Burada ilk sayfayı oluşturuyoruz.

```csharp
Aspose.Note.Page page = new Aspose.Note.Page(doc);
```

### Adım 3: Outline Nesnesini Başlatma
Outline'lar, bir sayfadaki içerik blokları için kapsayıcı görevi görür.

```csharp
Outline outline = new Outline(doc);
```

### Adım 4: OutlineElement Nesnesini Başlatma
Bu öğe, ekli dosyayı ve özel simgesini tutacaktır.

```csharp
OutlineElement outlineElem = new OutlineElement(doc);
```

### Adım 5: Simge Görüntüsünü Okuma ve AttachedFile Nesnesini Başlatma
Görüntü akışını (özel simge) açar ve gömmek istediğimiz dosyayı işaret ederiz.

```csharp
string dataDir = "Your Document Directory";
using (var stream = File.OpenRead(dataDir + "icon.jpg"))
{
    AttachedFile attachedFile = new AttachedFile(doc, dataDir + "attachment.txt", stream, ImageFormat.Jpeg);
}
```

> **Pro tip:** PNG simgesi tercih ediyorsanız `ImageFormat.Jpeg` yerine `ImageFormat.Png` kullanın.

### Adım 6: Attached File'ı OutlineElement'e Ekleme
Şimdi dosya (simge ile birlikte) outline öğesinin bir alt öğesi olur.

```csharp
outlineElem.AppendChildLast(attachedFile);
```

### Adım 7: OutlineElement'i Outline'a Ekleme
Bu, öğeyi outline kapsayıcısının içine yerleştirir.

```csharp
outline.AppendChildLast(outlineElem);
```

### Adım 8: Outline'ı Page'e Ekleme
Tüm outline hiyerarşisini sayfaya ekleyin.

```csharp
page.AppendChildLast(outline);
```

### Adım 9: Page'i Document'e Ekleme
Tamamlanmış sayfayı belge yapısına ekleyin.

```csharp
doc.AppendChildLast(page);
```

### Adım 10: OneNote Belgesini Kaydetme
Son olarak, belgeyi *.one* dosyası olarak diske yazın.

```csharp
dataDir = dataDir + "AttachFileAndSetIcon_out.one";
doc.Save(dataDir);
```

## Yaygın Kullanım Durumları
- **Sözleşme ekleme:** PDF ekleyin ve sözleşme logosu simgesi kullanın.  
- **Kod parçacıkları paylaşma:** `.txt` dosyasını özel bir “kod” simgesiyle ekleyin.  
- **Proje dokümantasyonu:** Tasarım dosyalarını ekleyin ve dosya türüne uygun bir küçük resim ayarlayın.

## Yaygın Sorunlar ve Çözümler

| Sorun | Çözüm |
|-------|----------|
| **Simge görünmüyor** | Geçirdiğiniz `ImageFormat` ile görüntü formatının eşleştiğini doğrulayın (ör. JPEG vs PNG). |
| **Dosya yolu hataları** | `Path.Combine(dataDir, "file.ext")` kullanarak eksik eğik çizgi sorunlarından kaçının. |
| **Büyük ek dosyalar performans gecikmesine neden olur** | Dosyayı önceden sıkıştırın veya birden fazla küçük ek dosyaya bölün. |

## Sıkça Sorulan Sorular

**Q: Aspose.Note for .NET kullanarak tek bir nota birden fazla dosya ekleyebilir miyim?**  
**A:** Evet. Her dosya için “Simge Görüntüsünü Okuma ve AttachedFile Nesnesini Başlatma” bloğunu tekrarlayın ve her `AttachedFile`'ı aynı `OutlineElement`'e ekleyin veya ayrı öğeler oluşturun.

**Q: Dosya ekleri için özel simgeler ayarlamak mümkün mü?**  
**A:** Kesinlikle. `AttachedFile` yapıcı yöntemi, bir görüntü akışı geçirmenize ve görüntü formatını belirtmenize olanak tanır, böylece simge üzerinde tam kontrol sahibi olursunuz.

**Q: Aspose.Note, simge ayarlamak için başka görüntü formatlarını destekliyor mu?**  
**A:** Evet. JPEG'in yanı sıra PNG, BMP, GIF veya `System.Drawing.Imaging.ImageFormat` tarafından desteklenen herhangi bir formatı kullanabilirsiniz.

**Q: Dış URL'lerden dosya ekleyebilir miyim?**  
**A:** Aspose.Note yerel akışlarla çalışsa da, bir dosyayı `HttpClient` ile indirip bir `MemoryStream` içinde saklayabilir ve ardından bu akışı `AttachedFile`'a geçirebilirsiniz.

**Q: Dosya ekleri için bir boyut sınırlaması var mı?**  
**A:** Aspose.Note kendisi katı bir sınırlama getirmez, ancak çok büyük dosyalar bellek kullanımı ve performansı etkileyebilir. Büyük ek dosyaları sıkıştırmayı düşünün.

---

**Son Güncelleme:** 2026-04-03  
**Test Edilen Versiyon:** Aspose.Note 24.11 for .NET  
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}