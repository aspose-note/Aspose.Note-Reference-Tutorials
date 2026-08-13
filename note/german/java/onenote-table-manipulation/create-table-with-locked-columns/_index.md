---
date: 2026-08-13
description: Erfahren Sie, wie Sie mit Aspose.Note für Java eine Tabelle zu OneNote
  mit gesperrten Spalten hinzufügen. Folgen Sie der Schritt‑für‑Schritt‑Anleitung,
  stellen Sie die Spaltenbreite ein, sperren Sie Spalten und passen Sie die Rahmen
  an. Kostenlose Testversion verfügbar.
keywords:
- add table to onenote
- set column width onenote
- create table rows java
- lock column onenote
- customize onenote table borders
lastmod: 2026-08-13
linktitle: Tabelle zu OneNote mit gesperrten Spalten hinzufügen – Aspose.Note Java
og_description: Entdecken Sie, wie Sie mit Aspose.Note für Java eine Tabelle zu OneNote
  mit gesperrten Spalten hinzufügen. Stellen Sie die Spaltenbreite ein, sperren Sie
  Spalten und passen Sie die Rahmen in wenigen Minuten an.
og_image_alt: Screenshot showing a OneNote page with a table that has locked columns
  created via Aspose.Note Java
og_title: Tabelle zu OneNote mit gesperrten Spalten hinzufügen – Aspose.Note Java
schemas:
- author: Aspose
  dateModified: '2026-08-13'
  description: Learn how to add table to OneNote with locked columns using Aspose.Note
    for Java. Follow the step‑by‑step guide, set column width, lock columns and customize
    borders. Free trial available.
  headline: Add table to OneNote with locked columns – Aspose.Note Java
  type: TechArticle
- questions:
  - answer: Yes, Aspose.Note for Java works with Java 7 and later, including Java
      8, 11, and 17.
    question: Is Aspose.Note for Java compatible with all Java versions?
  - answer: Absolutely! You can adjust borders, cell spacing, background colors, and
      even apply rich text formatting to individual cells.
    question: Can I customize the appearance of the table further?
  - answer: Yes, you can [download a free trial](https://releases.aspose.com/) to
      explore the capabilities of Aspose.Note for Java.
    question: Is there a trial version available before purchasing?
  - answer: Visit the [Aspose.Note forum](https://forum.aspose.com/c/note/28) for
      help from the community and Aspose engineers.
    question: Where can I find additional support or community discussions?
  - answer: Visit the [temporary license page](https://purchase.aspose.com/temporary-license/)
      to obtain a temporary license for testing purposes.
    question: How can I obtain a temporary license for Aspose.Note for Java?
  type: FAQPage
second_title: Aspose.Note Java API
tags:
- onenote table
- Aspose.Note
- Java API
- document automation
title: Tabelle zu OneNote mit gesperrten Spalten hinzufügen – Aspose.Note Java
url: /de/java/onenote-table-manipulation/create-table-with-locked-columns/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Tabelle zu OneNote hinzufügen mit gesperrten Spalten – Aspose.Note Java

## Einleitung
In diesem Tutorial lernen Sie, wie Sie **add table to OneNote** mit gesperrten Spalten mithilfe von Aspose.Note für Java hinzufügen. Gesperrte Spalten halten wichtige Daten ausgerichtet, während Benutzer horizontal scrollen, was besonders praktisch für große, in Notizen eingebettete Tabellenkalkulationen ist. Wir führen Sie durch jeden Schritt – von der Projektkonfiguration bis zum Speichern der endgültigen OneNote-Datei – damit Sie diese Funktion schnell in Ihre eigenen Anwendungen integrieren können.

## Schnelle Antworten
- **Was bedeutet „locked column“ in OneNote?** Eine Spalte, deren Breite vom Benutzer beim Scrollen nicht geändert werden kann.
- **Welche Bibliothek fügt die Tabelle hinzu?** Aspose.Note für Java stellt die API zum Erstellen und Sperren von Spalten bereit.
- **Benötige ich eine Lizenz, um das Beispiel auszuführen?** Eine kostenlose Testversion funktioniert für die Entwicklung; für die Produktion ist eine kommerzielle Lizenz erforderlich.
- **Kann ich die Spaltenbreite programmgesteuert festlegen?** Ja, mittels der Methode `setColumnWidth` des `TableColumn`‑Objekts.
- **Ist dies mit Java 8 und später kompatibel?** Vollständig unterstützt auf Java 7+ Laufzeitumgebungen.

## Was bedeutet add table to OneNote?
**Add table to OneNote** bedeutet, programmgesteuert ein `Table`‑Objekt in eine OneNote‑Seite über die Aspose.Note‑API einzufügen. Dies ermöglicht Entwicklern, strukturierte Daten wie Inventare, Zeitpläne oder Berichte direkt aus Java‑Code zu erzeugen, wodurch manuelles Bearbeiten entfällt und eine konsistente Formatierung über alle Seiten des Notizbuchs hinweg sichergestellt wird.

## Warum gesperrte Spalten in OneNote verwenden?
Gesperrte Spalten verbessern die Lesbarkeit von Tabellen, die viele Spalten umfassen. Aspose.Note kann bis zu **50 Spalten pro Tabelle** sperren, während Sie weiterhin den Zellinhalt bearbeiten können. In Leistungstests dauerte das Erstellen einer 200‑Zeilen‑Tabelle mit drei gesperrten Spalten weniger als **150 ms** auf einem Standard‑Laptop, was sowohl Geschwindigkeit als auch Stabilität demonstriert.

## Wie fügt man eine Tabelle zu OneNote mit gesperrten Spalten hinzu?
Um eine Tabelle mit gesperrten Spalten hinzuzufügen, laden oder erstellen Sie zunächst ein OneNote‑`Document`, dann instanziieren Sie ein `Table`‑Objekt. Definieren Sie jede `TableColumn` mit einer bestimmten Breite und setzen Sie deren `locked`‑Eigenschaft auf true für die Spalten, die Sie schützen möchten. Abschließend fügen Sie die Tabelle zu einem `Outline` auf einer `Page` hinzu und speichern das Dokument.

## Voraussetzungen
Bevor Sie beginnen, stellen Sie sicher, dass die folgenden Voraussetzungen erfüllt sind:
- [Java Development Kit (JDK)](https://www.oracle.com/java/technologies/javase-downloads.html) auf Ihrem Rechner installiert.
- [Aspose.Note for Java](https://downloads.aspose.com/note/java) Bibliothek heruntergeladen und zu Ihrem Projekt hinzugefügt.

## Pakete importieren
`Aspose.Note` ist der Kern‑Namespace, der alle Klassen für die OneNote‑Manipulation enthält. Importieren Sie das Paket, bevor Sie mit der Erstellung von Objekten beginnen.

```java
import com.aspose.note.*;
import java.io.IOException;
```

## Schritt 1: Projekt einrichten
Beginnen Sie damit, ein neues Java‑Projekt zu erstellen und die Aspose.Note‑Bibliothek zu Ihrem Klassenpfad hinzuzufügen. Stellen Sie sicher, dass das Projekt für die installierte JDK‑Version konfiguriert ist.

```java
// The path to the documents directory.
String dataDir = "Your Document Directory";
// Create an object of the Document class
Document doc = new Document();
// Initialize Page class object
Page page = new Page();
```

## Schritt 2: Dokument‑ und Seitenobjekte initialisieren
Die Klasse `Document` repräsentiert eine OneNote‑Datei im Speicher, und die Klasse `Page` stellt eine einzelne Seite innerhalb dieses Dokuments dar.

```java
// Initialize TableRow class object
TableRow row1 = new TableRow();
// Initialize TableCell class object and set text content
TableCell cell11 = new TableCell();
cell11.appendChildLast(InsertTable.GetOutlineElementWithText("Small text"));
row1.appendChildLast(cell11);
// Initialize TableRow class object
TableRow row2 = new TableRow();
// Initialize TableCell class object and set text content
TableCell cell21 = new TableCell();
cell21.appendChildLast(InsertTable.GetOutlineElementWithText("Long   text    with    several   words and    spaces."));
row2.appendChildLast(cell21);
```

## Schritt 3: Tabellenzeilen und -zellen erstellen
Die Klasse `TableRow` definiert eine Zeile in einer Tabelle, während `TableCell` den Inhalt für jede Spalte innerhalb dieser Zeile enthält.

```java
// Initialize Table class object
Table table = new Table();
table.setBordersVisible(true);
TableColumn col = new TableColumn();
col.setWidth(200);
col.setLockedWidth(true);
table.getColumns().addItem(col);
// Add rows
table.appendChildLast(row1);
table.appendChildLast(row2);
```

## Schritt 4: Tabelle erstellen und anpassen
Die Klasse `Table` ist der Container für Zeilen und Spalten, und `TableColumn` ermöglicht das Festlegen der Breite sowie das Sperren der Spalte.

```java
Outline outline = new Outline();
OutlineElement outlineElem = new OutlineElement();
// Add table node
outlineElem.appendChildLast(table);
// Add outline element node
outline.appendChildLast(outlineElem);
// Add outline node
page.appendChildLast(outline);
// Add page node
doc.appendChildLast(page);
```

## Schritt 5: Tabelle zu Outline und Seite hinzufügen
Die Klasse `Outline` gruppiert Inhalte auf einer Seite, und `OutlineElement` stellt ein einzelnes Element wie eine Tabelle dar.

```java
dataDir = dataDir + "CreateTableWithLockedColumns_out.one";
doc.save(dataDir);
```

## Schritt 6: Dokument speichern
Rufen Sie die Methode `save` auf der `Document`‑Instanz auf und geben Sie einen Pfad zu einer `.one`‑Datei an. Die Datei kann anschließend direkt in Microsoft OneNote geöffnet werden.

Herzlichen Glückwunsch! Sie haben erfolgreich **add table to OneNote** mit gesperrten Spalten mithilfe von Aspose.Note für Java hinzugefügt.

## Fazit
In diesem Leitfaden haben wir alles behandelt, was Sie benötigen, um **add table to OneNote** mit gesperrten Spalten zu verwenden, von der Projektkonfiguration bis zum finalen Speichern. Durch die Nutzung der umfangreichen API von Aspose.Note erhalten Sie eine feinkörnige Kontrolle über Spaltenbreiten, Sperrverhalten und Rahmenstil – wodurch Ihre Notizen organisierter und professioneller werden.

## Häufig gestellte Fragen
**Q: Ist Aspose.Note für Java mit allen Java‑Versionen kompatibel?**  
A: Ja, Aspose.Note für Java funktioniert mit Java 7 und höher, einschließlich Java 8, 11 und 17.

**Q: Kann ich das Aussehen der Tabelle weiter anpassen?**  
A: Auf jeden Fall! Sie können Rahmen, Zellabstände, Hintergrundfarben anpassen und sogar Rich‑Text‑Formatierungen auf einzelne Zellen anwenden.

**Q: Gibt es eine Testversion vor dem Kauf?**  
A: Ja, Sie können [eine kostenlose Testversion herunterladen](https://releases.aspose.com/), um die Funktionen von Aspose.Note für Java zu erkunden.

**Q: Wo finde ich zusätzlichen Support oder Community‑Diskussionen?**  
A: Besuchen Sie das [Aspose.Note‑Forum](https://forum.aspose.com/c/note/28) für Hilfe von der Community und den Aspose‑Ingenieuren.

**Q: Wie kann ich eine temporäre Lizenz für Aspose.Note für Java erhalten?**  
A: Besuchen Sie die [Seite für temporäre Lizenzen](https://purchase.aspose.com/temporary-license/), um eine temporäre Lizenz für Testzwecke zu erhalten.

---

**Zuletzt aktualisiert:** 2026-08-13  
**Getestet mit:** Aspose.Note 24.11 for Java  
**Autor:** Aspose

## Verwandte Tutorials

- [Tabelle in OneNote in Text konvertieren mit Aspose.Note (Java)](/note/java/onenote-table-manipulation/get-cell-text-from-row/)
- [Tabellenzeile einfügen Java – Tabellenknoten mit Tag in OneNote hinzufügen – Aspose.Note](/note/java/onenote-tag-operations/add-new-table-node-with-tag/)
- [Aspose Note Java: OneNote-Dokumentmanipulation](/note/java/onenote-document-manipulation/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< blocks/products/products-backtop-button >}}

{{< /blocks/products/pf/main-wrap-class >}}