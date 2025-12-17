---
date: 2025-12-17
description: Leer hoe u OneNote kunt exporteren door een document op te slaan als
  een grijswaarden‑PNG‑afbeelding met Aspose.Note voor Java. Inclusief stappen om
  een OneNote‑document te laden en een grijswaardenafbeelding te maken.
linktitle: How to Export OneNote as Grayscale Image – Aspose.Note
second_title: Aspose.Note Java API
title: Hoe OneNote exporteren als grijswaardenafbeelding – Aspose.Note
url: /nl/java/onenote-document-saving/save-to-grayscale-image/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Opslaan als Grijswaardenafbeelding in OneNote - Aspose.Note

## Introductie

In deze tutorial laten we je **hoe je onenote exporteert** zien door een document op te slaan als een grijswaardenafbeelding met Aspose.Note voor Java. Grijswaardenafbeeldingen zijn monochrome afbeeldingen die alleen grijstinten bevatten, wat nuttig kan zijn voor afdrukken, archivering of het verkleinen van de bestandsgrootte. We lopen door het laden van een OneNote‑document, het configureren van de opslaan‑opties om **een grijswaardenafbeelding te maken**, en uiteindelijk **het document opslaan als PNG**.

## Snelle Antwoorden
- **Wat betekent “hoe je onenote exporteert”?** Het verwijst naar het programmatically omzetten van een OneNote‑bestand naar een ander formaat, zoals een afbeelding.  
- **Welk formaat is het beste voor grijswaardenoutput?** PNG werkt goed omdat het verliesvrije kwaliteit behoudt en de grijswaarden‑kleurmodus ondersteunt.  
- **Heb ik een licentie nodig?** Een geldige Aspose.Note‑licentie is vereist voor productiegebruik; een tijdelijke proeflicentie is beschikbaar voor testen.  
- **Welke Java‑versie is vereist?** Java 8 of hoger wordt aanbevolen.  
- **Kan ik de afbeeldingsgrootte wijzigen?** Ja, je kunt de eigenschappen van `ImageSaveOptions` zoals `Resolution` of `PageSize` aanpassen vóór het opslaan.

## Wat is “hoe je onenote exporteert”?
Exporteren van OneNote betekent programmatically een OneNote‑`.one`‑bestand omzetten naar een andere representatie—zoals PDF, HTML of een afbeelding. In deze gids richten we ons op exporteren naar een **grijswaarden‑PNG**‑afbeelding, wat een veelvoorkomende eis is voor documentatie‑ of afdrukwerkstromen.

## Waarom OneNote exporteren als een grijswaardenafbeelding?
- **Kleinere bestandsgrootte** – Grijswaarden‑PNG’s zijn doorgaans kleiner dan full‑color afbeeldingen.  
- **Betere leesbaarheid** – Voor afgedrukte rapporten biedt grijswaarden vaak duidelijker contrast.  
- **Compatibiliteit** – PNG wordt breed ondersteund door browsers, editors en mobiele apparaten.  

## Vereisten

Voordat we beginnen, zorg dat je het volgende hebt:

1. Java Development Kit (JDK) geïnstalleerd op je systeem.  
2. Aspose.Note voor Java‑bibliotheek. Je kunt deze downloaden van [here](https://releases.aspose.com/note/java/).  
3. Basiskennis van Java‑programmeren.  

## Pakketten Importeren

Om te beginnen, importeer de benodigde pakketten:

```java
import com.aspose.note.ColorMode;
import com.aspose.note.Document;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.SaveFormat;
import java.io.IOException;
```

## Stap 1: Het OneNote‑document Laden

Eerst **laad je onenote‑document** in Aspose.Note. Vervang `"Your Document Directory"` door het pad naar je lokale map en `"Aspose.one"` door de naam van je OneNote‑bestand.

```java
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Aspose.one");
```

## Stap 2: Uitvoerpad en Opties Instellen

Definieer het uitvoerpad voor de grijswaardenafbeelding en specificeer de opslaan‑opties. We stellen de `ColorMode` in op `GrayScale` en gebruiken het **save document as png**‑formaat.

```java
dataDir = dataDir + "SaveAsGrayscaleImage_out.png";
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);
options.setColorMode(ColorMode.GrayScale);
```

## Stap 3: Het Document Opslaan

Sla tenslotte het document op als een grijswaarden‑PNG‑afbeelding met de geconfigureerde opties.

```java
oneFile.save(dataDir, options);
```

## Veelvoorkomende Problemen en Oplossingen
- **FileNotFoundException** – Controleer of `dataDir` naar de juiste map wijst en of het `.one`‑bestand bestaat.  
- **LicenseException** – Zorg ervoor dat je een geldige Aspose.Note‑licentie hebt toegepast vóór het aanroepen van `save`.  
- **Low‑resolution output** – Pas `options.setResolution(300)` aan om de DPI te verhogen indien nodig.

## Veelgestelde Vragen

**Q1: Kan ik de grijswaardenafbeelding in een ander formaat opslaan?**  
A1: Ja, wijzig simpelweg de `SaveFormat`‑parameter in de `ImageSaveOptions`‑constructor naar `Jpeg`, `Bmp`, etc.

**Q2: Is Aspose.Note compatibel met alle versies van OneNote‑documenten?**  
A2: Aspose.Note ondersteunt Microsoft OneNote 2010 en latere versies.

**Q3: Vereist Aspose.Note een licentie om te gebruiken?**  
A3: Een geldige licentie is vereist voor productiegebruik, maar een tijdelijke proeflicentie kan worden verkregen voor evaluatie.

**Q4: Kan ik andere aspecten van het document manipuleren voordat ik het als afbeelding opsla?**  
A4: Absoluut! Aspose.Note biedt een uitgebreide API voor het bewerken van secties, pagina's en inhoud vóór export.

**Q5: Waar kan ik ondersteuning vinden als ik problemen tegenkom?**  
A5: Je kunt ondersteuning vinden op het Aspose.Note‑forum [here](https://forum.aspose.com/c/note/28).

## Conclusie

Je hebt nu geleerd **hoe je onen OneNote‑bestand te laden, de opslaan‑opties te configureren om **een grijswaardenafbeelding te maken**, en **het document op te slaan als PNG**. Deze techniek is handig voor het genereren van lichtgewicht, print‑klare visuals uit OneNote‑notitieboeken. Voel je vrij om te experimenteren met andere `ColorMode`‑instellingen of afbeeldingsformaten om aan de behoeften van je project te voldoen.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Last Updated:** 2025-12-17  
**Tested With:** Aspose.Note 24.12 for Java  
**Author:** Aspose  

---