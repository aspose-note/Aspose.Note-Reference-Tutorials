---
date: 2026-01-20
description: Erfahren Sie, wie Sie den Tabellenstil in OneNote mit Aspose.Note für
  Java ändern und die Hintergrundfarben von Tabellenzeilen festlegen. Folgen Sie der
  Schritt‑für‑Schritt‑Anleitung, um Hintergrundfarbe, fett formatierten Text anzuwenden
  und das OneNote‑Dokument zu speichern.
linktitle: Change Table Style in OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: Wie man den Tabellenstil in OneNote mit Aspose.Note ändert
url: /de/java/onenote-table-manipulation/change-table-style/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

#buch. In diesem Tutorial führen wir Sie durch den gesamten Prozess – vom Laden einer OneNote-Datei, dem Festlegen von Hintergrundfarben für Tabellenzeilen, dem Anwenden von fett- und kursivformatierung, bis zum endgültigenfsmethode `setRowStyle`.  
- **Wie mache ich Text in einer OneNote-Tabelle fett?** Setzen Sie das `bold`-Flag in `setRowStyle`.  
- **Was ist erforderlich, um die geänderte Datei zu speichern?** Rufen Sie `document.save(...)` mit einem gültigen Pfad auf.  
- **Benötige ich eine Lizenz für den Produktionseinsatz?** Ja, eine kommerzielle Lizenz ist erforderlich.

## Was bedeutet „Tabellenstil ändern“ in OneNote?
Den Stil einer Tabelle zu ändern bedeutet, Zeilenfarben, Textformatierung und das Gesamterscheinungsbild zu verändern, sodass die Daten leichter zu lesen und optisch ansprechend sind. Aspose.Note bietet eine fluente API, um diese Eigenschaften programmgesteuert zu manipulieren.

## Warum Aspose.Note für Java verwenden?
- **Vollständige Kontrolle** über OneNote-Strukturen ohne manuelle UI-Arbeit.  
- **Plattformübergreifende** Unterstützung; funktioniert auf jedem OS, das Java ausführt.  
- **Umfangreiche Formatierungs**‑Optionen wie Hintergrundfarben, fett und kursiver Text.  

## Voraussetzungen
Stellen Sie vor dem Start sicher, dass Sie Folgendes haben:
- **Java-Entwicklungsumgebung** – JDK 8 oder höher installiert.  
- **Aspose.Note für Java Bibliothek** – Download von der [Download-Seite](https://releases.aspose.com/note/java/).  
- **Dokumentenverzeichnis** – Ein Ordner, in dem Ihre `.one`-Dateien gespeichert werden.  

## Pakete importieren
Importieren Sie in Ihrem Java-Projekt die notwendigen Pakete, um mit Aspose.Note zu arbeiten:
```java
import com.aspose.note.*;
import java.awt.Color;
import java.io.IOException;
import java.nio.file.Paths;
import java.util.List;
```

## Schritt 1: Dokument einrichten
Laden Sie das OneNote-Dokument in Aspose.Note und rufen Sie die Liste der Tabellenknoten ab.
```java
// Set up the document and get the list of table nodes
String dataDir = "Your Document Directory";
Document document = new Document(dataDir + "ChangeTableStyleIn.one");
List<Table> nodes = document.getChildNodes(Table.class);
```

## Schritt 2: Zeilenstile festlegen
Iterieren Sie über jede Tabelle, legen Sie den Stil für jede Zeile fest, einschließlich der Hervorhebung der ersten Zeile nach der Kopfzeile. Dies demonstriert **Tabellenzeilen-Hintergrund festlegen** und **wie man Hintergrundfarbe anwendet**.
```java
// Set row styles for each table in the document
for (Table table : nodes) {
    setRowStyle(table.getFirstChild(), Color.GRAY, true, true);
    // Highlight first row after the head.
    boolean flag = false;
    List<TableRow> rows = table.getChildren();
    for (int i = 1; i < rows.size(); ++i) {
        setRowStyle(rows.get(i), flag ? Color.lightGray : new java.awt.Color(-1, true), false, false);
        flag = !flag;
    }
}
```

## setRowStyle-Methode
Die Hilfsmethode wendet Hintergrundfarbe, fett und kursiv Formatierung auf jede Zelle einer Zeile an. Hier wird **wie man Text in OneNote fett macht** implementiert.
```java
    private static void setRowStyle(TableRow row, Color highlightColor, boolean bold, boolean italic) {
        for (TableCell cell: row)
        {
            cell.setBackgroundColor(highlightColor);
            for (RichText node: cell.getChildNodes(RichText.class))
            {
                node.getParagraphStyle().setBold(bold);
                node.getParagraphStyle().setItalic(italic);
                for (TextRun run: node.getTextRuns())
                {
                    run.getStyle().setBold(bold);
                    run.getStyle().setItalic(italic);
                }
            }
        }
    }
```

## Schritt 3: Dokument speichern
Nachdem die Tabellen formatiert wurden, speichern Sie das geänderte Dokument. Dies zeigt **wie man ein OneNote-Dokument speichert** mit der neuen Formatierung.
```java
// Save the modified document
document.save(Paths.get(dataDir, "ChangeTableStyleOut.one").toString());
```

## Fazit
Aspose.Note für Java vereinfacht den Prozess der Manipulation von OneNote-Dateien. Durch die Nutzung der Fähigkeiten der Bibliothek können Sie problemlos Tabellenstile ändern, Hintergrundfarben für Tabellenzeilen festlegen, Text fett formatieren und das OneNote-Dokument speichern – alles mit wenigen Codezeilen.

## Häufig gestellte Fragen
### Wo finde ich die Dokumentation für Aspose.Note für Java?
Besuchen Sie die [Dokumentation](https://reference.aspose.com/note/java/) für umfassende Anleitungen.

### Wie kann ich eine temporäre Lizenz für Aspose.Note für Java erhalten?
Folgen Sie diesem [Link](https://purchase.aspose.com/temporary-license/), um eine temporäre Lizenz zu erhalten.

### Gibt es eine kostenlose Testversion für Aspose.Note für Java?
Ja, Sie können eine kostenlose Testversion von [hier](https://releases.aspose.com/) herunterladen.

### Wo kann ich Unterstützung für Aspose.Note für Java erhalten?
Treten Sie dem [Aspose.Note-Forum](https://forum.aspose.com/c/note/28) bei, um Unterstützung von der Community zu erhalten.

### Wie kaufe ich Aspose.Note für Java?
Sie können die Bibliothek [hier](https://purchase.aspose.com/buy) erwerben.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Last Updated:** 2026-01-20  
**Tested With:** Aspose.Note for Java 24.11  
**Author:** Aspose  

---