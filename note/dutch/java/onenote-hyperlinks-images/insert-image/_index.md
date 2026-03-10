---
date: 2025-12-21
description: Leer hoe u afbeeldingen kunt toevoegen aan OneNote‑documenten met Java
  en Aspose.Note voor Java. Volg onze stapsgewijze handleiding om afbeeldingen in
  te voegen en optioneel OneNote op te slaan als PDF.
linktitle: Insert an Image in OneNote Document with Java
second_title: Aspose.Note Java API
title: Hoe een afbeelding toe te voegen aan OneNote met Java
url: /nl/java/onenote-hyperlinks-images/insert-image/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Voeg een afbeelding in in OneNote-document met Java

## Introductie

In deze tutorial verkennen we hoe je een afbeelding in een OneNote-document kunt invoegen met Java met behulp van Aspose.Note voor Java. Aspose.Note for Java is een krachtige bibliotheek die ontwikkelaars in staat stelt om programmatisch met Microsoft OneNote-bestanden te werken, waardoor verschillende bewerkingen mogelijk zijn, zoals het maken, lezen en manipuleren van OneNote-documenten.

## Snelle antwoorden
- **Wat is de gemakkelijkste manier om een ​​afbeelding toe te voegen aan OneNote met Java?** 
Gebruik de `Image`‑klasse van Aspose.Note for Java en voeg deze toe aan een pagina.
- **Heb ik een licentie nodig voor productiegebruik?** 
Ja, een licentie is vereist voor productie‑implementaties.
- **Kan ik aangepaste afmetingen voor de afbeelding instellen?** 
Absoluut – roep `setWidth()` en `setHeight()` aan op het `Image`-object.
- **Is het mogelijk om het OneNote-bestand als PDF op te slaan nadat de afbeelding is toegevoegd?** 
Ja, roep `save(..., SaveFormat.Pdf)` naar **OneNote sla op als PDF**.
- **Welke Java-versie wordt ondersteund?** 
Aspose.Note voor Java werkt met JDK8 en hoger.

## Hoe kan ik een afbeelding toevoegen aan OneNote met Java?

Voordat we in de code duiken, laten we kort beschrijven waarom je programmatisch afbeeldingen in OneNote zou willen insluiten. Of je nu notulen maakt, gewelddadige rapporten geschreven, of een documentatie‑pipeline bouwt, het invoegen van afbeeldingen geeft je notities een visuele context die platte tekst niet kan bieden. Met Aspose.Note voor Java kun je dit volledig in code doen, zonder dat je de OneNote‑UI kunt openen.

## Vereisten

Voordat we beginnen, zorg ervoor dat je de volgende vereisten hebt ingesteld:

### 1. Java-ontwikkelingskit (JDK)
Zorg ervoor dat je Java Development Kit (JDK) op je systeem hebt geïnstalleerd. Je kunt JDK downloaden en installeren vanaf de Oracle‑website.

### 2. Aspose.Note voor Java-bibliotheek
Download en installeer de Aspose.Note voor Java‑bibliotheek door de [documentatie](https://reference.aspose.com/note/java/) om te volgen.

## Pakketten importeren

Begin met het importeren van de gecombineerde pakketten in je Java-project. Deze pakketten omvatten de Aspose.Note‑bibliotheek en andere vereiste afhankelijkheden.

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.HorizontalAlignment;
import com.aspose.note.Image;
import com.aspose.note.LoadOptions;
import com.aspose.note.Page;
import com.aspose.note.SaveFormat;
```

Laten we het proces van het toevoegen van een afbeelding in een OneNote-document opsplitsen in meerdere stappen:

## Stap 1: Laad het OneNote-document

Laad eerst je het OneNote-document waarin je de afbeelding wilt invoegen.

```java
LoadOptions options = new LoadOptions();
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Sample1.one", options);
```

## Stap 2: De pagina ophalen

Verkrijg de pagina in het document waar je de afbeelding wilt invoegen.

```java
Page page = oneFile.getFirstChild();
```

## Stap 3: De afbeelding laden

Laad de afbeelding die je wilt invoegen in het OneNote‑document.

```java
Image image = new Image(oneFile, dataDir + "Input.jpg");
```

## Stap 4: Afbeeldingskenmerken aanpassen (optioneel)

Optioneel kun je de grootte, locatie en uitlijning van de afbeelding aanpassen volgens je vereisten. Dit is waar je **afbeeldingsafmetingen instelt Java** stijl.

```java
image.setWidth(100);
image.setHeight(100);
image.setVerticalOffset(400);
image.setHorizontalOffset(100);
image.setAlignment(HorizontalAlignment.Right);
```

## Stap 5: Afbeelding aan de pagina toevoegen

Voeg de afbeelding toe aan de pagina in het OneNote‑document.

```java
page.appendChildLast(image);
```

## Stap 6: Het document opslaan

Sla het gewijzigde document op, inclusief de ingevoegde afbeelding. Je kunt ook **OneNote opslaan als PDF** in deze fase.

```java
try {
    oneFile.save(dataDir + "InsertanImage_out.pdf", SaveFormat.Pdf);
} catch (IOException e) {
    e.printStackTrace();
}
```

## Conclusie

In deze tutorial hebben we geleerd hoe je een afbeelding in een OneNote-document kunt invoegen met Java met behulp van de Aspose.Note voor Java-bibliotheek. Door de stapsgewijze gids te volgen, kun je moeiteloos afbeeldingen programmatisch opnemen in je OneNote-documenten opnemen.

## Veelgestelde vragen

### Vraag 1: Kan ik met deze methode meerdere afbeeldingen in één OneNote-document invoegen?

**A1:** Ja, je kunt meerdere afbeeldingen in één OneNote-document toevoegen door het proces dat in deze tutorial wordt beschreven voor elke afbeelding te herhalen.

### V2: Is Aspose.Note voor Java compatibel met alle versies van OneNote?

**A2:** Aspose.Note for Java ondersteunt het werken met OneNote‑bestanden die zijn gemaakt in Microsoft OneNote 2010 en latere versies.

### V3: Kan ik afbeeldingen van verschillende formaten, zoals PNG of GIF, in een OneNote-document invoegen?

**A3:** Ja, Aspose.Note for Java ondersteunt het invoegen van afbeeldingen in diverse formaten, waaronder PNG, JPEG, GIF en meer.

### V4: Is er een proefversie van Aspose.Note voor Java beschikbaar voor testdoeleinden?

**A4:** Ja, je kunt een gratis proefversie van Aspose.Note voor het downloaden van Java van de website voor evaluatiedoeleinden.

### V5: Hoe kan ik technische ondersteuning krijgen voor Aspose.Note voor Java?

**A5:** Je kunt technische ondersteuning voor Aspose.Note for Java krijgen door het [forum](https://forum.aspose.com/c/note/28) te bezoeken dat gewijd is aan Aspose.Note‑producten.

---

**Laatst bijgewerkt:** 21-12-2025
**Getest met:** Aspose.Note voor Java 24.10
**Auteur:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}