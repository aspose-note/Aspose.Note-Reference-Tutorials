---
title: Konvertieren Sie ein OneNote-Dokument in ein Bild – Java
linktitle: Konvertieren Sie ein OneNote-Dokument in ein Bild – Java
second_title: Aspose.Note Java API
description: Erfahren Sie, wie Sie OneNote mit Aspose.Note für Java in ein Bild konvertieren. Befolgen Sie die einfachen Schritte, laden Sie das Dokument, initialisieren Sie die Optionen und speichern Sie es als PNG.
type: docs
weight: 14
url: /de/java/onenote-document-loading/convert-to-image/
---
## Einführung

In diesem Tutorial führen wir Sie durch den Prozess der Verwendung von Aspose.Note für Java zum Konvertieren eines OneNote-Dokuments in ein Bild. Wir unterteilen jeden Schritt in leicht verständliche Anweisungen.

## Voraussetzungen

Bevor wir beginnen, stellen Sie sicher, dass Sie über Folgendes verfügen:

1. Java Development Kit (JDK) auf Ihrem System installiert.
2.  Aspose.Note für Java-Bibliothek. Sie können es herunterladen unter[Hier](https://releases.aspose.com/note/java/).

## Pakete importieren

Importieren Sie zunächst die erforderlichen Pakete in Ihren Java-Code:

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.SaveFormat;
```

Lassen Sie uns nun den bereitgestellten Beispielcode in mehrere Schritte aufteilen:

## Schritt 1: Dokumentenverzeichnis einrichten

Definieren Sie das Verzeichnis, in dem sich Ihr OneNote-Dokument befindet:

```java
String dataDir = "Your Document Directory";
```

 Ersetzen`"Your Document Directory"` mit dem Pfad zu Ihrem OneNote-Dokument.

## Schritt 2: Laden Sie das Dokument

Laden Sie das OneNote-Dokument in Aspose.Note:

```java
Document oneFile = new Document(dataDir + "Sample1.one");
```

 Sicherstellen`"Sample1.one"` entspricht dem Namen Ihrer OneNote-Dokumentdatei.

## Schritt 3: ImageSaveOptions initialisieren

 Initialisieren Sie die`ImageSaveOptions` Objekt zur Angabe des Speicherformats:

```java
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);
```

Hier speichern wir das Dokument als PNG-Bild. Bei Bedarf können Sie auch andere Formate wie JPEG oder BMP auswählen.

## Schritt 4: Speichern Sie das Dokument als Bild

Speichern Sie das geladene Dokument als Bild:

```java
oneFile.save(dataDir + "ConvertToImage_out.png", options);
```

Diese Zeile speichert das Dokument als PNG-Bild mit den angegebenen Optionen.

## Schritt 5: Bestätigung ausdrucken

Drucken Sie eine Nachricht aus, um zu bestätigen, dass die Datei gespeichert wurde:

```java
System.out.println("File saved: " + dataDir + "ConvertToImage_out.png");
```

Diese Zeile informiert Sie über die erfolgreiche Konvertierung und den Speicherort der gespeicherten Bilddatei.

## Abschluss

Wenn Sie die oben beschriebenen Schritte ausführen, können Sie mit Aspose.Note für Java mühelos ein OneNote-Dokument in ein Bild konvertieren. Dies ist eine einfache und effektive Möglichkeit, Dokumentkonvertierungen in Ihren Java-Anwendungen durchzuführen.

## FAQs

### F1: Kann ich mehrere OneNote-Dokumente auf einmal konvertieren?

A1: Ja, Sie können eine Liste von Dokumenten durchlaufen und den Konvertierungsvorgang für jedes Dokument durchführen.

### F2: Unterstützt Aspose.Note neben Bildern auch andere Ausgabeformate?

A2: Ja, Aspose.Note unterstützt verschiedene Ausgabeformate wie PDF-, HTML- und Microsoft Word-Formate.

### F3: Ist Aspose.Note mit allen Versionen von OneNote-Dateien kompatibel?

A3: Aspose.Note bietet Kompatibilität mit OneNote-Dateien, die in verschiedenen Versionen von Microsoft OneNote erstellt wurden.

### F4: Kann ich die Auflösung der Ausgabebilder anpassen?

A4: Ja, Sie können die Auflösung und andere Parameter mithilfe der in Aspose.Note verfügbaren Optionen anpassen.

### F5: Benötigt Aspose.Note eine Internetverbindung für die Dokumentkonvertierung?

A5: Nein, Aspose.Note funktioniert lokal, ohne dass eine Internetverbindung erforderlich ist.