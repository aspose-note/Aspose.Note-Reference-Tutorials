---
title: Ontvang revisies van pagina's in OneNote - Aspose.Note
linktitle: Ontvang revisies van pagina's in OneNote - Aspose.Note
second_title: Aspose.Note Java-API
description: Leer hoe u revisies van pagina's binnen OneNote-documenten kunt ophalen met Aspose.Note Java. Integreer dit in uw Java-apps voor efficiënt documentbeheer.
type: docs
weight: 15
url: /nl/java/onenote-page-manipulation/get-revisions-of-pages/
---
## Invoering

In deze zelfstudie verdiepen we ons in de mogelijkheden van Aspose.Note voor Java, een krachtige bibliotheek waarmee u naadloos met Microsoft OneNote-bestanden kunt werken in uw Java-toepassingen. We zullen ons specifiek concentreren op het ophalen van revisies van pagina's binnen een OneNote-document. Aan het einde van deze handleiding beschikt u over de kennis om paginarevisies efficiënt te extraheren, inclusief details zoals tijd van laatste wijziging, aanmaaktijd, titel, niveau en auteur.

## Vereisten

Voordat u in deze zelfstudie duikt, moet u ervoor zorgen dat u aan de volgende vereisten voldoet:

### Java Development Kit (JDK) geïnstalleerd

Zorg ervoor dat de Java Development Kit op uw systeem is geïnstalleerd. U kunt het downloaden en installeren vanaf de Oracle-website of een pakketbeheerder gebruiken als u op een Unix-gebaseerd systeem werkt.

### Aspose.Note voor Java-bibliotheek

 Download en installeer Aspose.Note voor Java-bibliotheek vanaf de website. Je kunt de downloadlink vinden[hier](https://releases.aspose.com/note/java/) . Volg de installatie-instructies in de documentatie[hier](https://reference.aspose.com/note/java/).

## Pakketten importeren

Importeer om te beginnen de benodigde pakketten in uw Java-project. Met deze pakketten kunt u gebruikmaken van de functionaliteit van Aspose.Note voor Java.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.PageHistory;
```

Laten we nu de voorbeeldcode in meerdere stappen opsplitsen om elk onderdeel en de functionaliteit ervan te begrijpen.

## Stap 1: Documentmap instellen

Definieer de map waarin uw OneNote-document zich bevindt.

```java
String dataDir = "Your Document Directory";
```

## Stap 2: Laad het document

Laad het OneNote-document in Aspose.Note.

```java
Document doc = new Document(dataDir + "Sample1.one");
```

## Stap 3: Krijg de eerste pagina

Haal de eerste pagina uit het document op.

```java
Page firstPage = doc.getFirstChild();
```

## Stap 4: Paginarevisies ophalen

Haal de revisiegeschiedenis van de pagina op.

```java
PageHistory revisions = doc.getPageHistory(firstPage);
```

## Stap 5: Doorloop paginarevisies

Blader door de lijst met paginarevisies en haal relevante informatie op.

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

## Conclusie

In deze zelfstudie hebben we onderzocht hoe u revisies van pagina's in een OneNote-document kunt ophalen met Aspose.Note voor Java. Door de stapsgewijze handleiding te volgen en gebruik te maken van de meegeleverde voorbeeldcode, kunt u deze functionaliteit eenvoudig in uw Java-applicaties integreren, waardoor een efficiënt beheer van OneNote-bestanden mogelijk wordt.

## Veelgestelde vragen

### V1: Kan ik Aspose.Note voor Java gebruiken om nieuwe OneNote-documenten te maken?

A1: Ja, Aspose.Note voor Java biedt uitgebreide ondersteuning voor het programmatisch maken, lezen en manipuleren van OneNote-documenten.

### V2: Is Aspose.Note voor Java compatibel met verschillende versies van OneNote-bestanden?

A2: Ja, Aspose.Note voor Java ondersteunt verschillende versies van Microsoft OneNote-bestanden, waardoor compatibiliteit tussen verschillende omgevingen wordt gegarandeerd.

### V3: Kan ik het uitvoerformaat aanpassen bij het exporteren van OneNote-documenten?

A3: Absoluut, Aspose.Note voor Java biedt flexibiliteit bij het exporteren van OneNote-documenten naar verschillende formaten zoals PDF, HTML en afbeeldingen, met opties voor aanpassing.

### V4: Heeft Aspose.Note voor Java een licentie nodig voor commercieel gebruik?

A4: Ja, voor commercieel gebruik van Aspose.Note voor Java is een geldige licentie vereist. U kunt een licentie verkrijgen via de Aspose-website.

### V5: Waar kan ik hulp zoeken als ik problemen ondervind of vragen heb over Aspose.Note voor Java?

 A5: Voor ondersteuning en assistentie kunt u het Aspose.Note-forum bezoeken[hier](https://forum.aspose.com/c/note/28)waar u vragen kunt stellen, ervaringen kunt delen en kunt communiceren met andere gebruikers en experts.