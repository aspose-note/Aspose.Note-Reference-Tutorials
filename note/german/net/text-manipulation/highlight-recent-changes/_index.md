---
title: Markieren Sie alle letzten Änderungen im Aspose.Note-Text
linktitle: Markieren Sie alle letzten Änderungen im Aspose.Note-Text
second_title: Aspose.Note .NET-API
description: Erweitern Sie Ihre Note-Dokumente mit Aspose.Note für .NET! Erfahren Sie in dieser Schritt-für-Schritt-Anleitung, wie Sie aktuelle Textänderungen hervorheben.
type: docs
weight: 19
url: /de/net/text-manipulation/highlight-recent-changes/
---
## Einführung
Möchten Sie Ihren Note-Dokumenten mithilfe von .NET dynamische und optisch ansprechende Funktionen hinzufügen? Aspose.Note für .NET ist eine leistungsstarke Lösung, mit der Sie Ihre Note-Dateien nahtlos bearbeiten und verbessern können. In diesem Tutorial befassen wir uns mit einem bestimmten Aspekt: dem Hervorheben aller letzten Änderungen im Aspose.Note-Text.
## Voraussetzungen
Bevor wir uns auf diese Reise begeben, stellen Sie sicher, dass die folgenden Voraussetzungen erfüllt sind:
-  Aspose.Note für .NET: Stellen Sie sicher, dass Sie die Aspose.Note-Bibliothek installiert haben. Sie können es hier herunterladen[Aspose.Note für .NET-Dokumentation](https://reference.aspose.com/note/net/).
- Entwicklungsumgebung: Richten Sie eine .NET-Entwicklungsumgebung ein, einschließlich einer IDE wie Visual Studio.
- Beispieldokument: Bereiten Sie ein Notizdokument (in diesem Fall „Aspose.one“) vor, das den Text enthält, den Sie hervorheben möchten.
## Namespaces importieren
Importieren Sie zunächst die erforderlichen Namespaces in Ihr .NET-Projekt:
```csharp
    using System;
    using System.Drawing;
    using System.IO;
    using System.Linq;
```
## Schritt 1: Laden Sie das Dokument
Beginnen Sie mit dem Laden des Note-Dokuments in Aspose.Note:
```csharp
string dataDir = "Your Document Directory";
Document document = new Document(dataDir + "Aspose.one");
```
## Schritt 2: Identifizieren Sie die letzten Änderungen
Identifizieren Sie als Nächstes die RichText-Knoten, die in der letzten Woche geändert wurden:
```csharp
var richTextNodes = document.GetChildNodes<RichText>().Where(e => e.LastModifiedTime >= DateTime.Today.Subtract(TimeSpan.FromDays(7)));
```
## Schritt 3: Hervorhebungsfarben festlegen
Legen Sie nun die Hervorhebungsfarbe für die identifizierten Knoten und Textläufe fest:
```csharp
foreach (var node in richTextNodes)
{
    // Legen Sie die Hervorhebungsfarbe für den Absatz fest
    node.ParagraphStyle.Highlight = Color.DarkGreen;
    // Legen Sie die Hervorhebungsfarbe für jeden Textlauf fest
    foreach (var run in node.TextRuns)
    {
        run.Style.Highlight = Color.DarkSeaGreen;
    }
}
```
## Schritt 4: Speichern Sie das geänderte Dokument
Speichern Sie das Dokument mit den hervorgehobenen letzten Änderungen:
```csharp
document.Save(Path.Combine(dataDir, "HighlightAllRecentChanges.pdf"));
```
## Schritt 5: Erfolgsmeldung anzeigen
Zeigen Sie abschließend eine Erfolgsmeldung an, um den Benutzer zu informieren:
```csharp
Console.WriteLine("\nText's recent changes are highlighted successfully.");
```
## Abschluss
In diesem Tutorial haben wir untersucht, wie Sie Aspose.Note für .NET verwenden, um alle letzten Textänderungen in einem Note-Dokument hervorzuheben. Diese Funktion verbessert die Sichtbarkeit von Dokumenten und ist eine wertvolle Ergänzung Ihres Toolkits für die Arbeit mit Notizdateien.
## FAQs
### Kann ich für verschiedene Zeiträume unterschiedliche Hervorhebungsfarben anwenden?
Ja, Sie können den Code anpassen, um je nach Ihren spezifischen Anforderungen unterschiedliche Hervorhebungsfarben festzulegen.
### Ist Aspose.Note mit den neuesten .NET-Frameworks kompatibel?
Aspose.Note aktualisiert seine Bibliotheken regelmäßig, um die Kompatibilität mit den neuesten .NET-Frameworks sicherzustellen.
### Wie kann ich mit Fehlern bei der Implementierung dieser Funktion umgehen?
Sie können Try-Catch-Blöcke integrieren, um Ausnahmen zu behandeln und ein reibungsloses Benutzererlebnis zu gewährleisten.
### Unterstützt Aspose.Note andere Textformatierungsfunktionen?
Absolut! Aspose.Note bietet eine breite Palette von Funktionen zur Textformatierung, einschließlich Schriftarten, -größen und mehr.
### Kann ich diese Lösung in eine Webanwendung integrieren?
Ja, Sie können Aspose.Note für .NET in Webanwendungen integrieren, um die Dokumentverarbeitungsfunktionen zu verbessern.