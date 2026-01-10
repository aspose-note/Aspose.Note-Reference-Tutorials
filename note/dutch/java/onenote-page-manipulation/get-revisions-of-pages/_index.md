---
date: 2026-01-10
description: Leer hoe u de laatst gewijzigde tijd kunt opvragen en revisies van OneNote‑pagina’s
  kunt ophalen met Aspose.Note voor Java. Integreer dit in uw Java‑applicaties voor
  efficiënt documentbeheer.
linktitle: Get Revisions of Pages in OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: Hoe de laatste wijzigingstijd van OneNote-pagina’s op te halen – Aspose.Note
url: /nl/java/onenote-page-manipulation/get-revisions-of-pages/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Ophalen van revisies van pagina's in OneNote - Aspose.Note

## Inleiding

In deze tutorial **get last modified time** voor pagina's in een OneNote‑document ophalen en ontdekken hoe je de volledige revisiegeschiedenis kunt ophalen met Aspose.Note voor Java. Of je nu een document‑beheersysteem bouwt, wijzigingen audit, of simpelweg de datum wilt weergeven waarop een pagina voor het laatst is bewerkt, deze gids laat je precies zien hoe je die informatie programmatically kunt extraheren.

## Snelle antwoorden
- **Wat retourneert “get last modified time”?** De tijdstempel van de meest recente bewerking op een OneNote‑pagina.  
- **Welke klasse levert de revisiegeschiedenis?** `PageHistory` via `Document.getPageHistory(Page)`.  
- **Heb ik een licentie nodig voor deze functie?** Ja, een geldige Aspose.Note‑licentie is vereist voor productiegebruik.  
- **Welke Java‑versie wordt ondersteund?** Java 8 of hoger (JDK 8+).  
- **Kan ik revisies filteren op auteur?** Je kunt de `Author`‑eigenschap van elk `Page`‑object lezen en je eigen filter toepassen.

## Wat is “get last modified time” in OneNote?

De **last modified time** is een metagegevensveld dat bij elke pagina wordt opgeslagen en registreert wanneer de pagina voor het laatst is gewijzigd. Aspose.Note maakt deze waarde beschikbaar via de `Page.getLastModifiedTime()`‑methode, waardoor het eenvoudig is om wijzigingsdatums weer te geven of te loggen.

## Waarom paginarevisies ophalen?

- **Auditsporen:** Houd een overzicht bij van wie wat en wanneer heeft gewijzigd.  
- **Versie‑vergelijking:** Bouw functionaliteit die twee revisies naast elkaar vergelijkt.  
- **Inzichten in gebruikerssamenwerking:** Begrijp bewerkingspatronen in gedeelde notitieblokken.  

## Voorvereisten

Zorg ervoor dat je het volgende hebt voordat je begint:

### Java Development Kit (JDK) Installed
Installeer JDK 8 of later vanaf de Oracle‑website of via je favoriete pakketbeheerder.

### Aspose.Note for Java Library
Download de bibliotheek van de officiële site. Je kunt de downloadlink **[hier](https://releases.aspose.com/note/java/)** vinden. Volg de installatie‑instructies in de documentatie **[hier](https://reference.aspose.com/note/java/)**.

## Importeer pakketten

Om te beginnen, importeer je de benodigde pakketten in je Java‑project. Deze pakketten stellen je in staat om de functionaliteit van Aspose.Note voor Java te benutten.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.PageHistory;
```

Laten we nu de voorbeeldcode opsplitsen in meerdere stappen om elk onderdeel en de functionaliteit ervan te begrijpen.

## Hoe de last modified time van een OneNote‑pagina ophalen

### Stap 1: Documentmap instellen
Definieer de map waarin je OneNote‑document zich bevindt.

```java
String dataDir = "Your Document Directory";
```

### Stap 2: Document laden
Laad het OneNote‑document in Aspose.Note.

```java
Document doc = new Document(dataDir + "Sample1.one");
```

### Stap 3: Eerste pagina ophalen
Haal de eerste pagina op uit het document.

```java
Page firstPage = doc.getFirstChild();
```

### Stap 4: Pagina‑revisies ophalen
Verkrijg de revisiegeschiedenis van de pagina.

```java
PageHistory revisions = doc.getPageHistory(firstPage);
```

### Stap 5: Pagina‑revisies doorlopen
Itereer door de lijst met pagina‑revisies en haal relevante informatie op, inclusief de **last modified time**.

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

## Veelvoorkomende problemen en oplossingen
- **Null `PageHistory`:** Zorg ervoor dat het document daadwerkelijk revisies bevat; anders kan `getPageHistory` `null` retourneren.  
- **Tijdzoneverschillen:** `getLastModifiedTime()` retourneert een `java.util.Date` in de standaardtijdzone van het systeem. Converteer naar UTC indien nodig.  
- **Licentie niet geladen:** Zonder een geldige licentie kan Aspose.Note in evaluatiemodus werken, waardoor het aantal verwerkte pagina's wordt beperkt.

## Veelgestelde vragen

### Q1: Kan ik Aspose.Note voor Java gebruiken om nieuwe OneNote‑documenten te maken?
A1: Ja, Aspose.Note voor Java biedt uitgebreide ondersteuning voor het programmatically maken, lezen en manipuleren van OneNote‑documenten.

### Q2: Is Aspose.Note voor Java compatibel met verschillende versies van OneNote‑bestanden?
A2: Ja, Aspose.Note voor Java ondersteunt verschillende versies van Microsoft OneNote‑bestanden, waardoor compatibiliteit in diverse omgevingen wordt gegarandeerd.

### Q3: Kan ik het uitvoerformaat aanpassen bij het exporteren van OneNote‑documenten?
A3: Absoluut, Aspose.Note voor Java biedt flexibiliteit bij het exporteren van OneNote‑documenten naar verschillende formaten zoals PDF, HTML en afbeeldingen, met aanpassingsopties.

### Q4: Vereist Aspose.Note voor Java een licentie voor commercieel gebruik?
A4: Ja, een geldige licentie is vereist voor commercieel gebruik van Aspose.Note voor Java. Je kunt een licentie verkrijgen via de Aspose‑website.

### Q5: Waar kan ik hulp zoeken als ik problemen ondervind of vragen heb over Aspose.Note voor Java?
A5: Voor ondersteuning kun je het Aspose.Note‑forum **[hier](https://forum.aspose.com/c/note/28)** bezoeken, waar je vragen kunt stellen, ervaringen kunt delen en kunt communiceren met andere gebruikers en experts.

---

**Last Updated:** 2026-01-10  
**Tested With:** Aspose.Note for Java 23.12 (latest at time of writing)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}