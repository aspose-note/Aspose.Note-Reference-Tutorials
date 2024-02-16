---
title: Přidejte textový uzel s tagem v Aspose.Note
linktitle: Přidejte textový uzel s tagem v Aspose.Note
second_title: Aspose.Note .NET API
description: Naučte se přidávat textové uzly se značkami do dokumentů OneNotu pomocí Aspose.Note pro .NET.
type: docs
weight: 12
url: /cs/net/tag-management/add-text-node-tag/
---
## Úvod

Aspose.Note for .NET je výkonná knihovna, která umožňuje vývojářům vytvářet, manipulovat a převádět soubory Microsoft OneNote programově pomocí rozhraní .NET. V tomto tutoriálu prozkoumáme, jak přidat textový uzel se značkou do dokumentu OneNote pomocí Aspose.Note pro .NET.

## Předpoklady

Než začneme, ujistěte se, že máte následující předpoklady:

1. Visual Studio: Ujistěte se, že máte v systému nainstalované Visual Studio.
2.  Aspose.Note pro .NET: Stáhněte a nainstalujte Aspose.Note pro .NET z[webová stránka](https://releases.aspose.com/note/net/).
3. Základní znalost C#: Seznamte se se základy programovacího jazyka C#.

## Import jmenných prostorů

Nejprve musíte importovat potřebné jmenné prostory pro přístup ke třídám a metodám potřebným pro práci s Aspose.Note pro .NET.

```csharp
using System.Drawing;
using System.IO;
using Aspose.Note;
using System;
using System.Collections.Generic;
```

## Krok 1: Vytvořte objekt dokumentu

Inicializujte objekt dokumentu, abyste mohli začít pracovat s dokumentem OneNotu.

```csharp
// Cesta k adresáři dokumentů.
string dataDir = "Your Document Directory";
Document doc = new Document();
```

## Krok 2: Inicializujte objekty stránky a obrysu

Vytvořte objekty Stránka a Obrys pro strukturování obsahu dokumentu OneNotu.

```csharp
Aspose.Note.Page page = new Aspose.Note.Page(doc);
Outline outline = new Outline(doc);
```

## Krok 3: Přidejte textový uzel s tagem

Vytvořte objekt RichText s požadovaným textem a stylem a poté jej přidejte do prvku OutlineElement.

```csharp
OutlineElement outlineElem = new OutlineElement(doc);
ParagraphStyle textStyle = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
RichText text = new RichText(doc) { Text = "OneNote text.", ParagraphStyle = textStyle };
text.Tags.Add(NoteTag.CreateYellowStar());
outlineElem.AppendChildLast(text);
```

## Krok 4: Připojte prvek osnovy a uzly stránky

Připojte prvek OutlineElement k obrysu a poté přidejte obrys ke stránce. Nakonec připojte stránku k dokumentu.

```csharp
outline.AppendChildLast(outlineElem);
page.AppendChildLast(outline);
doc.AppendChildLast(page);
```

## Krok 5: Uložte dokument

Uložte upravený dokument OneNotu do určeného umístění.

```csharp
string dataDir = "Your Document Directory";
string outputPath = Path.Combine(dataDir, "AddTextNodeWithTag_out.one");
doc.Save(outputPath);
```

## Závěr

Gratulujeme! Úspěšně jste se naučili, jak přidat textový uzel s tagem do dokumentu OneNotu pomocí Aspose.Note pro .NET. S těmito znalostmi nyní můžete své soubory OneNotu programově upravovat a vylepšovat.

## FAQ

### Q1: Mohu do stejného dokumentu přidat více textových uzlů s různými značkami?

Odpověď 1: Ano, můžete přidat více textových uzlů s různými značkami stejným postupem pro každý uzel.

### Q2: Je Aspose.Note pro .NET kompatibilní se všemi verzemi OneNotu?

Odpověď 2: Aspose.Note pro .NET podporuje různé verze OneNotu, včetně 2010, 2013, 2016 a vyšších.

### Q3: Mohu přizpůsobit barvy a styly značek?

A3: Ano, můžete přizpůsobit barvy a styly značek podle svých požadavků.

### Q4: Podporuje Aspose.Note pro .NET šifrování dokumentů?

Odpověď 4: Ano, Aspose.Note pro .NET podporuje šifrování dokumentů, aby byla zajištěna bezpečnost dat.

### Q5: Kde najdu další zdroje a podporu pro Aspose.Note pro .NET?

 A5: Můžete prozkoumat[Aspose.Note pro dokumentaci .NET](https://reference.aspose.com/note/net/) vyhledat pomoc u[Aspose.Note fórum](https://forum.aspose.com/c/note/28).