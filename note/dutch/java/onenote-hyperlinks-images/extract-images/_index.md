---
title: Extraheer afbeeldingen uit een OneNote-document met Java
linktitle: Extraheer afbeeldingen uit een OneNote-document met Java
second_title: Aspose.Note Java-API
description: Leer hoe u afbeeldingen uit OneNote-documenten kunt extraheren met behulp van Java met de Aspose.Note-bibliotheek. Volg onze stapsgewijze handleiding voor naadloze beeldextractie.
weight: 14
url: /nl/java/onenote-hyperlinks-images/extract-images/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Extraheer afbeeldingen uit een OneNote-document met Java

## Invoering

In deze zelfstudie begeleiden we u bij het extraheren van afbeeldingen uit een OneNote-document met behulp van Java met behulp van de Aspose.Note-bibliotheek.

## Vereisten

Zorg ervoor dat u over het volgende beschikt voordat u begint:

1.  Java Development Kit (JDK): Zorg ervoor dat Java op uw systeem is geïnstalleerd. Je kunt het downloaden en installeren vanaf de[website](https://www.oracle.com/java/technologies/javase-jdk15-downloads.html).

2.  Aspose.Note-bibliotheek: download de Aspose.Note-bibliotheek en neem deze op in uw Java-project. U kunt deze verkrijgen bij de[download link](https://releases.aspose.com/note/java/).

## Pakketten importeren

Importeer om te beginnen de benodigde pakketten:

```java
import java.io.IOException;
import java.nio.file.Files;
import java.nio.file.Paths;
import java.util.List;
import com.aspose.note.Document;
import com.aspose.note.Image;
```

## Stap 1: Laad het document

Laad eerst het OneNote-document met Aspose.Note:

```java
String dataDir = "Your Document Directory";
Document doc = new Document(dataDir + "Sample1.one");
```

## Stap 2: Haal alle afbeeldingen op

Haal vervolgens alle afbeeldingen uit het document op:

```java
List<Image> list = doc.getChildNodes(Image.class);
System.out.printf("Total Images: %s\n\n", list.size());
```

## Stap 3: Afbeeldingen extraheren

Blader door de lijst met afbeeldingen en sla elke afbeelding op in een bestand:

```java
for (int i = 0; i < list.size(); i++) {
    Image image = list.get(i);
    String outputFile = "ExtractImages_out" + i + "_" + image.getFileName();
    byte[] buffer = image.getBytes();
    Files.write(Paths.get(dataDir + outputFile), buffer);
    System.out.printf("File saved: %s\n", dataDir);
}
```

## Conclusie

Het extraheren van afbeeldingen uit een OneNote-document met behulp van Java kan naadloos worden bereikt met de Aspose.Note-bibliotheek. Door de stappen in deze tutorial te volgen, kunt u moeiteloos afbeeldingen uit uw documenten halen voor verdere verwerking of analyse.

## Veelgestelde vragen

### V1: Kan ik afbeeldingen extraheren uit met een wachtwoord beveiligde OneNote-documenten?

A1: Ja, Aspose.Note ondersteunt ook het extraheren van afbeeldingen uit met een wachtwoord beveiligde documenten.

### V2: Is Aspose.Note compatibel met verschillende versies van Java?

A2: Aspose.Note is compatibel met verschillende versies van Java, wat flexibiliteit voor ontwikkelaars garandeert.

### V3: Kan ik afbeeldingen uit meerdere OneNote-documenten in één keer extraheren?

A3: Absoluut, u kunt door meerdere documenten bladeren en afbeeldingen uit elk ervan extraheren met behulp van Aspose.Note.

### V4: Zijn er beperkingen qua grootte voor de OneNote-documenten?

A4: Aspose.Note verwerkt documenten van verschillende formaten efficiënt, waardoor er geen beperkingen zijn op de documentgrootte voor het extraheren van afbeeldingen.

### V5: Ondersteunt Aspose.Note het extraheren van andere soorten inhoud dan afbeeldingen?

A5: Ja, naast afbeeldingen staat Aspose.Note de extractie van tekst, bijlagen en andere inhoudstypen uit OneNote-documenten toe.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
