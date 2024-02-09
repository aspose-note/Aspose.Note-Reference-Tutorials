---
title: Aspose.Note'ta OneNote Belgesi Oluşturun ve HTML'ye Kaydedin
linktitle: Aspose.Note'ta OneNote Belgesi Oluşturun ve HTML'ye Kaydedin
second_title: Aspose.Note .NET API'si
description: Aspose.Note API'yi kullanarak .NET uygulamalarında Microsoft OneNote belgelerini HTML formatında nasıl oluşturacağınızı ve kaydedeceğinizi öğrenin. Adım adım örnekler içeren kapsamlı eğitimimizi takip edin.
type: docs
weight: 14
url: /tr/net/loading-and-saving-operations/create-onenote-doc-save-to-html/
---
## giriiş

Aspose.Note for .NET, geliştiricilerin .NET uygulamalarında Microsoft OneNote belgeleriyle programlı olarak çalışmasına olanak tanıyan güçlü bir API'dir. Aspose.Note ile OneNote dosyalarını zahmetsizce oluşturabilir, değiştirebilir ve dönüştürebilirsiniz. Bu eğitimde, bir OneNote belgesinin nasıl oluşturulacağını ve Aspose.Note for .NET API tarafından sağlanan çeşitli seçenekleri kullanarak HTML formatında nasıl kaydedileceğini inceleyeceğiz.

## Önkoşullar

Başlamadan önce aşağıdaki önkoşullara sahip olduğunuzdan emin olun:

- Temel C# programlama dili bilgisi.
- Sisteminizde Visual Studio yüklü.
-  Aspose.Note for .NET API'si projenizde yüklü. Şuradan indirebilirsiniz[Burada](https://releases.aspose.com/note/net/).
- Microsoft OneNote belgelerinin yapısına aşinalık.

## Ad Alanlarını İçe Aktar

Kodlama kısmına geçmeden önce gerekli ad alanlarını içe aktaralım:

```csharp
using System;
using System.Drawing;
using System.Globalization;
using System.IO;

using Aspose.Note.Saving;
using Aspose.Note.Saving.Html;

```

Şimdi her örneği birden fazla adıma ayıralım ve Aspose.Note for .NET kullanarak bir OneNote belgesinin nasıl oluşturulacağını ve HTML formatında nasıl kaydedileceğini görelim.

## 1. Adım: Varsayılan Seçeneklerle OneNote Belgesi Oluşturun

```csharp
public static void CreateAndSaveToHTMLUsingDefaultOptions()
{
    // OneNote belgesini başlat
    Document doc = new Document();
    Page page = doc.AppendChildLast(new Page());

    // Belgedeki tüm metinler için varsayılan stil.
    ParagraphStyle textStyle = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
    page.Title = new Title()
    {
        TitleText = new RichText() { Text = "Title text.", ParagraphStyle = textStyle },
        TitleDate = new RichText() { Text = new DateTime(2011, 11, 11).ToString("D", CultureInfo.InvariantCulture), ParagraphStyle = textStyle },
        TitleTime = new RichText() { Text = "12:34", ParagraphStyle = textStyle }
    };

    // HTML formatında kaydet
    string dataDir = "Your Document Directory";
    string outputPath = Path.Combine(dataDir, "CreateOneNoteDocAndSaveToHTML_out.html");
    doc.Save(outputPath);

    Console.WriteLine("\nOneNote document created successfully.\nFile saved at " + outputPath);
}
```

Bu adımda yeni bir OneNote belgesi başlatıyoruz, başlıklı bir sayfa ekliyoruz ve varsayılan seçenekleri kullanarak bunu HTML formatında kaydediyoruz.

## Adım 2: Belirli Bir Sayfa Aralığını Oluşturun ve HTML'ye Kaydedin

```csharp
public static void CreateAndSavePageRange()
{
    // OneNote belgesini başlat
    Document doc = new Document();
    Page page = doc.AppendChildLast(new Page());

    // Belgedeki tüm metinler için varsayılan stil.
    ParagraphStyle textStyle = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
    page.Title = new Title()
    {
        TitleText = new RichText() { Text = "Title text.", ParagraphStyle = textStyle },
        TitleDate = new RichText() { Text = new DateTime(2011, 11, 11).ToString("D", CultureInfo.InvariantCulture), ParagraphStyle = textStyle },
        TitleTime = new RichText() { Text = "12:34", ParagraphStyle = textStyle }
    };

    // HTML formatında kaydet
    string dataDir = "Your Document Directory";
    string outputPath = Path.Combine(dataDir, "CreateAndSavePageRange_out.html");
    doc.Save(outputPath, new HtmlSaveOptions { PageCount = 1, PageIndex = 0 });

    Console.WriteLine("\nOneNote document created successfully and saved as page range.\nFile saved at " + outputPath);
}
```

Burada, bir belgenin nasıl oluşturulacağını ve belirli bir sayfa aralığının HTML formatında nasıl kaydedileceğini göstereceğiz.

## 3. Adım: Gömülü Kaynaklarla Bellek Akışına HTML olarak kaydedin

```csharp
public static void SaveAsHTMLToMemoryStreamWithEmbeddedResources()
{
    // OneNote belgesini yükleyin
    string dataDir = "Your Document Directory";
    var document = new Document(Path.Combine(dataDir, "Aspose.one"));

    // HTML kaydetme seçeneklerini belirtin
    var options = new HtmlSaveOptions()
    {
        ExportCss = ResourceExportType.ExportEmbedded,
        ExportFonts = ResourceExportType.ExportEmbedded,
        ExportImages = ResourceExportType.ExportEmbedded,
        FontFaceTypes = FontFaceType.Ttf
    };

    // Belgeyi bir bellek akışına kaydedin
    var memoryStream = new MemoryStream();
    document.Save(memoryStream, options);
}
```

Bu adım, bir OneNote belgesinin katıştırılmış kaynaklarla (CSS, yazı tipleri ve resimler) HTML biçiminde bir bellek akışına nasıl kaydedileceğini gösterir.

## Adım 4: Kaynakları Ayrı Dosyalarda Bulundurarak Dosyaya HTML Olarak Kaydetme

```csharp
public static void SaveAsHTMLToFileWithResourcesInSeparateFiles()
{
    // OneNote belgesini yükleyin
    string dataDir = "Your Document Directory";
    var document = new Document(Path.Combine(dataDir, "Aspose.one"));

    // HTML kaydetme seçeneklerini belirtin
    var options = new HtmlSaveOptions()
    {
        ExportCss = ResourceExportType.ExportAsStream,
        ExportFonts = ResourceExportType.ExportAsStream,
        ExportImages = ResourceExportType.ExportAsStream,
        FontFaceTypes = FontFaceType.Ttf
    };

    //Belgeyi, ayrı dosyalarda depolanan kaynaklarla HTML dosyasına kaydedin
    document.Save(Path.Combine(dataDir, "document_out.html"), options);
}
```

Bu adımda, bir OneNote belgesini tüm kaynaklar (CSS, yazı tipleri ve resimler) ayrı dosyalarda depolanacak şekilde HTML biçiminde kaydediyoruz.

## Adım 5: Kaynakları Kaydetmek için Geri Aramalarla Bellek Akışına HTML olarak kaydedin

```csharp
public static void SaveAsHTMLToMemoryStreamWithCallBacksToSaveResources()
{
    // Geri aramaların kaydedilmesi yapılandırmasını belirtin
    var savingCallbacks = new UserSavingCallbacks()
    {
        RootFolder = "documentFolder",
        CssFolder = "css",
        KeepCssStreamOpened = true,
        ImagesFolder = "images",
        FontsFolder = "fonts"
    };

    // HTML kaydetme seçeneklerini belirtin
    var options = new HtmlSaveOptions
    {
        FontFaceTypes = FontFaceType.Ttf,
        CssSavingCallback = savingCallbacks,
        FontSavingCallback = savingCallbacks,
        ImageSavingCallback = savingCallbacks
    };

    // OneNote belgesini yükleyin
    string dataDir = "Your Document Directory";
    var document = new Document(Path.Combine(dataDir, "Aspose.one"));

    // Kullanıcı tanımlı geri aramalar tarafından yönetilen kaynaklarla belgeyi HTML biçiminde kaydedin
    using (var stream = File.Create(Path.Combine(savingCallbacks.RootFolder, "document.html")))
    {
        document.Save(stream, options);
    }

    // Verileri CSS akışına manuel olarak ekleme
    using (var writer = new StreamWriter(savingCallbacks.CssStream))
    {
        writer.WriteLine();
        writer.WriteLine("/* This line is appended to stream manually by user */");
    }
}
```

Burada, kullanıcı tanımlı geri aramalarla yönetilen kaynaklarla bir OneNote belgesinin HTML biçiminde nasıl kaydedileceğini gösteriyoruz.

## Çözüm

Bu makalede, Aspose.Note for .NET kullanarak OneNote belgeleriyle nasıl çalışılacağını ve bunları HTML formatında nasıl kaydedileceğini araştırdık. Adım adım kılavuzu takip ederek kolayca yapabilirsiniz.

 Bu işlevselliği .NET uygulamalarınıza entegre ederek OneNote dosyalarını verimli bir şekilde yönetmenize olanak tanıyın.

## SSS'ler

### S1: Kaydedilen HTML dosyasının görünümünü özelleştirebilir miyim?

Cevap1: Evet, dönüştürme işlemi sırasında oluşturulan CSS stil sayfalarını değiştirerek görünümü özelleştirebilirsiniz.

### S2: Aspose.Note, HTML'nin yanı sıra diğer formatlara dönüştürmeyi de destekliyor mu?

Cevap2: Evet, Aspose.Note, PDF, görseller ve Microsoft Word belgeleri gibi çeşitli formatlara dönüştürmeyi destekler.

### S3: Aspose.Note .NET Core uygulamalarıyla uyumlu mu?

Cevap3: Evet, Aspose.Note hem .NET Framework hem de .NET Core uygulamalarıyla uyumludur.

### S4: Aspose.Note'u kullanarak OneNote belgelerinden metin ve görseller çıkarabilir miyim?

Cevap4: Evet, Aspose.Note API'yi kullanarak metin ve görselleri çıkarabilir, ayrıca diğer çeşitli işlemleri gerçekleştirebilirsiniz.

### S5: Aspose.Note özelliklerini test etmek için deneme sürümü mevcut mu?

 C5: Evet, ücretsiz deneme sürümünü şuradan indirebilirsiniz:[Burada](https://releases.aspose.com/).