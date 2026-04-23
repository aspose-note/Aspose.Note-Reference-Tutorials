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

## Introduction

OneNote, notları düzenlemek için güçlü bir araçtır ve **track changes onenote** gerektiğinde, sayfa revizyonlarını yönetmek etkili iş birliği için hayati önem taşır. Aspose.Note for Java ile revizyonları programlı olarak ele alabilir, bir sayfayı kim düzenlediğini görebilir ve hatta zaman damgalarını ayarlayabilirsiniz. Bu öğretici, bir belgeyi yüklemekten revizyon özetini güncellemeye kadar her adımı size gösterir.

## Quick Answers
- **track changes onenote ne anlama geliyor?** Bu, bir OneNote sayfasını kimin ne zaman düzenlediğini izlemeyi ifade eder.
- **Hangi kütüphane gereklidir?** Aspose.Note for Java.
- **Bir revizyonun yazarını veya tarihini değiştirebilir miyim?** Evet, RevisionSummary API'si (`modify revision date`) kullanılarak.
- **Önceden bir OneNote dosyasına ihtiyacım var mı?** Evet, bir örnek `.one` dosyası gereklidir.
- **Üretim için lisans gerekli mi?** Ticari kullanım için geçerli bir Aspose.Note lisansı gereklidir.

## Revizyon özeti örneği nedir?

*revision summary* bir sayfadaki en son değişiklikler hakkında meta veriler sağlar—yazar adı, son değiştirilme zamanı ve diğer detaylar. Bu rehberde bu bilgileri alıp görüntüleyecek, ardından **modify revision date** nasıl yapılacağını göstereceğiz.

## Why track changes onenote with Aspose.Note?

- **Collaboration:** En son düzenlemeleri kimin yaptığını hızlıca görebilirsiniz.
- **Auditing:** Uyumluluk için değişikliklerin güvenilir bir geçmişini tutun.
- **Automation:** Revizyon yönetimini back‑end hizmetlerine veya taşıma araçlarına entegre edin.

## Prerequisites

### Java Development Environment
Sisteminize Java Development Kit (JDK) kurulu olduğundan emin olun.

### Aspose.Note for Java Library
Aspose.Note for Java kütüphanesini [buradan](https://releases.aspose.com/note/java/) indirip kurun.

### OneNote Document
Test amaçlı bir örnek OneNote belgesine sahip olun.

## Import Packages
Java projenizde Aspose.Note for Java ile çalışmak için gerekli paketleri içe aktarın.

```java
import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.RevisionSummary;
import java.io.IOException;
import java.util.Calendar;
```

Sağlanan örneği daha net anlamak için birden fazla adıma ayıralım.

## Step 1: Load OneNote Document

Adım 1: OneNote Belgesini Yükle

İlk olarak, OneNote belgesini yükleyin ve ilk alt sayfayı alın.

```java
String dataDir = "Your Document Directory";
Document document = new Document(dataDir + "Sample1.one");
Page page = document.getFirstChild();
```

## Step 2: Read Page Revision Summary

Adım 2: Sayfa Revizyon Özeti Okuma

Sayfa için içerik revizyon özetini okuyun. Bu, sayfayı en son kimin düzenlediğini gösteren **revision summary example**'dır.

```java
RevisionSummary pageRevisionInfo = page.getPageContentRevisionSummary();
System.out.println(String.format("Author:\t%s\nModified:\t%s",
        pageRevisionInfo.getAuthorMostRecent(),
        pageRevisionInfo.getLastModifiedTime().toString()));
```

## Step 3: Update Page Revision Summary

Adım 3: Sayfa Revizyon Özetini Güncelleme

Sayfa revizyon özetini yeni bir yazar ve yeni bir değiştirilme tarihiyle güncelleyin. Bu, **modify revision date**'i programlı olarak nasıl yapacağınızı gösterir.

```java
pageRevisionInfo.setAuthorMostRecent("New Author");
Calendar modifiedDate = Calendar.getInstance();
pageRevisionInfo.setLastModifiedTime(modifiedDate.getTime());
document.save(dataDir + "WorkingWithPageRevisions_out.one");
```

## Conclusion

OneNote belgelerindeki sayfa revizyonlarını programlı olarak yönetmek, Aspose.Note for Java ile basitleştirilebilir. Bu öğreticideki adımları izleyerek **track changes onenote**'u etkili bir şekilde yapabilir, revizyon detaylarını görebilir ve hatta iş akışınıza uyacak şekilde **modify revision date**'i değiştirebilirsiniz.

## FAQ's

### Q1: Aspose.Note for Java'yi diğer Java kütüphaneleriyle birlikte kullanabilir miyim?

A: Evet, Aspose.Note for Java, işlevselliği artırmak için diğer Java kütüphaneleriyle entegre edilebilir.

### Q2: Aspose.Note for Java tüm OneNote belge sürümlerini destekliyor mu?

A: Aspose.Note for Java, eski sürümler dahil olmak üzere çeşitli OneNote belge sürümlerini destekler.

### Q3: Aspose.Note for Java kurumsal seviyedeki uygulamalar için uygun mu?

A: Kesinlikle, Aspose.Note for Java, güçlü özellikleri ve ölçeklenebilirliğiyle kurumsal seviyedeki uygulamaların ihtiyaçlarını karşılayacak şekilde tasarlanmıştır.

### Q4: Aspose.Note for Java ile sayfa revizyonlarını özelleştirebilir miyim?

A: Evet, Aspose.Note for Java kullanarak sayfa revizyonlarını gereksinimlerinize göre özelleştirebilirsiniz.

### Q5: Aspose.Note for Java için desteği nereden alabilirim?

A: Aspose.Note for Java desteğini [Aspose.Note forumundan](https://forum.aspose.com/c/note/28) alabilirsiniz.

---

**Last Updated:** 2026-01-15  
**Tested With:** Aspose.Note for Java 24.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}