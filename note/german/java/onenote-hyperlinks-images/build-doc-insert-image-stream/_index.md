---
title: Erstellen Sie ein Dokument und fügen Sie ein Bild mit Stream in OneNote – Java ein
linktitle: Erstellen Sie ein Dokument und fügen Sie ein Bild mit Stream in OneNote – Java ein
second_title: Aspose.Note Java API
description: Erfahren Sie, wie Sie mit Aspose.Note für Java mühelos Bilder in OneNote-Dokumente integrieren. Schritt-für-Schritt-Anleitung für Java-Entwickler.
weight: 13
url: /de/java/onenote-hyperlinks-images/build-doc-insert-image-stream/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Erstellen Sie ein Dokument und fügen Sie ein Bild mit Stream in OneNote – Java ein

## Einführung

Willkommen zu unserem umfassenden Tutorial zur Verwendung von Aspose.Note für Java zum Erstellen von Dokumenten und Einfügen von Bildern mithilfe von Bildstreams in OneNote! In diesem Tutorial führen wir Sie Schritt für Schritt durch den Prozess und stellen sicher, dass Sie jede Phase genau verstehen. Am Ende können Sie Bilder mühelos mit Java in Ihre OneNote-Dokumente integrieren.

## Voraussetzungen

Bevor wir uns mit dem Tutorial befassen, stellen Sie sicher, dass die folgenden Voraussetzungen erfüllt sind:

### Java Development Kit (JDK)

Stellen Sie sicher, dass auf Ihrem System das Java Development Kit (JDK) installiert ist. Sie können es von der Oracle-Website herunterladen.

### Aspose.Note für Java-Bibliothek

 Laden Sie die Aspose.Note für Java-Bibliothek von der bereitgestellten Website herunter und installieren Sie sie[Verknüpfung](https://releases.aspose.com/note/java/).

### IDE-Setup

Richten Sie Ihre integrierte Entwicklungsumgebung (IDE) mit den erforderlichen Konfigurationen ein, um mit Java-Projekten zu arbeiten.

## Pakete importieren

Importieren Sie zunächst die erforderlichen Pakete in Ihr Java-Projekt. Diese Pakete stellen die erforderliche Funktionalität für die Arbeit mit OneNote-Dokumenten und -Bildern bereit.

```java
import java.io.FileInputStream;
import java.io.FileNotFoundException;
import java.io.IOException;
import java.io.InputStream;
import com.aspose.note.Document;
import com.aspose.note.HorizontalAlignment;
import com.aspose.note.Image;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.SaveFormat;
```

## Schritt 1: Dokumentenverzeichnis einrichten

 Definieren Sie das Verzeichnis, in dem sich Ihr Dokument und Ihre Bilder befinden. Ersetzen`"Your Document Directory"` mit dem Pfad zu Ihrem Verzeichnis.

```java
String dataDir = "Your Document Directory";
```

## Schritt 2: Dokumentobjekt erstellen

 Initialisieren Sie eine Instanz von`Document` Klasse, um mit der Arbeit mit Ihrem OneNote-Dokument zu beginnen.

```java
Document doc = new Document();
```

## Schritt 3: Seitenobjekt initialisieren

 Ein ... kreieren`Page` Objekt zur Darstellung der Seite im Dokument.

```java
Page page = new Page();
```

## Schritt 4: Gliederung erstellen

 Initialisieren Sie eine`Outline` Objekt zur Strukturierung des Inhalts innerhalb der Seite.

```java
Outline outline1 = new Outline();
outline1.setVerticalOffset(600);
outline1.setHorizontalOffset(0);
```

## Schritt 5: Gliederungselement erstellen

 Erstelle ein`OutlineElement` um das Bild zu halten und seine Position festzulegen.

```java
OutlineElement outlineElem1 = new OutlineElement();
```

## Schritt 6: Bildstream laden

 Laden Sie den Bildstream mit`FileInputStream` für das gewünschte Bild.

```java
InputStream fs = null;
try {
    fs = new FileInputStream(dataDir + "image.jpg");
} catch (FileNotFoundException e) {
    e.printStackTrace();
}
```

## Schritt 7: Bild einfügen

 Fügen Sie das Bild in das Dokument ein, indem Sie ein erstellen`Image` Objekt und legen Sie seine Ausrichtung fest.

```java
Image image = new Image(null, dataDir + "image1.jpg");
image.setAlignment(HorizontalAlignment.Right);
```

## Schritt 8: Bild an Gliederungselement anhängen

Hängen Sie das Bild an das Gliederungselement an.

```java
outlineElem1.appendChildLast(image);
```

## Schritt 9: Gliederungselement an Gliederung anhängen

Fügen Sie das Gliederungselement zur Gliederung hinzu.

```java
outline1.appendChildLast(outlineElem1);
```

## Schritt 10: Gliederung an die Seite anhängen

Fügen Sie die Gliederung zur Seite hinzu.

```java
page.appendChildLast(outline1);
```

## Schritt 11: Seite an Dokument anhängen

Hängen Sie abschließend die Seite an das Dokument an.

```java
doc.appendChildLast(page);
```

## Schritt 12: Dokument speichern

Speichern Sie das geänderte Dokument und geben Sie dabei das gewünschte Format an (z. B. PDF).

```java
try {
    doc.save("D://Aspose_JavaProjects//OneNote//out3.pdf", SaveFormat.Pdf);
} catch (IOException e) {
    e.printStackTrace();
}
```

Wenn Sie diese Schritte befolgen, können Sie mithilfe von Aspose.Note für Java mühelos Dokumente erstellen und Bilder mithilfe von Bildstreams in OneNote einfügen.

## Abschluss

Zusammenfassend lässt sich sagen, dass die Beherrschung der Integration von Bildern in Ihre OneNote-Dokumente mithilfe von Java Ihren Dokumenterstellungsprozess erheblich verbessern kann. Mit Aspose.Note für Java steht Ihnen ein leistungsstarkes Tool zur Verfügung, mit dem Sie diese Aufgabe nahtlos erledigen können.

## FAQs

### F1: Ist Aspose.Note für Java mit allen Versionen von OneNote kompatibel?

A1: Aspose.Note für Java unterstützt verschiedene Versionen von OneNote und gewährleistet so die Kompatibilität in verschiedenen Umgebungen.

### F2: Kann ich das Erscheinungsbild eingefügter Bilder in OneNote-Dokumenten mit Aspose.Note für Java anpassen?

A2: Ja, Sie können verschiedene Aspekte der eingefügten Bilder, wie Ausrichtung, Größe und Ausrichtung, an Ihre spezifischen Anforderungen anpassen.

### F3: Bietet Aspose.Note für Java Unterstützung für andere Dokumentformate außer PDF?

A3: Ja, Aspose.Note für Java unterstützt eine Vielzahl von Dokumentformaten, einschließlich DOCX, HTML und mehr, was Ihnen Flexibilität bei Ihren Dokumentenverwaltungsaufgaben bietet.

### F4: Wo finde ich zusätzliche Ressourcen und Unterstützung für Aspose.Note für Java?

A4: Über die bereitgestellten Links können Sie auf Dokumentation, Download-Links, Support-Foren und temporäre Lizenzen für Aspose.Note für Java zugreifen.

### F5: Gibt es eine Testversion für Aspose.Note für Java?

A5: Ja, Sie können eine kostenlose Testversion von Aspose.Note für Java erhalten, um dessen Funktionen und Fähigkeiten zu erkunden, bevor Sie eine Kaufentscheidung treffen.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
