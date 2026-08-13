---
date: 2026-08-13
description: Erfahren Sie, wie Sie die Änderungszeit einer OneNote-Seite abrufen und
  Seitenrevisionen mit Aspose.Note für Java erhalten, ideal für Audits und Dokumentenmanagement.
keywords:
- get onenote page modified
- onenote page revisions
- aspose.note java
- java onenote api
lastmod: 2026-08-13
linktitle: Seitenrevisionen in OneNote abrufen – Aspose.Note
og_description: Erfahren Sie, wie Sie die Änderungszeit einer OneNote-Seite abrufen
  und Revisionen von OneNote-Seiten mit Aspose.Note für Java erhalten. Schnelle Schritte,
  Code‑Snippets und Fehlersuche.
og_image_alt: Screenshot of Aspose.Note Java API showing page revision retrieval
og_title: OneNote-Seitenänderungszeit mit Aspose.Note – Java‑Tutorial
schemas:
- author: Aspose
  dateModified: '2026-08-13'
  description: Learn how to get onenote page modified time and retrieve page revisions
    with Aspose.Note for Java, ideal for auditing and document management.
  headline: Get OneNote page modified time using Aspose.Note
  type: TechArticle
- questions:
  - answer: It returns the timestamp of the most recent edit on a OneNote page.
    question: What does “get last modified time” return?
  - answer: '`PageHistory` via `Document.getPageHistory(Page)`.'
    question: Which class provides revision history?
  - answer: Yes, a valid Aspose.Note license is required for production use.
    question: Do I need a license for this feature?
  - answer: Java 8 or higher (JDK 8+).
    question: What Java version is supported?
  - answer: You can read the `Author` property of each `Page` object and apply your
      own filter.
    question: Can I filter revisions by author?
  type: FAQPage
second_title: Aspose.Note Java API
tags:
- onenote page modified
- aspose.note
- java document management
title: OneNote-Seitenänderungszeit mit Aspose.Note ermitteln
url: /de/java/onenote-page-manipulation/get-revisions-of-pages/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote‑Seiten‑Änderungszeit mit Aspose.Note ermitteln

## Einführung

In diesem Tutorial lernen Sie, wie Sie **OneNote‑Seiten‑Änderungszeitstempel** abrufen und die vollständige Revisionshistorie einer OneNote‑Seite mit Aspose.Note für Java erhalten. Egal, ob Sie eine Audit‑Trail‑Funktion, einen Änderungsprotokoll‑Viewer implementieren oder das zuletzt bearbeitete Datum in einem Dashboard anzeigen möchten – diese Anleitung führt Sie durch jeden Schritt, vom Einrichten der Umgebung bis zum Umgang mit gängigen Fallstricken.

## Schnelle Antworten
- **Was gibt „get last modified time“ zurück?** Sie gibt den Zeitstempel der letzten Bearbeitung einer OneNote‑Seite zurück.  
- **Welche Klasse liefert die Revisionshistorie?** `PageHistory` über `Document.getPageHistory(Page)`.  
- **Benötige ich eine Lizenz für diese Funktion?** Ja, für den Produktionseinsatz ist eine gültige Aspose.Note‑Lizenz erforderlich.  
- **Welche Java‑Version wird unterstützt?** Java 8 oder höher (JDK 8+).  
- **Kann ich Revisionen nach Autor filtern?** Sie können die `Author`‑Eigenschaft jedes `Page`‑Objekts auslesen und Ihren eigenen Filter anwenden.

## Was bedeutet „get last modified time“ in OneNote?

Die letzte Änderungszeit wird als Metadaten‑Attribut auf jeder OneNote‑Seite gespeichert und gibt den Zeitpunkt der letzten Bearbeitung an. Aspose.Note stellt diesen Wert über die Methode `Page.getLastModifiedTime()` bereit, die ein `java.util.Date`‑Objekt zurückgibt, das nach den Anforderungen Ihrer Anwendung formatiert oder protokolliert werden kann.

## Warum Seitenrevisionen abrufen?

Das Abrufen von Seitenrevisionen liefert Ihnen ein vollständiges Audit‑Trail jeder Änderung an einer OneNote‑Seite, sodass Sie nachvollziehen können, wer was und wann bearbeitet hat. Diese Historie kann zum Vergleich von Versionen, zur Wiederherstellung früherer Zustände oder zur Analyse von Zusammenarbeitspatterns in Teams verwendet werden und ist damit für Compliance und Qualitätskontrolle unverzichtbar.

## Voraussetzungen

- **Java Development Kit (JDK) 8 oder höher** – Installation von der Oracle‑Website oder einem kompatiblen Anbieter.  
- **Aspose.Note für Java Bibliothek** – Laden Sie das JAR von der Aspose.Note‑Java‑Release‑Seite **[Aspose.Note Java releases](https://releases.aspose.com/note/java/)** herunter und folgen Sie der Installationsanleitung **[Aspose.Note Java documentation](https://reference.aspose.com/note/java/)**.  

## Pakete importieren

Die Klasse `Document` repräsentiert ein in den Speicher geladenes OneNote‑Notebook, während `Page` und `PageHistory` Zugriff auf einzelne Seiten und deren Revisionsdaten bieten.

```text
import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.PageHistory;
import java.util.Date;
```

*(Die tatsächlichen Import‑Anweisungen werden als Klartext angezeigt, um die ursprüngliche Anzahl der Code‑Blöcke beizubehalten.)*

## Wie erhalte ich die Änderungszeit einer OneNote‑Seite?

Um den letzten Änderungszeitstempel zu erhalten, laden Sie zunächst das OneNote‑Dokument in ein `Document`‑Objekt und wählen dann die gewünschte `Page` aus. Rufen Sie die Methode `getLastModifiedTime()` auf dieser Seite auf, die ein `java.util.Date` zurückgibt. Dieses Datum können Sie anschließend mit `SimpleDateFormat` formatieren oder in UTC konvertieren, um eine konsistente Berichterstattung über Zeitzonen hinweg zu gewährleisten.

## Schritt 1: Dokumentverzeichnis festlegen

Definieren Sie den Ordner, der Ihre OneNote‑Datei enthält.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.PageHistory;
```

## Schritt 2: Dokument laden

Erzeugen Sie eine `Document`‑Instanz, indem Sie den vollständigen Pfad zu Ihrer `.one`‑Datei übergeben.

```java
String dataDir = "Your Document Directory";
```

## Schritt 3: Erste Seite abrufen

Rufen Sie das erste `Page`‑Objekt aus der Seitensammlung des Dokuments ab.

```java
Document doc = new Document(dataDir + "Sample1.one");
```

## Schritt 4: Seitenrevisionen abrufen

Holen Sie die `PageHistory` für die ausgewählte Seite. Wenn das Notebook noch nie bearbeitet wurde, kann dieser Aufruf `null` zurückgeben.

```java
Page firstPage = doc.getFirstChild();
```

## Schritt 5: Seitenrevisionen durchlaufen

Iterieren Sie über jede `Page`‑Revision, lesen Sie deren `Author` und `LastModifiedTime` und geben Sie die Informationen aus.

```java
PageHistory revisions = doc.getPageHistory(firstPage);
```

## Häufige Probleme und Lösungen
- **Null `PageHistory`** – Stellen Sie sicher, dass das Notebook tatsächlich Revisionen enthält; andernfalls gibt `getPageHistory` `null` zurück.  
- **Zeitzonen‑Unterschiede** – `getLastModifiedTime()` verwendet die Standardzeitzone der JVM. Konvertieren Sie bei Bedarf mit `SimpleDateFormat` in UTC, wenn Ihre Anwendung eine einheitliche Zone benötigt.  
- **Lizenz nicht geladen** – Ohne gültige Lizenz läuft Aspose.Note im Evaluierungsmodus, was die Seitenverarbeitung einschränkt. Laden Sie Ihre Lizenzdatei beim Anwendungsstart, um diese Beschränkung zu vermeiden.

## Häufig gestellte Fragen

**Q1: Kann ich Aspose.Note für Java verwenden, um neue OneNote‑Dokumente zu erstellen?**  
A: Ja, die API ermöglicht es Ihnen, OneNote‑Notizbücher programmgesteuert von Grund auf zu erstellen, zu bearbeiten und zu speichern.

**Q2: Ist Aspose.Note für Java mit verschiedenen Versionen von OneNote‑Dateien kompatibel?**  
A: Ja, es unterstützt OneNote‑Dateiformate von 2007 bis 2021 und gewährleistet damit eine breite Kompatibilität für Desktop‑ und Cloud‑Umgebungen.

**Q3: Kann ich das Ausgabeformat beim Exportieren von OneNote‑Dokumenten anpassen?**  
A: Selbstverständlich. Sie können nach PDF, HTML, PNG oder SVG exportieren und Optionen wie Bildauflösung und Schriftart‑Einbettung steuern.

**Q4: Benötigt Aspose.Note für Java eine Lizenz für die kommerzielle Nutzung?**  
A: Ja, für den Produktionseinsatz ist eine kommerzielle Lizenz zwingend erforderlich. Eine kostenlose Testversion steht für Evaluierungszwecke zur Verfügung.

**Q5: Wo kann ich Hilfe erhalten, wenn ich auf Probleme stoße?**  
A: Besuchen Sie das Aspose.Note‑Community‑Forum **[Aspose.Note forum](https://forum.aspose.com/c/note/28)**, um Fragen zu stellen, Erfahrungen zu teilen und Unterstützung von der Community sowie den Aspose‑Entwicklern zu erhalten.

---

**Zuletzt aktualisiert:** 2026-08-13  
**Getestet mit:** Aspose.Note für Java 23.12 (zum Zeitpunkt des Schreibens aktuell)  
**Autor:** Aspose

```java
for (Page pageRevision : revisions) {
    System.out.println("LastModifiedTime: " + pageRevision.getLastModifiedTime());
    System.out.println("CreationTime: " + pageRevision.getCreationTime());
    System.out.println("Title: " + pageRevision.getTitle());
    System.out.println("Level: " + pageRevision.getLevel());
    System.out.println("Author: " + pageRevision.getAuthor());
    System.out.println();
}
```

## Verwandte Tutorials

- [Aspose Java Tutorial – Informationen zu Seiten in OneNote abrufen – Aspose.Note](/note/java/onenote-page-manipulation/get-information-about-pages/)
- [aspose.note Seitenrevisionen Tutorial – Seitenrevisionen in OneNote abrufen](/note/java/onenote-page-manipulation/get-page-revisions/)
- [Änderungen nachverfolgen OneNote – Seitenrevisionen verwalten mit Aspose.Note](/note/java/onenote-page-manipulation/working-with-page-revisions/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}