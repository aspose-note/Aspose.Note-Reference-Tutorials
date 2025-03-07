---
title: Nummerierte Liste in OneNote erstellen – Aspose.Note
linktitle: Nummerierte Liste in OneNote erstellen – Aspose.Note
second_title: Aspose.Note Java API
description: Erfahren Sie, wie Sie mit Aspose.Note für Java mühelos eine nummerierte Liste in OneNote erstellen. Laden Sie eine kostenlose Testversion herunter und tauchen Sie ein in die Welt der Java-Entwicklung!
weight: 14
url: /de/java/onenote-text-manipulation/create-numbered-list/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Nummerierte Liste in OneNote erstellen – Aspose.Note

## Einführung
Aspose.Note für Java ermöglicht Java-Entwicklern die nahtlose Arbeit mit Microsoft OneNote-Dateien. In diesem Tutorial führen wir Sie durch den Prozess der Erstellung einer nummerierten Liste in OneNote mit der leistungsstarken Aspose.Note für Java-Bibliothek.
## Voraussetzungen
Bevor Sie mit dem Tutorial beginnen, stellen Sie sicher, dass die folgenden Voraussetzungen erfüllt sind:
- Installiertes Java Development Kit (JDK) auf Ihrem Computer.
-  Aspose.Note für Java-Bibliothek heruntergeladen von[Hier](https://releases.aspose.com/note/java/).
## Pakete importieren
Importieren wir zunächst die notwendigen Pakete in Ihr Java-Projekt, um die Funktionalitäten von Aspose.Note optimal zu nutzen. Fügen Sie den folgenden Code in Ihr Projekt ein:
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
## Schritt 1: Dokument-, Seiten- und Gliederungsobjekte initialisieren
```java
// Ihr Dokumentenverzeichnis
String dataDir = "Your Document Directory";
// Erstellen Sie Dokument-, Seiten- und Gliederungsobjekte
Document doc = new Document();
Page page = new Page();
Outline outline = new Outline();
// Legen Sie den Standardtextstil fest
ParagraphStyle defaultStyle = new ParagraphStyle()
                                        .setFontColor(Color.black)
                                        .setFontName("Arial")
                                        .setFontSize(10);
Document doc = new Document();
Page page = new Page();
Outline outline = new Outline();
```
## Schritt 2: Standardtextstil festlegen
```java
ParagraphStyle defaultStyle = new ParagraphStyle()
                                        .setFontColor(Color.black)
                                        .setFontName("Arial")
                                        .setFontSize(10);
```
## Schritt 3: Gliederungselemente erstellen
Lassen Sie uns nun die Elemente für Ihre nummerierte Liste erstellen.
```java
OutlineElement outlineElem1 = new OutlineElement();
outlineElem1.setNumberList(new NumberList("{0})", NumberFormat.DecimalNumbers, "Arial", 10));
RichText text1 = new RichText().append("First");
text1.setParagraphStyle(defaultStyle);
outlineElem1.appendChildLast(text1);
// Wiederholen Sie den Vorgang für andere Elemente (outlineElem2 und outlineElem3).
```
## Schritt 4: Gliederungselemente zur Gliederung hinzufügen
```java
outline.appendChildLast(outlineElem1);
outline.appendChildLast(outlineElem2);
outline.appendChildLast(outlineElem3);
```
## Schritt 5: Gliederung zur Seite hinzufügen
```java
page.appendChildLast(outline);
```
## Schritt 6: Speichern des Dokuments
```java
doc.appendChildLast(page);
doc.save(dataDir + "CreateNumberedList_out.pdf");
System.out.printf("File saved: %s\n", dataDir + "CreateNumberedList_out.pdf");
```
Befolgen Sie diese Schritte sorgfältig, und Sie werden mit Aspose.Note für Java mühelos eine nummerierte Liste in OneNote erstellen.
## Abschluss
In diesem Tutorial haben wir den nahtlosen Prozess der Erstellung einer nummerierten Liste in OneNote mit Aspose.Note für Java untersucht. Die robusten Funktionen der Bibliothek machen sie zu einem unschätzbar wertvollen Werkzeug für Java-Entwickler, die mit Microsoft OneNote-Dateien arbeiten.
## Häufig gestellte Fragen
### F: Kann ich das Nummerierungsformat in meiner OneNote-Liste anpassen?
A: Auf jeden Fall! Sie können das Nummerierungsformat mithilfe der von Aspose.Note für Java bereitgestellten NumberList-Klasse anpassen.
### F: Gibt es eine Testversion für Aspose.Note für Java?
 A: Ja, Sie können eine kostenlose Testversion herunterladen[Hier](https://releases.aspose.com/).
### F: Wie erhalte ich Unterstützung für Aspose.Note für Java?
 A: Besuchen Sie die[Aspose.Note für Java-Forum](https://forum.aspose.com/c/note/28) für die Unterstützung der Gemeinschaft.
### F: Wo finde ich eine ausführliche Dokumentation für Aspose.Note für Java?
 A: Siehe[Dokumentation](https://reference.aspose.com/note/java/) für umfassende Informationen.
### F: Wie kaufe ich eine Lizenz für Aspose.Note für Java?
 A: Sie können eine Lizenz kaufen[Hier](https://purchase.aspose.com/buy).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
