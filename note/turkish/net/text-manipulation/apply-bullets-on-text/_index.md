---
title: Aspose.Note'ta Metne Madde İşaretleri Uygula
linktitle: Aspose.Note'ta Metne Madde İşaretleri Uygula
second_title: Aspose.Note .NET API'si
description: OneNote belgelerinizi geliştirmek için Aspose.Note for .NET'te metne madde işaretlerini nasıl uygulayacağınızı öğrenin. Etkili biçimlendirme için bu adım adım kılavuzu izleyin.
weight: 10
url: /tr/net/text-manipulation/apply-bullets-on-text/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Note'ta Metne Madde İşaretleri Uygula

## giriiş
Aspose.Note for .NET kullanarak metne madde işaretleri uygulamayla ilgili bu adım adım kılavuza hoş geldiniz. Aspose.Note, geliştiricilerin .NET uygulamalarında Microsoft OneNote dosyalarıyla sorunsuz bir şekilde çalışmasına olanak tanıyan güçlü bir kitaplıktır. Bu eğitimde, OneNote belgelerinizin görsel çekiciliğini artırmak için metne madde işaretleri uygulama sürecinde size yol göstereceğiz.
## Önkoşullar
Eğiticiye dalmadan önce aşağıdaki önkoşullara sahip olduğunuzdan emin olun:
- Temel C# ve .NET programlama bilgisi.
-  Aspose.Note for .NET kütüphanesi kuruldu. İndirebilirsin[Burada](https://releases.aspose.com/note/net/).
## Ad Alanlarını İçe Aktar
C# kodunuzda gerekli ad alanlarını eklediğinizden emin olun:
```csharp
using System;
using System.Globalization;
using System.IO;
using Aspose.Note;
using System.Drawing;
using System.Collections.Generic;
```
## 1. Adım: Belgenizi Ayarlayın
```csharp
// Belgeler dizininin yolu.
string dataDir = "Your Document Directory";
//Document sınıfının bir nesnesini oluşturun
Aspose.Note.Document doc = new Aspose.Note.Document();
```
## Adım 2: Sayfayı ve Anahattı Başlatın
```csharp
// Sayfa sınıfı nesnesini başlat
Aspose.Note.Page page = new Aspose.Note.Page(doc);
// Outline sınıfı nesnesini başlat
Outline outline = new Outline(doc);
```
## 3. Adım: Varsayılan Metin Stilini Ayarlayın
```csharp
// TextStyle sınıfı nesnesini başlatın ve biçimlendirme özelliklerini ayarlayın
ParagraphStyle defaultStyle = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
```
## Adım 4: Madde İşaretleriyle Anahat Öğeleri Oluşturun
```csharp
// OutlineElement sınıfı nesnelerini başlatın ve madde işaretleri uygulayın
OutlineElement outlineElem1 = new OutlineElement(doc) { NumberList = new NumberList("*", "Arial", 10) };
RichText text1 = new RichText(doc) { Text = "First", ParagraphStyle = defaultStyle };
outlineElem1.AppendChildLast(text1);
// Diğer anahat öğeleri için tekrarlayın
```
## Adım 5: Anahat'a Anahat Öğeleri Ekleme
```csharp
// Anahat öğeleri ekleme
outline.AppendChildLast(outlineElem1);
// Diğer anahat öğeleri için tekrarlayın
```
## Adım 6: Sayfaya Anahat Ekleyin
```csharp
// Anahat düğümü ekle
page.AppendChildLast(outline);
```
## Adım 7: Belgeye Sayfa Ekleme
```csharp
//Sayfa düğümü ekle
doc.AppendChildLast(page);
```
## Adım 8: OneNote Belgesini Kaydetme
```csharp
// OneNote belgesini kaydet
dataDir = dataDir + "ApplyBulletsOnText_out.one"; 
doc.Save(dataDir);
Console.WriteLine("\nBullets applied successfully on a text.\nFile saved at " + dataDir); 
```
## Çözüm
Tebrikler! Aspose.Note for .NET'i kullanarak metne madde işaretlerinin nasıl uygulanacağını başarıyla öğrendiniz. Bu özellik, OneNote belgelerinizin biçimlendirmesini önemli ölçüde geliştirerek onları görsel olarak daha çekici hale getirebilir.
## SSS'ler
### Listedeki her öğeye farklı madde işareti stilleri uygulayabilir miyim?
 Evet, madde işareti stillerini değiştirerek özelleştirebilirsiniz.`NumberList` her biri için özellikler`OutlineElement`.
### Aspose.Note, Microsoft OneNote'un en son sürümüyle uyumlu mu?
Aspose.Note, Microsoft OneNote'un çeşitli sürümlerini destekleyerek hem eski hem de yeni sürümlerle uyumluluk sağlar.
### Aspose.Note'u ticari amaçlarla kullanabilir miyim?
 Evet, Aspose.Note for .NET'i ticari projelerde kullanabilirsiniz. Lisans almak için şu adresi ziyaret edin:[Burada](https://purchase.aspose.com/buy).
### Aspose.Note for .NET'in deneme sürümü mevcut mu?
 Evet, ücretsiz deneme sürümünü indirebilirsiniz[Burada](https://releases.aspose.com/).
### Ek destek ve kaynakları nerede bulabilirim?
 Aspose.Note topluluk forumunu ziyaret edebilirsiniz[Burada](https://forum.aspose.com/c/note/28) Destek ve tartışmalar için.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
