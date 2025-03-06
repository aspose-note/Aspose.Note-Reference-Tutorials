---
title: OneNote'ta Kaydetme Seçeneklerini Belirleme - Aspose.Note
linktitle: OneNote'ta Kaydetme Seçeneklerini Belirleme - Aspose.Note
second_title: Aspose.Note Java API'si
description: Aspose.Note for Java'yı kullanarak OneNote'ta kaydetme seçeneklerini nasıl belirleyeceğinizi öğrenin. Sayfa dizini, sayım ve sıkıştırma ayarlarını zahmetsizce özelleştirin.
weight: 24
url: /tr/java/onenote-document-saving/specify-save-options/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote'ta Kaydetme Seçeneklerini Belirleme - Aspose.Note

## giriiş

Bu eğitimde Aspose.Note for Java'yı kullanarak OneNote'ta kaydetme seçeneklerini nasıl belirleyeceğimizi öğreneceğiz. Aspose.Note, geliştiricilerin OneNote belgelerini programlı olarak oluşturmasına, değiştirmesine ve dönüştürmesine olanak tanıyan güçlü bir Java kitaplığıdır. Aspose.Note ile çıktıyı ihtiyaçlarınıza göre özelleştirmek için çeşitli kaydetme seçeneklerini kolayca kontrol edebilirsiniz.

## Önkoşullar

Başlamadan önce aşağıdaki önkoşullara sahip olduğunuzdan emin olun:

1. Java programlama dili hakkında temel bilgiler.
2. JDK (Java Development Kit) sisteminizde kuruludur.
3.  Aspose.Note for Java kütüphanesi kuruldu. Şuradan indirebilirsiniz[Burada](https://releases.aspose.com/note/java/).

## Paketleri İçe Aktar

Başlamak için gerekli paketleri Java kodunuza aktarın:

```java
import com.aspose.note.Document;
import com.aspose.note.PdfImageCompression;
import com.aspose.note.PdfSaveOptions;
import java.io.IOException;
```

Örneği birden çok adıma ayıralım:

## 1. Adım: OneNote Belgesini Yükleyin

```java
// Belgeler dizininin yolu.
String dataDir = "Your Document Directory";

// Belgeyi Aspose.Note'a yükleyin.
Document doc = new Document(dataDir + "Aspose.one");
```

 Bu adımda OneNote belgesinin yolunu belirtiyoruz ve onu`Document` nesne.

## Adım 2: PdfSaveOptions Nesnesini Başlatın

```java
// PdfSaveOptions nesnesini başlat
PdfSaveOptions opts = new PdfSaveOptions();
```

 Burada bir başlangıç başlatıyoruz`PdfSaveOptions` Belgeyi PDF olarak kaydetme seçeneklerini belirlemek için kullanılacak nesne.

## 3. Adım: Sayfa Dizini ve Sayısını Ayarlayın

```java
// Sayfa dizinini ayarla
opts.setPageIndex(2);

// Sayfa sayısını ayarla
opts.setPageCount(3);
```

Bu satırlar kaydedilecek sayfaların indeksini ve sayısını ayarlar. Bu örnekte indeks 2'den başlayarak toplam 3 sayfayı kaydediyoruz.

## Adım 4: Sıkıştırma Ayarlarını Belirleyin

```java
// Gerekirse sıkıştırmayı belirtin
opts.setImageCompression(PdfImageCompression.Jpeg);
opts.setJpegQuality(90);
```

Burada PDF için görüntü sıkıştırma ayarlarını belirtiyoruz. Sıkıştırmayı JPEG formatına ayarladık ve JPEG kalitesini %90 olarak belirledik.

## Adım 5: Belgeyi Seçeneklerle Kaydetme

```java
dataDir = dataDir + "Document.SaveWithOptions_out.pdf";
doc.save(dataDir, opts);
```

Son olarak belgeyi belirtilen seçeneklerle kaydediyoruz. Çıktı PDF'si, verilen seçeneklerle belirtilen konuma kaydedilecektir.

## Çözüm

Bu eğitimde Aspose.Note for Java'yı kullanarak OneNote'ta kaydetme seçeneklerini nasıl belirleyeceğimizi öğrendik. Kaydetme seçeneklerini özelleştirerek çıktı belgesinin sayfa dizini, sayım ve sıkıştırma ayarları gibi çeşitli yönlerini kontrol edebilirsiniz.

## SSS'ler

### S1: Aspose.Note büyük OneNote belgelerini işleyebilir mi?

Cevap1: Evet, Aspose.Note büyük OneNote belgelerini verimli bir şekilde işleyecek şekilde tasarlanmıştır.

### S2: Aspose.Note en son Java sürümleriyle uyumlu mu?

Cevap2: Evet, Aspose.Note en son Java sürümleriyle uyumludur.

### S3: OneNote belgelerini Aspose.Note'u kullanarak diğer formatlara dönüştürebilir miyim?

Cevap3: Evet, Aspose.Note, OneNote belgelerinin PDF, DOCX ve HTML gibi çeşitli formatlara dönüştürülmesini destekler.

### S4: Aspose.Note, OneNote belgelerinin şifrelenmesi ve şifresinin çözülmesi için destek sağlıyor mu?

Cevap4: Evet, Aspose.Note, OneNote belgelerinin şifrelenmesi ve şifresinin çözülmesi için API'ler sağlar.

### S5: Aspose.Note ticari kullanıma uygun mudur?

Cevap5: Evet, Aspose.Note lisans satın alınarak ticari amaçlarla kullanılabilir.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
