---
title: Převod poznámkových bloků do formátu PDF (sloučený) v Aspose Note .NET
linktitle: Převod poznámkových bloků do formátu PDF (sloučený) v Aspose Note .NET
second_title: Aspose.Note .NET API
description: Naučte se, jak bez námahy převést poznámkové bloky OneNote na sloučené PDF pomocí Aspose.Note pro .NET. Bezproblémově uchovávejte svůj obsah.
weight: 15
url: /cs/net/notebook-operations/convert-to-pdf-flattened/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Převod poznámkových bloků do formátu PDF (sloučený) v Aspose Note .NET

## Úvod

Chcete převést své poznámkové bloky OneNote na sloučené soubory PDF pomocí Aspose Note .NET? Jste na správném místě! V tomto tutoriálu projdeme procesem krok za krokem.

## Předpoklady

Než začneme, ujistěte se, že máte následující:

1.  Aspose.Note pro .NET: Ujistěte se, že jste si stáhli a nainstalovali Aspose.Note pro .NET. Pokud ne, můžete to získat od[tady](https://releases.aspose.com/note/net/).
2. Visual Studio: Pro kódování a kompilaci budete potřebovat Visual Studio nainstalované ve vašem systému.
3. OneNote Notebook: Připravte si OneNote Notebook, který chcete převést do PDF.

## Import jmenných prostorů

Začněme importem potřebných jmenných prostorů do vašeho kódu C#:

```csharp
using System.IO;
using Aspose.Note;
using Aspose.Note.Saving;
using System;
using System.Collections.Generic;
```

## Krok 1: Načtěte OneNote Notebook

```csharp
// Cesta k adresáři dokumentů.
string dataDir = "Your Document Directory";

// Načtěte poznámkový blok OneNotu
var notebook = new Notebook(dataDir + "Notizbuch �ffnen.onetoc2");
```

 V tomto kroku načteme OneNote Notebook pomocí`Notebook` třídy poskytuje Aspose.Note.

## Krok 2: Převeďte do PDF pomocí zploštění

```csharp
// Uložte Poznámkový blok jako PDF se sloučením
dataDir = dataDir + "ConvertToPDFAsFlattened_out.pdf";
notebook.Save(
    dataDir,
    new NotebookPdfSaveOptions
    {
        Flatten = true
    }); 
```

 Zde uložíme načtený notebook jako PDF s příponou`Flatten` vlastnost nastavena na`true`. Tato vlastnost sloučí veškerý obsah, včetně anotací a obrázků, do PDF.

## Krok 3: Tisk zprávy o úspěchu

```csharp
Console.WriteLine("\nNoteBook document converted to PDF as flattened successfully.\nFile saved at " + dataDir);
```

Nakonec vytiskneme zprávu o úspěchu spolu s cestou, kam je PDF uložen.

## Závěr

Gratulujeme! Úspěšně jste převedli svůj OneNote Notebook do sloučeného PDF pomocí Aspose.Note for .NET. Tento proces zajišťuje, že veškerý váš obsah bude přesně zachován ve formátu PDF, což usnadňuje sdílení a distribuci.

## FAQ

### Q1: Mohu zachovat interaktivní prvky v PDF?

Odpověď 1: Aspose.Note sloučí obsah, včetně interaktivních prvků, jako jsou zaškrtávací políčka nebo pole formuláře, do PDF, čímž se stanou statickými.

### Q2: Podporuje Aspose.Note převod poznámkových bloků do jiných formátů?

Odpověď 2: Ano, Aspose.Note podporuje převod poznámkových bloků do různých formátů, jako je PDF, HTML, Obrázek a další.

### Q3: Mohu přizpůsobit možnosti převodu?

A3: Rozhodně! Aspose.Note poskytuje rozsáhlé možnosti přizpůsobení během procesu převodu, což vám umožňuje přizpůsobit výstup podle vašich požadavků.

### Q4: Je k dispozici zkušební verze?

 A4: Ano, můžete získat bezplatnou zkušební verzi Aspose.Note od[tady](https://releases.aspose.com/).

### Q5: Kde mohu získat podporu, pokud narazím na nějaké problémy?

 A5: Můžete požádat o podporu od komunity Aspose na[Aspose.Note fóra](https://forum.aspose.com/c/note/28).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
