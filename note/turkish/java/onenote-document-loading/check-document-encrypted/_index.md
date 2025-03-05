---
title: OneNote Belgesinin Şifreli olup olmadığını kontrol etme - Java
linktitle: OneNote Belgesinin Şifreli olup olmadığını kontrol etme - Java
second_title: Aspose.Note Java API'si
description: Aspose.Note kullanarak bir OneNote belgesinin Java'da şifrelenip şifrelenmediğini nasıl kontrol edeceğinizi öğrenin. Verimli belge işleme için adım adım kılavuzumuzu izleyin.
type: docs
weight: 10
url: /tr/java/onenote-document-loading/check-document-encrypted/
---
## giriiş

Java'da OneNote belgeleriyle çalışırken belgenin işlenmeden önce şifrelenmediğinden emin olmak çok önemlidir. Belgelerin şifrelenmesi ekstra bir güvenlik katmanı ekleyebilir ancak doğru şekilde işlenmezse işlem adımlarını da karmaşık hale getirebilir. Bu eğitimde, bir OneNote belgesinin Aspose.Note for Java kullanılarak şifrelenip şifrelenmediğini kontrol etme sürecinde size rehberlik edeceğiz.

## Önkoşullar

Başlamadan önce aşağıdaki önkoşulların mevcut olduğundan emin olun:

1.  Java Geliştirme Kiti (JDK): Sisteminizde Java'nın kurulu olduğundan emin olun. Şuradan indirebilirsiniz[Burada](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).

2.  Aspose.Note for Java Kütüphanesi: Aspose.Note for Java kütüphanesini indirin ve kurun. İndirme linkini bulabilirsiniz[Burada](https://releases.aspose.com/note/java/).

## Paketleri İçe Aktar

Başlamak için gerekli paketleri Java projenize aktarın:

```java
import com.aspose.note.Document;
import com.aspose.note.LoadOptions;
import java.io.FileInputStream;
import java.io.IOException;
import java.nio.file.Paths;
```

Süreci birden fazla adıma ayıralım:

## 1. Adım: Akıştaki Belgenin Şifreli olup olmadığını kontrol edin

```java
public static void CheckIfDocumentFromStreamIsEncrypted() throws IOException {
    // ExStart:CheckIfDocumentFromStreamIsEncrypted
    String dataDir = "Your Document Directory";

    LoadOptions loadOptions = new LoadOptions();
    loadOptions.setDocumentPassword("password");

    FileInputStream stream = new FileInputStream(Paths.get(dataDir, "Sample1.one").toString());

    try {
        Document ref[] = { null };
        if (!Document.isEncrypted(stream, loadOptions, ref)) {
            System.out.println("The document is loaded and ready to be processed.");
        } else {
            System.out.println("The document is encrypted. Provide a password.");
        }
    } finally {
        stream.close();
    }
    // ExEnd:CheckIfDocumentFromStreamIsEncrypted
}
```

Açıklama:

- Bu yöntem, bir akıştan yüklenen bir belgenin şifrelenip şifrelenmediğini kontrol eder.
-  Kullanarak belge şifresini ayarlar.`setDocumentPassword` yöntemi`LoadOptions` sınıf.
- `Document.isEncrypted` Belgenin şifrelenip şifrelenmediğini belirlemek için kullanılan yöntem.

## Adım 2: Dosyadaki Belgenin Şifreli olup olmadığını kontrol edin

```java
public static void CheckIfDocumentFromFileIsEncrypted() throws IOException {
    // ExStart:CheckIfDocumentFromFileIsEncrypted
    String dataDir = "Your Document Directory";

    Document ref[] = { null };
    if (!Document.isEncrypted(Paths.get(dataDir, "Sample1.one").toString(), "VerySecretPassword", ref)) {
        if (ref[0] != null) {
            System.out.println("The document is decrypted. It is loaded and ready to be processed.");
        } else {
            System.out.println("The document is encrypted. Invalid password was provided.");
        }
    } else {
        System.out.println("The document is NOT encrypted. It is loaded and ready to be processed.");
    }
    // ExEnd:CheckIfDocumentFromFileIsEncrypted
}
```

Açıklama:

- Bu yöntem, bir dosyadan yüklenen belgenin şifrelenip şifrelenmediğini kontrol eder.
-  Şunu kullanır:`Document.isEncrypted` önceki adıma benzer ancak bir dosya yolu ve parola parametresi içeren bir yöntem.

## Çözüm

Bu eğitimde, Aspose.Note kullanarak bir OneNote belgesinin Java'da şifrelenip şifrelenmediğini nasıl kontrol edeceğimizi öğrendik. Adım adım kılavuzu takip ederek ve verilen kod örneklerinden yararlanarak belgelerinizin şifreleme durumunu etkin bir şekilde belirleyebilir, Java uygulamalarınızda sorunsuz işlem yapılmasını sağlayabilirsiniz.

## SSS'ler

### S1: Şifreleme durumunu şifre girmeden kontrol edebilir miyim?

Cevap1: Evet, şifre girmeden şifreleme durumunu kontrol edebilirsiniz.`Document.isEncrypted` yöntemi bunu yapmanızı sağlar.

### S2: Yanlış şifre girersem ne olur?

 Cevap2: Şifreleme durumunu kontrol ederken yanlış bir şifre girerseniz, yöntem geri dönecektir.`true`, belgenin şifrelendiğini ancak sağlanan parolanın yanlış olduğunu belirtir.

### S3: Şifrelenmiş bir belgenin şifresini programlı olarak çözmek mümkün müdür?

C3: Evet, belge yükleme sırasında doğru parolayı sağlayarak şifrelenmiş bir belgenin şifresini programlı olarak çözebilirsiniz.

### S4: Aspose.Note'u OneNote'un yanı sıra diğer belge formatları için de kullanabilir miyim?

Cevap4: Hayır, Aspose.Note yalnızca OneNote belgeleriyle çalışmak üzere özel olarak tasarlanmıştır.

### S5: Aspose.Note for Java için daha fazla kaynağı ve desteği nerede bulabilirim?

 A5: ziyaret edebilirsiniz[Aspose.Note forumu](https://forum.aspose.com/c/note/28) topluluk desteği ve dokümantasyon için.