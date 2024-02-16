---
title: Uložit pomocí specifikovaných písem v Aspose.Note
linktitle: Uložit pomocí specifikovaných písem v Aspose.Note
second_title: Aspose.Note .NET API
description: Naučte se ukládat dokumenty se zadanými fonty v Aspose.Note pro .NET. Snadno upravte nastavení písma pro konzistentní formátování dokumentu.
type: docs
weight: 28
url: /cs/net/loading-and-saving-operations/save-using-specified-fonts/
---
## Úvod

V tomto tutoriálu se naučíme ukládat dokumenty pomocí specifikovaných písem v Aspose.Note pro .NET. Krok za krokem prozkoumáme různé metody, jak toho dosáhnout.

## Předpoklady

Než začneme, ujistěte se, že máte následující:

1.  Aspose.Note pro .NET: Ujistěte se, že jste nainstalovali Aspose.Note pro .NET. Můžete si jej stáhnout z[tady](https://releases.aspose.com/note/net/).

2. Vývojové prostředí: Potřebujete vývojové prostředí nastavené pro vývoj .NET.

## Import jmenných prostorů

Nejprve importujme potřebné jmenné prostory:

```csharp
using System;
using System.IO;

using Aspose.Note.Fonts;
using Aspose.Note.Saving;

```

## Krok 1: Uložení s výchozím názvem písma

V tomto kroku uložíme dokument pomocí zadaného výchozího názvu písma.

```csharp
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontName()
{
    // Cesta k adresáři dokumentů.
    string dataDir = "Your Document Directory";

    // Vložte dokument do Aspose.Note.
    Document oneFile = new Document(Path.Combine(dataDir, "missing-font.one"));

    // Uložte dokument jako PDF se zadaným výchozím písmem.
    dataDir = dataDir + "SaveUsingDocumentFontsSubsystemWithDefaultFontName_out.pdf";
    oneFile.Save(dataDir, new PdfSaveOptions()
                          {
                              FontsSubsystem = DocumentFontsSubsystem.UsingDefaultFont("Times New Roman")
                          });
}
```

## Krok 2: Uložení s výchozím písmem ze souboru

Dále uložme dokument pomocí výchozího písma načteného ze souboru.

```csharp
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontFromFile()
{
    // Cesta k adresáři dokumentů.
    string dataDir = "Your Document Directory";

    string fontFile = Path.Combine(dataDir, "geo_1.ttf");

    // Vložte dokument do Aspose.Note.
    Document oneFile = new Document(Path.Combine(dataDir, "missing-font.one"));

    // Uložte dokument jako PDF s výchozím písmem načteným ze souboru.
    dataDir = dataDir + "SaveUsingDocumentFontsSubsystemWithDefaultFontFromFile_out.pdf";
    oneFile.Save(dataDir, new PdfSaveOptions()
                          {
                              FontsSubsystem = DocumentFontsSubsystem.UsingDefaultFontFromFile(fontFile)
                          });
}
```

## Krok 3: Ukládání s výchozím písmem ze streamu

Nakonec uložme dokument pomocí výchozího písma načteného ze streamu.

```csharp
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontFromStream()
{
    // Cesta k adresáři dokumentů.
    string dataDir = "Your Document Directory";

    string fontFile = Path.Combine(dataDir, "geo_1.ttf");

    // Vložte dokument do Aspose.Note.
    Document oneFile = new Document(Path.Combine(dataDir, "missing-font.one"));

    // Uložte dokument jako PDF s výchozím písmem načteným ze streamu.
    dataDir = dataDir + "SaveUsingDocumentFontsSubsystemWithDefaultFontFromStream_out.pdf";

    using (var stream = File.Open(fontFile, FileMode.Open, FileAccess.Read, FileShare.Read))
    {
        oneFile.Save(dataDir, new PdfSaveOptions()
                              {
                                  FontsSubsystem = DocumentFontsSubsystem.UsingDefaultFontFromStream(stream)
                              });
    }
}
```

## Závěr

V tomto tutoriálu jsme prozkoumali, jak ukládat dokumenty pomocí specifikovaných písem v Aspose.Note pro .NET. Pomocí těchto kroků můžete upravit nastavení písma podle svých požadavků a zajistit, aby byly vaše dokumenty naformátovány podle potřeby.

## FAQ

### Q1: Mohu použít jakékoli písmo pro ukládání dokumentů v Aspose.Note?

A1: Ano, pro ukládání dokumentů můžete zadat libovolné písmo. Jen se ujistěte, že soubor s písmem je přístupný a správně načtený.

### Q2: Je Aspose.Note kompatibilní s různými formáty dokumentů?

Odpověď 2: Aspose.Note primárně funguje s dokumenty OneNote, ale poskytuje možnosti uložení v různých formátech včetně PDF.

### Q3: Jak mohu vyřešit chybějící písma při ukládání dokumentů?

A3: Aspose.Note nabízí možnosti použití výchozích písem v případě, že zadané písmo chybí, což zajišťuje konzistentní formátování dokumentu.

### Q4: Podporuje Aspose.Note vkládání písem do výstupních dokumentů?

Odpověď 4: Ano, Aspose.Note umožňuje vkládání písem, aby byla zajištěna přenositelnost dokumentu a konzistentní vykreslování na různých platformách.

### Q5: Kde mohu získat další pomoc s Aspose.Note?

 A5: Pro další pomoc nebo technickou podporu můžete navštívit stránku[Aspose.Note fórum](https://forum.aspose.com/c/note/28).