---
title: Konvertieren Sie ein Notizbuch in PDF mit den Optionen in OneNote – Aspose.Note
linktitle: Konvertieren Sie ein Notizbuch in PDF mit den Optionen in OneNote – Aspose.Note
second_title: Aspose.Note Java API
description: Passen Sie OneNote-Notizbücher ganz einfach an und exportieren Sie sie in PDF! Aspose.Note für Java übernimmt die schwere Arbeit. Schritt-für-Schritt-Anleitung inklusive! #OneNote #Java #Aspose
weight: 17
url: /de/java/onenote-notebook-operations/convert-notebook-to-pdf-with-options/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Konvertieren Sie ein Notizbuch in PDF mit den Optionen in OneNote – Aspose.Note

## Einführung

In diesem Tutorial tauchen wir in die Welt der Konvertierung von Notizbüchern in PDF mit anpassbaren Optionen mithilfe von Aspose.Note für Java ein. Aspose.Note ist eine leistungsstarke Java-API, die es Entwicklern ermöglicht, Microsoft OneNote-Dokumente programmgesteuert zu bearbeiten. Das Konvertieren von Notizbüchern in das PDF-Format ist eine häufige Anforderung in verschiedenen Anwendungen, und mit Aspose.Note wird diese Aufgabe rationalisiert und effizient.

## Voraussetzungen

Bevor wir beginnen, stellen Sie sicher, dass die folgenden Voraussetzungen erfüllt sind:

1. Java Development Kit (JDK): Stellen Sie sicher, dass JDK auf Ihrem System installiert ist.
2. Aspose.Note für Java: Laden Sie Aspose.Note für Java von herunter und installieren Sie es[Download-Link](https://releases.aspose.com/note/java/).
3. IDE (Integrated Development Environment): Wählen Sie Ihre bevorzugte IDE für die Java-Entwicklung. IntelliJ IDEA, Eclipse oder NetBeans sind beliebte Optionen.

## Pakete importieren

Zunächst müssen Sie die erforderlichen Pakete in Ihr Java-Projekt importieren. Diese Pakete stellen die Klassen und Methoden bereit, die für die Arbeit mit OneNote-Dokumenten erforderlich sind.

```java
import com.aspose.note.Notebook;
import java.io.IOException;
import com.aspose.note.KeepSolidObjectsAlgorithm;
import com.aspose.note.Notebook;
import com.aspose.note.NotebookPdfSaveOptions;
import com.aspose.note.PdfSaveOptions;
```

## Schritt 1: Laden Sie das OneNote-Notizbuch

Um ein Notizbuch in PDF zu konvertieren, müssen Sie zuerst das OneNote-Notizbuch laden. Stellen Sie sicher, dass der Pfad zur Notebook-Datei korrekt angegeben ist.

```java
String dataDir = "Your Document Directory";
// Laden Sie ein OneNote-Notizbuch
Notebook notebook = new Notebook(dataDir + "Notizbuch �ffnen.onetoc2");
```

## Schritt 2: Legen Sie die PDF-Speicheroptionen fest

Aspose.Note bietet verschiedene Optionen zum Anpassen der PDF-Ausgabe. Sie können Optionen wie Seitenaufteilungsalgorithmen, Kopf-/Fußzeileneinstellungen und mehr festlegen.

```java
// Geben Sie PDF-Speicheroptionen an
NotebookPdfSaveOptions notebookSaveOptions = new NotebookPdfSaveOptions();
PdfSaveOptions documentSaveOptions = notebookSaveOptions.getDocumentSaveOptions();
documentSaveOptions.setPageSplittingAlgorithm(new KeepSolidObjectsAlgorithm());
```

## Schritt 3: Speichern Sie das Notizbuch als PDF

Sobald Sie das Notizbuch geladen und die Speicheroptionen festgelegt haben, ist es an der Zeit, das Notizbuch als PDF-Datei zu speichern.

```java
dataDir = dataDir + "ExportNotebooktoPDFwithOptions_out.pdf";
// Speichern Sie das Notizbuch
notebook.save(dataDir, notebookSaveOptions);
```

## Abschluss

In diesem Tutorial haben wir untersucht, wie Sie OneNote-Notizbücher mit Aspose.Note für Java in das PDF-Format konvertieren. Wenn Sie diese einfachen Schritte befolgen, können Sie Dokumentkonvertierungen in Ihren Java-Anwendungen effizient durchführen.

---

## FAQs

### F1: Kann ich das Erscheinungsbild der PDF-Ausgabe anpassen?

A1: Ja, Aspose.Note bietet verschiedene Optionen zum Anpassen der PDF-Ausgabe, einschließlich Kopf-/Fußzeileneinstellungen, Seitenaufteilungsalgorithmen und mehr.

### F2: Ist Aspose.Note mit allen Versionen von OneNote kompatibel?

A2: Aspose.Note unterstützt Microsoft OneNote 2010 und spätere Versionen.

### F3: Bietet Aspose.Note eine kostenlose Testversion an?

 A3: Ja, Sie können eine kostenlose Testversion von Aspose.Note herunterladen unter[Hier](https://releases.aspose.com/).

### F4: Wo finde ich Dokumentation für Aspose.Note?

 A4: Sie finden eine umfassende Dokumentation für Aspose.Note[Hier](https://reference.aspose.com/note/java/).

### F5: Wie kann ich Unterstützung für Aspose.Note erhalten?

 A5: Für technische Unterstützung oder Fragen können Sie das Aspose.Note-Supportforum besuchen[Hier](https://forum.aspose.com/c/note/28).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
