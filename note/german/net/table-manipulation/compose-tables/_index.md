---
title: Erstellen Sie Tabellen mit Aspose.Note
linktitle: Erstellen Sie Tabellen mit Aspose.Note
second_title: Aspose.Note .NET-API
description: Erfahren Sie, wie Sie mit Aspose.Note für .NET strukturierte Tabellen mit Rich-Text-Inhalten erstellen. Verbessern Sie mühelos die Organisation und Lesbarkeit von Dokumenten.
weight: 11
url: /de/net/table-manipulation/compose-tables/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Erstellen Sie Tabellen mit Aspose.Note

## Einführung

Tabellen sind grundlegende Bestandteile von Dokumenten und ermöglichen eine strukturierte Darstellung von Informationen. Aspose.Note für .NET bietet robuste Tools zum mühelosen Erstellen von Tabellen. In diesem Tutorial führen wir Sie durch den Prozess der Erstellung von Tabellen mit Rich-Text-Inhalten mit Aspose.Note.

## Voraussetzungen

Bevor Sie mit Aspose.Note für .NET in die Tabellenerstellung eintauchen, stellen Sie sicher, dass Sie die folgenden Voraussetzungen erfüllen:

1. Umgebungseinrichtung: Stellen Sie sicher, dass Sie eine geeignete Entwicklungsumgebung mit .NET Framework oder .NET Core eingerichtet haben.
2.  Installation: Laden Sie Aspose.Note für .NET von herunter und installieren Sie es[Webseite](https://releases.aspose.com/note/net/).
3. Grundkenntnisse: Machen Sie sich mit den Grundkonzepten der C#-Programmierung und Dokumentmanipulation vertraut.

## Namespaces importieren

Bevor Sie mit dem Erstellen von Tabellen beginnen, stellen Sie sicher, dass Sie die erforderlichen Namespaces importieren:

```csharp
using System;
using System.Drawing;
using System.IO;
using System.Linq;
```

Lassen Sie uns das bereitgestellte Beispiel in überschaubare Schritte unterteilen:

## Schritt 1: Richten Sie das Dokumentenverzeichnis ein

Definieren Sie vor dem Erstellen der Tabelle das Verzeichnis, in dem das Dokument gespeichert werden soll.

```csharp
string dataDir = "Your Document Directory";
```

## Schritt 2: Kopfzeilentext erstellen

Definieren Sie den Kopfzeilentext mit bestimmten Stilen wie Schriftgröße und Fettdruck.

```csharp
var headerText = new RichText() { ParagraphStyle = new ParagraphStyle() { FontSize = 18, IsBold = true }, Alignment = HorizontalAlignment.Center }
					.Append("Super contest for suppliers.");
```

## Schritt 3: Seite und Gliederung erstellen

Initialisieren Sie eine Seite und eine Gliederung, um den Inhalt zu strukturieren.

```csharp
var page = new Page();
var outline = page.AppendChildLast(new Outline() { HorizontalOffset = 50 });
outline.AppendChildLast(new OutlineElement()).AppendChildLast(headerText);
```

## Schritt 4: Zusammenfassungstext hinzufügen

Fügen Sie vor der Tabelle einen zusammenfassenden Text ein.

```csharp
var bodyTextHeader = outline.AppendChildLast(new OutlineElement()).AppendChildLast(new RichText() { ParagraphStyle = ParagraphStyle.Default });
bodyTextHeader.Append("This is the final ranking of proposals got from our suppliers.");
```

## Schritt 5: Tabelle erstellen

Initialisieren Sie eine Tabelle, um Daten in Zeilen und Spalten zu organisieren.

```csharp
var ranking = outline.AppendChildLast(new OutlineElement()).AppendChildLast(new Table());
```

## Schritt 6: Kopfzeile hinzufügen

Füllen Sie die Tabelle mit einer Kopfzeile, die Spaltentitel enthält.

```csharp
var headerRow = ranking.AppendChildFirst(new TableRow());
foreach (var header in new[] { "Supplier", "Contacts", "Score A", "Score B", "Score C", "Final score", "Attached materials", "Comments" })
{
   ranking.Columns.Add(new TableColumn());
   headerRow.AppendChildLast(new TableCell() { BackgroundColor = backGroundColor })
			 .AppendChildLast(new OutlineElement())
			 .AppendChildLast(new RichText() { ParagraphStyle = headerStyle })
			 .Append(header);
}
```

## Schritt 7: Leere Zeilen hinzufügen

Fügen Sie leere Zeilen ein, um das Einfügen von Daten vorzubereiten.

```csharp
for (int i = 0; i < 5; i++)
{
   backGroundColor = backGroundColor.IsEmpty ? Color.LightGray : Color.Empty;
   var row = ranking.AppendChildLast(new TableRow());
   for (int j = 0; j < ranking.Columns.Count(); j++)
   {
	   row.AppendChildLast(new TableCell() { BackgroundColor = backGroundColor })
		  .AppendChildLast(new OutlineElement())
		  .AppendChildLast(new RichText() { ParagraphStyle = ParagraphStyle.Default });
   }
}
```

## Schritt 8: Kontaktinformationen hinzufügen

Füllen Sie die Spalte „Kontakte“ mit Vorlageninhalten.

```csharp
foreach (var row in ranking.Skip(1))
{
   var contactsCell = row.ElementAt(1);
   contactsCell.AppendChildLast(new OutlineElement())
			   .AppendChildLast(new RichText() { ParagraphStyle = ParagraphStyle.Default })
			   .Append("Web: ").Append("link", new TextStyle() { HyperlinkAddress = "www.link.com", IsHyperlink = true });
   contactsCell.AppendChildLast(new OutlineElement())
			   .AppendChildLast(new RichText() { ParagraphStyle = ParagraphStyle.Default })
			   .Append("E-mail: ").Append("mail", new TextStyle() { HyperlinkAddress = "mailto:hi@link.com", IsHyperlink = true });
}
```

## Schritt 9: Speichern Sie das Dokument

Speichern Sie das erstellte Tabellendokument.

```csharp
var d = new Document();
d.AppendChildLast(page);
d.Save(Path.Combine(dataDir, "ComposeTable_out.one"));
```

## Schritt 10: Bestätigung

Bestätigen Sie die erfolgreiche Dokumenterstellung.

```csharp
Console.WriteLine("\nThe document is composed successfully.");
```

## Abschluss

In diesem Tutorial haben wir untersucht, wie man mit Aspose.Note für .NET Tabellen mit Rich-Text-Inhalten erstellt. Wenn Sie diese Schritt-für-Schritt-Anleitung befolgen, können Sie effizient strukturierte Tabellen in Ihren Dokumenten erstellen und so die Lesbarkeit und Organisation verbessern.

## FAQs

### F1: Kann ich den Stil von Tabellenelementen anpassen?
   
A1: Ja, Sie können verschiedene Aspekte wie Schriftgröße, Farbe und Ausrichtung an Ihre Anforderungen anpassen.

### F2: Ist Aspose.Note mit anderen .NET-Bibliotheken kompatibel?
   
A2: Aspose.Note lässt sich nahtlos in andere .NET-Bibliotheken integrieren und bietet umfassende Flexibilität bei der Dokumentenbearbeitung.

### F3: Unterstützt Aspose.Note den Export von Tabellen in verschiedene Formate?
   
A3: Absolut, Aspose.Note ermöglicht Ihnen den Export von Tabellen in verschiedene Formate, einschließlich PDF, DOCX und HTML.

### F4: Kann ich Tabellen dynamisch mit Daten aus externen Quellen füllen?
   
A4: Ja, Sie können Tabellen dynamisch füllen, indem Sie Daten aus Datenbanken, APIs oder Benutzereingaben abrufen.

### F5: Ist technischer Support für Aspose.Note-Benutzer verfügbar?
   
A5: Ja, Aspose bietet umfassenden technischen Support über seine Foren und speziellen Supportkanäle.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
