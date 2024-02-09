---
title: Přidejte uzel obrázku s tagem v Aspose.Note
linktitle: Přidejte uzel obrázku s tagem v Aspose.Note
second_title: Aspose.Note .NET API
description: Naučte se, jak vylepšit dokumenty OneNote přidáním obrázků s vlastními značkami pomocí Aspose.Note pro .NET.
type: docs
weight: 10
url: /cs/net/tag-management/add-image-node-tag/
---
## Úvod

V tomto tutoriálu prozkoumáme, jak přidat obrazový uzel se značkou pomocí Aspose.Note pro .NET. Tato funkce vám umožňuje vylepšit vaše dokumenty OneNotu přidáním obrázků s vlastními značkami.

## Předpoklady

Než začnete, ujistěte se, že máte následující:

1. Visual Studio: Nainstalujte Visual Studio IDE do vašeho systému.
2.  Aspose.Note pro .NET: Stáhněte si a nainstalujte knihovnu Aspose.Note pro .NET z[odkaz ke stažení](https://releases.aspose.com/note/net/).
3. Základní znalosti: Seznamte se s programovacím jazykem C# a .NET frameworkem.

## Importovat jmenné prostory

Nejprve se ujistěte, že jste do kódu C# zahrnuli potřebné jmenné prostory:

```csharp
using System.Drawing;
using System.IO;
using Aspose.Note;
using System;
using System.Collections.Generic;
```

## Krok 1: Inicializujte objekty dokumentu a stránky

 Začněte vytvořením instance souboru`Document` třída a a`Page` objekt:

```csharp
Document doc = new Document();
Aspose.Note.Page page = new Aspose.Note.Page(doc);
```

## Krok 2: Inicializujte objekty Outline a OutlineElement

 Dále inicializujte`Outline` a`OutlineElement` objekty:

```csharp
Outline outline = new Outline(doc);
OutlineElement outlineElem = new OutlineElement(doc);
```

## Krok 3: Načtěte a vložte obrázek

Načtěte požadovaný obrázek a vložte jej do uzlu dokumentu:

```csharp
Aspose.Note.Image image = new Aspose.Note.Image(doc, "path_to_your_image.jpg");
outlineElem.AppendChildLast(image);
```

## Krok 4: Přidejte k obrázku značku

Přidejte k obrázku vlastní značku:

```csharp
image.Tags.Add(NoteTag.CreateYellowStar());
```

## Krok 5: Připojte prvek osnovy a uzly stránky

Připojte prvek osnovy a uzly osnovy na stránku:

```csharp
outline.AppendChildLast(outlineElem);
page.AppendChildLast(outline);
```

## Krok 6: Uložte dokument

Uložte upravený dokument OneNotu:

```csharp
doc.AppendChildLast(page);
string outputFilePath = "output_path/AddImageNodeWithTag_out.one";
doc.Save(outputFilePath);
```

## Závěr

Podle těchto kroků můžete pomocí Aspose.Note for .NET bez problémů přidat obrazový uzel s vlastní značkou a obohatit tak své dokumenty OneNotu o personalizované vizuály.

## FAQ

### Q1: Mohu přidat více obrázků s různými tagy do jednoho dokumentu pomocí Aspose.Note?

Odpověď 1: Ano, můžete přidat více obrázků s různými značkami podle podobných kroků pro každý obrázek.

### Q2: Je Aspose.Note kompatibilní se všemi verzemi OneNotu?

Odpověď 2: Aspose.Note podporuje různé verze OneNotu a zajišťuje kompatibilitu v různých prostředích.

### Q3: Mohu upravit vzhled značky přidané k obrázku?

Odpověď 3: Ano, Aspose.Note poskytuje flexibilitu při přizpůsobení vzhledu značky tak, aby vyhovoval vašim preferencím.

### Q4: Nabízí Aspose.Note podporu pro přidávání obrázků z adres URL?

A4: Aspose.Note primárně podporuje přidávání obrázků z místních adresářů, ale můžete začlenit externí obrázky tak, že je nejprve stáhnete lokálně.

### Otázka 5: Existují nějaká omezení velikosti nebo formátu obrázků, které lze přidat?

A5: Aspose.Note podporuje širokou škálu obrazových formátů a neklade žádná přísná omezení na velikost obrazu, což vám umožňuje začlenit do vašich dokumentů různé vizuální prvky.