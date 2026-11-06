---
date: 2026-11-05
description: Naučte se, jak snížit velikost souboru TIFF při konverzi poznámkových
  bloků OneNote do TIFF v Javě pomocí Aspose.Note. Obsahuje možnosti JPEG, PackBits
  a černobílého TIFF.
keywords:
- reduce tiff file size
- black white tiff
- tiff jpeg compression
- aspose note java
lastmod: 2026-11-05
linktitle: Jak snížit velikost souboru TIFF při konverzi OneNote v Javě
og_description: Naučte se, jak snížit velikost souboru TIFF při konverzi poznámkových
  bloků OneNote do TIFF v Javě pomocí Aspose.Note. Obsahuje možnosti JPEG, PackBits
  a černobílého TIFF.
og_image_alt: Developer guide showing OneNote to TIFF conversion with compression
  options in Java
og_title: Jak snížit velikost souboru TIFF při konverzi OneNote v Javě
schemas:
- author: Aspose
  dateModified: '2026-11-05'
  description: Learn how to reduce TIFF file size when converting OneNote notebooks
    to TIFF in Java using Aspose.Note. Includes JPEG, PackBits and black‑white TIFF
    options.
  headline: How to reduce TIFF file size when converting OneNote in Java
  type: TechArticle
- description: Learn how to reduce TIFF file size when converting OneNote notebooks
    to TIFF in Java using Aspose.Note. Includes JPEG, PackBits and black‑white TIFF
    options.
  name: How to reduce TIFF file size when converting OneNote in Java
  steps:
  - name: Point `dataDir` to the folder containing your `.one` file.
    text: Point `dataDir` to the folder containing your `.one` file.
  - name: Call `SaveToTiffUsingJpegCompression()` from your main method or service.
    text: Call `SaveToTiffUsingJpegCompression()` from your main method or service.
  - name: The resulting `.tiff` file will appear in the same directory.
    text: The resulting `.tiff` file will appear in the same directory.
  type: HowTo
- questions:
  - answer: Yes. While Aspose.Note focuses on OneNote files, Aspose.PDF, Aspose.Words,
      and other libraries provide similar `ImageSaveOptions` for their formats.
    question: Can I convert other document types (e.g., PDF, DOCX) to TIFF with these
      options?
  - answer: The JPEG algorithm is the same, but the image data lives inside a TIFF
      container, which can hold multiple pages and richer metadata.
    question: How does TIFF JPEG compression differ from a standard JPEG file?
  - answer: Absolutely. Iterate over a directory, call any of the three methods for
      each file, and collect the resulting TIFFs.
    question: Is it possible to batch‑process many `.one` files?
  - answer: Yes. Use `options.setResolution(int dpi)` before saving.
    question: Can I control the DPI/resolution of the output TIFF?
  - answer: The API itself is synchronous, but you can wrap calls in Java’s `CompletableFuture`
      or a thread pool for parallel execution.
    question: Does Aspose.Note support asynchronous processing?
  type: FAQPage
second_title: Aspose.Note Java API
tags:
- reduce tiff file size
- aspose.note
- java tiff conversion
- black white tiff
- image compression
title: Jak snížit velikost souboru TIFF při konverzi OneNote v Javě
url: /cs/java/onenote-document-saving/save-to-tiff-image-using-image-save-options/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak snížit velikost souboru TIFF při konverzi OneNote v Javě

## Úvod

V tomto tutoriálu se dozvíte, jak **snížit velikost souboru TIFF** při konverzi poznámkových bloků OneNote na TIFF obrázky pomocí Aspose.Note pro Java. Provedeme vás třemi metodami komprese — TIFF JPEG, PackBits a CCITT Group 3 (černobílý TIFF) — ukážeme, jak upravit kvalitu obrazu, řídit režim barev a udržet velikost souboru optimální pro web, archivaci nebo faxové scénáře.

## Rychlé odpovědi
- **Co je komprese TIFF JPEG?** Ztrátová metoda komprese, která snižuje velikost souboru TIFF při zachování vizuální kvality.  
- **Která knihovna provádí konverzi?** Aspose.Note pro Java.  
- **Potřebuji licenci?** Bezplatná zkušební verze funguje pro testování; licence je vyžadována pro produkční nasazení.  
- **Mohu změnit kvalitu obrazu?** Ano, nastavte vlastnost `quality` na `ImageSaveOptions`.  
- **Je možná hromadná konverze?** Ano – projděte dokumenty ve smyčce a použijte stejné možnosti.

## Přehled komprese TIFF JPEG

Komprese TIFF JPEG ukládá data obrazu v kontejneru TIFF, ale používá ztrátový algoritmus JPEG k zmenšení souboru. Je ideální, když potřebujete rovnováhu mezi **kvalitou TIFF obrazu** a menší velikostí souboru, zejména pro webové nebo archivní scénáře.

## Proč používat různé typy komprese TIFF?

Typ komprese volíte podle obsahu a potřeb úložiště: JPEG je nejlepší pro fotografie, PackBits poskytuje bezztrátovou kompresi pro grafiku s velkými jednotnými oblastmi a CCITT Group 3 nabízí vysoký poměr komprese pro černobílé faxové dokumenty. Výběrem správné metody můžete **snížit velikost souboru TIFF** aniž byste ohrozili vizuální věrnost požadovanou vaší aplikací.

## Výběr správné komprese

- **JPEG** – Nastavitelná kvalita (0‑100) vám umožní vyvážit velikost a detail, ideální pro stránky s bohatými barvami.  
- **PackBits** – Bezztrátové kódování běhu délky; ideální, když musíte zachovat každý pixel přesně.  
- **CCITT Group 3** – Pouze černobílá; maximalizuje kompresi pro naskenovaný text nebo faxové dokumenty.  

## Převod OneNote do TIFF pomocí Aspose.Note

Pokud je vaším cílem **převést OneNote do TIFF**, níže uvedené tři metody pokrývají nejčastější scénáře. Každá metoda načte soubor `.one`, nakonfiguruje `ImageSaveOptions` a uloží výsledek jako soubor `.tiff`.

## Požadavky

- Java Development Kit (JDK) nainstalován.  
- Knihovna Aspose.Note pro Java přidána do vašeho projektu (Maven/Gradle nebo ručně JAR).  
- Základní znalost syntaxe Javy.

## Import balíčků

`ImageSaveOptions`, `TiffCompression` a `ColorMode` třídy jsou jádrem konverzního API.

`ImageSaveOptions` definuje možnosti pro ukládání obrázků, jako je formát a komprese.  
`TiffCompression` vyjmenovává podporované algoritmy komprese TIFF.  
`ColorMode` určuje barevnou hloubku, např. barva nebo černobílá.  

```java
// Placeholder for import statements – keep your imports here
```

```java
import com.aspose.note.*;
import java.io.IOException;
import java.nio.file.Paths;
```

## Krok 1: uložení do TIFF pomocí komprese TIFF JPEG

### Ukládání TIFF s JPEG kompresí v Javě

Načtěte soubor OneNote, nakonfigurujte `ImageSaveOptions` s JPEG kompresí, volitelně nastavte hodnotu `quality` a zavolejte metodu uložení. Tento dvoukrokový vzor vám dává plnou kontrolu nad velikostí výstupu a vizuální věrností.

1. Nastavte `dataDir` na složku obsahující váš soubor `.one`.  
2. Zavolejte `SaveToTiffUsingJpegCompression()` z vaší hlavní metody nebo služby.  
3. Výsledný soubor `.tiff` se objeví ve stejném adresáři.

```java
// Placeholder for the JPEG compression method implementation
```

```java
public static void SaveToTiffUsingJpegCompression() throws IOException {
    // The path to the documents directory.
    String dataDir = "Your Document Directory";

    // Load the document into Aspose.Note.
    Document oneFile = new Document(Paths.get(dataDir, "Aspose.one").toString());

    ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);
    options.setTiffCompression(TiffCompression.Jpeg);
    options.setQuality(93);

    oneFile.save(Paths.get(dataDir,"SaveToTiffUsingJpegCompression.tiff").toString(), options);
}
```

**Vysvětlení**

- `ImageSaveOptions` říká Aspose.Note, aby výstupem byl TIFF soubor.  
- `setTiffCompression(TiffCompression.Jpeg)` vybírá JPEG kompresi.  
- `setQuality(93)` (volitelné) jemně ladí kvalitu obrazu; nižší hodnoty produkují menší soubory.

## Přehled komprese TIFF PackBits

PackBits je bezztrátový kompresní algoritmus, který funguje nejlépe pro obrázky s velkými oblastmi jednolitých barev. V dokumentaci se často označuje jako **tiff packbits compression**.

## Ukládání TIFF s kompresí PackBits v Javě

Pokud potřebujete bezztrátovou možnost, PackBits je jednoduchý algoritmus běhu délky, který dobře funguje pro grafiku s jednolitými barvami. Nakonfigurujte `ImageSaveOptions` s `TiffCompression.PackBits` a uložte dokument.

```java
// Placeholder for the PackBits compression method implementation
```

```java
public static void SaveToTiffUsingPackBitsCompression() throws IOException {
    // The path to the documents directory.
    String dataDir = "Your Document Directory";

    // Load the document into Aspose.Note.
    Document oneFile = new Document(Paths.get(dataDir, "Aspose.one").toString());

    ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);
    options.setTiffCompression(TiffCompression.PackBits);

    oneFile.save(Paths.get(dataDir, "SaveToTiffUsingPackBitsCompression.tiff").toString(), options);
}
```

**Vysvětlení**

- `setTiffCompression(TiffCompression.PackBits)` přepíná metodu komprese.  
- Není potřeba nastavení kvality, protože PackBits je bezztrátový.

## Ukládání TIFF s kompresí CCITT Group 3 v Javě

Pro faxové dokumenty často potřebujete **černobílý TIFF**. CCITT Group 3 poskytuje vysokou kompresi pro monochromatické obrázky. Nastavte režim barev na černobílý a vyberte výčtový typ komprese CCITT 3.

```java
// Placeholder for the CCITT Group 3 compression method implementation
```

```java
public static void SaveToTiffUsingCcitt3Compression() throws IOException {
    // The path to the documents directory.
    String dataDir = "Your Document Directory";

    // Load the document into Aspose.Note.
    Document oneFile = new Document(Paths.get(dataDir, "Aspose.one").toString());

    ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);
    options.setColorMode(ColorMode.BlackAndWhite);
    options.setTiffCompression(TiffCompression.Ccitt3);

    oneFile.save(Paths.get(dataDir, "SaveToTiffUsingCcitt3Compression.tiff").toString(), options);
}
```

**Vysvětlení**

- `setColorMode(ColorMode.BlackAndWhite)` vynutí černobílý výstup.  
- `setTiffCompression(TiffCompression.Ccitt3)` použije faxovou kompresi.

## Časté problémy a tipy

| Problém | Řešení |
|-------|----------|
| **Výstupní soubor je větší, než se očekávalo** | Zkuste snížit hodnotu JPEG `quality` nebo přepněte na PackBits, pokud je bezztrátová komprese přijatelná. |
| **Barvy vypadají vybledlé** | Ujistěte se, že jste neúmyslně nenastavili `ColorMode.BlackAndWhite`, když potřebujete plnou barvu. |
| **Chyba nepodporovaného formátu obrazu** | Ověřte, že používáte aktuální verzi Aspose.Note; starší sestavy mohou postrádat některé výčty komprese. |
| **LicenseException za běhu** | Nainstalujte platnou licenci Aspose.Note (`License license = new License(); license.setLicense("Aspose.Note.Java.lic");`). |

## Často kladené otázky

**Q: Mohu převést i jiné typy dokumentů (např. PDF, DOCX) do TIFF s těmito možnostmi?**  
A: Ano. Zatímco Aspose.Note se zaměřuje na soubory OneNote, Aspose.PDF, Aspose.Words a další knihovny poskytují podobné `ImageSaveOptions` pro jejich formáty.

**Q: Jak se komprese TIFF JPEG liší od standardního JPEG souboru?**  
A: Algoritmus JPEG je stejný, ale data obrazu jsou uložena v kontejneru TIFF, který může obsahovat více stránek a bohatší metadata.

**Q: Je možné hromadně zpracovat mnoho souborů `.one`?**  
A: Rozhodně. Procházejte adresář, zavolejte kteroukoliv ze tří metod pro každý soubor a shromážděte výsledné TIFF soubory.

**Q: Mohu řídit DPI/rozlišení výstupního TIFF?**  
A: Ano. Použijte `options.setResolution(int dpi)` před uložením.

**Q: Podporuje Aspose.Note asynchronní zpracování?**  
A: API samo je synchronní, ale můžete volání zabalit do Java `CompletableFuture` nebo thread poolu pro paralelní provedení.

## Závěr

Nyní máte kompletní **Java nástroj pro konverzi TIFF**, který vám umožní **snížit velikost souboru TIFF** při ukládání dokumentů OneNote jako TIFF soubory pomocí JPEG, PackBits nebo CCITT Group 3 faxové komprese. Přizpůsobte kvalitu, režim barev a rozlišení podle vašich konkrétních požadavků a integrujte tyto metody do hromadných pracovních postupů pro maximální produktivitu.

---

**Poslední aktualizace:** 2026-11-05  
**Testováno s:** Aspose.Note for Java 26.4 (latest at time of writing)  
**Autor:** Aspose

## Související tutoriály

- [Jak vykreslit obrázek stránky OneNote (JPEG) pomocí Save Format s Aspose.Note pro Java](/note/java/onenote-document-saving/save-to-jpeg-image-using-save-format/)
- [Použít Aspose.Note pro Java k uložení OneNote jako PNG s možnostmi – převod poznámkového bloku na obrázek](/note/java/onenote-notebook-operations/convert-notebook-to-image-with-options/)
- [Jak exportovat OneNote jako odstíny šedi – Aspose.Note](/note/java/onenote-document-saving/save-to-grayscale-image/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}