---
title: Erhalten Sie Bildinformationen von OneNote mit Java
linktitle: Erhalten Sie Bildinformationen von OneNote mit Java
second_title: Aspose.Note Java API
description: Extrahieren Sie Bildinformationen aus OneNote-Dokumenten in Java! Erhalten Sie Bildabmessungen, Dateinamen und mehr. Einfache Schritte und Codebeispiele enthalten. #OneNote #Java #Aspose
type: docs
weight: 15
url: /de/java/onenote-hyperlinks-images/get-image-info/
---
## Einführung

Im Bereich der Java-Entwicklung ist das Extrahieren von Informationen aus verschiedenen Dokumentformaten eine häufige Aufgabe. OneNote, eine beliebte Plattform zum Notieren, enthält neben Text häufig auch Bilder. Das programmgesteuerte Abrufen von Bildinformationen aus OneNote-Dateien mithilfe von Java kann die Arbeitsabläufe bei der Dokumentverarbeitung rationalisieren. In diesem Tutorial erfahren Sie, wie Sie mit Aspose.Note für Java Bilddetails aus OneNote-Dokumenten extrahieren.

## Voraussetzungen

Bevor wir uns mit der Implementierung befassen, stellen Sie sicher, dass die folgenden Voraussetzungen erfüllt sind:

### 1. Java Development Kit (JDK)

Stellen Sie sicher, dass auf Ihrem System das Java Development Kit (JDK) installiert ist. Sie können das neueste JDK von herunterladen und installieren[Oracle-Website](https://www.oracle.com/java/technologies/javase-jdk15-downloads.html).

### 2. Aspose.Note für Java-Bibliothek

 Laden Sie die Aspose.Note für Java-Bibliothek herunter und fügen Sie sie in Ihr Projekt ein. Die Bibliothek erhalten Sie über die[Download-Seite](https://releases.aspose.com/note/java/).

### 3. OneNote-Dokument

Bereiten Sie ein OneNote-Beispieldokument vor, das Bilder enthält. Dieses Dokument wird zum programmgesteuerten Extrahieren von Bildinformationen verwendet.

## Pakete importieren

Importieren Sie zunächst die erforderlichen Pakete aus Aspose.Note für Java:

```java
import java.io.IOException;
import java.util.List;
import com.aspose.note.Document;
import com.aspose.note.Image;
```

Teilen wir den obigen Code in Schritt-für-Schritt-Anleitungen auf:

## Schritt 1: Dokumentverzeichnis festlegen

```java
String dataDir = "Your Document Directory";
```

 Ersetzen`"Your Document Directory"` mit dem Pfad zu Ihrem OneNote-Dokument.

## Schritt 2: Laden Sie das Dokument

```java
Document doc = new Document(dataDir + "Sample1.one");
```

Laden Sie das OneNote-Dokument mit der Aspose.Note für Java-Bibliothek. Stellen Sie sicher, dass Sie den richtigen Pfad zu Ihrem Dokument angeben.

## Schritt 3: Holen Sie sich alle Bilder

```java
List<Image> list = doc.getChildNodes(Image.class);
```

Rufen Sie alle Bilder aus dem geladenen OneNote-Dokument ab.

## Schritt 4: Gesamtzahl der Bilder drucken

```java
System.out.printf("Total Images: %s\n\n", list.size());
```

Drucken Sie die Gesamtzahl der im Dokument gefundenen Bilder.

## Schritt 5: Bildinformationen durchsuchen und drucken

```java
for (Image image : list) {
    System.out.println("Width: " + image.getWidth());
    System.out.println("Height: " + image.getHeight());
    System.out.println("OriginalWidth: " + image.getOriginalWidth());
    System.out.println("OriginalHeight: " + image.getOriginalHeight());
    System.out.println("FileName: " + image.getFileName());
    System.out.println("LastModifiedTime: " + image.getLastModifiedTime());
    System.out.println();
}
```

Gehen Sie die Liste der Bilder durch und drucken Sie Details wie Breite, Höhe, Originalabmessungen, Dateiname und den Zeitpunkt der letzten Änderung für jedes Bild.

## Abschluss

Wenn Sie die in diesem Tutorial beschriebenen Schritte befolgen, können Sie mit Hilfe der Aspose.Note für Java-Bibliothek effektiv Bildinformationen aus OneNote-Dokumenten mithilfe von Java abrufen. Durch die Integration dieser Funktionalität in Ihre Anwendungen können Aufgaben im Zusammenhang mit der Dokumentenverarbeitung automatisiert und so die Effizienz und Produktivität gesteigert werden.

## FAQs

### F1: Kann Aspose.Note für Java neben OneNote auch andere Dokumentformate verarbeiten?

A1: Ja, Aspose.Note für Java unterstützt verschiedene Dokumentformate, darunter OneNote, PDF und Microsoft Word.

### F2: Ist Aspose.Note für Java sowohl für den persönlichen als auch für den kommerziellen Gebrauch geeignet?

A2: Ja, Sie können Aspose.Note für Java sowohl für persönliche als auch kommerzielle Zwecke nutzen.

### F3: Bietet Aspose.Note für Java technischen Support?

 A3: Ja, technischer Support ist über die Aspose-Foren unter verfügbar[Hier](https://forum.aspose.com/c/note/28).

### F4: Kann ich Aspose.Note für Java testen, bevor ich einen Kauf tätige?

 A4: Ja, Sie können eine kostenlose Testversion von Aspose.Note für Java unter erkunden[Aspose.Note für Java](https://releases.aspose.com/note/java/).

### F5: Wie kann ich eine temporäre Lizenz für Aspose.Note für Java erhalten?
 
 A5: Sie können eine temporäre Lizenz erwerben bei[Temporäre Lizenz/](https://purchase.aspose.com/temporary-license/).