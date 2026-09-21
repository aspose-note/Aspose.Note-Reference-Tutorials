---
date: 2026-07-29
description: Erfahren Sie, wie Sie einen Link onenote einbetten, OneNote als PDF speichern
  und Hyperlinks mit Java und Aspose.Note hinzufügen. Exportieren Sie OneNote mühelos
  als PDF.
keywords:
- embed link onenote
- export onenote to pdf
- generate pdf from onenote
- add hyperlink in onenote
- save onenote pdf
lastmod: 2026-07-29
linktitle: OneNote als PDF speichern und Hyperlink in OneNote mit Java hinzufügen
og_description: Link onenote einbetten und OneNote mit Java und Aspose.Note als PDF
  exportieren. Erfahren Sie Schritt für Schritt, wie Sie Hyperlinks hinzufügen und
  ein PDF erzeugen.
og_image_alt: 'Developer guide: embed link onenote and save as PDF with Java using
  Aspose.Note'
og_title: Link onenote einbetten – OneNote als PDF mit Java speichern
schemas:
- author: Aspose
  dateModified: '2026-07-29'
  description: Learn how to embed link onenote, save OneNote as PDF, and add hyperlinks
    using Java with Aspose.Note. Export OneNote to PDF effortlessly.
  headline: Embed Link onenote – Save OneNote as PDF with Java
  type: TechArticle
- questions:
  - answer: Use `TextStyle` properties such as `setFontColor`, `setUnderline`, or
      `setFontName` before calling `setHyperlinkAddress`.
    question: How can I customize the appearance of the hyperlink?
  - answer: Yes, Aspose.Note supports DOCX, XPS, HTML, and several other export formats.
    question: Can I save the document in formats other than PDF?
  - answer: Load the existing file with `new Document("input.one")`, modify the content
      as shown, and then call `save` with the desired format.
    question: What if I need to add a hyperlink to an existing OneNote file?
  - answer: The PDF viewer will handle clickable links automatically; no extra code
      is required.
    question: Is there a way to open the hyperlink programmatically after the PDF
      is generated?
  - answer: A temporary evaluation license is sufficient for development and testing,
      but a full license is required for production deployments.
    question: Do I need a license for development use?
  type: FAQPage
second_title: Aspose.Note Java API
tags:
- onenote pdf conversion
- Aspose.Note
- Java document processing
title: Link onenote einbetten – OneNote als PDF mit Java speichern
url: /de/java/onenote-hyperlinks-images/add-hyperlink/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote als PDF speichern und Hyperlink in OneNote mit Java hinzufügen

## Einleitung

Wenn Sie **embed link onenote** benötigen, während Sie ein Notizbuch in ein tragbares PDF umwandeln, sind Sie hier genau richtig. Dieses Tutorial führt Sie durch das Speichern von OneNote als PDF und das Einfügen anklickbarer Hyperlinks mit Java und der Aspose.Note-Bibliothek. Sie werden sehen, warum dieser Ansatz ideal für die Archivierung, das Teilen und die Automatisierung von Dokumentenpipelines ist.

## Schnelle Antworten
- **Kann ich OneNote mit Java als PDF speichern?** Ja, Aspose.Note for Java bietet einen einzelnen `save`‑Aufruf zum Erzeugen eines PDFs.
- **Wie bette ich einen Hyperlink ein?** Verwenden Sie `TextStyle.setHyperlinkAddress` auf einem `RichText`‑Segment.
- **Was sind die Voraussetzungen?** JDK 8+ und die Aspose.Note for Java‑Bibliothek.
- **Welche Ausgabeformate werden unterstützt?** PDF, DOCX, XPS und mehr.
- **Ist für die Produktion eine Lizenz erforderlich?** Ja, für den nicht‑Evaluations‑Einsatz ist eine kommerzielle Lizenz erforderlich.

## Was bedeutet „save onenote as pdf“?

Das Speichern eines OneNote‑Notizbuchs als PDF erzeugt eine schreibgeschützte, plattformübergreifende Version Ihrer Notizen, die jeder ohne die OneNote‑App öffnen kann. Dieses Format ist ideal für die Archivierung, das Drucken oder das Teilen mit Mitarbeitern, die OneNote nicht installiert haben, und bewahrt dabei das ursprüngliche Layout, Bilder und eingebettete Hyperlinks.

## Warum PDF aus OneNote mit Aspose.Note Java erzeugen?

Aspose.Note for Java kann **export onenote to pdf** mit 100 % Layout‑Treue, wobei bis zu 200 Seiten pro Dokument verarbeitet werden, ohne die gesamte Datei in den Speicher zu laden. Die Bibliothek verarbeitet über 30 verschiedene Inhaltstypen – einschließlich Bilder, Tabellen und 95 % der Hyperlink‑Stile – sodass Sie eine getreue Kopie des ursprünglichen Notizbuchs erhalten. Sie läuft zudem auf Windows, Linux und macOS und ermöglicht Stapelkonvertierungen in Cloud‑ oder On‑Premise‑Diensten.

## Voraussetzungen

Bevor wir beginnen, stellen Sie sicher, dass die folgenden Voraussetzungen auf Ihrem System installiert und eingerichtet sind:

### Java Development Kit (JDK)

Stellen Sie sicher, dass das Java Development Kit (JDK) auf Ihrem System installiert ist. Sie können das JDK von der [Oracle-Website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) herunterladen und installieren.

### Aspose.Note for Java Library

Laden Sie die Aspose.Note for Java-Bibliothek herunter und installieren Sie sie. Die Dokumentation und den Download‑Link finden Sie [hier](https://reference.aspose.com/note/java/).

## Pakete importieren

Um zu beginnen, importieren Sie die erforderlichen Pakete, die für die Arbeit mit Aspose.Note for Java nötig sind.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.TextStyle;
import com.aspose.note.ParagraphStyle;
import com.aspose.note.Title;
```

Nun zerlegen wir das bereitgestellte Beispiel in mehrere Schritte:

## Wie bette ich link onenote beim Speichern als PDF ein?

Laden Sie eine neue `Document`‑Instanz, bauen Sie die Seitenstruktur auf, definieren Sie einen rot gefärbten `TextStyle` für den Hyperlink und rufen Sie schließlich `document.save("output.pdf", SaveFormat.Pdf)` auf. Diese Reihenfolge erzeugt ein PDF, das einen voll funktionsfähigen Hyperlink enthält und alle ursprünglichen Formatierungen und Bilder bewahrt.

## Schritt 1: Dokumentstruktur einrichten

`Document` stellt ein OneNote‑Notizbuch in Aspose.Note dar.  
`Page` ist ein Container für Gliederungen und andere seitenbezogene Elemente.

```java
String dataDir = "Your Document Directory";
Document doc = new Document();
Page page = new Page();
Title title = new Title();
```

## Schritt 2: Standard‑Textstil definieren

`ParagraphStyle` definiert die Standardformatierung für Absätze, wie Ausrichtung, Abstand und Einrückung.

```java
ParagraphStyle defaultTextStyle = new ParagraphStyle()
                                            .setFontName("Arial")
                                            .setFontSize(10)
                                            .setFontColor(java.awt.Color.GRAY);
```

## Schritt 3: Titeltext festlegen

`Title` stellt das Seitentitel‑Element in einem OneNote‑Dokument dar.

```java
RichText titleText = new RichText().append("Title");
titleText.setParagraphStyle(defaultTextStyle);
title.setTitleText(titleText);
page.setTitle(title);
```

## Schritt 4: Gliederung und Gliederungselemente erstellen

`Outline` fungiert als Container für eine Hierarchie von Inhaltsblöcken.  
`OutlineElement` ist ein einzelnes Element innerhalb einer Gliederung, z. B. ein Absatz oder eine Tabelle.

```java
Outline outline = new Outline();
OutlineElement outlineElem = new OutlineElement();
```

## Schritt 5: Textstil für Hyperlink definieren

`TextStyle` steuert das visuelle Erscheinungsbild von Textabschnitten, einschließlich Schriftart, Farbe und Unterstreichung.

```java
TextStyle textStyleRed = new TextStyle()
                                    .setFontName("Arial")
                                    .setFontSize(10)
                                    .setFontColor(java.awt.Color.red);
```

## Schritt 6: Text mit Hyperlink hinzufügen

`RichText` stellt einen Lauf formatierten Textes innerhalb eines Absatzes dar. Das Festlegen einer Hyperlink‑Adresse macht den Text im exportierten PDF anklickbar.

```java
RichText text = new RichText()
                            .append("This is ", textStyleRed)
                            .append("hyperlink", new TextStyle().setHyperlinkAddress("https://www.google.com"))
                            .append(". This text is not a hyperlink.", TextStyle.getDefault());
text.setParagraphStyle(defaultTextStyle);
outlineElem.appendChildLast(text);
```

## Schritt 7: Gliederung zur Seite und Seite zum Dokument hinzufügen

Dieser Schritt fügt die zuvor erstellten Gliederungselemente zur Seite hinzu und fügt dann die Seite dem `Document`‑Objekt hinzu.

```java
outline.appendChildLast(outlineElem);
page.appendChildLast(outline);
doc.appendChildLast(page);
```

## Schritt 8: Dokument als PDF speichern

`SaveFormat.Pdf` weist Aspose.Note an, das Dokument im PDF‑Format zu exportieren.

```java
doc.save(dataDir + "AddHyperlink_out.pdf");
System.out.printf("File saved: %s\n", dataDir + "AddHyperlink_out.pdf");
```

## Fazit

Herzlichen Glückwunsch! Sie haben **OneNote erfolgreich als PDF gespeichert** und dem Dokument mit Java und der Aspose.Note‑Bibliothek einen Hyperlink hinzugefügt. Diese Möglichkeit erlaubt es Ihnen, **embed link onenote** und interaktive, teilbare PDFs direkt aus Ihrem OneNote‑Inhalt zu erstellen.

## Häufig gestellte Fragen

**F: Wie kann ich das Aussehen des Hyperlinks anpassen?**  
A: Verwenden Sie `TextStyle`‑Eigenschaften wie `setFontColor`, `setUnderline` oder `setFontName`, bevor Sie `setHyperlinkAddress` aufrufen.

**F: Kann ich das Dokument in anderen Formaten als PDF speichern?**  
A: Ja, Aspose.Note unterstützt DOCX, XPS, HTML und mehrere weitere Exportformate.

**F: Was, wenn ich einem bestehenden OneNote‑Datei einen Hyperlink hinzufügen muss?**  
A: Laden Sie die vorhandene Datei mit `new Document("input.one")`, ändern Sie den Inhalt wie gezeigt und rufen Sie anschließend `save` mit dem gewünschten Format auf.

**F: Gibt es eine Möglichkeit, den Hyperlink programmgesteuert zu öffnen, nachdem das PDF erzeugt wurde?**  
A: Der PDF‑Betrachter verarbeitet anklickbare Links automatisch; zusätzlicher Code ist nicht erforderlich.

**F: Benötige ich eine Lizenz für die Entwicklung?**  
A: Eine temporäre Evaluationslizenz reicht für Entwicklung und Tests aus, für den Produktionseinsatz ist jedoch eine Voll‑Lizenz erforderlich.

---

**Zuletzt aktualisiert:** 2026-07-29  
**Getestet mit:** Aspose.Note for Java 26.4  
**Autor:** Aspose

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.TextStyle;
import com.aspose.note.ParagraphStyle;
import com.aspose.note.Title;
```

## Verwandte Tutorials

- [Wie man OneNote mit Aspose.Note für Java als PDF speichert](/note/java/onenote-document-loading/load-save-format/)
- [OneNote mit Aspose.Note und PdfSaveOptions in PDF konvertieren](/note/java/onenote-document-loading/load-pdf-save-options/)
- [Hyperlink zu Bild in OneNote mit Java hinzufügen](/note/java/onenote-hyperlinks-images/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}