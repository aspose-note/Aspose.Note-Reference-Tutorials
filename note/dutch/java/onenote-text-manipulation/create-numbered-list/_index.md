---
title: Maak een genummerde lijst in OneNote - Aspose.Note
linktitle: Maak een genummerde lijst in OneNote - Aspose.Note
second_title: Aspose.Note Java-API
description: Leer hoe u moeiteloos een genummerde lijst kunt maken in OneNote met Aspose.Note voor Java. Download een gratis proefversie en duik in de wereld van Java-ontwikkeling!
weight: 14
url: /nl/java/onenote-text-manipulation/create-numbered-list/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Maak een genummerde lijst in OneNote - Aspose.Note

## Invoering
Aspose.Note voor Java stelt Java-ontwikkelaars in staat naadloos met Microsoft OneNote-bestanden te werken. In deze zelfstudie begeleiden we u bij het maken van een genummerde lijst in OneNote met de krachtige Aspose.Note voor Java-bibliotheek.
## Vereisten
Voordat u in de zelfstudie duikt, moet u ervoor zorgen dat aan de volgende vereisten is voldaan:
- Java Development Kit (JDK) op uw computer geïnstalleerd.
-  Aspose.Note voor Java-bibliotheek gedownload van[hier](https://releases.aspose.com/note/java/).
## Pakketten importeren
Laten we eerst de benodigde pakketten in uw Java-project importeren om de functionaliteiten van Aspose.Note optimaal te benutten. Neem de volgende code op in uw project:
```java
import java.awt.Color;
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.NumberFormat;
import com.aspose.note.NumberList;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.ParagraphStyle;
```
## Stap 1: Document-, pagina- en overzichtsobjecten initialiseren
```java
// Uw documentenmap
String dataDir = "Your Document Directory";
// Maak document-, pagina- en overzichtsobjecten
Document doc = new Document();
Page page = new Page();
Outline outline = new Outline();
// Stel de standaardtekststijl in
ParagraphStyle defaultStyle = new ParagraphStyle()
                                        .setFontColor(Color.black)
                                        .setFontName("Arial")
                                        .setFontSize(10);
Document doc = new Document();
Page page = new Page();
Outline outline = new Outline();
```
## Stap 2: Standaard tekststijl instellen
```java
ParagraphStyle defaultStyle = new ParagraphStyle()
                                        .setFontColor(Color.black)
                                        .setFontName("Arial")
                                        .setFontSize(10);
```
## Stap 3: Overzichtselementen maken
Laten we nu de elementen voor uw genummerde lijst maken.
```java
OutlineElement outlineElem1 = new OutlineElement();
outlineElem1.setNumberList(new NumberList("{0})", NumberFormat.DecimalNumbers, "Arial", 10));
RichText text1 = new RichText().append("First");
text1.setParagraphStyle(defaultStyle);
outlineElem1.appendChildLast(text1);
// Herhaal dit voor andere elementen (outlineElem2 en outlineElem3)
```
## Stap 4: Omtrekelementen aan de omtrek toevoegen
```java
outline.appendChildLast(outlineElem1);
outline.appendChildLast(outlineElem2);
outline.appendChildLast(outlineElem3);
```
## Stap 5: Omtrek aan pagina toevoegen
```java
page.appendChildLast(outline);
```
## Stap 6: Het document opslaan
```java
doc.appendChildLast(page);
doc.save(dataDir + "CreateNumberedList_out.pdf");
System.out.printf("File saved: %s\n", dataDir + "CreateNumberedList_out.pdf");
```
Volg deze stappen nauwgezet en u maakt moeiteloos een genummerde lijst in OneNote met behulp van Aspose.Note voor Java.
## Conclusie
In deze zelfstudie hebben we het naadloze proces onderzocht van het maken van een genummerde lijst in OneNote met behulp van Aspose.Note voor Java. De robuuste functies van de bibliotheek maken het tot een hulpmiddel van onschatbare waarde voor Java-ontwikkelaars die met Microsoft OneNote-bestanden werken.
## Veel Gestelde Vragen
### Vraag: Kan ik de nummeringsnotatie in mijn OneNote-lijst aanpassen?
EEN: Absoluut! U kunt het nummeringsformaat aanpassen met behulp van de klasse NumberList die wordt geleverd door Aspose.Note voor Java.
### Vraag: Is er een proefversie beschikbaar voor Aspose.Note voor Java?
 A: Ja, u kunt een gratis proefversie downloaden[hier](https://releases.aspose.com/).
### Vraag: Hoe kan ik ondersteuning krijgen voor Aspose.Note voor Java?
 A: Bezoek de[Aspose.Opmerking voor Java-forum](https://forum.aspose.com/c/note/28) voor gemeenschapssteun.
### Vraag: Waar kan ik gedetailleerde documentatie vinden voor Aspose.Note voor Java?
 A: Raadpleeg de[documentatie](https://reference.aspose.com/note/java/) voor uitgebreide informatie.
### Vraag: Hoe koop ik een licentie voor Aspose.Note voor Java?
 A: U kunt een licentie kopen[hier](https://purchase.aspose.com/buy).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
