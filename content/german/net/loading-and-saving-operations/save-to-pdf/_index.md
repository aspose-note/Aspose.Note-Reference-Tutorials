---
title: In Aspose.Note als PDF speichern
linktitle: In Aspose.Note als PDF speichern
second_title: Aspose.Note .NET-API
description: Erfahren Sie, wie Sie Microsoft OneNote-Dokumente mit Aspose.Note für .NET im PDF-Format speichern. Schritt-für-Schritt-Anleitung mit Codebeispielen für Seitenlayouts im Letter- und A4-Format.
type: docs
weight: 26
url: /de/net/loading-and-saving-operations/save-to-pdf/
---
## Einführung

In diesem Tutorial erfahren Sie, wie Sie Dokumente mit Aspose.Note für .NET im PDF-Format speichern. Aspose.Note ist eine leistungsstarke Bibliothek, die es Entwicklern ermöglicht, programmgesteuert mit Microsoft OneNote-Dateien zu arbeiten. Wir behandeln die Voraussetzungen, importieren Namespaces und stellen Schritt-für-Schritt-Anleitungen zum Speichern von Dokumenten als PDF in verschiedenen Seitenlayouts bereit.

## Voraussetzungen

Bevor wir beginnen, stellen Sie sicher, dass Sie über Folgendes verfügen:

- Visual Studio ist auf Ihrem System installiert.
-  Aspose.Note für .NET-Bibliothek heruntergeladen und installiert. Sie können es herunterladen unter[Hier](https://releases.aspose.com/note/net/).
- Grundkenntnisse der Programmiersprache C#.

## Namespaces importieren

Importieren wir zunächst die erforderlichen Namespaces in unseren C#-Code:

```csharp
using System;
using System.IO;

using Aspose.Note.Saving;
```

Nachdem wir nun die Voraussetzungen erfüllt und die Namespaces importiert haben, können wir mit dem Speichern von Dokumenten als PDF in verschiedenen Seitenlayouts fortfahren.

## Schritt 1: Mit den Letter-Seiteneinstellungen als PDF speichern


```csharp
public static void SaveToPdfUsingLetterPageSettings()
{
    // Der Pfad zum Dokumentenverzeichnis.
    string dataDir = "Your Document Directory";

    // Laden Sie das Dokument in Aspose.Note.
    Document oneFile = new Document(dataDir + "OneNote.one");

    var dst = Path.Combine(dataDir, "SaveToPdfUsingLetterPageSettings.pdf");

    // Speichern Sie das Dokument.
    oneFile.Save(dst, new PdfSaveOptions() { PageSettings = PageSettings.Letter });

    Console.WriteLine("\nOneNote document saved successfully.\nFile saved at " + dst);
}
```

### Erläuterung:

- Wir laden das OneNote-Dokument in Aspose.Note.
- Definieren Sie den Zielpfad für die gespeicherte PDF-Datei.
-  Speichern Sie das Dokument mit im PDF-Format`PdfSaveOptions` mit`PageSettings` einstellen`Letter`.

## Schritt 2: Speichern Sie als PDF mit den A4-Seiteneinstellungen ohne Höhenbeschränkung

```csharp
public static void SaveToPdfUsingA4PageSettingsWithoutHeightLimit()
{
    // Der Pfad zum Dokumentenverzeichnis.
    string dataDir = "Your Document Directory";

    // Laden Sie das Dokument in Aspose.Note.
    Document oneFile = new Document(dataDir + "OneNote.one");

    var dst = Path.Combine(dataDir, "SaveToPdfUsingA4PageSettingsWithoutHeightLimit.pdf");

    // Speichern Sie das Dokument.
    oneFile.Save(dst, new PdfSaveOptions() { PageSettings = PageSettings.A4NoHeightLimit });

    Console.WriteLine("\nOneNote document saved successfully.\nFile saved at " + dst);
}
```

### Erläuterung:

- Ähnlich wie im vorherigen Schritt laden wir das OneNote-Dokument in Aspose.Note.
- Definieren Sie den Zielpfad für die gespeicherte PDF-Datei.
-  Speichern Sie das Dokument mit im PDF-Format`PdfSaveOptions` mit`PageSettings` einstellen`A4NoHeightLimit`.

## Abschluss

In diesem Tutorial haben wir gelernt, wie man Dokumente mit Aspose.Note für .NET im PDF-Format speichert. Wir haben zwei verschiedene Seitenlayouts abgedeckt: Letter und A4 ohne Höhenbeschränkung. Mit Aspose.Note können Entwickler OneNote-Dateien einfach programmgesteuert bearbeiten und so Flexibilität und Effizienz bei Dokumentenverwaltungsaufgaben bieten.

## FAQs

### F1: Kann Aspose.Note komplexe OneNote-Dateien verarbeiten?

A1: Ja, Aspose.Note unterstützt verschiedene Features und Funktionalitäten, um komplexe OneNote-Dateien effektiv zu verarbeiten.

### F2: Ist Aspose.Note für kommerzielle Projekte geeignet?

 A2: Absolut, Aspose.Note kann problemlos in kommerziellen Projekten verwendet werden. Sie können eine Lizenz erwerben[Hier](https://purchase.aspose.com/buy).

### F3: Bietet Aspose.Note eine kostenlose Testversion an?

 A3: Ja, Sie können Aspose.Note mit einer kostenlosen Testversion erkunden[Hier](https://releases.aspose.com/).

### F4: Wo finde ich Dokumentation für Aspose.Note?

 A4: Hier finden Sie eine ausführliche Dokumentation[Hier](https://reference.aspose.com/note/net/).

### F5: Benötigen Sie weitere Unterstützung?

 A5: Sie können jederzeit Fragen stellen oder Unterstützung im Aspose.Note-Forum suchen[Hier](https://forum.aspose.com/c/note/28).