---
date: 2025-12-18
description: Leer hoe u OneNote‑pagina’s kunt exporteren naar PDF met Aspose.Note
  voor Java. Kies splitsingsalgoritmen, stel paginaverdeling in en genereer eenvoudig
  PDF‑bestanden.
linktitle: Export OneNote Pages with Splitting Algorithm Method – Aspose.Note
second_title: Aspose.Note Java API
title: Export OneNote-pagina's met splitsingsalgoritme-methode – Aspose.Note
url: /nl/java/onenote-document-saving/use-splitting-algorithm-method/
weight: 26
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote-pagina's exporteren met Splitsingsalgoritme-methode – Aspose.Note

## Inleiding

Als je **OneNote-pagina's** programmatically wilt **exporteren** naar een PDF‑document, maakt Aspose.Note voor Java dit eenvoudig. In deze tutorial lopen we de Splitsingsalgoritme‑methode door, waarmee je kunt bepalen hoe inhoud over pagina's wordt verdeeld, zodat je een nette en goed leesbare PDF‑output krijgt. Je ziet hoe je de PDF‑opslaoptopties instelt, het juiste pagina‑splitsingsalgoritme kiest en uiteindelijk het PDF‑bestand genereert — allemaal met slechts een paar regels Java‑code.

## Snelle antwoorden
- **Wat doet het Splitsingsalgoritme?** Het bepaalt hoe objecten die over paginagrenzen heen lopen worden behandeld bij het exporteren van OneNote-pagina's naar PDF.  
- **Welke bibliotheek is vereist?** Aspose.Note voor Java (download van de officiële Aspose‑site).  
- **Heb ik een licentie nodig?** Een tijdelijke of volledige licentie is vereist voor productiegebruik; een gratis proefversie is beschikbaar.  
- **Kan ik grote OneNote-notitieblokken exporteren?** Ja – de bibliotheek verwerkt grote bestanden efficiënt en laat je paginaverdelingsregels instellen.  
- **Welke uitvoerformaten worden ondersteund?** PDF, JPEG, PNG, XPS en meer; deze gids richt zich op PDF‑export.

## Wat is **export onenote pages**?
Het exporteren van OneNote-pagina's betekent dat je het native `.one`‑bestandsformaat omzet naar een draagbaarder formaat zoals PDF. Dit is handig voor delen, archiveren of afdrukken van inhoud zonder dat de OneNote‑applicatie nodig is.

## Waarom het Splitsingsalgoritme gebruiken voor **export onenote pages**?
Het algoritme geeft je fijnmazige controle over hoe complexe objecten (tabellen, afbeeldingen, tekeningen) worden behandeld bij paginabreaks. Door het juiste algoritme te selecteren kun je:

* De visuele lay-out van elke pagina behouden.  
* Knippen van inhoud voorkomen die anders zou worden afgekapt.  
* Het aantal gegenereerde pagina's verminderen wanneer objecten netjes naar de volgende pagina kunnen worden verplaatst.  

## Vereisten

Voordat we beginnen, zorg dat je de volgende vereisten hebt:

1. Java Development Kit (JDK): Zorg dat je JDK op je systeem geïnstalleerd hebt. Je kunt het downloaden van de [website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).
2. Aspose.Note voor Java‑bibliotheek: Download en installeer de Aspose.Note voor Java‑bibliotheek via de [download‑link](https://releases.aspose.com/note/java/).

## Pakketten importeren

Importeer in je Java‑project de benodigde pakketten om de functionaliteit van Aspose.Note te gebruiken.

```java
import java.io.IOException;
import com.aspose.note.AlwaysSplitObjectsAlgorithm;
import com.aspose.note.Document;
import com.aspose.note.KeepPartAndCloneSolidObjectToNextPageAlgorithm;
import com.aspose.note.KeepSolidObjectsAlgorithm;
import com.aspose.note.PdfSaveOptions;
```

## Stap 1: Documentmap definiëren

Stel de map in waar je OneNote‑document zich bevindt.

```java
String dataDir = "Your Document Directory";
```

## Stap 2: Het OneNote‑document laden

Laad het OneNote‑document met behulp van de `Document`‑klasse van Aspose.Note.

```java
Document doc = new Document(dataDir + "Sample1.one");
```

## Stap 3: PDF‑opslaoptopties instellen

Maak een instantie van `PdfSaveOptions` om opties te specificeren voor het opslaan van het document als PDF. Hier stel je het **pagina‑splitsings**‑gedrag en andere PDF‑gerelateerde instellingen in.

```java
PdfSaveOptions pdfSaveOptions = new PdfSaveOptions();
```

## Stap 4: Paginaverdelingsalgoritme instellen

Kies het passende splitsingsalgoritme volgens je eisen. Hier gebruiken we `KeepPartAndCloneSolidObjectToNextPageAlgorithm`, dat een deel van een object op de huidige pagina behoudt en de rest kloont naar de volgende pagina.

```java
pdfSaveOptions.setPageSplittingAlgorithm(new KeepPartAndCloneSolidObjectToNextPageAlgorithm(100));
```

## Stap 5: Het document opslaan

Sla het document op met de opgegeven PDF‑opslaoptopties. Deze stap **genereert PDF onenote**‑output die je kunt openen, delen of afdrukken.

```java
try {
    doc.save(dataDir + "UsingSplittingAlgorithmMethod_out.Jpeg", pdfSaveOptions);
} catch (Exception ex) {
    System.out.println("Exception: " + ex.getMessage());
}
```

## Veelvoorkomende problemen en oplossingen

| Probleem | Oplossing |
|----------|-----------|
| **Objecten worden afgekapt bij paginagrenzen** | Probeer een ander algoritme zoals `AlwaysSplitObjectsAlgorithm` of verhoog de drempelwaarde in `KeepPartAndCloneSolidObjectToNextPageAlgorithm`. |
| **Uitvoer‑PDF is leeg** | Controleer of het bron‑`.one`‑bestand niet corrupt is en of het `dataDir`‑pad correct is. |
| **Prestaties zijn traag bij grote notitieblokken** | Gebruik `pdfSaveOptions.setCompressImages(true)` om het geheugenverbruik te verlagen, en overweeg het notitieblok in kleinere secties te verwerken. |

## Veelgestelde vragen

**Q: Kan ik Aspose.Note voor Java gebruiken met andere programmeertalen?**  
A: Ja, Aspose.Note is ook beschikbaar voor .NET, C++ en Python.

**Q: Is Aspose.Note geschikt voor het verwerken van grote OneNote‑bestanden?**  
A: Absoluut. De bibliotheek is geoptimaliseerd voor efficiënte verwerking van grote notitieblokken.

**Q: Waar vind ik extra bronnen en ondersteuning voor Aspose.Note?**  
A: Je kunt de [documentatie](https://reference.aspose.com/note/java/) en het [forum](https://forum.aspose.com/c/note/28) raadplegen voor ondersteuning en begeleiding.

**Q: Kan ik Aspose.Note eerst uitproberen voordat ik het koop?**  
A: Ja, je kunt een [gratis proefversie](https://releases.aspose.com/) gebruiken om de functies te verkennen voordat je een aankoop doet.

**Q: Hoe kan ik een tijdelijke licentie voor Aspose.Note verkrijgen?**  
A: Je kunt een [tijdelijke licentie](https://purchase.aspose.com/temporary-license/) aanvragen om het product gedurende een proefperiode te evalueren.

---

**Laatst bijgewerkt:** 2025-12-18  
**Getest met:** Aspose.Note 24.12 voor Java  
**Auteur:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}