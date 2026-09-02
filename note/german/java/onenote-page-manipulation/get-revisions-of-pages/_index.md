---
date: 2026-01-10
description: Erfahren Sie, wie Sie die letzte Änderungszeit ermitteln und Revisionen
  von OneNote‑Seiten mit Aspose.Note für Java abrufen können. Integrieren Sie dies
  in Ihre Java‑Anwendungen für ein effizientes Dokumentenmanagement.
linktitle: Get Revisions of Pages in OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: Wie man die letzte Änderungszeit von OneNote‑Seiten ermittelt – Aspose.Note
url: /de/java/onenote-page-manipulation/get-revisions-of-pages/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Abrufen von Revisionen von Seiten in OneNote - Aspose.Note

## Einleitung

In diesem Tutorial erhalten Sie **die letzte Änderungszeit** für Seiten in einem OneNote‑Dokument und erfahren, wie Sie die vollständige Revisionshistorie mit Aspose.Note für Java abrufen können. Egal, ob Sie ein Dokument‑Management‑System bauen, Änderungen prüfen oder einfach anzeigen möchten, wann eine Seite zuletzt bearbeitet wurde – diese Anleitung zeigt Ihnen Schritt für Schritt, wie Sie diese Informationen programmgesteuert extrahieren.

## Schnelle Antworten
- **Was gibt „get last modified time“ zurück?** Der Zeitstempel der zuletzt vorgenommenen Bearbeitung einer OneNote‑Seite.  
- **Welche Klasse liefert die Revisionshistorie?** `PageHistory` über `Document.getPageHistory(Page)`.  
- **Benötige ich eine Lizenz für diese Funktion?** Ja, eine gültige Aspose.Note‑Lizenz ist für den Produktionseinsatz erforderlich.  
- **Welche Java‑Version wird unterstützt?** Java 8 oder höher (JDK 8+).  
- **Kann ich Revisionen nach Autor filtern?** Sie können die `Author`‑Eigenschaft jedes `Page`‑Objekts auslesen und Ihren eigenen Filter anwenden.

## Was ist „get last modified time“ in OneNote?

**Die **last modified time** ist ein Metadatenfeld, das mit jeder Seite gespeichert wird und den Zeitpunkt der zuletzt vorgenommenen Änderung aufzeichnet. Aspose.Note stellt diesen Wert über die Methode `Page.getLastModifiedTime()` bereit, sodass er leicht angezeigt oder protokolliert werden kann.**

## Warum Seitenrevisionen abrufen?

- **Audit‑Spuren:** Halten Sie fest, wer was und wann geändert hat.  
- **Versionsvergleich:** Erstellen Sie Funktionen, die zwei Revisionen nebeneinander vergleichen.  
- **Einblicke in die Zusammenarbeit von Benutzern:** Verstehen Sie Bearbeitungsmuster in gemeinsam genutzten Notizbüchern.  

## Voraussetzungen

Bevor Sie beginnen, stellen Sie sicher, dass Sie Folgendes haben:

### Java Development Kit (JDK) installiert
Installieren Sie JDK 8 oder höher von der Oracle-Website oder Ihrem bevorzugten Paketmanager.

### Aspose.Note für Java-Bibliothek
Laden Sie die Bibliothek von der offiziellen Seite herunter. Den Download‑Link finden Sie **[hier](https://releases.aspose.com/note/java/)**. Befolgen Sie die Installationsanweisungen in der Dokumentation **[hier](https://reference.aspose.com/note/java/)**.

## Pakete importieren

Um zu beginnen, importieren Sie die erforderlichen Pakete in Ihr Java‑Projekt. Diese Pakete ermöglichen es Ihnen, die von Aspose.Note für Java bereitgestellte Funktionalität zu nutzen.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.PageHistory;
```

Jetzt zerlegen wir den bereitgestellten Beispielcode in mehrere Schritte, um jede Komponente und ihre Funktionalität zu verstehen.

## Wie man die letzte Änderungszeit einer OneNote‑Seite erhält

### Schritt 1: Dokumentverzeichnis festlegen
Definieren Sie das Verzeichnis, in dem sich Ihr OneNote‑Dokument befindet.

```java
String dataDir = "Your Document Directory";
```

### Schritt 2: Dokument laden
Laden Sie das OneNote‑Dokument in Aspose.Note.

```java
Document doc = new Document(dataDir + "Sample1.one");
```

### Schritt 3: Erste Seite abrufen
Rufen Sie die erste Seite aus dem Dokument ab.

```java
Page firstPage = doc.getFirstChild();
```

### Schritt 4: Seitenrevisionen abrufen
Erhalten Sie die Revisionshistorie der Seite.

```java
PageHistory revisions = doc.getPageHistory(firstPage);
```

### Schritt 5: Seitenrevisionen durchlaufen
Iterieren Sie durch die Liste der Seitenrevisionen und holen Sie relevante Informationen, einschließlich der **last modified time**.

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

## Häufige Probleme und Lösungen
- **Null `PageHistory`:** Stellen Sie sicher, dass das Dokument tatsächlich Revisionen enthält; andernfalls kann `getPageHistory` `null` zurückgeben.  
- **Zeitzonendifferenzen:** `getLastModifiedTime()` gibt ein `java.util.Date` in der Standardzeitzone des Systems zurück. Konvertieren Sie es bei Bedarf nach UTC.  
- **Lizenz nicht geladen:** Ohne eine gültige Lizenz kann Aspose.Note im Evaluierungsmodus arbeiten, wodurch die Anzahl der verarbeiteten Seiten begrenzt wird.

## Häufig gestellte Fragen

### Q1: Kann ich Aspose.Note für Java verwenden, um neue OneNote‑Dokumente zu erstellen?
A1: Ja, Aspose.Note für Java bietet umfassende Unterstützung zum Erstellen, Lesen und programmgesteuerten Bearbeiten von OneNote‑Dokumenten.

### Q2: Ist Aspose.Note für Java mit verschiedenen Versionen von OneNote‑Dateien kompatibel?
A2: Ja, Aspose.Note für Java unterstützt verschiedene Versionen von Microsoft OneNote‑Dateien und gewährleistet die Kompatibilität in unterschiedlichen Umgebungen.

### Q3: Kann ich das Ausgabeformat beim Exportieren von OneNote‑Dokumenten anpassen?
A3: Absolut, Aspose.Note für Java bietet Flexibilität beim Exportieren von OneNote‑Dokumenten in verschiedene Formate wie PDF, HTML und Bilder, mit Anpassungsoptionen.

### Q4: Erfordert Aspose.Note für Java eine Lizenz für die kommerzielle Nutzung?
A4: Ja, für die kommerzielle Nutzung von Aspose.Note für Java ist eine gültige Lizenz erforderlich. Sie können eine Lizenz über die Aspose‑Website erhalten.

### Q5: Wo kann ich Hilfe erhalten, wenn ich Probleme habe oder Fragen zu Aspose.Note für Java habe?
A5: Für Support und Hilfe können Sie das Aspose.Note‑Forum **[hier](https://forum.aspose.com/c/note/28)** besuchen, wo Sie Fragen stellen, Erfahrungen teilen und mit anderen Benutzern und Experten interagieren können.

---

**Zuletzt aktualisiert:** 2026-01-10  
**Getestet mit:** Aspose.Note für Java 23.12 (neueste zum Zeitpunkt der Erstellung)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}