---
title: Textknoten mit Tag in OneNote hinzufügen – Aspose.Note
linktitle: Textknoten mit Tag in OneNote hinzufügen – Aspose.Note
second_title: Aspose.Note Java API
description: Erfahren Sie, wie Sie mit Aspose.Note für Java Textknoten mit Tags in OneNote hinzufügen. Einfach, effizient und entwicklerfreundlich. Laden Sie die Bibliothek jetzt herunter!
type: docs
weight: 13
url: /de/java/onenote-tag-operations/add-text-node-with-tag/
---
## Einführung
In diesem Tutorial erfahren Sie, wie Sie mit Aspose.Note für Java einen Textknoten mit einem Tag in OneNote hinzufügen. Aspose.Note ist eine leistungsstarke Java-Bibliothek, die es Entwicklern ermöglicht, programmgesteuert mit Microsoft OneNote-Dateien zu arbeiten. Das Hinzufügen von Textknoten mit Tags ist eine häufige Anforderung bei der Dokumentverarbeitung und Aspose.Note vereinfacht diese Aufgabe.
## Voraussetzungen
Bevor wir uns mit dem Tutorial befassen, stellen Sie sicher, dass Sie die folgenden Voraussetzungen erfüllen:
- Grundkenntnisse der Java-Programmierung.
-  Aspose.Note für Java-Bibliothek installiert. Sie können es herunterladen[Hier](https://releases.aspose.com/note/java/).
- Eine integrierte Entwicklungsumgebung (IDE), die für die Java-Entwicklung eingerichtet wurde.
## Pakete importieren
Beginnen Sie mit dem Importieren der erforderlichen Pakete für Ihr Java-Projekt. Fügen Sie in Ihren Code die folgenden Importe ein:
```java
import java.awt.Color;
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.NoteTag;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.TagIcon;
import com.aspose.note.ParagraphStyle;
```
## Schritt 1: Dokumentobjekt erstellen
Initialisieren Sie ein Document-Klassenobjekt, um das OneNote-Dokument darzustellen:
```java
// Der Pfad zum Dokumentenverzeichnis.
String dataDir = "Your Document Directory";
//Erstellen Sie ein Objekt der Document-Klasse
Document doc = new Document();
```
## Schritt 2: Seitenklassenobjekt initialisieren
Initialisieren Sie ein Page-Klassenobjekt, um die Seite im Dokument darzustellen:
```java
// Initialisieren Sie das Page-Klassenobjekt
Page page = new Page();
```
## Schritt 3: Outline-Klassenobjekt initialisieren
Initialisieren Sie ein Outline-Klassenobjekt, um den Inhalt innerhalb der Seite zu strukturieren:
```java
// Initialisieren Sie das Outline-Klassenobjekt
Outline outline = new Outline();
```
## Schritt 4: Initialisieren Sie das OutlineElement-Klassenobjekt
Initialisieren Sie ein OutlineElement-Klassenobjekt, um ein Element innerhalb der Gliederung darzustellen:
```java
// Initialisieren Sie das OutlineElement-Klassenobjekt
OutlineElement outlineElem = new OutlineElement();
```
## Schritt 5: Textstil anpassen
Richten Sie den Stil für den Textknoten ein, z. B. Schriftfarbe, Name und Größe:
```java
// Passen Sie den Textstil an
ParagraphStyle textStyle = new ParagraphStyle()
                                .setFontColor(Color.BLACK)
                                .setFontName("Arial")
                                .setFontSize(10);
```
## Schritt 6: RichText-Objekt erstellen
Erstellen Sie ein RichText-Objekt und hängen Sie den gewünschten Text daran an:
```java
// Erstellen Sie ein RichText-Objekt
RichText text = new RichText().append("OneNote text.");
text.setParagraphStyle(textStyle);
```
## Schritt 7: Notiz-Tag hinzufügen
Fügen Sie dem Text ein Notiz-Tag, beispielsweise einen gelben Stern, hinzu:
```java
// Notiz-Tag hinzufügen
NoteTag noteTag = NoteTag.createYellowStar();
text.getTags().add(noteTag);
```
## Schritt 8: Textknoten hinzufügen
Fügen Sie den Textknoten zum Gliederungselement hinzu:
```java
// Textknoten hinzufügen
outlineElem.appendChildLast(text);
```
## Schritt 9: Gliederungselement zur Gliederung hinzufügen
Fügen Sie das Gliederungselement zur Gliederung hinzu:
```java
// Gliederungselementknoten hinzufügen
outline.appendChildLast(outlineElem);
```
## Schritt 10: Gliederung zur Seite hinzufügen
Fügen Sie die Gliederung zur Seite hinzu:
```java
// Gliederungsknoten hinzufügen
page.appendChildLast(outline);
```
## Schritt 11: Seite zum Dokument hinzufügen
Fügen Sie die Seite zum Dokument hinzu:
```java
// Seitenknoten hinzufügen
doc.appendChildLast(page);
```
## Schritt 12: OneNote-Dokument speichern
Speichern Sie das OneNote-Dokument im angegebenen Verzeichnis:
```java
// OneNote-Dokument speichern
doc.save(dataDir + "AddTextNodeWithTag_out.one");
```
Glückwunsch! Sie haben mit Aspose.Note für Java erfolgreich einen Textknoten mit einem Tag in OneNote hinzugefügt.
## Abschluss
In diesem Tutorial haben wir den schrittweisen Prozess des Hinzufügens eines Textknotens mit einem Tag in OneNote mithilfe der Aspose.Note für Java-Bibliothek behandelt. Diese leistungsstarke Bibliothek vereinfacht die Dokumentenverarbeitung und erleichtert Entwicklern die programmgesteuerte Bearbeitung von OneNote-Dateien.
## Häufig gestellte Fragen
### F: Kann ich Aspose.Note für Java mit anderen Java-Bibliotheken verwenden?
A: Ja, Aspose.Note für Java kann nahtlos in andere Java-Bibliotheken integriert werden, um die Dokumentverarbeitungsmöglichkeiten zu verbessern.
### F: Gibt es eine kostenlose Testversion für Aspose.Note für Java?
 A: Ja, Sie können auf die kostenlose Testversion zugreifen[Hier](https://releases.aspose.com/).
### F: Wie erhalte ich Unterstützung für Aspose.Note für Java?
A: Sie können Unterstützung von der Aspose.Note-Community erhalten[Forum](https://forum.aspose.com/c/note/28).
### F: Sind temporäre Lizenzen für Aspose.Note für Java verfügbar?
 A: Ja, Sie können temporäre Lizenzen erhalten[Hier](https://purchase.aspose.com/temporary-license/).
### F: Wo finde ich die Dokumentation für Aspose.Note für Java?
 A: Die Dokumentation ist verfügbar[Hier](https://reference.aspose.com/note/java/).