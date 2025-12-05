---
date: 2025-12-04
description: Lernen Sie, wie Sie Bilder aus OneNote‑Dateien extrahieren und OneNote
  in Text in Java mit Aspose.Note konvertieren. Schritt‑für‑Schritt‑Anleitung mit
  Codebeispielen.
language: de
linktitle: Extract Images from OneNote using Document Visitor - Java
second_title: Aspose.Note Java API
title: Bilder aus OneNote mit Document Visitor extrahieren – Java
url: /java/onenote-document-loading/extract-content-using-document-visitor/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Bilder aus OneNote mit Document Visitor extrahieren – Java

## Einführung

Aspose.Note for Java macht es einfach, **Bilder aus OneNote**-Notizbüchern zu extrahieren sowie die zugrunde liegende `.one`‑Datei in Java zu lesen. In diesem Tutorial führen wir Sie durch ein vollständiges, praxisnahes Beispiel, das zeigt, wie man eine OneNote‑Datei lädt, ihre Struktur mit einem benutzerdefinierten `DocumentVisitor` durchläuft und sowohl Bilder als auch Klartext herauszieht. Am Ende wissen Sie außerdem, wie man **OneNote in Text konvertiert**, falls Sie nur den Textinhalt benötigen.

## Schnelle Antworten
- **Welche Bibliothek benötige ich?** Aspose.Note for Java (Download-Link unten).  
- **Kann ich nur Bilder extrahieren?** Ja – implementieren Sie die Methode `VisitImageStart` in einem `DocumentVisitor`.  
- **Wie lese ich eine .one‑Datei in Java?** Verwenden Sie `new Document(path, new LoadOptions())`.  
- **Benötige ich eine Lizenz für die Produktion?** Eine kommerzielle Lizenz ist für den Einsatz außerhalb der Testphase erforderlich.  
- **Welche Java‑Version wird unterstützt?** JDK 8 oder höher.

## Voraussetzungen

Bevor Sie beginnen, stellen Sie sicher, dass Sie Folgendes haben:

1. Java Development Kit (JDK) 8 oder neuer installiert.  
2. Aspose.Note for Java‑Bibliothek heruntergeladen. Sie können sie **[hier](https://releases.aspose.com/note/java/)** herunterladen.  
3. Ein OneNote‑Dokument (`.one`‑Datei), aus dem Sie Bilder extrahieren oder das Sie in Text konvertieren möchten.

## Pakete importieren

Zuerst importieren Sie die erforderlichen Klassen aus der Aspose.Note‑API.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.DocumentVisitor;
import com.aspose.note.Image;
import com.aspose.note.LoadOptions;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.OutlineGroup;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.Title;
```

## Schritt 1: Einen benutzerdefinierten Document Visitor einrichten

Erstellen Sie eine Klasse, die `DocumentVisitor` erweitert. Diese Klasse wird für jeden Knoten im OneNote‑Dokument aufgerufen und ermöglicht Ihnen, **Bilder aus OneNote** zu extrahieren und optional Text zu sammeln.

```java
public class ExtractOneNoteContentUsingDocumentvisitor extends DocumentVisitor {
    
    final private StringBuilder mBuilder;
    final private boolean mIsSkipText;
    private int nodecount;

    public ExtractOneNoteContentUsingDocumentvisitor() {
        nodecount = 0;
        mIsSkipText = false;
        mBuilder = new StringBuilder();
    }
    
    // Other methods will be implemented here
}
```

## Schritt 2: Besucher‑Methoden implementieren

Fügen Sie Overrides für die Knotenarten hinzu, die Sie interessieren. Unten behandeln wir Rich‑Text, Bilder, Titel, Seiten, Gliederungen und Gliederungselemente. Die Methode `VisitImageStart` ist der Ort, an dem die Bildextraktion erfolgt.

```java
// Visitor methods for different types of nodes

public /* override */ void VisitRichTextStart(RichText run) {
    ++nodecount;
    AppendText(run.getText());
}

public /* override */ void VisitDocumentStart(Document document) {
    ++nodecount;
}

public /* override */ void VisitPageStart(Page page) {
    ++nodecount;
}

public /* override */ void VisitTitleStart(Title title) {
    ++nodecount;
}

public /* override */ void VisitImageStart(Image image) {
    ++nodecount;
    // Here you could save the image to disk or process it further
    System.out.println("Found image with size: " + image.getData().length + " bytes");
}

public /* override */ void VisitOutlineGroupStart(OutlineGroup outlineGroup) {
    ++nodecount;
}

public void VisitOutlineStart(Outline outline) {
    ++nodecount;
}

public void VisitOutlineElementStart(OutlineElement outlineElement) {
    ++nodecount;
}
```

### Warum diese Methoden implementieren?

- **Bilder aus OneNote extrahieren:** `VisitImageStart` gibt Ihnen direkten Zugriff auf die rohen Bildbytes.  
- **OneNote in Text konvertieren:** `VisitRichTextStart` sammelt den Textinhalt und ermöglicht eine einfache **OneNote‑zu‑Text‑Konvertierung**.  
- **.one‑Datei in Java lesen:** Das Visitor‑Muster abstrahiert die zugrunde liegende `.one`‑Dateistruktur, sodass Sie das Binärformat nicht selbst parsen müssen.

## Schritt 3: Den Visitor aus Ihrer Main‑Methode ausführen

Laden Sie die `.one`‑Datei, instanziieren Sie Ihren Visitor und starten Sie die Traversierung.

```java
public static void main(String[] args) throws IOException {
    // Open the document we want to convert.
    String dataDir = "Your Document Directory";
    Document doc = new Document(dataDir + "Sample1.one", new LoadOptions());
    
    // Create an object that inherits from the DocumentVisitor class.
    ExtractOneNoteContentUsingDocumentvisitor myConverter = new ExtractOneNoteContentUsingDocumentvisitor();
    
    // Accept the visitor to start the visiting process.
    doc.accept(myConverter);
    
    // Retrieve the result of the operation.
    System.out.println(myConverter.GetText());   // Text extracted from the notebook
    System.out.println(myConverter.NodeCount()); // Total nodes visited
}
```

## Häufige Anwendungsfälle

- **Automatisierte Berichterstellung:** Bilder und Text aus einem OneNote‑Besprechungsnotizbuch extrahieren, um eine PDF‑ oder HTML‑Zusammenfassung zu erstellen.  
- **Inhaltsmigration:** Legacy‑OneNote‑Archive in Klartextdateien konvertieren, um sie zu indizieren oder in Suchmaschinen zu importieren.  
- **Digitale Asset‑Extraktion:** Eingebettete Screenshots, Diagramme oder Fotos sammeln, um sie in anderen Anwendungen wiederzuverwenden.

## Fehlersuche & Tipps

- **Große Notizbücher:** Wenn Speicherprobleme auftreten, verarbeiten Sie Seiten einzeln, indem Sie `VisitPageStart` prüfen und Seiten‑Ressourcen nur bei Bedarf laden.  
- **Bildformate:** Das `Image`‑Objekt gibt rohe Bytes zurück; Sie müssen möglicherweise das Format (PNG, JPEG) vor dem Speichern erkennen.  
- **Lizenzfehler:** Stellen Sie sicher, dass Sie die Aspose‑Lizenz gesetzt haben (`License license = new License(); license.setLicense("Aspose.Note.Java.lic");`) bevor Sie das Dokument in der Produktion laden.

## Häufig gestellte Fragen

**F: Kann ich bestimmte Inhaltstypen aus dem OneNote‑Dokument extrahieren?**  
A: Ja – indem Sie nur die Visitor‑Methoden überschreiben, die Sie benötigen (z. B. `VisitImageStart` für Bilder, `VisitRichTextStart` für Text).

**F: Ist Aspose.Note for Java mit verschiedenen Versionen von OneNote‑Dokumenten kompatibel?**  
A: Absolut. Die Bibliothek unterstützt alle gängigen OneNote‑Dateiversionen, sodass Sie problemlos **.one‑Dateien in Java lesen** können, unabhängig von der ursprünglichen OneNote‑Version.

**F: Kann ich diesen Extraktionsprozess in meine Java‑Anwendung integrieren?**  
A: Ja. Das Visitor‑Muster funktioniert nahtlos in jeder Java‑Codebasis; fügen Sie einfach die Bibliotheks‑JAR hinzu und rufen Sie das oben gezeigte Beispiel auf.

**F: Bietet Aspose.Note for Java Unterstützung für die Verarbeitung komplexer OneNote‑Dokumente?**  
A: Ja. Verschachtelte Gliederungen, eingebettete Medien und benutzerdefinierte Daten werden alle über die Visitor‑API bereitgestellt.

**F: Gibt es ein Limit für die Größe des OneNote‑Dokuments, das verarbeitet werden kann?**  
A: Es gibt kein festes Limit, aber extrem große Notizbücher können mehr Heap‑Speicher benötigen; erwägen Sie, sie seitenweise zu verarbeiten.

**F: Wie konvertiere ich den extrahierten Text in eine Klartextdatei?**  
A: Nachdem `myConverter.GetText()` einen `String` zurückgibt, schreiben Sie ihn mit Standard‑Java‑I/O in eine Datei (`Files.write(Paths.get("output.txt"), text.getBytes());`).

---  

**Zuletzt aktualisiert:** 2025-12-04  
**Getestet mit:** Aspose.Note for Java 24.10  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}