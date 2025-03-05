---
title: OneNote Belgesi Oluşturma ve HTML'ye Kaydetme - Java
linktitle: OneNote Belgesi Oluşturma ve HTML'ye Kaydetme - Java
second_title: Aspose.Note Java API'si
description: Aspose.Note for Java'yı kullanarak OneNote belgeleri oluşturmayı ve HTML olarak kaydetmeyi öğrenin. Programlı OneNote dosya işleme için Java uygulamalarına entegre edin.

type: docs
weight: 18
url: /tr/java/onenote-document-loading/create-onenote-save-to-html/
---
## giriiş

Aspose.Note for Java, geliştiricilerin Microsoft OneNote dosyalarıyla programlı olarak çalışmasına olanak tanıyan güçlü bir kitaplıktır. Bu eğitimde, Aspose.Note for Java'yı kullanarak bir OneNote belgesinin nasıl oluşturulacağını ve HTML formatında nasıl kaydedileceğini inceleyeceğiz.

## Önkoşullar

Başlamadan önce aşağıdakilere sahip olduğunuzdan emin olun:

1. Sisteminizde Java Geliştirme Kiti (JDK) yüklü.
2.  Aspose.Note for Java kütüphanesi. Şuradan indirebilirsiniz[Burada](https://releases.aspose.com/note/java/).
3. Java programlamanın temel bilgisi.

## Paketleri İçe Aktar

Öncelikle gerekli paketleri Java projenize aktarın:

```java
import java.io.ByteArrayOutputStream;
import java.io.File;
import java.io.FileOutputStream;
import java.io.IOException;
import java.io.OutputStream;
import java.io.OutputStreamWriter;
import java.nio.file.Paths;
import com.aspose.note.CssSavingArgs;
import com.aspose.note.Document;
import com.aspose.note.FontFaceType;
import com.aspose.note.FontSavingArgs;
import com.aspose.note.HtmlSaveOptions;
import com.aspose.note.ICssSavingCallback;
import com.aspose.note.IFontSavingCallback;
import com.aspose.note.IImageSavingCallback;
import com.aspose.note.ImageSavingArgs;
import com.aspose.note.ResourceExportType;
```

## 1. Adım: OneNote Belge Nesnesi Oluşturun

```java
Document document = new Document("Path_to_your_sample_one_file");
```

 Bu kod bir başlatır`Document` örnek bir OneNote dosyası yükleyerek nesneyi oluşturun.

## 2. Adım: Bellek Akışına HTML olarak kaydedin

```java
HtmlSaveOptions options = new HtmlSaveOptions();
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);
options.setFontFaceTypes(FontFaceType.Ttf);

ByteArrayOutputStream outputStream = new ByteArrayOutputStream();
document.save(outputStream, options);
```

Burada HTML kaydetme seçeneklerini ayarlayıp belgeyi bir bellek akışına kaydediyoruz.

## 3. Adım: Kaynakları Ayrı Dosyalarda HTML olarak kaydedin

```java
HtmlSaveOptions options = new HtmlSaveOptions();
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);

document.save("output_directory/document.html", options);
```

Bu adım, belgeyi CSS, yazı tipleri ve resimler gibi kaynakları ayrı dosyalarda içeren HTML olarak kaydeder.

## 4. Adım: Kaynakları Kaydetmek için Geri Aramalarla Bellek Akışına HTML olarak kaydedin

```java
Document document = new Document("Path_to_your_sample_one_file");

UserSavingCallbacks savingCallbacks = new UserSavingCallbacks();
savingCallbacks.setRootFolder("documentFolder");
savingCallbacks.setCssFolder("css");
savingCallbacks.setKeepCssStreamOpened(true);
savingCallbacks.setImagesFolder("images");
savingCallbacks.setFontsFolder("fonts");

HtmlSaveOptions options = new HtmlSaveOptions();
options.setFontFaceTypes(FontFaceType.Ttf);
options.setCssSavingCallback(savingCallbacks);
options.setImageSavingCallback(savingCallbacks);
options.setFontSavingCallback(savingCallbacks);
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);

File dir = new File(savingCallbacks.getRootFolder());
if (!dir.exists()) {
    dir.mkdir();
}

document.save(Paths.get(savingCallbacks.getRootFolder(), "document.html").toString(), options);
```

Burada, kaynak tasarrufunu gerçekleştirmek için geri aramaları kullanarak belgeyi HTML olarak bir bellek akışına kaydediyoruz.

## Çözüm

Tebrikler! Aspose.Note for Java'yı kullanarak bir OneNote belgesinin nasıl oluşturulacağını ve HTML formatında kaydedileceğini öğrendiniz. OneNote dosyalarıyla programlı olarak çalışmak için artık bu işlevselliği Java uygulamalarınızla bütünleştirebilirsiniz.

## SSS'ler

### S1: Birden fazla OneNote belgesini tek seferde HTML'ye dönüştürebilir miyim?

Cevap1: Evet, birden fazla belge arasında geçiş yapabilir ve kaydetme işlemini tekrarlayarak uygulayabilirsiniz.

### S2: Aspose.Note for Java, HTML'nin yanı sıra diğer çıktı formatlarını da destekliyor mu?

Cevap2: Evet, Aspose.Note for Java; PDF, DOCX ve görüntü formatları dahil olmak üzere çeşitli çıktı formatlarını destekler.

### S3: Aspose.Note for Java'nın deneme sürümü mevcut mu?

C3: Evet, ücretsiz deneme sürümünü şuradan indirebilirsiniz:[Burada](https://releases.aspose.com/).

### S4: Aspose.Note for Java desteğini nereden alabilirim?

 Cevap4: Destek alabilirsiniz[Aspose.Note forumu](https://forum.aspose.com/c/note/28).

### S5: Aspose.Note for Java lisansını nasıl satın alabilirim?

 Cevap5: Lisansı şuradan satın alabilirsiniz:[Web sitesi](https://purchase.aspose.com/buy).