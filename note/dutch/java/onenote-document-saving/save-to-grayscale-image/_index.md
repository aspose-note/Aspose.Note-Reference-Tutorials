---
date: 2026-06-30
description: Leer hoe u OneNote kunt exporteren door een document op te slaan als
  een grijswaarden PNG-afbeelding met behulp van Aspose.Note voor Java. Bevat stappen
  om een OneNote-document te laden en een grijswaardenafbeelding te maken.
keywords:
- how to export onenote
- adjust image resolution
- reduce onenote size
- create grayscale png
- grayscale conversion java
linktitle: Hoe OneNote exporteren als grijswaardenafbeelding – Aspose.Note
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
title: Hoe OneNote exporteren als grijswaardenafbeelding – Aspose.Note
url: /nl/java/onenote-document-saving/save-to-grayscale-image/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Opslaan als Grijswaardenafbeelding in OneNote - Aspose.Note

## Inleiding

In deze tutorial ontdek je **hoe onenote te exporteren** door een OneNote `.one`-bestand te converteren naar een hoogwaardige grijswaarden PNG-afbeelding met behulp van Aspose.Note voor Java. Grijswaardenconversie is vaak nodig voor Java‑ontwikkelaars voor afdrukken, archivering, of om **OneNote-grootte te verkleinen** zonder essentiële inhoud te verliezen. We lopen door het laden van een OneNote‑document, het configureren van de opslaan‑opties—incl. **afbeeldingsresolutie aanpassen**—en tenslotte het opslaan van het document als PNG.

## Snelle Antwoorden
- **Wat betekent “hoe onenote te exporteren”?** Het verwijst naar het programmatisch converteren van een OneNote‑bestand naar een ander formaat, zoals een afbeelding, met behulp van code.  
- **Welk formaat is het beste voor grijswaardenoutput?** PNG werkt goed omdat het verlies‑vrije kwaliteit behoudt en een dedicated grijswaardenkleurmodus ondersteunt.  
- **Heb ik een licentie nodig?** Een geldige Aspose.Note‑licentie is vereist voor productiegebruik; een tijdelijke proeflicentie is beschikbaar voor testen.  
- **Welke Java‑versie is vereist?** Java 8 of hoger wordt aanbevolen.  
- **Kan ik de afbeeldingsgrootte wijzigen?** Ja, je kunt de `ImageSaveOptions`‑eigenschappen zoals `Resolution` of `PageSize` aanpassen vóór het opslaan.  

## Wat is “hoe onenote te exporteren”?

Exporteren van OneNote betekent het programmatisch converteren van een OneNote `.one`‑bestand naar een andere representatie—zoals PDF, HTML of een afbeelding. In deze gids richten we ons op **het maken van grijswaarden‑PNG**‑afbeeldingen, een veelvoorkomende vereiste voor documentatie of print‑klare workflows. Met Aspose.Note gebeurt de conversie volledig in het geheugen, zodat je nooit Microsoft OneNote op de server hoeft te installeren.

## Waarom OneNote exporteren als een grijswaardenafbeelding?

Grijswaarden‑PNGs zijn doorgaans **30‑40 % kleiner** dan hun full‑color tegenhangers, wat de weblevering versnelt en opslagkosten verlaagt. Ze bieden ook **duidelijker contrast** op laserprinters, waardoor rapporten makkelijker leesbaar zijn. Omdat PNG universeel wordt ondersteund, werken de resulterende bestanden op browsers, mobiele apparaten en desktop‑editors zonder extra codecs.

## Vereisten

1. Java Development Kit (JDK) 8 of nieuwer geïnstalleerd.  
2. Aspose.Note for Java‑bibliotheek – download de nieuwste release van [hier](https://releases.aspose.com/note/java/).  
3. Een basisbegrip van Java‑syntaxis en Maven/Gradle projectopzet.  

## Pakketten Importeren

De `ImageSaveOptions`‑klasse bepaalt hoe het document wordt gerenderd naar een afbeelding.  
`ColorMode` is een enumeratie die je in staat stelt te schakelen tussen full‑color en grijswaardenoutput.

```java
import com.aspose.note.ColorMode;
import com.aspose.note.Document;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.SaveFormat;
import java.io.IOException;
```

## Stap 1: Laad het OneNote‑document

`Document` vertegenwoordigt een OneNote‑notebook en biedt methoden om de inhoud te laden, bewerken en opslaan. Eerst, **laad het OneNote‑document** in Aspose.Note. Vervang `"Your Document Directory"` door het pad naar je lokale map en `"Aspose.one"` door de naam van je OneNote‑bestand.

```java
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Aspose.one");
```

## Stap 2: Stel Uitvoerpad en Opties In

`ImageSaveOptions` configureert hoe een OneNote‑document wordt gerenderd naar een afbeeldingsbestand. De `ColorMode`‑enumeratie selecteert de kleurweergavemodus, zoals grijswaarden of full‑color. Definieer het uitvoerpad voor de grijswaardenafbeelding en specificeer de opslaan‑opties. We stellen de `ColorMode` in op `GrayScale` en gebruiken het **opslaan van document als PNG**‑formaat. Je kunt ook **afbeeldingsresolutie aanpassen** naar 300 DPI voor prints van hoge kwaliteit.

```java
dataDir = dataDir + "SaveAsGrayscaleImage_out.png";
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);
options.setColorMode(ColorMode.GrayScale);
```

## Stap 3: Sla het Document Op

Tot slot, sla het document op als een grijswaarden‑PNG‑afbeelding met behulp van de geconfigureerde opties. De `save`‑methode schrijft het bestand naar schijf zonder dat er tijdelijke tussenbestanden nodig zijn.

```java
oneFile.save(dataDir, options);
```

## Veelvoorkomende Problemen en Oplossingen
- **FileNotFoundException** – Controleer of `dataDir` naar de juiste map wijst en dat het `.one`‑bestand bestaat.  
- **LicenseException** – Zorg ervoor dat je een geldige Aspose.Note‑licentie hebt toegepast vóór het aanroepen van `save`.  
- **Low‑resolution output** – Pas `options.setResolution(300)` aan om de DPI te verhogen; een hogere DPI levert scherpere prints op maar grotere bestandsgroottes.  

## Veelgestelde Vragen

**Q1: Kan ik de grijswaardenafbeelding in een ander formaat opslaan?**  
A1: Ja, wijzig simpelweg de `SaveFormat`‑parameter in de `ImageSaveOptions`‑constructor naar `Jpeg`, `Bmp`, of een van de meer dan 20 ondersteunde beeldformaten.

**Q2: Is Aspose.Note compatibel met alle versies van OneNote‑documenten?**  
A2: Aspose.Note ondersteunt Microsoft OneNote 2010 en later, en dekt meer dan 95 % van de notebooks die vandaag actief worden gebruikt.

**Q3: Vereist Aspose.Note een licentie om te gebruiken?**  
A3: Een geldige licentie is vereist voor productiegebruik, maar een tijdelijke proeflicentie kan gratis worden verkregen voor evaluatie.

**Q4: Kan ik andere aspecten van het document manipuleren voordat ik het als afbeelding opsla?**  
A4: Zeker! Aspose.Note biedt API's om secties, pagina's en individuele elementen zoals tekst, tabellen en afbeeldingen te bewerken vóór export.

**Q5: Waar kan ik ondersteuning vinden als ik problemen tegenkom?**  
A5: Je kunt ondersteuning vinden op het Aspose.Note‑forum [hier](https://forum.aspose.com/c/note/28).

## Conclusie

Je hebt nu geleerd **hoe onenote te exporteren** door een OneNote‑bestand te laden, de opslaan‑opties te configureren om **een grijswaardenafbeelding te maken**, en **het document als PNG op te slaan**. Deze aanpak is ideaal voor het genereren van lichtgewicht, print‑klare visuals uit OneNote‑notebooks. Voel je vrij om te experimenteren met andere `ColorMode`‑instellingen, hogere DPI‑waarden, of alternatieve beeldformaten om aan de eisen van je project te voldoen.

---

**Laatst bijgewerkt:** 2026-06-30  
**Getest met:** Aspose.Note 27.0 for Java  
**Auteur:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Gerelateerde Tutorials

- [Export OneNote-pagina naar PNG-afbeelding in Java met Aspose.Note](/note/java/onenote-document-loading/convert-page-to-png-image/)
- [aspnote stel jpeg-resolutie in – Stel Uitvoerbeeldresolutie in OneNote in - Aspose.Note](/note/java/onenote-document-saving/set-output-image-resolution/)
- [Hoe OneNote op te slaan als PDF met Aspose.Note voor Java](/note/java/onenote-document-loading/load-save-format/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}