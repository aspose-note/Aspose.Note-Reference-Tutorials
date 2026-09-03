---
date: 2026-01-15
description: Leer hoe u wijzigingen in OneNote kunt bijhouden en paginavergissingen
  kunt beheren in OneNote‑documenten met Aspose.Note voor Java. Bevat een voorbeeld
  van een revisiesamenvatting en hoe u de revisiedatum kunt wijzigen.
linktitle: Working with Page Revisions in OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: Wijzigingen bijhouden OneNote – Beheer paginavergissingen met Aspose.Note
url: /nl/java/onenote-page-manipulation/working-with-page-revisions/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Werken met paginarevisies in OneNote - Aspose.Note

## Inleiding

OneNote is een krachtig hulpmiddel voor het organiseren van notities, en wanneer je **track changes onenote** moet bijhouden, wordt het beheren van paginarevisies essentieel voor effectieve samenwerking. Met Aspose.Note voor Java kun je programmatically revisies afhandelen, zien wie een pagina heeft bewerkt, en zelfs tijdstempels aanpassen. Deze tutorial leidt je door elke stap, van het laden van een document tot het bijwerken van de revisiesamenvatting.

## Snelle antwoorden
- **Wat betekent “track changes onenote”?** Het verwijst naar het monitoren wie een OneNote‑pagina heeft bewerkt en wanneer.
- **Welke bibliotheek is vereist?** Aspose.Note voor Java.
- **Kan ik de auteur of datum van een revisie wijzigen?** Ja, met de RevisionSummary API (`modify revision date`).
- **Heb ik vooraf een OneNote‑bestand nodig?** Ja, een voorbeeld‑`.one`‑bestand is vereist.
- **Is een licentie nodig voor productie?** Een geldige Aspose.Note‑licentie is vereist voor commercieel gebruik.

## Wat is een voorbeeld van een revisiesamenvatting?
Een *revisiesamenvatting* biedt metadata over de meest recente wijzigingen op een pagina—naam van de auteur, laatst gewijzigde tijd, en andere details. In deze gids halen we die informatie op en tonen we deze, en laten we vervolgens zien hoe je **modify revision date** kunt **wijzigen**.

## Waarom track changes onenote gebruiken met Aspose.Note?
- **Samenwerking:** Zie snel wie de laatste bewerkingen heeft gedaan.
- **Auditing:** Houd een betrouwbare geschiedenis van wijzigingen bij voor compliance.
- **Automatisering:** Integreer revisiebeheer in back‑end services of migratietools.

## Voorvereisten

### Java-ontwikkelomgeving
Zorg ervoor dat je Java Development Kit (JDK) op je systeem hebt geïnstalleerd.

### Aspose.Note voor Java-bibliotheek
Download en installeer de Aspose.Note voor Java-bibliotheek van [hier](https://releases.aspose.com/note/java/).

### OneNote‑document
Zorg voor een voorbeeld OneNote‑document klaar voor testdoeleinden.

## Importeer pakketten

Importeer in je Java‑project de benodigde pakketten om met Aspose.Note voor Java te werken.

```java
import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.RevisionSummary;
import java.io.IOException;
import java.util.Calendar;
```

Laten we het gegeven voorbeeld opsplitsen in meerdere stappen voor een duidelijk begrip.

## Stap 1: OneNote‑document laden

Laad eerst het OneNote‑document en haal de eerste onderliggende pagina op.

```java
String dataDir = "Your Document Directory";
Document document = new Document(dataDir + "Sample1.one");
Page page = document.getFirstChild();
```

## Stap 2: Paginarevisiesamenvatting lezen

Lees de inhoudsrevisiesamenvatting voor de pagina. Dit is het **revision summary example** dat laat zien wie de pagina het laatst heeft bewerkt.

```java
RevisionSummary pageRevisionInfo = page.getPageContentRevisionSummary();
System.out.println(String.format("Author:\t%s\nModified:\t%s",
        pageRevisionInfo.getAuthorMostRecent(),
        pageRevisionInfo.getLastModifiedTime().toString()));
```

## Stap 3: Paginarevisiesamenvatting bijwerken

Werk de paginarevisiesamenvatting bij met een nieuwe auteur en een nieuwe wijzigingsdatum. Dit toont aan hoe je **modify revision date** programmatically kunt **wijzigen**.

```java
pageRevisionInfo.setAuthorMostRecent("New Author");
Calendar modifiedDate = Calendar.getInstance();
pageRevisionInfo.setLastModifiedTime(modifiedDate.getTime());
document.save(dataDir + "WorkingWithPageRevisions_out.one");
```

## Conclusie

Het programmatic beheren van paginarevisies in OneNote‑documenten kan worden vereenvoudigd met Aspose.Note voor Java. Door de stappen in deze tutorial te volgen, kun je effectief **track changes onenote**, revisiedetails bekijken, en zelfs **modify revision date** aanpassen aan je workflow.

## Veelgestelde vragen

### Q1: Kan ik Aspose.Note voor Java gebruiken met andere Java‑bibliotheken?

A: Ja, Aspose.Note voor Java kan worden geïntegreerd met andere Java‑bibliotheken om functionaliteit uit te breiden.

### Q2: Ondersteunt Aspose.Note voor Java alle versies van OneNote‑documenten?

A: Aspose.Note voor Java ondersteunt verschillende versies van OneNote‑documenten, inclusief oudere versies.

### Q3: Is Aspose.Note voor Java geschikt voor enterprise‑level toepassingen?

A: Absoluut, Aspose.Note voor Java is ontworpen om te voldoen aan de behoeften van enterprise‑level toepassingen met robuuste functies en schaalbaarheid.

### Q4: Kan ik paginarevisies aanpassen met Aspose.Note voor Java?

A: Ja, je kunt paginarevisies aanpassen aan je vereisten met behulp van Aspose.Note voor Java.

### Q5: Waar kan ik ondersteuning krijgen voor Aspose.Note voor Java?

A: Je kunt ondersteuning voor Aspose.Note voor Java krijgen via het [Aspose.Note forum](https://forum.aspose.com/c/note/28).

---

**Laatst bijgewerkt:** 2026-01-15  
**Getest met:** Aspose.Note voor Java 24.12  
**Auteur:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}