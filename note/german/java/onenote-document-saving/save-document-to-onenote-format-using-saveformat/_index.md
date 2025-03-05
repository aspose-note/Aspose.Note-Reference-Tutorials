---
title: Dokument mit SaveFormat – Aspose.Note in OneNote speichern
linktitle: Dokument mit SaveFormat – Aspose.Note in OneNote speichern
second_title: Aspose.Note Java API
description: Erfahren Sie, wie Sie Dokumente mit Aspose.Note für Java im OneNote-Format speichern. Befolgen Sie diese Schritt-für-Schritt-Anleitung für eine nahtlose Integration in Ihre Java-Anwendungen.
type: docs
weight: 12
url: /de/java/onenote-document-saving/save-document-to-onenote-format-using-saveformat/
---
## Einführung

Aspose.Note für Java ist eine leistungsstarke Bibliothek, die es Entwicklern ermöglicht, programmgesteuert mit Microsoft OneNote-Dateien zu arbeiten. Das Speichern eines Dokuments im OneNote-Format mit SaveFormat ist ein unkomplizierter Vorgang. In diesem Tutorial gehen wir die Schritte durch, die zum Ausführen dieser Aufgabe erforderlich sind.

## Voraussetzungen

Bevor wir beginnen, stellen Sie sicher, dass Sie über Folgendes verfügen:

1. Java Development Kit (JDK) auf Ihrem System installiert.
2.  Aspose.Note für Java-Bibliothek heruntergeladen. Sie können es von bekommen[Hier](https://releases.aspose.com/note/java/).
3. Grundlegendes Verständnis der Programmiersprache Java.

## Pakete importieren

 Zunächst müssen Sie die erforderlichen Pakete in Ihr Java-Projekt importieren. Dazu gehört auch der Import`com.aspose.note` Paket für die Arbeit mit Aspose.Note-Funktionen.

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.SaveFormat;
```

## Schritt 1: Dokumentenverzeichnis einrichten

Definieren Sie das Verzeichnis, in dem sich Ihr Dokument befindet und in dem Sie die Ausgabedatei speichern möchten.

```java
String dataDir = "Your Document Directory";
```

## Schritt 2: Dokument laden

 Laden Sie das Dokument mit in Ihre Java-Anwendung`Document` Klasse, bereitgestellt von Aspose.Note.

```java
Document document = new Document(dataDir + "Sample1.one");
```

## Schritt 3: Dokument im OneNote-Format speichern

Speichern Sie das geladene Dokument im OneNote-Format mit`save` -Methode und Angabe des gewünschten Ausgabedateiformats als`SaveFormat.One`.

```java
document.save(dataDir + "SaveDocToOneNoteFormatUsingSaveformat_out.one", SaveFormat.One);
```

## Abschluss

In diesem Tutorial haben wir gelernt, wie man ein Dokument mit SaveFormat in Aspose.Note für Java im OneNote-Format speichert. Wenn Sie diese einfachen Schritte befolgen, können Sie diese Funktionalität nahtlos in Ihre Java-Anwendungen integrieren.

## FAQs

### F1: Ist Aspose.Note für Java mit allen Versionen von Microsoft OneNote kompatibel?

A1: Aspose.Note für Java unterstützt verschiedene Versionen von Microsoft OneNote und gewährleistet so die Kompatibilität in verschiedenen Umgebungen.

### F2: Kann ich Aspose.Note für Java testen, bevor ich es kaufe?

 A2: Ja, Sie können eine kostenlose Testversion von Aspose.Note für Java herunterladen unter[Hier](https://releases.aspose.com/).

### F3: Wo finde ich Dokumentation für Aspose.Note für Java?

 A3: Eine ausführliche Dokumentation zu Aspose.Note für Java finden Sie hier[Hier](https://reference.aspose.com/note/java/).

### F4: Wie erhalte ich technischen Support für Aspose.Note für Java?

 A4: Für technische Hilfe und Support können Sie das Aspose.Note-Forum besuchen[Hier](https://forum.aspose.com/c/note/28).

### F5: Gibt es eine temporäre Lizenzoption für Aspose.Note für Java?

 A5: Ja, Sie können eine temporäre Lizenz für Aspose.Note für Java erhalten von[Hier](https://purchase.aspose.com/temporary-license/).