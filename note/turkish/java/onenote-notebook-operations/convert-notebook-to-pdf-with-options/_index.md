---
date: 2025-12-28
description: Java için Aspose.Note kullanarak OneNote'u PDF'ye tam kontrolle nasıl
  dışa aktaracağınızı öğrenin. OneNote defterini PDF'ye dışa aktarma seçeneklerini
  ve Java ile defteri PDF'ye dönüştürme rehberini içerir.
linktitle: How to Export OneNote to PDF with Options – Convert Notebook to PDF using
  Aspose.Note
second_title: Aspose.Note Java API
title: OneNote'u Seçeneklerle PDF Olarak Dışa Aktarma – Aspose.Note Kullanarak Defteri
  PDF'e Dönüştürme
url: /tr/java/onenote-notebook-operations/convert-notebook-to-pdf-with-options/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote'u PDF'ye Seçeneklerle Dışa Aktarma – Aspose.Note Java API

## Introduction

Bu öğreticide, Aspose.Note for Java kullanarak özelleştirilebilir seçeneklerle **OneNote'u PDF'ye nasıl dışa aktaracağınızı** öğreneceksiniz. OneNote defterini PDF'ye dönüştürmek sık karşılaşılan bir gereksinimdir—toplantı notlarını paylaşmanız, belgeleri arşivlemeniz veya yazdırılabilir raporlar oluşturmanız gerektiğinde. Aspose.Note ile süreç basittir, tamamen programlanabilir ve ortaya çıkan PDF üzerinde ince ayar kontrolü sağlar.

## Quick Answers
- **API ne yapar?** Bir OneNote defterini yükler ve isteğe bağlı ayarlarla PDF olarak kaydeder.  
- **Hangi dil kullanılıyor?** Java – sunucu‑tarafı veya masaüstü uygulamaları için mükemmeldir.  
- **Lisans gerekir mi?** Geliştirme için ücretsiz deneme çalışır; üretim için ticari lisans gereklidir.  
- **Sayfa düzenini kontrol edebilir miyim?** Evet, sayfa‑bölme algoritmalarını, üst‑alt bilgi ayarlarını ve daha fazlasını belirleyebilirsiniz.  
- **Kod örneği çalıştırılabilir mi?** Kesinlikle – sadece yer tutucu yolu kendi defter konumunuzla değiştirin.

## What is “how to export onenote to pdf”?

OneNote'u PDF'ye dışa aktarmak, yerel OneNote defterini (`*.onetoc2` ve ilgili bölüm dosyalarını) taşınabilir, sabit‑sayfa düzenine sahip bir PDF belgesine dönüştürmek anlamına gelir. Bu dönüşüm biçimlendirmeyi, görüntüleri ve gömülü nesneleri korur ve içeriği OneNote gerektirmeden herhangi bir cihazda görüntülenebilir hâle getirir.

## Why use Aspose.Note for Java?

- **Microsoft Office bağımlılığı yok** – Java çalıştıran herhangi bir platformda çalışır.  
- **Zengin PDF seçenekleri** – sayfa bölme, üst‑alt bilgi ve nesne işleme kontrolü sağlar.  
- **Yüksek doğruluk** – PDF çıktısı, orijinal OneNote görünümüne çok yakın olur.  
- **Ölçeklenebilir** – binlerce defteri toplu işleme için uygundur.

## Prerequisites

Başlamadan önce şunların kurulu olduğundan emin olun:

1. **Java Development Kit (JDK)** – sürüm 8 veya üzeri.  
2. **Aspose.Note for Java** – [download link](https://releases.aspose.com/note/java/) adresinden indirin.  
3. **Bir IDE** – IntelliJ IDEA, Eclipse veya NetBeans (seçiminiz).  
4. **Dönüştürmek istediğiniz OneNote defteri** (örnek: `Notizbuch öffnen.onetoc2`).

## Import Packages

İlk olarak, defter işleme ve PDF kaydetme işlevselliğini sağlayan sınıfları içe aktarın.

```java
import com.aspose.note.Notebook;
import java.io.IOException;
import com.aspose.note.KeepSolidObjectsAlgorithm;
import com.aspose.note.Notebook;
import com.aspose.note.NotebookPdfSaveOptions;
import com.aspose.note.PdfSaveOptions;
```

## Step 1: Load the OneNote Notebook

Diskten defter dosyasını yükleyin. `Your Document Directory` ifadesini `.onetoc2` dosyanızın bulunduğu gerçek klasörle değiştirin.

```java
String dataDir = "Your Document Directory";
// Load a OneNote Notebook
Notebook notebook = new Notebook(dataDir + "Notizbuch �ffnen.onetoc2");
```

## Step 2: Specify PDF Save Options

Burada PDF'nin nasıl oluşturulacağını tanımlarsınız. Örnek, katı nesneleri birlikte tutan bir sayfa‑bölme algoritması ayarlar; bu, aynı sayfada kalması gereken diyagramlar veya tablolar olduğunda faydalıdır.

```java
// Specify PDF save options
NotebookPdfSaveOptions notebookSaveOptions = new NotebookPdfSaveOptions();
PdfSaveOptions documentSaveOptions = notebookSaveOptions.getDocumentSaveOptions();
documentSaveOptions.setPageSplittingAlgorithm(new KeepSolidObjectsAlgorithm());
```

## Step 3: Save the Notebook as PDF

Son olarak, defteri bir PDF dosyası olarak yazın. Çıktı yolu istediğiniz herhangi bir konum olabilir.

```java
dataDir = dataDir + "ExportNotebooktoPDFwithOptions_out.pdf";
// Save the Notebook
notebook.save(dataDir, notebookSaveOptions);
```

## Common Issues and Solutions

| Sorun | Neden Oluşur | Çözüm |
|-------|--------------|-------|
| **Dosya bulunamadı** | Yanlış `dataDir` veya dosya adı. | Yolu tekrar kontrol edin ve defter dosyasının mevcut olduğundan emin olun. |
| **Eksik yazı tipleri** | PDF oluşturma, OneNote'daki aynı yazı tiplerine ihtiyaç duyar. | Gerekli yazı tiplerini sunucuya kurun veya ek Aspose seçenekleriyle gömün. |
| **Büyük defterler OutOfMemoryError hatasına neden olur** | Tüm defter belleğe yüklenir. | Bölümleri tek tek işleyin veya JVM yığın boyutunu (`-Xmx`) artırın. |

## Conclusion

**OneNote'u PDF'ye nasıl dışa aktaracağınızı** Aspose.Note for Java kullanarak, defteri yükleme, PDF seçeneklerini yapılandırma ve sonucu kaydetme adımlarını ele aldık. Bu adımları izleyerek, defter‑to‑PDF dönüşümünü herhangi bir Java uygulamasına entegre edebilirsiniz; ister masaüstü aracı, ister web servisi, ister toplu‑işlem arka ucu olsun.

## FAQ's

### Q1: PDF çıktısının görünümünü özelleştirebilir miyim?

A1: Evet, Aspose.Note PDF çıktısını özelleştirmek için üst‑alt bilgi ayarları, sayfa bölme algoritmaları ve daha fazlası dahil çeşitli seçenekler sunar.

### Q2: Aspose.Note tüm OneNote sürümleriyle uyumlu mu?

A2: Aspose.Note Microsoft OneNote 2010 ve sonraki sürümlerini destekler.

### Q3: Aspose.Note ücretsiz deneme sunuyor mu?

A3: Evet, Aspose.Note'un ücretsiz denemesini [buradan](https://releases.aspose.com/) indirebilirsiniz.

### Q4: Aspose.Note belgelerini nerede bulabilirim?

A4: Aspose.Note için kapsamlı belgeleri [burada](https://reference.aspose.com/note/java/) bulabilirsiniz.

### Q5: Aspose.Note için destek nasıl alabilirim?

A5: Herhangi bir teknik yardım veya sorunuz için Aspose.Note destek forumunu [burada](https://forum.aspose.com/c/note/28/) ziyaret edebilirsiniz.

## Additional Frequently Asked Questions

**S: OneNote defterini görüntü kaybı olmadan PDF'ye nasıl dışa aktarırım?**  
C: `KeepSolidObjectsAlgorithm`'un ayarlandığından (gösterildiği gibi) ve kaynak defterin görüntü dosyalarının aynı dizinde erişilebilir olduğundan emin olun.

**S: Tek bir çalıştırmada birden fazla defteri toplu olarak dönüştürebilir miyim?**  
C: Evet. Defter yollarının bir listesini döngüye alın, her biri için bir `Notebook` örneği oluşturun, aynı `NotebookPdfSaveOptions`'ı uygulayın ve `save()` metodunu çağırın.

**S: Dönüştürme sırasında PDF meta verilerini (yazar, başlık) ayarlamanın bir yolu var mı?**  
C: Kaydetmeden önce `PdfSaveOptions.setMetadata()` metodunu kullanarak yazar, başlık, konu ve anahtar kelimeleri tanımlayın.

**S: API şifre korumalı PDF'leri destekliyor mu?**  
C: Diğer seçenekleri yapılandırdıktan sonra `PdfSaveOptions` üzerinde `setEncryptionPassword()` metodunu kullanarak bir şifre belirleyebilirsiniz.

**S: Bu öğreticide hangi Aspose.Note sürümü kullanıldı?**  
C: Kod, Aspose.Note for Java 23.12 sürümüyle test edilmiştir.

---

**Last Updated:** 2025-12-28  
**Tested With:** Aspose.Note for Java 23.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}