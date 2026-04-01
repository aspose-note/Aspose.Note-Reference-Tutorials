---
date: 2026-04-01
description: Erfahren Sie, wie Sie Aufgaben aus Outlook in OneNote mit Aspose.Note
  für Java extrahieren. Folgen Sie dieser Schritt‑für‑Schritt‑Anleitung, um Aufgabendetails
  schnell abzurufen.
keywords:
- how to extract tasks
- Aspose.Note Java
- Outlook task extraction
linktitle: Outlook‑Aufgabe in OneNote abrufen – Aspose.Note
second_title: Aspose.Note Java API
title: Wie man Outlook‑Aufgaben in OneNote mit Aspose.Note extrahiert
url: /de/java/task-and-outlook-integration/get-outlook-task/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Outlook-Aufgabe in OneNote abrufen - Aspose.Note

## Einleitung
Willkommen zu unserem umfassenden Leitfaden, wie man **Aufgaben extrahiert** aus Outlook in einem OneNote-Notizbuch mithilfe von Aspose.Note für Java. Egal, ob Sie ein Migrationswerkzeug erstellen, Berichte generieren oder einfach Aufgaben‑Daten synchronisieren müssen, führt Sie dieses Tutorial durch jeden Schritt – vom Laden der OneNote‑Datei bis zum Auslesen der Eigenschaften jeder Outlook‑Aufgabe. Am Ende haben Sie ein einsatzbereites Code‑Snippet, das Sie an Ihre eigenen Projekte anpassen können.

## Schnelle Antworten
- **Worum geht es in diesem Tutorial?** Extrahieren von Outlook‑Aufgabendetails aus einem OneNote‑Dokument mit Aspose.Note für Java.  
- **Welche API wird verwendet?** Aspose.Note Java‑Bibliothek.  
- **Benötige ich eine Lizenz?** Eine kostenlose Testversion reicht für die Entwicklung; für die Produktion ist eine kommerzielle Lizenz erforderlich.  
- **Wie lange dauert die Implementierung?** Etwa 10‑15 Minuten, sobald die Umgebung eingerichtet ist.  
- **Kann ich mehrere Notizbücher verarbeiten?** Ja – einfach über die Dateien iterieren und dieselbe Logik wiederverwenden.

## Was ist Aufgabenextraktion?
Aufgabenextraktion bezeichnet das Lesen strukturierter Aufgabeninformationen (wie Fälligkeitsdaten, Status und Symbole), die Outlook innerhalb von OneNote‑Seiten als `NoteTask`‑Tags speichert. Dadurch erhalten Sie programmgesteuerten Zugriff auf Aufgabendaten, ohne manuell kopieren zu müssen.

## Warum Aspose.Note für Java verwenden?
- **Kein Microsoft Office erforderlich** – funktioniert auf jeder Plattform mit einer Java‑Laufzeit.  
- **Vollständige Treue** – bewahrt alle OneNote‑Elemente und gibt Ihnen direkten Zugriff auf Tags.  
- **Hohe Leistung** – optimiert für große Notizbücher und Batch‑Verarbeitung.  

## Voraussetzungen
Bevor wir beginnen, stellen Sie sicher, dass Sie Folgendes bereit haben:

- **Java-Entwicklungsumgebung** – JDK 8 oder neuer installiert und konfiguriert.  
- **Aspose.Note-Bibliothek** – Laden Sie das neueste Java‑Paket von der offiziellen Seite [here](https://releases.aspose.com/note/java/).  
- **Eine Beispiel-OneNote-Datei** – Das Tutorial verwendet `Sample1.one`; Sie können sie durch jedes Notizbuch ersetzen, das Outlook‑Aufgaben enthält.

## Pakete importieren
Fügen Sie die erforderlichen Importe zu Ihrer Java‑Klasse hinzu. Diese Klassen geben Ihnen Zugriff auf das Dokumentenmodell und das Outlook‑spezifische `NoteTask`‑Tag.

```java
import java.io.IOException;
import java.util.List;
import com.aspose.note.Document;
import com.aspose.note.ITag;
import com.aspose.note.NoteTask;
import com.aspose.note.RichText;
```

## Schritt‑für‑Schritt‑Anleitung

### Schritt 1: Dokumentverzeichnis einrichten
Definieren Sie den Ordner, der Ihre OneNote‑Datei enthält. Sowohl ein absoluter als auch ein relativer Pfad funktionieren, achten Sie jedoch darauf, den Pfad‑String übersichtlich zu halten.

```java
String dataDir = "Your Document Directory";
```

### Schritt 2: OneNote‑Dokument laden
Erzeugen Sie eine `Document`‑Instanz, indem Sie auf die `.one`‑Datei verweisen. Aspose.Note parst die Datei in eine DOM‑ähnliche Struktur, die Sie traversieren können.

```java
Document doc = new Document(dataDir + "Sample1.one");
```

### Schritt 3: Alle RichText‑Knoten abrufen
Outlook‑Aufgaben werden in `RichText`‑Elementen gespeichert. Rufen Sie jeden `RichText`‑Knoten ab, damit Sie dessen Tags prüfen können.

```java
List<RichText> nodes = (List<RichText>) doc.getChildNodes(RichText.class);
```

### Schritt 4: Jeden Knoten iterieren
Iterieren Sie über jeden `RichText`‑Knoten, untersuchen Sie dessen Tags und handeln Sie, wenn Sie ein `NoteTask`‑Tag finden. Der untenstehende Code gibt die nützlichsten Eigenschaften jeder Aufgabe aus.

```java
for (RichText richText : nodes) {
    for (ITag tag : richText.getTags()) {
        if (tag.getClass() == NoteTask.class) {
            NoteTask noteTask = (NoteTask) tag;
            
            // Retrieve properties
            System.out.println("Completed Time: " + noteTask.getCompletedTime());
            System.out.println("Create Time: " + noteTask.getCreationTime());
            System.out.println("Due Date: " + noteTask.getDueDate());
            System.out.println("Status: " + noteTask.getStatus());
            System.out.println("Icon: " + noteTask.getIcon());
        }
    }
}
```

**Pro Tipp:** Wenn Sie nur einen Teil der Eigenschaften benötigen, können Sie die anderen überspringen, um die Leistung bei der Verarbeitung großer Notizbücher zu verbessern.

### Häufige Probleme & Lösungen
- **Keine Aufgaben gefunden:** Stellen Sie sicher, dass die OneNote‑Seite tatsächlich Outlook‑Aufgaben enthält. Sie erscheinen als Kontrollkästchen mit einem kleinen Outlook‑Symbol.  
- **Null‑Werte:** Einige Aufgabenfelder (z. B. `CompletedTime`) können `null` sein, wenn die Aufgabe noch nicht abgeschlossen ist. Schützen Sie sich vor `NullPointerException`, indem Sie vor dem Ausgeben auf `null` prüfen.  
- **Datei nicht gefunden:** Vergewissern Sie sich, dass `dataDir` mit dem passenden Pfadtrennzeichen (`/` oder `\\`) für Ihr Betriebssystem endet.

## Fazit
Herzlichen Glückwunsch! Sie haben gelernt, **wie man Aufgaben** aus Outlook in OneNote mithilfe der Aspose.Note Java‑API extrahiert. Dieser Ansatz gibt Ihnen die vollständige programmgesteuerte Kontrolle über Aufgabendaten und ermöglicht die Integration in benutzerdefinierte Reporting‑Tools, Datenbanken oder andere Geschäfts‑Workflows.

## Häufig gestellte Fragen

**Q: Ist Aspose.Note mit allen Versionen von OneNote kompatibel?**  
A: Aspose.Note unterstützt Microsoft OneNote 2010 und spätere Versionen.

**Q: Kann ich Aspose.Note sowohl für private als auch für kommerzielle Projekte nutzen?**  
A: Ja, Aspose.Note kann sowohl für private als auch für kommerzielle Projekte verwendet werden. Besuchen Sie [here](https://purchase.aspose.com/buy), um Lizenzoptionen zu erkunden.

**Q: Gibt es eine kostenlose Testversion für Aspose.Note?**  
A: Ja, Sie können die kostenlose Testversion [here](https://releases.aspose.com/) nutzen.

**Q: Wie kann ich Support für Aspose.Note erhalten?**  
A: Besuchen Sie das [Aspose.Note Forum](https://forum.aspose.com/c/note/28) für Community‑Support. Für zusätzliche Hilfe können Sie eine [temporary license](https://purchase.aspose.com/temporary-license/) erwerben.

**Q: Gibt es Beispiel‑OneNote‑Dokumente zum Testen?**  
A: Sie finden Beispiel‑Dokumente in der Aspose.Note‑Dokumentation [here](https://reference.aspose.com/note/java/).

---

**Zuletzt aktualisiert:** 2026-04-01  
**Getestet mit:** Aspose.Note für Java 24.12 (zum Zeitpunkt des Schreibens neueste)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}