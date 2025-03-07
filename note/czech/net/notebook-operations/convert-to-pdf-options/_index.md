---
title: Převeďte Poznámkové bloky do PDF pomocí možností v Aspose Note .NET
linktitle: Převeďte Poznámkové bloky do PDF pomocí možností v Aspose Note .NET
second_title: Aspose.Note .NET API
description: Přečtěte si, jak převést poznámkové bloky Microsoft OneNote do formátu PDF pomocí knihovny Aspose.Note for .NET s přizpůsobitelnými možnostmi.
weight: 16
url: /cs/net/notebook-operations/convert-to-pdf-options/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Převeďte Poznámkové bloky do PDF pomocí možností v Aspose Note .NET

## Úvod

V tomto tutoriálu projdeme procesem převodu poznámkových bloků do formátu PDF pomocí knihovny Aspose.Note for .NET. Aspose.Note pro .NET poskytuje výkonnou sadu funkcí pro programovou práci se soubory Microsoft OneNote.

## Předpoklady

Než začneme, ujistěte se, že máte následující předpoklady:

### 1. Aspose.Note pro .NET Library
 Ujistěte se, že jste si stáhli a nainstalovali knihovnu Aspose.Note for .NET. Můžete si jej stáhnout z[webová stránka](https://releases.aspose.com/note/net/).

### 2. Vývojové prostředí
Měli byste mít nastavené vývojové prostředí, jako je Visual Studio, s nainstalovaným nezbytným .NET frameworkem.

## Import jmenných prostorů

Než začneme používat Aspose.Note pro .NET v našem projektu, importujme požadované jmenné prostory:

```csharp
using System.IO;
using Aspose.Note;
using Aspose.Note.Saving;
using System;
using System.Collections.Generic;
```

Nyní si rozdělme proces převodu poznámkových bloků do PDF s možnostmi do několika kroků:

## Krok 1: Vložte notebook

Nejprve musíme načíst poznámkový blok OneNote, který chceme převést do souboru PDF.

```csharp
// Cesta k adresáři dokumentů.
string dataDir = "Your Document Directory";

// Načtěte poznámkový blok OneNotu
var notebook = new Notebook(dataDir + "Notizbuch �ffnen.onetoc2");
```

## Krok 2: Určete možnosti uložení PDF

Dále upřesníme možnosti uložení poznámkového bloku jako souboru PDF. Můžeme přizpůsobit různá nastavení, jako je algoritmus rozdělení stránky, okraje a velikost stránky.

```csharp
var notebookSaveOptions = new NotebookPdfSaveOptions();
var documentSaveOptions = notebookSaveOptions.DocumentSaveOptions;

documentSaveOptions.PageSplittingAlgorithm = new KeepSolidObjectsAlgorithm();
```

## Krok 3: Uložte Poznámkový blok jako PDF

Nyní poznámkový blok uložíme jako soubor PDF pomocí zadaných možností.

```csharp
dataDir = dataDir + "ConvertToPDF_out.pdf";

// Uložte notebook
notebook.Save(dataDir, notebookSaveOptions);
```

## Krok 4: Ověřte převod

Nakonec ověřte, že převod proběhl úspěšně a vytiskněte místo, kde je soubor PDF uložen.

```csharp
Console.WriteLine("\nNoteBook document converted to pdf successfully with save options.\nFile saved at " + dataDir);
```

## Závěr

V tomto tutoriálu jsme se naučili, jak převést poznámkové bloky OneNote do formátu PDF pomocí knihovny Aspose.Note for .NET. Podle výše uvedených kroků můžete tuto funkci snadno integrovat do svých aplikací .NET.

## FAQ

### Q1: Je Aspose.Note pro .NET kompatibilní se všemi verzemi Microsoft OneNote?

Odpověď 1: Ano, Aspose.Note pro .NET podporuje různé verze Microsoft OneNote, včetně formátů .one a .onetoc2.

### Q2: Mohu přizpůsobit vzhled výstupu PDF?

Odpověď 2: Ano, můžete určit různé možnosti, jako je velikost stránky, okraje a algoritmus dělení stránky, abyste přizpůsobili vzhled výstupu PDF.

### Q3: Poskytuje Aspose.Note pro .NET podporu pro jiné formáty souborů?

Odpověď 3: Ano, Aspose.Note pro .NET podporuje převod do různých jiných formátů, jako jsou obrázky, HTML a dokumenty Microsoft Word.

### Q4: Je k dispozici bezplatná zkušební verze pro Aspose.Note pro .NET?

Odpověď 4: Ano, z webové stránky si můžete stáhnout bezplatnou zkušební verzi Aspose.Note pro .NET a před nákupem vyhodnotit její funkce.

### Q5: Jak mohu získat technickou podporu pro Aspose.Note pro .NET?

 Odpověď 5: Technickou podporu pro Aspose.Note pro .NET získáte návštěvou webu[Aspose.Note fórum](https://forum.aspose.com/c/note/28) nebo kontaktujte přímo tým podpory Aspose.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
