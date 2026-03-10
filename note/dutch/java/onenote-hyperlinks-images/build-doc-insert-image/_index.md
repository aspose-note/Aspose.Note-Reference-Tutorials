---
date: 2025-12-20
description: Leer hoe je een afbeelding toevoegt aan OneNote met Aspose.Note voor
  Java. Stapsgewijze handleiding om OneNote‑documenten te bouwen en afbeeldingen via
  code in te voegen.
linktitle: How to add picture to OneNote using Java – Build Document and Insert Image
second_title: Aspose.Note Java API
title: Hoe een afbeelding toevoegen aan OneNote met Java – Document bouwen en afbeelding
  invoegen
url: /nl/java/onenote-hyperlinks-images/build-doc-insert-image/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hoe een afbeelding toevoegen aan OneNote met Java – Document bouwen en afbeelding invoegen

## Introductie

In deze tutorial leer je **hoe je een afbeelding toevoegt aan OneNote** met de Aspose.Note Java API. We lopen stap voor stap door het maken van een OneNote‑document vanaf nul, het invoegen van een afbeelding, en het opslaan van het resultaat als PDF. Of je nu een rapportagetool bouwt, notities automatiseert, of gewoon grafische elementen programmatisch moet insluiten, deze gids biedt een duidelijke, praktische route.

## Snelle antwoorden
- **Welke bibliotheek heb ik nodig?** Aspose.Note for Java.
- **Kan ik elk afbeeldingsformaat invoegen?** JPEG, PNG, BMP, GIF en meer worden ondersteund.
- **Welke uitvoerformaten zijn beschikbaar?** Je kunt opslaan als OneNote, PDF, XPS, HTML, enz.
- **Heb ik een licentie nodig voor productie?** Ja, een commerciële licentie is vereist voor niet‑trial gebruik.
- **Is de code cross‑platform?** Absoluut – Java draait op Windows, Linux en macOS.

## Wat betekent “afbeelding toevoegen aan OneNote”?
Een afbeelding toevoegen aan OneNote betekent dat je programmatisch een afbeeldingsbestand in een OneNote‑pagina insluit zodat deze naast tekst, outlines of andere elementen verschijnt. De Aspose.Note API abstraheert het OneNote‑bestandformaat, zodat je je kunt concentreren op de inhoud in plaats van op de onderliggende XML‑structuur.

## Waarom afbeelding toevoegen aan OneNote met Java?
- **Automatisering:** Genereer automatisch notulen met screenshots.
- **Consistentie:** Zorg ervoor dat elke pagina dezelfde lay-out en branding volgt.
- **Integratie:** Combineer gegevens uit andere systemen (bijv. grafieken) direct in OneNote‑notebooks.
- **Cross‑platform:** Java laat je dezelfde code uitvoeren op elke server of desktopomgeving.

## Vereisten

Voordat we beginnen, zorg dat je het volgende hebt:

1. **Java Development Kit (JDK)** – elke recente versie (8 of later).  
2. **Aspose.Note for Java bibliotheek** – download deze van de [website](https://releases.aspose.com/note/java/).  
3. **IDE** – IntelliJ IDEA, Eclipse, of een andere Java‑compatibele editor naar keuze.  

## Pakketten importeren

Begin met het importeren van de benodigde klassen in je Java‑bronbestand:

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.HorizontalAlignment;
import com.aspose.note.Image;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.SaveFormat;
```

## Stapsgewijze gids

### Stap 1: Document opzetten

Maak een nieuw OneNote‑document en een paginacontainer waarin de inhoud wordt geplaatst.

```java
String dataDir = "Your Document Directory";
Document doc = new Document();
Page page = new Page();
```

### Stap 2: Initialiseer de Outline

Een *outline* fungeert als een container voor elementen zoals tekst en afbeeldingen. We stellen de offsets op nul in zodat de inhoud begint in de linkerbovenhoek.

```java
Outline outline = new Outline();
outline.setVerticalOffset(0);
outline.setHorizontalOffset(0);
```

### Stap 3: Afbeelding laden en uitlijnen

Laad de afbeelding die je wilt insluiten en lijn deze uit aan de rechterkant van de pagina. Dit is waar we daadwerkelijk **afbeelding toevoegen aan OneNote**.

```java
Image image = new Image(null, dataDir + "Input.jpg");
image.setAlignment(HorizontalAlignment.Right);
```

### Stap 4: Bevestig de afbeelding aan een Outline‑element

Plaats de afbeelding binnen een `OutlineElement`. Deze stap koppelt het visuele object aan de outline‑hiërarchie van het document.

```java
OutlineElement outlineElem = new OutlineElement();
outlineElem.appendChildLast(image);
```

### Stap 5: Stel de documentstructuur samen

Voeg het outline‑element toe aan de outline, koppel vervolgens de outline aan de pagina, en voeg ten slotte de pagina toe aan het document.

```java
outline.appendChildLast(outlineElem);
page.appendChildLast(outline);
doc.appendChildLast(page);
```

### Stap 6: Sla het OneNote‑document op

Sla het document op schijf op. In dit voorbeeld exporteren we naar PDF, maar je kunt ook opslaan als een native OneNote‑bestand (`.one`) door het `SaveFormat` aan te passen.

```java
try {
    doc.save(dataDir + "NewOneNotedocument_out", SaveFormat.Pdf);
} catch (IOException e) {
    e.printStackTrace();
}
```

## Veelvoorkomende problemen en oplossingen

| Probleem | Waarom het gebeurt | Oplossing |
|----------|--------------------|-----------|
| **Afbeelding verschijnt niet** | Verkeerd bestandspad of niet‑ondersteund formaat. | Controleer of `dataDir` naar de juiste map wijst en gebruik een ondersteund afbeeldingsformaat (JPEG, PNG, enz.). |
| **Document opgeslagen als lege PDF** | Outline‑offsets onjuist ingesteld. | Zorg dat `setVerticalOffset(0)` en `setHorizontalOffset(0)` worden aangeroepen, of pas de offsets aan zodat de inhoud binnen de paginagrenzen valt. |
| **IOException bij opslaan** | Doelmap bestaat niet of er ontbreken schrijfrechten. | Maak de map vooraf aan of voer het programma uit met de juiste permissies. |

## Veelgestelde vragen

**Q1: Waar kan ik de documentatie voor Aspose.Note voor Java vinden?**  
A1: U kunt de documentatie raadplegen [hier](https://reference.aspose.com/note/java/).

**Q2: Hoe download ik Aspose.Note voor Java?**  
A2: U kunt Aspose.Note voor Java downloaden van de [downloadpagina](https://releases.aspose.com/note/java/).

**Q3: Is er een gratis proefversie beschikbaar voor Aspose.Note voor Java?**  
A3: Ja, u kunt een gratis proefversie krijgen via de [website](https://releases.aspose.com/).

**Q4: Waar kan ik ondersteuning krijgen voor Aspose.Note voor Java?**  
A4: Voor ondersteuning kunt u het [Aspose.Note‑forum](https://forum.aspose.com/c/note/28) bezoeken.

**Q5: Kan ik een tijdelijke licentie verkrijgen voor Aspose.Note voor Java?**  
A5: Ja, u kunt een tijdelijke licentie aanvragen [hier](https://purchase.aspose.com/temporary-license/).

---

**Laatst bijgewerkt:** 2025-12-20  
**Getest met:** Aspose.Note for Java 24.12 (latest)  
**Auteur:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}