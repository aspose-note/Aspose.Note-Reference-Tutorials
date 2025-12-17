---
date: 2025-12-17
description: Leer hoe u OneNote‑documenten als TIFF‑bestanden kunt opslaan met TIFF‑JPEG‑compressie,
  PackBits of CCITT Group 3‑fax in Java. Beheer de beeldkwaliteit, bestandsgrootte
  en kleurmodus met Aspose.Note.
linktitle: Save to TIFF Image Using TIFF JPEG Compression in OneNote
second_title: Aspose.Note Java API
title: Opslaan naar TIFF‑afbeelding met TIFF‑JPEG‑compressie in OneNote
url: /nl/java/onenote-document-saving/save-to-tiff-image-using-image-save-options/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Opslaan als TIFF-afbeelding met TIFF JPEG-compressie in OneNote

## Inleiding

In deze tutorial ontdek je **hoe je een OneNote‑document opslaat als een TIFF‑bestand met TIFF JPEG‑compressie** en twee andere populaire compressiemethoden. We lopen de benodigde setup door, importeren de vereiste Java‑pakketten en bieden duidelijke stap‑voor‑stap‑code voor elke compressie‑optie. Aan het einde kun je **TIFF‑afbeeldingskwaliteit** beheersen, de bestandsgrootte verkleinen en zelfs zwart‑wit‑TIFF's produceren voor fax‑achtige output.

## Snelle antwoorden
- **Wat is TIFF JPEG‑compressie?** Een verlies‑rijke compressiemethode die de TIFF‑bestandsgrootte verkleint terwijl de visuele kwaliteit behouden blijft.  
- **Welke bibliotheek verwerkt de conversie?** Aspose.Note for Java.  
- **Heb ik een licentie nodig?** Een gratis proefversie werkt voor testen; een licentie is vereist voor productie.  
- **Kan ik de afbeeldingskwaliteit aanpassen?** Ja, stel de `quality`‑eigenschap in op `ImageSaveOptions`.  
- **Is batch‑conversie mogelijk?** Absoluut – loop door documenten en pas dezelfde opties toe.

## Wat is TIFF JPEG‑compressie?

TIFF JPEG‑compressie slaat beeldgegevens op in de TIFF‑container maar past het verlies‑rijke algoritme van JPEG toe om het bestand te verkleinen. Het is ideaal wanneer je een balans nodig hebt tussen **tiff‑afbeeldingskwaliteit** en een kleinere bestandsgrootte, vooral voor web‑ of archiveringsscenario's.

## Waarom verschillende TIFF‑compressietypen gebruiken?

- **JPEG** – Goed voor foto’s; biedt aanpasbare kwaliteit.  
- **PackBits** – Eenvoudige, verlies‑vrije run‑length‑codering; nuttig voor graphics met grote uniforme gebieden.  
- **CCITT Group 3 Fax** – Alleen zwart‑wit; perfect voor gescande documenten en fax‑overdracht.  

Het kiezen van de juiste compressie stelt je in staat om aan opslagbeperkingen te voldoen zonder de visuele nauwkeurigheid die voor jouw toepassing nodig is op te offeren.

## Voorvereisten

- Java Development Kit (JDK) geïnstalleerd.  
- Aspose.Note for Java‑bibliotheek toegevoegd aan je project (Maven/Gradle of handmatige JAR).  
- Basiskennis van Java‑syntaxis.

## Pakketten importeren

Eerst importeer je de benodigde Aspose.Note‑klassen in je Java‑bestand:

```java
import com.aspose.note.*;
import java.io.IOException;
import java.nio.file.Paths;
```

## Stap 1: Opslaan als TIFF met TIFF JPEG‑compressie

Hieronder staat de volledige methode die een OneNote‑bestand laadt en opslaat als een TIFF met JPEG‑compressie. Pas de `quality`‑waarde (0‑100) aan om **tiff‑afbeeldingskwaliteit** te regelen.

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
- `setQuality(93)` (optioneel) verfijnt de afbeeldingskwaliteit; lagere waarden produceren kleinere bestanden.

### Hoe TIFF opslaan met JPEG‑compressie in Java
1. Wijs `dataDir` naar de map die je `.one`‑bestand bevat.  
2. Roep `SaveToTiffUsingJpegCompression()` aan vanuit je main‑methode of service.  
3. Het resulterende `.tiff`‑bestand verschijnt in dezelfde map.

## Stap 2: Opslaan als TIFF met PackBits‑compressie

Als je een verlies‑vrije optie nodig hebt, is PackBits een eenvoudig run‑length‑algoritme dat goed werkt voor graphics met effen kleuren.

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

- `setColorMode(ColorMode.BlackAndWhite)` dwingt een monochrome output af.  
- `setTiffCompression(TiffCompression.Ccitt3)` past de fax‑gerichte compressie toe.

## Veelvoorkomende problemen & tips

| Probleem | Oplossing |
|----------|-----------|
| **Uitvoerbestand is groter dan verwacht** | Probeer de JPEG `quality`‑waarde te verlagen of schakel over naar PackBits als verlies‑vrij acceptabel is. |
| **Kleuren lijken vervaagd** | Zorg ervoor dat je niet per ongeluk `ColorMode.BlackAndWhite` instelt wanneer je volledige kleur nodig hebt. |
| **Niet‑ondersteunde afbeeldingformaat‑fout** | Controleer of je een recente versie van Aspose.Note gebruikt; oudere builds kunnen bepaalde compressie‑enums missen. |
| **LicenseException tijdens uitvoering** | Installeer een geldige Aspose.Note‑licentie (`License license = new License(); license.setLicense("Aspose.Note.Java.lic");`). |

## Veelgestelde vragen

**V: Kan ik andere documenttypen (bijv. PDF, DOCX) naar TIFF converteren met deze opties?**  
A: Ja. Aspose.Note richt zich op OneNote‑bestanden, maar de andere bibliotheken van Aspose (PDF, Words) bieden vergelijkbare `ImageSaveOptions` voor hun respectieve formaten.

**V: Hoe verschilt TIFF JPEG‑compressie van standaard JPEG‑bestanden?**  
A: De beeldgegevens worden opgeslagen in een TIFF‑container, waardoor metadata behouden blijven en meerdere pagina's mogelijk zijn, terwijl het compressie‑algoritme JPEG blijft.

**V: Is het mogelijk om veel `.one`‑bestanden batch‑gewijs te verwerken?**  
A: Absoluut. Loop door een map, roep een van de drie methoden per bestand aan en verzamel de resulterende TIFF‑bestanden.

**V: Kan ik de DPI/resolutie van de uitvoer‑TIFF regelen?**  
A: Ja. Gebruik `options.setResolution(int dpi)` vóór het opslaan.

**V: Ondersteunt Aspose.Note asynchrone verwerking?**  
A: De API zelf is synchroon, maar je kunt oproepen wikkelen in Java’s `CompletableFuture` of thread‑pools voor parallelle uitvoering.

## Conclusie

Je hebt nu een complete **java tiff-conversie**‑toolkit die je in staat stelt OneNote‑documenten op te slaan als TIFF‑bestanden met JPEG-, PackBits- of CCITT Group 3 Fax‑compressie. Pas de kwaliteit, kleurmodus en resolutie aan om te voldoen aan je specifieke **tiff‑afbeeldingskwaliteit**‑eisen, en integreer deze methoden in batch‑workflows voor maximale productiviteit.

---

**Laatst bijgewerkt:** 2025-12-17  
**Getest met:** Aspose.Note for Java 23.12 (latest op het moment van schrijven)  
**Auteur:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}