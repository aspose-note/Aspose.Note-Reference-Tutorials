---
date: 2026-03-14
description: Naučte se, jak v Javě ukládat dokumenty OneNote jako soubory TIFF pomocí
  komprese TIFF JPEG, komprese TIFF PackBits nebo CCITT Group 3 Fax. Ovládejte kvalitu
  obrazu, velikost souboru a barevný režim pomocí Aspose.Note.
linktitle: Save to TIFF Image Using TIFF JPEG Compression in OneNote
second_title: Aspose.Note Java API
title: Uložit do TIFF obrázku pomocí TIFF JPEG komprese v OneNote
url: /cs/java/onenote-document-saving/save-to-tiff-image-using-image-save-options/
weight: 21
---

 unchanged. Ensure we didn't translate any URLs (none). Ensure we kept markdown formatting.

Now produce final answer.{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Uložení obrázku TIFF pomocí komprese TIFF JPEG v OneNote

## Úvod

V tomto tutoriálu objevíte **jak uložit dokument OneNote do souboru TIFF pomocí komprese TIFF JPEG** a dva další populární kompresní metody. Provedeme vás potřebným nastavením, importem nezbytných Java balíčků a poskytneme jasný krok‑za‑krokem kód pro každou možnost komprese. Na konci budete schopni řídit **kvalitu obrázku TIFF**, snížit velikost souboru a dokonce vytvořit černobílé TIFF soubory pro fax‑styl výstup.

## Rychlé odpovědi
- **Co je komprese TIFF JPEG?** Metoda ztrátové komprese, která snižuje velikost souboru TIFF při zachování vizuální kvality.  
- **Která knihovna provádí konverzi?** Aspose.Note for Java.  
- **Potřebuji licenci?** Bezplatná zkušební verze funguje pro testování; licence je vyžadována pro produkci.  
- **Mohu změnit kvalitu obrázku?** Ano, nastavte vlastnost `quality` na `ImageSaveOptions`.  
- **Je možná hromadná konverze?** Rozhodně – projděte dokumenty ve smyčce a použijte stejné možnosti.

## Co je komprese TIFF JPEG?

Komprese TIFF JPEG ukládá obrazová data v kontejneru TIFF, ale používá ztrátový algoritmus JPEG k zmenšení souboru. Je ideální, když potřebujete rovnováhu mezi **kvalitou obrázku TIFF** a menší velikostí souboru, zejména pro webové nebo archivní scénáře.

## Proč používat různé typy komprese TIFF?
- **JPEG** – Vhodné pro fotografie; nabízí nastavitelnou kvalitu.  
- **PackBits** – Jednoduché, bezztrátové kódování běhové délky; užitečné pro grafiku s velkými jednotnými oblastmi.  
- **CCITT Group 3 Fax** – Pouze černobílé; ideální pro skenované dokumenty a faxové přenosy.  

Výběrem správné komprese můžete splnit požadavky na úložiště, aniž byste obětovali vizuální věrnost potřebnou pro vaši aplikaci.

## Převod One na TIFF pomocí Aspose.Note
Pokud je vaším cílem **převést OneNote na TIFF**, níže uvedené tři metody pokrývají nejčastější scénáře. Každá metoda načte soubor `.one`, nakonfiguruje `ImageSaveOptions` a uloží výsledek jako soubor `.tiff`.

## Požadavky

- Nainstalovaný Java Development Kit (JDK).  
- Knihovna Aspose.Note pro Java přidána do vašeho projektu (Maven/Gradle nebo ruční JAR).  
- Základní znalost syntaxe Java.

## Import balíčků

First, bring the necessary Aspose.Note classes into your Java file:

```java
import com.aspose.note.*;
import java.io.IOException;
import java.nio.file.Paths;
```

## Krok 1: Uložení do TIFF pomocí komprese TIFF JPEG

Níže je kompletní metoda, která načte soubor OneNote a uloží jej jako TIFF s JPEG kompresí. Nastavte hodnotu `quality` (0‑100) pro řízení **kvality obrázku TIFF**.

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

- `ImageSaveOptions` říká Aspose.Note, aby výstupem byl soubor TIFF.  
- `setTiffCompression(TiffCompression.Jpeg)` vybírá JPEG kompresi.  
- `setQuality(93)` (volitelné) jemně ladí kvalitu obrázku; nižší hodnoty produkují menší soubory.

### Jak uložit TIFF s JPEG kompresí v Javě
1. Nastavte `dataDir` na složku obsahující váš soubor `.one`.  
2. Zavolejte `SaveToTiffUsingJpegCompression()` z vaší hlavní metody nebo služby.  
3. Výsledný soubor `.tiff` se objeví ve stejném adresáři.

## Přehled komprese TIFF PackBits

PackBits je bezztrátový kompresní algoritmus, který funguje nejlépe pro obrázky s velkými oblastmi jednolitých barev. V dokumentaci se často označuje jako **tiff packbits compression**.

## Krok 2: Uložení do TIFF pomocí komprese PackBits

Pokud potřebujete bezztrátovou možnost, PackBits je jednoduchý algoritmus běhové délky, který funguje dobře pro grafiku s jednolitými barvami.

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
- Nastavení kvality není potřeba, protože PackBits je bezztrátový.

## Krok 3: Uložení do TIFF pomocí komprese CCITT Group 3 Fax (černobílý TIFF)

Pro dokumenty ve stylu faxu často potřebujete **černobílý TIFF**. CCITT Group 3 poskytuje vysokou kompresi pro monochromatické obrázky.

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

- `setColorMode(ColorMode.BlackAndWhite)` vynutí monochromatický výstup.  
- `setTiffCompression(TiffCompression.Ccitt3)` aplikuje fax‑orientovanou kompresi.

## Časté problémy a tipy

| Problém | Řešení |
|-------|----------|
| **Výstupní soubor je větší, než se očekávalo** | Zkuste snížit hodnotu JPEG `quality` nebo přepněte na PackBits, pokud je bezztrátová komprese přijatelna. |
| **Barvy vypadají vybledlé** | Ujistěte se, že jste neúmyslně nenastavili `ColorMode.BlackAndWhite`, když potřebujete plnou barvu. |
| **Chyba nepodporovaného formátu obrázku** | Ověřte, že používáte aktuální verzi Aspose.Note; starší verze mohou postrádat některé kompresní výčty. |
| **LicenseException za běhu** | Nainstalujte platnou licenci Aspose.Note (`License license = new License(); license.setLicense("Aspose.Note.Java.lic");`). |

## Často kladené otázky

**Q: Mohu převádět i jiné typy dokumentů (např. PDF, DOCX) na TIFF s těmito možnostmi?**  
A: Ano. Zatímco Aspose.Note se zaměřuje na soubory OneNote, Aspose.PDF, Aspose.Words a další knihovny poskytují podobné `ImageSaveOptions` pro jejich formáty.

**Q: Jak se komprese TIFF JPEG liší od standardního JPEG souboru?**  
A: Algoritmus JPEG je stejný, ale obrazová data jsou uložena uvnitř kontejneru TIFF, který může obsahovat více stránek a bohatší metadata.

**Q: Je možné hromadně zpracovat mnoho souborů `.one`?**  
A: Rozhodně. Procházejte adresář, zavolejte kteroukoliv ze tří metod pro každý soubor a shromážděte výsledné TIFFy.

**Q: Mohu řídit DPI/rozlišení výstupního TIFF?**  
A: Ano. Použijte `options.setResolution(int dpi)` před uložením.

**Q: Podporuje Aspose.Note asynchronní zpracování?**  
A: API je samotné synchronní, ale můžete volání zabalit do Java `CompletableFuture` nebo thread poolu pro paralelní provedení.

## Závěr

Nyní máte kompletní **java tiff conversion** sadu nástrojů, která vám umožní ukládat dokumenty OneNote jako soubory TIFF pomocí komprese JPEG, PackBits nebo CCITT Group 3 Fax. Nastavte kvalitu, režim barev a rozlišení tak, aby vyhovovaly vašim konkrétním požadavkům na **kvalitu obrázku TIFF**, a integrujte tyto metody do hromadných pracovních postupů pro maximální produktivitu.

---

**Poslední aktualizace:** 2026-03-14  
**Testováno s:** Aspose.Note for Java 23.12 (latest at time of writing)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}