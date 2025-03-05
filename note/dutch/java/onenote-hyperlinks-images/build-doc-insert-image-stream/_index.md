---
title: Bouw een document en voeg een afbeelding in met Stream in OneNote - Java
linktitle: Bouw een document en voeg een afbeelding in met Stream in OneNote - Java
second_title: Aspose.Note Java-API
description: Leer hoe u moeiteloos afbeeldingen in OneNote-documenten kunt integreren met Aspose.Note voor Java. Stap-voor-stap handleiding voor Java-ontwikkelaars.
type: docs
weight: 13
url: /nl/java/onenote-hyperlinks-images/build-doc-insert-image-stream/
---
## Invoering

Welkom bij onze uitgebreide tutorial over het gebruik van Aspose.Note voor Java om documenten te bouwen en afbeeldingen in te voegen met behulp van afbeeldingsstreams in OneNote! In deze tutorial begeleiden we u stap voor stap door het proces, zodat u elke fase duidelijk begrijpt. Uiteindelijk kunt u met Java moeiteloos afbeeldingen in uw OneNote-documenten integreren.

## Vereisten

Voordat we ingaan op de tutorial, zorg ervoor dat je aan de volgende vereisten voldoet:

### Java-ontwikkelkit (JDK)

Zorg ervoor dat Java Development Kit (JDK) op uw systeem is geïnstalleerd. U kunt het downloaden van de Oracle-website.

### Aspose.Note voor Java-bibliotheek

 Download en installeer de Aspose.Note voor Java-bibliotheek uit de meegeleverde bibliotheek[koppeling](https://releases.aspose.com/note/java/).

### IDE-installatie

Zet uw Integrated Development Environment (IDE) op met de nodige configuraties om met Java-projecten te werken.

## Pakketten importeren

Importeer om te beginnen de vereiste pakketten in uw Java-project. Deze pakketten bieden de nodige functionaliteit om met OneNote-documenten en afbeeldingen te werken.

```java
import java.io.FileInputStream;
import java.io.FileNotFoundException;
import java.io.IOException;
import java.io.InputStream;
import com.aspose.note.Document;
import com.aspose.note.HorizontalAlignment;
import com.aspose.note.Image;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.SaveFormat;
```

## Stap 1: Documentmap instellen

 Definieer de map waar uw document en afbeeldingen zich bevinden. Vervangen`"Your Document Directory"` met het pad naar uw map.

```java
String dataDir = "Your Document Directory";
```

## Stap 2: Maak een documentobject

 Initialiseer een exemplaar van de`Document` klasse om aan de slag te gaan met uw OneNote-document.

```java
Document doc = new Document();
```

## Stap 3: Initialiseer het paginaobject

 Maak een`Page` object om de pagina in het document weer te geven.

```java
Page page = new Page();
```

## Stap 4: Maak een overzicht

 Initialiseer een`Outline` object om de inhoud op de pagina te structureren.

```java
Outline outline1 = new Outline();
outline1.setVerticalOffset(600);
outline1.setHorizontalOffset(0);
```

## Stap 5: Maak een overzichtselement

 Creëer een`OutlineElement` om de afbeelding vast te houden en de positie ervan te specificeren.

```java
OutlineElement outlineElem1 = new OutlineElement();
```

## Stap 6: Laad de beeldstream

 Laad de beeldstream met behulp van de`FileInputStream` voor het gewenste beeld.

```java
InputStream fs = null;
try {
    fs = new FileInputStream(dataDir + "image.jpg");
} catch (FileNotFoundException e) {
    e.printStackTrace();
}
```

## Stap 7: Afbeelding invoegen

 Voeg de afbeelding in het document in door een`Image` object en het instellen van de uitlijning ervan.

```java
Image image = new Image(null, dataDir + "image1.jpg");
image.setAlignment(HorizontalAlignment.Right);
```

## Stap 8: Voeg afbeelding toe aan overzichtselement

Voeg de afbeelding toe aan het overzichtselement.

```java
outlineElem1.appendChildLast(image);
```

## Stap 9: Voeg een overzichtselement toe aan de omtrek

Voeg het overzichtselement toe aan de omtrek.

```java
outline1.appendChildLast(outlineElem1);
```

## Stap 10: Voeg een overzicht toe aan de pagina

Voeg de omtrek toe aan de pagina.

```java
page.appendChildLast(outline1);
```

## Stap 11: Pagina aan document toevoegen

Voeg ten slotte de pagina toe aan het document.

```java
doc.appendChildLast(page);
```

## Stap 12: Document opslaan

Sla het gewijzigde document op en geef het gewenste formaat op (bijvoorbeeld PDF).

```java
try {
    doc.save("D://Aspose_JavaProjects//OneNote//out3.pdf", SaveFormat.Pdf);
} catch (IOException e) {
    e.printStackTrace();
}
```

Door deze stappen te volgen, kunt u moeiteloos documenten samenstellen en afbeeldingen invoegen met behulp van afbeeldingsstreams in OneNote met behulp van Aspose.Note voor Java.

## Conclusie

Concluderend: het beheersen van de integratie van afbeeldingen in uw OneNote-documenten met behulp van Java kan uw proces voor het maken van documenten aanzienlijk verbeteren. Met Aspose.Note voor Java beschikt u over een krachtig hulpmiddel om deze taak naadloos uit te voeren.

## Veelgestelde vragen

### V1: Is Aspose.Note voor Java compatibel met alle versies van OneNote?

A1: Aspose.Note voor Java ondersteunt verschillende versies van OneNote, waardoor compatibiliteit tussen verschillende omgevingen wordt gegarandeerd.

### V2: Kan ik het uiterlijk van ingevoegde afbeeldingen in OneNote-documenten aanpassen met Aspose.Note voor Java?

A2: Ja, u kunt verschillende aspecten van ingevoegde afbeeldingen aanpassen, zoals uitlijning, grootte en richting, zodat deze aan uw specifieke vereisten voldoen.

### V3: Biedt Aspose.Note voor Java ondersteuning voor andere documentformaten dan PDF?

A3: Ja, Aspose.Note voor Java ondersteunt een breed scala aan documentformaten, waaronder DOCX, HTML en meer, waardoor u flexibiliteit krijgt bij uw documentbeheertaken.

### V4: Waar kan ik aanvullende bronnen en ondersteuning vinden voor Aspose.Note voor Java?

A4: Via de aangeboden links heeft u toegang tot documentatie, downloadlinks, ondersteuningsforums en tijdelijke licenties voor Aspose.Note voor Java.

### V5: Is er een proefversie beschikbaar voor Aspose.Note voor Java?

A5: Ja, u kunt een gratis proefversie van Aspose.Note voor Java verkrijgen om de functies en mogelijkheden ervan te verkennen voordat u een aankoopbeslissing neemt.
