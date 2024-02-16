---
title: Aspose.Note'ta Şablondan Belge Oluştur
linktitle: Aspose.Note'ta Şablondan Belge Oluştur
second_title: Aspose.Note .NET API'si
description: Aspose.Note for .NET ile dinamik belgeleri zahmetsizce oluşturun. Kişiselleştirilmiş ve veriye dayalı belge oluşturmak için adım adım kılavuzumuzu izleyin.
type: docs
weight: 18
url: /tr/net/text-manipulation/generate-document-from-template/
---
## giriiş
Aspose.Note for .NET, sürekli gelişen belge oluşturma ortamında, dinamik belgeleri zahmetsizce oluşturmak için güçlü bir araç olarak öne çıkıyor. İster raporlarla, ister faturalarla, ister kişiselleştirilmiş belgelerle ilgileniyor olun, bu eğitim size Aspose.Note for .NET kullanarak bir şablondan belge oluşturma sürecinde rehberlik edecektir.
## Önkoşullar
Adım adım kılavuza dalmadan önce aşağıdaki önkoşulların yerine getirildiğinden emin olun:
1.  Aspose.Note for .NET Kütüphanesi: Kütüphaneyi şuradan indirip yükleyin:[.NET belgeleri için Aspose.Note](https://reference.aspose.com/note/net/).
2. Belge Şablonu: OneNote formatında (.one uzantılı) bir şablon belgesi hazırlayın. Bu, dinamik olarak oluşturulan belgenizin temelini oluşturacaktır.
## Ad Alanlarını İçe Aktar
Projenize gerekli ad alanlarını eklediğinizden emin olun:
```csharp
    using System;
    using System.Collections.Generic;
    using System.IO;
```
Şimdi kılavuzdaki her adımı ayrı ayrı inceleyelim.
## 1. Adım: Belge Dizininizi Tanımlayın
```csharp
string dataDir = "Your Document Directory";
```
"Belge Dizininiz"i, oluşturulan belgenizi kaydetmek istediğiniz yolla değiştirin.
## Adım 2: Değiştirilen Değerlerle Bir Sözlük Oluşturun
```csharp
var templateData = new Dictionary<string, string>
{
    { "Company", "Atlas Shrugged Ltd" },
    { "CandidateName", "John Galt" },
    { "JobTitle", "Chief Entrepreneur Officer" },
    { "Department", "Sales" },
    { "Salary", "123456 USD" },
    { "Vacation", "30" },
    { "StartDate", "29 Feb 2024" },
    { "YourName", "Ayn Rand" }
};
```
Anahtarların şablonunuzdaki yer tutucular olduğu ve değerlerin de bunları değiştirmek istediğiniz veriler olduğu bir sözlük tanımlayın.

## 3. Adım: Şablon Belgesini Yükleyin
```csharp
var templateDocument = new Document(Path.Combine(dataDir, "JobOffer.one"));
```
OneNote şablon belgenizi Aspose.Note'a yükleyin.

## 4. Adım: Şablon Kelimelerini Dinamik Verilerle Değiştirin
```csharp
foreach (var paragraph in templateDocument.GetChildNodes<RichText>())
{
    foreach (var replacement in templateData)
    {
        paragraph.Replace($"${{{replacement.Key}}}", replacement.Value);
    }
}
```
Yer tutucuları dinamik verilerle değiştirerek şablondaki her paragrafı yineleyin.

## Adım 5: Oluşturulan Belgeyi Kaydedin
```csharp
templateDocument.Save(Path.Combine(dataDir, "JobOffer_out.one"));
```
Dinamik olarak oluşturulan belgeyi belirttiğiniz dizine kaydedin.

## Çözüm
Tebrikler! Aspose.Note for .NET'i kullanarak başarıyla dinamik bir belge oluşturdunuz. Bu süreç, kişiselleştirilmiş ve veriye dayalı belgeleri sorunsuz bir şekilde oluşturmak için bir fırsatlar dünyasının kapılarını açar.

## Sıkça Sorulan Sorular
### Aspose.Note for .NET'i diğer belge formatlarıyla kullanabilir miyim?
Evet, Aspose.Note for .NET öncelikle OneNote belgeleriyle ilgilenir, ancak Aspose farklı formatlar için çeşitli kütüphaneler sağlar.
### Aspose.Note for .NET'in ücretsiz deneme sürümü mevcut mu?
Evet, ücretsiz deneme sürümüyle Aspose.Note for .NET'in yeteneklerini keşfedebilirsiniz. Ziyaret etmek[Burada](https://releases.aspose.com/) daha fazla bilgi için.
### Aspose.Note for .NET için nasıl destek alabilirim?
 Ziyaret edin[.NET forumu için Aspose.Note](https://forum.aspose.com/c/note/28) toplumdan ve uzmanlardan yardım almak.
### Aspose.Note for .NET için geçici lisanslar mevcut mu?
 Evet, geçici lisans alabilirsiniz[Burada](https://purchase.aspose.com/temporary-license/) test ve değerlendirme amaçlıdır.
### Aspose.Note for .NET'in kapsamlı belgelerini nerede bulabilirim?
 Bakın[dokümantasyon](https://reference.aspose.com/note/net/) Aspose.Note for .NET kullanımı hakkında ayrıntılı bilgi için.