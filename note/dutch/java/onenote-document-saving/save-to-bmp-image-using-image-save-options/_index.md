---
date: 2026-03-05
description: Leer hoe u OneNote‑documenten kunt exporteren naar BMP‑afbeeldingen met
  behulp van de Image Save Options van Aspose.Note voor Java. Bekijk ook hoe u OneNote
  kunt converteren naar PDF of OneNote kunt opslaan als PNG.
linktitle: how to export onenote to BMP Image Using Image Save Options
second_title: Aspose.Note Java API
title: Hoe OneNote exporteren naar BMP-afbeelding met behulp van afbeeldingsbewaaropties
url: /nl/java/onenote-document-saving/save-to-bmp-image-using-image-save-options/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# hoe onenote exporteren naar BMP-afbeelding met Image Save Options

## Hoe onenote exporteren naar BMP-afbeelding

Aspose.Note for Java is een krachtige bibliotheek die Java‑ontwikkelaars in staat stelt om programmatically met Microsoft OneNote‑bestanden te werken. **In deze tutorial leer je hoe je onenote‑documenten exporteert naar BMP‑afbeeldingen** met behulp van de Image Save Options‑functie van Aspose.Note for Java. We lopen elke stap door, leggen uit waarom je BMP boven andere formaten zou kunnen kiezen, en laten zien hoe je deze mogelijkheid in je eigen applicaties kunt integreren.

## Snelle antwoorden
- **Wat doet de Image Save Options‑klasse?** Hiermee kun je het uitvoer‑afbeeldingsformaat (BMP, PNG, JPEG, enz.) opgeven bij het converteren van een OneNote‑pagina.  
- **Heb ik een licentie nodig om het voorbeeld uit te voeren?** Een gratis proefversie werkt voor evaluatie, maar een commerciële licentie is vereist voor productiegebruik.  
- **Kan ik een OneNote‑pagina converteren naar PDF of PNG in plaats van BMP?** Ja – wijzig eenvoudig de `SaveFormat`‑enum (bijv. `SaveFormat.Pdf` of `SaveFormat.Png`).  
- **Welke Java‑versie wordt ondersteund?** Java 8 en hoger worden volledig ondersteund.  
- **Is er speciale afhandeling voor grote documenten?** Je kunt de uitvoer streamen om hoog geheugenverbruik te vermijden.

## Wat is “Image Save Options” in Aspose.Note?
De `ImageSaveOptions`‑klasse biedt fijnmazige controle over hoe OneNote‑pagina's worden gerenderd als rasterafbeeldingen. Je kunt het afbeeldingsformaat, de resolutie, kleurdiepte en meer instellen. Deze flexibiliteit maakt het eenvoudig om **onenote‑pagina‑afbeeldingen te exporteren** voor legacy‑systemen (BMP) of moderne websituaties (PNG/JPEG).  

## Voorvereisten

Before you begin, make sure you have:

1. Basiskennis van de programmeertaal Java.  
2. JDK (Java Development Kit) geïnstalleerd op je machine.  
3. Een IDE zoals Eclipse of IntelliJ IDEA.  
4. Aspose.Note for Java‑bibliotheek – download deze van [hier](https://releases.aspose.com/note/java/).

## Pakketten importeren

First, import the necessary Aspose.Note classes and standard Java I/O utilities:

```java
import com.aspose.note.*;
import java.io.IOException;
```

## Stap 1: Het OneNote‑document laden

```java
// The path to the documents directory.
String dataDir = "Your Document Directory";

// Load the document into Aspose.Note.
Document oneFile = new Document(dataDir + "Aspose.one");
```

Hier wijzen we naar de map die het bron‑OneNote‑bestand (`Aspose.one`) bevat en laden het in een `Document`‑object. Dit object geeft je volledige toegang tot pagina's, secties en andere elementen binnen het notitieboek.

## Stap 2: Het document opslaan als BMP‑afbeelding

```java
dataDir = dataDir + "SaveToBmpImageUsingImageSaveOptions_out.bmp";

// Save the document.
oneFile.save(dataDir, new ImageSaveOptions(SaveFormat.Bmp));
```

We voegen de uitvoerbestandsnaam samen en roepen vervolgens `save` aan met een `ImageSaveOptions`‑instantie geconfigureerd voor **BMP** (`SaveFormat.Bmp`).  
Als je een **onenote‑pagina wilt opslaan** als PNG, vervang dan eenvoudig `SaveFormat.Bmp` door `SaveFormat.Png`. Evenzo maakt `SaveFormat.Pdf` een **onenote‑naar‑pdf** conversie mogelijk.

## Waarom BMP kiezen?
- **Lossless kwaliteit** – BMP slaat ruwe pixelgegevens op, waardoor het exacte uiterlijk van de originele pagina behouden blijft.  
- **Compatibiliteit** – Oudere Windows‑applicaties vereisen vaak BMP‑bestanden.  
- **Eenvoud** – Geen compressie‑artefacten, waardoor het ideaal is voor verdere beeldverwerking.

## Veelvoorkomende problemen & tips

- **Bestandspad‑fouten** – Zorg ervoor dat `dataDir` eindigt met de juiste scheidingsteken (`/` of `\`).  
- **Grote notitieboeken** – Voor zeer grote OneNote‑bestanden kun je overwegen elke pagina afzonderlijk op te slaan om het geheugenverbruik laag te houden.  
- **Licentie‑uitzonderingen** – Het uitvoeren van de code zonder een geldige licentie voegt een watermerk toe aan de gegenereerde afbeelding.

## Conclusie

In deze gids hebben we **hoe onenote**‑documenten te exporteren naar BMP‑afbeeldingen laten zien met behulp van `ImageSaveOptions` van Aspose.Note for Java. Door de `SaveFormat`‑enum te wisselen kun je ook PNG, JPEG, PDF of andere ondersteunde formaten genereren, waardoor je een flexibele manier hebt om OneNote‑inhoud te exporteren voor elke downstream‑scenario.

## Veelgestelde vragen

**Q1: Kan ik OneNote‑documenten opslaan in andere afbeeldingsformaten dan BMP?**  
A: Ja, je kunt `ImageSaveOptions` gebruiken met `SaveFormat.Png`, `SaveFormat.Jpeg`, `SaveFormat.Gif` of `SaveFormat.Tiff` om naar die formaten te exporteren.

**Q2: Ondersteunt Aspose.Note for Java conversie tussen verschillende documentformaten?**  
A: Zeker. Naast afbeeldingsformaten kun je OneNote‑bestanden converteren naar PDF, DOCX, HTML en meer met de juiste `SaveFormat`.

**Q3: Is Aspose.Note for Java compatibel met de nieuwste versies van OneNote?**  
A: Ja, de bibliotheek wordt regelmatig bijgewerkt om in sync te blijven met de nieuwste OneNote‑releases.

**Q4: Kan ik de inhoud van OneNote‑documenten programmatically manipuleren?**  
A: Ja, je kunt pagina's, secties en rijke inhoud (tekst, afbeeldingen, tabellen) toevoegen, bewerken of verwijderen via de API.

**Q5: Biedt Aspose.Note for Java technische ondersteuning?**  
A: Ja, Aspose biedt technische ondersteuning en een speciaal forum. Bezoek het [Aspose.Note‑forum](https://forum.aspose.com/c/note/28) voor hulp.

---

**Laatst bijgewerkt:** 2026-03-05  
**Getest met:** Aspose.Note for Java 24.12  
**Auteur:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}