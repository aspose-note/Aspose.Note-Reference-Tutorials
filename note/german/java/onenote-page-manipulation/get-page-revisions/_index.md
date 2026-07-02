---
date: 2026-01-10
description: Lernen Sie das Aspose.Note‑Tutorial zu Seitenrevisionen für Java – rufen
  Sie OneNote‑Seitenrevisionen programmgesteuert mit Aspose.Note ab. Folgen Sie unserer
  Schritt‑für‑Schritt‑Anleitung.
linktitle: Get Page Revisions in OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: aspose.note Seitenrevisionen Tutorial – Seitenrevisionen in OneNote abrufen
url: /de/java/onenote-page-manipulation/get-page-revisions/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Seitenrevisionen in OneNote abrufen - Aspose.Note

OneNote ist eine leistungsstarke Notizplattform, und wenn Sie Änderungen prüfen müssen, zeigt Ihnen das **aspose.note page revisions tutorial** genau, wie Sie die Revisionshistorie mit nur wenigen Zeilen Java‑Code abrufen. In diesem Leitfaden führen wir Sie durch alles, was Sie benötigen – von der Einrichtung der Umgebung bis zum Ausgeben der Details jeder Revision – damit Sie Änderungen, Autorenbeiträge und Zeitstempel mühelos nachverfolgen können.

## Schnelle Antworten
- **Worum geht es im Tutorial?** Retrieving page revision history from a OneNote file using Aspose.Note for Java.  
- **Welche Bibliotheksversion ist erforderlich?** Any recent Aspose.Note for Java release that supports `LoadOptions.setLoadHistory`.  
- **Benötige ich eine Lizenz?** A temporary evaluation license works for testing; a commercial license is required for production.  
- **Kann ich Revisionen ändern?** The API is read‑only for revisions; you can only retrieve them.  
- **Was sind die wichtigsten Voraussetzungen?** Java JDK, Aspose.Note for Java, and a OneNote document with revision data.

## Was ist das „aspose.note page revisions tutorial“?
Das Tutorial zeigt, wie Sie programmgesteuert auf die historischen Versionen einer OneNote‑Seite zugreifen können. Jede Revision enthält Metadaten wie Autor, Erstellungszeit und Änderungszeit, sodass Sie Prüfpfade oder Änderungsprotokoll‑Funktionen in Ihren Anwendungen erstellen können.

## Warum Aspose.Note für die Verfolgung von Seitenrevisionen verwenden?
- **Keine UI‑Abhängigkeit** – funktioniert vollständig im Code und ist ideal für Backend‑Dienste.  
- **Plattformübergreifend** – Java läuft auf Windows, Linux und macOS.  
- **Vollständige Kontrolle** – ruft jede Revisions‑Eigenschaft ab, ohne OneNote manuell zu öffnen.  
- **Performance** – das Laden der Historie ist optimiert, sodass selbst große Notizbücher schnell verarbeitet werden.

## Voraussetzungen

### 1. Java Development Kit (JDK)
Stellen Sie sicher, dass ein aktuelles JDK (8 oder höher) installiert ist und `JAVA_HOME` gesetzt ist.

### 2. Aspose.Note for Java
Laden Sie die Bibliothek über den [download link](https://releases.aspose.com/note/java/) herunter.

### 3. Beispiel‑OneNote‑Dokument
Erstellen Sie ein OneNote‑Datei (z. B. `Sample1.one`) oder holen Sie eine, die Seiten mit Revisionshistorie enthält.

## Pakete importieren
Importieren Sie zunächst die erforderlichen Aspose.Note‑Klassen.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.LoadOptions;
import com.aspose.note.Page;
```

## Schritt‑für‑Schritt‑Implementierung

### Schritt 1: Dokumentverzeichnis einrichten
Definieren Sie den Ordner, in dem sich Ihre OneNote‑Datei befindet.

```java
String dataDir = "Your Document Directory";
```

### Schritt 2: OneNote‑Dokument mit aktivierter Historie laden
Aktivieren Sie das `LoadOptions`‑Flag, um Revisionsdaten abzurufen.

```java
LoadOptions loadOptions = new LoadOptions();
loadOptions.setLoadHistory(true);
Document document = new Document(dataDir + "Sample1.one", loadOptions);
```

### Schritt 3: Erste Seite abrufen
Holen Sie das erste Seitenobjekt; dies dient als Referenzpunkt zum Abrufen seiner Historie.

```java
Page firstPage = document.getFirstChild();
```

### Schritt 4: Durch Seitenrevisionen iterieren
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

> **Pro‑Tipp:** Wenn Sie Revisionen nach einem bestimmten Autor oder Datumsbereich filtern müssen, fügen Sie einfach bedingte Prüfungen innerhalb der `for`‑Schleife hinzu.

## Häufige Probleme & Lösungen
- **Keine Revisionen zurückgegeben:** Stellen Sie sicher, dass `loadOptions.setLoadHistory(true)` vor dem Laden des Dokuments aufgerufen wird.  
- **Null‑Autor oder -Titel:** Einige ältere OneNote‑Versionen speichern diese Felder möglicherweise nicht; behandeln Sie `null`‑Werte angemessen.  
- **Performance‑Verzögerung bei großen Notizbüchern:** Laden Sie nur die benötigten Abschnitte oder erhöhen Sie die JVM‑Heap‑Größe.

## Häufig gestellte Fragen

**Q1: Kann ich Aspose.Note für Java verwenden, um Seitenrevisionen zu ändern?**  
A1: Nein, die API unterstützt derzeit nur den schreibgeschützten Zugriff auf Seitenrevisionen.

**Q2: Ist Aspose.Note für Java mit verschiedenen Versionen von OneNote‑Dokumenten kompatibel?**  
A2: Ja, es funktioniert mit verschiedenen OneNote‑Dateiformaten und ermöglicht eine nahtlose Verarbeitung über Versionen hinweg.

**Q3: Benötigt Aspose.Note für Java eine Lizenz?**  
A3: Für den Produktionseinsatz ist eine kommerzielle Lizenz erforderlich, aber eine temporäre Evaluationslizenz steht für Tests zur Verfügung.

**Q4: Kann ich Unterstützung erhalten, wenn ich beim Einsatz von Aspose.Note für Java auf Probleme stoße?**  
A4: Ja, Sie können im Aspose.Note‑Forum [hier](https://forum.aspose.com/c/note/28) Fragen stellen.

**Q5: Gibt es eine kostenlose Testversion von Aspose.Note für Java?**  
A5: Ja, Sie können eine kostenlose Testversion von der [Website](https://releases.aspose.com/) herunterladen.

---

**Zuletzt aktualisiert:** 2026-01-10  
**Getestet mit:** Aspose.Note for Java (latest release)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}