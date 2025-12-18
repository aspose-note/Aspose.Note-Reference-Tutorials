---
date: 2025-12-18
description: Aspose.Note for Java kullanarak OneNote sayfalarını PDF’ye nasıl dışa
  aktaracağınızı öğrenin. Bölme algoritmalarını seçin, sayfa bölmeyi ayarlayın ve
  PDF dosyalarını kolayca oluşturun.
linktitle: Export OneNote Pages with Splitting Algorithm Method – Aspose.Note
second_title: Aspose.Note Java API
title: OneNote Sayfalarını Bölme Algoritması Yöntemiyle Dışa Aktar – Aspose.Note
url: /tr/java/onenote-document-saving/use-splitting-algorithm-method/
weight: 26
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote Sayfalarını Bölme Algoritması Yöntemi ile Dışa Aktarma – Aspose.Note

## Giriş

Programlı olarak OneNote sayfalarını PDF belgesine **dışa aktarmanız** gerekiyorsa, Aspose.Note for Java bunu oldukça basit hale getirir. Bu öğreticide Bölme Algoritması Yöntemi'ni adım adım inceleyeceğiz; bu yöntem, içeriğin sayfalara nasıl bölündüğünü kontrol etmenizi sağlar ve temiz, okunabilir bir PDF çıktısı elde etmenize yardımcı olur. PDF kaydetme seçeneklerini nasıl ayarlayacağınızı, doğru sayfa‑bölme algoritmasını nasıl seçeceğinizi ve sonunda PDF dosyasını nasıl oluşturacağınızı göreceksiniz—tüm bunlar sadece birkaç satır Java kodu ile.

## Hızlı Yanıtlar
- **Bölme Algoritması ne yapar?** OneNote sayfalarını PDF'ye dışa aktarırken sayfa sınırlarını aşan nesnelerin nasıl işlendiğini belirler.  
- **Hangi kütüphane gereklidir?** Aspose.Note for Java (resmi Aspose sitesinden indirin).  
- **Lisans gerekir mi?** Üretim kullanımı için geçici ya da tam lisans gereklidir; ücretsiz deneme sürümü mevcuttur.  
- **Büyük OneNote defterlerini dışa aktarabilir miyim?** Evet – kütüphane büyük dosyaları verimli bir şekilde işler ve sayfa‑bölme kurallarını ayarlamanıza izin verir.  
- **Hangi çıktı formatları destekleniyor?** PDF, JPEG, PNG, XPS ve daha fazlası; bu kılavuz PDF dışa aktarmaya odaklanmaktadır.

## **export onenote pages** nedir?
OneNote sayfalarını dışa aktarmak, yerel `.one` dosya formatını PDF gibi daha taşınabilir bir formata dönüştürmek anlamına gelir. Bu, içeriği OneNote uygulamasına ihtiyaç duymadan paylaşmak, arşivlemek veya yazdırmak için faydalıdır.

## **export onenote pages** için Bölme Algoritması neden kullanılmalı?
Algoritma, karmaşık nesnelerin (tablolar, görseller, çizimler) sayfa sonlarında nasıl işlendiği üzerinde ince ayar yapmanızı sağlar. Uygun algoritmayı seçerek şunları yapabilirsiniz:

* Her sayfanın görsel düzenini koruyun.  
* Kesilmiş içeriklerin ortaya çıkmasını önleyin.  
* Nesneler bir sonraki sayfaya temiz bir şekilde taşınabildiğinde oluşturulan sayfa sayısını azaltın.  

## Gereksinimler

Başlamadan önce aşağıdaki gereksinimlerin karşılandığından emin olun:

1. Java Development Kit (JDK): Sisteminizde JDK yüklü olduğundan emin olun. İndirmek için [website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) adresini ziyaret edebilirsiniz.
2. Aspose.Note for Java Library: Aspose.Note for Java kütüphanesini [download link](https://releases.aspose.com/note/java/) adresinden indirip kurun.

## Paketleri İçe Aktarma

Java projenizde Aspose.Note işlevlerini kullanmak için gerekli paketleri içe aktarın.

```java
import java.io.IOException;
import com.aspose.note.AlwaysSplitObjectsAlgorithm;
import com.aspose.note.Document;
import com.aspose.note.KeepPartAndCloneSolidObjectToNextPageAlgorithm;
import com.aspose.note.KeepSolidObjectsAlgorithm;
import com.aspose.note.PdfSaveOptions;
```

## Adım 1: Belge Dizinini Tanımlama

OneNote belgenizin bulunduğu dizini ayarlayın.

```java
String dataDir = "Your Document Directory";
```

## Adım 2: OneNote Belgesini Yükleme

Aspose.Note'un `Document` sınıfını kullanarak OneNote belgesini yükleyin.

```java
Document doc = new Document(dataDir + "Sample1.one");
```

## Adım 3: PDF Kaydetme Seçeneklerini Ayarlama

Belgeyi PDF olarak kaydetmek için `PdfSaveOptions` örneği oluşturun. Burada **sayfa bölme** davranışı ve diğer PDF‑ile ilgili ayarları belirleyebilirsiniz.

```java
PdfSaveOptions pdfSaveOptions = new PdfSaveOptions();
```

## Adım 4: Sayfa Bölme Algoritmasını Ayarlama

İhtiyacınıza uygun bölme algoritmasını seçin. Burada `KeepPartAndCloneSolidObjectToNextPageAlgorithm` kullanıyoruz; bu algoritma, bir nesnenin bir kısmını mevcut sayfada tutar ve kalanını bir sonraki sayfaya kopyalar.

```java
pdfSaveOptions.setPageSplittingAlgorithm(new KeepPartAndCloneSolidObjectToNextPageAlgorithm(100));
```

## Adım 5: Belgeyi Kaydetme

Belgeyi belirttiğiniz PDF kaydetme seçenekleriyle kaydedin. Bu adım **PDF onenote** çıktısı üretir; oluşturulan dosyayı açabilir, paylaşabilir veya yazdırabilirsiniz.

```java
try {
    doc.save(dataDir + "UsingSplittingAlgorithmMethod_out.Jpeg", pdfSaveOptions);
} catch (Exception ex) {
    System.out.println("Exception: " + ex.getMessage());
}
```

## Ortak Sorunlar ve Çözümler

| Sorun | Çözüm |
|-------|----------|
| **Nesneler sayfa sınırlarında kesiliyor** | `AlwaysSplitObjectsAlgorithm` gibi farklı bir algoritma deneyin veya `KeepPartAndCloneSolidObjectToNextPageAlgorithm` içinde eşik değerini artırın. |
| **Çıktı PDF'i boş** | Kaynak `.one` dosyasının bozuk olmadığını ve `dataDir` yolunun doğru olduğunu doğrulayın. |
| **Büyük defterlerde performans yavaş** | Bellek kullanımını azaltmak için `pdfSaveOptions.setCompressImages(true)` kullanın ve defteri daha küçük bölümlerde işlemeyi düşünün. |

## Sıkça Sorulan Sorular

**S: Aspose.Note for Java'yı diğer programlama dilleriyle kullanabilir miyim?**  
C: Evet, Aspose.Note .NET, C++ ve Python için de mevcuttur.

**S: Aspose.Note büyük OneNote dosyalarını işlemek için uygun mu?**  
C: Kesinlikle. Kütüphane büyük defterleri verimli bir şekilde işlemek üzere optimize edilmiştir.

**S: Aspose.Note için ek kaynaklar ve destek nereden bulunur?**  
C: Destek ve rehberlik için [documentation](https://reference.aspose.com/note/java/) ve [forum](https://forum.aspose.com/c/note/28) adreslerine başvurabilirsiniz.

**S: Satın almadan önce Aspose.Note'ı deneyebilir miyim?**  
C: Evet, özellikleri keşfetmek için [free trial](https://releases.aspose.com/) alabilirsiniz.

**S: Aspose.Note için geçici bir lisans nasıl alınır?**  
C: Ürünü deneme süresi içinde değerlendirmek için [temporary license](https://purchase.aspose.com/temporary-license/) talep edebilirsiniz.

**Son Güncelleme:** 2025-12-18  
**Test Edilen Versiyon:** Aspose.Note 24.12 for Java  
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}