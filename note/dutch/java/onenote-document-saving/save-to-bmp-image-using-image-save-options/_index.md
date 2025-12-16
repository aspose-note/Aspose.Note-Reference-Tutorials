---
date: 2025-12-16
description: Leer hoe u OneNote‑documenten kunt opslaan als BMP‑afbeeldingen met behulp
  van de afbeeldingsopslagopties van Aspose.Note voor Java. Zie ook hoe u OneNote
  kunt opslaan als PDF of PNG.
linktitle: how to save onenote to BMP Image Using Image Save Options
second_title: Aspose.Note Java API
title: hoe OneNote op te slaan als BMP-afbeelding met behulp van afbeeldingsopslagopties
url: /nl/java/onenote-document-saving/save-to-bmp-image-using-image-save-options/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# hoe onenote opslaan als BMP-afbeelding met behulp van Image Save Options

## Inleiding

Aspose.Note for Java is een krachtige bibliotheek die Java‑ontwikkelaars in staat stelt om Microsoft OneNote‑bestanden programmatisch te bewerken. **In deze tutorial leer je hoe je onenote‑documenten opslaat als BMP‑afbeeldingen** met behulp van de Image Save Options‑functie van Aspose.Note for Java. We lopen elke stap door, leggen uit waarom je BMP boven andere formaten zou kunnen kiezen, en laten zien hoe je deze functionaliteit in je eigen applicaties kunt integreren.

## Snelle antwoorden
- **Wat doet de Image Save Options‑klasse?** Het stelt je in staat om het uitvoer‑image‑formaat (BMP, PNG, JPEG, enz.) op te geven bij het converteren van een OneNote‑pagina.  
- **Heb ik een licentie nodig om het voorbeeld uit te voeren?** Een gratis proefversie werkt voor evaluatie, maar een commerciële licentie is vereist voor productiegebruik.  
- **Kan ik een OneNote‑pagina converteren naar PDF of PNG in plaats van BMP?** Ja – wijzig eenvoudig de `SaveFormat`‑enum (bijv. `SaveFormat.Pdf` of `SaveFormat.Png`).  
- **Welke Java‑versie wordt ondersteund?** Java 8 en later worden volledig ondersteund.  
- **Is er speciale afhandeling voor grote documenten?** Je kunt de uitvoer streamen om een hoog geheugenverbruik te voorkomen.

## Wat is “Image Save Options” in Aspose.Note?

De `ImageSaveOptions`‑klasse biedt fijnmazige controle over hoe OneNote‑pagina's worden gerenderd als rasterafbeeldingen. Je kunt het image‑formaat, de resolutie, de kleurdiepte en meer instellen. Deze flexibiliteit maakt het eenvoudig om BMP‑bestanden te genereren voor legacy‑systemen of PNG/JPEG‑bestanden voor webgebruik.

## Voorwaarden

Zorg ervoor dat je het volgende hebt voordat je begint:

1. Basiskennis van de programmeertaal Java.  
2. JDK (Java Development Kit) geïnstalleerd op je machine.  
3. Een IDE zoals Eclipse of IntelliJ IDEA.  
4. Aspose.Note for Java‑bibliotheek – download deze van [here](https://releases.aspose.com/note/java/).

## Importeer pakketten

Importeer eerst de benodigde Aspose.Note‑klassen en standaard Java I/O‑hulpmiddelen:

```java
import com.aspose.note.*;
import java.io.IOException;
```

## Stap 1: Laad het OneNote‑document

Hier wijzen we naar de map die het bron‑OneNote‑bestand (`Aspose.one`) bevat en laden het in een `Document`‑object. Dit object geeft je volledige toegang tot pagina's, secties en andere elementen binnen het notitieboek.

```java
// The path to the documents directory.
String dataDir = "Your Document Directory";

// Load the document into Aspose.Note.
Document oneFile = new Document(dataDir + "Aspose.one");
```

## Stap 2: Sla het document op als BMP‑afbeelding

We voegen de uitvoerbestandsnaam samen en roepen vervolgens `save` aan met een `ImageSaveOptions`‑instantie geconfigureerd voor **BMP** (`SaveFormat.Bmp`).  
Als je een **onenote‑pagina** als PNG wilt **opslaan**, vervang je eenvoudig `SaveFormat.Bmp` door `SaveFormat.Png`. Evenzo maakt `SaveFormat.Pdf` een **onenote‑naar‑pdf**‑conversie mogelijk.

```java
dataDir = dataDir + "SaveToBmpImageUsingImageSaveOptions_out.bmp";

// Save the document.
oneFile.save(dataDir, new ImageSaveOptions(SaveFormat.Bmp));
```

## Waarom BMP kiezen?

- **Lossless quality** – BMP slaat ruwe pixelgegevens op, waardoor de exacte weergave van de oorspronkelijke pagina behouden blijft.  
- **Compatibility** – Oudere Windows‑toepassingen vereisen vaak BMP‑bestanden.  
- **Simplicity** – Geen compressie‑artefacten, waardoor het ideaal is voor verdere beeldverwerking.

## Veelvoorkomende problemen & tips

- **File path errors** – Zorg ervoor dat `dataDir` eindigt met de juiste scheidingsteken (`/` of `\`).  
- **Large notebooks** – Voor zeer grote OneNote‑bestanden kun je overwegen elke pagina afzonderlijk op te slaan om het geheugenverbruik laag te houden.  
- **License exceptions** – Het uitvoeren van de code zonder een geldige licentie voegt een watermerk toe aan de gegenereerde afbeelding.

## Conclusie

In deze gids hebben we **hoe onenote**‑documenten op te slaan als BMP‑afbeeldingen met behulp van Aspose.Note for Java’s `ImageSaveOptions` gedemonstreerd. Door de `SaveFormat`‑enum te wisselen kun je ook PNG, JPEG, PDF of andere ondersteunde formaten genereren, waardoor je een flexibele manier hebt om OneNote‑inhoud te exporteren voor elke downstream‑situatie.

## Veelgestelde vragen

**Q1: Kan ik OneNote‑documenten opslaan in andere afbeeldingsformaten dan BMP?**  
A: Ja, je kunt `ImageSaveOptions` gebruiken met `SaveFormat.Png`, `SaveFormat.Jpeg`, `SaveFormat.Gif` of `SaveFormat.Tiff` om naar die formaten te exporteren.

**Q2: Ondersteunt Aspose.Note for Java conversie tussen verschillende documentformaten?**  
A: Absoluut. Naast afbeeldingsformaten kun je OneNote‑bestanden converteren naar PDF, DOCX, HTML en meer met de juiste `SaveFormat`.

**Q3: Is Aspose.Note for Java compatibel met de nieuwste versies van OneNote?**  
A: Ja, de bibliotheek wordt regelmatig bijgewerkt om in sync te blijven met de nieuwste OneNote‑releases.

**Q4: Kan ik de inhoud van OneNote‑documenten programmatisch manipuleren?**  
A: Ja, je kunt pagina's, secties en rijke inhoud (tekst, afbeeldingen, tabellen) toevoegen, bewerken of verwijderen via de API.

**Q5: Biedt Aspose.Note for Java technische ondersteuning?**  
A: Ja, Aspose biedt technische ondersteuning en een speciaal forum. Bezoek het [Aspose.Note forum](https://forum.aspose.com/c/note/28) voor hulp.

---

**Laatst bijgewerkt:** 2025-12-16  
**Getest met:** Aspose.Note for Java 24.12  
**Auteur:** Aspose

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
