---
title: Neuen Bildknoten mit Tag in OneNote hinzufügen – Aspose.Note
linktitle: Neuen Bildknoten mit Tag in OneNote hinzufügen – Aspose.Note
second_title: Aspose.Note Java API
description: Erfahren Sie, wie Sie mit Aspose.Note für Java einen neuen Bildknoten mit einem Tag in OneNote hinzufügen. Verbessern Sie mühelos Ihre Java-Programmierkenntnisse.
type: docs
weight: 10
url: /de/java/onenote-tag-operations/add-new-image-node-with-tag/
---
## Einführung
Im Bereich der Java-Programmierung sticht Aspose.Note als leistungsstarkes Tool für die einfache Handhabung von OneNote-Dokumenten hervor. Wenn Sie Ihre Fähigkeiten verbessern und lernen möchten, wie Sie mit Aspose.Note einen neuen Bildknoten mit einem Tag in OneNote hinzufügen, sind Sie hier genau richtig. Diese Schritt-für-Schritt-Anleitung führt Sie durch den Prozess und stellt sicher, dass Sie jedes Konzept gründlich verstehen.
## Voraussetzungen
Bevor wir uns mit dem Tutorial befassen, stellen wir sicher, dass Sie alles haben, was Sie brauchen:
1.  Aspose.Note für Java: Stellen Sie sicher, dass die Aspose.Note-Bibliothek installiert ist. Wenn nicht, können Sie es herunterladen[Hier](https://releases.aspose.com/note/java/).
2. Java-Entwicklungsumgebung: Stellen Sie sicher, dass auf Ihrem Computer eine funktionierende Java-Entwicklungsumgebung eingerichtet ist.
Nachdem wir nun die Voraussetzungen geschaffen haben, fahren wir mit den nächsten Schritten fort.
## Pakete importieren
Beginnen Sie in Ihrem Java-Projekt mit dem Importieren der erforderlichen Pakete:
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
## Schritt 1: Dokumentobjekt erstellen
```java
// Der Pfad zum Dokumentenverzeichnis.
String dataDir = "Your Document Directory";
// Erstellen Sie ein Objekt der Document-Klasse
Document doc = new Document();
```
## Schritt 2: Seitenklassenobjekt initialisieren
```java
// Initialisieren Sie das Page-Klassenobjekt
Page page = new Page();
```
## Schritt 3: Outline-Klassenobjekt initialisieren
```java
// Initialisieren Sie das Outline-Klassenobjekt
Outline outline = new Outline();
```
## Schritt 4: Initialisieren Sie das OutlineElement-Klassenobjekt
```java
// Initialisieren Sie das OutlineElement-Klassenobjekt
OutlineElement outlineElem = new OutlineElement();
```
## Schritt 5: Bild laden und einfügen
```java
// ein Bild laden
Image image = new Image(null, dataDir + "Input.jpg");
// Bild in den Dokumentknoten einfügen
outlineElem.appendChildLast(image);
```
## Schritt 6: Notiz-Tag zum Bild hinzufügen
```java
// Fügen Sie dem Bild ein gelbes Sternnotiz-Tag hinzu
NoteTag noteTag = NoteTag.createYellowStar();
image.getTags().add(noteTag);
```
## Schritt 7: Gliederungselementknoten hinzufügen
```java
// Gliederungselementknoten hinzufügen
outline.appendChildLast(outlineElem);
```
## Schritt 8: Gliederungsknoten hinzufügen
```java
// Gliederungsknoten hinzufügen
page.appendChildLast(outline);
```
## Schritt 9: Seitenknoten hinzufügen
```java
// Seitenknoten hinzufügen
doc.appendChildLast(page);
```
## Schritt 10: OneNote-Dokument speichern
```java
// OneNote-Dokument als PDF speichern
doc.save(dataDir + "AddNewImageNodeWithTag_out.pdf", SaveFormat.Pdf);
```
Glückwunsch! Sie haben mit Aspose.Note für Java erfolgreich einen neuen Bildknoten mit einem Tag in OneNote hinzugefügt.
## Abschluss
 Die Beherrschung von Aspose.Note für Java eröffnet spannende Möglichkeiten bei der Manipulation von OneNote-Dokumenten. Durch das Befolgen dieses Tutorials haben Sie eine praktische Fähigkeit erworben, die auf verschiedene Projekte angewendet werden kann. Erkunden Sie weiterhin die Aspose.Note-Dokumentation[Hier](https://reference.aspose.com/note/java/)für erweiterte Funktionen und Möglichkeiten.
## FAQs
### Wo finde ich die Aspose.Note-Dokumentation?
 Die Dokumentation finden Sie hier[Hier](https://reference.aspose.com/note/java/).
### Wie lade ich Aspose.Note für Java herunter?
 Sie können es von der Veröffentlichungsseite herunterladen[Hier](https://releases.aspose.com/note/java/).
### Gibt es eine kostenlose Testversion?
 Ja, Sie können auf die kostenlose Testversion zugreifen[Hier](https://releases.aspose.com/).
### Wo erhalte ich Support für Aspose.Note?
 Besuchen Sie das Community-Forum[Hier](https://forum.aspose.com/c/note/28) zur Unterstützung.
### Benötige ich eine temporäre Lizenz?
 Bei Bedarf können Sie eine temporäre Lizenz erwerben[Hier](https://purchase.aspose.com/temporary-license/).