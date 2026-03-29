---
date: 2026-03-29
description: Leer hoe u de taal voor tekst in OneNote instelt met Aspose.Note voor
  Java. Deze stapsgewijze handleiding laat u zien hoe u een OneNote‑document maakt,
  de teksttaal wijzigt en het OneNote‑bestand efficiënt opslaat.
linktitle: Set Proofing Language for Text in OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: Hoe de taal voor tekst in OneNote instellen – Aspose.Note
url: /nl/java/onenote-text-manipulation/set-proofing-language-for-text/
weight: 22
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hoe de taal voor tekst in OneNote instellen – Aspose.Note

## Introductie
Als je **hoe de taal in te stellen** voor specifieke stukjes tekst in een OneNote-notitieboek nodig hebt, maakt Aspose.Note voor Java het eenvoudig. In deze tutorial leer je hoe je een OneNote‑document maakt, de teksttaal wijzigt voor individuele woorden of zinnen, en uiteindelijk het OneNote‑bestand opslaat met de juiste proefleestaal toegepast. Aan het einde begrijp je waarom het instellen van de taal belangrijk is voor spelling‑controle en lokalisatie, en heb je een kant‑klaar code‑voorbeeld.

## Snelle antwoorden
- **Wat beïnvloedt “set language”?** Het vertelt OneNote welke proeflezen‑woordenboek te gebruiken voor spelling‑ en grammaticacontrole.  
- **Kan ik verschillende talen in dezelfde notitie instellen?** Ja, je kunt een taal toewijzen aan elke tekstrun.  
- **Heb ik een licentie nodig voor Aspose.Note?** Een gratis proefversie werkt voor testen; een commerciële licentie is vereist voor productie.  
- **Welke Java‑versies worden ondersteund?** Aspose.Note voor Java ondersteunt Java 8 en nieuwer.  
- **Is de output een .one‑bestand?** Ja, het document wordt opgeslagen als een OneNote *.one*‑bestand.

## Voorwaarden
Voordat je in de code duikt, zorg dat je het volgende hebt:

1. **Java Development Environment** – JDK 8 of hoger geïnstalleerd en geconfigureerd.  
2. **Aspose.Note for Java Library** – Download en installeer de bibliotheek via de [download link](https://releases.aspose.com/note/java/).  
3. **Document Directory** – Maak een map op je computer waar het gegenereerde OneNote‑bestand wordt opgeslagen.

## Waarom taal voor tekst in OneNote instellen?
Het instellen van de proefleestaal zorgt ervoor dat spelling‑controle, grammaticatips en zoekindexering correct werken voor meertalige inhoud. Dit is vooral nuttig voor:

- **Globale teams** die samenwerken aan één notitieblok.  
- **Gelokaliseerde documentatie** waarbij elke sectie in een andere taal kan zijn.  
- **Data‑gedreven toepassingen** die programmatisch notities genereren voor gebruikers wereldwijd.

## Pakketten importeren
Begin met het importeren van de benodigde Aspose.Note‑klassen en Java‑hulpmiddelen.

```java
import com.aspose.note.*;
import java.io.IOException;
import java.nio.file.Paths;
import java.util.Locale;
```

## Stap 1: Document en pagina instellen
Maak een nieuw OneNote‑document en een pagina die je inhoud zal bevatten. Deze stap toont ook **create OneNote document**.

```java
// The path to the documents directory.
String dataDir = "Your Document Directory";
Document document = new Document();
Page page = new Page();
```

## Stap 2: Outline en outline‑element maken
Een outline is de container voor notitieboekinhoud. Hier bouwen we de structuur die later de taalspecifieke tekst zal bevatten.

```java
Outline outline = new Outline();
OutlineElement outlineElem = new OutlineElement();
```

## Stap 3: Rich‑text toevoegen met taalinstellingen
Nu **wijzigen we de teksttaal** door een `TextStyle` met een specifieke `Locale` aan elk tekstsegment toe te voegen. Dit demonstreert **set language for text**.

```java
RichText text = new RichText()
                        .append("United States", new TextStyle().setLanguage(Locale.forLanguageTag("en-US")))
                        .append(" Germany", new TextStyle().setLanguage(Locale.forLanguageTag("de-DE")))
                        .append(" China", new TextStyle().setLanguage(Locale.forLanguageTag("zh-CN")));
text.setParagraphStyle(ParagraphStyle.getDefault());
```

## Stap 4: Elementen organiseren en opslaan
Stel de outline‑hiërarchie samen, koppel deze aan de pagina, en sla tenslotte het **OneNote‑bestand** op met de toegepaste taalinstellingen.

```java
outlineElem.appendChildLast(text);
outline.appendChildLast(outlineElem);
page.appendChildLast(outline);
document.appendChildLast(page);
document.save(Paths.get(dataDir, "SetProofingLanguageForText.one").toString()); 
```

## Veelvoorkomende valkuilen & tips
- **Locale‑formaat** – Gebruik de IETF BCP‑47‑tag (bijv. `en-US`, `de-DE`). Een onjuiste tag valt terug op de taal van het document.  
- **Bestandspad** – Zorg ervoor dat `dataDir` naar een bestaande map wijst; anders gooit `document.save` een `IOException`.  
- **Pro tip:** Als je de taal voor een hele alinea wilt instellen, pas dan de `TextStyle` toe op de `ParagraphStyle` in plaats van op elke `append`‑aanroep.

## Conclusie
Je hebt zojuist geleerd **hoe de taal** voor individuele tekstfragmenten in een OneNote‑notitieboek in te stellen met Aspose.Note voor Java. Deze mogelijkheid stelt je in staat om **OneNote‑documenten** programmatisch te **maken**, **teksttaal** dynamisch te **wijzigen**, en **OneNote‑bestanden** op te slaan met nauwkeurige proefleestmetadata.

## Veelgestelde vragen

**Q: Kan ik de proefleestaal instellen voor andere talen die niet in het voorbeeld staan?**  
A: Absoluut! Voeg extra `append`‑aanroepen toe met de gewenste `Locale.forLanguageTag("xx-XX")`.

**Q: Is Aspose.Note voor Java compatibel met de nieuwste Java‑versies?**  
A: Ja, de bibliotheek wordt regelmatig bijgewerkt om de nieuwste Java‑releases te ondersteunen.

**Q: Hoe kan ik fouten afhandelen tijdens het taal‑instellingsproces?**  
A: Plaats de opslaactie in een `try‑catch`‑blok om `IOException` of `AsposeException` op te vangen.

**Q: Kan ik deze code integreren in een webapplicatie?**  
A: Zeker. Voeg gewoon de Aspose.Note‑JAR toe aan de classpath van je webproject en zorg dat de server schrijfrechten heeft voor de doelmap.

**Q: Waar vind ik extra voorbeelden en documentatie voor Aspose.Note voor Java?**  
A: Bekijk de [documentation](https://reference.aspose.com/note/java/) voor een volledige lijst van API’s en voorbeeldprojecten.

---

**Laatst bijgewerkt:** 2026-03-29  
**Getest met:** Aspose.Note for Java 24.12  
**Auteur:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}