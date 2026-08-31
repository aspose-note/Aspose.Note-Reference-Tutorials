---
date: 2026-01-15
description: Aspose.Note for Java kullanarak OneNote'ta değişiklikleri izlemeyi ve
  OneNote belgelerindeki sayfa revizyonlarını yönetmeyi öğrenin. Bir revizyon özeti
  örneği ve revizyon tarihini nasıl değiştireceğinizi içerir.
linktitle: Working with Page Revisions in OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: OneNote'da değişiklikleri izleme – Aspose.Note ile Sayfa Revizyonlarını Yönet
url: /tr/java/onenote-page-manipulation/working-with-page-revisions/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote'ta Sayfa Revizyonlarıyla Çalışma - Aspose.Note

## Giriiş

OneNote, notları düzenlemek için güçlü bir araç ve **değişiklikleri takip eden onenote** ülkelerinde, sayfa değişikliklerinin oluşturulması etkili iş birliği için hayati öneme sahiptir. Aspose.Note for Java dosya değişikliklerini programlı olarak ele alabilir, bir programın kim tarafından yönetileceğini görebilir ve hatta zaman damgalarını ayarlayabilirsiniz. Bu öğretici, bir belgeyi yüklemeden güncellemeye, özetlemeyi güncellemeye kadar adım boyutunu gösterir.

## Hızlı Yanıtlar
- **takip değişiklikleri onenote ne anlıyor?** Bu, bir OneNote kimin ne zaman saklamasını izlemeyi ifade eder.
- **Hangi kütüphanesi gereklidir?** Aspose.Note for Java.
- **Bir düzeltmenin yazarını veya ortaya çıkma ihtimali var mı?** Evet, RevisionSummary API'si (`revizyon tarihini değiştir`) ile.
- **Önceden bir OneNote dosyasına ihtiyacım var mı?** Evet, bir örnek `.one` dosyası gereklidir.
- **Üretim için lisans gerekli mi?** Ticari kullanım için geçerli bir Aspose.Note lisansı gereklidir.

## Revizyon özeti örneği nedir?

*revizyon özeti* bir sayfadaki en son değişiklikler hakkında meta veriler sağlar—yazar adı, son değişme zamanı ve diğer ayrıntılar. Bu rehberde bu bilgileri alıp görüntüleyecek, ardından **revizyon tarihini değiştir** nasıl göreceksinizz.

## Aspose.Note ile onenote'taki değişiklikleri neden takip etmelisiniz?

- **İşbirliği:** En son düzenlemeleri kimin yaptığını kısaca görebilirsiniz.
- **Denetim:** Uyumluluk için güvenilir bir geçmişini tutun.
- **Otomasyon:** Revizyon yönetimini arka uç hizmetlerine veya taşıma araçlarına entegre edin.

## Önkoşullar

### Java Geliştirme Ortamı
Sisteminize Java Development Kit (JDK) kurulu olduğundan emin olun.

### Java Kitaplığı için Aspose.Note
Aspose.Note for Java kütüphanesini [buradan](https://releases.aspose.com/note/java/) indirip kurun.

### OneNote Belgesi
Test amaçlı bir örnek OneNote belgesine sahip olun.

## Paketleri İçe Aktar
Java projenizde Aspose.Note for Java ile çalışmak için gerekli kapları içe aktarın.

```java
import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.RevisionSummary;
import java.io.IOException;
import java.util.Calendar;
```

Sağlanan örneği daha net anlamak için birden fazla adıma ayıralım.

## Adım 1: OneNote Belgesini Yükle

İlk olarak, OneNote belgesini yükleyin ve ilk alt sayfayı alın.

```java
String dataDir = "Your Document Directory";
Document document = new Document(dataDir + "Sample1.one");
Page page = document.getFirstChild();
```

## Adım 2: Sayfa Revizyon Özeti Okuma

Sayfa için içerik revizyon özetini okuyun. Bu, sayfayı en son kimin düzenlediğini gösteren **revision summary example**'dır.

```java
RevisionSummary pageRevisionInfo = page.getPageContentRevisionSummary();
System.out.println(String.format("Author:\t%s\nModified:\t%s",
        pageRevisionInfo.getAuthorMostRecent(),
        pageRevisionInfo.getLastModifiedTime().toString()));
```

## Adım 3: Sayfa Revizyon Özetini Güncelleme

Sayfa revizyon özetini yeni bir yazar ve yeni bir değiştirilme tarihiyle güncelleyin. Bu, **modify revision date**'i programlı olarak nasıl yapacağınızı gösterir.

```java
pageRevisionInfo.setAuthorMostRecent("New Author");
Calendar modifiedDate = Calendar.getInstance();
pageRevisionInfo.setLastModifiedTime(modifiedDate.getTime());
document.save(dataDir + "WorkingWithPageRevisions_out.one");
```

## Çözüm

OneNote sözleşmelerindeki sayfa güncellemelerini programlı olarak yapılandırma, Aspose.Note for Java ile basit bir şekilde kullanılabilir. Bu bilgisayarda gezinmek suretiyle **değişiklikleri takip ederek onenote**'u etkili bir şekilde gerçekleştirebilir, inceleme ayrıntılarını görüntüleyebilir ve hatta iş incelemenize kayıt ederek **revizyon tarihini değiştirebilirsiniz**'i değiştirebilirsiniz.

## SSS

### S1: Aspose.Note for Java'yı diğer Java kütüphaneleriyle birlikte kullanabilir miyim?

A: Evet, Aspose.Note for Java, kurtarmak için diğer Java kütüphaneleriyle entegre edilebilir.

### S2: Aspose.Note for Java tüm OneNote belge sürümlerini yüklemiş mi?

A: Aspose.Note for Java, eski sürümler dahil olmak üzere çeşitli OneNote belge sürümlerini içerir.

### S3: Aspose.Note for Java kurumsal düzeydeki uygulamalar için uygun mu?

C: Kesinlikle, Aspose.Note for Java, güçlü özellikler ve ölçeklenebilirliğiyle kurumsal olarak saklanabilecek kapasiteler uygun şekilde tasarlanmıştır.

### S4: Aspose.Note for Java ile sayfa iyileştirmelerini özelleştirebilir miyim?

C: Evet, Aspose.Note for Java kullanarak sayfa değişikliklerini içeriğini size göre özelleştirebilirsiniz.

### S5: Aspose.Note for Java desteğini nereden alabilirim?

C: Aspose.Note for Java'yı [Aspose.Note forumundan](https://forum.aspose.com/c/note/28) alabilirsiniz.

---

**Son Güncelleme:** 2026-01-15
**Şunlarla Test Edildi:** Java 24.12 için Aspose.Note
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}