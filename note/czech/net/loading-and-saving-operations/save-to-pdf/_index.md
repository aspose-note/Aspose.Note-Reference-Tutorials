---
title: Uložit do PDF v Aspose.Note
linktitle: Uložit do PDF v Aspose.Note
second_title: Aspose.Note .NET API
description: Naučte se ukládat dokumenty Microsoft OneNote do formátu PDF pomocí Aspose.Note pro .NET. Výukový program krok za krokem s příklady kódu pro rozvržení stránky Letter a A4.
weight: 26
url: /cs/net/loading-and-saving-operations/save-to-pdf/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Uložit do PDF v Aspose.Note

## Úvod

tomto tutoriálu prozkoumáme, jak ukládat dokumenty do formátu PDF pomocí Aspose.Note pro .NET. Aspose.Note je výkonná knihovna, která umožňuje vývojářům pracovat se soubory Microsoft OneNote programově. Pokryjeme předpoklady, importujeme jmenné prostory a poskytneme podrobné průvodce ukládáním dokumentů do PDF v různých rozvrženích stránek.

## Předpoklady

Než začneme, ujistěte se, že máte následující:

- Visual Studio nainstalované ve vašem systému.
-  Knihovna Aspose.Note pro .NET byla stažena a nainstalována. Můžete si jej stáhnout z[tady](https://releases.aspose.com/note/net/).
- Základní znalost programovacího jazyka C#.

## Import jmenných prostorů

Nejprve importujme potřebné jmenné prostory do našeho kódu C#:

```csharp
using System;
using System.IO;

using Aspose.Note.Saving;
```

Nyní, když máme pokryty předpoklady a importované jmenné prostory, pojďme pokračovat s ukládáním dokumentů do PDF v různých rozvrženích stránky.

## Krok 1: Uložte do PDF pomocí nastavení stránky Letter


```csharp
public static void SaveToPdfUsingLetterPageSettings()
{
    // Cesta k adresáři dokumentů.
    string dataDir = "Your Document Directory";

    // Vložte dokument do Aspose.Note.
    Document oneFile = new Document(dataDir + "OneNote.one");

    var dst = Path.Combine(dataDir, "SaveToPdfUsingLetterPageSettings.pdf");

    // Uložte dokument.
    oneFile.Save(dst, new PdfSaveOptions() { PageSettings = PageSettings.Letter });

    Console.WriteLine("\nOneNote document saved successfully.\nFile saved at " + dst);
}
```

### Vysvětlení:

- Načteme dokument OneNote do Aspose.Note.
- Definujte cílovou cestu pro uložený soubor PDF.
-  Uložte dokument do PDF pomocí`PdfSaveOptions` s`PageSettings` nastaven na`Letter`.

## Krok 2: Uložte do PDF pomocí nastavení stránky A4 bez omezení výšky

```csharp
public static void SaveToPdfUsingA4PageSettingsWithoutHeightLimit()
{
    // Cesta k adresáři dokumentů.
    string dataDir = "Your Document Directory";

    // Vložte dokument do Aspose.Note.
    Document oneFile = new Document(dataDir + "OneNote.one");

    var dst = Path.Combine(dataDir, "SaveToPdfUsingA4PageSettingsWithoutHeightLimit.pdf");

    // Uložte dokument.
    oneFile.Save(dst, new PdfSaveOptions() { PageSettings = PageSettings.A4NoHeightLimit });

    Console.WriteLine("\nOneNote document saved successfully.\nFile saved at " + dst);
}
```

### Vysvětlení:

- Podobně jako v předchozím kroku načteme dokument OneNote do Aspose.Note.
- Definujte cílovou cestu pro uložený soubor PDF.
-  Uložte dokument do PDF pomocí`PdfSaveOptions` s`PageSettings` nastaven na`A4NoHeightLimit`.

## Závěr

V tomto tutoriálu jsme se naučili ukládat dokumenty do formátu PDF pomocí Aspose.Note pro .NET. Pokryli jsme dvě různá rozvržení stránky: Letter a A4 bez omezení výšky. S Aspose.Note mohou vývojáři snadno programově manipulovat se soubory OneNote, což poskytuje flexibilitu a efektivitu v úlohách správy dokumentů.

## FAQ

### Q1: Dokáže Aspose.Note zpracovat složité soubory OneNotu?

Odpověď 1: Ano, Aspose.Note podporuje různé funkce a funkce pro efektivní zpracování složitých souborů OneNotu.

### Q2: Je Aspose.Note vhodný pro komerční projekty?

 A2: Absolutně, Aspose.Note lze snadno použít v komerčních projektech. Můžete si zakoupit licenci[tady](https://purchase.aspose.com/buy).

### Q3: Nabízí Aspose.Note bezplatnou zkušební verzi?

 A3: Ano, můžete prozkoumat Aspose.Note s bezplatnou zkušební verzí[tady](https://releases.aspose.com/).

### Q4: Kde najdu dokumentaci k Aspose.Note?

 A4: Můžete najít podrobnou dokumentaci[tady](https://reference.aspose.com/note/net/).

### Q5: Potřebujete další pomoc?

 A5: Neváhejte se zeptat na jakékoli otázky nebo vyhledat podporu na fóru Aspose.Note[tady](https://forum.aspose.com/c/note/28).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
