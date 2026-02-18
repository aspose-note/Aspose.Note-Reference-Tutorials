---
date: 2026-02-18
description: Erfahren Sie, wie Sie ein OneNote‑Dokument erstellen, Rich‑Text formatieren
  und in Java mit Aspose.Note als PDF speichern. Schritt‑für‑Schritt‑Anleitung für
  nahtlose Automatisierung.
linktitle: Create OneNote document and save as PDF in Java
second_title: Aspose.Note Java API
title: OneNote-Dokument erstellen und in Java als PDF speichern
url: /de/java/onenote-document-manipulation/create-onenote-document-formatted-rich-text/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote-Dokument erstellen und als PDF in Java speichern

## Einleitung

Wenn Sie ein **OneNote-Dokument erstellen** und **OneNote als PDF speichern** möchten, während Sie die Rich‑Text‑Formatierung beibehalten, sind Sie hier genau richtig. In diesem Tutorial führen wir Sie durch das Erstellen eines OneNote-Dokuments, das Anwenden benutzerdefinierter Stile und das direkte Exportieren in PDF mit Aspose.Note für Java. Am Ende haben Sie ein wiederverwendbares Snippet, das Sie in jedes Java‑Projekt einbinden können, um hochwertige OneNote‑zu‑PDF‑Konvertierungen zu automatisieren.

## Schnelle Antworten
- **Worum geht es in diesem Tutorial?** Wie man ein OneNote-Dokument mit formatiertem Text erstellt und es als PDF speichert.  
- **Welche Bibliothek wird benötigt?** Aspose.Note für Java (von der offiziellen Website herunterladbar).  
- **Benötige ich eine Lizenz?** Eine temporäre Lizenz funktioniert für Tests; für die Produktion ist eine Voll‑Lizenz erforderlich.  
- **Welche IDE kann ich verwenden?** Jede Java‑IDE – IntelliJ IDEA, Eclipse oder NetBeans.  
- **Kann ich das Ausgabeformat ändern?** Ja, Aspose.Note unterstützt PDF, HTML, PNG und mehr.

## Was bedeutet „save onenote pdf“?
Das Speichern von OneNote als PDF bedeutet, die OneNote‑Seitenstruktur – einschließlich Text, Bildern und Formatierung – in eine statische PDF‑Datei zu konvertieren, die auf jeder Plattform angezeigt werden kann, ohne dass OneNote erforderlich ist.

## Warum Rich‑Text in Java formatieren?
Das direkte Anwenden von **format rich text** in Java ermöglicht es Ihnen, Dokumente zu erzeugen, die professionell aussehen und Ihren Markenrichtlinien entsprechen, ohne manuelle Nachbearbeitung.

## Voraussetzungen

1. **Java Development Kit (JDK)** – jede aktuelle Version (8 oder höher).  
2. **Aspose.Note for Java JAR** – laden Sie es von dem [download link](https://releases.aspose.com/note/java/) herunter.  
3. **IDE** – IntelliJ IDEA, Eclipse oder ein beliebiger Editor Ihrer Wahl.  

## Pakete importieren

Bevor wir beginnen, importieren Sie die erforderlichen Klassen in Ihre Java‑Datei:

```java
import java.awt.Color;
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.SaveFormat;
import com.aspose.note.TextStyle;
import com.aspose.note.ParagraphStyle;
import com.aspose.note.Title;
```

## Wie man ein OneNote-Dokument erstellt – Schritt‑für‑Schritt‑Anleitung

### Schritt 1: Dokument und Seite einrichten

Initialisieren Sie die `Document`‑ und `Page`‑Objekte, die den gesamten Inhalt enthalten werden:

```java
String dataDir = "Your Document Directory";
Document doc = new Document();
Page page = new Page();
```

### Schritt 2: Titel mit Formatierung erstellen

Fügen Sie ein Titel‑Element hinzu und wenden Sie einen **set paragraph style** an, um das Aussehen zu steuern:

```java
Title title = new Title();
ParagraphStyle defaultTextStyle = new ParagraphStyle()
                                        .setFontColor(Color.black)
                                        .setFontName("Arial")
                                        .setFontSize(10);

RichText titleText = new RichText().append("Title!");
titleText.setParagraphStyle(defaultTextStyle);
title.setTitleText(titleText);
```

### Schritt 3: Rich‑Text mit Formatierung erstellen

Hier erstellen wir Rich‑Text‑Inhalte mithilfe mehrerer `TextStyle`‑Objekte, um **rich text formatting** zu demonstrieren:

```java
Outline outline = new Outline();
OutlineElement outlineElem = new OutlineElement();

TextStyle textStyleForHelloWord = new TextStyle()
                                        .setFontColor(Color.red)
                                        .setFontName("Arial")
                                        .setFontSize(10);

TextStyle textStyleForOneNoteWord = new TextStyle()
                                        .setFontColor(Color.green)
                                        .setFontName("Calibri")
                                        .setFontSize(10)
                                        .setItalic(true);

TextStyle textStyleForTextWord = new TextStyle()
                                        .setFontColor(Color.blue)
                                        .setFontName("Arial")
                                        .setFontSize(15)
                                        .setBold(true)
                                        .setItalic(true);

RichText text = new RichText()
        .append("Hello", textStyleForHelloWord)
        .append(" OneNote", textStyleForOneNoteWord)
        .append(" text", textStyleForTextWord)
        .append("!", TextStyle.getDefault());
text.setParagraphStyle(defaultTextStyle);
```

### Schritt 4: Elemente zu Seite und Dokument hinzufügen

Kombinieren Sie den Titel und den Rich‑Text in der Seitenhierarchie:

```java
outlineElem.appendChildLast(text);
outline.appendChildLast(outlineElem);
page.setTitle(title);
page.appendChildLast(outline);
doc.appendChildLast(page);
```

### Schritt 5: Dokument speichern – onenote pdf exportieren

Exportieren Sie schließlich das OneNote‑Dokument als PDF‑Datei:

```java
doc.save(dataDir + "CreateOneNoteDocument_out.pdf", SaveFormat.Pdf);
```

## Häufige Probleme und Lösungen

| Problem | Lösung |
|-------|----------|
| **File not found** | Überprüfen Sie, ob `dataDir` auf einen bestehenden Ordner zeigt und Sie Schreibrechte haben. |
| **Missing fonts** | Stellen Sie sicher, dass die von Ihnen referenzierten Schriftarten (z. B. *Calibri*) auf dem Host‑Computer installiert sind. |
| **License not applied** | Laden Sie Ihre Aspose‑Lizenz, bevor Sie das `Document` erstellen, um Evaluations‑Wasserzeichen zu vermeiden. |

## Häufig gestellte Fragen

**Q: Kann ich die Schriftstile weiter anpassen?**  
A: Ja, Sie können zusätzliche Eigenschaften wie Unterstreichung, Durchstreichen und Textausrichtung über die Klassen `TextStyle` und `ParagraphStyle` anpassen.

**Q: Ist Aspose.Note für Java mit allen Java‑IDEs kompatibel?**  
A: Absolut. Solange die IDE die Standard‑Java‑Entwicklung unterstützt, können Sie das Aspose.Note‑JAR zum Klassenpfad des Projekts hinzufügen.

**Q: Kann ich diese Funktionalität in Web‑Anwendungen integrieren?**  
A: Ja, derselbe Code funktioniert in servlet‑basierten oder Spring‑Boot‑Anwendungen und ermöglicht die dynamische OneNote‑zu‑PDF‑Erzeugung auf der Serverseite.

**Q: Gibt es Lizenzanforderungen für die Verwendung von Aspose.Note für Java?**  
A: Für den Produktionseinsatz ist eine kommerzielle Lizenz erforderlich. Eine temporäre Lizenz steht für Evaluierung und Tests zur Verfügung.

**Q: Unterstützt Aspose.Note für Java weitere Dokumentformate neben OneNote?**  
A: Es unterstützt PDF, HTML, PNG, JPEG und mehrere andere Exportformate, wodurch Sie die Flexibilität erhalten, OneNote‑Seiten in das gewünschte Format zu konvertieren.

## Fazit

In diesem Leitfaden haben wir gezeigt, wie man ein **OneNote‑Dokument erstellt**, **Rich‑Text‑Formatierung** anwendet und **OneNote als PDF speichert** mit Aspose.Note für Java. Durch Befolgen der Schritt‑für‑Schritt‑Anleitung können Sie die Erstellung hochwertiger OneNote‑Dokumente automatisieren und sie in jedem Java‑basierten System in PDF konvertieren.

---

**Zuletzt aktualisiert:** 2026-02-18  
**Getestet mit:** Aspose.Note for Java 24.11 (latest at time of writing)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}