---
date: 2026-03-16
description: Aspose.Note for Java kullanarak OneNote PDF'yi Bölme Algoritması Yöntemi
  ile dışa aktarmayı, sayfa sonlarını kontrol etmeyi ve PDF görüntülerini verimli
  bir şekilde sıkıştırmayı öğrenin.
linktitle: Export OneNote PDF with Splitting Algorithm Method – Aspose.Note
second_title: Aspose.Note Java API
title: OneNote PDF'yi Bölme Algoritması Yöntemiyle Dışa Aktar – Aspose.Note
url: /tr/java/onenote-document-saving/use-splitting-algorithm-method/
weight: 26
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Splitting Algoritması Yöntemiyle OneNote PDF Dışa Aktarma – Aspose.Note

## Giriş

Programlı olarak **OneNote PDF dışa aktarmanız** gerekiyorsa, Aspose.Note for Java bunu basit hale getirir. Bu öğreticide Splitting Algorithm Method (Bölme Algoritması Yöntemi) üzerinden ilerleyeceğiz; bu yöntem içerik sayfalar arasında nasıl bölüneceğini kontrol etmenizi sağlar ve temiz, okunabilir bir PDF çıktısı elde etmenize yardımcı olur. PDF kaydetme seçeneklerini nasıl ayarlayacağınızı, doğru sayfa‑bölme algoritmasını nasıl seçeceğinizi ve sonunda PDF dosyasını nasıl oluşturacağınızı göreceksiniz — sadece birkaç satır Java kodu ile.

## Hızlı Yanıtlar
- **Splitting Algorithm ne yapar?** OneNote sayfalarını PDF'ye dışa aktarırken sayfa sınırlarını aşan nesnelerin nasıl ele alındığını belirler.  
- **Hangi kütüphane gereklidir?** Aspose.Note for Java (resmi Aspose sitesinden indirin).  
- **Lisans gerekir mi?** Üretim kullanımı için geçici veya tam lisans gereklidir; ücretsiz deneme mevcuttur.  
- **Büyük OneNote defterlerini dışa aktarabilir miyim?** Evet — kütüphane büyük dosyaları verimli bir şekilde işler ve sayfa‑bölme kurallarını ayarlamanıza izin verir.  
- **Hangi çıktı formatları destekleniyor?** PDF, JPEG, PNG, XPS ve daha fazlası; bu kılavuz PDF dışa aktarmaya odaklanmaktadır.  
- **PDF görüntülerini nasıl sıkıştırabilirim?** Oluşturulan PDF'deki görüntü boyutunu azaltmak için `pdfSaveOptions.setCompressImages(true)` kullanın.  

## Splitting Algoritmasıyla OneNote PDF Nasıl Dışa Aktarılır
Bu bölüm, **OneNote sayfalarını** akıllı bir şekilde sayfa sonlarını yöneterek PDF'ye dönüştürmek için gereken adımları size adım adım gösterir.

## OneNote PDF dışa aktarma nedir?
OneNote PDF dışa aktarmak, yerel `.one` dosya formatını taşınabilir bir PDF belgesine dönüştürmek anlamına gelir. Bu, içeriği OneNote uygulamasına ihtiyaç duymadan paylaşmak, arşivlemek veya yazdırmak için kullanışlıdır.

## OneNote PDF dışa aktarmada Splitting Algoritması neden kullanılır?
Algoritma, karmaşık nesnelerin (tablolar, görüntüler, çizimler) sayfa sonlarında nasıl ele alındığı üzerinde ayrıntılı kontrol sağlar. Uygun algoritmayı seçerek şunları yapabilirsiniz:

* Her sayfanın görsel düzenini koruyun.  
* Kesilecek şekilde kırpılmış içeriği önleyin.  
* Nesneler bir sonraki sayfaya temiz bir şekilde taşınabildiğinde oluşturulan sayfa sayısını azaltın.  

## Ön Koşullar

Başlamadan önce, aşağıdaki ön koşullara sahip olduğunuzdan emin olun:

1. Java Development Kit (JDK): Sisteminizde JDK yüklü olduğundan emin olun. [website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) adresinden indirebilirsiniz.
2. Aspose.Note for Java Kütüphanesi: Aspose.Note for Java kütüphanesini [download link](https://releases.aspose.com/note/java/) adresinden indirip kurun.

## Paketleri İçe Aktarma

Java projenizde, Aspose.Note işlevlerini kullanmak için gerekli paketleri içe aktarın.

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

`PdfSaveOptions` sınıfından bir örnek oluşturarak belgeyi PDF olarak kaydetme seçeneklerini belirleyin. Burada **sayfa bölme** davranışını ve diğer PDF‑ile ilgili ayarları yaparsınız.

```java
PdfSaveOptions pdfSaveOptions = new PdfSaveOptions();
```

## Adım 4: Sayfa Bölme Algoritmasını Ayarlama

Gereksinimlerinize göre uygun bölme algoritmasını seçin. Burada, `KeepPartAndCloneSolidObjectToNextPageAlgorithm` kullanıyoruz; bu algoritma bir nesnenin bir kısmını mevcut sayfada tutar ve kalanını bir sonraki sayfaya kopyalar.

```java
pdfSaveOptions.setPageSplittingAlgorithm(new KeepPartAndCloneSolidObjectToNextPageAlgorithm(100));
```

## Adım 5: Belgeyi Kaydetme

Belgeyi belirtilen PDF kaydetme seçenekleriyle kaydedin. Bu adım, **PDF onenote** çıktısı oluşturur; bu çıktıyı açabilir, paylaşabilir veya yazdırabilirsiniz.

```java
try {
    doc.save(dataDir + "UsingSplittingAlgorithmMethod_out.Jpeg", pdfSaveOptions);
} catch (Exception ex) {
    System.out.println("Exception: " + ex.getMessage());
}
```

## Yaygın Sorunlar ve Çözümleri

| Sorun | Çözüm |
|-------|----------|
| **Nesneler sayfa sınırlarında kesiliyor** | `AlwaysSplitObjectsAlgorithm` gibi farklı bir algoritma deneyin veya `KeepPartAndCloneSolidObjectToNextPageAlgorithm` içinde eşik değerini artırın. |
| **Çıktı PDF boş** | Kaynak `.one` dosyasının bozuk olmadığını ve `dataDir` yolunun doğru olduğunu doğrulayın. |
| **Büyük defterlerde performans yavaş** | `pdfSaveOptions.setCompressImages(true)` kullanarak bellek kullanımını azaltın ve defteri daha küçük bölümlerde işlemeyi düşünün. |

## Sıkça Sorulan Sorular

**S: Aspose.Note for Java'yı diğer programlama dilleriyle kullanabilir miyim?**  
C: Evet, Aspose.Note .NET, C++ ve Python için de mevcuttur.

**S: Aspose.Note büyük OneNote dosyalarını işlemek için uygun mu?**  
C: Kesinlikle. Kütüphane büyük defterleri verimli bir şekilde işlemek için optimize edilmiştir.

**S: Aspose.Note için ek kaynakları ve desteği nerede bulabilirim?**  
C: Destek ve rehberlik için [documentation](https://reference.aspose.com/note/java/) ve [forum](https://forum.aspose.com/c/note/28) adreslerine başvurabilirsiniz.

**S: Aspose.Note'u satın almadan deneyebilir miyim?**  
C: Evet, satın almadan önce özellikleri keşfetmek için bir [free trial](https://releases.aspose.com/) alabilirsiniz.

**S: Aspose.Note için geçici bir lisans nasıl alabilirim?**  
C: Ürünü deneme süresi içinde değerlendirmek için bir [temporary license](https://purchase.aspose.com/temporary-license/) talep edebilirsiniz.

---

**Son Güncelleme:** 2026-03-16  
**Test Edilen Versiyon:** Aspose.Note 24.12 for Java  
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}