---
date: 2025-12-09
description: Erfahren Sie, wie Sie OneNote in Java mit Aspose.Note for Java als PDF
  mit formatierter Rich‑Text‑Formatierung speichern. Folgen Sie unserer Schritt‑für‑Schritt‑Anleitung
  für nahtlose Dokumentenautomatisierung.
linktitle: Save OneNote as PDF with Formatted Rich Text in Java
second_title: Aspose.Note Java API
title: OneNote in Java als PDF mit formatierter Rich‑Text speichern
url: /de/java/onenote-document-manipulation/create-onenote-document-formatted-rich-text/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote als PDF mit formatierter Rich‑Text in Java speichern

## Einführung

Wenn Sie **OneNote als PDF** speichern möchten und dabei die Rich‑Text‑Formatierung beibehalten wollen, sind Sie hier genau richtig. In diesem Tutorial führen wir Sie durch das Erstellen eines OneNote‑Dokuments, das Anwenden benutzerdefinierter Stile und das direkte Exportieren nach PDF mit Aspose.Note für Java. Am Ende haben Sie einen wiederverwendbaren Code‑Snippet, den Sie in jedes Java‑Projekt einbinden können, um elegante OneNote‑zu‑PDF‑Konvertierungen zu automatisieren.

## Schnellantworten
- **Was lehrt dieses Tutorial?** Wie man ein OneNote‑Dokument mit formatiertem Text erstellt und als PDF speichert.  
- **Welche Bibliothek wird benötigt?** Aspose.Note für Java (downloadbar von der offiziellen Seite).  
- **Benötige ich eine Lizenz?** Eine temporäre Lizenz reicht für Tests; für den Produktionseinsatz ist eine Voll‑Lizenz erforderlich.  
- **Welche IDE kann ich verwenden?** Jede Java‑IDE – IntelliJ IDEA, Eclipse oder NetBeans.  
- **Kann ich das Ausgabeformat ändern?** Ja, Aspose.Note unterstützt PDF, HTML, PNG und weitere Formate.

## Was bedeutet „save onenote as pdf“?
OneNote als PDF zu speichern bedeutet, die OneNote‑Seitenstruktur – einschließlich Text, Bilder und Formatierung – in eine statische PDF‑Datei zu konvertieren, die auf jeder Plattform angezeigt werden kann, ohne dass OneNote erforderlich ist.

## Warum Rich‑Text‑Formatierung in Java?
Die direkte Anwendung von Rich‑Text‑Formatierung (Schriftarten, Farben, Stile) in Java ermöglicht es Ihnen, Dokumente zu erzeugen, die professionell aussehen und Ihren Markenrichtlinien entsprechen, ohne manuelle Nachbearbeitung.

## Voraussetzungen

1. **Java Development Kit (JDK)** – jede aktuelle Version (8 oder höher).  
2. **Aspose.Note für Java JAR** – herunterladen Sie es über den [download link](https://releases.aspose.com/note/java/).  
3. **IDE** – IntelliJ IDEA, Eclipse oder ein beliebiger Editor Ihrer.  

## Pakete importieren

Zunächst müssen Sie die erforderlichen Pakete in Ihr Java‑Projekt importieren. Fügen Sie die folgenden Import‑Anweisungen am Anfang Ihrer Java‑Datei ein:

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

## Schritt 1: Dokument und Seite einrichten

Beginnen wir mit der Initialisierung der `Document`‑ und `Page`‑Objekte:

```java
String dataDir = "Your Document Directory";
Document doc = new Document();
Page page = new Page();
```

## Schritt 2: Titel mit Formatierung erstellen

Erstellen wir nun einen Titel mit formatiertem Text:

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

## Schritt 3: Rich‑Text mit Formatierung erstellen

Als nächstes erzeugen wir Rich‑Text mit verschiedenen Formatierungsstilen:

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

## Schritt 4: Elemente zur Seite und zum Dokument hinzufügen

Jetzt fügen wir den Titel und den Rich‑Text zur Seite sowie zu den Outline‑Elementen hinzu:

```java
outlineElem.appendChildLast(text);
outline.appendChildLast(outlineElem);
page.setTitle(title);
page.appendChildLast(outline);
doc.appendChildLast(page);
```

## Schritt 5: Dokument speichern

Abschließend speichern wir das erstellte OneNote‑Dokument als PDF:

```java
doc.save(dataDir + "CreateOneNoteDocument_out.pdf", SaveFormat.Pdf);
```

## Häufige Probleme und Lösungen

| Problem | Lösung |
|---------|--------|
| **Datei nicht gefunden** | Stellen Sie sicher, dass `dataDir` auf einen existierenden Ordner verweist und Sie Schreibrechte besitzen. |
| **Schriftarten fehlen** | Vergewissern Sie sich, dass die referenzierten Schriftarten (z. B. *Calibri*) auf dem Host‑Computer installiert sind. |
| **Lizenz nicht angewendet** | Laden Sie Ihre Aspose‑Lizenz, bevor Sie das `Document` erstellen, um Wasserzeichen der Evaluierung zu vermeiden. |

## Häufig gestellte Fragen

**F: Kann ich die Schriftarten weiter anpassen?**  
A: Ja, Sie können zusätzliche Eigenschaften wie Unterstreichung, Durchstreichung und Textausrichtung über die Klassen `TextStyle` und `ParagraphStyle` einstellen.

**F: Ist Aspose.Note für Java mit allen Java‑IDEs kompatibel?**  
A: Absolut. Solange die IDE die Standard‑Java‑Entwicklung unterstützt, können Sie das Aspose.Note‑JAR dem Klassenpfad des Projekts hinzufügen.

**F: Kann ich diese Funktionalität in Web‑Anwendungen integrieren?**  
A: Ja, derselbe Code funktioniert in servlet‑basierten oder Spring‑Boot‑Anwendungen und ermöglicht die dynamische OneNote‑zu‑PDF‑Erstellung serverseitig.

**F: Gibt es Lizenzanforderungen für die Nutzung von Aspose.Note für Java?**  
A: Für den Produktionseinsatz ist eine kommerzielle Lizenz erforderlich. Eine temporäre Lizenz steht für Evaluierung und Tests zur Verfügung.

**F: Unterstützt Aspose.Note für Java weitere Dokumentformate neben OneNote?**  
A: Es unterstützt PDF, HTML, PNG, JPEG und mehrere andere Exportformate, sodass Sie OneNote‑Seiten in das von Ihnen benötigte Format konvertieren können.

## Fazit

In diesem Leitfaden haben wir gezeigt, wie man **OneNote als PDF** speichert und dabei Rich‑Text‑Formatierung mit Aspose.Note für Java anwendet. Durch Befolgen der Schritt‑für‑Schritt‑Anleitung können Sie die Erstellung hochwertiger OneNote‑Dokumente automatisieren und sie in jedem Java‑basierten System in PDF umwandeln.

---

**Zuletzt aktualisiert:** 2025-12-09  
**Getestet mit:** Aspose.Note für Java 24.11 (zum Zeitpunkt der Erstellung)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}