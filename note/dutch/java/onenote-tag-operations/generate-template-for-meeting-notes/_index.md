---
date: 2026-10-26
description: Leer hoe je selectievakjes toevoegt aan OneNote tijdens het genereren
  van een meeting notes template met Aspose.Note for Java, en pas de font style van
  OneNote eenvoudig aan.
keywords:
- add checkboxes onenote
- generate meeting notes template
- customize font style onenote
- create outline onenote
lastmod: 2026-10-26
linktitle: Genereer Meeting Notes Template met Aspose.Note for Java – Maak Outline
  in OneNote
og_description: Leer hoe je selectievakjes toevoegt aan OneNote tijdens het genereren
  van een meeting notes template met Aspose.Note for Java, en pas de font style van
  OneNote eenvoudig aan.
og_image_alt: 'Developer guide: add checkboxes onenote and generate meeting notes
  template using Aspose.Note for Java'
og_title: Voeg selectievakjes toe aan OneNote en maak notitiesjabloon in Java
schemas:
- author: Aspose
  dateModified: '2026-10-26'
  description: Learn how to add checkboxes onenote while generating a meeting notes
    template with Aspose.Note for Java, and customize font style onenote easily.
  headline: Add checkboxes onenote and create notes template in Java
  type: TechArticle
- questions:
  - answer: You can create a bulleted list and manually mark items, but using `NoteCheckBox`
      provides interactive checkboxes that sync with OneNote’s UI.
    question: How do I add a checklist to OneNote without using checkboxes?
  - answer: Absolutely. Just change the date formatting or pass a custom title string
      to reuse the same structure for each week.
    question: Can I use this template to create a meeting agenda template for weekly
      repeats?
  - answer: Define `ParagraphStyle` objects with your corporate font name, size, and
      color, then apply them to each `RichText` element as shown in Step 1.
    question: What is the best way to customize font style onenote for branding?
  - answer: Yes. After saving the OneNote file, you can load it with Aspose.Note and
      export to PDF using `Document.save("output.pdf", SaveFormat.Pdf)`.
    question: Does Aspose.Note support exporting the outline to PDF?
  - answer: You can set the checkbox state by adding a `NoteCheckBox` tag with the
      `Checked` property set to `true`.
    question: Is there a way to programmatically mark a checkbox as completed?
  type: FAQPage
second_title: Aspose.Note Java API
tags:
- onenote
- Aspose.Note
- Java
- meeting notes template
- checkboxes
title: Voeg selectievakjes toe aan OneNote en maak notitiesjabloon in Java
url: /nl/java/onenote-tag-operations/generate-template-for-meeting-notes/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Vinkvakjes toevoegen in OneNote en notitiesjabloon maken in Java

## Inleiding
In moderne samenwerkingsomgevingen kun je **add checkboxes onenote** snel toevoegen en een gepolijste notitiesjabloon voor vergaderingen genereren zonder handmatige opmaak. Aspose.Note for Java geeft je volledige controle over paginatitels, hiërarchische outlines, lettertype‑styling en interactieve vinkvakjes, zodat je in enkele seconden een herbruikbare agenda kunt maken. Deze gids leidt je stap voor stap—van het importeren van de benodigde klassen tot het opslaan van het uiteindelijke OneNote‑bestand—zodat je je kunt concentreren op de inhoud van de vergadering, niet op saaie UI‑werkzaamheden.

## Snelle antwoorden
- **Wat betekent “add checkboxes onenote”?** Het betekent programmatically interactieve vink‑vakjes in een OneNote‑outline invoegen, net zoals de UI dat doet.  
- **Welke bibliotheek helpt hierbij?** Aspose.Note for Java biedt de volledige API.  
- **Kan ik vinkvakjes aan de outline toevoegen?** Ja – gebruik `NoteCheckBox.createBlueCheckBox()` of andere kleurvarianten.  
- **Heb ik een licentie nodig?** Een gratis proefversie werkt voor ontwikkeling; een commerciële licentie is vereist voor productiegebruik.  
- **Welke Java‑versie wordt ondersteund?** Java 8 en later.

## Wat is add checkboxes onenote?
Add checkboxes onenote voegt een `NoteCheckBox`‑tag toe aan een `RichText`‑element, waardoor een gewone tekstregel wordt omgezet in een interactieve vink‑box die gebruikers direct in de OneNote‑UI kunnen aanvinken of uitvinken, waarbij de status van het vakje behouden blijft over apparaten en consistentie wordt gegarandeerd.

## Waarom Aspose.Note gebruiken voor het genereren van een notitiesjabloon voor vergaderingen?
Aspose.Note verwerkt **meer dan 50 invoer‑ en uitvoerformaten** en kan pagina’s met **tot 500 regels** aan zonder het volledige document in het geheugen te laden, waardoor snelle, geheugen‑efficiënte generatie van grote agenda’s mogelijk is. Het biedt ook een vloeiende API voor styling, ondersteunt Unicode‑tekens en integreert naadloos met andere Aspose‑bibliotheken, waardoor het ideaal is voor enterprise‑scale documentatie‑workflows voor vergaderingen.

## Voorvereisten
- Basiskennis van Java‑programmeren.  
- Aspose.Note for Java‑bibliotheek geïnstalleerd. Je kunt **Aspose.Note for Java downloaden** vanaf de officiële Aspose.Note for Java‑releasepagina: [Aspose.Note for Java release page](https://releases.aspose.com/note/java/).  
- Een IDE zoals Eclipse of IntelliJ IDEA.  

## Pakketten importeren
De klassen `Document`, `Outline`, `ParagraphStyle`, `RichText` en `NoteCheckBox` vormen de kernbouwstenen.  

`Document` vertegenwoordigt het volledige OneNote‑bestand in het geheugen, waardoor pagina’s en inhoud kunnen worden toegevoegd of aangepast.  
`Outline` modelleert de hiërarchische lijststructuur die in OneNote wordt weergegeven, waardoor geneste opsommingstekens en nummering mogelijk zijn.  
`ParagraphStyle` definieert herbruikbare lettertype‑ en alinea‑attributen die op meerdere `RichText`‑elementen kunnen worden toegepast.  
`RichText` bevat de feitelijke tekstinhoud van een alinea en kan tags bevatten zoals `NoteCheckBox`.  
`NoteCheckBox` maakt een interactieve vinkvak‑tag die aan een `RichText`‑alinea kan worden gekoppeld.

```java
import com.aspose.note.*;
import java.io.IOException;
import java.nio.file.Paths;
import java.text.DateFormat;
import java.time.Instant;
import java.util.Date;
import java.util.Locale;
```

## Stap 1: documentstructuur maken
Instantieer eerst een `Document`, stel een paginatitel in en definieer twee herbruikbare `ParagraphStyle`‑objecten—één voor koppen en één voor de hoofdtekst.  

`ParagraphStyle`‑objecten laten je dezelfde lettertypefamilie, grootte en kleur op meerdere alinea’s toepassen zonder code te herhalen.

```java
// The path to the documents directory.
String dataDir = "Your Document Directory";
// Create an object of the Document class
ParagraphStyle headerStyle = new ParagraphStyle()
                                    .setFontName("Calibri")
                                    .setFontSize(16);
ParagraphStyle bodyStyle = new ParagraphStyle()
                                    .setFontName("Calibri")
                                    .setFontSize(12);
DateFormat dateFormat = DateFormat.getDateInstance(DateFormat.SHORT, Locale.US);
Document d = new Document();
boolean restartFlag = true;
RichText titleText = new RichText().append(String.format("Weekly meeting %s", dateFormat.format(Date.from(Instant.now()))));
titleText.setParagraphStyle(ParagraphStyle.getDefault());
Title title = new Title();
title.setTitleText(titleText);
Page page = new Page();
page.setTitle(title);
d.appendChildLast(page);
```

*Wat we hebben gedaan:*  
- `headerStyle` gedefinieerd voor koppen en `bodyStyle` voor gewone tekst.  
- Een `Document` aangemaakt en een `Title` toegevoegd die de datum van vandaag bevat, waardoor de pagina een duidelijke kop krijgt.

## Stap 2: belangrijke punten outline‑en
Voeg vervolgens een `Outline`‑object toe aan de pagina en vul het met secties zoals “Agenda”, “Discussion Items” en “Action Items”.  

Het `Outline`‑object vertegenwoordigt de hiërarchische lijst die je in OneNote ziet. Met `createListNumberingStyle` genereren we een genummerde lijst die voor elke nieuwe sectie kan worden herstart.

```java
Outline outline = page.appendChildLast(new Outline());
outline.setVerticalOffset(30);
outline.setHorizontalOffset(30);
RichText richText = outline.appendChildLast(new OutlineElement()).appendChildLast(new RichText());
richText.append("Important");
richText.setParagraphStyle(headerStyle);
for (String e: new String[] { "First", "Second", "Third" })
{
    OutlineElement outlineElement = outline.appendChildLast(new OutlineElement());
    outlineElement.setNumberList(createListNumberingStyle(bodyStyle, restartFlag));
    richText = outlineElement.appendChildLast(new RichText());
    richText.append(e);
    richText.setParagraphStyle(bodyStyle);
    restartFlag = false;
}
```

*Waarom dit belangrijk is:*  
- De outline‑hiërarchie spiegelt de handmatige structuur die je in OneNote zou typen, waardoor consistentie over alle gegenereerde pagina’s wordt gewaarborgd.  
- Nummeringsstijlen houden elke agendasectie overzichtelijk en makkelijk te volgen.

## Stap 3: actiepunten markeren (hoe vinkvakjes toe te voegen)
Actiepunten hebben een visueel signaal nodig. Door een `NoteCheckBox`‑tag aan elk `RichText`‑element te koppelen, enable je **add checkboxes onenote** direct binnen de outline.  

`NoteCheckBox.createBlueCheckBox()` maakt een blauw‑aangeduid vakje; andere kleuren zijn beschikbaar voor branding.

```java
richText = outline.appendChildLast(new OutlineElement()).appendChildLast(new RichText());
richText.append("TO DO");
richText.setParagraphStyle(headerStyle);
richText.setSpaceBefore(15);
restartFlag = true;
for (String e: new String[] { "First", "Second", "Third" })
{
    OutlineElement outlineElement = outline.appendChildLast(new OutlineElement());
    outlineElement.setNumberList(createListNumberingStyle(bodyStyle, restartFlag));
    richText = outlineElement.appendChildLast(new RichText());
    richText.append(e);
    richText.setParagraphStyle(bodyStyle);
    richText.getTags().add(NoteCheckBox.createBlueCheckBox());
    restartFlag = false;
}
```

*Pro tip:* Gebruik `NoteCheckBox.createBlueCheckBox()` voor een blauw vinkvak; andere kleuren zijn beschikbaar als je een andere visuele stijl nodig hebt.

## Stap 4: lettertype‑stijl onenote aanpassen
Om de notities van de vergadering in lijn te houden met je merk, pas je de eerder gedefinieerde `ParagraphStyle`‑objecten toe op elk `RichText`‑element.  

Het instellen van de eigenschappen `FontName`, `FontSize` en `FontColor` zorgt ervoor dat de gegenereerde pagina overeenkomt met je corporate style guide.

```java
// Save OneNote document
d.save(Paths.get(dataDir, "meetingNotes.one").toString());
```

## Stap 5: het document opslaan
Schrijf tenslotte het OneNote‑bestand naar schijf. Het bestand kan direct worden geopend in de OneNote‑desktopapp, en je kunt het later ook naar PDF converteren indien nodig.

*Direct antwoord:* Roep `document.save("MeetingTemplate.one")` aan—de API schrijft een volledig compatibel OneNote‑bestand dat onmiddellijk opent in de OneNote‑client.

## Veelvoorkomende problemen en oplossingen
| Probleem | Oplossing |
|-------|----------|
| **Checkboxes verschijnen niet** | Zorg ervoor dat je `richText.getTags().add(NoteCheckBox.createBlueCheckBox())` hebt aangeroepen na het instellen van de alinea‑stijl. |
| **Lettertypen zien er anders uit in OneNote** | Controleer of de lettertype‑naam (bijv. “Calibri”) geïnstalleerd is op de machine waarop OneNote het bestand opent. |
| **Outline niet ingesprongen** | Pas `setVerticalOffset` en `setHorizontalOffset` aan op het `Outline`‑object. |
| **Nummering start onverwacht opnieuw** | Gebruik de `restartFlag` correct; stel deze alleen in op `true` voor de eerste lijst in een nieuwe sectie. |

## Veelgestelde vragen
### Hoe voeg ik add checkboxes onenote toe?
Laad een `RichText`‑element en roep `richText.getTags().add(NoteCheckBox.createBlueCheckBox())` aan. De tag verandert de regel in een interactieve checkbox die gebruikers binnen OneNote kunnen aanvinken.

### Kan ik de lettertype‑stijlen in mijn notities aanpassen?
Ja. Maak `ParagraphStyle`‑objecten met de gewenste `FontName`, `FontSize` en `FontColor`, en wijs ze toe aan elk `RichText`‑element zoals getoond in Stap 1.

### Is Aspose.Note compatibel met andere Java‑bibliotheken?
Aspose.Note werkt naast andere Aspose‑producten (PDF, Cells, Slides) en standaard Java‑bibliotheken, waardoor je bewerkingen kunt ketenen zoals het converteren van het gegenereerde OneNote‑bestand naar PDF.

### Hoe kan ik extra secties aan mijn notities toevoegen?
Herbruik hetzelfde patroon: maak een nieuw `Outline`‑knooppunt, pas een `ParagraphStyle` toe, en voeg eventueel vinkvakjes toe. De API is volledig herhaalbaar voor elk aantal secties.

### Zijn er licentie‑overwegingen voor Aspose.Note?
Raadpleeg de [Aspose.Note‑documentatie](https://reference.aspose.com/note/java/) voor volledige licentie‑details. Een gratis proefversie is voldoende voor ontwikkeling; een commerciële licentie is vereist voor productie‑implementaties.

### Is er een proefversie beschikbaar voor Aspose.Note?
Ja, je kunt de **gratis Aspose.Note‑proefdownloadpagina** bezoeken: [Aspose.Note trial download page](https://releases.aspose.com/).

## FAQ
**Q: Hoe voeg ik een checklist toe aan OneNote zonder vinkvakjes?**  
A: Je kunt een opsomming maken en items handmatig markeren, maar met `NoteCheckBox` krijg je interactieve vinkvakjes die synchroniseren met de OneNote‑UI.

**Q: Kan ik deze sjabloon gebruiken om wekelijks een vergaderagenda te maken?**  
A: Absoluut. Pas gewoon de datumopmaak aan of geef een aangepaste titel‑string door om dezelfde structuur elke week opnieuw te gebruiken.

**Q: Wat is de beste manier om lettertype‑stijl onenote aan te passen voor branding?**  
A: Definieer `ParagraphStyle`‑objecten met je bedrijfslettertype, -grootte en -kleur, en pas ze toe op elk `RichText`‑element zoals getoond in Stap 1.

**Q: Ondersteunt Aspose.Note het exporteren van de outline naar PDF?**  
A: Ja. Na het opslaan van het OneNote‑bestand kun je het laden met Aspose.Note en exporteren naar PDF via `Document.save("output.pdf", SaveFormat.Pdf)`.

**Q: Is er een manier om programmatically een checkbox als voltooid te markeren?**  
A: Je kunt de checkbox‑status instellen door een `NoteCheckBox`‑tag toe te voegen met de eigenschap `Checked` ingesteld op `true`.

---

**Laatst bijgewerkt:** 2026-10-26  
**Getest met:** Aspose.Note for Java 24.11 (latest at time of writing)  
**Auteur:** Aspose

## Gerelateerde tutorials

- [Add Tags to OneNote – Create Tagged OneNote Document with Aspose.Note](/note/java/onenote-tag-operations/)
- [How to Customize OneNote Styles with Aspose.Note for Java](/note/java/onenote-styles/)
- [Create OneNote Document Java – Aspose Note Java Tutorial](/note/java/onenote-document-manipulation/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}