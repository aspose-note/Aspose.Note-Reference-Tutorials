---
title: Aspose.Note Metninde Madde İşareti veya Numara Listesini Alma
linktitle: Aspose.Note Metninde Madde İşareti veya Numara Listesini Alma
second_title: Aspose.Note .NET API'si
description: Madde işareti veya sayı listelerini almaya yönelik adım adım kılavuzumuzla Aspose.Note for .NET'in potansiyelini ortaya çıkarın. OneNote belge işleme becerilerinizi geliştirin!
weight: 23
url: /tr/net/text-manipulation/retrieve-bullet-number-list/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Note Metninde Madde İşareti veya Numara Listesini Alma

## giriiş
Geliştiricilerin OneNote belge manipülasyonunu zahmetsizce gerçekleştirmesine olanak tanıyan sağlam ve çok yönlü bir kitaplık olan Aspose.Note for .NET dünyasına hoş geldiniz. Bu eğitimde, Aspose.Note for .NET'i kullanarak madde işareti veya sayı listelerini alma sürecini derinlemesine inceleyeceğiz. İster deneyimli bir geliştirici olun ister kodlama meraklısı olun, bu kılavuz sizi Aspose.Note'ta listelerle çalışmanın inceliklerinde gezinmenizi sağlayacak bilgiyle donatacaktır.
## Önkoşullar
Bu kodlama yolculuğuna çıkmadan önce aşağıdaki önkoşulların mevcut olduğundan emin olun:
-  Aspose.Note for .NET: Aspose.Note kütüphanesinin kurulu olduğundan emin olun. Değilse, adresinden indirebilirsiniz.[.NET belgeleri için Aspose.Note](https://reference.aspose.com/note/net/).
- Geliştirme Ortamı: Makinenizde çalışan bir geliştirme ortamı, tercihen Microsoft Visual Studio'yu kurun.
- Temel C# Bilgisi: Bu eğitim bu dilde yazıldığı için C#'a aşina olun.
## Ad Alanlarını İçe Aktar
Aspose.Note for .NET ile etkileşim kurabilmek için gerekli ad alanlarını projenize aktarmanız gerekir. Kodunuzun başına aşağıdaki ad alanlarını ekleyin:
```csharp
using System;
using System.Globalization;
using System.IO;
using Aspose.Note;
using System.Collections.Generic;
```
Şimdi madde işareti veya numara listelerini alma sürecini adım adım inceleyelim:
## 1. Adım: Belge Dizininizi Ayarlayın
```csharp
// Belgeler dizininin yolu.
string dataDir = "Your Document Directory";
```
 Yer değiştirmek`"Your Document Directory"` Aspose.Note belgenizin bulunduğu gerçek yolla.
## Adım 2: Belgeyi Yükleyin
```csharp
// Belgeyi Aspose.Note'a yükleyin.
Document oneFile = new Document(dataDir + "ApplyNumberingOnText.one");
```
 Değiştirdiğinizden emin olun`"ApplyNumberingOnText.one"` özel OneNote belgenizin adıyla birlikte.
## 3. Adım: Düğüm Koleksiyonunu Alın
```csharp
// Anahat öğesinin düğümlerinin bir koleksiyonunu alın.
IList<OutlineElement> nodes = oneFile.GetChildNodes<OutlineElement>();
```
Bu adım, yüklenen belgeden anahat düğümlerinin bir koleksiyonunu alır.
## Adım 4: Her Düğümde Yineleme Yapın
```csharp
// Her düğümde yineleme yapın.
foreach (OutlineElement node in nodes)
{
    if (node.NumberList != null)
    {
        NumberList list = node.NumberList;
        // Sonraki adımlara geçin...
    }
}
```
Bu döngü yalnızca sayı listesi içeren düğümlerle ilgilenmemizi sağlar.
## Adım 5: Yazı Tipi Bilgilerini Alın
```csharp
// Yazı tipi adını al
Console.WriteLine("Font Name: " + list.Font);
// Yazı tipi uzunluğunu al
Console.WriteLine("Font Length: " + list.Font.Length);
// Yazı tipi boyutunu al
Console.WriteLine("Font Size: " + list.FontSize);
// Yazı tipi rengini al
Console.WriteLine("Font Color: " + list.FontColor);
// Formatı al
Console.WriteLine("Font format: " + list.Format);
// Kalın olarak kontrol edin
Console.WriteLine("Is bold: " + list.IsBold);
// İtalik kontrol edin
Console.WriteLine("Is italic: " + list.IsItalic);
Console.WriteLine();
```
Bu kod satırları, sayı listesinden yazı tipiyle ilgili çeşitli bilgileri çıkarır.
## Çözüm
 Tebrikler! Aspose.Note for .NET'i kullanarak madde işareti veya sayı listelerini nasıl alacağınızı başarıyla öğrendiniz. Araştırmanıza devam ederken, bkz.[dokümantasyon](https://reference.aspose.com/note/net/) Daha ayrıntılı bilgiler ve işlevler için.
## SSS'ler
### Aspose.Note for .NET'i diğer programlama dilleriyle birlikte kullanabilir miyim?
Aspose.Note öncelikle .NET'i destekler ancak kütüphanenin farklı platformlar ve diller için uyarlanmış başka sürümleri de vardır.
### Aspose.Note en son OneNote formatlarıyla uyumlu mu?
Evet, Aspose.Note çok çeşitli OneNote formatlarını destekleyerek en son sürümlerle uyumluluk sağlar.
### Aspose.Note için nasıl geçici lisans alabilirim?
 Ziyaret etmek[bu bağlantı](https://purchase.aspose.com/temporary-license/) değerlendirme amacıyla geçici bir lisans almak.
### Aspose.Note kullanıcıları için hangi destek seçenekleri mevcut?
Şurayı keşfedebilir ve yardım isteyebilirsiniz:[Aspose.Note forumu](https://forum.aspose.com/c/note/28) Karşılaşabileceğiniz her türlü soru veya sorun için.
### Aspose.Note for .NET'in ücretsiz deneme sürümü var mı?
 Evet, Aspose.Note for .NET'in ücretsiz deneme sürümüne erişebilirsiniz[Burada](https://releases.aspose.com/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
