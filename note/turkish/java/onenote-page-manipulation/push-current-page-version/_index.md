---
date: 2026-01-12
description: Aspose.Note for Java ile mevcut sürümü iterek OneNote sayfalarını nasıl
  kaydedeceğinizi öğrenin. OneNote dosyasını yükleme, geçmiş ekleme, sayfayı klonlama
  ve sürüm geçmişini güncelleme konularını kapsayan adım adım rehber.
linktitle: Push Current Page Version in OneNote - Aspose.Note
second_title: Aspense.Note Java API
title: OneNote Sayfa Sürümünü Kaydetme – OneNote'ta Mevcut Sayfa Sürümünü Gönder -
  Aspose.Note
url: /tr/java/onenote-page-manipulation/push-current-page-version/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote Sayfa Sürümünü Kaydetme – Mevcut Sayfa Sürümünü OneNote'da İtme

## Giriş

Bu öğreticide, Aspose.Note for Java kullanarak mevcut sayfa sürümünü iterek **OneNote** sayfalarını nasıl kaydedeceğinizi keşfedeceksiniz. Tam bir denetim izi tutmanız gerekse ya da sadece sürüm geçmişini yönetmeniz gerekse, aşağıdaki adımlar bir OneNote dosyasını nasıl yükleyeceğinizi, geçmiş girişleri ekleyeceğinizi, bir sayfayı klonlayacağınızı ve OneNote sürümünü programlı olarak nasıl güncelleyeceğinizi gösterir.

## Hızlı Yanıtlar
- **“push current page version” ne anlama geliyor?** Mevcut sayfanın bir anlık görüntüsünü belgenin sürüm geçmişine ekler.  
- **Neden Aspose.Note for Java kullanmalı?** Microsoft Office gerektirmeden OneNote dosyalarını manipüle etmek için saf‑Java bir API sağlar.  
- **Bunu denemek için lisansa ihtiyacım var mı?** Ücretsiz bir deneme indirilebilir, ancak üretim kullanımı için lisans gereklidir.  
- **Birçok sayfa için sürümlemeyi otomatikleştirebilir miyim?** Evet, sayfalar arasında döngü kurabilir ve her biri için aynı API'yi çağırabilirsiniz.  
- **Kaydedilen dosya en yeni OneNote ile uyumlu mu?** Aspose.Note, mevcut OneNote formatlarıyla uyumluluğu sürdürür.

## Sürüm geçmişiyle “OneNote nasıl kaydedilir” ne demektir?
Sürüm geçmişiyle OneNote kaydetmek, her düzenlemeyi ayrı bir giriş olarak depolamak anlamına gelir; böylece daha sonra geri alabilir veya değişiklikleri inceleyebilirsiniz. Aspose.Note’un `PageHistory` sınıfı bunu basitleştirir.

## Neden mevcut sayfa sürümünü itmeliyiz?
- **Denetlenebilirlik:** Her değişiklik kaydedilir, uyumluluk gereksinimlerini karşılar.  
- **İşbirliği:** Takım üyeleri kimlerin neyi ne zaman değiştirdiğini görebilir.  
- **Güvenlik:** Kazara üzerine yazılan içerik geçmişten geri getirilebilir.

## Önkoşullar

Başlamadan önce, şunların olduğundan emin olun:

1. Java programlama temelleri hakkında bilgi.  
2. Makinenizde yüklü Java Development Kit (JDK).  
3. Aspose.Note for Java kütüphanesi – bunu [buradan](https://releases.aspose.com/note/java/) indirebilirsiniz.  
4. Sürümlemek istediğiniz bir örnek OneNote belgesi (ör. `Sample1.one`).

## Paketleri İçe Aktarın

İlk olarak, OneNote belgeleri ve bunların geçmişiyle çalışabilmek için gerekli sınıfları içe aktarın.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.PageHistory;
```

## Adım 1: OneNote Belgesini Yükleyin

OneNote dosyasını yüklemek, **geçmiş ekleme** sürecinin ilk adımıdır. API, `.one` dosyasını bir `Document` nesnesine okur.

```java
String dataDir = "Your Document Directory";
Document document = new Document(dataDir + "Sample1.one");
```

> **İpucu:** `dataDir`, OneNote dosyanızın bulunduğu klasöre işaret etmelidir. Farklı bir belgeyle çalışıyorsanız dosya adını ayarlayın.

## Adım 2: Mevcut Sayfayı ve Onun Geçmişini Alın

Sürüm geçmişini yönetmek için sürümlemek istediğiniz sayfaya ve ona bağlı `PageHistory` nesnesine bir referansa ihtiyacınız var.

```java
Page page = document.getFirstChild();
PageHistory pageHistory = document.getPageHistory(page);
```

> **Neden önemli:** `getFirstChild()` ilk sayfayı alır (diğerleri için döngü yapabilirsiniz) ve `getPageHistory(page)` sürüm anlık görüntülerinin saklandığı konteyneri size verir.

## Adım 3: Mevcut Sayfa Sürümünü İtin

Şimdi **sayfayı klonlamayı** ve geçmişe itmemizi yapıyoruz. Klonlama, gelecekteki düzenlemelerden bağımsız bir derin kopya oluşturur.

```java
pageHistory.addItem(page.deepClone());
```

> **Pro ipucu:** `deepClone()` kullanmak, tüm iç içe öğelerin (metin, resimler, tablolar) sürüm girişinde yakalanmasını garanti eder.

## Adım 4: Belgeyi Kaydedin

Son olarak, belgeyi kaydederek **OneNote sürümünü güncelleyin**. Yeni dosya eklenen geçmiş girişini içerecek.

```java
document.save(dataDir + "PushCurrentPageVersion_out.one");
```

OneNote'ta `PushCurrentPageVersion_out.one` dosyasını açtığınızda, UI üzerinden erişilebilen sürüm geçmişini göreceksiniz.

## Yaygın Tuzaklar ve Nasıl Kaçınılır

- **Yazma izinlerinin eksik olması:** Çıktı dizininin yazılabilir olduğundan emin olun; aksi takdirde `save()` bir istisna fırlatır.  
- **Yanlış dosya yolu:** `dataDir`'in bir yol ayırıcı (`/` veya `\`) ile bittiğini iki kez kontrol edin.  
- **Büyük belgeler:** Çok büyük OneNote dosyaları için, bellek kullanımını azaltmak amacıyla yalnızca sürümlemeniz gereken sayfaları klonlamayı düşünün.

## Sonuç

Artık **OneNote** sayfalarını mevcut sürümü iterek nasıl kaydedeceğinizi, etkili bir şekilde **sürüm geçmişini yönetebileceğinizi** ve Aspose.Note for Java kullanarak **OneNote sürümünü güncelleyebileceğinizi** biliyorsunuz. Bu yaklaşım otomatik raporlama hatlarına, yedekleme çözümlerine veya işbirlikçi düzenleme araçlarına entegre edilebilir.

## Sıkça Sorulan Sorular

**S: Aspose.Note for Java'yı şifreli OneNote dosyalarıyla kullanabilir miyim?**  
C: Evet, kütüphane hem şifreli hem de şifresiz OneNote belgelerini açmayı destekler.

**S: API en yeni OneNote sürümleriyle uyumlu mu?**  
C: Aspose.Note, en yeni OneNote dosya formatlarıyla uyumlu kalmaya çalışır.

**S: Sürümleme sırasında metin ve resimleri manipüle edebilir miyim?**  
C: Kesinlikle. Sayfa içeriğini düzenleyebilir, ardından değişiklikleri yakalamak için yeni bir sürüm itebilirsiniz.

**S: Aspose.Note OneNote dosyalarını diğer formatlara dönüştürmeye izin veriyor mu?**  
C: Evet, API üzerinden doğrudan PDF, HTML veya görüntü formatlarına dönüştürebilirsiniz.

**S: Sorun yaşarsam nereden yardım alabilirim?**  
C: Topluluk desteği için [Aspose.Note forumunu](https://forum.aspose.com/c/note/28) ziyaret edin veya Aspose destek ile iletişime geçin.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Last Updated:** 2026-01-12  
**Tested With:** Aspose.Note for Java 24.11  
**Author:** Aspose  

---