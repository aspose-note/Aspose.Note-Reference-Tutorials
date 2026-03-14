---
date: 2026-03-14
description: Leer hoe u OneNote‑documenten als TIFF‑bestanden kunt opslaan met TIFF‑JPEG‑compressie,
  TIFF‑PackBits‑compressie of CCITT Group 3‑fax in Java. Beheer de beeldkwaliteit,
  bestandsgrootte en kleurmodus met Aspose.Note.
linktitle: Save to TIFF Image Using TIFF JPEG Compression in OneNote
second_title: Aspose.Note Java API
title: Opslaan als TIFF-afbeelding met TIFF JPEG-compressie in OneNote
url: /nl/java/onenote-document-saving/save-to-tiff-image-using-image-save-options/
weight: 21
---

 JPEG-compressie in OneNote"

Proceed.

We'll translate each paragraph.

Make sure to keep bullet points, tables.

Let's write.

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# TIFF-afbeelding opslaan met TIFF JPEG-compressie in OneNote

## Inleiding

In deze tutorial ontdek je **hoe je een OneNote‑document opslaat als een TIFF‑bestand met TIFF JPEG‑compressie** en twee andere populaire compressiemethoden. We lopen de benodigde configuratie door, importeren de benodigde Java‑pakketten en bieden duidelijke stap‑voor‑stap‑code voor elke compressie‑optie. Aan het einde kun je **TIFF‑afbeeldingskwaliteit** regelen, de bestandsgrootte verkleinen en zelfs zwart‑wit‑TIFF’s maken voor fax‑achtige uitvoer.

## Snelle antwoorden
- **Wat is TIFF JPEG‑compressie?** Een verliesgevende compressiemethode die de TIFF‑bestandsgrootte verkleint terwijl de visuele kwaliteit behouden blijft.  
- **Welke bibliotheek voert de conversie uit?** Aspose.Note for Java.  
- **Heb ik een licentie nodig?** Een gratis proefversie werkt voor testen; een licentie is vereist voor productie.  
- **Kan ik de beeldkwaliteit aanpassen?** Ja, stel de `quality`‑eigenschap in op `ImageSaveOptions`.  
- **Is batch‑conversie mogelijk?** Absoluut – loop door documenten en pas dezelfde opties toe.

## Wat is TIFF JPEG‑compressie?
TIFF JPEG‑compressie slaat beeldgegevens op in een TIFF‑container maar past het verliesgevende JPEG‑algoritme toe om het bestand te verkleinen. Het is ideaal wanneer je een balans nodig hebt tussen **tiff‑beeldkwaliteit** en een kleinere bestandsgrootte, vooral voor web‑ of archiveringsscenario’s.

## Waarom verschillende TIFF‑compressietypen gebruiken?
- **JPEG** – Goed voor foto’s; biedt instelbare kwaliteit.  
- **PackBits** – Eenvoudige, verlies‑vrije run‑length‑codering; nuttig voor grafische afbeeldingen met grote uniforme gebieden.  
- **CCITT Group 3 Fax** – Alleen zwart‑wit; perfect voor gescande documenten en fax‑overdracht.  

De juiste compressie kiezen laat je opslagbeperkingen halen zonder de visuele getrouwheid die je applicatie vereist op te offeren.

## OneNote naar TIFF converteren met Aspose.Note
Als je doel is om **OneNote naar TIFF te converteren**, behandelen de drie onderstaande methoden de meest voorkomende scenario’s. Elke methode laadt een `.one`‑bestand, configureert `ImageSaveOptions` en slaat het resultaat op als een `.tiff`‑bestand.

## Voorvereisten

- Java Development Kit (JDK) geïnstalleerd.  
- Aspose.Note for Java‑bibliotheek toegevoegd aan je project (Maven/Gradle of handmatig JAR).  
- Basiskennis van Java‑syntaxis.

## Pakketten importeren

Breng eerst de benodigde Aspose.Note‑klassen in je Java‑bestand:

```java
import com.aspose.note.*;
import java.io.IOException;
import java.nio.file.Paths;
```

## Stap 1: Opslaan als TIFF met TIFF JPEG‑compressie

Hieronder staat de volledige methode die een OneNote‑bestand laadt en opslaat als een TIFF met JPEG‑compressie. Pas de `quality`‑waarde (0‑100) aan om **tiff‑beeldkwaliteit** te regelen.

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
- `setQuality(93)` (optioneel) verfijnt de beeldkwaliteit; lagere waarden leveren kleinere bestanden op.

### Hoe TIFF met JPEG‑compressie opslaan in Java
1. Verwijs `dataDir` naar de map die je `.one`‑bestand bevat.  
2. Roep `SaveToTiffUsingJpegCompression()` aan vanuit je `main`‑methode of service.  
3. Het resulterende `.tiff`‑bestand verschijnt in dezelfde directory.

## Overzicht van TIFF PackBits‑compressie

PackBits is een verlies‑vrije compressie‑algoritme dat het beste werkt voor afbeeldingen met grote gebieden van egale kleur. Het wordt vaak aangeduid als **tiff packbits compression** in de documentatie.

## Stap 2: Opslaan als TIFF met PackBits‑compressie

Als je een verlies‑vrije optie nodig hebt, is PackBits een eenvoudige run‑length‑algoritme die goed werkt voor grafische afbeeldingen met egale kleuren.

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

- `setTiffCompression(TiffCompression.PackBits)` schakelt de compressiemethode om.  
- Er is geen kwaliteitsinstelling nodig omdat PackBits verlies‑vrij is.

## Stap 3: Opslaan als TIFF met CCITT Group 3 Fax‑compressie (Zwart‑wit‑TIFF)

Voor fax‑achtige documenten wil je vaak een **zwart‑wit‑TIFF**. CCITT Group 3 biedt hoge compressie voor monochrome afbeeldingen.

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
| **Uitvoerbestand is groter dan verwacht** | Probeer de JPEG `quality`‑waarde te verlagen of schakel over naar PackBits als verlies‑vrij acceptabel is. |
| **Kleuren zien er vervaagd uit** | Zorg ervoor dat je niet per ongeluk `ColorMode.BlackAndWhite` hebt ingesteld wanneer je volledige kleur nodig hebt. |
| **Niet‑ondersteunde afbeeldingstype‑fout** | Controleer of je een recente versie van Aspose.Note gebruikt; oudere builds missen mogelijk bepaalde compressie‑enums. |
| **LicenseException tijdens runtime** | Installeer een geldige Aspose.Note‑licentie (`License license = new License(); license.setLicense("Aspose.Note.Java.lic");`). |

## Veelgestelde vragen

**V: Kan ik andere documenttypen (bijv. PDF, DOCX) naar TIFF converteren met deze opties?**  
A: Ja. Terwijl Aspose.Note zich richt op OneNote‑bestanden, bieden Aspose.PDF, Aspose.Words en andere bibliotheken vergelijkbare `ImageSaveOptions` voor hun formaten.

**V: Hoe verschilt TIFF JPEG‑compressie van een standaard JPEG‑bestand?**  
A: Het JPEG‑algoritme is hetzelfde, maar de beeldgegevens bevinden zich in een TIFF‑container, die meerdere pagina’s en rijkere metadata kan bevatten.

**V: Is het mogelijk om veel `.one`‑bestanden in batch te verwerken?**  
A: Absoluut. Loop door een map, roep een van de drie methoden aan voor elk bestand en verzamel de resulterende TIFF’s.

**V: Kan ik de DPI/resolutie van de uitvoer‑TIFF regelen?**  
A: Ja. Gebruik `options.setResolution(int dpi)` vóór het opslaan.

**V: Ondersteunt Aspose.Note asynchrone verwerking?**  
A: De API zelf is synchroon, maar je kunt oproepen wikkelen in Java’s `CompletableFuture` of een thread‑pool voor parallelle uitvoering.

## Conclusie

Je beschikt nu over een volledige **java tiff conversion**‑toolkit waarmee je OneNote‑documenten kunt opslaan als TIFF‑bestanden met JPEG, PackBits of CCITT Group 3 Fax‑compressie. Pas de kwaliteit, kleurmodus en resolutie aan om te voldoen aan je specifieke **tiff‑beeldkwaliteit**‑eisen, en integreer deze methoden in batch‑workflows voor maximale productiviteit.

---

**Laatst bijgewerkt:** 2026-03-14  
**Getest met:** Aspose.Note for Java 23.12 (latest at time of writing)  
**Auteur:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}