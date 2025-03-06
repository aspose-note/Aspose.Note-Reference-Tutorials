---
title: Nieuw afbeeldingsknooppunt met tag toevoegen in OneNote - Aspose.Note
linktitle: Nieuw afbeeldingsknooppunt met tag toevoegen in OneNote - Aspose.Note
second_title: Aspose.Note Java-API
description: Leer hoe u een nieuw afbeeldingsknooppunt met een tag toevoegt in OneNote met behulp van Aspose.Note voor Java. Verbeter moeiteloos uw Java-programmeervaardigheden.
weight: 10
url: /nl/java/onenote-tag-operations/add-new-image-node-with-tag/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Nieuw afbeeldingsknooppunt met tag toevoegen in OneNote - Aspose.Note

## Invoering
Op het gebied van Java-programmeren onderscheidt Aspose.Note zich als een krachtig hulpmiddel voor het gemakkelijk verwerken van OneNote-documenten. Als u uw vaardigheden wilt verbeteren en wilt leren hoe u een nieuw afbeeldingsknooppunt met een tag in OneNote kunt toevoegen met behulp van Aspose.Note, dan bent u hier aan het juiste adres. Deze stapsgewijze handleiding begeleidt u door het proces, zodat u elk concept grondig begrijpt.
## Vereisten
Voordat we ingaan op de tutorial, zorgen we ervoor dat je alles hebt wat je nodig hebt:
1.  Aspose.Note voor Java: Zorg ervoor dat de Aspose.Note-bibliotheek is geïnstalleerd. Zo niet, dan kunt u deze downloaden[hier](https://releases.aspose.com/note/java/).
2. Java-ontwikkelomgeving: Zorg ervoor dat er een werkende Java-ontwikkelomgeving op uw computer is geïnstalleerd.
Nu we aan de voorwaarden hebben voldaan, gaan we verder met de volgende stappen.
## Pakketten importeren
Begin in uw Java-project met het importeren van de benodigde pakketten:
```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.Image;
import com.aspose.note.NoteTag;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.SaveFormat;
import com.aspose.note.TagIcon;
```
## Stap 1: Documentobject maken
```java
// Het pad naar de documentenmap.
String dataDir = "Your Document Directory";
// maak een object van de klasse Document
Document doc = new Document();
```
## Stap 2: Initialiseer het paginaklasse-object
```java
// initialiseer het Page-klasseobject
Page page = new Page();
```
## Stap 3: Initialiseer het omtrekklasseobject
```java
// initialiseer het Outline-klasseobject
Outline outline = new Outline();
```
## Stap 4: Initialiseer het OutlineElement-klasseobject
```java
// initialiseer het OutlineElement-klasseobject
OutlineElement outlineElem = new OutlineElement();
```
## Stap 5: Afbeelding laden en invoegen
```java
// laad een afbeelding
Image image = new Image(null, dataDir + "Input.jpg");
// voeg een afbeelding in het documentknooppunt in
outlineElem.appendChildLast(image);
```
## Stap 6: Voeg een notitietag toe aan de afbeelding
```java
// voeg een gele sternotitietag toe aan de afbeelding
NoteTag noteTag = NoteTag.createYellowStar();
image.getTags().add(noteTag);
```
## Stap 7: Voeg een overzichtselementknooppunt toe
```java
// voeg een overzichtselementknooppunt toe
outline.appendChildLast(outlineElem);
```
## Stap 8: Voeg een overzichtsknooppunt toe
```java
// voeg een overzichtsknooppunt toe
page.appendChildLast(outline);
```
## Stap 9: Paginaknooppunt toevoegen
```java
// paginaknooppunt toevoegen
doc.appendChildLast(page);
```
## Stap 10: OneNote-document opslaan
```java
// sla het OneNote-document op als PDF
doc.save(dataDir + "AddNewImageNodeWithTag_out.pdf", SaveFormat.Pdf);
```
Gefeliciteerd! U hebt met succes een nieuw afbeeldingsknooppunt met een tag toegevoegd in OneNote met behulp van Aspose.Note voor Java.
## Conclusie
 Het beheersen van Aspose.Note voor Java opent opwindende mogelijkheden bij het manipuleren van OneNote-documenten. Door deze tutorial te volgen, heb je een praktische vaardigheid verworven die op verschillende projecten kan worden toegepast. Blijf de Aspose.Note-documentatie verkennen[hier](https://reference.aspose.com/note/java/)voor meer geavanceerde functies en mogelijkheden.
## Veelgestelde vragen
### Waar kan ik Aspose.Note-documentatie vinden?
 U kunt de documentatie vinden[hier](https://reference.aspose.com/note/java/).
### Hoe download ik Aspose.Note voor Java?
 Je kunt het downloaden vanaf de releasepagina[hier](https://releases.aspose.com/note/java/).
### Is er een gratis proefversie beschikbaar?
 Ja, u heeft toegang tot de gratis proefperiode[hier](https://releases.aspose.com/).
### Waar kan ik ondersteuning krijgen voor Aspose.Note?
 Bezoek het communityforum[hier](https://forum.aspose.com/c/note/28) Voor ondersteuning.
### Heb ik een tijdelijke licentie nodig?
 Indien nodig kunt u een tijdelijke licentie verkrijgen[hier](https://purchase.aspose.com/temporary-license/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
