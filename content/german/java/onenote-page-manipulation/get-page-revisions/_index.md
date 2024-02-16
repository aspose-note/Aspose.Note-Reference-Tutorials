---
title: Seitenrevisionen in OneNote abrufen – Aspose.Note
linktitle: Seitenrevisionen in OneNote abrufen – Aspose.Note
second_title: Aspose.Note Java API
description: Erfahren Sie, wie Sie mit Aspose.Note für Java Seitenrevisionen in OneNote abrufen. Befolgen Sie unsere Schritt-für-Schritt-Anleitung für eine effiziente Nachverfolgung von Änderungen.
type: docs
weight: 14
url: /de/java/onenote-page-manipulation/get-page-revisions/
---
## Einführung

OneNote ist ein leistungsstarkes Tool zum Organisieren und Verwalten Ihrer Notizen. Manchmal müssen Sie jedoch die an Ihren Seiten vorgenommenen Änderungen und Überarbeitungen nachverfolgen. Mit Aspose.Note für Java können Sie Seitenrevisionen ganz einfach programmgesteuert abrufen. In diesem Tutorial führen wir Sie durch den Prozess zum Abrufen von Seitenrevisionen in OneNote mithilfe von Aspose.Note für Java.

## Voraussetzungen

Bevor wir beginnen, stellen Sie sicher, dass die folgenden Voraussetzungen erfüllt sind:

### 1. Java Development Kit (JDK)

Stellen Sie sicher, dass auf Ihrem System das Java Development Kit (JDK) installiert ist. Sie können JDK von der Oracle-Website herunterladen und installieren.

### 2. Aspose.Note für Java

Laden Sie Aspose.Note für Java herunter und installieren Sie es[Download-Link](https://releases.aspose.com/note/java/).

### 3. Beispiel für ein OneNote-Dokument

Bereiten Sie ein OneNote-Beispieldokument vor (`Sample1.one`), die die Seiten enthält, von denen Sie Revisionen abrufen möchten.

## Pakete importieren

Zunächst müssen Sie die erforderlichen Pakete aus Aspose.Note für Java importieren.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.LoadOptions;
import com.aspose.note.Page;
```

Lassen Sie uns nun das bereitgestellte Beispiel in mehrere Schritte unterteilen:

## Schritt 1: Dokumentenverzeichnis einrichten

Definieren Sie den Verzeichnispfad, in dem sich Ihr OneNote-Dokument befindet.

```java
String dataDir = "Your Document Directory";
```

## Schritt 2: OneNote-Dokument laden

 Laden Sie das OneNote-Dokument mit`LoadOptions` um den Ladeverlauf zu aktivieren.

```java
LoadOptions loadOptions = new LoadOptions();
loadOptions.setLoadHistory(true);
Document document = new Document(dataDir + "Sample1.one", loadOptions);
```

## Schritt 3: Erste Seite abrufen

Rufen Sie die erste Seite aus dem geladenen Dokument ab.

```java
Page firstPage = document.getFirstChild();
```

## Schritt 4: Seitenrevisionen durchlaufen

Durchlaufen Sie jede Seitenrevision und rufen Sie relevante Informationen wie den Zeitpunkt der letzten Änderung, den Zeitpunkt der Erstellung, den Titel, die Ebene und den Autor ab.

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

## Abschluss

In diesem Tutorial haben wir gelernt, wie man mit Aspose.Note für Java Seitenrevisionen in OneNote abruft. Wenn Sie diese Schritte befolgen, können Sie an Ihren OneNote-Seiten vorgenommene Änderungen effizient programmgesteuert nachverfolgen.

## FAQs

### F1: Kann ich Aspose.Note für Java verwenden, um Seitenrevisionen zu ändern?

A1: Nein, Aspose.Note für Java unterstützt derzeit das Abrufen von Seitenrevisionen, jedoch nicht deren Änderung.

### F2: Ist Aspose.Note für Java mit verschiedenen Versionen von OneNote-Dokumenten kompatibel?

A2: Ja, Aspose.Note für Java unterstützt verschiedene Versionen von OneNote-Dokumenten, sodass Sie nahtlos mit verschiedenen Dateiformaten arbeiten können.

### F3: Ist für die Nutzung von Aspose.Note für Java eine Lizenz erforderlich?

A3: Ja, Sie müssen eine Lizenz erwerben, um Aspose.Note für Java in kommerziellen Projekten verwenden zu können. Sie können jedoch auch eine temporäre Lizenz zu Evaluierungszwecken erwerben.

### F4: Kann ich Unterstützung suchen, wenn bei der Verwendung von Aspose.Note für Java Probleme auftreten?

 A4: Ja, Sie können Unterstützung im Aspose.Note-Forum suchen[Hier](https://forum.aspose.com/c/note/28).

### F5: Gibt es eine kostenlose Testversion für Aspose.Note für Java?

 A5: Ja, Sie können über die auf eine kostenlose Testversion von Aspose.Note für Java zugreifen[Webseite](https://releases.aspose.com/).