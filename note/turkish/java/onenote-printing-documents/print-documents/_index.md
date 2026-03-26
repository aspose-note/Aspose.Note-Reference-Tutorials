---
date: 2026-01-18
description: OneNote belgelerini Aspose.Note for Java kullanarak nasıl yazdıracağınızı
  öğrenin. Bu kılavuz, PDF olarak yazdırmayı, yazdırma ayarlarını özelleştirmeyi ve
  sanal yazıcı Java seçeneklerini kullanmayı gösterir.
linktitle: Print Documents in OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: OneNote Nasıl Yazdırılır – Aspose.Note
url: /tr/java/onenote-printing-documents/print-documents/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote'ta Belgeleri Yazdırma - Aspose.Note

## Giriş

Java uygulamasından OneNote sayfalarını yazdırmak sık karşılaşılan bir gereksinimdir; ister basılı raporlar, PDF arşivleri ya da sanal yazıcılarla entegrasyon ihtiyacınız olsun. Bu öğreticide, **OneNote belgelerini nasıl yazdıracağınızı** Aspose.Note for Java kullanarak öğrenecek, basit yazdırma, yazdırma ayarlarını özelleştirme, PDF'ye yazdırma ve sanal bir yazıcı Java iş akışını kullanma konularını kapsayacağız.

## Hızlı Yanıtlar
- **Java'dan OneNote'u doğrudan PDF'ye yazdırabilir miyim?** Evet – `DocumentPrintAttributeSet` i “Microsoft XPS Document Writer” veya “doPDF 8” gibi bir PDF sanal yazıcısıyla kullanın.  
- **Yazdırma için lisansa ihtiyacım var mı?** Üretim kullanımında geçerli bir Aspose.Note for Java lisansı gereklidir.  
- **Yazdırılan sayfaları nasıl sınırlayabilirim?** `asposeAttr.setPrintRange(startPage, endPage)` ile yazdırma aralığını ayarlayın.  
- **Kopya sayısını değiştirebilir miyim?** Evet, `asposeAttr.setCopies(numberOfCopies)` kullanın.  
- **Sanal bir yazıcı destekleniyor mu?** Kesinlikle – Aspose.Note, Java'nın erişebildiği herhangi bir yüklü sanal yazıcıyla çalışır.

## “how to print onenote” ifadesi ne anlama geliyor?
Bu ifade, uygulamanızdan OneNote sayfa içeriğini programlı olarak bir yazıcıya ya da bir dosya formatına (PDF gibi) göndermeyi tanımlar. Aspose.Note for Java, düşük seviyeli yazdırma API'lerini soyutlayarak cihaz yönetimi yerine iş mantığına odaklanmanızı sağlar.

## OneNote'u yazdırmak için neden Aspose.Note for Java kullanmalısınız?
- **Tam kontrol** yazdırma seçenekleri üzerinde (aralık, kopya sayısı, yazıcı seçimi).  
- **Sorunsuz PDF oluşturma** “print to pdf java” desteğiyle sanal yazıcılar aracılığıyla.  
- **COM etkileşimi yok** – saf Java, çapraz platform sunucular için ideal.  
- **Sağlam hata yönetimi** `PrintException` ve ayrıntılı attribute sınıflarıyla.

## Önkoşullar

Başlamadan önce, aşağıdakilere sahip olduğunuzdan emin olun:

1. **Java Development Kit (JDK)** – 8 veya üzeri sürüm yüklü.  
2. **Aspose.Note for Java JAR** – resmi siteden **[buradan](https://releases.aspose.com/note/java/)** indirin.  
3. **OneNote belgesi** – yazdırmak istediğiniz bir `.one` dosyası.  
4. (İsteğe bağlı) Yüklü bir **sanal PDF yazıcı** (ör. Microsoft XPS Document Writer, doPDF).

## Paketleri İçe Aktarma

İlk olarak, gerekli sınıfları Java kaynak dosyanıza içe aktarın:

```java
import javax.print.PrintException;

import com.aspose.note.Document;
import com.aspose.note.DocumentPrintAttributeSet;
import com.aspose.note.PrintOptions;
```

## Adım‑Adım Kılavuz

### Adım 1: Bir Belgeyi Yazdırma (Temel)

Bu örnek, varsayılan yazıcıyı kullanarak tüm OneNote dosyasını yazdırır.

```java
public static void PrintDocument() throws PrintException {
    // Specify the directory where your document is located
    String dataDir = "Your Document Directory";
    
    // Load the OneNote document
    Document document = new Document(dataDir + "YourDocument.one");
    
    // Print the document
    document.print();
}
```

**Neden önemli:** Ek bir yapılandırma olmadan yazdırmayı tetiklemenin en basit yolunu gösterir.

### Adım 2: Özelleştirilmiş Yazdırma Ayarlarıyla Bir Belgeyi Yazdırma

Eğer **yazdırma ayarlarını özelleştirmeniz** gerekiyorsa—örneğin sadece 1‑2 sayfaları yazdırmak—`DocumentPrintAttributeSet` kullanabilirsiniz.

```java
public static void PrintDocumentWithPrintOptions() throws PrintException {
    // Specify the directory where your document is located
    String dataDir = "Your Document Directory";

    // Load the OneNote document
    Document document = new Document(dataDir + "YourDocument.one");

    // Define print options
    final DocumentPrintAttributeSet asposeAttr = new DocumentPrintAttributeSet("Microsoft XPS Document Writer");
    asposeAttr.setPrintRange(1, 2);

    // Print the document with specified options
    document.print(asposeAttr);
}
```

**İpucu:** Çıktıyı başka bir yere yönlendirmek için `"Microsoft XPS Document Writer"` ifadesini yüklü herhangi bir yazıcı adıyla değiştirin.

### Adım 3: Sanal Yazıcı Kullanarak Belgeleri Yazdırma (Print to PDF Java)

Sanal yazıcılar, Java'dan çıkmadan PDF dosyaları oluşturmanızı sağlar. Aşağıda **doPDF 8** örnek olarak kullanılmıştır.

```java
public static void PrintDocumentsWithVirtualPrinter() throws PrintException {
    // Specify the directory where your document is located
    String dataDir = "Your Document Directory";
    Document doc = new Document(dataDir + "YourDocument.one");
     
    // Define print options for virtual printer
    final DocumentPrintAttributeSet asposeAttr = new DocumentPrintAttributeSet("doPDF 8");
    asposeAttr.setPrintRange(1, 2);
    asposeAttr.setCopies(3);
     
    PrintOptions printOptions = new PrintOptions();
    printOptions.setDocumentName("YourDocument.one");
    printOptions.setPrinterSettings(asposeAttr);
      
    // Print the document using virtual printer
    doc.print(printOptions);
}
```

**Profesyonel ipucu:** Tek bir çalıştırmada kaç PDF kopyası üretileceğini kontrol etmek için `asposeAttr.setCopies()` ayarlayın.

## Yaygın Sorunlar ve Çözümler

| Sorun | Çözüm |
|-------|----------|
| **Yazıcı bulunamadı** | Windows > Devices and Printers bölümünde gösterildiği gibi yazıcı adının tam olarak eşleştiğini doğrulayın. |
| **`PrintException` oluştu** | OneNote dosyasının kilitli olmadığından ve JRE'nin yazıcıya erişim iznine sahip olduğundan emin olun. |
| **PDF çıktısı boş** | Sanal yazıcı sürücüsünün doğru şekilde yüklendiğini ve yazdırma işi için varsayılan olarak ayarlandığını kontrol edin. |
| **Yanlış sayfa aralığı** | Sayfa numaralarının 1‑tabanlı olduğunu unutmayın; `setPrintRange(1, 2)` ilk iki sayfayı yazar. |

## Sıkça Sorulan Sorular

### S1: OneNote belgesinin belirli sayfalarını yazdırabilir miyim?
**C:** Evet, çıktıyı ihtiyacınız olan sayfalara sınırlamak için `asposeAttr.setPrintRange(startPage, endPage)` kullanın.

### S2: Aspose.Note for Java sanal yazıcılarla uyumlu mu?
**C:** Kesinlikle. Kütüphane, Windows'un sunduğu herhangi bir yazıcıyla, sanal PDF yazıcıları da dahil olmak üzere çalışır.

### S3: Kopya sayısı gibi yazdırma ayarlarını özelleştirebilir miyim?
**C:** Evet, `print()` çağırmadan önce `asposeAttr.setCopies(numberOfCopies)` metodunu çağırın.

### S4: Aspose.Note for Java belgeleri yazdırmak için lisans gerektiriyor mu?
**C:** Üretim dağıtımları için geçerli bir lisans gereklidir; değerlendirme amacıyla geçici bir deneme lisansı mevcuttur.

### S5: Aspose.Note for Java için daha fazla destek ve kaynak nereden bulunabilir?
**C:** Forumlar, dokümantasyon ve örnekler için resmi destek sayfasını **[Aspose.Note for Java destek sayfası](https://forum.aspose.com/c/note/28)** ziyaret edin.

---

**Son Güncelleme:** 2026-01-18  
**Test Edilen Sürüm:** Aspose.Note for Java 24.12 (yazım anındaki en son sürüm)  
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}