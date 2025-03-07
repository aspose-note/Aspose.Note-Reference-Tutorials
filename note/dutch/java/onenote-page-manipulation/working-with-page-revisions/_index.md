---
title: Werken met paginarevisies in OneNote - Aspose.Note
linktitle: Werken met paginarevisies in OneNote - Aspose.Note
second_title: Aspose.Note Java-API
description: Leer hoe u paginarevisies in OneNote-documenten kunt beheren met Aspose.Note voor Java. Biedt een stapsgewijze handleiding voor effectief bijhouden van revisies en samenwerking.
weight: 21
url: /nl/java/onenote-page-manipulation/working-with-page-revisions/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Werken met paginarevisies in OneNote - Aspose.Note

## Invoering

OneNote is een krachtig hulpmiddel voor het organiseren en beheren van notities, maar soms moet u met revisies werken om wijzigingen bij te houden en effectief samen te werken. Met Aspose.Note voor Java kunt u paginarevisies in OneNote-documenten eenvoudig programmatisch beheren. Deze tutorial begeleidt u stap voor stap door het proces.

## Vereisten

Zorg ervoor dat u over het volgende beschikt voordat u begint:

### Java-ontwikkelomgeving

Zorg ervoor dat Java Development Kit (JDK) op uw systeem is geïnstalleerd.

### Aspose.Note voor Java-bibliotheek

Download en installeer Aspose.Note voor Java-bibliotheek van[hier](https://releases.aspose.com/note/java/).

### OneNote-document

Houd een voorbeeld van een OneNote-document bij de hand voor testdoeleinden.

## Pakketten importeren

Importeer in uw Java-project de benodigde pakketten om met Aspose.Note voor Java te werken.

```java
import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.RevisionSummary;
import java.io.IOException;
import java.util.Calendar;
```

Laten we het gegeven voorbeeld opsplitsen in meerdere stappen voor een duidelijk begrip.

## Stap 1: OneNote-document laden

Laad eerst het OneNote-document en haal de eerste onderliggende pagina op.

```java
String dataDir = "Your Document Directory";
Document document = new Document(dataDir + "Sample1.one");
Page page = document.getFirstChild();
```

## Stap 2: Lees de samenvatting van de paginarevisie

Lees de samenvatting van de inhoudsrevisie voor de pagina.

```java
RevisionSummary pageRevisionInfo = page.getPageContentRevisionSummary();
System.out.println(String.format("Author:\t%s\nModified:\t%s",
        pageRevisionInfo.getAuthorMostRecent(),
        pageRevisionInfo.getLastModifiedTime().toString()));
```

## Stap 3: Update de samenvatting van de paginarevisie

Update het overzicht van de paginarevisie met de nieuwe auteur en de gewijzigde datum.

```java
pageRevisionInfo.setAuthorMostRecent("New Author");
Calendar modifiedDate = Calendar.getInstance();
pageRevisionInfo.setLastModifiedTime(modifiedDate.getTime());
document.save(dataDir + "WorkingWithPageRevisions_out.one");
```

## Conclusie

Het programmatisch beheren van paginarevisies in OneNote-documenten kan worden vereenvoudigd met Aspose.Note voor Java. Door de stappen in deze zelfstudie te volgen, kunt u effectief werken met paginarevisies om wijzigingen bij te houden en naadloos samen te werken.

## Veelgestelde vragen

### V1: Kan ik Aspose.Note voor Java gebruiken met andere Java-bibliotheken?

A: Ja, Aspose.Note voor Java kan worden geïntegreerd met andere Java-bibliotheken om de functionaliteit te verbeteren.

### V2: Ondersteunt Aspose.Note voor Java alle versies van OneNote-documenten?

A: Aspose.Note voor Java ondersteunt verschillende versies van OneNote-documenten, inclusief oudere versies.

### V3: Is Aspose.Note voor Java geschikt voor toepassingen op ondernemingsniveau?

A: Absoluut, Aspose.Note voor Java is ontworpen om te voldoen aan de behoeften van applicaties op ondernemingsniveau met robuuste functies en schaalbaarheid.

### V4: Kan ik paginarevisies aanpassen met Aspose.Note voor Java?

A: Ja, u kunt paginarevisies aanpassen aan uw vereisten met behulp van Aspose.Note voor Java.

### V5: Waar kan ik ondersteuning krijgen voor Aspose.Note voor Java?

 A: U kunt ondersteuning voor Aspose.Note voor Java krijgen van de[Aspose.Note-forum](https://forum.aspose.com/c/note/28).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
