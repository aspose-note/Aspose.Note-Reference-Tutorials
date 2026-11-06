---
date: 2026-11-05
description: Leer hoe u de TIFF‑bestandsgrootte kunt verkleinen bij het converteren
  van OneNote‑notitieblokken naar TIFF in Java met Aspose.Note. Inclusief JPEG, PackBits
  en zwart‑wit TIFF‑opties.
keywords:
- reduce tiff file size
- black white tiff
- tiff jpeg compression
- aspose note java
lastmod: 2026-11-05
linktitle: Hoe de TIFF‑bestandsgrootte te verkleinen bij het converteren van OneNote
  in Java
og_description: Leer hoe u de TIFF‑bestandsgrootte kunt verkleinen bij het converteren
  van OneNote‑notitieblokken naar TIFF in Java met Aspose.Note. Inclusief JPEG, PackBits
  en zwart‑wit TIFF‑opties.
og_image_alt: Developer guide showing OneNote to TIFF conversion with compression
  options in Java
og_title: Hoe de TIFF‑bestandsgrootte te verkleinen bij het converteren van OneNote
  in Java
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
title: Hoe de TIFF‑bestandsgrootte te verkleinen bij het converteren van OneNote in
  Java
url: /nl/java/onenote-document-saving/save-to-tiff-image-using-image-save-options/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hoe TIFF-bestandsgrootte te verkleinen bij het converteren van OneNote in Java

## Inleiding

In deze tutorial ontdek je hoe je **TIFF-bestandsgrootte** kunt verkleinen tijdens het converteren van OneNote-notitieblokken naar TIFF-afbeeldingen met Aspose.Note for Java. We lopen drie compressiemethoden door—TIFF JPEG, PackBits en CCITT Group 3 (zwart‑wit TIFF)—en laten zien hoe je de beeldkwaliteit kunt aanpassen, de kleermodus kunt regelen, en de bestandsgrootte optimaal houdt voor web-, archiverings- of fax‑scenario's.

## Snelle antwoorden
- **Wat is TIFF JPEG-compressie?** Een verliesgevende compressiemethode die de TIFF-bestandsgrootte verkleint terwijl de visuele kwaliteit behouden blijft.  
- **Welke bibliotheek verwerkt de conversie?** Aspose.Note for Java.  
- **Heb ik een licentie nodig?** Een gratis proefversie werkt voor testen; een licentie is vereist voor productie.  
- **Kan ik de beeldkwaliteit aanpassen?** Ja, stel de `quality`‑eigenschap in op `ImageSaveOptions`.  
- **Is batchconversie mogelijk?** Absoluut – loop door documenten en pas dezelfde opties toe.

## Overzicht van TIFF JPEG-compressie

TIFF JPEG-compressie slaat beeldgegevens op in een TIFF-container maar past het verliesgevende JPEG-algoritme toe om het bestand te verkleinen. Het is ideaal wanneer je een balans nodig hebt tussen **tiff-beeldkwaliteit** en een kleinere bestandsgrootte, vooral voor web‑ of archiveringsscenario's.

## Waarom verschillende TIFF-compressietypen gebruiken?

Je kiest het compressietype op basis van de inhoud en opslagbehoeften: JPEG werkt het beste voor foto’s, PackBits biedt verliesloze compressie voor grafische afbeeldingen met grote uniforme gebieden, en CCITT Group 3 levert een hoge compressieverhouding voor monochrome fax‑achtige documenten. Het kiezen van de juiste methode stelt je in staat **TIFF-bestandsgrootte** te verkleinen zonder de visuele getrouwheid die je applicatie vereist te compromitteren.

## De juiste compressie kiezen

- **JPEG** – Aanpasbare kwaliteit (0‑100) laat je een afweging maken tussen grootte en detail, perfect voor kleur‑rijke pagina’s.  
- **PackBits** – Verliesloze run‑length‑codering; ideaal wanneer je elke pixel exact moet behouden.  
- **CCITT Group 3** – Alleen monochroom; maximaliseert compressie voor gescande tekst of faxdocumenten.  

## OneNote naar TIFF converteren met Aspose.Note

Als je doel is om **OneNote naar TIFF te converteren**, behandelen de drie onderstaande methoden de meest voorkomende scenario's. Elke methode laadt een `.one`‑bestand, configureert `ImageSaveOptions` en slaat het resultaat op als een `.tiff`‑bestand.

## Vereisten

- Java Development Kit (JDK) geïnstalleerd.  
- Aspose.Note for Java‑bibliotheek toegevoegd aan je project (Maven/Gradle of handmatige JAR).  
- Basiskennis van Java‑syntaxis.

## Pakketten importeren

De klassen `ImageSaveOptions`, `TiffCompression` en `ColorMode` vormen de kern van de conversie‑API.  

`ImageSaveOptions` definieert de opties voor het opslaan van afbeeldingen, zoals formaat en compressie.  
`TiffCompression` somt de ondersteunde TIFF-compressie‑algoritmen op.  
`ColorMode` specificeert de kleurdiepte, bijv. kleur of zwart‑wit.  

```java
// Placeholder for import statements – keep your imports here
```

```java
import com.aspose.note.*;
import java.io.IOException;
import java.nio.file.Paths;
```

## Stap 1: opslaan naar TIFF met TIFF JPEG-compressie

### TIFF opslaan met JPEG-compressie in Java

Laad het OneNote‑bestand, configureer `ImageSaveOptions` met JPEG-compressie, stel eventueel de `quality`‑waarde in, en roep de save‑methode aan. Dit tweestappenpatroon geeft je volledige controle over de uitvoergrootte en visuele getrouwheid.

1. Wijs `dataDir` naar de map die je `.one`‑bestand bevat.  
2. Roep `SaveToTiffUsingJpegCompression()` aan vanuit je hoofd‑methode of service.  
3. Het resulterende `.tiff`‑bestand verschijnt in dezelfde directory.

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

**Uitleg**

- `ImageSaveOptions` vertelt Aspose.Note om een TIFF‑bestand te genereren.  
- `setTiffCompression(TiffCompression.Jpeg)` selecteert JPEG‑compressie.  
- `setQuality(93)` (optioneel) stemt de beeldkwaliteit fijn af; lagere waarden produceren kleinere bestanden.

## Overzicht van TIFF PackBits-compressie

PackBits is een verliesloos compressie‑algoritme dat het beste werkt voor afbeeldingen met grote gebieden van effen kleur. Het wordt vaak aangeduid als **tiff packbits compressie** in de documentatie.

## TIFF opslaan met PackBits-compressie in Java

Als je een verliesloze optie nodig hebt, is PackBits een eenvoudig run‑length‑algoritme dat goed werkt voor grafische afbeeldingen met effen kleuren. Configureer `ImageSaveOptions` met `TiffCompression.PackBits` en sla het document op.

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

**Uitleg**

- `setTiffCompression(TiffCompression.PackBits)` schakelt de compressiemethode.  
- Geen kwaliteitsinstelling nodig omdat PackBits verliesloos is.

## TIFF opslaan met CCITT Group 3-compressie in Java

Voor fax‑achtige documenten wil je vaak een **zwart‑wit TIFF**. CCITT Group 3 biedt hoge compressie voor monochrome afbeeldingen. Stel de kleermodus in op zwart‑wit en kies de CCITT 3‑compressie‑enum.

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

**Uitleg**

- `setColorMode(ColorMode.BlackAndWhite)` dwingt een monochrome uitvoer af.  
- `setTiffCompression(TiffCompression.Ccitt3)` past de fax‑gerichte compressie toe.

## Veelvoorkomende problemen & tips

| Probleem | Oplossing |
|----------|-----------|
| **Uitvoerbestand is groter dan verwacht** | Probeer de JPEG `quality`‑waarde te verlagen of schakel over naar PackBits als verliesloos acceptabel is. |
| **Kleuren lijken vervaagd** | Zorg ervoor dat je niet per ongeluk `ColorMode.BlackAndWhite` hebt ingesteld wanneer je volledige kleur nodig hebt. |
| **Niet‑ondersteunde afbeeldingformaat‑fout** | Controleer of je een recente versie van Aspose.Note gebruikt; oudere builds kunnen bepaalde compressie‑enums missen. |
| **LicenseException tijdens uitvoering** | Installeer een geldige Aspose.Note‑licentie (`License license = new License(); license.setLicense("Aspose.Note.Java.lic");`). |

## Veelgestelde vragen

**Q: Kan ik andere documenttypen (bijv. PDF, DOCX) naar TIFF converteren met deze opties?**  
A: Ja. Terwijl Aspose.Note zich richt op OneNote‑bestanden, bieden Aspose.PDF, Aspose.Words en andere bibliotheken vergelijkbare `ImageSaveOptions` voor hun formaten.

**Q: Hoe verschilt TIFF JPEG-compressie van een standaard JPEG‑bestand?**  
A: Het JPEG‑algoritme is hetzelfde, maar de beeldgegevens bevinden zich in een TIFF‑container, die meerdere pagina's en rijkere metadata kan bevatten.

**Q: Is het mogelijk om veel `.one`‑bestanden batch‑matig te verwerken?**  
A: Absoluut. Loop door een map, roep een van de drie methoden aan voor elk bestand, en verzamel de resulterende TIFF‑bestanden.

**Q: Kan ik de DPI/resolutie van de uitvoer‑TIFF regelen?**  
A: Ja. Gebruik `options.setResolution(int dpi)` vóór het opslaan.

**Q: Ondersteunt Aspose.Note asynchrone verwerking?**  
A: De API zelf is synchroon, maar je kunt oproepen wikkelen in Java’s `CompletableFuture` of een thread‑pool voor parallelle uitvoering.

## Conclusie

Je hebt nu een complete **Java TIFF-conversietoolkit** die je in staat stelt **TIFF-bestandsgrootte** te verkleinen bij het opslaan van OneNote‑documenten als TIFF‑bestanden met JPEG-, PackBits- of CCITT Group 3‑faxcompressie. Pas kwaliteit, kleermodus en resolutie aan om aan je specifieke eisen te voldoen, en integreer deze methoden in batch‑werkstromen voor maximale productiviteit.

---

**Last Updated:** 2026-11-05  
**Tested With:** Aspose.Note for Java 26.4 (latest at time of writing)  
**Author:** Aspose

## Gerelateerde tutorials

- [Hoe OneNote-pagina-afbeelding (JPEG) te renderen met Save Format met Aspose.Note for Java](/note/java/onenote-document-saving/save-to-jpeg-image-using-save-format/)
- [Aspose.Note for Java gebruiken om OneNote op te slaan als PNG met opties – Notitieboek converteren naar afbeelding](/note/java/onenote-notebook-operations/convert-notebook-to-image-with-options/)
- [Hoe OneNote exporteren als grijswaardenafbeelding – Aspose.Note](/note/java/onenote-document-saving/save-to-grayscale-image/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}