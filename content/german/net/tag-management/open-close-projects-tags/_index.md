---
title: Öffnen und schließen Sie Projekte mit Tags in Aspose.Note
linktitle: Öffnen und schließen Sie Projekte mit Tags in Aspose.Note
second_title: Aspose.Note .NET-API
description: Erfahren Sie, wie Sie Microsoft OneNote-Dateien programmgesteuert mit Aspose.Note für .NET bearbeiten. Projekte mit Tags effizient öffnen und schließen.
type: docs
weight: 15
url: /de/net/tag-management/open-close-projects-tags/
---
## Einführung

In diesem Tutorial erfahren Sie, wie Sie mit Aspose.Note für .NET Projekte mit Tags öffnen und schließen. Aspose.Note ist eine leistungsstarke API, die es Entwicklern ermöglicht, programmgesteuert mit Microsoft OneNote-Dateien zu arbeiten und Aufgaben wie die Bearbeitung von Text, Bildern und Tags in den Dokumenten zu ermöglichen.

## Voraussetzungen

Bevor wir beginnen, stellen Sie sicher, dass die folgenden Voraussetzungen erfüllt sind:

## Namespaces importieren

```csharp
using System.IO;
using System.Linq;
```

Lassen Sie uns nun jedes Beispiel in mehrere Schritte unterteilen:

## Schritt 1: Laden Sie das Dokument

Zuerst müssen wir das Dokument in Aspose.Note laden.

```csharp
string dataDir = "Your Document Directory";
var oneFile = new Document(Path.Combine(dataDir, "ProjectNotes.one"));
```

## Schritt 2: Projekt-C-Elemente schließen

Schließen wir nun alle Kontrollkästchen im Zusammenhang mit „Projekt C“.

```csharp
foreach (var node in oneFile.GetChildNodes<ITaggable>())
{
    foreach (var checkBox in node.Tags.OfType<CheckBox>())
    {
        if (checkBox.Label.Contains("Project C") && !checkBox.Checked)
        {
            checkBox.SetCompleted();
        }
    }
}
```

## Schritt 3: Speichern Sie die C-Notizen des geschlossenen Projekts

Speichern Sie das geänderte Dokument mit geschlossenen „Projekt C“-Elementen.

```csharp
oneFile.Save("Path to save the closed Project C notes");
```

## Schritt 4: Öffnen Sie Projekt-C-Elemente

Als nächstes öffnen wir alle Kontrollkästchen im Zusammenhang mit „Projekt C“.

```csharp
var oneFile = new Document("Path to the closed Project C notes");

foreach (var node in oneFile.GetChildNodes<ITaggable>())
{
    foreach (var checkBox in node.Tags.OfType<CheckBox>())
    {
        if (checkBox.Label.Contains("Project C") && checkBox.Checked)
        {
            checkBox.SetOpen();
        }
    }
}
```

## Schritt 5: Speichern Sie die C-Notizen des geöffneten Projekts

Speichern Sie das geänderte Dokument mit geöffneten „Projekt C“-Elementen.

```csharp
oneFile.Save(Path.Combine(dataDir, "ProjectNoteWithOpenProjectC.one"));
```

Jetzt haben Sie gelernt, wie Sie Projekte mit Tags in Aspose.Note unter Verwendung von .NET öffnen und schließen.

## Abschluss

Aspose.Note für .NET bietet eine praktische Möglichkeit, OneNote-Dokumente programmgesteuert zu bearbeiten. Wenn Sie diesem Tutorial folgen, können Sie Ihre Projekte effizient verwalten, indem Sie Elemente mithilfe von Tags öffnen und schließen.

## FAQs

### F1: Ist Aspose.Note mit allen Versionen von OneNote kompatibel?

A1: Aspose.Note unterstützt Microsoft OneNote 2010 und neuere Versionen.

### F2: Kann ich Aspose.Note für kommerzielle Projekte verwenden?

 A2: Ja, Sie können Aspose.Note sowohl für persönliche als auch für kommerzielle Projekte verwenden. Besuchen[Hier](https://purchase.aspose.com/buy) eine Lizenz zu erwerben.

### F3: Bietet Aspose.Note eine kostenlose Testversion an?

 A3: Ja, Sie können eine kostenlose Testversion erhalten[Hier](https://releases.aspose.com/).

### F4: Wo finde ich Dokumentation für Aspose.Note?

 A4: Sie finden die Dokumentation[Hier](https://reference.aspose.com/note/net/).

### F5: Wo erhalte ich Unterstützung für Aspose.Note?

 A5: Für Unterstützung können Sie Aspose.Note besuchen[Forum](https://forum.aspose.com/c/note/28).