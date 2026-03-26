---
date: 2026-01-05
description: Leer hoe je de standaardlocale instelt, een OneNote-document laadt, de
  Aspose-licentie instelt, OneNote converteert naar PNG en OneNote opslaat als afbeelding
  met Aspose.Note voor Java.
linktitle: Working with Locales in OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: Standaardlocale instellen in OneNote – Aspose.Note Java
url: /nl/java/onenote-notebook-operations/working-with-locales/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Standaardlocale instellen in OneNote – Aspose.Note Java

## Inleiding

Als u **de standaardlocale moet instellen** tijdens het verwerken van OneNote‑bestanden, maakt Aspose.Note voor Java dit eenvoudig. In deze tutorial lopen we alles door wat u nodig heeft — van het licentiëren van het product tot het laden van een OneNote‑document, het wijzigen van de locale en uiteindelijk het converteren van het bestand naar een PNG‑afbeelding. Aan het einde kunt u taalinstellingen aanpassen en locale‑specifieke uitvoer genereren met slechts een paar regels code.

## Snelle antwoorden
- **Wat doet “standaardlocale instellen”?** Het bepaalt de taal‑ en regionale opmaak die Aspose.Note gebruikt bij het lezen of schrijven van OneNote‑bestanden.  
- **Heb ik een licentie nodig?** Ja — stel de Aspose‑licentie in om de volledige functionaliteit te ontgrendelen.  
- **Welke Java‑versie is vereist?** Elke JDK 8+ wordt ondersteund.  
- **Kan ik OneNote naar PNG converteren?** Absoluut; de API laat u pagina’s als afbeeldingen opslaan.  
- **Is het proces thread‑safe?** Het instellen van de standaardlocale is globaal, dus configureer het één keer bij het opstarten van de applicatie.

## Wat is “standaardlocale instellen” in Aspose.Note?
Het instellen van de standaardlocale vertelt Aspose.Note welke taal‑ en cultuurconventies moeten worden toegepast bij het parseren van datums, getallen en tekst. Dit is essentieel voor multi‑regionale toepassingen die consistente opmaak nodig hebben over verschillende gebruikerslocales.

## Waarom de standaardlocale instellen bij het werken met OneNote?
- **Nauwkeurige gegevensrepresentatie:** Datums en getallen worden correct weergegeven voor de beoogde doelgroep.  
- **Consistente UI‑teksten:** Tekst die uit OneNote wordt gehaald respecteert de taalinstellingen.  
- **Vereenvoudigde conversie:** Wanneer u later een OneNote‑bestand naar PNG of andere formaten converteert, komt de visuele lay-out overeen met de verwachte locale.

## Vereisten

- **Java‑ontwikkelomgeving:** JDK geïnstalleerd en `JAVA_HOME` geconfigureerd.  
- **Aspose.Note‑bibliotheek:** Download de nieuwste JAR via de [downloadlink](https://releases.aspose.com/note/java/).  
- **Een geldig Aspose‑licentiebestand** (gratis proefversie werkt voor testen).

## Importpakketten

Voordat u code schrijft, importeert u de klassen die de benodigde functionaliteit bieden.

```java
import java.io.IOException;
import java.nio.file.Path;
import java.util.Locale;
import com.aspose.note.Document;
import com.aspose.note.License;
import com.aspose.note.LocaleOptions;
```

## Stap 1: Aspose‑licentie instellen

```java
License license = new License();
license.setLicense("licenseFile");
```

Het instellen van de Aspose‑licentie ontgrendelt alle functies, inclusief locale‑beheer en afbeeldingconversie.

## Stap 2: Standaardlocale instellen

```java
java.util.Locale.setDefault(new java.util.Locale("en", "rs"));
```

Hier **stellen we de standaardlocale** in op Engels (`en`) met de landcode `rs`. Pas de taal‑ en landcodes aan naar uw doelregion.

## Stap 3: OneNote‑document laden

```java
String inputFile = "Sample1.one";
Path inputPath = Paths.get(inputFile);

Document oneFile = new Document(inputPath.toString());
```

Deze stap **laadt het OneNote‑document** in het `Document`‑object zodat u met de inhoud kunt werken.

## Stap 4: OneNote naar PNG converteren (OneNote‑bestandsconversie)

```java
oneFile.save("sample.png");
```

De `save`‑methode voert een **OneNote‑bestandsconversie** uit, waarbij het notitieboek (of een specifieke pagina) wordt geëxporteerd als een PNG‑afbeelding — effectief **convert onenote to png** en **save onenote as image**.

## Veelvoorkomende problemen & tips

- **Licentie niet gevonden:** Zorg ervoor dat het pad naar `licenseFile` correct is en dat het bestand leesrechten heeft.  
- **Locale niet toegepast:** Roep `Locale.setDefault` **aan vóór** het laden van het document.  
- **Afbeeldingsoutput ontbreekt:** Controleer of het OneNote‑bestand daadwerkelijk renderbare pagina’s bevat; lege notitieboeken produceren een lege PNG.

## Veelgestelde vragen

**V: Is Aspose.Note compatibel met verschillende versies van Java?**  
A: Ja, Aspose.Note ondersteunt Java 8 en later, waardoor brede compatibiliteit met ontwikkelomgevingen wordt gegarandeerd.

**V: Kan ik Aspose.Note integreren met andere Java‑bibliotheken?**  
A: Absoluut. De API werkt naadloos samen met populaire bibliotheken zoals Apache POI, Jackson en Spring.

**V: Biedt Aspose.Note ondersteuning voor verschillende bestandsformaten?**  
A: Hoewel de kernfocus OneNote‑bestanden is, kan de bibliotheek exporteren naar PNG, JPEG, PDF en andere afbeeldingsformaten.

**V: Is er een community‑forum voor Aspose.Note‑gebruikers om hulp te zoeken en kennis te delen?**  
A: Ja, het Aspose‑community‑forum biedt een platform waar gebruikers met experts kunnen communiceren, vragen kunnen stellen en samenwerken aan oplossingen. Bezoek het [supportforum](https://forum.aspose.com/c/note/28) voor assistentie.

**V: Kan ik Aspose.Note uitproberen voordat ik het koop?**  
A: Zeker, u kunt de mogelijkheden van Aspose.Note verkennen door de gratis proefversie op de website te gebruiken.

## Conclusie

Door deze stappen te volgen heeft u geleerd hoe u **de standaardlocale instelt**, **OneNote‑document laadt**, **Aspose‑licentie configureert** en **OneNote naar PNG converteert** met Aspose.Note voor Java. Deze workflow stelt u in staat locale‑bewuste rapporten en afbeeldingen te genereren die geschikt zijn voor een wereldwijd publiek.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Laatst bijgewerkt:** 2026-01-05  
**Getest met:** Aspose.Note 24.11 for Java  
**Auteur:** Aspose  

---