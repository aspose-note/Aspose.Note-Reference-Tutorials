---
title: Verwenden Sie den Algorithmus „Keep Solid Objects“ in OneNote – Aspose.Note
linktitle: Verwenden Sie den Algorithmus „Keep Solid Objects“ in OneNote – Aspose.Note
second_title: Aspose.Note Java API
description: Erfahren Sie, wie Sie feste Objekte in Ihren Aspose.Note-Dokumenten bei der Konvertierung in PDF mit dem Keep Solid Objects-Algorithmus in Java beibehalten.
type: docs
weight: 25
url: /de/java/onenote-document-saving/use-keep-solid-objects-algorithm/
---
## Einführung

In diesem Tutorial erfahren Sie, wie Sie den Keep Solid Objects-Algorithmus in Aspose.Note für Java verwenden. Dieser Algorithmus ist von unschätzbarem Wert für die Aufrechterhaltung der Integrität fester Objekte in Ihren Dokumenten bei der Konvertierung in das PDF-Format. Wir werden den Prozess Schritt für Schritt aufschlüsseln und so für Klarheit und Verständnis in jeder Phase sorgen.

## Voraussetzungen

Bevor wir beginnen, stellen Sie sicher, dass Sie über Folgendes verfügen:

1. Java Development Kit (JDK) auf Ihrem System installiert.
2.  Aspose.Note für Java-Bibliothek. Sie können es herunterladen unter[Hier](https://releases.aspose.com/note/java/).

## Pakete importieren

Importieren wir zunächst die notwendigen Pakete:

```java
import java.io.IOException;
import com.aspose.note.AlwaysSplitObjectsAlgorithm;
import com.aspose.note.Document;
import com.aspose.note.KeepPartAndCloneSolidObjectToNextPageAlgorithm;
import com.aspose.note.KeepSolidObjectsAlgorithm;
import com.aspose.note.PdfSaveOptions;
```

## Schritt 1: Laden Sie das Dokument

Laden Sie das Dokument mit dem folgenden Codeausschnitt in Aspose.Note:

```java
String dataDir = "Your Document Directory";
Document doc = new Document(dataDir + "Aspose.one");
```

## Schritt 2: Konfigurieren Sie die PDF-Speicheroptionen

Definieren Sie PdfSaveOptions und setzen Sie den PageSplittingAlgorithm auf KeepSolidObjectsAlgorithm:

```java
PdfSaveOptions pdfSaveOptions = new PdfSaveOptions();
pdfSaveOptions.setPageSplittingAlgorithm(new KeepSolidObjectsAlgorithm());
```

## Schritt 3: Höhenbegrenzung anpassen (optional)

Sie können die Höhenbegrenzung geklonter Teile bei Bedarf anpassen:

```java
float heightLimitOfClonedPart = 500;
pdfSaveOptions.setPageSplittingAlgorithm(new KeepSolidObjectsAlgorithm(heightLimitOfClonedPart));
```

## Schritt 4: Speichern Sie das Dokument

Speichern Sie abschließend das Dokument mit den angegebenen PDF-Speicheroptionen:

```java
String outputDir = "Your Output Directory";
String outputFile = outputDir + "UsingKeepSolidObjectsAlgorithm_out.pdf";
doc.save(outputFile);
```

## Abschluss

In diesem Tutorial haben wir gelernt, wie man den Keep Solid Objects-Algorithmus in Aspose.Note für Java verwendet. Dieser Algorithmus stellt sicher, dass feste Objekte in Ihren Dokumenten bei der Konvertierung in das PDF-Format erhalten bleiben und so die Dokumentintegrität gewahrt bleibt.

## FAQs

### F1: Kann ich die Höhenbegrenzung für geklonte Teile anpassen?

 A1: Ja, Sie können die Höhenbegrenzung geklonter Teile mithilfe von entsprechend Ihren Anforderungen anpassen`heightLimitOfClonedPart` Parameter.

### F2: Wo finde ich weitere Dokumentation?

 A2: Eine ausführliche Dokumentation finden Sie zu Aspose.Note für Java[Hier](https://reference.aspose.com/note/java/).

### F3: Gibt es eine kostenlose Testversion?

 A3: Ja, Sie können eine kostenlose Testversion von Aspose.Note für Java erhalten[Hier](https://releases.aspose.com/).

### F4: Wie kann ich Support erhalten, wenn ich auf Probleme stoße?

 A4: Sie können Unterstützung von der Aspose-Community erhalten[Hier](https://forum.aspose.com/c/note/28).

### F5: Wo kann ich eine Lizenz erwerben?

 A5: Sie können eine Lizenz für Aspose.Note für Java erwerben[Hier](https://purchase.aspose.com/buy).
