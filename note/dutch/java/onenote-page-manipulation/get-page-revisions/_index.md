---
date: 2026-01-10
description: Leer de aspose.note‑paginarevisies‑tutorial voor Java – haal OneNote‑paginarevisies
  programmeringsmatig op met Aspose.Note. Volg onze stap‑voor‑stap‑gids.
linktitle: Get Page Revisions in OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: aspose.note paginarevisies tutorial – Haal paginarevisies op in OneNote
url: /nl/java/onenote-page-manipulation/get-page-revisions/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Pagina-revisies ophalen in OneNote - Aspose.Note

OneNote is een krachtig notitie‑platform, en wanneer je wijzigingen moet auditen, laat de **aspose.note page revisions tutorial** je precies zien hoe je de revisiegeschiedenis kunt ophalen met slechts een paar regels Java‑code. In deze gids lopen we alles door wat je nodig hebt — van het instellen van de omgeving tot het afdrukken van de details van elke revisie — zodat je bewerkingen, bijdragen van auteurs en tijdstempels moeiteloos kunt bijhouden.

## Snelle antwoorden
- **Waar gaat de tutorial over?** Het ophalen van de paginarevisiegeschiedenis uit een OneNote‑bestand met Aspose.Note voor Java.  
- **Welke bibliotheekversie is vereist?** Elke recente Aspose.Note voor Java‑release die `LoadOptions.setLoadHistory` ondersteunt.  
- **Heb ik een licentie nodig?** Een tijdelijke evaluatielicentie werkt voor testen; een commerciële licentie is vereist voor productie.  
- **Kan ik revisies wijzigen?** De API is alleen‑lezen voor revisies; je kunt ze alleen ophalen.  
- **Wat zijn de belangrijkste vereisten?** Java JDK, Aspose.Note voor Java, en een OneNote‑document met revisiegegevens.

## Wat is de “aspose.note page revisions tutorial”?
De tutorial laat zien hoe je programmatisch toegang krijgt tot de historische versies van een OneNote‑pagina. Elke revisie bevat metadata zoals de auteur, aanmaaktijd en wijzigingstijd, waardoor je auditsporen of wijzigingslog‑functies in je applicaties kunt bouwen.

## Waarom Aspose.Note gebruiken voor het bijhouden van paginarevisies?
- **Geen UI‑afhankelijkheid** – werkt volledig in code, perfect voor backend‑services.  
- **Cross‑platform** – Java draait op Windows, Linux en macOS.  
- **Volledige controle** – haal elke revisie‑eigenschap op zonder OneNote handmatig te openen.  
- **Prestaties** – het laden van de geschiedenis is geoptimaliseerd, zodat zelfs grote notitieblokken snel worden verwerkt.

## Vereisten

### 1. Java Development Kit (JDK)
Zorg ervoor dat een recente JDK (8 of hoger) is geïnstalleerd en `JAVA_HOME` is ingesteld.

### 2. Aspose.Note for Java
Download de bibliotheek van de [download link](https://releases.aspose.com/note/java/).

### 3. Voorbeeld OneNote‑document
Maak of verkrijg een OneNote‑bestand (bijv. `Sample1.one`) dat pagina's met revisiegeschiedenis bevat.

## Pakketten importeren
Importeer eerst de benodigde Aspose.Note‑klassen.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.LoadOptions;
import com.aspose.note.Page;
```

## Stapsgewijze implementatie

### Stap 1: Documentmap instellen
Definieer de map waarin je OneNote‑bestand zich bevindt.

```java
String dataDir = "Your Document Directory";
```

### Stap 2: OneNote‑document laden met geschiedenis ingeschakeld
Schakel de `LoadOptions`‑vlag in om revisiegegevens op te halen.

```java
LoadOptions loadOptions = new LoadOptions();
loadOptions.setLoadHistory(true);
Document document = new Document(dataDir + "Sample1.one", loadOptions);
```

### Stap 3: De eerste pagina ophalen
Pak het eerste paginapunt; dit zal het referentiepunt zijn voor het ophalen van de geschiedenis.

```java
Page firstPage = document.getFirstChild();
```

### Stap 4: Door paginarevisies itereren
Loop door elke revisie en print nuttige metadata zoals tijdstempels, titel, niveau en auteur.

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

> **Pro tip:** Als je revisies wilt filteren op een specifieke auteur of datumbereik, voeg dan eenvoudig conditionele controles toe binnen de `for`‑lus.

## Veelvoorkomende problemen & oplossingen
- **Geen revisies geretourneerd:** Controleer of `loadOptions.setLoadHistory(true)` wordt aangeroepen vóór het laden van het document.  
- **Null auteur of titel:** Sommige oudere OneNote‑versies slaan deze velden mogelijk niet op; behandel `null`‑waarden op een nette manier.  
- **Prestatievertraging bij grote notitieblokken:** Laad alleen de secties die je nodig hebt of vergroot de JVM‑heap‑grootte.

## Veelgestelde vragen

**Q1: Kan ik Aspose.Note voor Java gebruiken om paginarevisies te wijzigen?**  
A1: Nee, de API ondersteunt momenteel alleen alleen‑lezen toegang tot paginarevisies.

**Q2: Is Aspose.Note voor Java compatibel met verschillende versies van OneNote‑documenten?**  
A2: Ja, het werkt met verschillende OneNote‑bestandsformaten, waardoor naadloze verwerking over versies heen mogelijk is.

**Q3: Vereist Aspose.Note voor Java een licentie om te gebruiken?**  
A3: Een commerciële licentie is vereist voor productiegebruik, maar een tijdelijke evaluatielicentie is beschikbaar voor testen.

**Q4: Kan ik ondersteuning krijgen als ik problemen ondervind bij het gebruik van Aspose.Note voor Java?**  
A4: Ja, je kunt vragen stellen op het Aspose.Note‑forum [hier](https://forum.aspose.com/c/note/28).

**Q5: Is er een gratis proefversie beschikbaar voor Aspose.Note voor Java?**  
A5: Ja, je kunt een gratis proefversie downloaden van de [website](https://releases.aspose.com/).

---

**Laatst bijgewerkt:** 2026-01-10  
**Getest met:** Aspose.Note for Java (latest release)  
**Auteur:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}