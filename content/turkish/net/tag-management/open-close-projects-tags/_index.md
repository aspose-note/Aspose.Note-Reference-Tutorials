---
title: Aspose.Note'ta Projeleri Etiketlerle Açma ve Kapatma
linktitle: Aspose.Note'ta Projeleri Etiketlerle Açma ve Kapatma
second_title: Aspose.Note .NET API'si
description: Aspose.Note for .NET'i kullanarak Microsoft OneNote dosyalarını programlı olarak nasıl değiştireceğinizi öğrenin. Projeleri etiketlerle verimli bir şekilde açın ve kapatın.
type: docs
weight: 15
url: /tr/net/tag-management/open-close-projects-tags/
---
## giriiş

Bu eğitimde, etiketleri olan projeleri açmak ve kapatmak için Aspose.Note for .NET'i nasıl kullanacağımızı öğreneceğiz. Aspose.Note, geliştiricilerin Microsoft OneNote dosyalarıyla programlı olarak çalışmasına olanak tanıyan, belgelerdeki metin, resim ve etiketleri değiştirme gibi görevleri mümkün kılan güçlü bir API'dir.

## Önkoşullar

Başlamadan önce aşağıdaki önkoşulları oluşturduğunuzdan emin olun:

## Ad Alanlarını İçe Aktar

```csharp
using System.IO;
using System.Linq;
```

Şimdi her örneği birden fazla adıma ayıralım:

## 1. Adım: Belgeyi Yükleyin

Öncelikle belgeyi Aspose.Note'a yüklememiz gerekiyor.

```csharp
string dataDir = "Your Document Directory";
var oneFile = new Document(Path.Combine(dataDir, "ProjectNotes.one"));
```

## Adım 2: Proje C Öğelerini Kapatın

Şimdi 'Proje C' ile ilgili tüm onay kutusu öğelerini kapatalım.

```csharp
foreach (var node in oneFile.GetChildNodes<ITaggable>())
{
    foreach (var checkBox in node.Tags.OfType<CheckBox>())
    {
        if (checkBox.Label.Contains("Project C") && !checkBox.Checked)
        {
            checkBox.SetCompleted();
        }
    }
}
```

## Adım 3: Kapalı Proje C Notlarını Kaydedin

Değiştirilen belgeyi kapalı 'Proje C' öğeleriyle kaydedin.

```csharp
oneFile.Save("Path to save the closed Project C notes");
```

## Adım 4: Proje C Öğelerini Açın

Daha sonra 'Proje C' ile ilgili tüm onay kutusu öğelerini açalım.

```csharp
var oneFile = new Document("Path to the closed Project C notes");

foreach (var node in oneFile.GetChildNodes<ITaggable>())
{
    foreach (var checkBox in node.Tags.OfType<CheckBox>())
    {
        if (checkBox.Label.Contains("Project C") && checkBox.Checked)
        {
            checkBox.SetOpen();
        }
    }
}
```

## Adım 5: Açık Proje C Notlarını Kaydedin

Değiştirilen belgeyi açılan 'Proje C' öğeleriyle birlikte kaydedin.

```csharp
oneFile.Save(Path.Combine(dataDir, "ProjectNoteWithOpenProjectC.one"));
```

Artık Aspose.Note'ta .NET kullanarak etiketleri olan projeleri nasıl açıp kapatacağınızı öğrendiniz.

## Çözüm

Aspose.Note for .NET, OneNote belgelerini programlı olarak işlemek için kullanışlı bir yol sağlar. Bu öğreticiyi takip ederek, etiketleri kullanarak öğeleri açıp kapatarak projelerinizi verimli bir şekilde yönetebilirsiniz.

## SSS'ler

### S1: Aspose.Note, OneNote'un tüm sürümleriyle uyumlu mudur?

Cevap1: Aspose.Note, Microsoft OneNote 2010 ve daha yeni sürümleri destekler.

### S2: Aspose.Note'u ticari projeler için kullanabilir miyim?

 Cevap2: Evet, Aspose.Note'u hem kişisel hem de ticari projeleriniz için kullanabilirsiniz. Ziyaret etmek[Burada](https://purchase.aspose.com/buy) lisans satın almak için.

### S3: Aspose.Note ücretsiz deneme sunuyor mu?

A3: Evet, ücretsiz deneme sürümünden yararlanabilirsiniz[Burada](https://releases.aspose.com/).

### S4: Aspose.Note belgelerini nerede bulabilirim?

 A4: Belgeleri bulabilirsiniz[Burada](https://reference.aspose.com/note/net/).

### S5: Aspose.Note için nereden destek alabilirim?

Cevap5: Destek için Aspose.Note'u ziyaret edebilirsiniz.[forum](https://forum.aspose.com/c/note/28).