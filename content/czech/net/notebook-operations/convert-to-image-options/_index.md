---
title: Převeďte notebooky na obrázek s možnostmi v Aspose Note .NET
linktitle: Převeďte notebooky na obrázek s možnostmi v Aspose Note .NET
second_title: Aspose.Note .NET API
description: Naučte se, jak převést poznámkové bloky na obrázky s přizpůsobitelnými možnostmi pomocí Aspose.Note pro .NET.
type: docs
weight: 13
url: /cs/net/notebook-operations/convert-to-image-options/
---
## Úvod

tomto tutoriálu se ponoříme do převodu poznámkových bloků na obrázky s různými možnostmi pomocí knihovny Aspose.Note for .NET. Aspose.Note je výkonné rozhraní .NET API, které umožňuje vývojářům pracovat se soubory Microsoft OneNote programově. Podle kroků uvedených v této příručce se naučíte, jak bez námahy převést notebooky na obrázky a zároveň upravit výstup podle vašich požadavků.

## Předpoklady

Než začneme, ujistěte se, že máte následující předpoklady:

1. Základní znalost C#: Pro pochopení a implementaci poskytnutých úryvků kódu je nezbytná znalost programovacího jazyka C#.

2.  Aspose.Note pro .NET: Stáhněte a nainstalujte Aspose.Note pro .NET z[webová stránka](https://releases.aspose.com/note/net/). Můžete získat bezplatnou zkušební verzi nebo zakoupit licenci podle svých potřeb.

3. Vývojové prostředí: Nastavte své preferované vývojové prostředí pomocí sady Visual Studio nebo jiného IDE, které podporuje vývoj .NET.

## Importovat jmenné prostory

Pro začátek importujme potřebné jmenné prostory pro práci s Aspose.Note pro .NET.

```csharp
using System.IO;
using Aspose.Note;
using Aspose.Note.Saving;
using System;
using System.Collections.Generic;
```

Nyní si rozdělme proces převodu poznámkových bloků na obrázky s možnostmi do několika kroků.

## Krok 1: Vložte notebook

Nejprve načtěte soubor poznámkového bloku, který chcete převést na obrázek.

```csharp
// Cesta k adresáři dokumentů.
string dataDir = "Your Document Directory";

// Načtěte poznámkový blok OneNotu
var notebook = new Notebook(dataDir + "Notizbuch �ffnen.onetoc2");
```

## Krok 2: Nastavte možnosti uložení obrázku

Zadejte možnosti pro uložení poznámkového bloku jako obrázku. Zde nastavíme formát obrázku na PNG a přizpůsobíme rozlišení.

```csharp
var notebookSaveOptions = new NotebookImageSaveOptions(SaveFormat.Png);

var documentSaveOptions = notebookSaveOptions.DocumentSaveOptions;

documentSaveOptions.Resolution = 400;
```

## Krok 3: Uložte notebook jako obrázek

Uložte zápisník jako obrázek pomocí zadaných možností.

```csharp
dataDir = dataDir + "ConvertToImageWithOptions_out.png";

// Uložte notebook
notebook.Save(dataDir, notebookSaveOptions);
```

## Závěr

Na závěr jsme prozkoumali, jak převést notebooky na obrázky s různými možnostmi pomocí Aspose.Note pro .NET. Podle kroků uvedených v tomto kurzu můžete tuto funkci bez problémů integrovat do svých aplikací .NET a umožnit tak efektivní manipulaci se soubory Microsoft OneNote.

## FAQ

### Q1: Mohu pomocí Aspose.Note pro .NET převést více notebooků současně?

Odpověď 1: Ano, můžete procházet více soubory poznámkového bloku a převádět je na obrázky pomocí podobných metod, které jsou uvedeny v tomto kurzu.

### Q2: Je Aspose.Note for .NET kompatibilní s .NET Core?

Odpověď 2: Ano, Aspose.Note pro .NET je kompatibilní s prostředími .NET Framework i .NET Core.

### Otázka 3: Existují nějaká omezení velikosti notebooků, které lze převést na obrázky?

Odpověď 3: Aspose.Note for .NET neklade konkrétní omezení na velikost notebooků, které lze převést, ale výkon se může lišit v závislosti na velikosti a složitosti notebooku.

### Otázka 4: Mohu upravit výstup obrazu nad rámec nastavení rozlišení?

Odpověď 4: Ano, Aspose.Note pro .NET poskytuje různé možnosti přizpůsobení výstupu obrázku, jako je úprava okrajů, barev a úrovní komprese.

### Q5: Podporuje Aspose.Note pro .NET jiné formáty obrázků kromě PNG?

Odpověď 5: Ano, Aspose.Note for .NET podporuje několik formátů obrázků, včetně JPEG, BMP, GIF a TIFF.