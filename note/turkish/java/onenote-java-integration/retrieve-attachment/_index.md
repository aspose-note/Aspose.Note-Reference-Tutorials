---
date: 2025-12-31
description: Java ve Aspose.Note kullanarak OneNote eklerini nasıl çıkaracağınızı
  öğrenin. .one belgelerindeki dosyaları hızlı ve güvenilir bir şekilde alın.
linktitle: Retrieve Attachment from OneNote using Java
second_title: Aspose.Note Java API
title: Java kullanarak OneNote eklerini nasıl çıkarılır
url: /tr/java/onenote-java-integration/retrieve-attachment/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java ile OneNote eklerini nasıl çıkarılır

## Giriş

Günümüz dijital çağında, **OneNote verilerini programlı olarak nasıl çıkarılır** sorusu, belge‑odaklı uygulamalar geliştiren geliştiriciler için yaygın bir zorluktur. Aspose.Note for Java, Microsoft OneNote *.one* dosyalarından içerik okuyabilen, manipüle edebilen ve dışa aktarabilen zengin bir API sağlayarak bu görevi basitleştirir. Bu öğreticide, Java kullanarak bir OneNote defterinden resimler, PDF’ler veya Word belgeleri gibi ekleri nasıl alacağınızı öğreneceksiniz.

## Hızlı Yanıtlar
- **Hangi kütüphane gerekiyor?** Aspose.Note for Java  
- **.one dosyasından manuel paket açmadan dosyalar çıkarılabilir mi?** Evet, API .one formatını doğrudan okur.  
- **Geliştirme için lisansa ihtiyaç var mı?** Test için ücretsiz değerlendirme lisansı yeterlidir; üretim için tam lisans gereklidir.  
- **Hangi Java sürümü destekleniyor?** Java 8 ve üzeri.  
- **Toplu işleme mümkün mü?** Kesinlikle—aynı kodla birden çok belgeyi döngü içinde işleyebilirsiniz.

## “OneNote eklerini nasıl çıkarılır” nedir?
OneNote içeriğini çıkarmak, bir *.one* defterini programlı olarak okuyup gömülü kaynaklarını (ekler, resimler, metin) dışa aktarmak anlamına gelir. Bu, otomatik belge arşivleme, içerik taşıma veya özel raporlama gibi senaryoları mümkün kılar.

## Neden Aspose.Note for Java?
- **Tam format desteği** – OneNote dosya yapısının her öğesini işler.  
- **Office kurulumu gerekmez** – Sunucular veya CI pipeline’ları gibi başsız ortamlarla çalışır.  
- **Toplu‑işleme hazır** – Minimum bellek ayak iziyle tek çalışmada onlarca defteri işleyin.  

## Önkoşullar

Kodlamaya başlamadan önce aşağıdakilerin hazır olduğundan emin olun:

### Java Development Kit (JDK)

1. Oracle ya da bir OpenJDK dağıtımcısından en son JDK’yı indirin.  
2. JDK `bin` dizinini sistem `PATH`’inize ekleyin.  
3. `java -version` ve `javac -version` komutlarıyla doğrulayın.

### Aspose.Note for Java

1. Aspose.Note for Java’ın [indirilen sayfasına](https://releases.aspose.com/note/java/) gidin.  
2. En son sürüm arşivini indirin.  
3. JAR dosyalarını projenizin referans gösterebileceği bir klasöre çıkarın.

## Paketleri İçe Aktarma

Başlamak için ihtiyaç duyacağınız sınıfları içe aktarın. Aşağıdaki blok orijinal öğreticideki gibi değiştirilmemiştir:

```java
import java.io.ByteArrayInputStream;
import java.io.IOException;
import java.nio.file.Files;
import java.nio.file.Path;
import java.nio.file.StandardCopyOption;
import java.util.List;
import com.aspose.note.AttachedFile;
import com.aspose.note.Document;
```

> **İpucu:** Bu importları dosyanızın en üst kısmında tutmak, gelecekteki bakım işlerini kolaylaştırır.

## Adım‑Adım Kılavuz

### Adım 1: Belge Dizinini Tanımlama

Kaynak *.one* dosyasının makinenizde bulunduğu yeri belirtin.

```java
String dataDir = "Your Document Directory";
```

`"Your Document Directory"` ifadesini OneNote dosyanızın bulunduğu mutlak ya da göreli yol ile değiştirin.

### Adım 2: Belgeyi Yükleme

OneNote defterini temsil eden bir `Document` örneği oluşturun.

```java
Document doc = new Document(dataDir + "Sample1.one");
```

> Bu satır **OneNote dosyasını alır** ve sonraki işlemler için hazır hâle getirir.

### Adım 3: Ek Listesini Alın

Belgeden tüm ekli dosyaları (resimler, PDF’ler vb.) isteyin.

```java
List<AttachedFile> attachments = doc.getChildNodes(AttachedFile.class);
```

Dönen `List` içinde her bir gömülü kaynağı temsil eden `AttachedFile` nesneleri bulunur.

### Adım 4: Ekleri Alıp Kaydetme

Koleksiyonu döngüyle gezerek ikili veriyi çıkarın ve her dosyayı diske yazın.

```java
for (AttachedFile a : attachments) {
    byte[] buffer = a.getBytes();
    ByteArrayInputStream stream = new ByteArrayInputStream(buffer);
    String outputFile = "Output_" + a.getFileName();
    Path outputPath = Utils.getPath(RetrieveAttachment.class, outputFile);
    Files.copy(stream, outputPath, StandardCopyOption.REPLACE_EXISTING);
    System.out.println("File saved: " + outputPath);
}
```

- `a.getBytes()` ekin ham baytlarını döndürür.  
- `Utils.getPath(...)` güvenli bir çıktı konumu oluşturur (istediğiniz herhangi bir `Path` ile değiştirebilirsiniz).  
- Döngü, kaydedilen her dosyanın tam yolunu ekrana yazarak anlık geri bildirim sağlar.

## Yaygın Sorunlar & Çözümler

| Sorun | Neden Oluşur | Çözüm |
|-------|----------------|-----|
| **Hiç ek bulunamadı** | Defterde ekli dosya olmayabilir veya ekler farklı bir sayfada depolanmış olabilir. | *.one* dosyasını OneNote’ta manuel kontrol edin veya ekleri bulmak için sayfalar arasında (`doc.getChildNodes(Page.class)`) döngü yapın. |
| **Windows’da `AccessDeniedException`** | Çıktı klasörü yalnızca‑okunur veya yükseltilmiş izin gerektiriyor. | Yazılabilir bir dizin seçin (ör. kullanıcının `Documents` klasörü) veya JVM’i gerekli yetkilerle çalıştırın. |
| **Büyük dosyalar OutOfMemoryError veriyor** | Ekler aynı anda belleğe yükleniyor. | Bayt dizisini tamamen belleğe almadan `Files.newOutputStream` ile doğrudan dosyaya akıtın. |

## Sık Sorulan Sorular

**S1: Şifre korumalı OneNote belgelerinden ekler alınabilir mi?**  
C: Aspose.Note for Java, belgeyi yüklerken doğru kimlik bilgilerini sağladığınızda şifre korumalı defterleri açmayı destekler.

**S2: Aspose.Note for Java birden fazla OneNote dosyasının toplu işlenmesini destekliyor mu?**  
C: Evet, kodu *.one* dosyalarının bir listesini döngüyle işleyen bir yapı içine yerleştirerek her birinden ekleri çıkarabilirsiniz.

**S3: Alınabilecek eklerin boyut veya sayısı konusunda bir sınırlama var mı?**  
C: API büyük defterleri işlemek üzere tasarlanmıştır; pratik sınırlamalar JVM heap boyutunuza ve mevcut disk alanına bağlıdır.

**S4: Çıktı konumunu ve dosya adlandırma düzenini özelleştirebilir miyim?**  
C: Kesinlikle—döngüdeki `outputFile` ve `outputPath` değişkenlerini istediğiniz adlandırma şeması ve dizin yapısına göre değiştirebilirsiniz.

**S5: Aspose.Note for Java teknik sorunlar için destek sağlıyor mu?**  
C: Evet, geliştiriciler [https://forum.aspose.com/c/note/28](https://forum.aspose.com/c/note/28) adresindeki Aspose.Note forumu üzerinden kapsamlı destek alabilirler.

---

**Son Güncelleme:** 2025-12-31  
**Test Edilen Sürüm:** Aspose.Note for Java 24.11  
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}