---
title: Fügen Sie mit Java ein Bild in ein OneNote-Dokument ein
linktitle: Fügen Sie mit Java ein Bild in ein OneNote-Dokument ein
second_title: Aspose.Note Java API
description: Erfahren Sie, wie Sie mithilfe der Aspose.Note für Java-Bibliothek Bilder in OneNote-Dokumente mithilfe von Java einfügen. Befolgen Sie unsere Schritt-für-Schritt-Anleitung für eine nahtlose Integration.
weight: 16
url: /de/java/onenote-hyperlinks-images/insert-image/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Fügen Sie mit Java ein Bild in ein OneNote-Dokument ein

## Einführung

In diesem Tutorial erfahren Sie, wie Sie mit Hilfe von Aspose.Note für Java ein Bild in ein OneNote-Dokument mit Java einfügen. Aspose.Note für Java ist eine leistungsstarke Bibliothek, die es Entwicklern ermöglicht, programmgesteuert mit Microsoft OneNote-Dateien zu arbeiten und verschiedene Vorgänge wie das Erstellen, Lesen und Bearbeiten von OneNote-Dokumenten zu ermöglichen.

## Voraussetzungen

Bevor wir beginnen, stellen Sie sicher, dass die folgenden Voraussetzungen erfüllt sind:

### 1. Java Development Kit (JDK)
Stellen Sie sicher, dass auf Ihrem System das Java Development Kit (JDK) installiert ist. Sie können JDK von der Oracle-Website herunterladen und installieren.

### 2. Aspose.Note für Java-Bibliothek
 Laden Sie die Aspose.Note für Java-Bibliothek herunter und richten Sie sie ein, indem Sie den Anweisungen folgen[Dokumentation](https://reference.aspose.com/note/java/).

## Pakete importieren

Beginnen Sie mit dem Importieren der erforderlichen Pakete in Ihr Java-Projekt. Diese Pakete umfassen die Aspose.Note-Bibliothek und andere erforderliche Abhängigkeiten.

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.HorizontalAlignment;
import com.aspose.note.Image;
import com.aspose.note.LoadOptions;
import com.aspose.note.Page;
import com.aspose.note.SaveFormat;
```

Lassen Sie uns den Prozess des Einfügens eines Bildes in ein OneNote-Dokument in mehrere Schritte unterteilen:

## Schritt 1: Laden Sie das OneNote-Dokument

Laden Sie zunächst das OneNote-Dokument, in das Sie das Bild einfügen möchten.

```java
LoadOptions options = new LoadOptions();
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Sample1.one", options);
```

## Schritt 2: Holen Sie sich die Seite

Rufen Sie die Seite im Dokument auf, auf der Sie das Bild einfügen möchten.

```java
Page page = oneFile.getFirstChild();
```

## Schritt 3: Laden Sie das Bild

Laden Sie das Bild, das Sie in das OneNote-Dokument einfügen möchten.

```java
Image image = new Image(oneFile, dataDir + "Input.jpg");
```

## Schritt 4: Bildattribute anpassen (optional)

Optional können Sie die Größe, Position und Ausrichtung des Bildes entsprechend Ihren Anforderungen anpassen.

```java
image.setWidth(100);
image.setHeight(100);
image.setVerticalOffset(400);
image.setHorizontalOffset(100);
image.setAlignment(HorizontalAlignment.Right);
```

## Schritt 5: Bild zur Seite hinzufügen

Fügen Sie das Bild zur Seite im OneNote-Dokument hinzu.

```java
page.appendChildLast(image);
```

## Schritt 6: Speichern Sie das Dokument

Speichern Sie das geänderte Dokument, einschließlich des eingefügten Bildes.

```java
try {
    oneFile.save(dataDir + "InsertanImage_out.pdf", SaveFormat.Pdf);
} catch (IOException e) {
    e.printStackTrace();
}
```

## Abschluss

In diesem Tutorial haben wir gelernt, wie man mit Java mithilfe der Aspose.Note für Java-Bibliothek ein Bild in ein OneNote-Dokument einfügt. Wenn Sie der Schritt-für-Schritt-Anleitung folgen, können Sie Bilder mühelos programmgesteuert in Ihre OneNote-Dokumente integrieren.

## FAQs

### F1: Kann ich mit dieser Methode mehrere Bilder in ein einzelnes OneNote-Dokument einfügen?

A1: Ja, Sie können mehrere Bilder in ein einzelnes OneNote-Dokument einfügen, indem Sie den in diesem Tutorial beschriebenen Vorgang für jedes Bild wiederholen.

### F2: Ist Aspose.Note für Java mit allen Versionen von OneNote kompatibel?

A2: Aspose.Note für Java unterstützt die Arbeit mit OneNote-Dateien, die in Microsoft OneNote 2010 und späteren Versionen erstellt wurden.

### F3: Kann ich Bilder in verschiedenen Formaten wie PNG oder GIF in ein OneNote-Dokument einfügen?

A3: Ja, Aspose.Note für Java unterstützt das Einfügen von Bildern in verschiedenen Formaten, einschließlich PNG, JPEG, GIF und mehr.

### F4: Gibt es eine Testversion von Aspose.Note für Java zu Testzwecken?

A4: Ja, Sie können zu Evaluierungszwecken eine kostenlose Testversion von Aspose.Note für Java von der Website herunterladen.

### F5: Wie erhalte ich technischen Support für Aspose.Note für Java?

 A5: Sie können technischen Support für Aspose.Note für Java erhalten, indem Sie die besuchen[Forum](https://forum.aspose.com/c/note/28) gewidmet Aspose.Note-Produkten.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
