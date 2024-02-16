---
title: Erstellen Sie eine Tabelle mit gesperrten Spalten in OneNote – Aspose.Note
linktitle: Erstellen Sie eine Tabelle mit gesperrten Spalten in OneNote – Aspose.Note
second_title: Aspose.Note Java API
description: Verbessern Sie Ihr OneNote-Erlebnis mit Aspose.Note für Java. Erfahren Sie anhand einer Schritt-für-Schritt-Anleitung, wie Sie Tabellen mit gesperrten Spalten erstellen. Laden Sie jetzt Ihre kostenlose Testversion herunter!
type: docs
weight: 12
url: /de/java/onenote-table-manipulation/create-table-with-locked-columns/
---
## Einführung
OneNote ist ein leistungsstarkes Tool zum Organisieren von Informationen, und Aspose.Note für Java erweitert seine Funktionen, indem es eine nahtlose Möglichkeit zum Erstellen von Tabellen mit gesperrten Spalten bietet. In diesem Tutorial führen wir Sie durch den Prozess der Verwendung von Aspose.Note für Java zum Erstellen einer Tabelle mit gesperrten Spalten in OneNote.
## Voraussetzungen
Bevor Sie beginnen, stellen Sie sicher, dass die folgenden Voraussetzungen erfüllt sind:
- [Java Development Kit (JDK)](https://www.oracle.com/java/technologies/javase-downloads.html)auf Ihrem Computer installiert.
- [Aspose.Note für Java](https://downloads.aspose.com/note/java) Bibliothek heruntergeladen und Ihrem Projekt hinzugefügt.
## Pakete importieren
Importieren Sie in Ihrem Java-Projekt die notwendigen Pakete für die Arbeit mit Aspose.Hinweis:
```java
import com.aspose.note.*;
import java.io.IOException;
```
## Schritt 1: Richten Sie Ihr Projekt ein
Erstellen Sie zunächst ein neues Java-Projekt und fügen Sie die Aspose.Note-Bibliothek Ihrem Klassenpfad hinzu. Stellen Sie sicher, dass Ihr Projekt für die Verwendung des JDK konfiguriert ist.
## Schritt 2: Dokument- und Seitenobjekte initialisieren
```java
// Der Pfad zum Dokumentenverzeichnis.
String dataDir = "Your Document Directory";
//Erstellen Sie ein Objekt der Document-Klasse
Document doc = new Document();
// Initialisieren Sie das Page-Klassenobjekt
Page page = new Page();
```
## Schritt 3: Tabellenzeilen und Zellen erstellen
```java
// Initialisieren Sie das TableRow-Klassenobjekt
TableRow row1 = new TableRow();
// Initialisieren Sie das TableCell-Klassenobjekt und legen Sie den Textinhalt fest
TableCell cell11 = new TableCell();
cell11.appendChildLast(InsertTable.GetOutlineElementWithText("Small text"));
row1.appendChildLast(cell11);
// Initialisieren Sie das TableRow-Klassenobjekt
TableRow row2 = new TableRow();
// Initialisieren Sie das TableCell-Klassenobjekt und legen Sie den Textinhalt fest
TableCell cell21 = new TableCell();
cell21.appendChildLast(InsertTable.GetOutlineElementWithText("Long   text    with    several   words and    spaces."));
row2.appendChildLast(cell21);
```
## Schritt 4: Erstellen und anpassen Sie die Tabelle
```java
// Initialisieren Sie das Tabellenklassenobjekt
Table table = new Table();
table.setBordersVisible(true);
TableColumn col = new TableColumn();
col.setWidth(200);
col.setLockedWidth(true);
table.getColumns().addItem(col);
// Zeilen hinzufügen
table.appendChildLast(row1);
table.appendChildLast(row2);
```
## Schritt 5: Tabelle zur Gliederung und Seite hinzufügen
```java
Outline outline = new Outline();
OutlineElement outlineElem = new OutlineElement();
// Tabellenknoten hinzufügen
outlineElem.appendChildLast(table);
// Gliederungselementknoten hinzufügen
outline.appendChildLast(outlineElem);
// Gliederungsknoten hinzufügen
page.appendChildLast(outline);
// Seitenknoten hinzufügen
doc.appendChildLast(page);
```
## Schritt 6: Speichern Sie das Dokument
```java
dataDir = dataDir + "CreateTableWithLockedColumns_out.one";
doc.save(dataDir);
```
Glückwunsch! Sie haben mit Aspose.Note für Java erfolgreich eine Tabelle mit gesperrten Spalten in OneNote erstellt.
## Abschluss
In diesem Tutorial haben wir den Prozess der Verwendung von Aspose.Note für Java untersucht, um Ihr OneNote-Erlebnis durch die Erstellung von Tabellen mit gesperrten Spalten zu verbessern. Diese Funktionalität fügt Ihren Notizen eine neue Ebene der Organisation und Struktur hinzu.
## FAQs
### Ist Aspose.Note für Java mit allen Java-Versionen kompatibel?
Ja, Aspose.Note für Java ist mit Java 6 und späteren Versionen kompatibel.
### Kann ich das Erscheinungsbild der Tabelle weiter anpassen?
Absolut! Aspose.Note für Java bietet umfangreiche Optionen zum Anpassen von Tabellen, wie zum Beispiel das Anpassen von Rändern, Zellenabständen und mehr.
### Gibt es vor dem Kauf eine Testversion?
 Ja, du kannst[Laden Sie eine kostenlose Testversion herunter](https://releases.aspose.com/) um die Funktionen von Aspose.Note für Java zu erkunden.
### Wo finde ich zusätzliche Unterstützung oder Community-Diskussionen?
 Besuche den[Aspose.Note-Forum](https://forum.aspose.com/c/note/28) für Unterstützung und Community-Diskussionen.
### Wie kann ich eine temporäre Lizenz für Aspose.Note für Java erhalten?
 Besuchen[dieser Link](https://purchase.aspose.com/temporary-license/) um eine temporäre Lizenz zu Testzwecken zu erhalten.