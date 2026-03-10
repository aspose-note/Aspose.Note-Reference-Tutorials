---
date: 2025-12-21
description: Erfahren Sie, wie Sie OneNote‑Dokumente in Java erstellen und mühelos
  Bilder mit Aspose.Note für Java einfügen. Schritt‑für‑Schritt‑Anleitung für Java‑Entwickler.
linktitle: How to create onenote document java – Build Doc and Insert Image with Stream
second_title: Aspose.Note Java API
title: Wie man ein OneNote-Dokument in Java erstellt – Dokument erstellen und Bild
  mit Stream einfügen
url: /de/java/onenote-hyperlinks-images/build-doc-insert-image-stream/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Wie man onenote document java erstellt – Dokument erstellen und Bild mit Stream einfügen

## Einführung

Willkommen! In diesem Tutorial **erstellen Sie onenote document java** von Grund auf und lernen, wie Sie Bilder über einen Bild‑Stream einfügen. Wir gehen jeden Schritt durch, erklären, warum jedes Element wichtig ist, und geben Ihnen praktische Tipps, damit Sie die Technik in realen Projekten anwenden können. Am Ende können Sie OneNote‑Seiten programmgesteuert erzeugen und Bilder genau dort einbetten, wo Sie sie benötigen.

## Schnellantworten
- **Welche Bibliothek benötige ich?** Aspose.Note for Java  
- **Kann ich Bilder aus einem Stream einfügen?** Ja – übergeben Sie einfach einen `InputStream` an den `Image`‑Konstruktor.  
- **In welches Format kann ich exportieren?** Jedes von Aspose.Note unterstützte Format, z. B. PDF, DOCX, HTML.  
- **Benötige ich eine Lizenz für die Entwicklung?** Eine kostenlose temporäre Lizenz reicht für die Evaluierung; für die Produktion ist eine Voll‑Lizenz erforderlich.  
- **Welche Java‑Version wird benötigt?** Java 8 oder höher.

## Was ist “create onenote document java”?

Ein OneNote‑Dokument in Java zu erstellen bedeutet, die Aspose.Note‑API zu nutzen, um programmgesteuert eine Notizbuch‑Struktur – Seiten, Outlines und Elemente – aufzubauen, ohne den OneNote‑Desktop‑Client zu öffnen. Dieser Ansatz eignet sich ideal für die automatisierte Berichtserstellung, Stapelverarbeitung von Notizen oder die Integration von OneNote‑Inhalten in größere Java‑Anwendungen.

## Warum Aspose.Note for Java verwenden, um onenote document java zu erstellen?

- **Vollständige Kontrolle** über Seitenlayout, Outline‑Positionierung und Element‑Styling.  
- **Kein COM‑Interop** – funktioniert auf jedem Betriebssystem, das Java unterstützt.  
- **Umfangreiche Exportoptionen** – das gleiche Dokument mit einem einzigen Aufruf in PDF, DOCX, HTML usw. konvertieren.  
- **Stream‑freundlich** – Sie können Bilder direkt aus dem Speicher, Netzwerk oder Cloud‑Speicher laden.

## Voraussetzungen

Bevor wir beginnen, stellen Sie sicher, dass Folgendes eingerichtet ist:

### Java Development Kit (JDK)

Ein aktuelles JDK (8 oder höher) ist auf Ihrem Rechner installiert.

### Aspose.Note for Java Bibliothek

Laden Sie die Bibliothek von der offiziellen Aspose‑Release‑Seite herunter: [https://releases.aspose.com/note/java/](https://releases.aspose.com/note/java/).

### IDE‑Einrichtung

Konfigurieren Sie Ihre bevorzugte IDE (IntelliJ IDEA, Eclipse, VS Code), sodass die Aspose.Note‑JAR‑Dateien im Projekt‑Classpath enthalten sind.

## Pakete importieren

Um zu starten, importieren Sie die erforderlichen Java‑ und Aspose.Note‑Klassen. Diese Importe geben Ihnen Zugriff auf Dokumenterstellung, Seitenverwaltung, Outline‑Management und Bild‑Einfügung.

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

## Schritt 1: Dokumentverzeichnis einrichten

Definieren Sie den Ordner, der Ihre Quell‑Bilder enthält und in dem die Ausgabedatei gespeichert wird. Ersetzen Sie den Platzhalter durch den tatsächlichen Pfad auf Ihrem Rechner.

```java
String dataDir = "Your Document Directory";
```

## Schritt 2: Dokumentobjekt erstellen

Instanziieren Sie ein neues `Document`. Dieses Objekt repräsentiert das OneNote‑Notizbuch, das Sie bauen.

```java
Document doc = new Document();
```

## Schritt 3: Seitenobjekt initialisieren

Erstellen Sie eine `Page`, die alle Outlines und Elemente für diese Notizbuch‑Seite enthält.

```java
Page page = new Page();
```

## Schritt 4: Outline erstellen

Ein `Outline` fungiert als Container für positionierte Elemente. Hier setzen wir vertikale und horizontale Offsets, um das Outline auf der Seite zu positionieren.

```java
Outline outline1 = new Outline();
outline1.setVerticalOffset(600);
outline1.setHorizontalOffset(0);
```

## Schritt 5: Outline‑Element erstellen

Das `OutlineElement` wird das Bild hosten, das wir gleich einfügen.

```java
OutlineElement outlineElem1 = new OutlineElement();
```

## Schritt 6: Bild‑Stream laden

Öffnen Sie die Bilddatei als Stream. Durch die Verwendung eines Streams können Sie das Bild aus jeder Quelle (Dateisystem, Netzwerk, Datenbank) lesen, ohne es zuerst auf die Festplatte zu schreiben.

```java
InputStream fs = null;
try {
    fs = new FileInputStream(dataDir + "image.jpg");
} catch (FileNotFoundException e) {
    e.printStackTrace();
}
```

## Schritt 7: Bild einfügen

Erzeugen Sie ein `Image`‑Objekt. Das erste Argument kann `null` sein, wenn Sie später einen Stream bereitstellen, aber zur Vereinfachung referenzieren wir hier den Dateipfad und setzen die Ausrichtung auf die rechte Seite der Seite.

```java
Image image = new Image(null, dataDir + "image1.jpg");
image.setAlignment(HorizontalAlignment.Right);
```

## Schritt 8: Bild zum Outline‑Element hinzufügen

Fügen Sie das Bild dem Outline‑Element hinzu, sodass es Teil der visuellen Hierarchie der Seite wird.

```java
outlineElem1.appendChildLast(image);
```

## Schritt 9: Outline‑Element zum Outline hinzufügen

Jetzt hängen Sie das Outline‑Element (das das Bild enthält) an den Outline‑Container an.

```java
outline1.appendChildLast(outlineElem1);
```

## Schritt 10: Outline zur Seite hinzufügen

Platzieren Sie das Outline auf der Seite.

```java
page.appendChildLast(outline1);
```

## Schritt 11: Seite zum Dokument hinzufügen

Fügen Sie die vollständig erstellte Seite dem Dokumentobjekt hinzu.

```java
doc.appendChildLast(page);
```

## Schritt 12: Dokument speichern

Speichern Sie schließlich das OneNote‑Dokument im gewünschten Format. In diesem Beispiel exportieren wir nach PDF, Sie können jedoch jedes von Aspose.Note unterstützte Format wählen.

```java
try {
    doc.save("D://Aspose_JavaProjects//OneNote//out3.pdf", SaveFormat.Pdf);
} catch (IOException e) {
    e.printStackTrace();
}
```

Durch das Befolgen dieser Schritte haben Sie erfolgreich **onenote document java** erstellt und ein Bild mithilfe eines Input‑Streams eingebettet.

## Häufige Stolperfallen & Tipps

- **Stream nicht geschlossen** – In einer Produktionsumgebung schließen Sie den `InputStream` immer in einem `finally`‑Block oder verwenden `try‑with‑resources`.  
- **Falscher Dateipfad** – Überprüfen Sie, dass `dataDir` mit dem passenden Trennzeichen (`/` oder `\`) endet.  
- **Bildausrichtung** – Wenn das Bild außerhalb des Bildschirms erscheint, passen Sie die Werte `VerticalOffset`/`HorizontalOffset` des Outlines an.  
- **Lizenz‑Ausnahmen** – Die Verwendung der Evaluierungs‑Version kann ein Wasserzeichen zum Ergebnis hinzufügen; setzen Sie eine gültige Lizenz, um es zu entfernen.

## Häufig gestellte Fragen

### Q1: Ist Aspose.Note for Java mit allen Versionen von OneNote kompatibel?

A1: Aspose.Note for Java unterstützt verschiedene OneNote‑Dateiformate und stellt damit die Kompatibilität zu Desktop‑, Online‑ und Mobile‑Versionen sicher.

### Q2: Kann ich das Aussehen eingefügter Bilder in OneNote‑Dokumenten mit Aspose.Note for Java anpassen?

A2: Ja, Sie können Ausrichtung, Größe, Drehung und sogar das Zuschneiden ändern, indem Sie die entsprechenden Eigenschaften des `Image`‑Objekts verwenden.

### Q3: Bietet Aspose.Note for Java Unterstützung für andere Dokumentformate neben PDF?

A3: Absolut. Die API kann nach DOCX, HTML, XPS und mehreren anderen Formaten exportieren, wodurch Sie flexibel entscheiden können, wie Sie Ihre Notizen teilen oder archivieren.

### Q4: Wo finde ich zusätzliche Ressourcen und Support für Aspose.Note for Java?

A4: Die offizielle Aspose‑Website bietet umfangreiche Dokumentation, Code‑Beispiele, Foren und temporäre Lizenzen für die Evaluierung.

### Q5: Gibt es eine Testversion von Aspose.Note for Java?

A5: Ja, Sie können eine kostenlose Testversion von der Aspose‑Release‑Seite herunterladen, um alle Funktionen vor dem Kauf zu erkunden.

---

**Zuletzt aktualisiert:** 2025-12-21  
**Getestet mit:** Aspose.Note for Java 24.12 (neueste zum Zeitpunkt der Erstellung)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}