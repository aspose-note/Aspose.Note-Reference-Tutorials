---
title: Aspose.Note'ta Belirtilen Yazı Tiplerini Kullanarak Kaydetme
linktitle: Aspose.Note'ta Belirtilen Yazı Tiplerini Kullanarak Kaydetme
second_title: Aspose.Note .NET API'si
description: Aspose.Note for .NET'te belirli yazı tiplerine sahip belgeleri nasıl kaydedeceğinizi öğrenin. Tutarlı belge biçimlendirmesi için yazı tipi ayarlarını kolayca özelleştirin.
weight: 28
url: /tr/net/loading-and-saving-operations/save-using-specified-fonts/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Note'ta Belirtilen Yazı Tiplerini Kullanarak Kaydetme

## giriiş

Bu eğitimde, Aspose.Note for .NET'te belirtilen yazı tiplerini kullanarak belgeleri nasıl kaydedeceğimizi öğreneceğiz. Bunu başarmak için farklı yöntemleri adım adım inceleyeceğiz.

## Önkoşullar

Başlamadan önce aşağıdakilere sahip olduğunuzdan emin olun:

1.  Aspose.Note for .NET: Aspose.Note for .NET'i yüklediğinizden emin olun. Şuradan indirebilirsiniz[Burada](https://releases.aspose.com/note/net/).

2. Geliştirme Ortamı: .NET geliştirme için kurulmuş bir geliştirme ortamına ihtiyacınız var.

## Ad Alanlarını İçe Aktar

Öncelikle gerekli ad alanlarını içe aktaralım:

```csharp
using System;
using System.IO;

using Aspose.Note.Fonts;
using Aspose.Note.Saving;

```

## Adım 1: Varsayılan Yazı Tipi Adıyla Kaydetme

Bu adımda, belirtilen varsayılan yazı tipi adını kullanarak bir belgeyi kaydedeceğiz.

```csharp
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontName()
{
    // Belgeler dizininin yolu.
    string dataDir = "Your Document Directory";

    // Belgeyi Aspose.Note'a yükleyin.
    Document oneFile = new Document(Path.Combine(dataDir, "missing-font.one"));

    // Belgeyi belirtilen varsayılan yazı tipiyle PDF olarak kaydedin.
    dataDir = dataDir + "SaveUsingDocumentFontsSubsystemWithDefaultFontName_out.pdf";
    oneFile.Save(dataDir, new PdfSaveOptions()
                          {
                              FontsSubsystem = DocumentFontsSubsystem.UsingDefaultFont("Times New Roman")
                          });
}
```

## Adım 2: Dosyadan Varsayılan Yazı Tipiyle Kaydetme

Sonra, bir dosyadan yüklenen varsayılan yazı tipini kullanarak belgeyi kaydedelim.

```csharp
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontFromFile()
{
    // Belgeler dizininin yolu.
    string dataDir = "Your Document Directory";

    string fontFile = Path.Combine(dataDir, "geo_1.ttf");

    // Belgeyi Aspose.Note'a yükleyin.
    Document oneFile = new Document(Path.Combine(dataDir, "missing-font.one"));

    // Belgeyi, dosyadan yüklenen varsayılan yazı tipiyle PDF olarak kaydedin.
    dataDir = dataDir + "SaveUsingDocumentFontsSubsystemWithDefaultFontFromFile_out.pdf";
    oneFile.Save(dataDir, new PdfSaveOptions()
                          {
                              FontsSubsystem = DocumentFontsSubsystem.UsingDefaultFontFromFile(fontFile)
                          });
}
```

## 3. Adım: Akıştan Varsayılan Yazı Tipiyle Kaydetme

Son olarak, bir akıştan yüklenen varsayılan yazı tipini kullanarak bir belgeyi kaydedelim.

```csharp
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontFromStream()
{
    // Belgeler dizininin yolu.
    string dataDir = "Your Document Directory";

    string fontFile = Path.Combine(dataDir, "geo_1.ttf");

    // Belgeyi Aspose.Note'a yükleyin.
    Document oneFile = new Document(Path.Combine(dataDir, "missing-font.one"));

    // Belgeyi akıştan yüklenen varsayılan yazı tipiyle PDF olarak kaydedin.
    dataDir = dataDir + "SaveUsingDocumentFontsSubsystemWithDefaultFontFromStream_out.pdf";

    using (var stream = File.Open(fontFile, FileMode.Open, FileAccess.Read, FileShare.Read))
    {
        oneFile.Save(dataDir, new PdfSaveOptions()
                              {
                                  FontsSubsystem = DocumentFontsSubsystem.UsingDefaultFontFromStream(stream)
                              });
    }
}
```

## Çözüm

Bu eğitimde Aspose.Note for .NET'te belirtilen yazı tiplerini kullanarak belgelerin nasıl kaydedileceğini araştırdık. Bu adımları izleyerek yazı tipi ayarlarını gereksinimlerinize göre özelleştirerek belgelerinizin istediğiniz gibi biçimlendirilmesini sağlayabilirsiniz.

## SSS'ler

### S1: Aspose.Note'ta belgeleri kaydetmek için herhangi bir yazı tipi kullanabilir miyim?

Cevap1: Evet, belgeleri kaydetmek için herhangi bir yazı tipini belirtebilirsiniz. Yazı tipi dosyasının erişilebilir olduğundan ve doğru şekilde yüklendiğinden emin olun.

### S2: Aspose.Note farklı belge formatlarıyla uyumlu mudur?

Cevap2: Aspose.Note öncelikle OneNote belgeleriyle çalışır ancak PDF dahil çeşitli formatlarda kaydetme seçenekleri sunar.

### S3: Belgeleri kaydederken eksik yazı tiplerini nasıl halledebilirim?

Cevap3: Aspose.Note, belirtilen yazı tipinin eksik olması durumunda varsayılan yazı tiplerini kullanma seçenekleri sunarak tutarlı belge formatı sağlar.

### S4: Aspose.Note çıktı belgelerine yazı tipi yerleştirmeyi destekliyor mu?

Cevap4: Evet, Aspose.Note, belgenin taşınabilirliğini ve farklı platformlarda tutarlı görüntülenmesini sağlamak için yazı tiplerinin yerleştirilmesine olanak tanır.

### S5: Aspose.Note ile ilgili daha fazla yardımı nereden alabilirim?

 Cevap5: Daha fazla yardım veya teknik destek için şu adresi ziyaret edebilirsiniz:[Aspose.Note forumu](https://forum.aspose.com/c/note/28).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
