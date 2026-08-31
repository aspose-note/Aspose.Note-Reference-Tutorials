---
date: 2026-01-12
description: Aspose.Note for Java kullanarak OneNote sayfa sayısını nasıl alacağınızı
  ve toplam OneNote sayfalarını nasıl yazdıracağınızı öğrenin. Bu öğreticide, sayfa
  sayısını almak ve görüntülemek için adım adım kod gösterilmektedir.
linktitle: Get OneNote Page Count with Aspose.Note for Java
second_title: Aspose.Note Java API
title: Aspose.Note for Java ile OneNote Sayfa Sayısını Al
url: /tr/java/onenote-page-manipulation/get-page-count/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Note for Java ile OneNote Sayfa Sayısını Alın

## Giriiş

Bu öğreticide, Aspose.Note for Java'yı kullanarak bir OneNote belgesinden **OneNote sayfa sayısını nasıl aldığınızı** bilgileriniz. Projeyi kurma, bir `.one` yükleme, sayfa sayısını alma ve sonunda **toplam OneNote sayfalarını** konsola **yazdırma** adımlarını birlikte inceleyerek oynayın. Raporlama aracı oluşturma ya da belge saklamanız gerekiyorsa, bu kılavuz boyutunda net, çalıştırmaya hazır bir çözüm sunar.

## Hızlı Yanıtlar
- **Bu eğitimi kapsıyor mu?** Aspose.Note for Java ile bir OneNote dosyasındaki toplam sayfa sayısını alıp yazdırma.
- **Hangi sürümü gerekli mi?** Aspose.Note for Java (resmi sürümün indirilmesi).
- **Lisans gerekli mi?** Test için ücretsiz deneme sürümü çalışır; üretim için ticari lisans gerekir.
- **Kaç satır kod?** Sadece dört kısa pasaj – bir içe aktarma, bir yükleme, bir sayma ve bir yazdırma.
- **Herhangi bir işletim sisteminde çalıştırılabilir miyim?** Evet, uyumlu bir JDK ve Aspose.Note JAR'ı olduğu süre boyunca.

## Önkoşullar

Başlamadan önce, aşağıdaki ön bilgilere sahip olduğunuzdan emin olun:

1. **Java Development Kit (JDK)** – herhangi bir güncel sürüm (JDK8 veya üzeri).
2. **Aspose.Note for Java Library** – kütüphaneyi [indirme sayfası](https://releases.aspose.com/note/java/) adresinden indirip kurun.
3. **Entegre Geliştirme Ortamı (IDE)** – IntelliJ IDEA, Eclipse veya herhangi bir editörü tercih ettiniz.

## Paketleri İçe Aktar

Başlamak için, Java projenize gerekli kapları içe aktarın:

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Page;
```

Şimdi, örneği birden fazla adıma ayıralım:

## 1. Adım: Projenizi Kurun

IDE'nizde yeni bir Java projesi oluşturur ve Aspose.Note JAR'ını farklı sınıf seçeneklerini tamamlar. Bu, daha sonra kullanılacak `Belge` ve `Sayfa` sınıflarına erişim sağlar.

## Adım 2: Belgeyi Yükleyin

```java
String dataDir = "Your Document Directory";
Document doc = new Document(dataDir + "Sample1.one");
```

`"Your Document Directory"` ifadesini OneNote `.one` dosyanızın bulunduğu gerçek yol ile değiştirin.

## Adım 3: Sayfa Sayısını Alın

```java
int count = doc.getChildNodes(Page.class).size();
```

`getChildNodes(Page.class).size()` çağrısı toplam sayfa sayısını döndürür; bu, **OneNote sayfa sayısını almanın** temelidir.

## Toplam OneNote Sayfasını Yazdır

```java
System.out.printf("Total Pages: %s", count);
```

Bu satır **toplam OneNote sayfalarını** konsola **yazdırır**, size anlık geri bildirim sağlar.

## Çözüm

Bu basit adımları izleyerek, Aspose.Note for Java'yı kullanarak herhangi bir OneNote belgesinin sayfa sayısını zahmetsizce alıp görüntüleyebilirsiniz. Bu snippet'i daha büyük uygulamalara entegre ederek belge analizini otomatikleştirir, özetler halinde veya içerikte doğru biçimde oluşturabilirsiniz.

## Sıkça Sorulan Sorular

**S: Bu kodu çok‑iş parçalarıyla birleştirilmiş bir şekilde kullanılabilir miyim?**
C: Evet, `Document` sınıfı yalnızca okuma işlemleri için thread-safe'dir. Aynı `Belge' örneğinin aynısı ve değiştirmekten vazgeçmek.

**S: Dosya yolu yanlış olursa ne olur?**
A: Bir `IOException` başlatılır. Dosyanın eksik olması verilerinin ele almak için işlenmesi try‑catch yüklemenin sürdürülmesine alınır.

**S: Şifreli OneNote dosyalarıyla çalışır mı?**
C: Aspose.Note şu anda şifreli OneNote penceresini açmayı desteklemiyor. İşleme girmeden önce korumayı kaldırmanız gerekir.

**S: Büyük bir not defterindeki sayfalarda verimli bir şekilde nasıl sayabilirim?**
A: `getChildNodes` yöntemi zaten optimize edilmiştir, ancak yalnızca belirli bir sayfa alt ayarına ihtiyacınız varsa, akış değişimi (akış) olarak da görüntüleyebilirsiniz.

**S: Sayfaları saydıktan sonra her sayfanın başlığını listeleyebilir miyim?**
A: Evet, `doc.getChildNodes(Page.class)` üzerinde döngü kurup `page.getTitle()` yöntemini çağırarak her sayfanın başlığını alabilirsiniz.

---

**Son Güncelleme:** 2026-01-12
**Şunlarla Test Edildi:** Java 24.12 için Aspose.Note
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}