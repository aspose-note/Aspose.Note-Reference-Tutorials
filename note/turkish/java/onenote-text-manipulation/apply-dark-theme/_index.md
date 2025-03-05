---
title: OneNote'ta Metne Koyu Tema Uygulama - Aspose.Note
linktitle: OneNote'ta Metne Koyu Tema Uygulama - Aspose.Note
second_title: Aspose.Note Java API'si
description: Aspose.Note for Java'yı kullanarak OneNote metninize koyu bir tema uygulamanın kolay adımlarını keşfedin. Dijital dokümantasyon deneyiminizi zahmetsizce geliştirin.
type: docs
weight: 11
url: /tr/java/onenote-text-manipulation/apply-dark-theme/
---
## giriiş
Sürekli gelişen dijital belgeleme ortamında, notlarınızın estetiği okunabilirliği ve kullanıcı deneyimini önemli ölçüde etkileyebilir. Dikkate değer yönlerden biri, görsel olarak çekici ve rahat bir ortam sağlayan karanlık bir temanın uygulanmasıdır. Bu eğitimde, Aspose.Note for Java'yı kullanarak OneNote'ta metne karanlık bir tema uygulama sürecinde size rehberlik edeceğiz.
## Önkoşullar
Eğiticiye dalmadan önce aşağıdaki önkoşullara sahip olduğunuzdan emin olun:
-  Aspose.Note for Java: Aspose.Note for Java kütüphanesini şu adresten indirip yükleyin:[Burada](https://releases.aspose.com/note/java/).
- Java Geliştirme Kiti (JDK): Makinenizde Java'nın kurulu olduğundan emin olun.
- Entegre Geliştirme Ortamı (IDE): Sorunsuz geliştirme için Eclipse veya IntelliJ gibi bir IDE seçin.
## Paketleri İçe Aktar
Başlamak için gerekli paketleri Java projenize aktarın:
```java
import com.aspose.note.*;
import java.awt.*;
import java.io.IOException;
import java.nio.file.Paths;
```
## 1. Adım: Sayfa Arka Plan Rengini Ayarlayın
```java
// Belgeler dizininin yolu.
String dataDir = "Your Document Directory";
// Belgeyi Aspose.Note'a yükleyin.
Document doc = new Document(Paths.get(dataDir, "Aspose.one").toString());
for (Page page: doc)
{
    page.setBackgroundColor(Color.BLACK);
}
```
## 2. Adım: Metin Rengini Ayarlayın
```java
for (RichText node: doc.getChildNodes(RichText.class))
{
    Color c = node.getParagraphStyle().getFontColor();
    if (c.getAlpha() <= 10 || Math.abs(c.getRed() - Color.BLACK.getRed()) + Math.abs(c.getGreen() - Color.BLACK.getGreen()) + Math.abs(c.getBlue() - Color.BLACK.getBlue()) <= 30)
    {
        node.getParagraphStyle().setFontColor(Color.WHITE);
    }
}
```
## 3. Adım: Belgeyi Kaydet
```java
doc.save(Paths.get(dataDir, "AsposeDarkTheme.pdf").toString());
```
Bu adımları her belge için tekrarlayın; Aspose.Note for Java'yı kullanarak OneNote metninize başarıyla karanlık bir tema uygulamış olacaksınız.
## Çözüm
Sonuç olarak, Aspose.Note for Java ile dijital notlarınızın görsel çekiciliğini artırmak çok kolay. Bu adım adım kılavuzu izleyerek OneNote'taki metne zahmetsizce karanlık bir tema uygulayabilir ve belgeleme deneyiminizi geliştirebilirsiniz.
## SSS
### Koyu temayı yalnızca belirli bölümlere uygulayabilir miyim?
Evet, koyu temayı belgenizdeki belirli bölümlere seçici olarak uygulamak için kodu değiştirebilirsiniz.
### Aspose.Note for Java'da önceden tanımlanmış karanlık temalar mevcut mu?
Şu an itibariyle Aspose.Note for Java, temaları özelleştirmenize izin veriyor ancak önceden tanımlanmış karanlık temalar yok.
### Aspose.Note for Java diğer belge formatlarını destekliyor mu?
Evet, Aspose.Note for Java; PDF, DOCX ve HTML dahil olmak üzere çeşitli belge formatlarını destekler.
### Aspose.Note for Java'nın deneme sürümü mevcut mu?
 Evet, ücretsiz deneme sürümüne erişebilirsiniz[Burada](https://releases.aspose.com/).
### Aspose.Note for Java'ya nasıl destek alabilirim?
 Ziyaret edin[Aspose.Note forumu](https://forum.aspose.com/c/note/28) topluluk desteği için veya premium destek seçeneklerini keşfedin[Burada](https://purchase.aspose.com/temporary-license/).