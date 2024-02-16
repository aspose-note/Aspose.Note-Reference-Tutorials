---
title: Převést notebooky na obrázek (zploštěný) v Aspose Note .NET
linktitle: Převést notebooky na obrázek (zploštěný) v Aspose Note .NET
second_title: Aspose.Note .NET API
description: Přečtěte si, jak převést poznámkové bloky OneNote na sloučené obrázky pomocí Aspose.Note pro .NET. Podrobný průvodce pro bezproblémovou integraci.
type: docs
weight: 12
url: /cs/net/notebook-operations/convert-to-image-flattened/
---
## Úvod

V tomto tutoriálu se naučíme, jak používat Aspose.Note pro .NET k převodu poznámkových bloků na sloučené obrázky. Tento proces rozdělíme do jednoduchých kroků, které vám pomohou jej pochopit a efektivně implementovat.

## Předpoklady

Než začneme, ujistěte se, že máte následující:

1.  Aspose.Note pro .NET: Pokud jste to ještě neudělali, stáhněte si a nainstalujte Aspose.Note pro .NET z[tady](https://releases.aspose.com/note/net/).
2. Vývojové prostředí: Ujistěte se, že máte pro vývoj .NET nastaveno vhodné vývojové prostředí.
3. Poznámkový blok OneNotu: Připravte si poznámkový blok OneNotu, který chcete převést na obrázek.

## Import jmenných prostorů

Než začnete s procesem převodu, musíte do kódu importovat potřebné jmenné prostory:

```csharp
using Aspose.Note.Saving;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

Nyní se pojďme ponořit do podrobného průvodce převodem poznámkových bloků na sloučené obrázky pomocí Aspose.Note pro .NET.

## Krok 1: Vložte notebook

Nejprve načtěte poznámkový blok OneNote, který chcete převést do aplikace.

```csharp
// Cesta k adresáři dokumentů.
string dataDir = "Your Document Directory";

// Načtěte poznámkový blok OneNotu
var notebook = new Notebook(dataDir + "Notizbuch öffnen.onetoc2");
```

## Krok 2: Nastavte možnosti uložení

Definujte možnosti uložení pro notebook, včetně formátu obrázku a rozlišení.

```csharp
var notebookSaveOptions = new NotebookImageSaveOptions(SaveFormat.Png);
var documentSaveOptions = notebookSaveOptions.DocumentSaveOptions;

documentSaveOptions.Resolution = 400;
notebookSaveOptions.Flatten = true;
```

## Krok 3: Uložte notebook jako obrázek

Nyní uložte poznámkový blok jako sloučený obrázek pomocí definovaných možností uložení.

```csharp
dataDir = dataDir + "ConvertToImageAsFlattenedNotebook_out.png";

// Uložte notebook
notebook.Save(dataDir, notebookSaveOptions);
```

## Závěr

V tomto tutoriálu jsme se naučili, jak převést poznámkové bloky na sloučené obrázky pomocí Aspose.Note pro .NET. Pokud budete postupovat podle podrobného průvodce, můžete tuto funkci hladce integrovat do svých aplikací .NET.

## FAQ

### Q1: Dokáže Aspose.Note pro .NET zpracovat složité notebooky?

Odpověď 1: Ano, Aspose.Note pro .NET je schopen efektivně zpracovávat složité notebooky.

### Q2: Je k dispozici bezplatná zkušební verze pro Aspose.Note pro .NET?

 A2: Ano, můžete si stáhnout bezplatnou zkušební verzi z[tady](https://releases.aspose.com/).

### Q3: Poskytuje Aspose podporu pro své produkty?

 A3: Ano, můžete získat podporu od komunity Aspose[tady](https://forum.aspose.com/c/note/28).

### Q4: Mohu si zakoupit dočasnou licenci pro Aspose.Note pro .NET?

 A4: Ano, můžete si zakoupit dočasnou licenci[tady](https://purchase.aspose.com/temporary-license/).

### Q5: Kde najdu dokumentaci k Aspose.Note pro .NET?

 A5: Můžete najít dokumentaci[tady](https://reference.aspose.com/note/net/).