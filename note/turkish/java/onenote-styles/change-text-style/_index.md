---
date: 2026-01-18
description: Java'da OneNote'ta yazı tipi rengini nasıl ayarlayacağınızı, Aspose.Note
  kullanarak metni vurgulamayı, yazı tipi boyutunu değiştirmeyi ve OneNote'u PDF olarak
  kaydetmeyi öğrenin. Adım adım kodlu rehber.
linktitle: Change Text Style in OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: OneNote'ta Java ile Yazı Tipi Rengini Ayarla – Aspose.Note
url: /tr/java/onenote-styles/change-text-style/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote'ta Java ile Yazı Tipi Rengini Ayarlama – Aspose.Note

## Giriş

## Hızlı Yanıtlar
- **Belirli kelimelerin yazı tipi rengini değiştirebilir miyim?** Evet – `TextRun` nesneleri üzerinden döngü yaparak `setFontColor` ayarlayın.
- **Aspose.Note OneNote'u PDF olarak kaydetmeme izin veriyor mu?** Kesinlikle; `document.save("output.pdf")` kullanın.
- **Hangi Java sürümü gerekiyor?** Java 8 veya üzeri.
- **Vurgulama destekleniyor mu?** `TextStyle` üzerinde `setHighlight(Color)` kullanın.
- **OneNote'u tek satırda PDF'ye dönüştürebilir miyim?** Doğrudan değil, ancak `save` yöntemi dönüşümü gerçekleştirir.

## “set font color java” nedir?

Bu ifade, Java kodu kullanarak bir OneNote dosyasındaki metin öğelerine programlı olarak yeni bir yazı tipi rengi atamayı ifade eder. Aspose.Note ile, OneNote arayüzünü açmadan yazı tipi rengi, vurgulama ve boyut gibi stil özellikleri üzerinde tam kontrol elde edersiniz.

## OneNote'ta metin stilini neden değiştirmelisiniz?

- **Gelişmiş okunabilirlik** – renkli veya vurgulanan metin, ana noktalara dikkat çeker.
- **Marka tutarlılığı** – toplantı notları boyunca kurumsal renkleri zorunlu kılar.
- **Dışa aktarma kalitesi** – stil verilen notlar, **onenote'u pdf'ye dönüştürerek** paylaşıldığında daha profesyonel görünür.

## Önkoşullar

İçeriğe geçmeden önce şunların olduğundan emin olun:

1. Temel Java programlama bilgisi.  
2. JDK 8 veya daha yeni bir sürüm yüklü.  
3. Projeye Aspose.Note for Java kütüphanesinin eklenmesi (Maven/Gradle veya manuel JAR).  
4. Deneme yapmak için bir örnek OneNote dosyası (`Sample1.one`).

## Paketleri İçe Aktarma

İlk olarak, ihtiyacımız olan sınıfları içe aktarın:

```java
import java.awt.Color;
import java.io.IOException;
import java.util.List;
import com.aspose.note.Document;
import com.aspose.note.RichText;
import com.aspose.note.TextRun;
import com.aspose.note.TextStyle;
```

## Adım Adım Kılavuz

### Adım 1: Belgeyi Yükleme

```java
// Load the document into Aspose.Note
Document document = new Document("Your Document Directory/Sample1.one");
```

OneNote dosyasını (`Sample1.one`) yüklüyoruz, böylece Aspose.Note iç yapısıyla çalışabilir.

### Adım 2: RichText Düğümlerine Erişim

```java
// Get a particular RichText node
List<RichText> richTextNodes = document.getChildNodes(RichText.class);
RichText richText = richTextNodes.get(0);
```

`RichText` nesneleri gerçek paragrafları içerir. İlk düğümü alarak stil vermek istediğimiz metne bir referans elde ederiz.

### Adım 3: Metin Stilini Değiştir (set font color java)

```java
for (TextRun run : richText.getTextRuns()) {
    // Set font color
    run.getStyle().setFontColor(Color.yellow);
    // Set highlight color
    run.getStyle().setHighlight(Color.blue);
    // Set font size
    run.getStyle().setFontSize(20);
}
```

Döngü içinde **set font color Java** ile metni sarıya ayarlıyoruz, mavi bir vurgulama uyguluyoruz (**highlight text onenote** örneği) ve boyutu 20 punto artırıyoruz, bu da **modify font size onenote** örneğidir.

### Adım 4: Belgeyi Kaydet (save onenote as pdf)

```java
document.save("Your Document Directory/ChangeTextStyle_out.pdf");
System.out.printf("File saved: %s\n", "Your Document Directory/ChangeTextStyle_out.pdf");
```

`save` metodunu `.pdf` uzantısıyla çağırmak, otomatik olarak **convert onenote to pdf** yapar ve paylaşmaya hazır bir dosya oluşturur.

## Yaygın Sorunlar ve Çözümler

| Sorun | Sebep | Çözüm |
|-------|-------|-------|
| Renk değişikliği görünmüyor | Belge, kaydetmeden önce OneNote'ta açıktı | Java işlemi tamamlandıktan sonra OneNote'u kapatın veya dosyayı yeniden yükleyin |
| Vurgulama uygulanmadı | Arka planla aynı renkte bir renk kullanılıyor | Zıt bir `Color` seçin (ör. `Color.yellow`) |
| `document.save` `IOException` hatası veriyor | Geçersiz çıktı yolu | Dizin mevcut olduğundan ve yazma izniniz olduğundan emin olun |

## Sık Sorulan Sorular

**S: Bu stil değişikliklerini OneNote dosyamın yalnızca belirli bölümlerine uygulayabilir miyim?**  
C: Evet – `TextRun`'ler üzerinde döngü yapmadan önce `RichText` düğümlerini üst `Section` veya `Page`'e göre filtreleyin.

**S: Renk, vurgulama ve boyut dışında Aspose.Note hangi diğer biçimlendirmeleri yapabilir?**  
C: Yazı tipi ailesi, kalın/eğik/altı çizili, hizalama ve hatta paragraf aralığını değiştirebilirsiniz.

**S: Birden fazla OneNote dosyasını toplu işleme yapmak mümkün mü?**  
C: Kesinlikle. Yükleme ve stil verme mantığını, klasördeki her `.one` dosyasını işleyen bir döngüye sarın.

**S: Kütüphane DOCX gibi diğer formatlara doğrudan kaydetmeyi destekliyor mu?**  
C: Evet – Aspose.Note PDF, DOCX, HTML ve çeşitli görüntü formatlarına dışa aktarabilir.

**S: Daha fazla örnek ve API referansını nereden bulabilirim?**  
C: Resmi Aspose.Note dokümantasyon sitesini ziyaret edin, API referansını inceleyin ve ücretsiz deneme sürümünü indirerek uygulamalı test yapın.

## Sonuç

Artık Aspose.Note kullanarak **set font color Java**, metni vurgulama, yazı tipi boyutunu ayarlama ve **OneNote'u PDF olarak kaydetme** konularında tam bir uçtan uca örneğe sahipsiniz. Kodu belirli sayfalara hedeflemek, koşullu stil uygulamak veya daha büyük belge‑işleme akışlarına entegre etmek için özgürce uyarlayabilirsiniz.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Last Updated:** 2026-01-18  
**Tested With:** Aspose.Note 24.11 for Java  
**Author:** Aspose