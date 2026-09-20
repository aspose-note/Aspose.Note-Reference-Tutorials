---
date: 2026-06-30
description: Zjistěte, jak exportovat OneNote uložením dokumentu jako odstínově šedý
  PNG obrázek pomocí Aspose.Note pro Java. Obsahuje kroky k načtení dokumentu OneNote
  a vytvoření odstínově šedého obrázku.
keywords:
- how to export onenote
- adjust image resolution
- reduce onenote size
- create grayscale png
- grayscale conversion java
linktitle: Jak exportovat OneNote jako odstínově šedý obrázek – Aspose.Note
schemas:
- author: Aspose
  dateModified: '2026-06-30'
  description: Learn how to export onenote by saving a document as a grayscale PNG
    image using Aspose.Note for Java. Includes steps to load onenote document and
    create grayscale image.
  headline: How to Export OneNote as Grayscale Image – Aspose.Note
  type: TechArticle
- description: Learn how to export onenote by saving a document as a grayscale PNG
    image using Aspose.Note for Java. Includes steps to load onenote document and
    create grayscale image.
  name: How to Export OneNote as Grayscale Image – Aspose.Note
  steps:
  - name: Java Development Kit (JDK) 8 or newer installed.
    text: Java Development Kit (JDK) 8 or newer installed.
  - name: Aspose.Note for Java library – download the latest release from [here](https://releases.aspose.com/note/java/).
    text: Aspose.Note for Java library – download the latest release from [here](https://releases.aspose.com/note/java/).
  - name: A basic understanding of Java syntax and Maven/Gradle project setup.
    text: A basic understanding of Java syntax and Maven/Gradle project setup.
  type: HowTo
- questions:
  - answer: It refers to programmatically converting a OneNote file into another format,
      such as an image, using code.
    question: What does “how to export onenote” mean?
  - answer: PNG works well because it preserves loss‑less quality and supports a dedicated
      grayscale color mode.
    question: Which format is best for grayscale output?
  - answer: A valid Aspose.Note license is required for production use; a temporary
      trial license is available for testing.
    question: Do I need a license?
  - answer: Java 8 or higher is recommended.
    question: What Java version is required?
  - answer: Yes, you can adjust the `ImageSaveOptions` properties like `Resolution`
      or `PageSize` before saving.
    question: Can I change the image size?
  type: FAQPage
second_title: Aspose.Note Java API
title: Jak exportovat OneNote jako odstínově šedý obrázek – Aspose.Note
url: /cs/java/onenote-document-saving/save-to-grayscale-image/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Uložení do černobílého obrázku v OneNote - Aspose.Note

## Úvod

V tomto tutoriálu objevíte **jak exportovat onenote** převodem souboru OneNote `.one` na vysoce kvalitní černobílý PNG obrázek pomocí Aspose.Note pro Java. Převod do odstínů šedi vývojáři Java často potřebují pro tisk, archivaci nebo **zmenšení velikosti OneNote** bez ztráty důležitého obsahu. Provedeme vás načtením dokumentu OneNote, nastavením možností uložení – včetně **úpravy rozlišení obrázku** – a nakonec uložením dokumentu jako PNG.

## Rychlé odpovědi
- **Co znamená “how to export onenote”?** Odkazuje na programatické převádění souboru OneNote do jiného formátu, například obrázku, pomocí kódu.  
- **Který formát je nejlepší pro výstup v odstínech šedi?** PNG funguje dobře, protože zachovává bezztrátovou kvalitu a podporuje speciální režim černobílých barev.  
- **Potřebuji licenci?** Platná licence Aspose.Note je vyžadována pro produkční použití; dočasná zkušební licence je k dispozici pro testování.  
- **Jaká verze Javy je požadována?** Java 8 nebo vyšší se doporučuje.  
- **Mohu změnit velikost obrázku?** Ano, můžete upravit vlastnosti `ImageSaveOptions`, jako jsou `Resolution` nebo `PageSize`, před uložením.

## Co je “how to export onenote”?

Exportování OneNote znamená programatické převádění souboru OneNote `.one` do jiné reprezentace – například PDF, HTML nebo obrázku. V tomto průvodci se zaměřujeme na **vytváření černobílých PNG** obrázků, což je častý požadavek pro dokumentaci nebo workflow připravené k tisku. Pomocí Aspose.Note probíhá převod kompletně v paměti, takže nikdy nepotřebujete mít Microsoft OneNote nainstalovaný na serveru.

## Proč exportovat OneNote jako černobílý obrázek?

Černobílé PNG jsou obvykle **o 30‑40 % menší** než jejich plnobarevné protějšky, což urychluje doručování na web a snižuje náklady na úložiště. Také poskytují **ostřejší kontrast** na laserových tiskárnách, což usnadňuje čtení zpráv. Protože PNG je univerzálně podporováno, výsledné soubory fungují v prohlížečích, mobilních zařízeních i desktopových editorech bez dalších kodeků.

## Předpoklady

1. Nainstalovaný Java Development Kit (JDK) 8 nebo novější.  
2. Knihovna Aspose.Note pro Java – stáhněte nejnovější verzi z [zde](https://releases.aspose.com/note/java/).  
3. Základní znalost syntaxe Javy a nastavení projektu Maven/Gradle.  

## Import balíčků

Třída `ImageSaveOptions` řídí, jak je dokument vykreslen do obrázku.  
`ColorMode` je výčet, který vám umožňuje přepínat mezi plnobarevným a černobílým výstupem.

```java
import com.aspose.note.ColorMode;
import com.aspose.note.Document;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.SaveFormat;
import java.io.IOException;
```

## Krok 1: Načtení dokumentu OneNote

`Document` představuje sešit OneNote a poskytuje metody pro načtení, úpravu a uložení jeho obsahu. Nejprve **načtěte dokument OneNote** do Aspose.Note. Nahraďte `"Your Document Directory"` cestou k vaší místní složce a `"Aspose.one"` názvem vašeho souboru OneNote.

```java
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Aspose.one");
```

## Krok 2: Nastavení výstupní cesty a možností

`ImageSaveOptions` konfiguruje, jak je dokument OneNote vykreslen do souboru obrázku. Výčet `ColorMode` vybírá režim vykreslování barev, například černobílý nebo plnobarevný. Definujte výstupní cestu pro černobílý obrázek a specifikujte možnosti uložení. Nastavíme `ColorMode` na `GrayScale` a použijeme formát **uložit dokument jako PNG**. Můžete také **upravit rozlišení obrázku** na 300 DPI pro vysoce kvalitní tisk.

```java
dataDir = dataDir + "SaveAsGrayscaleImage_out.png";
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);
options.setColorMode(ColorMode.GrayScale);
```

## Krok 3: Uložení dokumentu

Nakonec uložte dokument jako černobílý PNG obrázek pomocí nakonfigurovaných možností. Metoda `save` zapíše soubor na disk, aniž by vyžadovala jakékoli mezilehlé dočasné soubory.

```java
oneFile.save(dataDir, options);
```

## Časté problémy a řešení
- **FileNotFoundException** – Ověřte, že `dataDir` ukazuje na správnou složku a že soubor `.one` existuje.  
- **LicenseException** – Ujistěte se, že jste před voláním `save` použili platnou licenci Aspose.Note.  
- **Low‑resolution output** – Upravit `options.setResolution(300)`, aby se zvýšilo DPI; vyšší DPI poskytuje ostřejší tisk, ale větší velikost souboru.  

## Často kladené otázky

**Q1: Mohu uložit černobílý obrázek v jiném formátu?**  
A1: Ano, stačí změnit parametr `SaveFormat` v konstruktoru `ImageSaveOptions` na `Jpeg`, `Bmp` nebo kterýkoli z více než 20 podporovaných formátů obrázků.

**Q2: Je Aspose.Note kompatibilní se všemi verzemi dokumentů OneNote?**  
A2: Aspose.Note podporuje Microsoft OneNote 2010 a novější, což pokrývá více než 95 % sešitů v aktivním používání dnes.

**Q3: Vyžaduje Aspose.Note licenci k použití?**  
A3: Platná licence je vyžadována pro produkční použití, ale dočasná zkušební licence může být získána pro hodnocení zdarma.

**Q4: Mohu upravit jiné aspekty dokumentu před jeho uložením jako obrázek?**  
A4: Rozhodně! Aspose.Note poskytuje API pro úpravu sekcí, stránek a jednotlivých prvků, jako jsou text, tabulky a obrázky, před exportem.

**Q5: Kde mohu najít podporu, pokud narazím na problémy?**  
A5: Podporu můžete najít na fóru Aspose.Note [zde](https://forum.aspose.com/c/note/28).

## Závěr

Nyní jste se naučili **jak exportovat onenote** načtením souboru OneNote, nastavením možností uložení pro **vytvoření černobílého obrázku** a **uložením dokumentu jako PNG**. Tento přístup je ideální pro generování lehkých, připravených k tisku vizuálů ze sešitů OneNote. Neváhejte experimentovat s dalšími nastaveními `ColorMode`, vyššími hodnotami DPI nebo alternativními formáty obrázků, aby vyhovovaly požadavkům vašeho projektu.

---

**Poslední aktualizace:** 2026-06-30  
**Testováno s:** Aspose.Note 27.0 for Java  
**Autor:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Související tutoriály

- [Exportovat stránku OneNote do PNG obrázku v Javě pomocí Aspose.Note](/note/java/onenote-document-loading/convert-page-to-png-image/)
- [aspnote nastavit rozlišení jpeg – Nastavit výstupní rozlišení obrázku v OneNote - Aspose.Note](/note/java/onenote-document-saving/set-output-image-resolution/)
- [Jak uložit OneNote jako PDF s Aspose.Note pro Java](/note/java/onenote-document-loading/load-save-format/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}