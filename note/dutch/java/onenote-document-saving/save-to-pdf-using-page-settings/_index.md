---
title: Opslaan naar PDF met behulp van pagina-instellingen in OneNote - Aspose.Note
linktitle: Opslaan naar PDF met behulp van pagina-instellingen in OneNote - Aspose.Note
second_title: Aspose.Note Java-API
description: Leer hoe u OneNote-documenten opslaat in PDF in Java met behulp van de Aspose.Note-bibliotheek. Stapsgewijze handleiding met codevoorbeelden voor verschillende pagina-instellingen.
weight: 19
url: /nl/java/onenote-document-saving/save-to-pdf-using-page-settings/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Opslaan naar PDF met behulp van pagina-instellingen in OneNote - Aspose.Note

## Invoering

In deze zelfstudie leren we hoe u OneNote-documenten in PDF-indeling kunt opslaan met behulp van verschillende pagina-instellingen met Aspose.Note voor Java. We behandelen twee methoden: opslaan met Letter-pagina-instellingen en opslaan met A4-pagina-instellingen zonder hoogtelimiet.

## Vereisten

Voordat we beginnen, zorg ervoor dat u aan de volgende vereisten voldoet:

1. Java Development Kit (JDK) op uw systeem geïnstalleerd.
2. Aspose.Note voor de Java-bibliotheek gedownload en opgenomen in uw Java-project.
3. Basiskennis van de Java-programmeertaal.

## Pakketten importeren

Zorg ervoor dat u de benodigde pakketten voor het gebruik van Aspose.Note voor Java in uw project hebt geïmporteerd. Hier is de importverklaring:

```java
import com.aspose.note.*;
import java.io.IOException;
import java.nio.file.Paths;
```

## Opslaan naar PDF met behulp van Letter-pagina-instellingen

### Stap 1: Laad het document

Laad eerst het OneNote-document in Aspose.Note:

```java
Document oneFile = new Document("path/to/your/OneNote.one");
```

### Stap 2: Definieer het bestemmingspad

Geef het doelpad voor het PDF-bestand op:

```java
String dst = "path/to/your/SaveToPdfUsingLetterPageSettings.pdf";
```

### Stap 3: Sla het document op

Sla het document op met Letter-pagina-instellingen:

```java
PdfSaveOptions options = new PdfSaveOptions();
options.setPageSettings(PageSettings.getLetter());
oneFile.save(dst, options);
```

## Opslaan naar PDF met A4-pagina-instellingen zonder hoogtelimiet

### Stap 1: Laad het document

Laad op dezelfde manier het OneNote-document in Aspose.Note:

```java
Document oneFile = new Document("path/to/your/OneNote.one");
```

### Stap 2: Definieer het bestemmingspad

Geef het doelpad voor het PDF-bestand op:

```java
String dst = "path/to/your/SaveToPdfUsingA4PageSettingsWithoutHeightLimit.pdf";
```

### Stap 3: Sla het document op

Sla het document op met A4-pagina-instellingen zonder hoogtelimiet:

```java
PdfSaveOptions options = new PdfSaveOptions();
options.setPageSettings(PageSettings.getA4NoHeightLimit());
oneFile.save(dst, options);
```

Nadat u deze stappen heeft gevolgd, heeft u uw OneNote-document met succes opgeslagen in PDF met behulp van verschillende pagina-instellingen.

## Conclusie

In deze zelfstudie hebben we onderzocht hoe u OneNote-documenten in PDF-indeling kunt opslaan met behulp van de Aspose.Note voor Java-bibliotheek. Door het stappenplan te volgen, kunt u deze functionaliteit eenvoudig integreren in uw Java-applicaties.

## Veelgestelde vragen

### Vraag 1: Kan ik de pagina-instellingen verder aanpassen?

A1: Ja, u kunt de pagina-instellingen aanpassen aan uw vereisten met behulp van Aspose.Note voor Java.

### V2: Ondersteunt Aspose.Note andere uitvoerformaten dan PDF?

A2: Ja, Aspose.Note ondersteunt verschillende uitvoerformaten, waaronder afbeeldingen en HTML.

### V3: Is Aspose.Note compatibel met verschillende versies van OneNote-bestanden?

A3: Ja, Aspose.Note ondersteunt OneNote-bestanden van verschillende versies, waaronder .one en .onetoc2.

### V4: Kan ik meerdere OneNote-bestanden in één keer naar PDF converteren?

A4: Ja, u kunt meerdere OneNote-bestanden batchgewijs verwerken met Aspose.Note voor Java.

### Vraag 5: Is er een proefversie beschikbaar voor testdoeleinden?

A5: Ja, u kunt een gratis proefversie van Aspose.Note voor Java krijgen via de website.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
