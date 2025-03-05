---
title: Erhalten Sie Revisionen von Seiten in OneNote – Aspose.Note
linktitle: Erhalten Sie Revisionen von Seiten in OneNote – Aspose.Note
second_title: Aspose.Note Java API
description: Erfahren Sie, wie Sie mit Aspose.Note Java Revisionen von Seiten in OneNote-Dokumenten abrufen. Integrieren Sie dies in Ihre Java-Apps für eine effiziente Dokumentenverwaltung.
type: docs
weight: 15
url: /de/java/onenote-page-manipulation/get-revisions-of-pages/
---
## Einführung

In diesem Tutorial befassen wir uns mit den Funktionen von Aspose.Note für Java, einer leistungsstarken Bibliothek, die Ihnen die nahtlose Arbeit mit Microsoft OneNote-Dateien in Ihren Java-Anwendungen ermöglicht. Konkret konzentrieren wir uns auf das Abrufen von Revisionen von Seiten innerhalb eines OneNote-Dokuments. Am Ende dieses Leitfadens verfügen Sie über das nötige Wissen, um Seitenrevisionen effizient zu extrahieren, einschließlich Details wie der letzten Änderungszeit, der Erstellungszeit, dem Titel, der Ebene und dem Autor.

## Voraussetzungen

Bevor Sie mit diesem Tutorial beginnen, stellen Sie sicher, dass die folgenden Voraussetzungen erfüllt sind:

### Java Development Kit (JDK) installiert

Stellen Sie sicher, dass das Java Development Kit auf Ihrem System installiert ist. Sie können es von der Oracle-Website herunterladen und installieren oder einen Paketmanager verwenden, wenn Sie ein Unix-basiertes System verwenden.

### Aspose.Note für Java-Bibliothek

 Laden Sie die Aspose.Note für Java-Bibliothek von der Website herunter und installieren Sie sie. Den Download-Link finden Sie hier[Hier](https://releases.aspose.com/note/java/) . Befolgen Sie die Installationsanweisungen in der Dokumentation[Hier](https://reference.aspose.com/note/java/).

## Pakete importieren

Importieren Sie zunächst die erforderlichen Pakete in Ihr Java-Projekt. Mit diesen Paketen können Sie die von Aspose.Note für Java bereitgestellten Funktionen nutzen.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.PageHistory;
```

Lassen Sie uns nun den bereitgestellten Beispielcode in mehrere Schritte aufteilen, um jede Komponente und ihre Funktionalität zu verstehen.

## Schritt 1: Dokumentverzeichnis festlegen

Definieren Sie das Verzeichnis, in dem sich Ihr OneNote-Dokument befindet.

```java
String dataDir = "Your Document Directory";
```

## Schritt 2: Laden Sie das Dokument

Laden Sie das OneNote-Dokument in Aspose.Note.

```java
Document doc = new Document(dataDir + "Sample1.one");
```

## Schritt 3: Erste Seite abrufen

Rufen Sie die erste Seite aus dem Dokument ab.

```java
Page firstPage = doc.getFirstChild();
```

## Schritt 4: Seitenrevisionen abrufen

Rufen Sie den Revisionsverlauf der Seite ab.

```java
PageHistory revisions = doc.getPageHistory(firstPage);
```

## Schritt 5: Seitenrevisionen durchlaufen

Durchsuchen Sie die Liste der Seitenrevisionen und rufen Sie relevante Informationen ab.

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

## Abschluss

In diesem Tutorial haben wir untersucht, wie Sie mit Aspose.Note für Java Revisionen von Seiten in einem OneNote-Dokument abrufen. Wenn Sie der Schritt-für-Schritt-Anleitung folgen und den bereitgestellten Beispielcode nutzen, können Sie diese Funktionalität problemlos in Ihre Java-Anwendungen integrieren und so eine effiziente Verwaltung von OneNote-Dateien ermöglichen.

## FAQs

### F1: Kann ich Aspose.Note für Java verwenden, um neue OneNote-Dokumente zu erstellen?

A1: Ja, Aspose.Note für Java bietet umfassende Unterstützung für das programmgesteuerte Erstellen, Lesen und Bearbeiten von OneNote-Dokumenten.

### F2: Ist Aspose.Note für Java mit verschiedenen Versionen von OneNote-Dateien kompatibel?

A2: Ja, Aspose.Note für Java unterstützt verschiedene Versionen von Microsoft OneNote-Dateien und gewährleistet so die Kompatibilität in verschiedenen Umgebungen.

### F3: Kann ich das Ausgabeformat beim Exportieren von OneNote-Dokumenten anpassen?

A3: Absolut, Aspose.Note für Java bietet Flexibilität beim Exportieren von OneNote-Dokumenten in verschiedene Formate wie PDF, HTML und Bilder, mit Optionen zur Anpassung.

### F4: Benötigt Aspose.Note für Java eine Lizenz für die kommerzielle Nutzung?

A4: Ja, für die kommerzielle Nutzung von Aspose.Note für Java ist eine gültige Lizenz erforderlich. Eine Lizenz erhalten Sie auf der Aspose-Website.

### F5: Wo kann ich Hilfe suchen, wenn ich auf Probleme stoße oder Fragen zu Aspose.Note für Java habe?

 A5: Für Unterstützung und Unterstützung können Sie das Aspose.Note-Forum besuchen[Hier](https://forum.aspose.com/c/note/28)Hier können Sie Fragen stellen, Erfahrungen austauschen und mit anderen Benutzern und Experten interagieren.