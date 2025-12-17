---
date: 2025-12-17
description: Naučte se, jak v Javě ukládat dokumenty OneNote jako soubory TIFF pomocí
  komprese TIFF JPEG, PackBits nebo CCITT Group 3 Fax. Ovládejte kvalitu obrazu, velikost
  souboru a režim barev pomocí Aspose.Note.
linktitle: Save to TIFF Image Using TIFF JPEG Compression in OneNote
second_title: Aspose.Note Java API
title: Uložit do TIFF obrázku pomocí komprese TIFF JPEG v OneNote
url: /cs/java/onenote-document-saving/save-to-tiff-image-using-image-save-options/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Uložení obrázku TIFF pomocí komprese TIFF JPEG v OneNote

## Úvod

V tomto tutoriálu se dozvíte **how to save a OneNote document to a TIFF file using TIFF JPEG compression** a také o dvou dalších populárních metodách komprese. Provedeme vás potřebným nastavením, importem nezbytných Java balíčků a poskytneme jasný krok‑za‑krokem kód pro každou možnost komprese. Na konci budete schopni řídit **TIFF image quality**, snížit velikost souboru a dokonce vytvořit černobílé TIFFy pro fax‑styl výstup.

## Rychlé odpovědi
- **What is TIFF JPEG compression?** Metoda ztrátové komprese, která snižuje velikost souboru TIFF při zachování vizuální kvality.  
- **Which library handles the conversion?** Aspose.Note for Java.  
- **Do I need a license?** Bezplatná zkušební verze funguje pro testování; licence je vyžadována pro produkci.  
- **Can I change the image quality?** Ano, nastavte vlastnost `quality` na `ImageSaveOptions`.  
- **Is batch conversion possible?** Rozhodně – projděte smyčkou dokumenty a použijte stejné možnosti.

## Co je TIFF JPEG Compression?

Komprese TIFF JPEG ukládá obrazová data v kontejneru TIFF, ale používá ztrátový algoritmus JPEG k zmenšení souboru. Je ideální, když potřebujete rovnováhu mezi **tiff image quality** a menší velikostí souboru, zejména pro webové nebo archivní scénáře.

## Proč používat různé typy komprese TIFF?

- **JPEG** – Vhodné pro fotografie; nabízí nastavitelnou kvalitu.  
- **PackBits** – Jednoduché, bezztrátové kódování běhu; užitečné pro grafiku s velkými jednotnými oblastmi.  
- **CCITT Group 3 Fax** – Pouze černobílé; perfektní pro skenované dokumenty a faxové přenosy.  

Výběrem správné komprese můžete splnit omezení úložiště, aniž byste obětovali vizuální věrnost požadovanou pro vaši aplikaci.

## Předpoklady

- Nainstalovaný Java Development Kit (JDK).  
- Knihovna Aspose.Note pro Java přidána do vašeho projektu (Maven/Gradle nebo ruční JAR).  
- Základní znalost syntaxe Java.

## Import balíčků

Nejprve přiveďte potřebné třídy Aspose.Note do vašeho Java souboru:

```java
import com.aspose.note.*;
import java.io.IOException;
import java.nio.file.Paths;
```

## Krok 1: Uložení do TIFF pomocí komprese TIFF JPEG

Níže je kompletní metoda, která načte soubor OneNote a uloží jej jako TIFF s JPEG kompresí. Upravit hodnotu `quality` (0‑100) pro řízení **tiff image quality**.

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
- `setQuality(93)` (volitelné) jemně ladí kvalitu obrazu; nižší hodnoty produkují menší soubory.

### Jak uložit TIFF s JPEG kompresí v Javě
1. Nastavte `dataDir` na složku obsahující váš soubor `.one`.  
2. Zavolejte `SaveToTiffUsingJpegCompression()` z vaší hlavní metody nebo služby.  
3. Výsledný soubor `.tiff` se objeví ve stejném adresáři.

## Krok 2: Uložení do TIFF pomocí komprese PackBits

Pokud potřebujete bezztrátovou možnost, PackBits je jednoduchý algoritmus běhové délky, který funguje dobře pro grafiku s jednotnými barvami.

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

Pro dokumenty ve stylu faxu často potřebujete **black and white TIFF**. CCITT Group 3 poskytuje vysokou kompresi pro monochromatické obrázky.

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
- `setTiffCompression(TiffCompression.Ccitt3)` použije fax‑orientovanou kompresi.

## Časté problémy a tipy

| Problém | Řešení |
|-------|----------|
| **Výstupní soubor je větší než očekáváno** | Zkuste snížit hodnotu JPEG `quality` nebo přepněte na PackBits, pokud je bezztrátová komprese přijatelná. |
| **Barvy vypadají vybledlé** | Ujistěte se, že nevybíráte neúmyslně `ColorMode.BlackAndWhite`, když potřebujete plnou barvu. |
| **Chyba nepodporovaného formátu obrázku** | Ověřte, že používáte aktuální verzi Aspose.Note; starší sestavení mohou postrádat některé kompresní výčty. |
| **LicenseException za běhu** | Nainstalujte platnou licenci Aspose.Note (`License license = new License(); license.setLicense("Aspose.Note.Java.lic");`). |

## Často kladené otázky

**Q: Můžu převádět jiné typy dokumentů (např. PDF, DOCX) na TIFF s těmito možnostmi?**  
A: Ano. Aspose.Note se zaměřuje na soubory OneNote, ale další knihovny Aspose (PDF, Words) poskytují podobné `ImageSaveOptions` pro jejich příslušné formáty.

**Q: Jak se liší komprese TIFF JPEG od standardních JPEG souborů?**  
A: Obrazová data jsou uložena uvnitř kontejneru TIFF, zachovávají metadata a umožňují více stránek, zatímco kompresní algoritmus zůstává JPEG.

**Q: Je možné hromadně zpracovat mnoho souborů `.one`?**  
A: Rozhodně. Projděte složku, zavolejte kteroukoliv ze tří metod pro každý soubor a shromážděte výsledné TIFFy.

**Q: Můžu řídit DPI/rozlišení výstupního TIFF?**  
A: Ano. Použijte `options.setResolution(int dpi)` před uložením.

**Q: Podporuje Aspose.Note asynchronní zpracování?**  
A: API je samo o sobě synchronní, ale můžete volání zabalit do Java `CompletableFuture` nebo thread poolů pro paralelní provádění.

## Závěr

Nyní máte kompletní **java tiff conversion** sadu nástrojů, která vám umožní ukládat dokumenty OneNote jako TIFF soubory pomocí JPEG, PackBits nebo CCITT Group 3 Fax komprese. Přizpůsobte kvalitu, režim barev a rozlišení tak, aby vyhovovaly vašim konkrétním požadavkům na **tiff image quality**, a integrujte tyto metody do hromadných pracovních postupů pro maximální produktivitu.

---

**Poslední aktualizace:** 2025-12-17  
**Testováno s:** Aspose.Note for Java 23.12 (nejnovější v době psaní)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}