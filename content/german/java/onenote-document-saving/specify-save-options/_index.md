---
title: Geben Sie Speicheroptionen in OneNote an – Aspose.Note
linktitle: Geben Sie Speicheroptionen in OneNote an – Aspose.Note
second_title: Aspose.Note Java API
description: Erfahren Sie, wie Sie mit Aspose.Note für Java Speicheroptionen in OneNote festlegen. Passen Sie Seitenindex, Anzahl und Komprimierungseinstellungen mühelos an.
type: docs
weight: 24
url: /de/java/onenote-document-saving/specify-save-options/
---
## Einführung

In diesem Tutorial erfahren Sie, wie Sie mit Aspose.Note für Java Speicheroptionen in OneNote festlegen. Aspose.Note ist eine leistungsstarke Java-Bibliothek, mit der Entwickler OneNote-Dokumente programmgesteuert erstellen, bearbeiten und konvertieren können. Mit Aspose.Note können Sie verschiedene Speicheroptionen einfach steuern, um die Ausgabe entsprechend Ihren Anforderungen anzupassen.

## Voraussetzungen

Bevor Sie beginnen, stellen Sie sicher, dass Sie die folgenden Voraussetzungen erfüllen:

1. Grundkenntnisse der Programmiersprache Java.
2. JDK (Java Development Kit) auf Ihrem System installiert.
3.  Aspose.Note für Java-Bibliothek installiert. Sie können es herunterladen unter[Hier](https://releases.aspose.com/note/java/).

## Pakete importieren

Importieren Sie zunächst die erforderlichen Pakete in Ihren Java-Code:

```java
import com.aspose.note.Document;
import com.aspose.note.PdfImageCompression;
import com.aspose.note.PdfSaveOptions;
import java.io.IOException;
```

Lassen Sie uns das Beispiel in mehrere Schritte unterteilen:

## Schritt 1: Laden Sie das OneNote-Dokument

```java
// Der Pfad zum Dokumentenverzeichnis.
String dataDir = "Your Document Directory";

// Laden Sie das Dokument in Aspose.Note.
Document doc = new Document(dataDir + "Aspose.one");
```

 In diesem Schritt geben wir den Pfad zum OneNote-Dokument an und laden es in das`Document` Objekt.

## Schritt 2: Initialisieren Sie das PdfSaveOptions-Objekt

```java
// Initialisieren Sie das PdfSaveOptions-Objekt
PdfSaveOptions opts = new PdfSaveOptions();
```

 Hier initialisieren wir a`PdfSaveOptions` Objekt, das verwendet wird, um die Optionen zum Speichern des Dokuments als PDF festzulegen.

## Schritt 3: Legen Sie den Seitenindex und die Anzahl fest

```java
// Seitenindex festlegen
opts.setPageIndex(2);

// Seitenanzahl festlegen
opts.setPageCount(3);
```

Diese Zeilen legen den Index und die Anzahl der zu speichernden Seiten fest. In diesem Beispiel speichern wir Seiten ab Index 2 und insgesamt 3 Seiten.

## Schritt 4: Legen Sie die Komprimierungseinstellungen fest

```java
// Geben Sie bei Bedarf die Komprimierung an
opts.setImageCompression(PdfImageCompression.Jpeg);
opts.setJpegQuality(90);
```

Hier legen wir die Bildkomprimierungseinstellungen für das PDF fest. Wir stellen die Komprimierung auf das JPEG-Format ein und geben die JPEG-Qualität mit 90 % an.

## Schritt 5: Speichern Sie das Dokument mit Optionen

```java
dataDir = dataDir + "Document.SaveWithOptions_out.pdf";
doc.save(dataDir, opts);
```

Abschließend speichern wir das Dokument mit den angegebenen Optionen. Das Ausgabe-PDF wird mit den angegebenen Optionen am angegebenen Speicherort gespeichert.

## Abschluss

In diesem Tutorial haben wir gelernt, wie Sie mit Aspose.Note für Java Speicheroptionen in OneNote festlegen. Durch das Anpassen der Speicheroptionen können Sie verschiedene Aspekte des Ausgabedokuments steuern, z. B. Seitenindex, Anzahl und Komprimierungseinstellungen.

## FAQs

### F1: Kann Aspose.Note große OneNote-Dokumente verarbeiten?

A1: Ja, Aspose.Note wurde für die effiziente Verarbeitung großer OneNote-Dokumente entwickelt.

### F2: Ist Aspose.Note mit den neuesten Java-Versionen kompatibel?

A2: Ja, Aspose.Note ist mit den neuesten Java-Versionen kompatibel.

### F3: Kann ich OneNote-Dokumente mit Aspose.Note in andere Formate konvertieren?

A3: Ja, Aspose.Note unterstützt die Konvertierung von OneNote-Dokumenten in verschiedene Formate wie PDF, DOCX und HTML.

### F4: Bietet Aspose.Note Unterstützung für die Ver- und Entschlüsselung von OneNote-Dokumenten?

A4: Ja, Aspose.Note bietet APIs für die Ver- und Entschlüsselung von OneNote-Dokumenten.

### F5: Ist Aspose.Note für die kommerzielle Nutzung geeignet?

A5: Ja, Aspose.Note kann durch den Erwerb einer Lizenz für kommerzielle Zwecke genutzt werden.