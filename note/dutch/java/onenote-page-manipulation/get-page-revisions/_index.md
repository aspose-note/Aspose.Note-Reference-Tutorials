---
title: Paginarevisies ophalen in OneNote - Aspose.Note
linktitle: Paginarevisies ophalen in OneNote - Aspose.Note
second_title: Aspose.Note Java-API
description: Leer hoe u paginarevisies in OneNote kunt ophalen met Aspose.Note voor Java. Volg onze stapsgewijze handleiding voor het efficiënt volgen van wijzigingen.
type: docs
weight: 14
url: /nl/java/onenote-page-manipulation/get-page-revisions/
---
## Invoering

OneNote is een krachtig hulpmiddel voor het organiseren en beheren van uw notities, maar soms moet u de wijzigingen en herzieningen van uw pagina's bijhouden. Met Aspose.Note voor Java kunt u eenvoudig paginarevisies programmatisch ophalen. In deze zelfstudie begeleiden we u bij het proces voor het verkrijgen van paginarevisies in OneNote met behulp van Aspose.Note voor Java.

## Vereisten

Voordat we aan de slag gaan, moet u ervoor zorgen dat u aan de volgende vereisten voldoet:

### 1. Java-ontwikkelingskit (JDK)

Zorg ervoor dat Java Development Kit (JDK) op uw systeem is geïnstalleerd. U kunt JDK downloaden en installeren vanaf de Oracle-website.

### 2. Aspose.Note voor Java

Download en installeer Aspose.Note voor Java vanaf de[download link](https://releases.aspose.com/note/java/).

### 3. Voorbeeld van een OneNote-document

Bereid een voorbeeld van een OneNote-document voor (`Sample1.one`) met de pagina's waarvan u revisies wilt ophalen.

## Pakketten importeren

Eerst moet u de benodigde pakketten importeren uit Aspose.Note voor Java.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.LoadOptions;
import com.aspose.note.Page;
```

Laten we het gegeven voorbeeld nu in meerdere stappen opsplitsen:

## Stap 1: Documentmap instellen

Definieer het mappad waar uw OneNote-document zich bevindt.

```java
String dataDir = "Your Document Directory";
```

## Stap 2: OneNote-document laden

 Laad het OneNote-document met`LoadOptions` om de laadgeschiedenis in te schakelen.

```java
LoadOptions loadOptions = new LoadOptions();
loadOptions.setLoadHistory(true);
Document document = new Document(dataDir + "Sample1.one", loadOptions);
```

## Stap 3: Krijg de eerste pagina

Haal de eerste pagina uit het geladen document op.

```java
Page firstPage = document.getFirstChild();
```

## Stap 4: Herhaal paginarevisies

Doorloop elke paginarevisie en haal relevante informatie op, zoals de tijd van de laatste wijziging, de aanmaaktijd, titel, niveau en auteur.

```java
for (Page pageRevision : document.getPageHistory(firstPage)) {
    System.out.println("LastModifiedTime: " + pageRevision.getLastModifiedTime());
    System.out.println("CreationTime: " + pageRevision.getCreationTime());
    System.out.println("Title: " + pageRevision.getTitle());
    System.out.println("Level: " + pageRevision.getLevel());
    System.out.println("Author: " + pageRevision.getAuthor());
    System.out.println();
}
```

## Conclusie

In deze zelfstudie hebben we geleerd hoe u paginarevisies in OneNote kunt ophalen met Aspose.Note voor Java. Door deze stappen te volgen, kunt u wijzigingen die programmatisch op uw OneNote-pagina's zijn aangebracht, efficiënt bijhouden.

## Veelgestelde vragen

### V1: Kan ik Aspose.Note voor Java gebruiken om paginarevisies te wijzigen?

A1: Nee, Aspose.Note voor Java ondersteunt momenteel het ophalen van paginarevisies, maar niet het wijzigen ervan.

### V2: Is Aspose.Note voor Java compatibel met verschillende versies van OneNote-documenten?

A2: Ja, Aspose.Note voor Java ondersteunt verschillende versies van OneNote-documenten, waardoor u naadloos met verschillende bestandsformaten kunt werken.

### V3: Heeft Aspose.Note voor Java een licentie nodig om te gebruiken?

A3: Ja, u moet een licentie aanschaffen om Aspose.Note voor Java in commerciële projecten te gebruiken. U kunt echter ook een tijdelijke licentie verkrijgen voor evaluatiedoeleinden.

### V4: Kan ik ondersteuning zoeken als ik problemen ondervind tijdens het gebruik van Aspose.Note voor Java?

 A4: Ja, u kunt ondersteuning zoeken op het Aspose.Note-forum[hier](https://forum.aspose.com/c/note/28).

### V5: Is er een gratis proefversie beschikbaar voor Aspose.Note voor Java?

 A5: Ja, u kunt toegang krijgen tot een gratis proefversie van Aspose.Note voor Java via de[website](https://releases.aspose.com/).