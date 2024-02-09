---
title: Následné exportní operace v Aspose.Poznámka
linktitle: Následné exportní operace v Aspose.Poznámka
second_title: Aspose.Note .NET API
description: Naučte se provádět následné operace exportu v Aspose.Note pro .NET, abyste efektivně ukládali dokumenty OneNotu v různých formátech.
type: docs
weight: 10
url: /cs/net/loading-and-saving-operations/consequent-export-operations/
---
## Úvod

V tomto tutoriálu se ponoříme do provádění následných exportních operací pomocí Aspose.Note pro .NET. Aspose.Note je výkonná knihovna, která umožňuje vývojářům pracovat se soubory Microsoft OneNote programově. Export dokumentů do různých formátů je běžným požadavkem a Aspose.Note tento úkol efektivně zjednodušuje. Pojďme prozkoumat, jak uložit dokument v různých formátech krok za krokem.

## Předpoklady

Než budete pokračovat v tomto návodu, ujistěte se, že máte následující:

1. Základní znalost programovacího jazyka C#.
2. Visual Studio nainstalované ve vašem systému.
3. Knihovna Aspose.Note pro .NET integrovaná do vašeho projektu.

## Importovat jmenné prostory

Nejprve se ujistěte, že jste do kódu C# importovali potřebné jmenné prostory:

```csharp
using System.IO;
using Aspose.Note;
using System;
using System.Drawing;
using System.Globalization;
```

## Krok 1: Inicializujte dokument

 Nejprve inicializujte nový`Document` objekt s vypnutou detekcí automatických změn rozvržení:

```csharp
Document doc = new Document() { AutomaticLayoutChangesDetectionEnabled = false };
```

## Krok 2: Inicializujte novou stránku

 Vytvoř nový`Page` objekt a specifikujte jeho vlastnosti:

```csharp
Aspose.Note.Page page = new Aspose.Note.Page(doc);
```

## Krok 3: Nastavte titulek stránky

Definujte název stránky spolu s informacemi o datu a čase:

```csharp
ParagraphStyle textStyle = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
page.Title = new Title(doc)
{
    TitleText = new RichText(doc) { Text = "Title text.", ParagraphStyle = textStyle },
    TitleDate = new RichText(doc) { Text = new DateTime(2011, 11, 11).ToString("D", CultureInfo.InvariantCulture), ParagraphStyle = textStyle },
    TitleTime = new RichText(doc) { Text = "12:34", ParagraphStyle = textStyle }
};
```

## Krok 4: Připojte uzel stránky

Přidejte uzel stránky do dokumentu:

```csharp
doc.AppendChildLast(page);
```

## Krok 5: Uložte dokument v různých formátech

Nyní uložte dokument OneNotu v různých formátech:

```csharp
string dataDir = "Your Document Directory";
doc.Save(dataDir + "ConsequentExportOperations_out.html");            
doc.Save(dataDir + "ConsequentExportOperations_out.pdf");            
doc.Save(dataDir + "ConsequentExportOperations_out.jpg");            
textStyle.FontSize = 11;           
doc.DetectLayoutChanges();            
doc.Save(dataDir + "ConsequentExportOperations_out.bmp");
```

## Závěr

Na závěr jsme se naučili, jak provádět následné exportní operace pomocí Aspose.Note pro .NET. Podle kroků popsaných v tomto kurzu můžete bezproblémově ukládat dokumenty OneNotu v různých formátech, čímž se zvýší všestrannost vašich aplikací.

## FAQ

### Q1: Mohu dále upravit název stránky?

A1: Ano, před uložením dokumentu můžete upravit text nadpisu, datum a čas podle svých požadavků.

### Q2: Jak zvládnu detekci změn rozložení?

 A2: Jak je ukázáno, můžete ručně zjistit změny rozložení pomocí`DetectLayoutChanges()` metoda poskytovaná Aspose.Note.

### Otázka 3: Podporuje Aspose.Note jiné formáty exportu kromě zmíněných?

Odpověď 3: Ano, Aspose.Note podporuje širokou škálu exportních formátů, včetně DOCX, PNG, TIFF a dalších.

### Q4: Je Aspose.Note kompatibilní s .NET Core?

Odpověď 4: Ano, Aspose.Note je kompatibilní s prostředími .NET Framework i .NET Core.

### Q5: Kde najdu další zdroje a podporu pro Aspose.Note?

Odpověď 5: Můžete navštívit dokumentaci a fórum Aspose.Note, kde najdete komplexní průvodce, výukové programy a podporu komunity.