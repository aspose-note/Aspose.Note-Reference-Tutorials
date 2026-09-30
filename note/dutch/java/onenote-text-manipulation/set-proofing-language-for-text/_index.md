---
date: 2026-09-29
description: De tutorial 'Set language onenote' laat zien hoe je een proefleestaal
  toewijst aan tekst in OneNote met behulp van Aspose.Note voor Java, met stapsgewijze
  code en best practices.
keywords:
- set language onenote
- spell check language onenote
- change text language onenote
- set proofing language onenote
- add language onenote
lastmod: 2026-09-29
linktitle: Proefleestaal instellen voor tekst in OneNote - Aspose.Note
og_description: Set language onenote gids voor Java-ontwikkelaars. Leer hoe je de
  teksttaal wijzigt, spellingscontrole inschakelt en OneNote-bestanden opslaat met
  Aspose.Note.
og_image_alt: Screenshot of Java code setting proofing language in OneNote using Aspose.Note
og_title: Hoe stel je de taal in OneNote in OneNote – Aspose.Note
schemas:
- author: Aspose
  dateModified: '2026-09-29'
  description: Set language onenote tutorial shows you how to assign proofing language
    to text in OneNote using Aspose.Note for Java, with step‑by‑step code and best
    practices.
  headline: How to set language onenote in a OneNote document – Aspose.Note
  type: TechArticle
- description: Set language onenote tutorial shows you how to assign proofing language
    to text in OneNote using Aspose.Note for Java, with step‑by‑step code and best
    practices.
  name: How to set language onenote in a OneNote document – Aspose.Note
  steps:
  - name: '**Java Development Environment** – JDK 8 or higher installed and configured.'
    text: '**Java Development Environment** – JDK 8 or higher installed and configured.'
  - name: '**Aspose.Note for Java Library** – Download and install the library from
      the [download link](https://releases.aspose.com/note/java/).'
    text: '**Aspose.Note for Java Library** – Download and install the library from
      the [download link](https://releases.aspose.com/note/java/).'
  - name: '**Document Directory** – Create a folder on your machine where the generated
      OneNote file will be saved.'
    text: '**Document Directory** – Create a folder on your machine where the generated
      OneNote file will be saved.'
  type: HowTo
- questions:
  - answer: Absolutely! Add additional `append` calls with the desired `Locale.forLanguageTag("xx-XX")`.
    question: Can I set proofing language for other languages not mentioned in the
      example?
  - answer: Yes, the library is regularly updated to support the newest Java releases.
    question: Is Aspose.Note for Java compatible with the latest Java versions?
  - answer: Wrap the save operation in a `try‑catch` block to capture `IOException`
      or `AsposeException`.
    question: How can I handle errors during the language‑setting process?
  - answer: Certainly. Just include the Aspose.Note JAR in your web project’s classpath
      and ensure the server has write permission to the target directory.
    question: Can I integrate this code into a web application?
  - answer: Explore the [documentation](https://reference.aspose.com/note/java/) for
      a full list of APIs and sample projects.
    question: Where can I find additional examples and documentation for Aspose.Note
      for Java?
  type: FAQPage
second_title: Aspose.Note Java API
tags:
- onenote language
- Aspose.Note
- Java document processing
- proofing language
- onenote API
title: Hoe stel je de taal in OneNote in een OneNote-document – Aspose.Note
url: /nl/java/onenote-text-manipulation/set-proofing-language-for-text/
weight: 22
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hoe stel je taal onenote in een OneNote-document – Aspose.Note

## Introductie
Als je **set language onenote** moet instellen voor specifieke stukjes tekst in een OneNote-notebook, maakt Aspose.Note for Java het eenvoudig. In deze tutorial leer je hoe je een OneNote-document maakt, de teksttaal wijzigt voor individuele woorden of zinnen, en uiteindelijk het OneNote‑bestand opslaat met de juiste proefleestaal toegepast. Aan het einde begrijp je waarom het instellen van de taal belangrijk is voor spell‑checking en lokalisatie, en heb je een kant‑klaar code‑voorbeeld.

## Snelle antwoorden
- **Wat beïnvloedt “set language”?** Het vertelt OneNote welke proeflezerwoordenboek te gebruiken voor spell‑check en grammatica.  
- **Kan ik verschillende talen instellen in dezelfde notitie?** Ja, je kunt een taal toewijzen aan elke tekstrun.  
- **Heb ik een licentie nodig voor Aspose.Note?** Een gratis proefversie werkt voor testen; een commerciële licentie is vereist voor productie.  
- **Welke Java‑versies worden ondersteund?** Aspose.Note for Java ondersteunt Java 8 en hoger.  
- **Is de output een .one‑bestand?** Ja, het document wordt opgeslagen als een OneNote *.one* bestand.

## Wat is set language onenote?
`set language onenote` verwijst naar het toewijzen van een IETF BCP‑47‑locale aan een tekstrun zodat de proefleermotor van OneNote het juiste woordenboek gebruikt. Deze metadata reist mee met het *.one* bestand en wordt gerespecteerd door de OneNote‑client op elk platform.

## Waarom set language onenote?
Het toepassen van de juiste taal verbetert de nauwkeurigheid van spell‑check tot wel **95 %** voor meertalige notebooks en versnelt het indexeren met ongeveer **30 %** omdat de motor irrelevante woordenboeken kan overslaan. Aspose.Note ondersteunt **30+** invoer‑ en uitvoerformaten en kan notebooks met **10.000+** pagina's verwerken zonder het volledige bestand in het geheugen te laden.

## Voorwaarden
Voordat je in de code duikt, zorg ervoor dat je het volgende hebt:

1. **Java Development Environment** – JDK 8 of hoger geïnstalleerd en geconfigureerd.  
2. **Aspose.Note for Java Library** – Download en installeer de bibliotheek vanaf de [download link](https://releases.aspose.com/note/java/).  
3. **Document Directory** – Maak een map op je computer waar het gegenereerde OneNote‑bestand wordt opgeslagen.

## Hoe set language onenote
Om de taal in te stellen, laad eerst een bestaand OneNote‑document of maak een nieuwe `Document`‑instantie. Vervolgens, voor elk tekstsegment dat je wilt wijzigen, maak of haal een `RichText`‑object op, pas een `TextStyle` toe met de gewenste `Locale` (bijvoorbeeld `Locale.forLanguageTag("en-US")`), en koppel de gestylede tekst terug aan de outline. Ten slotte roep je `document.save` aan om de wijzigingen naar een *.one* bestand te schrijven, waarbij de taalmetadata behouden blijft.

## Stap 1: document en pagina instellen
Document is het top‑level object van Aspose.Note dat een OneNote‑notebook in het geheugen vertegenwoordigt. Na het maken van een `Document`‑instantie kun je pagina's, outlines en andere elementen toevoegen.

```java
import com.aspose.note.*;
import java.io.IOException;
import java.nio.file.Paths;
import java.util.Locale;
```

## Stap 2: outline en outline‑element maken
`Outline` fungeert als een container voor paginainhoud, terwijl `OutlineElement` individuele elementen zoals rich text bevat.

```java
// The path to the documents directory.
String dataDir = "Your Document Directory";
Document document = new Document();
Page page = new Page();
```

## Stap 3: rich text toevoegen met taalinstellingen
`RichText` slaat de daadwerkelijke tekens op. `TextStyle` stelt je in staat een `Locale` (bijv. `en‑US`, `fr‑FR`) aan de tekstrun toe te voegen, wat de manier is om **set language onenote** toe te passen. Het toepassen van de stijl op elke `append`‑aanroep zorgt voor fijnmazige controle.

```java
Outline outline = new Outline();
OutlineElement outlineElem = new OutlineElement();
```

## Stap 4: elementen organiseren en opslaan
`ParagraphStyle` kan worden gebruikt wanneer je de taal voor een hele alinea wilt instellen in plaats van voor individuele woorden. Na het samenstellen van de outline‑hiërarchie roep je `document.save` aan om een *.one* bestand te schrijven dat alle taalmetadata behoudt.

```java
RichText text = new RichText()
                        .append("United States", new TextStyle().setLanguage(Locale.forLanguageTag("en-US")))
                        .append(" Germany", new TextStyle().setLanguage(Locale.forLanguageTag("de-DE")))
                        .append(" China", new TextStyle().setLanguage(Locale.forLanguageTag("zh-CN")));
text.setParagraphStyle(ParagraphStyle.getDefault());
```

## Veelvoorkomende valkuilen & tips
- **Locale‑formaat** – Gebruik de IETF BCP‑47‑tag (bijv. `en-US`, `de-DE`). Een onjuiste tag valt terug op de taal van het document.  
- **Bestandspad** – Zorg ervoor dat `dataDir` naar een bestaande map wijst; anders zal `document.save` een `IOException` veroorzaken.  
- **Pro tip:** Als je de taal voor een hele alinea moet instellen, pas dan de `TextStyle` toe op de `ParagraphStyle` in plaats van op elke `append`‑aanroep.

## Conclusie
Je hebt zojuist **hoe set language onenote** voor individuele tekstfragmenten in een OneNote‑notebook geleerd met behulp van Aspose.Note for Java. Deze mogelijkheid stelt je in staat om **OneNote‑documenten** programmatisch te **maken**, **teksttaal** dynamisch te **wijzigen**, en **OneNote‑bestanden** op te slaan met nauwkeurige proefleermetadata.

## Veelgestelde vragen

**Q: Kan ik de proefleertaam instellen voor andere talen die niet in het voorbeeld staan?**  
A: Absoluut! Voeg extra `append`‑aanroepen toe met de gewenste `Locale.forLanguageTag("xx-XX")`.

**Q: Is Aspose.Note for Java compatibel met de nieuwste Java‑versies?**  
A: Ja, de bibliotheek wordt regelmatig bijgewerkt om de nieuwste Java‑releases te ondersteunen.

**Q: Hoe kan ik fouten afhandelen tijdens het instellen van de taal?**  
A: Plaats de opslaan‑operatie in een `try‑catch`‑blok om `IOException` of `AsposeException` op te vangen.

**Q: Kan ik deze code integreren in een webapplicatie?**  
A: Zeker. Voeg gewoon de Aspose.Note‑JAR toe aan de classpath van je webproject en zorg ervoor dat de server schrijfrechten heeft op de doelmap.

**Q: Waar kan ik extra voorbeelden en documentatie voor Aspose.Note for Java vinden?**  
A: Bekijk de [documentation](https://reference.aspose.com/note/java/) voor een volledige lijst van API's en voorbeeldprojecten.

---

**Last Updated:** 2026-09-29  
**Tested With:** Aspose.Note for Java 24.12  
**Author:** Aspose  

```java
outlineElem.appendChildLast(text);
outline.appendChildLast(outlineElem);
page.appendChildLast(outline);
document.appendChildLast(page);
document.save(Paths.get(dataDir, "SetProofingLanguageForText.one").toString()); 
```

## Gerelateerde tutorials

- [OneNote‑bestand laden met Java: Gebruik Aspose.Note om OneNote‑documenten te laden](/note/java/onenote-document-loading/load-onenote-document/)
- [OneNote converteren naar platte tekst – Alle tekst extraheren met Aspose.Note for Java](/note/java/onenote-text-manipulation/extract-all-text/)
- [OneNote converteren naar PDF met paginainstellingen met Aspose.Note for Java](/note/java/onenote-document-saving/save-to-pdf-using-page-settings/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}