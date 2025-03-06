---
title: OneNote'ta Sayfa Düzeltmeleriyle Çalışma - Aspose.Note
linktitle: OneNote'ta Sayfa Düzeltmeleriyle Çalışma - Aspose.Note
second_title: Aspose.Note Java API'si
description: Aspose.Note for Java'yı kullanarak OneNote belgelerindeki sayfa revizyonlarını nasıl yöneteceğinizi öğrenin. Etkili revizyon takibi ve işbirliği için adım adım kılavuz sağlar.
weight: 21
url: /tr/java/onenote-page-manipulation/working-with-page-revisions/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote'ta Sayfa Düzeltmeleriyle Çalışma - Aspose.Note

## giriiş

OneNote, notları düzenlemek ve yönetmek için güçlü bir araçtır ancak bazen değişiklikleri izlemek ve etkili bir şekilde işbirliği yapmak için düzeltmeler üzerinde çalışmanız gerekir. Aspose.Note for Java ile OneNote belgelerindeki sayfa revizyonlarını programlı olarak kolayca yönetebilirsiniz. Bu eğitim size süreç boyunca adım adım rehberlik edecektir.

## Önkoşullar

Başlamadan önce aşağıdakilere sahip olduğunuzdan emin olun:

### Java Geliştirme Ortamı

Sisteminizde Java Development Kit'in (JDK) kurulu olduğundan emin olun.

### Java Kütüphanesi için Aspose.Note

Aspose.Note for Java kütüphanesini şu adresten indirip yükleyin:[Burada](https://releases.aspose.com/note/java/).

### OneNote Belgesi

Test amacıyla örnek bir OneNote belgesini hazır bulundurun.

## Paketleri İçe Aktar

Java projenizde Aspose.Note for Java ile çalışmak için gerekli paketleri içe aktarın.

```java
import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.RevisionSummary;
import java.io.IOException;
import java.util.Calendar;
```

Daha net bir anlayış için verilen örneği birden çok adıma ayıralım.

## 1. Adım: OneNote Belgesini Yükleyin

Öncelikle OneNote belgesini yükleyin ve ilk alt sayfayı alın.

```java
String dataDir = "Your Document Directory";
Document document = new Document(dataDir + "Sample1.one");
Page page = document.getFirstChild();
```

## Adım 2: Sayfa Revizyon Özetini Okuyun

Sayfanın içerik revizyon özetini okuyun.

```java
RevisionSummary pageRevisionInfo = page.getPageContentRevisionSummary();
System.out.println(String.format("Author:\t%s\nModified:\t%s",
        pageRevisionInfo.getAuthorMostRecent(),
        pageRevisionInfo.getLastModifiedTime().toString()));
```

## 3. Adım: Sayfa Revizyon Özetini Güncelleyin

Sayfa revizyon özetini yeni yazar ve değiştirilme tarihi ile güncelleyin.

```java
pageRevisionInfo.setAuthorMostRecent("New Author");
Calendar modifiedDate = Calendar.getInstance();
pageRevisionInfo.setLastModifiedTime(modifiedDate.getTime());
document.save(dataDir + "WorkingWithPageRevisions_out.one");
```

## Çözüm

OneNote belgelerindeki sayfa revizyonlarını programlı olarak yönetmek Aspose.Note for Java ile basitleştirilebilir. Bu öğreticide özetlenen adımları izleyerek, değişiklikleri izlemek ve sorunsuz bir şekilde işbirliği yapmak için sayfa revizyonlarıyla etkili bir şekilde çalışabilirsiniz.

## SSS'ler

### S1: Aspose.Note for Java'yı diğer Java kütüphaneleriyle birlikte kullanabilir miyim?

C: Evet, Aspose.Note for Java, işlevselliği geliştirmek için diğer Java kitaplıklarıyla entegre edilebilir.

### S2: Aspose.Note for Java, OneNote belgelerinin tüm sürümlerini destekliyor mu?

C: Aspose.Note for Java, eski sürümler de dahil olmak üzere OneNote belgelerinin çeşitli sürümlerini destekler.

### S3: Aspose.Note for Java, kurumsal düzeydeki uygulamalar için uygun mudur?

C: Kesinlikle, Aspose.Note for Java, güçlü özellikler ve ölçeklenebilirlik ile kurumsal düzeydeki uygulamaların ihtiyaçlarını karşılamak üzere tasarlanmıştır.

### S4: Aspose.Note for Java ile sayfa revizyonlarını özelleştirebilir miyim?

C: Evet, Aspose.Note for Java'yı kullanarak sayfa revizyonlarını gereksinimlerinize göre özelleştirebilirsiniz.

### S5: Aspose.Note for Java desteğini nereden alabilirim?

 C: Java için Aspose.Note desteğini şu adresten alabilirsiniz:[Aspose.Note forumu](https://forum.aspose.com/c/note/28).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
