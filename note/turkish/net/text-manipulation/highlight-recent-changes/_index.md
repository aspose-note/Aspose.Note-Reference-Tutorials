---
title: Aspose.Note Metnindeki Tüm Son Değişiklikleri Vurgula
linktitle: Aspose.Note Metnindeki Tüm Son Değişiklikleri Vurgula
second_title: Aspose.Note .NET API'si
description: Note belgelerinizi Aspose.Note for .NET ile geliştirin! Bu adım adım eğitimle metindeki son değişiklikleri nasıl vurgulayacağınızı öğrenin.
type: docs
weight: 19
url: /tr/net/text-manipulation/highlight-recent-changes/
---
## giriiş
.NET'i kullanarak Note belgelerinize dinamik ve görsel olarak çekici özellikler mi eklemek istiyorsunuz? Aspose.Note for .NET, Note dosyalarınızı sorunsuz bir şekilde değiştirmenize ve geliştirmenize olanak tanıyan güçlü bir çözümdür. Bu eğitimde belirli bir hususu ele alacağız: Aspose.Note metnindeki tüm son değişiklikleri vurgulamak.
## Önkoşullar
Bu yolculuğa çıkmadan önce aşağıdaki önkoşulların mevcut olduğundan emin olun:
-  Aspose.Note for .NET: Aspose.Note kütüphanesinin kurulu olduğundan emin olun. adresinden indirebilirsiniz.[.NET belgeleri için Aspose.Note](https://reference.aspose.com/note/net/).
- Geliştirme Ortamı: Visual Studio gibi bir IDE de dahil olmak üzere bir .NET geliştirme ortamı kurun.
- Örnek Belge: Vurgulamak istediğiniz metni içeren bir Not belgesi hazırlayın (bu durumda "Aspose.one").
## Ad Alanlarını İçe Aktar
Başlamak için .NET projenize gerekli ad alanlarını içe aktarın:
```csharp
    using System;
    using System.Drawing;
    using System.IO;
    using System.Linq;
```
## 1. Adım: Belgeyi Yükleyin
Note belgesini Aspose.Note'a yükleyerek başlayın:
```csharp
string dataDir = "Your Document Directory";
Document document = new Document(dataDir + "Aspose.one");
```
## 2. Adım: Son Değişiklikleri Belirleyin
Ardından, geçen hafta içinde değiştirilen RichText düğümlerini tanımlayın:
```csharp
var richTextNodes = document.GetChildNodes<RichText>().Where(e => e.LastModifiedTime >= DateTime.Today.Subtract(TimeSpan.FromDays(7)));
```
## 3. Adım: Vurgu Renklerini Ayarlayın
Şimdi belirlenen düğümler ve metin çalıştırmaları için vurgu rengini ayarlayın:
```csharp
foreach (var node in richTextNodes)
{
    // Paragrafın vurgu rengini ayarlama
    node.ParagraphStyle.Highlight = Color.DarkGreen;
    // Her metin çalıştırması için vurgu rengini ayarlayın
    foreach (var run in node.TextRuns)
    {
        run.Style.Highlight = Color.DarkSeaGreen;
    }
}
```
## Adım 4: Değiştirilen Belgeyi Kaydedin
Belgeyi vurgulanan son değişikliklerle birlikte kaydedin:
```csharp
document.Save(Path.Combine(dataDir, "HighlightAllRecentChanges.pdf"));
```
## Adım 5: Başarı Mesajını Görüntüleyin
Son olarak kullanıcıyı bilgilendirmek için bir başarı mesajı görüntüleyin:
```csharp
Console.WriteLine("\nText's recent changes are highlighted successfully.");
```
## Çözüm
Bu eğitimde, bir Note belgesindeki metindeki tüm son değişiklikleri vurgulamak için Aspose.Note for .NET'in nasıl kullanılacağını araştırdık. Bu özellik belge görünürlüğünü artırır ve Not dosyalarıyla çalışmaya yönelik araç takımınıza değerli bir katkı sağlar.
## SSS
### Çeşitli zaman dilimleri için farklı vurgu renkleri uygulayabilir miyim?
Evet, özel gereksinimlerinize göre farklı vurgu renkleri ayarlamak için kodu özelleştirebilirsiniz.
### Aspose.Note en yeni .NET çerçeveleriyle uyumlu mu?
Aspose.Note, en yeni .NET çerçeveleriyle uyumluluğu sağlamak için kitaplıklarını düzenli olarak günceller.
### Bu özelliği uygularken hataları nasıl halledebilirim?
İstisnaları ele almak ve sorunsuz bir kullanıcı deneyimi sağlamak için try-catch bloklarını dahil edebilirsiniz.
### Aspose.Note diğer metin biçimlendirme özelliklerini destekliyor mu?
Kesinlikle! Aspose.Note, yazı tipi stilleri, boyutları ve daha fazlası dahil olmak üzere metin formatlama için çok çeşitli özellikler sunar.
### Bu çözümü bir web uygulamasına entegre edebilir miyim?
Evet, belge işleme yeteneklerini geliştirmek için Aspose.Note for .NET'i web uygulamalarına entegre edebilirsiniz.