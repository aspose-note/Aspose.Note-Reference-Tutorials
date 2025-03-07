---
title: Dark Theme-Transformation mit Aspose.Note für .NET
linktitle: Wenden Sie in Aspose.Note ein dunkles Design auf Text an
second_title: Aspose.Note .NET-API
description: Transformieren Sie Ihre OneNote-Dokumente mit Aspose.Note für .NET! Wenden Sie mühelos ein elegantes, dunkles Thema an. Laden Sie es jetzt herunter und verbessern Sie Ihr Notizenerlebnis.
weight: 11
url: /de/net/text-manipulation/apply-dark-theme-text/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Dark Theme-Transformation mit Aspose.Note für .NET

## Einführung
Willkommen zu unserer Schritt-für-Schritt-Anleitung zum Anwenden eines dunklen Themas auf Text in Aspose.Note für .NET. Aspose.Note ist eine leistungsstarke .NET-API, die es Entwicklern ermöglicht, programmgesteuert mit Microsoft OneNote-Dateien zu arbeiten. In diesem Tutorial erfahren Sie, wie Sie Ihren OneNote-Dokumenten ein elegantes und modernes Aussehen verleihen, indem Sie dem Text ein dunkles Thema zuweisen.
## Voraussetzungen
Bevor wir uns mit dem Tutorial befassen, stellen Sie sicher, dass die folgenden Voraussetzungen erfüllt sind:
-  Aspose.Note für .NET: Stellen Sie sicher, dass Aspose.Note für .NET installiert ist. Wenn nicht, können Sie es hier herunterladen[Aspose.Note-Dokumentation](https://reference.aspose.com/note/net/).
- Entwicklungsumgebung: Richten Sie Ihre bevorzugte .NET-Entwicklungsumgebung ein, z. B. Visual Studio.
- Dokumentverzeichnis: Bereiten Sie das Verzeichnis vor, in dem sich Ihr OneNote-Dokument befindet.
## Namespaces importieren
Importieren Sie in Ihrem .NET-Projekt die erforderlichen Namespaces, um mit Aspose zu arbeiten.Hinweis:
```csharp
    using System;
    using System.Drawing;
    using System.IO;
```
## Schritt 1: Laden Sie das OneNote-Dokument
Laden Sie Ihr OneNote-Dokument mit dem folgenden Code in Aspose.Note:
```csharp
// Der Pfad zum Dokumentenverzeichnis.
string dataDir = "Your Document Directory";
// Laden Sie das Dokument in Aspose.Note.
Document doc = new Document(Path.Combine(dataDir, "Aspose.one"));
```
## Schritt 2: Hintergrundfarbe festlegen
Stellen Sie die Hintergrundfarbe jeder Seite auf Schwarz ein:
```csharp
foreach (var page in doc)
{
    page.BackgroundColor = Color.Black;
}
```
## Schritt 3: Passen Sie die Textfarbe an
Passen Sie die Schriftfarbe des Textes zur besseren Sichtbarkeit auf Weiß an:
```csharp
foreach (var node in doc.GetChildNodes<RichText>())
{
    var c = node.ParagraphStyle.FontColor;
    if (c.IsEmpty || Math.Abs(c.R - Color.Black.R) + Math.Abs(c.G - Color.Black.G) + Math.Abs(c.B - Color.Black.B) <= 30)
    {
        node.ParagraphStyle.FontColor = Color.White;
    }
}
```
## Schritt 4: Speichern Sie das Dokument
Speichern Sie das geänderte OneNote-Dokument als PDF:
```csharp
doc.Save(Path.Combine(dataDir, "AsposeDarkTheme.pdf"));
```
## Abschluss
Glückwunsch! Sie haben erfolgreich ein dunkles Design auf den Text in Ihrem Aspose.Note-Dokument angewendet. Diese einfache, aber effektive Verbesserung kann Ihren OneNote-Dateien ein anspruchsvolleres Aussehen verleihen.
## Häufig gestellte Fragen
### Kann ich ein dunkles Design auf bestimmte Abschnitte meines OneNote-Dokuments anwenden?
Ja, Sie können den Code so anpassen, dass er auf bestimmte Seiten oder Abschnitte in Ihrem Dokument abzielt.
### Unterstützt Aspose.Note neben PDF auch andere Exportformate?
Absolut! Aspose.Note unterstützt verschiedene Exportformate, darunter Bilder und Microsoft Word.
### Gibt es eine Grenze für die Dokumentgröße, die Aspose.Note verarbeiten kann?
Aspose.Note kann Dokumente unterschiedlicher Größe verarbeiten und seine Leistung ist auf Effizienz optimiert.
### Kann ich zum ursprünglichen Design zurückkehren, nachdem ich das dunkle Design angewendet habe?
Ja, Sie können den Code ändern, um je nach Ihren Vorlieben zwischen den Themen zu wechseln.
### Wo erhalte ich Unterstützung für Aspose.Note-bezogene Anfragen?
 Wenn Sie Hilfe benötigen, besuchen Sie die[Aspose.Note-Forum](https://forum.aspose.com/c/note/28) oder erkunden Sie die[Dokumentation](https://reference.aspose.com/note/net/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
