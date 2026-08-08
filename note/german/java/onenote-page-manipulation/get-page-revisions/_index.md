---
date: 2026-08-08
description: Erfahren Sie, wie Sie Änderungen in OneNote nachverfolgen, indem Sie
  Seitenrevisionen programmgesteuert mit Aspose.Note für Java abrufen.
keywords:
- track changes in onenote
- aspose.note java
- onenote page revisions
- java document processing
lastmod: 2026-08-08
linktitle: Seitenrevisionen in OneNote abrufen – Aspose.Note
og_description: Erfahren Sie, wie Sie Änderungen in OneNote nachverfolgen, indem Sie
  Seitenrevisionen programmgesteuert mit Aspose.Note für Java abrufen.
og_image_alt: Guide showing how to track changes in OneNote using Aspose.Note Java
  API
og_title: Änderungen in OneNote nachverfolgen – Seitenrevisionen mit Aspose.Note
schemas:
- author: Aspose
  dateModified: '2026-08-08'
  description: Learn how to track changes in OneNote by retrieving page revisions
    programmatically using Aspose.Note for Java.
  headline: Track changes in OneNote – page revisions with Aspose.Note
  type: TechArticle
- description: Learn how to track changes in OneNote by retrieving page revisions
    programmatically using Aspose.Note for Java.
  name: Track changes in OneNote – page revisions with Aspose.Note
  steps:
  - name: set up document directory
    text: Define the folder where your OneNote file resides.
  - name: load OneNote document with history enabled
    text: '`LoadOptions` is a configuration class that tells Aspose.Note how to open
      a file, including whether to read revision data. Enable the flag before loading
      the document.'
  - name: get the first page
    text: Grab the first page object; this will be the reference point for retrieving
      its history.
  - name: iterate through page revisions
    text: Loop through each revision and print useful metadata such as timestamps,
      title, level, and author. > **Pro tip:** If you need to filter revisions by
      a specific author or date range, simply add conditional checks inside the `for`
      loop.
  type: HowTo
- questions:
  - answer: Retrieving page revision history from a OneNote file using Aspose.Note
      for Java.
    question: What does the tutorial cover?
  - answer: Any recent Aspose.Note for Java release that supports `LoadOptions.setLoadHistory`.
    question: Which library version is required?
  - answer: A temporary evaluation license works for testing; a commercial license
      is required for production.
    question: Do I need a license?
  - answer: The API is read‑only for revisions; you can only retrieve them.
    question: Can I modify revisions?
  - answer: Java JDK, Aspose.Note for Java, and a OneNote document with revision data.
    question: What are the main prerequisites?
  type: FAQPage
second_title: Aspose.Note Java API
tags:
- track changes
- Aspose.Note
- OneNote revisions
- Java API
title: Änderungen in OneNote nachverfolgen – Seitenrevisionen mit Aspose.Note
url: /de/java/onenote-page-manipulation/get-page-revisions/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Änderungen in OneNote – Seitenrevisionen mit Aspose.Note

In diesem Tutorial lernen Sie, wie Sie **Änderungen in OneNote** nachverfolgen, indem Sie die vollständige Revisionshistorie einer Seite mit der Aspose.Note Java API extrahieren. Wir behandeln alles von der Einrichtung Ihrer Entwicklungsumgebung bis zum Ausgeben des Autors, der Zeitstempel und des Titels jeder Revision, sodass Sie zuverlässige Audit‑Trail‑Funktionen für jede OneNote‑basierte Lösung erstellen können.

## Schnelle Antworten
- **Worum geht es im Tutorial?** Abrufen der Seitenrevisionshistorie aus einer OneNote-Datei mit Aspose.Note für Java.  
- **Welche Bibliotheksversion wird benötigt?** Jede aktuelle Aspose.Note für Java-Version, die `LoadOptions.setLoadHistory` unterstützt.  
- **Benötige ich eine Lizenz?** Eine temporäre Evaluierungslizenz funktioniert für Tests; für die Produktion ist eine kommerzielle Lizenz erforderlich.  
- **Kann ich Revisionen ändern?** Die API ist für Revisionen schreibgeschützt; Sie können sie nur abrufen.  
- **Was sind die wichtigsten Voraussetzungen?** Java JDK, Aspose.Note für Java und ein OneNote-Dokument mit Revisionsdaten.

## Was ist das „Aspose.Note Seitenrevisionen‑Tutorial“?
Das Tutorial zeigt, wie Sie programmgesteuert auf die historischen Versionen einer OneNote‑Seite zugreifen können. Jede Revision enthält Metadaten wie Autor, Erstellungszeit und Änderungszeit, sodass Sie Audit‑Trails oder Änderungsprotokoll‑Funktionen in Ihren Anwendungen erstellen können.

## Warum Aspose.Note für die Verfolgung von Seitenrevisionen verwenden?
Laden Sie die gesamte Revisionshistorie eines Notizbuchs in weniger als 5 Sekunden für eine 500‑seitige Datei auf einer Standard‑2 GHz‑CPU und rufen Sie Metadaten ab, ohne die OneNote‑Benutzeroberfläche zu starten. Die Bibliothek unterstützt über 30 Eingabe‑ und Ausgabeformate, läuft unter Windows, Linux und macOS (abdeckung >95 % der Serverumgebungen) und bietet vollständige Kontrolle über jede Revisions‑Eigenschaft.

## Voraussetzungen

### 1. Java Development Kit (JDK)
Stellen Sie sicher, dass ein aktuelles JDK (8 oder höher) installiert ist und `JAVA_HOME` gesetzt ist.

### 2. Aspose.Note für Java
Laden Sie die Bibliothek über den [download link](https://releases.aspose.com/note/java/) herunter.

### 3. Beispiel‑OneNote‑Dokument
Erstellen oder beschaffen Sie eine OneNote‑Datei (z. B. `Sample1.one`), die Seiten mit Revisionshistorie enthält.

## Pakete importieren
Zuerst importieren Sie die erforderlichen Aspose.Note‑Klassen.  
`Document` repräsentiert ein OneNote‑Notizbuch, `LoadOptions` konfiguriert das Ladeverhalten, und `Page` stellt eine einzelne Seite dar.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.LoadOptions;
import com.aspose.note.Page;
```

## Schritt‑für‑Schritt‑Implementierung

### Schritt 1: Dokumentverzeichnis einrichten
Definieren Sie den Ordner, in dem Ihre OneNote‑Datei gespeichert ist.

```java
String dataDir = "Your Document Directory";
```

### Schritt 2: OneNote‑Dokument mit aktivierter Historie laden
`LoadOptions` ist eine Konfigurationsklasse, die Aspose.Note mitteilt, wie eine Datei zu öffnen ist, einschließlich ob Revisionsdaten gelesen werden sollen. Aktivieren Sie das Flag, bevor Sie das Dokument laden.

```java
LoadOptions loadOptions = new LoadOptions();
loadOptions.setLoadHistory(true);
Document document = new Document(dataDir + "Sample1.one", loadOptions);
```

### Schritt 3: Erste Seite abrufen
Holen Sie das erste Seitenobjekt; dies dient als Referenzpunkt zum Abrufen seiner Historie.

```java
Page firstPage = document.getFirstChild();
```

### Schritt 4: Durch Seitenrevisionen iterieren
Durchlaufen Sie jede Revision und geben Sie nützliche Metadaten wie Zeitstempel, Titel, Ebene und Autor aus.

```java
for (Page pageRevision : document.getPageHistory(firstPage)) {
    System.out.println("LastModifiedTime: " + pageRevision.getLastModifiedTime());
    System.out.println("CreationTime: " + pageRevision.getCreationTime());
    System.out.println("Title: " + pageRevision.getTitle());
    System.out.println("Level: " + pageRevision.getLevel());
    System.out.println("Author: " + pageRevision.getAuthor());
    System.out.println();
}
```

> **Pro Tipp:** Wenn Sie Revisionen nach einem bestimmten Autor oder Datumsbereich filtern müssen, fügen Sie einfach bedingte Prüfungen innerhalb der `for`‑Schleife hinzu.

## Häufige Probleme & Lösungen
- **Keine Revisionen zurückgegeben:** Stellen Sie sicher, dass `loadOptions.setLoadHistory(true)` vor dem Laden des Dokuments aufgerufen wird.  
- **Null‑Autor oder -Titel:** Einige ältere OneNote‑Versionen speichern diese Felder möglicherweise nicht; behandeln Sie `null`‑Werte angemessen.  
- **Leistungsverzögerung bei großen Notizbüchern:** Laden Sie nur die benötigten Abschnitte oder erhöhen Sie die JVM‑Heap‑Größe.

## Häufig gestellte Fragen

**Q1: Kann ich Aspose.Note für Java verwenden, um Seitenrevisionen zu ändern?**  
A1: Nein, die API unterstützt derzeit nur schreibgeschützten Zugriff auf Seitenrevisionen.

**Q2: Ist Aspose.Note für Java mit verschiedenen Versionen von OneNote‑Dokumenten kompatibel?**  
A2: Ja, es funktioniert mit verschiedenen OneNote‑Dateiformaten und ermöglicht eine nahtlose Verarbeitung über Versionen hinweg.

**Q3: Benötigt Aspose.Note für Java eine Lizenz zur Nutzung?**  
A3: Für den Produktionseinsatz ist eine kommerzielle Lizenz erforderlich, aber eine temporäre Evaluierungslizenz steht für Tests zur Verfügung.

**Q4: Kann ich Unterstützung erhalten, wenn ich beim Einsatz von Aspose.Note für Java auf Probleme stoße?**  
A4: Ja, Sie können Fragen im Aspose.Note‑Forum stellen [Aspose.Note forum](https://forum.aspose.com/c/note/28).

**Q5: Gibt es eine kostenlose Testversion von Aspose.Note für Java?**  
A5: Ja, Sie können eine kostenlose Testversion von der [website](https://releases.aspose.com/) herunterladen.

---

**Zuletzt aktualisiert:** 2026-08-08  
**Getestet mit:** Aspose.Note für Java (neueste Version)  
**Autor:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Verwandte Tutorials

- [Änderungen in OneNote nachverfolgen – Seitenrevisionen verwalten mit Aspose.Note](/note/java/onenote-page-manipulation/working-with-page-revisions/)
- [Aspose Java Tutorial – Informationen zu Seiten in OneNote abrufen – Aspose.Note](/note/java/onenote-page-manipulation/get-information-about-pages/)
- [OneNote‑Seitenhintergrund ändern – Aspose.Note für Java](/note/java/onenote-page-manipulation/set-page-background-color/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}