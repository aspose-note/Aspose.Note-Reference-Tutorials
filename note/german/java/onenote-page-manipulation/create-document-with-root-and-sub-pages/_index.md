---
description: Erfahren Sie, wie Sie OneNote‑PDFs speichern und Unterseiten in OneNote
  mit Aspose.Note für Java hinzufügen. Folgen Sie dieser Schritt‑für‑Schritt‑Anleitung,
  um Ihre Notizen effizient zu organisieren.
linktitle: How to Save OneNote PDF and Add Sub Pages
second_title: Aspose.Note Java API
title: Wie man OneNote-PDF speichert und Unterseiten hinzufügt
url: /de/java/onenote-page-manipulation/create-document-with-root-and-sub-pages/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Wie man OneNote PDF speichert und Unterseiten hinzufügt

## Einführung

In diesem Tutorial erfahren Sie **wie man OneNote PDF speichert** und dabei ein Dokument erstellt, das sowohl Stamm‑ als auch Unterseiten enthält, mithilfe von Aspose.Note für Java. Die Organisation Ihrer OneNote-Notizbücher mit einer klaren Hierarchie erleichtert die Navigation, und die Möglichkeit, in PDF zu exportieren, stellt sicher, dass Sie Ihre Notizen in einem universell lesbaren Format teilen können. Wir zeigen Ihnen außerdem, wie Sie **Unterseiten im OneNote‑Stil hinzufügen** können, um mehrstufige Strukturen mühelos aufzubauen.

## Schnelle Antworten
- **Was bedeutet das primäre Schlüsselwort?** Es bezieht sich auf das Exportieren eines OneNote-Notizbuchs nach PDF mit Aspose.Note.  
- **Welche API wird verwendet?** Aspose.Note für Java.  
- **Kann ich hierarchische Seiten erstellen?** Ja – setzen Sie das Seitenlevel, um Stamm‑ und Unterseiten zu bauen.  
- **Benötige ich eine Lizenz?** Eine kostenlose Testversion ist verfügbar; für den Produktionseinsatz ist eine kommerzielle Lizenz erforderlich.  
- **Welche Ausgabeformate werden unterstützt?** BMP, PDF, PNG und mehr.

## Was bedeutet „how to save OneNote PDF“?
OneNote als PDF zu speichern konvertiert die Seiten des Notizbuchs in ein festes Layout‑Dokument, das Formatierung, Bilder und Hierarchie beibehält. Das ist ideal zum Teilen, Archivieren oder Drucken von Notizen.

## Warum Unterseiten in OneNote hinzufügen?
Das Hinzufügen von Unterseiten ermöglicht es, verwandte Inhalte unter einer übergeordneten Seite zu gruppieren, ähnlich einer Ordnerstruktur. Es verbessert die Organisation, beschleunigt die Suche und optimiert das Leseerlebnis, wenn das Notizbuch nach PDF exportiert wird.

## Voraussetzungen

Bevor Sie beginnen, stellen Sie sicher, dass Sie die folgenden Voraussetzungen erfüllen:

1. Java Development Kit (JDK): Stellen Sie sicher, dass das JDK auf Ihrem System installiert ist.  
2. Aspose.Note für Java: Laden Sie Aspose.Note für Java von der [Website](https://purchase.aspose.com/buy) herunter und installieren Sie es.  
3. Integrated Development Environment (IDE): Wählen Sie eine Java‑IDE wie IntelliJ IDEA, Eclipse oder NetBeans.

## Pakete importieren

Starten Sie, indem Sie die notwendigen Pakete in Ihrem Java‑Projekt importieren:

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

## Schritt 1: Dokumentverzeichnis einrichten

Definieren Sie das Verzeichnis, in dem Sie Ihr OneNote‑Dokument speichern möchten:

```java
String dataDir = "Your Document Directory";
```

## Schritt 2: Dokumentobjekt erstellen

Instanziieren Sie ein `Document`‑Objekt:

```java
Document doc = new Document();
```

## Schritt 3: Seiten erstellen

Initialisieren Sie Seitenobjekte und setzen Sie deren Level. Das Setzen des Levels bestimmt, ob eine Seite eine Stamm‑ oder eine Unterseite ist:

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

## Schritt 5: Seiten zum Dokument hinzufügen

```java
doc.appendChildLast(page1);
doc.appendChildLast(page2);
doc.appendChildLast(page3);
```

## Schritt 6: Dokument speichern

Speichern Sie das OneNote‑Dokument als PDF (oder BMP in diesem Beispiel). Durch Ändern von `SaveFormat` können Sie nach PDF exportieren, was die Anforderung „how to save OneNote PDF“ erfüllt:

```java
try {
    doc.save(dataDir + "GenerateRootAndSubLevelPagesInOneNote_out.bmp", SaveFormat.Bmp);
} catch (IOException e) {
    // Handle exception
}
```

> **Pro Tipp:** Um direkt nach PDF zu exportieren, ersetzen Sie `SaveFormat.Bmp` durch `SaveFormat.Pdf`.

Herzlichen Glückwunsch! Sie haben erfolgreich ein OneNote‑Dokument mit Stamm‑ und Unterseiten erstellt und **wie man OneNote PDF speichert** mit Aspose.Note für Java gelernt.

## Warum das wichtig ist

- **Hierarchische Organisation:** Stamm‑ und Unterseiten ermöglichen es, Ordnerstrukturen innerhalb von OneNote nachzuahmen.  
- **Nahtloser PDF‑Export:** Sobald die Struktur erstellt ist, bewahrt der Export nach PDF die Hierarchie, sodass das Enddokument leicht zu lesen und zu teilen ist.  
- **Automatisierung:** Der Code kann in größere Java‑Anwendungen integriert werden, wodurch die stapelweise Erstellung strukturierter Notizbücher ermöglicht wird.

## Häufige Fallstricke & wie man sie vermeidet

| Problem | Ursache | Lösung |
|---------|---------|--------|
| Seiten erscheinen auf derselben Ebene | Falscher `setLevel`‑Wert | Verwenden Sie `setLevel((byte) 1)` für Stammseiten und `setLevel((byte) 2)` (oder höher) für Unterseiten. |
| PDF‑Ausgabe ist leer | Fehlendes `SaveFormat.Pdf` oder falscher Dateipfad | Stellen Sie sicher, dass das Verzeichnis existiert, und verwenden Sie `SaveFormat.Pdf`. |
| Schriftart wird nicht angewendet | Falscher Schriftname oder Schriftart fehlt im System | Stellen Sie sicher, dass die Schriftart (z. B. „David Transparent“) auf dem Rechner, auf dem der Code läuft, installiert ist. |

## Häufig gestellte Fragen

**F: Kann ich mehrere Ebenen von Unterseiten mit Aspose.Note für Java erstellen?**  
A: Ja, Sie können tiefere Hierarchien erzeugen, indem Sie höhere Level‑Zahlen setzen (z. B. `setLevel((byte) 3)` für eine Unterseite der dritten Ebene).

**F: Ist Aspose.Note für Java mit verschiedenen Java‑IDEs kompatibel?**  
A: Absolut. Es funktioniert mit IntelliJ IDEA, Eclipse, NetBeans und jeder IDE, die Java‑Entwicklung unterstützt.

**F: Kann ich die Formatierung von Text in meinem OneNote‑Dokument anpassen?**  
A: Ja. Verwenden Sie `ParagraphStyle`, um Schriftname, Größe, Farbe und weitere Attribute für jedes `RichText`‑Element festzulegen.

**F: Unterstützt Aspose.Note für Java das Speichern von Dokumenten in anderen Formaten als BMP?**  
A: Ja. Unterstützte Formate umfassen PDF, PNG, JPEG, DOCX und mehr. Ändern Sie das `SaveFormat`‑Enum entsprechend.

**F: Gibt es eine Testversion von Aspose.Note für Java?**  
A: Ja, Sie können eine kostenlose Testversion von der Aspose‑Website herunterladen.

## Fazit

Die Organisation Ihrer OneNote‑Notizbücher mit einer klaren hierarchischen Struktur und das Exportieren als PDF machen Ihre Notizen zugänglicher und teilbarer. Mit den oben beschriebenen Schritten wissen Sie jetzt **wie man OneNote PDF speichert** und **Unterseiten im OneNote‑Stil** programmgesteuert mit Aspose.Note für Java erstellt.

---

**Last Updated:** 2026-01-07  
**Tested With:** Aspose.Note für Java 24.11 (latest)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}