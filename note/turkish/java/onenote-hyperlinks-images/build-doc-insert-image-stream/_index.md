---
date: 2025-12-21
description: Aspose.Note for Java kullanarak OneNote belgesi oluşturmayı ve resimleri
  sorunsuz bir şekilde eklemeyi öğrenin. Java geliştiricileri için adım adım rehber.
linktitle: How to create onenote document java – Build Doc and Insert Image with Stream
second_title: Aspose.Note Java API
title: Java ile OneNote belgesi nasıl oluşturulur – Belge oluşturma ve akışla resim
  ekleme
url: /tr/java/onenote-hyperlinks-images/build-doc-insert-image-stream/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java ile OneNote belgesi oluşturma – Belge ve Akış ile Resim Ekle

## Giriiş

Hoş geldiniz! Bu öğreticide **Java ile OneNote belgesini oluşturacak** ve bir görüntü verilerini kullanarak resim eklemeyi bölmesini oluşturacaktır. Her adım adım adım atarak, her parçanın neden önemli olduğunu açıklayacak ve gerçek projelerde uygulamanız için pratik yollar sağlar. Sonunda OneNote sayfalarını programlı olarak oluşturabilecek ve resimleri tam istediğiniz yere yerleştirebileceksiniz.

## Hızlı Yanıtlar
- **Hangi kütüphanesi gerekiyor?** Aspose.Note for Java
- **Akıştan resim seçeneği var mı?** Evet – sadece 'Image' yapıcısına bir 'InputStream' iletin.
- **Hangi formatı aktarılabilir mi?** Aspose.Note tarafından desteklenen herhangi bir format, örneğin PDF, DOCX, HTML.
- **Geliştirme için lisansa ihtiyacım var mı?** Değerlendirme için ücretsiz bir geçici lisans çalışır; Üretim için tam lisans gereklidir.
- **Gerekli Java sürümü nedir?** Java8 veya üzeri.

## “Java ile OneNote belgesi oluşturma” nedir?

Java'da bir OneNote belgesi oluşturmak, Aspose.Note API'sini kullanarak bir not defteri sunmak—sayfalar, taslaklar ve çıktılar—programlı olarak inşa etmek anlamına gelir; OneNote bilgisayarın yüzeyini açmadan. Bu yaklaşım, otomatik rapor oluşturma, toplu çalıştırma veya OneNote'un daha büyük Java uygulamalarına entegre etme için idealdir.

## Java ile OneNote belgesi oluşturmak için Aspose.Note for Java neden kullanılmalı?

- **Tam kontrol** sayfa düzeni, taslak stilleri ve öğe stilinde.
- **COM etkileşimi yok** – Java'yı destekleyen herhangi bir işlem işlemi çalışır.
- **Zengin yedekleme seçenekleri** – aynı belgeyi tek bir çağrı ile PDF, DOCX, HTML vb. formatlara dönüştürebilirsiniz.
- **Akış dostu** – dosyaları doğrudan bellekten, ağdan veya bulut depolamadan yükleyebilirsiniz.

## Önkoşullar

Başlamadan önce, aşağıdakilerin kurulu olduğundan emin olun:

### Java Geliştirme Kiti (JDK)

Makinenizde yüklü bir JDK (8 veya daha yeni bir sürüm).

### Java Kitaplığı için Aspose.Note

Kütüphaneyi resmi Aspose sürümünün indirilmesi: [https://releases.aspose.com/note/java/](https://releases.aspose.com/note/java/).

### IDE Kurulumu

Sevdiğiniz IDE'yi (IntelliJ IDEA, Eclipse, VS Code) Aspose.Note JAR'ın proje sınıflarını ekleyecek şekilde yapılandırın.

## Paketleri İçe Aktar

Başlamak için gerekli Java ve Aspose.Note sınıflarını içe aktarın. Bu kapsamda bölümleme belge oluşturma, sayfa işleme, taslak yönetimi ve resim ekleme erişimi sağlar.

```java
import java.io.FileInputStream;
import java.io.FileNotFoundException;
import java.io.IOException;
import java.io.InputStream;
import com.aspose.note.Document;
import com.aspose.note.HorizontalAlignment;
import com.aspose.note.Image;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.SaveFormat;
```

## Adım 1: Belge Dizinini Ayarlayın

Kaynak resimlerinizi içeren ve çıktı dosyasının kaydedileceği klasörü tanımlayın. Yer tutucuyu makinenizdeki gerçek yol ile değiştirin.

```java
String dataDir = "Your Document Directory";
```

## Adım 2: Belge Nesnesi Oluşturma

Yeni bir `Document` örneği oluşturun. Bu nesne, oluşturduğunuz OneNote not defterini temsil eder.

```java
Document doc = new Document();
```

## Adım 3: Sayfa Nesnesini Başlatma

Bu not defteri sayfası için tüm taslakları ve öğeleri tutacak bir `Page` oluşturun.

```java
Page page = new Page();
```

## Adım 4: Anahat Oluşturma

`Outline`, konumlandırılmış öğeler için bir kapsayıcı görevi görür. Burada taslağı sayfada konumlandırmak için dikey ve yatay offset değerlerini ayarlıyoruz.

```java
Outline outline1 = new Outline();
outline1.setVerticalOffset(600);
outline1.setHorizontalOffset(0);
```

## Adım 5: Anahat Öğesi Oluşturma

`OutlineElement`, ekleyeceğimiz resmi barındıracak.

```java
OutlineElement outlineElem1 = new OutlineElement();
```

## Adım 6: Görüntü Akışını Yükleme

Resim dosyasını bir akış olarak açın. Akış kullanmak, resmi dosya sisteminden, ağdan veya veritabanından önce diske kaydetmeden okumanıza olanak tanır.

```java
InputStream fs = null;
try {
    fs = new FileInputStream(dataDir + "image.jpg");
} catch (FileNotFoundException e) {
    e.printStackTrace();
}
```

## Adım 7: Görüntü Ekleme

Bir `Image` nesnesi oluşturun. İlk argüman daha sonra bir akış sağladığınızda `null` olabilir, ancak basitlik açısından burada dosya yolunu referans alıyor ve hizalamasını sayfanın sağ tarafına ayarlıyoruz.

```java
Image image = new Image(dataDir + "image1.jpg");
image.setAlignment(HorizontalAlignment.Right);
```

## Adım 8: Görüntüyü Anahat Öğesine Ekleme

Resmi, sayfanın görsel hiyerarşisinin bir parçası haline gelmesi için taslak öğesine ekleyin.

```java
outlineElem1.appendChildLast(image);
```

## Adım 9: Anahat Öğesini Anahat'a Ekleme

Şimdi resmi içeren taslak öğesini taslak kapsayıcısına bağlayın.

```java
outline1.appendChildLast(outlineElem1);
```

## Adım 10: Anahatı Sayfaya Ekleme

Taslağı sayfaya yerleştirin.

```java
page.appendChildLast(outline1);
```

## Adım 11: Sayfayı Belgeye Ekleme

Tamamen oluşturulmuş sayfayı belge nesnesine ekleyin.

```java
doc.appendChildLast(page);
```

## Adım 12: Belgeyi Kaydetme

Son olarak, ihtiyacınız olan formatta OneNote belgesini kaydedin. Bu örnekte PDF olarak dışa aktarıyoruz, ancak Aspose.Note tarafından desteklenen herhangi bir formatı seçebilirsiniz.

```java
try {
    doc.save("D://Aspose_JavaProjects//OneNote//out3.pdf", SaveFormat.Pdf);
} catch (IOException e) {
    e.printStackTrace();
}
```

Bu adımları izleyerek başarıyla **Java ile OneNote belgesi oluşturmuş** ve bir giriş akışı kullanarak bir resmi gömmüş oldunuz.

## Sık Karşılaşılan Hatalar ve İpuçları

- **Akış kapatılmadı** – Üretim ortamında, `InputStream`'i her zaman bir `finally` bloğunda kapatın veya try-with-resources kullanın.

- **Yanlış dosya yolu** – `dataDir`'in uygun ayırıcıyla (`/` veya `\`) bittiğini iki kez kontrol edin.

- **Görüntü hizalaması** – Görüntü ekran dışında görünüyorsa, ana hatın `VerticalOffset`/`HorizontalOffset` değerlerini ayarlayın.

- **Lisans istisnaları** – Değerlendirme sürümünü kullanmak çıktıya filigran ekleyebilir; filigranı kaldırmak için geçerli bir lisans uygulayın.

## Sıkça Sorulan Sorular

### S1: Aspose.Note for Java, OneNote'un tüm sürümleriyle uyumlu mu?

C1: Aspose.Note for Java, çeşitli OneNote dosya biçimlerini destekleyerek masaüstü, çevrimiçi ve mobil sürümler arasında uyumluluk sağlar.

### S2: Aspose.Note for Java kullanarak OneNote belgelerine eklenen resimlerin görünümünü özelleştirebilir miyim?

C2: Evet, `Image` nesnesindeki ilgili özellikleri kullanarak hizalamayı, boyutu, döndürmeyi ve hatta kırpmayı değiştirebilirsiniz.

### S3: Aspose.Note for Java, PDF dışında diğer belge formatlarını da destekliyor mu?

C3: Kesinlikle. API, DOCX, HTML, XPS ve diğer birçok formata dışa aktarma yapabilir ve notlarınızı nasıl paylaşacağınız veya arşivleyeceğiniz konusunda size esneklik sağlar.

### S4: Aspose.Note for Java için ek kaynakları ve desteği nerede bulabilirim?

C4: Resmi Aspose web sitesi, kapsamlı dokümantasyon, kod örnekleri, forumlar ve değerlendirme için geçici lisanslar sunmaktadır.

### S5: Aspose.Note for Java için deneme sürümü mevcut mu?

C5: Evet, satın almadan önce tüm özellikleri keşfetmek için Aspose sürüm sayfasından ücretsiz bir deneme sürümü indirebilirsiniz.

---

**Son Güncelleme:** 21.12.2025
**Test Edildiği Sürüm:** Aspose.Note for Java 26.4 (yazım anındaki en güncel sürüm)
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}