---
title: Arbeiten mit Seitenrevisionen in OneNote – Aspose.Note
linktitle: Arbeiten mit Seitenrevisionen in OneNote – Aspose.Note
second_title: Aspose.Note Java API
description: Erfahren Sie, wie Sie Seitenrevisionen in OneNote-Dokumenten mit Aspose.Note für Java verwalten. Bietet eine Schritt-für-Schritt-Anleitung für eine effektive Revisionsverfolgung und Zusammenarbeit.
type: docs
weight: 21
url: /de/java/onenote-page-manipulation/working-with-page-revisions/
---
## Einführung

OneNote ist ein leistungsstarkes Tool zum Organisieren und Verwalten von Notizen. Manchmal müssen Sie jedoch mit Revisionen arbeiten, um Änderungen zu verfolgen und effektiv zusammenzuarbeiten. Mit Aspose.Note für Java können Sie Seitenrevisionen in OneNote-Dokumenten einfach programmgesteuert verwalten. Dieses Tutorial führt Sie Schritt für Schritt durch den Prozess.

## Voraussetzungen

Bevor Sie beginnen, stellen Sie sicher, dass Sie über Folgendes verfügen:

### Java-Entwicklungsumgebung

Stellen Sie sicher, dass auf Ihrem System das Java Development Kit (JDK) installiert ist.

### Aspose.Note für Java-Bibliothek

Laden Sie die Aspose.Note für Java-Bibliothek von herunter und installieren Sie sie[Hier](https://releases.aspose.com/note/java/).

### OneNote-Dokument

Halten Sie zu Testzwecken ein OneNote-Beispieldokument bereit.

## Pakete importieren

Importieren Sie in Ihr Java-Projekt die erforderlichen Pakete, um mit Aspose.Note für Java zu arbeiten.

```java
import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.RevisionSummary;
import java.io.IOException;
import java.util.Calendar;
```

Lassen Sie uns das bereitgestellte Beispiel zum besseren Verständnis in mehrere Schritte unterteilen.

## Schritt 1: OneNote-Dokument laden

Laden Sie zunächst das OneNote-Dokument und rufen Sie die erste untergeordnete Seite ab.

```java
String dataDir = "Your Document Directory";
Document document = new Document(dataDir + "Sample1.one");
Page page = document.getFirstChild();
```

## Schritt 2: Lesen Sie die Zusammenfassung der Seitenrevision

Lesen Sie die Zusammenfassung der Inhaltsüberarbeitung für die Seite.

```java
RevisionSummary pageRevisionInfo = page.getPageContentRevisionSummary();
System.out.println(String.format("Author:\t%s\nModified:\t%s",
        pageRevisionInfo.getAuthorMostRecent(),
        pageRevisionInfo.getLastModifiedTime().toString()));
```

## Schritt 3: Aktualisieren Sie die Seitenrevisionszusammenfassung

Aktualisieren Sie die Zusammenfassung der Seitenrevision mit dem neuen Autor und dem Änderungsdatum.

```java
pageRevisionInfo.setAuthorMostRecent("New Author");
Calendar modifiedDate = Calendar.getInstance();
pageRevisionInfo.setLastModifiedTime(modifiedDate.getTime());
document.save(dataDir + "WorkingWithPageRevisions_out.one");
```

## Abschluss

Die programmgesteuerte Verwaltung von Seitenrevisionen in OneNote-Dokumenten kann mit Aspose.Note für Java vereinfacht werden. Wenn Sie die in diesem Tutorial beschriebenen Schritte befolgen, können Sie effektiv mit Seitenrevisionen arbeiten, um Änderungen zu verfolgen und nahtlos zusammenzuarbeiten.

## FAQs

### F1: Kann ich Aspose.Note für Java mit anderen Java-Bibliotheken verwenden?

A: Ja, Aspose.Note für Java kann zur Verbesserung der Funktionalität in andere Java-Bibliotheken integriert werden.

### F2: Unterstützt Aspose.Note für Java alle Versionen von OneNote-Dokumenten?

A: Aspose.Note für Java unterstützt verschiedene Versionen von OneNote-Dokumenten, einschließlich älterer Versionen.

### F3: Ist Aspose.Note für Java für Anwendungen auf Unternehmensebene geeignet?

A: Absolut, Aspose.Note für Java ist darauf ausgelegt, die Anforderungen von Unternehmensanwendungen mit robusten Funktionen und Skalierbarkeit zu erfüllen.

### F4: Kann ich Seitenrevisionen mit Aspose.Note für Java anpassen?

A: Ja, Sie können Seitenrevisionen mit Aspose.Note für Java an Ihre Anforderungen anpassen.

### F5: Wo erhalte ich Unterstützung für Aspose.Note für Java?

 A: Sie können Unterstützung für Aspose.Note für Java von der erhalten[Aspose.Note-Forum](https://forum.aspose.com/c/note/28).