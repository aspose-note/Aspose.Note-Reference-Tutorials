---
title: Aspose.Note ile Ekli Dosyaları Alın
linktitle: Aspose.Note ile Ekli Dosyaları Alın
second_title: Aspose.Note .NET API'si
description: Aspose.Note for .NET'i kullanarak Microsoft OneNote belgelerinden ekli dosyaları nasıl alacağınızı öğrenin. Yükleme, düğüm alma ve ekleri yineleme adımlarını izleyin.
type: docs
weight: 12
url: /tr/net/attachments/retrieve-attached-files/
---
## giriiş

Bu eğitimde Aspose.Note for .NET kullanarak bir belgeden ekli dosyaların nasıl alınacağını inceleyeceğiz. Aspose.Note, geliştiricilerin Microsoft OneNote dosyalarıyla programlı olarak çalışmasına olanak tanıyan güçlü bir API'dir. Takip etmeyi kolaylaştırmak için süreci basit adımlara ayıracağız.

## Önkoşullar

Başlamadan önce aşağıdakilere sahip olduğunuzdan emin olun:

-  Aspose.Note for .NET: Aspose.Note for .NET'i yüklediğinizden emin olun. Şuradan indirebilirsiniz[Burada](https://releases.aspose.com/note/net/).

## Ad Alanlarını İçe Aktar

Öncelikle Aspose.Note ile çalışmak için gerekli ad alanlarını içe aktaralım:

```csharp
using System.IO;
using Aspose.Note;
using System;
using System.Collections.Generic;
using System.Drawing;
```

## 1. Adım: Belgeyi Yükleyin

```csharp
// Belgeler dizininin yolu.
string dataDir = "Your Document Directory";

// Belgeyi Aspose.Note'a yükleyin.
Document oneFile = new Document(dataDir + "Sample1.one");
```

## Adım 2: Ekli Dosya Düğümlerini Alın

```csharp
// Ekli dosya düğümlerinin listesini alın
IList<AttachedFile> nodes = oneFile.GetChildNodes<AttachedFile>();
```

## Adım 3: Ekli Dosyalar Üzerinden Yineleme Yapın

```csharp
// Tüm düğümler boyunca yineleme
foreach (AttachedFile file in nodes)
{
    // Ekli dosyayı bir akış nesnesine yükle
    using (Stream outputStream = new MemoryStream(file.Bytes))
    {
        // Yerel bir dosya oluşturun
        using (Stream fileStream = System.IO.File.OpenWrite(String.Format(dataDir + file.FileName)))
        {
            // Dosya akışını kopyala
            CopyStream(outputStream, fileStream);
        }
    }
}
```

## Çözüm

Bu eğitimde Aspose.Note for .NET kullanarak bir belgeden ekli dosyaların nasıl alınacağını öğrendik. Bu basit adımları izleyerek bu işlevselliği .NET uygulamalarınıza sorunsuz bir şekilde entegre edebilirsiniz.

## SSS'ler

### S1: Aspose.Note, OneNote dosyalarının tüm sürümleriyle uyumlu mudur?

Cevap1: Evet, Aspose.Note, Microsoft OneNote dosyalarının çeşitli sürümlerini destekleyerek farklı platformlar arasında uyumluluk sağlar.

### S2: Alınan ekli dosyaları yerel olarak kaydetmeden önce değiştirebilir miyim?

A2: Kesinlikle! Ekli dosyaları yerel olarak kaydetmeden önce uygulamanızda gerektiği gibi değiştirebilirsiniz.

### S3: Aspose.Note geliştiricilere destek sunuyor mu?

A3: Kesinlikle! Aspose, geliştiricilere karşılaştıkları herhangi bir soru veya sorun konusunda yardımcı olmak için kapsamlı belgeler ve özel bir destek forumu sağlar.

### S4: Aspose.Note'u satın almadan önce deneyebilir miyim?

Cevap4: Evet, satın alma kararını vermeden önce Aspose.Note'un özelliklerini ve işlevlerini keşfetmek için ücretsiz deneme sürümünden yararlanabilirsiniz.

### S5: Aspose.Note için nasıl geçici lisans alabilirim?

Cevap5: API'nin geliştirme ortamınızdaki tüm özelliklerini değerlendirmek için Aspose'tan geçici bir lisans talep edebilirsiniz.