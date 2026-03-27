---
date: 2026-01-23
description: Erfahren Sie, wie Sie die Spaltenbreite sperren, wenn Sie einer OneNote-Notiz
  eine Tabelle mit Aspose.Note für Java hinzufügen. Schritt‑für‑Schritt‑Anleitung
  mit Code, Tipps und FAQs.
linktitle: How to Lock Column in OneNote Table – Aspose.Note
second_title: Aspose.Note Java API
title: Wie man eine Spalte in einer OneNote‑Tabelle sperrt – Aspose.Note
url: /de/java/onenote-table-manipulation/create-table-with-locked-columns/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Wie man Spalten in OneNote‑Tabellen sperrt – Aspose.Note

## Introduction
OneNote ist eine vielseitige Notiz‑Plattform, und Aspose.Note für Java erleichtert das **Sperren von Spalten**‑Breiten, wenn Sie einer OneNote‑Tabelle eine Tabelle hinzufügen. In diesem Tutorial sehen Sie ein vollständiges, praxisnahes Beispiel, das zeigt, wie Sie die Tabellen‑Spaltenbreite festlegen, diese Breite sperren und die Rahmen von OneNote‑Tabellen anpassen – alles mit nur wenigen Zeilen Java‑Code.

## Quick Answers
- **Was bedeutet „Spalte sperren“?** Sie fixiert die Spaltenbreite, sodass der Benutzer sie in OneNote nicht mehr ändern kann.  
- **Welche Bibliothek stellt diese Funktion bereit?** Aspose.Note für Java.  
- **Benötige ich eine Lizenz, um das Beispiel auszuführen?** Eine kostenlose Testversion reicht für die Evaluierung; für den Produktionseinsatz ist eine kommerzielle Lizenz erforderlich.  
- **Kann ich nach dem Sperren der Spalte weitere Zeilen hinzufügen?** Ja, Sie können weiterhin Zeilen anhängen; die gesperrte Breite bleibt erhalten.  
- **Welche Java‑Version wird unterstützt?** Java 6 und höher.

## What is “how to lock column” in a OneNote table?
Das Sperren einer Spalte bedeutet, einem `TableColumn`‑Objekt eine feste Breite zuzuweisen und dessen `LockedWidth`‑Eigenschaft auf `true` zu setzen. Dadurch wird ein versehentliches Ändern der Größe durch Endbenutzer verhindert und das Layout bleibt konsistent.

## Why lock column width in OneNote?
- **Konsistentes Layout** – Ihre Notizen sehen auf jedem Gerät gleich aus.  
- **Bessere Lesbarkeit** – Langer Text wird innerhalb einer vorhersehbaren Spaltengröße umgebrochen.  
- **Professionelles Erscheinungsbild** – Gesperrte Spalten verleihen einen gepflegten, berichtähnlichen Eindruck.

## Prerequisites
Bevor Sie beginnen, stellen Sie sicher, dass Folgendes bereitsteht:

- [Java Development Kit (JDK)](https://www.oracle.com/java/technologies/javase-downloads.html) auf Ihrem Rechner installiert.  
- [Aspose.Note for Java](https://downloads.aspose.com/note/java) Bibliothek heruntergeladen und dem Klassenpfad Ihres Projekts hinzugefügt.

## Import Packages
Importieren Sie in Ihrem Java‑Projekt die erforderlichen Pakete für die Arbeit mit Aspose.Note:

```java
import com.aspose.note.*;
import java.io.IOException;
```

## Step 1: Set Up Your Project
Erstellen Sie ein neues Java‑Projekt (oder verwenden Sie ein bestehendes) und fügen Sie die Aspose.Note‑JAR‑Dateien dem Build‑Pfad hinzu. Stellen Sie sicher, dass das Projekt mit dem von Ihnen installierten JDK kompiliert wird.

## Step 2: Initialize Document and Page Objects
Wir beginnen damit, ein neues `Document` und eine `Page` zu erstellen, in der die Tabelle platziert wird.

```java
// The path to the documents directory.
String dataDir = "Your Document Directory";
// Create an object of the Document class
Document doc = new Document();
// Initialize Page class object
Page page = new Page();
```

## Step 3: Create Table Rows and Cells
Hier erstellen wir zwei Zeilen, jeweils mit einer einzelnen Zelle, die Beispieltext enthält. Dies demonstriert, wie sich die gesperrte Spalte bei kurzem und langem Inhalt verhält.

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

## Step 4: Create and Customize the Table
Jetzt erstellen wir die Tabelle, **setzen die Tabellen‑Spaltenbreite**, **sperren die Spalte** und **passen die OneNote‑Tabellenrahmen an**.

```java
// Initialize Table class object
Table table = new Table();
table.setBordersVisible(true);               // customize onenote table borders
TableColumn col = new TableColumn();
col.setWidth(200);                           // set table column width
col.setLockedWidth(true);                    // onenote table locked width
table.getColumns().addItem(col);
// Add rows
table.appendChildLast(row1);
table.appendChildLast(row2);
```

## Step 5: Add Table to Outline and Page
Wir fügen die Tabelle nun einem `OutlineElement` hinzu und schließlich zur Seite – das ist der **add outline element java** Schritt.

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

## Step 6: Save the Document
Speichern Sie die OneNote‑Datei (`.one`) im Verzeichnis, das Sie zuvor angegeben haben.

```java
dataDir = dataDir + "CreateTableWithLockedColumns_out.one";
doc.save(dataDir);
```

Herzlichen Glückwunsch! Sie haben erfolgreich **add table to OneNote** mit einer gesperrten Spalte, fester Breite und angepassten Rahmen mithilfe von Aspose.Note für Java erstellt.

## Common Issues and Solutions
| Problem | Lösung |
|-------|----------|
| Tabelle erscheint ohne Rahmen | Stellen Sie sicher, dass `table.setBordersVisible(true);` aufgerufen wird. |
| Spaltenbreite ändert sich nach dem Hinzufügen von Zeilen | Vergewissern Sie sich, dass `col.setLockedWidth(true);` **vor** dem Anhängen von Zeilen gesetzt ist. |
| Datei wurde nicht gespeichert | Prüfen Sie, dass `dataDir` auf einen beschreibbaren Ordner zeigt und mit einem gültigen Dateinamen endet. |

## Frequently Asked Questions

**F: Fall! Zellabstände, Hintergrundfarben und mehr über die Eigenschaften von Kauf?**  
A: Ja, Sie können [eine kostenlose Testversion herunterladen](https://releases.aspose.com/), um die Funktionen von Aspose.Note für Java zu erkunden.

**F: Wo finde ich zusätzlichen Support oder Community‑Diskussionen?**  
A: Besuchen Sie das [Aspose.Note‑Forum](/c/note/28) für Support und Community‑Diskussionen.

**F: Wie kann ich eine temporäre Lizenz für Aspose.Note für Java erhalten?**  
A: Besuchen Sie [diesen Link](https://purchase.aspose.com/temporary-license/), um eine temporäre Lizenz für Testzwecke zu erhalten.

---

**Zuletzt aktualisiert:** 2026-01-23  
**Getestet mit:** Aspose.Note für Java 24.11  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}