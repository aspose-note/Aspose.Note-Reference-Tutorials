---
title: Legen Sie den Standard-Absatzstil in OneNote fest – Aspose.Note
linktitle: Legen Sie den Standard-Absatzstil in OneNote fest – Aspose.Note
second_title: Aspose.Note Java API
description: Erfahren Sie, wie Sie mit Aspose.Note für Java Standardabsatzstile in OneNote festlegen. Befolgen Sie unsere Schritt-für-Schritt-Anleitung für eine effiziente Textformatierung in Ihren Java-Anwendungen.
type: docs
weight: 11
url: /de/java/onenote-styles/set-default-paragraph-style/
---
## Einführung

Aspose.Note für Java bietet leistungsstarke Funktionen zum Bearbeiten der Textformatierung, einschließlich der Festlegung von Standardabsatzstilen. Dieses Tutorial führt Sie durch den Prozess zum Festlegen von Standardabsatzstilen in OneNote mithilfe von Aspose.Note.

## Voraussetzungen

Bevor Sie beginnen, stellen Sie sicher, dass Sie über Folgendes verfügen:

1. Java Development Kit (JDK): Stellen Sie sicher, dass JDK auf Ihrem System installiert ist.
2.  Aspose.Note für Java-Bibliothek: Laden Sie Aspose.Note für Java von herunter und installieren Sie es[Download-Seite](https://releases.aspose.com/note/java/).
3. Integrierte Entwicklungsumgebung (IDE): Zur Vereinfachung des Codierens sollte eine IDE installiert sein, z. B. Eclipse oder IntelliJ IDEA.

## Pakete importieren

Importieren Sie zunächst die erforderlichen Pakete, um mit dem Codieren zu beginnen:

```java
import com.aspose.note.*;

import java.awt.*;
import java.io.FileInputStream;
import java.io.IOException;
import java.nio.file.Paths;
import java.util.List;
```

Lassen Sie uns nun den Beispielcode in mehrere Schritte unterteilen:

## Schritt 1: Dokument, Seite und Gliederung initialisieren

```java
String dataDir = "Your Document Directory";
Document document = new Document();
Page page = new Page();
Outline outline = new Outline();
```

## Schritt 2: Erstellen Sie ein Gliederungselement

```java
OutlineElement outlineElem = new OutlineElement();
```

## Schritt 3: Definieren Sie den Standard-Absatzstil

```java
ParagraphStyle defaultStyle = new ParagraphStyle()
										.setFontName("Courier New")
										.setFontSize(20);
```

## Schritt 4: Erstellen Sie Rich Text mit Standardstil

```java
RichText text = new RichText()
					.append("DefaultParagraphFontAndSize")
					.append(System.lineSeparator())
					.append("OnlyDefaultParagraphFont", new TextStyle().setFontSize(14))
					.append(System.lineSeparator())
					.append("OnlyDefaultParagraphFontSize", new TextStyle().setFontName("Verdana"));
text.setParagraphStyle(defaultStyle);
```

## Schritt 5: Rich-Text an das Gliederungselement anhängen

```java
outlineElem.appendChildLast(text);
```

## Schritt 6: Gliederungselement an Gliederung anhängen

```java
outline.appendChildLast(outlineElem);
```

## Schritt 7: Gliederung an die Seite anhängen

```java
page.appendChildLast(outline);
```

## Schritt 8: Seite an Dokument anhängen

```java
document.appendChildLast(page);
```

## Schritt 9: Dokument speichern

```java
document.save(Paths.get(dataDir, "SetDefaultParagraphStyle.one").toString());
```

Dieser Code legt den Standardabsatzstil in OneNote mithilfe von Aspose.Note für Java fest.

## Abschluss

Das programmgesteuerte Festlegen von Standardabsatzstilen in OneNote kann mit Aspose.Note für Java effizient erreicht werden. Wenn Sie die in diesem Tutorial beschriebenen Schritte befolgen, können Sie diese Funktionalität nahtlos in Ihre Java-Anwendungen integrieren.

## FAQs

### F1: Kann ich den Standard-Absatzstil weiter anpassen?

A1: Ja, Sie können verschiedene Parameter wie Schriftart, Größe, Farbe und Ausrichtung an Ihre Anforderungen anpassen.

### F2: Unterstützt Aspose.Note andere Textformatierungsvorgänge?

A2: Absolut, Aspose.Note bietet umfassende Unterstützung für die Bearbeitung der Textformatierung, einschließlich Schriftarten, Aufzählungspunkten und Einrückungen.

### F3: Ist Aspose.Note mit allen Versionen von OneNote kompatibel?

A3: Aspose.Note ist für die Zusammenarbeit mit Microsoft OneNote-Dateien in verschiedenen Versionen konzipiert und gewährleistet so eine umfassende Kompatibilität.

### F4: Kann ich Aspose.Note in mein bestehendes Java-Projekt integrieren?

A4: Ja, Sie können Aspose.Note problemlos in Ihre Java-Projekte integrieren, indem Sie die erforderlichen Abhängigkeiten hinzufügen und die erforderlichen Pakete importieren.

### F5: Gibt es eine Testversion für Aspose.Note?

 A5: Ja, Sie können über die auf eine kostenlose Testversion von Aspose.Note zugreifen[Webseite](https://releases.aspose.com/).