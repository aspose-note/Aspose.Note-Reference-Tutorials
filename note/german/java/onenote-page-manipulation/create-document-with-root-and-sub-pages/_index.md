---
title: Erstellen Sie ein Dokument mit Stamm- und Unterseiten in OneNote
linktitle: Erstellen Sie ein Dokument mit Stamm- und Unterseiten in OneNote
second_title: Aspose.Note Java API
description: Erstellen Sie mit Aspose.Note für Java ein Dokument mit Stamm- und Unterseiten in OneNote. Befolgen Sie die Schritt-für-Schritt-Anleitung, um Ihre Notizen effizient zu organisieren.
weight: 11
url: /de/java/onenote-page-manipulation/create-document-with-root-and-sub-pages/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Erstellen Sie ein Dokument mit Stamm- und Unterseiten in OneNote

## Einführung

In diesem Tutorial führen wir Sie durch den Prozess der Erstellung eines Dokuments mit Stamm- und Unterseiten in OneNote mithilfe von Aspose.Note für Java. Wenn Sie diese Schritte befolgen, können Sie Ihre OneNote-Dokumente effizient mit hierarchischer Struktur organisieren.

## Voraussetzungen

Bevor Sie beginnen, stellen Sie sicher, dass Sie die folgenden Voraussetzungen erfüllen:

1. Java Development Kit (JDK): Stellen Sie sicher, dass JDK auf Ihrem System installiert ist.
2. Aspose.Note für Java: Laden Sie Aspose.Note für Java von herunter und installieren Sie es[Webseite](https://purchase.aspose.com/buy).
3. Integrierte Entwicklungsumgebung (IDE): Wählen Sie eine Java-IDE wie IntelliJ IDEA, Eclipse oder NetBeans.

## Pakete importieren

Beginnen Sie mit dem Importieren der erforderlichen Pakete in Ihr Java-Projekt:

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.SaveFormat;
import com.aspose.note.ParagraphStyle;
```

## Schritt 1: Dokumentenverzeichnis einrichten

Definieren Sie das Verzeichnis, in dem Sie Ihr OneNote-Dokument speichern möchten:

```java
String dataDir = "Your Document Directory";
```

## Schritt 2: Dokumentobjekt erstellen

 Instanziieren Sie a`Document` Objekt:

```java
Document doc = new Document();
```

## Schritt 3: Seiten erstellen

Seitenobjekte initialisieren und deren Ebenen festlegen:

```java
Page page1 = new Page();
page1.setLevel((byte) 1);

Page page2 = new Page();
page2.setLevel((byte) 2);

Page page3 = new Page();
page3.setLevel((byte) 1);
```

## Schritt 4: Knoten zu Seiten hinzufügen

### Knoten zur ersten Seite hinzufügen

```java
Outline outline = new Outline();
OutlineElement outlineElem = new OutlineElement();
ParagraphStyle textStyle = new ParagraphStyle()
                                    .setFontColor(Color.black)
                                    .setFontName("David Transparent")
                                    .setFontSize(10);

RichText text = new RichText().append("First page.");
text.setParagraphStyle(textStyle);

outlineElem.appendChildLast(text);
outline.appendChildLast(outlineElem);
page1.appendChildLast(outline);
```

### Knoten zur zweiten Seite hinzufügen

```java
Outline outline2 = new Outline();
OutlineElement outlineElem2 = new OutlineElement();
ParagraphStyle textStyle2 = new ParagraphStyle()
                                    .setFontColor(Color.black)
                                    .setFontName("David Transparent")
                                    .setFontSize(10);

RichText text2 = new RichText().append("Second page.");
text2.setParagraphStyle(textStyle2);

outlineElem2.appendChildLast(text2);
outline2.appendChildLast(outlineElem2);
page2.appendChildLast(outline2);
```

### Knoten zur dritten Seite hinzufügen

```java
Outline outline3 = new Outline();
OutlineElement outlineElem3 = new OutlineElement();
ParagraphStyle textStyle3 = new ParagraphStyle()
                                    .setFontColor(Color.black)
                                    .setFontName("Broadway")
                                    .setFontSize(10);

RichText text3 = new RichText().append("Third page.");
text3.setParagraphStyle(textStyle3);

outlineElem3.appendChildLast(text3);
outline3.appendChildLast(outlineElem3);
page3.appendChildLast(outline3);
```

## Schritt 5: Fügen Sie dem Dokument Seiten hinzu

```java
doc.appendChildLast(page1);
doc.appendChildLast(page2);
doc.appendChildLast(page3);
```

## Schritt 6: Speichern Sie das Dokument

Speichern Sie das OneNote-Dokument:

```java
try {
    doc.save(dataDir + "GenerateRootAndSubLevelPagesInOneNote_out.bmp", SaveFormat.Bmp);
} catch (IOException e) {
    // Ausnahme behandeln
}
```

Glückwunsch! Sie haben mit Aspose.Note für Java erfolgreich ein Dokument mit Stamm- und Unterseiten in OneNote erstellt.

## Abschluss

Die Organisation Ihrer OneNote-Dokumente mit einer hierarchischen Struktur ist für eine bessere Verwaltung und Navigation unerlässlich. Mit Aspose.Note für Java können Sie effizient Dokumente mit Stamm- und Unterseiten erstellen und so ein klares und organisiertes Layout für Ihre Notizen bereitstellen.

## FAQs

### F1: Kann ich mit Aspose.Note für Java mehrere Ebenen von Unterseiten erstellen?

A1: Ja, Sie können mehrere Ebenen von Unterseiten erstellen, indem Sie für jede Seite die entsprechende Ebene festlegen.

### F2: Ist Aspose.Note für Java mit verschiedenen Java-IDEs kompatibel?

A2: Ja, Aspose.Note für Java ist mit gängigen Java-IDEs wie IntelliJ IDEA, Eclipse und NetBeans kompatibel.

### F3: Kann ich die Textformatierung in meinem OneNote-Dokument anpassen?

A3: Ja, Sie können Schriftart, Farbe, Größe und andere Formatierungsoptionen mithilfe der Rich-Text-Funktionen von Aspose.Note für Java anpassen.

### F4: Unterstützt Aspose.Note für Java das Speichern von Dokumenten in verschiedenen Formaten?

A4: Ja, Aspose.Note für Java unterstützt das Speichern von Dokumenten in verschiedenen Formaten, darunter BMP, PDF, PNG und mehr.

### F5: Gibt es eine Testversion für Aspose.Note für Java?

A5: Ja, Sie können eine kostenlose Testversion von Aspose.Note für Java von der Website herunterladen.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
