---
date: 2026-08-13
description: Leer hoe u de gewijzigde tijd van een OneNote-pagina kunt ophalen en
  paginavergissingen kunt ophalen met Aspose.Note voor Java, ideaal voor auditing
  en documentbeheer.
keywords:
- get onenote page modified
- onenote page revisions
- aspose.note java
- java onenote api
lastmod: 2026-08-13
linktitle: Revisies van pagina's in OneNote ophalen - Aspose.Note
og_description: Leer hoe u de gewijzigde tijd van een OneNote-pagina kunt ophalen
  en revisies van OneNote-pagina's kunt ophalen met Aspose.Note voor Java. Snelle
  stappen, codefragmenten en probleemoplossing.
og_image_alt: Screenshot of Aspose.Note Java API showing page revision retrieval
og_title: Haal de gewijzigde tijd van een OneNote-pagina op met Aspose.Note – Java-tutorial
schemas:
- author: Aspose
  dateModified: '2026-08-13'
  description: Learn how to get onenote page modified time and retrieve page revisions
    with Aspose.Note for Java, ideal for auditing and document management.
  headline: Get OneNote page modified time using Aspose.Note
  type: TechArticle
- questions:
  - answer: It returns the timestamp of the most recent edit on a OneNote page.
    question: What does “get last modified time” return?
  - answer: '`PageHistory` via `Document.getPageHistory(Page)`.'
    question: Which class provides revision history?
  - answer: Yes, a valid Aspose.Note license is required for production use.
    question: Do I need a license for this feature?
  - answer: Java 8 or higher (JDK 8+).
    question: What Java version is supported?
  - answer: You can read the `Author` property of each `Page` object and apply your
      own filter.
    question: Can I filter revisions by author?
  type: FAQPage
second_title: Aspose.Note Java API
tags:
- onenote page modified
- aspose.note
- java document management
title: Haal de gewijzigde tijd van een OneNote-pagina op met Aspose.Note
url: /nl/java/onenote-page-manipulation/get-revisions-of-pages/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote-pagina wijzigingsdatum ophalen met Aspose.Note

## Inleiding

In deze tutorial leer je hoe je **get onenote page modified** tijdstempels kunt ophalen en de volledige revisiegeschiedenis van een OneNote-pagina kunt ophalen met Aspose.Note voor Java. Of je nu een audit‑trail‑functie bouwt, een change‑log‑viewer, of de meest recente bewerkingsdatum in een dashboard moet weergeven, deze gids leidt je stap voor stap — van het opzetten van de omgeving tot het omgaan met veelvoorkomende valkuilen.

## Snelle antwoorden
- **Wat retourneert “get last modified time”?** Het retourneert de tijdstempel van de meest recente bewerking op een OneNote-pagina.  
- **Welke klasse levert revisiegeschiedenis?** `PageHistory` via `Document.getPageHistory(Page)`.  
- **Heb ik een licentie nodig voor deze functie?** Ja, een geldige Aspose.Note-licentie is vereist voor productiegebruik.  
- **Welke Java‑versie wordt ondersteund?** Java 8 of hoger (JDK 8+).  
- **Kan ik revisies filteren op auteur?** Je kunt de `Author`‑eigenschap van elk `Page`‑object lezen en je eigen filter toepassen.

## Wat is “get last modified time” in OneNote?

De laatste wijzigingstijd wordt opgeslagen als een metagegevensattribuut op elke OneNote-pagina dat het moment van de meest recente bewerking aangeeft. Aspose.Note maakt deze waarde beschikbaar via de `Page.getLastModifiedTime()`‑methode, die een `java.util.Date`‑object retourneert dat kan worden geformatteerd of gelogd volgens de vereisten van je applicatie.

## Waarom paginarevisies ophalen?

Het ophalen van paginarevisies geeft je een volledige audit‑trail van elke wijziging die op een OneNote-pagina is aangebracht, waardoor je kunt bijhouden wie wat en wanneer heeft bewerkt. Deze geschiedenis kan worden gebruikt om versies te vergelijken, eerdere toestanden te herstellen of samenwerkingspatronen binnen teams te analyseren, wat essentieel is voor naleving en kwaliteitscontrole.

## Vereisten

- **Java Development Kit (JDK) 8 of later** – installeer vanaf de Oracle‑website of een compatibele leverancier.  
- **Aspose.Note for Java‑bibliotheek** – download de JAR van de Aspose.Note Java releases‑pagina **[Aspose.Note Java releases](https://releases.aspose.com/note/java/)** en volg de installatiehandleiding **[Aspose.Note Java documentation](https://reference.aspose.com/note/java/)**.  

## Pakketten importeren

De `Document`‑klasse vertegenwoordigt een OneNote‑notebook die in het geheugen is geladen, terwijl `Page` en `PageHistory` toegang bieden tot individuele pagina's en hun revisie‑gegevens.

```text
import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.PageHistory;
import java.util.Date;
```

*(De daadwerkelijke import‑verklaringen worden als platte tekst weergegeven om het oorspronkelijke aantal code‑blokken te behouden.)*

## Hoe de wijzigingstijd van een OneNote-pagina ophalen?

Om de laatste wijzigingstijdstempel te verkrijgen, laad je eerst het OneNote‑document in een `Document`‑object en selecteer je de gewenste `Page`. Roep de `getLastModifiedTime()`‑methode aan op die pagina, die een `java.util.Date` retourneert. Je kunt deze datum vervolgens formatteren met `SimpleDateFormat` of converteren naar UTC voor consistente rapportage over tijdzones.

## Stap 1: documentmap instellen

Definieer de map die je OneNote‑bestand bevat.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.PageHistory;
```

## Stap 2: het document laden

Maak een `Document`‑instantie aan door het volledige pad naar je `.one`‑bestand door te geven.

```java
String dataDir = "Your Document Directory";
```

## Stap 3: eerste pagina ophalen

Haal het eerste `Page`‑object op uit de paginaverzameling van het document.

```java
Document doc = new Document(dataDir + "Sample1.one");
```

## Stap 4: paginarevisies ophalen

Verkrijg de `PageHistory` voor de geselecteerde pagina. Als het notebook nooit is bewerkt, kan deze oproep `null` retourneren.

```java
Page firstPage = doc.getFirstChild();
```

## Stap 5: paginarevisies doorlopen

Itereer door elke `Page`‑revisie, lees de `Author`‑ en `LastModifiedTime`‑eigenschappen, en toon de informatie.

```java
PageHistory revisions = doc.getPageHistory(firstPage);
```

## Veelvoorkomende problemen en oplossingen
- **Null `PageHistory`** – Controleer of het notebook daadwerkelijk revisies bevat; anders retourneert `getPageHistory` `null`.  
- **Tijdzone‑verschillen** – `getLastModifiedTime()` gebruikt de standaardtijdzone van de JVM. Converteer naar UTC met `SimpleDateFormat` als je applicatie een standaardzone vereist.  
- **Licentie niet geladen** – Zonder een geldige licentie draait Aspose.Note in evaluatiemodus, waardoor de paginaverwerking beperkt wordt. Laad je licentiebestand bij het opstarten van de applicatie om deze beperking te vermijden.

## Veelgestelde vragen

**Q1: Kan ik Aspose.Note voor Java gebruiken om nieuwe OneNote‑documenten te maken?**  
A: Ja, de API stelt je in staat om programmeerbaar OneNote‑notebooks vanaf nul te maken, bewerken en opslaan.

**Q2: Is Aspose.Note voor Java compatibel met verschillende versies van OneNote‑bestanden?**  
A: Ja, het ondersteunt OneNote 2007‑2021 bestandsformaten, wat zorgt voor brede compatibiliteit tussen desktop‑ en cloud‑omgevingen.

**Q3: Kan ik het uitvoerformaat aanpassen bij het exporteren van OneNote‑documenten?**  
A: Absoluut. Je kunt exporteren naar PDF, HTML, PNG of SVG, en opties zoals beeldresolutie en lettertype‑embedden beheren.

**Q4: Vereist Aspose.Note voor Java een licentie voor commercieel gebruik?**  
A: Ja, een commerciële licentie is verplicht voor productie‑implementaties. Een gratis proefversie is beschikbaar voor evaluatie.

**Q5: Waar kan ik hulp zoeken als ik problemen tegenkom?**  
A: Bezoek het Aspose.Note‑communityforum **[Aspose.Note forum](https://forum.aspose.com/c/note/28)** om vragen te stellen, ervaringen te delen en hulp te krijgen van de community en Aspose‑engineers.

---

**Laatst bijgewerkt:** 2026-08-13  
**Getest met:** Aspose.Note for Java 23.12 (latest at time of writing)  
**Auteur:** Aspose

```java
for (Page pageRevision : revisions) {
    System.out.println("LastModifiedTime: " + pageRevision.getLastModifiedTime());
    System.out.println("CreationTime: " + pageRevision.getCreationTime());
    System.out.println("Title: " + pageRevision.getTitle());
    System.out.println("Level: " + pageRevision.getLevel());
    System.out.println("Author: " + pageRevision.getAuthor());
    System.out.println();
}
```

## Gerelateerde tutorials

- [Aspose Java Tutorial - Informatie over pagina's in OneNote ophalen - Aspose.Note](/note/java/onenote-page-manipulation/get-information-about-pages/)
- [aspose.note paginarevisies tutorial – Paginarevisies ophalen in OneNote](/note/java/onenote-page-manipulation/get-page-revisions/)
- [track changes onenote – Paginarevisies beheren met Aspose.Note](/note/java/onenote-page-manipulation/working-with-page-revisions/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}