---
title: Erstellen Sie ein Dokument und fügen Sie ein Bild in OneNote mit Java ein
linktitle: Erstellen Sie ein Dokument und fügen Sie ein Bild in OneNote mit Java ein
second_title: Aspose.Note Java API
description: Erfahren Sie, wie Sie mit Aspose.Note für Java OneNote-Dokumente erstellen und Bilder einfügen. Schritt-für-Schritt-Anleitung für eine nahtlose Integration.
type: docs
weight: 12
url: /de/java/onenote-hyperlinks-images/build-doc-insert-image/
---
## Einführung

In diesem Tutorial erfahren Sie, wie Sie mit Aspose.Note für Java OneNote-Dokumente erstellen und Bilder in diese einfügen. Aspose.Note ist eine leistungsstarke Java-API, die es Entwicklern ermöglicht, programmgesteuert mit Microsoft OneNote-Dateien zu arbeiten. Wir werden jeden Schritt im Detail aufschlüsseln, um Sie durch den Prozess zu führen.

## Voraussetzungen

Bevor wir beginnen, stellen Sie sicher, dass Sie die folgenden Voraussetzungen erfüllen:

1. Java Development Kit (JDK): Stellen Sie sicher, dass JDK auf Ihrem System installiert ist.
2.  Aspose.Note für Java-Bibliothek: Laden Sie die Aspose.Note für Java-Bibliothek von herunter und installieren Sie sie[Webseite](https://releases.aspose.com/note/java/).
3. IDE (Integrated Development Environment): Verwenden Sie zum Codieren eine beliebige Java-unterstützte IDE wie IntelliJ IDEA oder Eclipse.

## Pakete importieren

Beginnen Sie mit dem Importieren der erforderlichen Pakete in Ihren Java-Code:

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.HorizontalAlignment;
import com.aspose.note.Image;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.SaveFormat;
```

## Schritt 1: Richten Sie das Dokument ein

Erstellen Sie zunächst ein neues OneNote-Dokument und initialisieren Sie die erforderlichen Objekte:

```java
String dataDir = "Your Document Directory";
Document doc = new Document();
Page page = new Page();
```

## Schritt 2: Gliederung initialisieren

Richten Sie die Gliederung für das Dokument ein und legen Sie die Offset-Eigenschaften fest:

```java
Outline outline = new Outline();
outline.setVerticalOffset(0);
outline.setHorizontalOffset(0);
```

## Schritt 3: Bild hinzufügen

Laden Sie ein Bild und legen Sie seine Ausrichtung fest:

```java
Image image = new Image(null, dataDir + "Input.jpg");
image.setAlignment(HorizontalAlignment.Right);
```

## Schritt 4: Bild zum Gliederungselement hinzufügen

Hängen Sie das Bild an ein Gliederungselement an:

```java
OutlineElement outlineElem = new OutlineElement();
outlineElem.appendChildLast(image);
```

## Schritt 5: Gliederung und Seitenknoten hinzufügen

Fügen Sie die Gliederungs- und Seitenknoten zum Dokument hinzu:

```java
outline.appendChildLast(outlineElem);
page.appendChildLast(outline);
doc.appendChildLast(page);
```

## Schritt 6: Dokument speichern

Speichern Sie abschließend das OneNote-Dokument:

```java
try {
    doc.save(dataDir + "NewOneNotedocument_out", SaveFormat.Pdf);
} catch (IOException e) {
    e.printStackTrace();
}
```

## Abschluss

Glückwunsch! Sie haben erfolgreich gelernt, wie Sie mit Aspose.Note für Java OneNote-Dokumente erstellen und Bilder in diese einfügen. Wenn Sie diese Schritte befolgen, können Sie OneNote-Dateien in Ihren Java-Anwendungen effizient verwalten und bearbeiten.

## FAQs

### F1: Wo finde ich die Dokumentation für Aspose.Note für Java?

 A1: Sie können auf die Dokumentation zugreifen[Hier](https://reference.aspose.com/note/java/).

### F2: Wie lade ich Aspose.Note für Java herunter?

 A2: Sie können Aspose.Note für Java von herunterladen[Download-Seite](https://releases.aspose.com/note/java/).

### F3: Gibt es eine kostenlose Testversion für Aspose.Note für Java?

 A3: Ja, Sie können eine kostenlose Testversion von erhalten[Webseite](https://releases.aspose.com/).

### F4: Wo erhalte ich Unterstützung für Aspose.Note für Java?

 A4: Für Unterstützung besuchen Sie die[Aspose.Note-Forum](https://forum.aspose.com/c/note/28).

### F5: Kann ich eine temporäre Lizenz für Aspose.Note für Java erhalten?

 A5: Ja, Sie können eine temporäre Lizenz beantragen[Hier](https://purchase.aspose.com/temporary-license/).
