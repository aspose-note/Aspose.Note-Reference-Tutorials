---
title: Speichern Sie das Subsystem „Spezifizierte Schriftarten“ in OneNote
linktitle: Speichern Sie das Subsystem „Spezifizierte Schriftarten“ in OneNote
second_title: Aspose.Note Java API
description: Erfahren Sie, wie Sie OneNote-Dokumente mithilfe des angegebenen Schriftarten-Subsystems in Java mit Aspose.Note speichern. Sorgen Sie mühelos für eine konsistente Schriftdarstellung auf allen Plattformen.
type: docs
weight: 22
url: /de/java/onenote-document-saving/save-using-specified-fonts-subsystem/
---
## Einführung

Aspose.Note für Java bietet robuste Funktionen für die Arbeit mit OneNote-Dokumenten. Eine häufige Anforderung bei der Arbeit mit solchen Dokumenten besteht darin, sicherzustellen, dass die Schriftarten ordnungsgemäß beibehalten werden, insbesondere wenn das Dokument exportiert oder in anderen Formaten wie PDF gespeichert werden soll. Dieses Tutorial führt Sie durch den Prozess des Speicherns von OneNote-Dokumenten und gibt dabei das Schriftarten-Subsystem an, um eine konsistente und genaue Darstellung von Text auf verschiedenen Plattformen sicherzustellen.

## Voraussetzungen

Bevor wir uns mit dem Tutorial befassen, stellen Sie sicher, dass die folgenden Voraussetzungen erfüllt sind:

### 1. Java Development Kit (JDK)

 Stellen Sie sicher, dass auf Ihrem System das Java Development Kit (JDK) installiert ist. Sie können es herunterladen unter[Hier](https://www.oracle.com/java/technologies/javase-jdk15-downloads.html) falls Sie es noch nicht getan haben.

### 2. Aspose.Note für Java-Bibliothek

 Laden Sie die Aspose.Note für Java-Bibliothek herunter und richten Sie sie ein. Sie können es hier herunterladen[Webseite](https://releases.aspose.com/note/java/).

## Pakete importieren

Stellen Sie sicher, dass Sie die erforderlichen Pakete in Ihr Java-Projekt importieren:

```java
import com.aspose.note.Document;
import com.aspose.note.PdfSaveOptions;
import com.aspose.note.fonts.DocumentFontsSubsystem;
import java.io.FileInputStream;
import java.io.IOException;
import java.io.InputStream;
import java.nio.file.Paths;
```

Lassen Sie uns nun jedes Beispiel in mehrere Schritte unterteilen, um den Prozess besser zu verstehen.

## Schritt 1: Speichern Sie das Document Fonts Subsystem mit dem Standardschriftartnamen

In diesem Schritt wird gezeigt, wie Sie ein Dokument im PDF-Format unter Verwendung eines angegebenen Standardschriftnamens speichern.

```java
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontName() throws IOException
{
    // Laden Sie das Dokument in Aspose.Note.
    Document oneFile = new Document("missing-font.one");

    // Geben Sie die Standardschriftart an.
    PdfSaveOptions options = new PdfSaveOptions();
    options.setFontsSubsystem(DocumentFontsSubsystem.usingDefaultFont("Times New Roman"));

    // Speichern Sie das Dokument als PDF.
    oneFile.save("SaveUsingDocumentFontsSubsystemWithDefaultFontName_out.pdf", options);
}
```

In diesem Schritt:
- Das OneNote-Dokument wird mit Aspose.Note geladen.
- Als Standardschriftart ist „Times New Roman“ angegeben.
- Das Dokument wird im PDF-Format mit der angegebenen Schriftart gespeichert.

## Schritt 2: Speichern Sie das Document Fonts Subsystem mit der Standardschriftart aus der Datei

In diesem Schritt wird gezeigt, wie Sie ein Dokument im PDF-Format mit einer aus einer Datei geladenen Standardschriftart speichern.

```java
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontFromFile() throws IOException
{
    // Laden Sie das Dokument in Aspose.Note.
    Document oneFile = new Document("missing-font.one");

    // Geben Sie den Pfad zur Schriftartdatei an.
    String fontFile = "geo_1.ttf";

    // Geben Sie die Standardschriftart aus der Datei an.
    PdfSaveOptions options = new PdfSaveOptions();
    options.setFontsSubsystem(DocumentFontsSubsystem.usingDefaultFontFromFile(fontFile));

    // Speichern Sie das Dokument als PDF.
    oneFile.save("SaveUsingDocumentFontsSubsystemWithDefaultFontFromFile_out.pdf", options);
}
```

In diesem Schritt:
- Die Schriftartdatei „geo_1.ttf“ wird geladen.
- Die Standardschriftart wird aus der geladenen Schriftartendatei angegeben.
- Das Dokument wird im PDF-Format mit der angegebenen Schriftart gespeichert.

## Schritt 3: Speichern Sie das Document Fonts Subsystem mit der Standardschriftart aus Stream

In diesem Schritt wird gezeigt, wie Sie ein Dokument im PDF-Format mit einer aus einem Stream geladenen Standardschriftart speichern.

```java
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontFromStream() throws IOException
{
    // Laden Sie das Dokument in Aspose.Note.
    Document oneFile = new Document("missing-font.one");

    // Geben Sie den Pfad zur Schriftartdatei an.
    String fontFile = "geo_1.ttf";

    // Laden Sie die Schriftartdatei als Stream.
    InputStream stream = new FileInputStream(fontFile);

    try
    {
        // Geben Sie die Standardschriftart aus dem Stream an.
        PdfSaveOptions options = new PdfSaveOptions();
        options.setFontsSubsystem(DocumentFontsSubsystem.usingDefaultFontFromStream(stream));

        // Speichern Sie das Dokument als PDF.
        oneFile.save("SaveUsingDocumentFontsSubsystemWithDefaultFontFromStream_out.pdf", options);
    }
    catch (Exception e)
    {
        stream.close();
    }
}
```

In diesem Schritt:
- Die Schriftartdatei „geo_1.ttf“ wird als Stream geladen.
- Die Standardschriftart wird aus dem geladenen Stream angegeben.
- Das Dokument wird im PDF-Format mit der angegebenen Schriftart gespeichert.

## Abschluss

In diesem Tutorial haben wir gelernt, wie man OneNote-Dokumente mithilfe des angegebenen Schriftarten-Subsystems in Java mithilfe von Aspose.Note speichert. Wenn Sie diese Schritte befolgen, können Sie beim Exportieren oder Speichern Ihrer Dokumente eine konsistente Schriftartendarstellung auf verschiedenen Plattformen sicherstellen.

## FAQs

### F1: Kann ich für verschiedene Teile des Dokuments unterschiedliche Schriftarten angeben?

A1: Ja, Sie können mit Aspose.Note für Java unterschiedliche Schriftarten für verschiedene Teile des Dokuments angeben.

### F2: Ist Aspose.Note mit allen Versionen von OneNote kompatibel?

A2: Aspose.Note unterstützt verschiedene Versionen von OneNote und gewährleistet so die Kompatibilität in verschiedenen Umgebungen.

### F3: Wie kann ich beim Speichern von Dokumenten mit fehlenden Schriftarten umgehen?

A3: Aspose.Note bietet Optionen zum Festlegen von Standardschriftarten, um fehlende Schriftarten beim Speichern von Dokumenten effektiv zu behandeln.

### F4: Kann ich die Schrifteigenschaften wie Größe und Stil anpassen?

A4: Ja, Sie können Schrifteigenschaften wie Größe, Stil und Farbe mit Aspose.Note für Java anpassen.

### F5: Gibt es eine Testversion für Aspose.Note für Java?

A5: Ja, Sie können auf der Website eine kostenlose Testversion von Aspose.Note für Java herunterladen.