---
date: 2025-12-28
description: Leer hoe u OneNote naar PDF kunt exporteren met volledige controle met
  Aspose.Note voor Java. Inclusief exportopties voor OneNote-notitieboek naar PDF
  en een Java-gids voor het converteren van een notitieboek naar PDF.
linktitle: How to Export OneNote to PDF with Options – Convert Notebook to PDF using
  Aspose.Note
second_title: Aspose.Note Java API
title: Hoe OneNote naar PDF exporteren met opties – Notebook converteren naar PDF
  met Aspose.Note
url: /nl/java/onenote-notebook-operations/convert-notebook-to-pdf-with-options/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hoe OneNote exporteren naar PDF met opties – Aspose.Note Java API

## Introductie

In deze tutorial leer je **hoe je OneNote exporteert naar PDF** met aanpasbare opties met behulp van Aspose.Note voor Java. Het converteren van een OneNote-notitieboek naar PDF is een veelvoorkomende behoefte—of je nu vergadernotities wilt delen, documentatie wilt archiveren of afdrukbare rapporten wilt genereren. Met Aspose.Note is het proces eenvoudig, volledig programmeerbaar en biedt het fijne controle over de resulterende PDF.

## Snelle antwoorden
- **Wat doet de API?** Het laadt een OneNote-notitieboek en slaat het op als PDF met optionele instellingen.  
- **Welke taal wordt gebruikt?** Java – perfect voor server‑side of desktop‑applicaties.  
- **Heb ik een licentie nodig?** Een gratis proefversie werkt voor ontwikkeling; een commerciële licentie is vereist voor productie.  
- **Kan ik de paginalay-out regelen?** Ja, je kunt paginaverdelingsalgoritmen, kop‑ en voetteksten en meer instellen.  
- **Is het code‑voorbeeld uitvoerbaar?** Absoluut – vervang alleen het tijdelijke pad door de locatie van jouw notitieboek.

## Wat betekent “hoe OneNote exporteren naar PDF”?

OneNote exporteren naar PDF houdt in dat het native OneNote-notitieboek (`*.onetoc2` en gerelateerde sectiebestanden) wordt omgezet naar een draagbaar, vaste‑lay‑out PDF‑document. Deze conversie behoudt opmaak, afbeeldingen en ingesloten objecten, terwijl de inhoud op elk apparaat kan worden bekeken zonder OneNote.

## Waarom Aspose.Note voor Java gebruiken?

- **Geen afhankelijkheid van Microsoft Office** – werkt op elk platform dat Java ondersteunt.  
- **Rijke PDF‑opties** – beheer paginaverdeling, kop‑/voetteksten en objectafhandeling.  
- **Hoge getrouwheid** – de PDF‑output komt sterk overeen met het oorspronkelijke OneNote‑uiterlijk.  
- **Schaalbaar** – geschikt voor batchverwerking van duizenden notitieboeken.

## Voorvereisten

Voordat we beginnen, zorg dat je het volgende hebt:

1. **Java Development Kit (JDK)** – versie 8 of hoger.  
2. **Aspose.Note voor Java** – download het via de [download link](https://releases.aspose.com/note/java/).  
3. **Een IDE** – IntelliJ IDEA, Eclipse of NetBeans (jouw keuze).  
4. **Een OneNote-notitieboek** dat je wilt converteren (bijv. `Notizbuch öffnen.onetoc2`).

## Importpakketten

Importeer eerst de klassen die notitieboekverwerking en PDF‑opslaan mogelijk maken.

```java
import com.aspose.note.Notebook;
import java.io.IOException;
import com.aspose.note.KeepSolidObjectsAlgorithm;
import com.aspose.note.Notebook;
import com.aspose.note.NotebookPdfSaveOptions;
import com.aspose.note.PdfSaveOptions;
```

## Stap 1: Het OneNote‑notitieboek laden

Laad het notitieboekbestand vanaf de schijf. Vervang `Your Document Directory` door de werkelijke map die jouw `.onetoc2`‑bestand bevat.

```java
String dataDir = "Your Document Directory";
// Load a OneNote Notebook
Notebook notebook = new Notebook(dataDir + "Notizbuch �ffnen.onetoc2");
```

## Stap 2: PDF‑opslaan‑opties specificeren

Hier definieer je hoe de PDF moet worden gegenereerd. Het voorbeeld stelt een paginaverdelingsalgoritme in dat solide objecten bij elkaar houdt, wat nuttig is bij diagrammen of tabellen die op dezelfde pagina moeten blijven.

```java
// Specify PDF save options
NotebookPdfSaveOptions notebookSaveOptions = new NotebookPdfSaveOptions();
PdfSaveOptions documentSaveOptions = notebookSaveOptions.getDocumentSaveOptions();
documentSaveOptions.setPageSplittingAlgorithm(new KeepSolidObjectsAlgorithm());
```

## Stap 3: Het notitieboek opslaan als PDF

Schrijf tenslotte het notitieboek weg als een PDF‑bestand. Het uitvoerpad kan elke gewenste locatie zijn.

```java
dataDir = dataDir + "ExportNotebooktoPDFwithOptions_out.pdf";
// Save the Notebook
notebook.save(dataDir, notebookSaveOptions);
```

## Veelvoorkomende problemen en oplossingen

| Probleem | Waarom het gebeurt | Oplossing |
|----------|--------------------|-----------|
| **Bestand niet gevonden** | Onjuiste `dataDir` of bestandsnaam. | Controleer het pad en zorg dat het notitieboekbestand bestaat. |
| **Ontbrekende lettertypen** | PDF‑rendering heeft dezelfde lettertypen nodig als OneNote. | Installeer de vereiste lettertypen op de server of embed ze via extra Aspose‑opties. |
| **Grote notitieboeken veroorzaken OutOfMemoryError** | Het volledige notitieboek wordt in het geheugen geladen. | Verwerk secties afzonderlijk of vergroot de JVM‑heapgrootte (`-Xmx`). |

## Conclusie

We hebben stap voor stap **hoe OneNote exporteren naar PDF** behandeld met Aspose.Note voor Java, van het laden van het notitieboek, het configureren van PDF‑opties tot het opslaan van het resultaat. Door deze stappen te volgen kun je notitieboek‑naar‑PDF‑conversie integreren in elke Java‑applicatie, of het nu een desktop‑tool, een webservice of een batch‑verwerkingsbackend is.

## Veelgestelde vragen

### Q1: Kan ik het uiterlijk van de PDF‑output aanpassen?

A1: Ja, Aspose.Note biedt diverse opties voor het aanpassen van de PDF‑output, inclusief kop‑/voettekstinstellingen, paginaverdelingsalgoritmen en meer.

### Q2: Is Aspose.Note compatibel met alle versies van OneNote?

A2: Aspose.Note ondersteunt Microsoft OneNote 2010 en latere versies.

### Q3: Biedt Aspose.Note een gratis proefversie?

A3: Ja, je kunt een gratis proefversie van Aspose.Note downloaden [hier](https://releases.aspose.com/).

### Q4: Waar vind ik documentatie voor Aspose.Note?

A4: Je kunt uitgebreide documentatie voor Aspose.Note vinden [hier](https://reference.aspose.com/note/java/).

### Q5: Hoe kan ik ondersteuning krijgen voor Aspose.Note?

A5: Voor technische assistentie of vragen kun je het Aspose.Note‑ondersteuningsforum bezoeken [hier](https://forum.aspose.com/c/note/28).

## Extra veelgestelde vragen

**Q: Hoe exporteer ik een OneNote‑notitieboek naar PDF zonder afbeeldingen te verliezen?**  
A: Zorg dat `KeepSolidObjectsAlgorithm` is ingesteld (zoals getoond) en dat de afbeeldingsbestanden van het bron‑notitieboek toegankelijk zijn in dezelfde map.

**Q: Kan ik meerdere notitieboeken in één keer batch‑converteren?**  
A: Ja. Loop door een lijst met notitieboek‑paden, instantiate een `Notebook` voor elk, pas dezelfde `NotebookPdfSaveOptions` toe en roep `save()` aan.

**Q: Is er een manier om PDF‑metadata (auteur, titel) in te stellen tijdens de conversie?**  
A: Gebruik `PdfSaveOptions.setMetadata()` om auteur, titel, onderwerp en trefwoorden te definiëren vóór het opslaan.

**Q: Ondersteunt de API wachtwoord‑beveiligde PDF‑bestanden?**  
A: Je kunt een wachtwoord instellen op de `PdfSaveOptions` via `setEncryptionPassword()` nadat je andere opties hebt geconfigureerd.

**Q: Welke versie van Aspose.Note werd gebruikt voor deze tutorial?**  
A: De code is getest met Aspose.Note voor Java 23.12.

---

**Laatst bijgewerkt:** 2025-12-28  
**Getest met:** Aspose.Note voor Java 23.12  
**Auteur:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}