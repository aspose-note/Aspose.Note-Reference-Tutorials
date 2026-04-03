---
date: 2026-04-03
description: Erfahren Sie, wie Sie Hyperlinks in Aspose.Note‑Dokumenten mit Aspose.Note
  für .NET hinzufügen, das Aussehen von Hyperlinks anpassen und mehrere Hyperlinks
  einfügen, um reichhaltigere OneNote‑Dateien zu erstellen.
keywords:
- how to add hyperlink
- insert multiple hyperlinks
- add hyperlink to onenote
- customize hyperlink appearance
- generate one file hyperlink
linktitle: Wie man einen Hyperlink in Aspose.Note‑Dokumenten hinzufügt
second_title: Aspose.Note .NET API
title: Wie man Hyperlinks in Aspose.Note‑Dokumenten hinzufügt
url: /de/net/hyperlinks/add-hyperlinks/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Wie man Hyperlinks in Aspose.Note-Dokumenten hinzufügt

## Einführung

In diesem Tutorial erfahren Sie **wie man Hyperlinks** zu Text in Aspose.Note-Dokumenten mit der .NET API hinzufügt. Das Hinzufügen eines Hyperlinks verwandelt statische Notizen in interaktiven, anklickbaren Inhalt – ideal zum Verlinken zu Webressourcen, internen Abschnitten oder externen Dateien. Wir gehen jeden Schritt durch, zeigen Ihnen, wie Sie **das Aussehen von Hyperlinks anpassen** und erklären, wie Sie **mehrere Hyperlinks einfügen** können, wenn Sie reichhaltigere OneNote-Seiten benötigen.

## Schnelle Antworten
- **Was ist die primäre Klasse zum Erstellen einer OneNote-Datei?** `Document` von Aspose.Note.
- **Welche Eigenschaft lässt Text wie einen Hyperlink funktionieren?** `IsHyperlink = true` bei `TextStyle`.
- **Kann ich zu externen Websites verlinken?** Ja, setzen Sie `HyperlinkAddress` auf eine URL wie `https://www.google.com`.
- **Benötige ich eine Lizenz für den Produktionseinsatz?** Eine gültige Aspose.Note-Lizenz ist für Nicht‑Evaluierungs‑Builds erforderlich.
- **Welche .NET-Versionen werden unterstützt?** .NET Framework 4.6+, .NET Core 3.1+, .NET 5/6+.

## Was bedeutet „wie man Hyperlinks hinzufügt“ in Aspose.Note?
Ein Hyperlink bedeutet, dass einer Textstelle eine URL zugeordnet wird, sodass beim Klicken innerhalb von OneNote die verlinkte Ressource in einem Browser oder einer anderen Anwendung geöffnet wird. Aspose.Note stellt das Flag `TextStyle.IsHyperlink` und die Eigenschaft `HyperlinkAddress` bereit, um dies programmgesteuert zu ermöglichen.

## Warum Hyperlinks zu OneNote-Dokumenten hinzufügen?
- **Verbesserte Navigation:** Direkt zu verwandten Webseiten oder Abschnitten springen.
- **Erweiterte Dokumentation:** Referenzen, Tutorials oder Quelldateien bereitstellen, ohne die Notiz zu verlassen.
- **Professionelles Aussehen:** Anpasbare Farben und Stile lassen Hyperlinks sich in das Design Ihres Dokuments einfügen.

## Voraussetzungen

1. Grundkenntnisse in C# und Visual Studio.
2. Aspose.Note for .NET library installed – download it from [here](https://releases.aspose.com/note/net/).
3. Verständnis der Aspose.Note-Dokumentstruktur (Seiten, Gliederungen, Rich Text).

## Namespaces importieren

Zuerst importieren Sie die Namespaces, die Ihnen Zugriff auf die Kernklassen von Aspose.Note und grundlegende .NET-Typen geben.

```csharp
using System;
using System.Drawing;
```

## Schritt‑für‑Schritt-Anleitung

### Schritt 1: Ein neues Document-Objekt erstellen

Instanziieren Sie ein `Document`, das alle Ihre Seiten und Inhalte enthält.

```csharp
Document doc = new Document();
```

### Schritt 2: Textstile definieren (einschließlich Hyperlink-Stil)

Erstellen Sie zwei `TextStyle`-Objekte – eines für normalen Text und eines für den Hyperlink.  
Hier passen wir außerdem **das Aussehen des Hyperlinks** an, indem wir die Schriftfarbe festlegen.

```csharp
TextStyle textStyleRed = new TextStyle
{
    FontColor = Color.Red,
    FontName = "Arial",
    FontSize = 10,
};

TextStyle textStyleHyperlink = new TextStyle
{
    IsHyperlink = true,
    HyperlinkAddress = "www.google.com"
};
```

> **Profi‑Tipp:** Um **mehrere Hyperlinks** einzufügen, definieren Sie zusätzliche `TextStyle`-Objekte mit unterschiedlichen `HyperlinkAddress`-Werten und verwenden Sie sie in späteren `RichText`-Segmenten wieder.

### Schritt 3: RichText-Objekte erstellen

Erstellen Sie den Absatz, der normalen Text und den Hyperlink kombiniert. Die Methode `Append` ermöglicht das Verketten von formatierten Fragmenten.

```csharp
RichText text = new RichText() { ParagraphStyle = ParagraphStyle.Default }
                    .Append("This is ", textStyleRed)
                    .Append("hyperlink", textStyleHyperlink)
                    .Append(". This text is not a hyperlink.", TextStyle.Default);
```

### Schritt 4: Outline und Outline-Element erstellen

Outlines fungieren als Container für visuelle Elemente auf einer Seite. Größe und Position nach Bedarf festlegen.

```csharp
Outline outline = new Outline()
{
    MaxWidth = 200,
    MaxHeight = 200,
    VerticalOffset = 100,
    HorizontalOffset = 100
};

OutlineElement outlineElem = new OutlineElement();
outlineElem.AppendChildLast(text);
```

### Schritt 5: Elemente zu einer Seite hinzufügen

Jede OneNote-Datei besteht aus Seiten. Wir erstellen ein `Title` und eine `Page` und fügen dann die Outline hinzu.

```csharp
Title title = new Title() { TitleText = titleText };
Page page = new Note.Page() { Title = title };

page.AppendChildLast(outline);
doc.AppendChildLast(page);
```

### Schritt 6: Dokument speichern

Wählen Sie einen Ordner, erstellen Sie den vollständigen Dateinamen und rufen Sie `Save` auf. Die Ausgabedatei wird eine gültige OneNote `.one`-Datei sein, die Ihren Hyperlink enthält.

```csharp
string dataDir = "Your Document Directory";
string outputFilePath = Path.Combine(dataDir, "AddHyperlink_out.one");
doc.Save(outputFilePath);
```

## Häufige Probleme und Lösungen

| Problem | Lösung |
|---------|--------|
| Hyperlink öffnet sich nicht | Stellen Sie sicher, dass `HyperlinkAddress` das Protokoll (`http://` oder `https://`) enthält. |
| Textfarbe wird nicht angewendet | `FontColor` beim für den Hyperlink verwendeten `TextStyle` setzen. |
| Mehrere Links auf einer Seite benötigt | Mehrere `TextStyle`-Objekte erstellen, jedes mit seiner eigenen `HyperlinkAddress`, und sie zu denselben oder verschiedenen `RichText`-Objekten hinzufügen. |
| Dokument lässt sich in OneNote nicht laden | Überprüfen Sie, ob Sie eine unterstützte OneNote-Version (2010+) verwenden. |

## Häufig gestellte Fragen

**Q: Kann ich mehrere Hyperlinks im selben Dokument mit Aspose.Note hinzufügen?**  
A: Ja, erstellen Sie einfach zusätzliche `TextStyle`-Instanzen mit unterschiedlichen `HyperlinkAddress`-Werten und hängen Sie sie an Ihre `RichText`-Objekte an.

**Q: Wie kann ich das Aussehen von Hyperlinks anpassen?**  
A: Verwenden Sie Eigenschaften wie `FontColor`, `FontName` und `FontSize` auf dem `TextStyle`, das `IsHyperlink = true` hat. So können Sie das Branding Ihres Dokuments berücksichtigen.

**Q: Unterstützt Aspose.Note Hyperlinks zu externen Websites?**  
A: Absolut. Setzen Sie `HyperlinkAddress` auf jede gültige URL (einschließlich `http://` oder `https://`), um aus der OneNote-Datei heraus zu verlinken.

**Q: Ist es möglich, eine einzelne OneNote-Datei zu erzeugen, die viele Hyperlinks enthält?**  
A: Ja. Durch wiederholtes Anhängen formatierter `RichText`-Segmente mit unterschiedlichen Hyperlink-Adressen können Sie **eine Datei‑Hyperlink‑Sammlung** erzeugen.

**Q: Ist Aspose.Note mit den neuesten OneNote-Versionen kompatibel?**  
A: Die Bibliothek funktioniert mit OneNote 2010 und später, einschließlich der Windows 10 UWP‑Version.

**Zuletzt aktualisiert:** 2026-04-03  
**Getestet mit:** Aspose.Note for .NET 24.11  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}