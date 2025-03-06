---
title: OneNote'ta Geçerli Sayfa Sürümünü Aktarın - Aspose.Note
linktitle: OneNote'ta Geçerli Sayfa Sürümünü Aktarın - Aspose.Note
second_title: Aspose.Note Java API'si
description: OneNote içeriğini güncel tutun! Sayfa geçmişini güncellemeyi ve sürümleri yönetmeyi öğrenin; adım adım kılavuz ve kod dahildir. #OneNote #Java #Aspose
weight: 18
url: /tr/java/onenote-page-manipulation/push-current-page-version/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote'ta Geçerli Sayfa Sürümünü Aktarın - Aspose.Note

## giriiş

Bu eğitimde, geçerli sayfa sürümünü OneNote'a aktarmak için Aspose.Note for Java'yı nasıl kullanabileceğimizi keşfedeceğiz. Aspose.Note, geliştiricilerin Microsoft OneNote belgeleriyle programlı olarak çalışmasına olanak tanıyan, OneNote dosyalarını oluşturma, değiştirme ve dönüştürme gibi çeşitli işlemleri mümkün kılan güçlü bir Java kitaplığıdır.

## Önkoşullar

Başlamadan önce aşağıdaki önkoşullara sahip olduğunuzdan emin olun:
1. Java programlama dili hakkında temel bilgiler.
2. Sisteminize Java Development Kit (JDK) yüklendi.
3.  Aspose.Note for Java kütüphanesi. Şuradan indirebilirsiniz[Burada](https://releases.aspose.com/note/java/).
4. Üzerinde çalışılacak örnek bir OneNote belgesi.

## Paketleri İçe Aktar

Aspose.Note işlevlerini kullanmak için öncelikle Java projenize gerekli paketleri içe aktarmanız gerekir.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.PageHistory;
```

## 1. Adım: OneNote Belgesini Yükleyin

```java
String dataDir = "Your Document Directory";
Document document = new Document(dataDir + "Sample1.one");
```

 Burada,`dataDir` OneNote belgenizin bulunduğu dizini işaret etmelidir. Yer değiştirmek`"Sample1.one"` OneNote dosyanızın adıyla.

## Adım 2: Geçerli Sayfayı ve Geçmişini Alın

```java
Page page = document.getFirstChild();
PageHistory pageHistory = document.getPageHistory(page);
```

 Belgenin ilk sayfasını kullanarak alıyoruz`getFirstChild()` ve ardından geçmişini kullanarak elde edin`getPageHistory()`.

## Adım 3: Geçerli Sayfa Sürümünü Aktarın

```java
pageHistory.addItem(page.deepClone());
```

Burada sayfanın güncel sürümünü kopyalayıp yeni bir öğe olarak ekleyerek geçmişine ekliyoruz.

## Adım 4: Belgeyi Kaydedin

```java
document.save(dataDir + "PushCurrentPageVersion_out.one");
```

Son olarak değiştirilen belgeyi güncellenmiş sayfa geçmişiyle birlikte kaydediyoruz.

## Çözüm

Bu eğitimde, Aspose.Note for Java'yı kullanarak OneNote'ta geçerli sayfa sürümünü nasıl aktaracağımızı öğrendik. Bu adımları izleyerek OneNote belgelerinizin sürümlendirmesini programlı olarak etkili bir şekilde yönetebilirsiniz.

## SSS'ler

### S1: Şifrelenmiş OneNote dosyalarıyla çalışmak için Aspose.Note for Java'yı kullanabilir miyim?

Cevap1: Evet, Aspose.Note for Java, hem şifrelenmiş hem de şifrelenmemiş OneNote dosyalarıyla çalışmayı destekler.

### S2: Aspose.Note for Java, OneNote'un en son sürümüyle uyumlu mu?

Cevap2: Aspose.Note for Java, OneNote belgelerinin en son sürümleriyle uyumluluğu korumaya çalışmaktadır.

### S3: Aspose.Note for Java'yı kullanarak OneNote belgeleri içindeki metin ve görselleri değiştirebilir miyim?

Cevap3: Kesinlikle, Aspose.Note for Java, OneNote dosyalarındaki metin, resim ve diğer öğelerin işlenmesi için kapsamlı işlevler sağlar.

### S4: Aspose.Note for Java, OneNote dosyalarının diğer formatlara dönüştürülmesini destekliyor mu?

Cevap4: Evet, Aspose.Note for Java, OneNote dosyalarının PDF, HTML ve görüntü formatları gibi çeşitli formatlara dönüştürülmesini destekler.

### S5: Herhangi bir sorunla karşılaşırsam Aspose.Note for Java desteğini nereden alabilirim?

 A5: ziyaret edebilirsiniz[Aspose.Note forumu](https://forum.aspose.com/c/note/28) topluluktan yardım istemek veya doğrudan Aspose desteğiyle iletişime geçmek için.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
