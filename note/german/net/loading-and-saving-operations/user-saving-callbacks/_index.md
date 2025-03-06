---
title: Benutzersparende Rückrufe in Aspose.Note
linktitle: Benutzersparende Rückrufe in Aspose.Note
second_title: Aspose.Note .NET-API
description: Erfahren Sie, wie Sie benutzerspeichernde Rückrufe in Aspose.Note für .NET implementieren, um das Speichern von Schriftarten, CSS und Bildern anzupassen.
weight: 31
url: /de/net/loading-and-saving-operations/user-saving-callbacks/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Benutzersparende Rückrufe in Aspose.Note

## Einführung

In diesem Tutorial erfahren Sie, wie Sie benutzersparende Rückrufe in Aspose.Note für .NET implementieren. Mit diesen Rückrufen können Sie den Speichervorgang anpassen, indem Sie Hooks bereitstellen, mit denen Sie in verschiedenen Phasen eingreifen können, z. B. beim Speichern von Schriftarten, CSS-Stylesheets und Bildern. Mithilfe dieser Rückrufe können Sie das Speicherverhalten an Ihre spezifischen Anforderungen anpassen und so die Flexibilität und Kontrolle über die Ausgabe erhöhen.

## Voraussetzungen

Bevor Sie sich mit der Implementierung benutzersparender Rückrufe in Aspose.Note befassen, stellen Sie sicher, dass die folgenden Voraussetzungen erfüllt sind:

1.  Aspose.Note für .NET SDK: Laden Sie das Aspose.Note für .NET SDK von herunter und installieren Sie es[Download-Seite](https://releases.aspose.com/note/net/).
   
2. Entwicklungsumgebung: Richten Sie eine geeignete Entwicklungsumgebung ein, z. B. Visual Studio oder eine andere .NET-Entwicklungsumgebung.

## Namespaces importieren

Stellen Sie zunächst sicher, dass Sie die erforderlichen Namespaces in Ihr Projekt importieren, um auf die erforderlichen Klassen und Methoden aus der Aspose.Note-Bibliothek zuzugreifen:

```csharp
using Aspose.Note.Saving.Html;
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Text;
```

Lassen Sie uns nun die Implementierung benutzersparender Rückrufe in mehrere Schritte unterteilen:

## Schritt 1: Callback-Eigenschaften definieren

```csharp
public string RootFolder { get; set; }
public bool KeepCssStreamOpened { get; set; }
public string CssFolder { get; set; }
public Stream CssStream { get; private set; }
public string FontsFolder { get; set; }
public string ImagesFolder { get; set; }
```

Hier definieren wir verschiedene Eigenschaften, um den Stammordner, den CSS-Ordner, den Schriftartenordner, den Bilderordner und andere relevante Einstellungen festzulegen.

## Schritt 2: Implementieren Sie den Rückruf zum Speichern von Schriftarten

```csharp
public void FontSaving(FontSavingArgs args)
{
    string uri;
    Stream stream;
    this.CreateResourceInFolder(this.FontsFolder, args.FileName, out uri, out stream);
    args.Stream = stream;
    args.Uri = Path.Combine("..", uri).Replace("\\", "\\\\");
}
```

 In diesem Schritt implementieren wir die`FontSaving` Rückrufmethode zum Speichern von Schriftarten. Es erstellt eine Ressource im angegebenen Schriftartenordner und weist den Stream und den URI entsprechend zu.

## Schritt 3: Implementieren Sie den CSS-Speicherrückruf

```csharp
public void CssSaving(CssSavingArgs args)
{
    string uri;
    Stream stream;
    this.CreateResourceInFolder(this.CssFolder, args.FileName, out uri, out stream);
    args.Stream = this.CssStream = stream;
    args.KeepStreamOpen = this.KeepCssStreamOpened;
    args.Uri = uri;
}
```

 Hier definieren wir die`CssSaving` Rückrufmethode zum Verwalten des Speicherns von CSS-Stylesheets. Es erstellt eine Ressource im angegebenen CSS-Ordner und legt den Stream, den URI und andere Eigenschaften entsprechend fest.

## Schritt 4: Implementieren Sie den Rückruf zum Speichern von Bildern

```csharp
public void ImageSaving(ImageSavingArgs args)
{
    string uri;
    Stream stream;
    this.CreateResourceInFolder(this.ImagesFolder, args.FileName, out uri, out stream);
    args.Stream = stream;
    args.Uri = uri;
}
```

 Zuletzt implementieren wir die`ImageSaving` Rückrufmethode zum Speichern von Bildern. Ähnlich wie bei den vorherigen Schritten wird eine Ressource im angegebenen Bilderordner erstellt und der Stream und der URI zugewiesen.

## Abschluss

In diesem Tutorial haben wir gelernt, wie man benutzersparende Rückrufe in Aspose.Note für .NET implementiert. Indem Sie die bereitgestellten Schritte befolgen, können Sie den Speichervorgang für Schriftarten, CSS-Stylesheets und Bilder anpassen und so eine größere Flexibilität und Kontrolle über die Ausgabe ermöglichen.

## FAQs

### F1: Kann ich diese Rückrufe verwenden, um andere Aspekte des Speichervorgangs anzupassen?

A1: Ja, Sie können diese Rückrufe erweitern oder zusätzliche implementieren, um verschiedene Aspekte des Speichervorgangs an Ihre Bedürfnisse anzupassen.

### F2: Ist Aspose.Note für .NET mit anderen .NET-Frameworks kompatibel?

A2: Ja, Aspose.Note für .NET ist mit verschiedenen .NET-Frameworks kompatibel, einschließlich .NET Core und .NET Standard.

### F3: Wie kann ich während des Speichervorgangs mit Fehlern oder Ausnahmen umgehen?

A3: Sie können Fehlerbehandlungsmechanismen in jede Rückrufmethode integrieren, um eventuell auftretende Fehler oder Ausnahmen ordnungsgemäß zu behandeln.

### F4: Gibt es irgendwelche Leistungsaspekte bei der Verwendung dieser Rückrufe?

A4: Obwohl diese Rückrufe Flexibilität bieten, stellen Sie sicher, dass sie effizient implementiert werden, um Leistungseinbußen zu vermeiden, insbesondere beim Umgang mit großen Dokumenten oder Ressourcen.

### F5: Kann ich das Speicherverhalten basierend auf Benutzereingaben oder anderen Bedingungen dynamisch ändern?

A5: Ja, Sie können bedingte Logik in die Rückrufmethoden integrieren, um das Speicherverhalten basierend auf verschiedenen Faktoren dynamisch anzupassen.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
