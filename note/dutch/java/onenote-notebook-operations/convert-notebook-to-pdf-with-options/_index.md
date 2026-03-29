---
date: 2026-03-29
description: Converteer OneNote-notitieblokken naar PDF met opties, sla het notitieblok
  op als PDF en voeg een PDF-kop- en voettekst toe met Aspose.Note voor Java.
linktitle: Convert Notebook to PDF with Options in OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: Converteer OneNote naar PDF met opties - Aspose.Note
url: /nl/java/onenote-notebook-operations/convert-notebook-to-pdf-with-options/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote converteren naar PDF met opties met Aspose.Note

## Introductie

In deze tutorial leer je hoe je **convert onenote to pdf** kunt uitvoeren met volledige controle over de output. Aspose.Note for Java maakt het eenvoudig om OneNote-notebooks te exporteren naar PDF, zodat je **save notebook as pdf** kunt doen terwijl je kopteksten, voetteksten en paginaverdeling aanpast. Of je nu rapporten moet genereren, notulen moet archiveren, of inhoud wilt delen met gebruikers die geen OneNote hebben, deze gids leidt je stap voor stap.

## Snelle antwoorden

- **Welke bibliotheek verwerkt de conversie?** Aspose.Note for Java.
- **Kan ik een koptekst of voettekst toevoegen aan de PDF?** Ja – gebruik PDF‑opslaanopties om aangepaste kopteksten/voetteksten in te voegen.
- **Heb ik een licentie nodig voor productie?** Een commerciële licentie is vereist voor niet‑trial gebruik.
- **Welke Java‑versies worden ondersteund?** Java 8 en later.
- **Hoe lang duurt de conversie?** Meestal enkele seconden voor notebooks van gemiddelde grootte.

## Wat is “convert onenote to pdf”?

OneNote naar PDF converteren betekent dat je een OneNote-notebook (het *.onetoc2*-bestand) neemt en elke pagina rendert als een PDF‑pagina. De resulterende PDF behoudt tekst, afbeeldingen en lay-out, waardoor deze op elk apparaat kan worden bekeken zonder OneNote.

## Waarom Aspose.Note gebruiken om onenote notebook pdf te exporteren?

- **Geen Office‑installatie vereist** – de API werkt zelfstandig.
- **Fijne controle** – je kunt paginaverdelingsalgoritmen instellen, lettertypen insluiten en kopteksten/voetteksten toevoegen.
- **Hoge getrouwheid** – het visuele uiterlijk van het originele notebook wordt behouden.
- **Cross‑platform** – werkt op Windows, Linux en macOS met elke Java‑runtime.

## Vereisten

Voordat we beginnen, zorg ervoor dat je de volgende vereisten hebt:

1. Java Development Kit (JDK) – JDK 8 of nieuwer geïnstalleerd.
2. Aspose.Note for Java – download en installeer vanaf de [download link](https://releases.aspose.com/note/java/).
3. IDE (Integrated Development Environment) – IntelliJ IDEA, Eclipse of NetBeans zijn populaire keuzes.

## Pakketten importeren

Eerst moet je de benodigde pakketten importeren in je Java‑project. Deze pakketten leveren de klassen en methoden die nodig zijn voor het werken met OneNote‑documenten.

```java
import com.aspose.note.Notebook;
import java.io.IOException;
import com.aspose.note.KeepSolidObjectsAlgorithm;
import com.aspose.note.Notebook;
import com.aspose.note.NotebookPdfSaveOptions;
import com.aspose.note.PdfSaveOptions;
```

## Stap 1: Laad het OneNote Notebook

Om **convert onenote to pdf** uit te voeren, moet je eerst het OneNote‑notebook laden. Zorg ervoor dat het pad naar het notebook‑bestand correct is opgegeven.

```java
String dataDir = "Your Document Directory";
// Load a OneNote Notebook
Notebook notebook = new Notebook(dataDir + "Notizbuch �ffnen.onetoc2");
```

## Stap 2: Specificeer PDF Save Options

Aspose.Note biedt verschillende opties voor het aanpassen van de PDF‑output. Je kunt opties specificeren zoals paginaverdelingsalgoritmen, koptekst/voettekst‑instellingen en meer.

```java
// Specify PDF save options
NotebookPdfSaveOptions notebookSaveOptions = new NotebookPdfSaveOptions();
PdfSaveOptions documentSaveOptions = notebookSaveOptions.getDocumentSaveOptions();
documentSaveOptions.setPageSplittingAlgorithm(new KeepSolidObjectsAlgorithm());
```

## Stap 3: Sla het Notebook op als PDF

Zodra je het notebook hebt geladen en de opslaanopties hebt gespecificeerd, is het tijd om **save the notebook as pdf**.

```java
dataDir = dataDir + "ExportNotebooktoPDFwithOptions_out.pdf";
// Save the Notebook
notebook.save(dataDir, notebookSaveOptions);
```

## Veelvoorkomende problemen en oplossingen

| Probleem | Oorzaak | Oplossing |
|----------|---------|-----------|
| PDF mist afbeeldingen | Afbeeldingen opgeslagen als ingesloten objecten niet geladen | Zorg ervoor dat het notebook‑bestand en alle gekoppelde bronnen zich in dezelfde map bevinden voordat je laadt. |
| Koptekst/voettekst verschijnt niet | Koptekst/voettekst‑opties niet ingesteld in `PdfSaveOptions` | Gebruik `documentSaveOptions.setHeaderFooter()` om de inhoud te definiëren vóór het opslaan. |
| Geheugenfout bij grote notebooks | Volledig notebook in het geheugen geladen | Verwerk het notebook in secties of vergroot de JVM‑heap‑grootte (`-Xmx2g`). |

## Veelgestelde vragen

### Q1: Kan ik het uiterlijk van de PDF output aanpassen?

A1: Ja, Aspose.Note biedt verschillende opties om de PDF‑output aan te passen, inclusief koptekst/voettekst‑instellingen, paginaverdelingsalgoritmen en meer.

### Q2: Is Aspose.Note compatibel met alle versies van OneNote?

A2: Aspose.Note ondersteunt Microsoft OneNote 2010 en latere versies.

### Q3: Biedt Aspose.Note een gratis proefversie?

A3: Ja, je kunt een gratis proefversie van Aspose.Note downloaden via [hier](https://releases.aspose.com/).

### Q4: Waar kan ik documentatie voor Aspose.Note vinden?

A4: Je kunt uitgebreide documentatie voor Aspose.Note vinden via [hier](https://reference.aspose.com/note/java/).

### Q5: Hoe kan ik ondersteuning voor Aspose.Note krijgen?

A5: Voor technische assistentie of vragen kun je het Aspose.Note‑ondersteuningsforum bezoeken via [hier](https://forum.aspose.com/c/note/28).

## Aanvullende veelgestelde vragen

**Q: Hoe voeg ik een aangepaste PDF‑koptekst of -voettekst toe?**  
A: Maak een `PdfHeaderFooterOptions`‑object, configureer de tekst of afbeeldingen, en wijs het toe aan `documentSaveOptions.setHeaderFooterOptions()` voordat je `save` aanroept.

**Q: Kan ik alleen geselecteerde secties van een notebook exporteren?**  
A: Ja – laad het notebook, haal de gewenste `Section`‑objecten op, en roep `section.save()` aan met dezelfde PDF‑opties.

**Q: Is het mogelijk om de gegenereerde PDF te versleutelen?**  
A: Absoluut. Gebruik `documentSaveOptions.setEncryptionPassword("yourPassword")` om de PDF te beveiligen.

**Q: Welke prestatie‑overwegingen moet ik in gedachten houden?**  
A: Voor zeer grote notebooks, overweeg het streamen van de output naar een `FileOutputStream` en vergroot de JVM‑heap‑grootte als je een `OutOfMemoryError` tegenkomt.

---

**Laatst bijgewerkt:** 2026-03-29  
**Getest met:** Aspose.Note for Java 24.12  
**Auteur:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}