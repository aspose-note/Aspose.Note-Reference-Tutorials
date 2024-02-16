---
title: Extrahieren Sie Bilder aus OneNote-Dokumenten mit Java
linktitle: Extrahieren Sie Bilder aus OneNote-Dokumenten mit Java
second_title: Aspose.Note Java API
description: Erfahren Sie, wie Sie mit Java mit der Aspose.Note-Bibliothek Bilder aus OneNote-Dokumenten extrahieren. Befolgen Sie unsere Schritt-für-Schritt-Anleitung für eine nahtlose Bildextraktion.
type: docs
weight: 14
url: /de/java/onenote-hyperlinks-images/extract-images/
---
## Einführung

In diesem Tutorial führen wir Sie durch den Prozess des Extrahierens von Bildern aus einem OneNote-Dokument mithilfe von Java mithilfe der Aspose.Note-Bibliothek.

## Voraussetzungen

Bevor Sie beginnen, stellen Sie sicher, dass Sie über Folgendes verfügen:

1.  Java Development Kit (JDK): Stellen Sie sicher, dass Java auf Ihrem System installiert ist. Sie können es herunterladen und installieren[Webseite](https://www.oracle.com/java/technologies/javase-jdk15-downloads.html).

2.  Aspose.Note-Bibliothek: Laden Sie die Aspose.Note-Bibliothek herunter und fügen Sie sie in Ihr Java-Projekt ein. Sie erhalten es von der[Download-Link](https://releases.aspose.com/note/java/).

## Pakete importieren

Importieren Sie zunächst die erforderlichen Pakete:

```java
import java.io.IOException;
import java.nio.file.Files;
import java.nio.file.Paths;
import java.util.List;
import com.aspose.note.Document;
import com.aspose.note.Image;
```

## Schritt 1: Laden Sie das Dokument

Laden Sie zunächst das OneNote-Dokument mit Aspose.Note:

```java
String dataDir = "Your Document Directory";
Document doc = new Document(dataDir + "Sample1.one");
```

## Schritt 2: Holen Sie sich alle Bilder

Rufen Sie als Nächstes alle Bilder aus dem Dokument ab:

```java
List<Image> list = doc.getChildNodes(Image.class);
System.out.printf("Total Images: %s\n\n", list.size());
```

## Schritt 3: Bilder extrahieren

Gehen Sie die Liste der Bilder durch und speichern Sie jedes Bild in einer Datei:

```java
for (int i = 0; i < list.size(); i++) {
    Image image = list.get(i);
    String outputFile = "ExtractImages_out" + i + "_" + image.getFileName();
    byte[] buffer = image.getBytes();
    Files.write(Paths.get(dataDir + outputFile), buffer);
    System.out.printf("File saved: %s\n", dataDir);
}
```

## Abschluss

Das Extrahieren von Bildern aus einem OneNote-Dokument mit Java kann mit der Aspose.Note-Bibliothek nahtlos erfolgen. Wenn Sie die in diesem Tutorial beschriebenen Schritte befolgen, können Sie mühelos Bilder aus Ihren Dokumenten zur weiteren Verarbeitung oder Analyse abrufen.

## FAQs

### F1: Kann ich Bilder aus passwortgeschützten OneNote-Dokumenten extrahieren?

A1: Ja, Aspose.Note unterstützt auch das Extrahieren von Bildern aus passwortgeschützten Dokumenten.

### F2: Ist Aspose.Note mit verschiedenen Java-Versionen kompatibel?

A2: Aspose.Note ist mit verschiedenen Java-Versionen kompatibel und gewährleistet so Flexibilität für Entwickler.

### F3: Kann ich Bilder aus mehreren OneNote-Dokumenten in einer einzigen Ausführung extrahieren?

A3: Auf jeden Fall können Sie mit Aspose.Note mehrere Dokumente durchlaufen und Bilder aus jedem dieser Dokumente extrahieren.

### F4: Gibt es Größenbeschränkungen für die OneNote-Dokumente?

A4: Aspose.Note verarbeitet Dokumente unterschiedlicher Größe effizient und stellt sicher, dass es bei der Bildextraktion keine Einschränkungen bei der Dokumentgröße gibt.

### F5: Unterstützt Aspose.Note das Extrahieren anderer Arten von Inhalten außer Bildern?

A5: Ja, neben Bildern ermöglicht Aspose.Note auch das Extrahieren von Text, Anhängen und anderen Inhaltstypen aus OneNote-Dokumenten.