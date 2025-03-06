---
title: Rufen Sie eine Aufzählungs- oder Nummernliste in Aspose.Note Text ab
linktitle: Rufen Sie eine Aufzählungs- oder Nummernliste in Aspose.Note Text ab
second_title: Aspose.Note .NET-API
description: Nutzen Sie das Potenzial von Aspose.Note für .NET mit unserer Schritt-für-Schritt-Anleitung zum Abrufen von Aufzählungs- oder Nummernlisten. Verbessern Sie Ihre Fähigkeiten zur Bearbeitung von OneNote-Dokumenten!
weight: 23
url: /de/net/text-manipulation/retrieve-bullet-number-list/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Rufen Sie eine Aufzählungs- oder Nummernliste in Aspose.Note Text ab

## Einführung
Willkommen in der Welt von Aspose.Note für .NET, einer robusten und vielseitigen Bibliothek, die Entwicklern die mühelose Handhabung von OneNote-Dokumenten ermöglicht. In diesem Tutorial befassen wir uns mit dem Prozess des Abrufens von Aufzählungs- oder Nummernlisten mit Aspose.Note für .NET. Egal, ob Sie ein erfahrener Entwickler oder ein begeisterter Programmierer sind, dieser Leitfaden vermittelt Ihnen das Wissen, um durch die Feinheiten der Arbeit mit Listen in Aspose.Note zu navigieren.
## Voraussetzungen
Bevor wir uns auf die Codierungsreise begeben, stellen Sie sicher, dass die folgenden Voraussetzungen erfüllt sind:
-  Aspose.Note für .NET: Stellen Sie sicher, dass Sie die Aspose.Note-Bibliothek installiert haben. Wenn nicht, können Sie es hier herunterladen[Aspose.Note für .NET-Dokumentation](https://reference.aspose.com/note/net/).
- Entwicklungsumgebung: Richten Sie auf Ihrem Computer eine funktionierende Entwicklungsumgebung, vorzugsweise Microsoft Visual Studio, ein.
- Grundkenntnisse von C#: Machen Sie sich mit C# vertraut, da dieses Tutorial in dieser Sprache verfasst ist.
## Namespaces importieren
Um mit Aspose.Note für .NET interagieren zu können, müssen Sie die erforderlichen Namespaces in Ihr Projekt importieren. Fügen Sie am Anfang Ihres Codes die folgenden Namespaces ein:
```csharp
using System;
using System.Globalization;
using System.IO;
using Aspose.Note;
using System.Collections.Generic;
```
Lassen Sie uns nun den Prozess zum Abrufen von Aufzählungs- oder Nummernlisten Schritt für Schritt aufschlüsseln:
## Schritt 1: Legen Sie Ihr Dokumentenverzeichnis fest
```csharp
// Der Pfad zum Dokumentenverzeichnis.
string dataDir = "Your Document Directory";
```
 Ersetzen`"Your Document Directory"` mit dem tatsächlichen Pfad, in dem sich Ihr Aspose.Note-Dokument befindet.
## Schritt 2: Laden Sie das Dokument
```csharp
// Laden Sie das Dokument in Aspose.Note.
Document oneFile = new Document(dataDir + "ApplyNumberingOnText.one");
```
 Stellen Sie sicher, dass Sie ersetzen`"ApplyNumberingOnText.one"` mit dem Namen Ihres spezifischen OneNote-Dokuments.
## Schritt 3: Sammlung von Knoten abrufen
```csharp
// Rufen Sie eine Sammlung von Knoten des Gliederungselements ab.
IList<OutlineElement> nodes = oneFile.GetChildNodes<OutlineElement>();
```
Dieser Schritt ruft eine Sammlung von Gliederungsknoten aus dem geladenen Dokument ab.
## Schritt 4: Durchlaufen Sie jeden Knoten
```csharp
// Durchlaufen Sie jeden Knoten.
foreach (OutlineElement node in nodes)
{
    if (node.NumberList != null)
    {
        NumberList list = node.NumberList;
        // Fahren Sie mit den nächsten Schritten fort...
    }
}
```
Diese Schleife stellt sicher, dass es sich nur um Knoten handelt, die eine Nummernliste enthalten.
## Schritt 5: Schriftartinformationen abrufen
```csharp
// Rufen Sie den Namen der Schriftart ab
Console.WriteLine("Font Name: " + list.Font);
// Schriftlänge abrufen
Console.WriteLine("Font Length: " + list.Font.Length);
// Schriftgröße abrufen
Console.WriteLine("Font Size: " + list.FontSize);
// Schriftfarbe abrufen
Console.WriteLine("Font Color: " + list.FontColor);
// Format abrufen
Console.WriteLine("Font format: " + list.Format);
// Fett markieren
Console.WriteLine("Is bold: " + list.IsBold);
// Überprüfen Sie die Kursivschrift
Console.WriteLine("Is italic: " + list.IsItalic);
Console.WriteLine();
```
Diese Codezeilen extrahieren verschiedene schriftartbezogene Informationen aus der Nummernliste.
## Abschluss
 Glückwunsch! Sie haben erfolgreich gelernt, wie Sie mit Aspose.Note für .NET Aufzählungs- oder Nummernlisten abrufen. Wenn Sie Ihre Erkundung fortsetzen, lesen Sie die[Dokumentation](https://reference.aspose.com/note/net/) für tiefergehende Einblicke und Funktionalitäten.
## FAQs
### Kann ich Aspose.Note für .NET mit anderen Programmiersprachen verwenden?
Aspose.Note unterstützt hauptsächlich .NET, es gibt jedoch auch andere Versionen der Bibliothek, die auf verschiedene Plattformen und Sprachen zugeschnitten sind.
### Ist Aspose.Note mit den neuesten OneNote-Formaten kompatibel?
Ja, Aspose.Note unterstützt eine Vielzahl von OneNote-Formaten und gewährleistet so die Kompatibilität mit den neuesten Versionen.
### Wie kann ich eine temporäre Lizenz für Aspose.Note erhalten?
 Besuchen[dieser Link](https://purchase.aspose.com/temporary-license/) um eine temporäre Lizenz zu Evaluierungszwecken zu erhalten.
### Welche Supportoptionen stehen Aspose.Note-Benutzern zur Verfügung?
Sie können das erkunden und Hilfe suchen[Aspose.Note-Forum](https://forum.aspose.com/c/note/28) für alle Fragen oder Probleme, auf die Sie stoßen könnten.
### Gibt es eine kostenlose Testversion von Aspose.Note für .NET?
 Ja, Sie können auf die kostenlose Testversion von Aspose.Note für .NET zugreifen[Hier](https://releases.aspose.com/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
