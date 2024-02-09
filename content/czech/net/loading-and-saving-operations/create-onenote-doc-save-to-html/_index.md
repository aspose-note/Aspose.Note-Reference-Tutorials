---
title: Vytvořte dokument OneNote a uložte jej do HTML v Aspose.Note
linktitle: Vytvořte dokument OneNote a uložte jej do HTML v Aspose.Note
second_title: Aspose.Note .NET API
description: Naučte se vytvářet a ukládat dokumenty Microsoft OneNote do formátu HTML v aplikacích .NET pomocí Aspose.Note API. Postupujte podle našeho komplexního tutoriálu s příklady krok za krokem.
type: docs
weight: 14
url: /cs/net/loading-and-saving-operations/create-onenote-doc-save-to-html/
---
## Úvod

Aspose.Note for .NET je výkonné rozhraní API, které umožňuje vývojářům pracovat s dokumenty Microsoft OneNote programově v jejich aplikacích .NET. S Aspose.Note můžete snadno vytvářet, manipulovat a převádět soubory OneNotu. V tomto tutoriálu prozkoumáme, jak vytvořit dokument OneNote a uložit jej do formátu HTML pomocí různých možností, které poskytuje Aspose.Note for .NET API.

## Předpoklady

Než začneme, ujistěte se, že máte následující předpoklady:

- Základní znalost programovacího jazyka C#.
- Visual Studio nainstalované ve vašem systému.
-  Aspose.Note for .NET API nainstalované ve vašem projektu. Můžete si jej stáhnout z[tady](https://releases.aspose.com/note/net/).
- Seznámení se strukturou dokumentů Microsoft OneNote.

## Importovat jmenné prostory

Než se ponoříme do kódovací části, importujme potřebné jmenné prostory:

```csharp
using System;
using System.Drawing;
using System.Globalization;
using System.IO;

using Aspose.Note.Saving;
using Aspose.Note.Saving.Html;

```

Nyní si každý příklad rozdělíme do několika kroků a uvidíme, jak vytvořit dokument OneNote a uložit jej do formátu HTML pomocí Aspose.Note pro .NET.

## Krok 1: Vytvořte dokument OneNotu s výchozími možnostmi

```csharp
public static void CreateAndSaveToHTMLUsingDefaultOptions()
{
    // Inicializujte dokument OneNotu
    Document doc = new Document();
    Page page = doc.AppendChildLast(new Page());

    // Výchozí styl pro veškerý text v dokumentu.
    ParagraphStyle textStyle = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
    page.Title = new Title()
    {
        TitleText = new RichText() { Text = "Title text.", ParagraphStyle = textStyle },
        TitleDate = new RichText() { Text = new DateTime(2011, 11, 11).ToString("D", CultureInfo.InvariantCulture), ParagraphStyle = textStyle },
        TitleTime = new RichText() { Text = "12:34", ParagraphStyle = textStyle }
    };

    // Uložit do formátu HTML
    string dataDir = "Your Document Directory";
    string outputPath = Path.Combine(dataDir, "CreateOneNoteDocAndSaveToHTML_out.html");
    doc.Save(outputPath);

    Console.WriteLine("\nOneNote document created successfully.\nFile saved at " + outputPath);
}
```

V tomto kroku inicializujeme nový dokument OneNotu, přidáme stránku s názvem a uložíme ji do formátu HTML pomocí výchozích možností.

## Krok 2: Vytvořte a uložte konkrétní rozsah stránek do HTML

```csharp
public static void CreateAndSavePageRange()
{
    // Inicializujte dokument OneNotu
    Document doc = new Document();
    Page page = doc.AppendChildLast(new Page());

    // Výchozí styl pro veškerý text v dokumentu.
    ParagraphStyle textStyle = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
    page.Title = new Title()
    {
        TitleText = new RichText() { Text = "Title text.", ParagraphStyle = textStyle },
        TitleDate = new RichText() { Text = new DateTime(2011, 11, 11).ToString("D", CultureInfo.InvariantCulture), ParagraphStyle = textStyle },
        TitleTime = new RichText() { Text = "12:34", ParagraphStyle = textStyle }
    };

    // Uložit do formátu HTML
    string dataDir = "Your Document Directory";
    string outputPath = Path.Combine(dataDir, "CreateAndSavePageRange_out.html");
    doc.Save(outputPath, new HtmlSaveOptions { PageCount = 1, PageIndex = 0 });

    Console.WriteLine("\nOneNote document created successfully and saved as page range.\nFile saved at " + outputPath);
}
```

Zde si ukážeme, jak vytvořit dokument a uložit určitý rozsah stránek do formátu HTML.

## Krok 3: Uložit jako HTML do Memory Stream s vloženými zdroji

```csharp
public static void SaveAsHTMLToMemoryStreamWithEmbeddedResources()
{
    // Načtěte dokument OneNotu
    string dataDir = "Your Document Directory";
    var document = new Document(Path.Combine(dataDir, "Aspose.one"));

    // Zadejte možnosti uložení HTML
    var options = new HtmlSaveOptions()
    {
        ExportCss = ResourceExportType.ExportEmbedded,
        ExportFonts = ResourceExportType.ExportEmbedded,
        ExportImages = ResourceExportType.ExportEmbedded,
        FontFaceTypes = FontFaceType.Ttf
    };

    // Uložte dokument do paměťového streamu
    var memoryStream = new MemoryStream();
    document.Save(memoryStream, options);
}
```

Tento krok ukazuje, jak uložit dokument OneNotu do formátu HTML s vloženými prostředky (CSS, písma a obrázky) do datového proudu paměti.

## Krok 4: Uložit jako HTML do souboru se zdroji v samostatných souborech

```csharp
public static void SaveAsHTMLToFileWithResourcesInSeparateFiles()
{
    // Načtěte dokument OneNotu
    string dataDir = "Your Document Directory";
    var document = new Document(Path.Combine(dataDir, "Aspose.one"));

    // Zadejte možnosti uložení HTML
    var options = new HtmlSaveOptions()
    {
        ExportCss = ResourceExportType.ExportAsStream,
        ExportFonts = ResourceExportType.ExportAsStream,
        ExportImages = ResourceExportType.ExportAsStream,
        FontFaceTypes = FontFaceType.Ttf
    };

    //Uložte dokument do souboru HTML se zdroji uloženými v samostatných souborech
    document.Save(Path.Combine(dataDir, "document_out.html"), options);
}
```

V tomto kroku uložíme dokument OneNotu do formátu HTML se všemi prostředky (CSS, fonty a obrázky) uloženými v samostatných souborech.

## Krok 5: Uložit jako HTML do Memory Stream se zpětnými voláními pro uložení zdrojů

```csharp
public static void SaveAsHTMLToMemoryStreamWithCallBacksToSaveResources()
{
    // Zadejte konfiguraci ukládání zpětných volání
    var savingCallbacks = new UserSavingCallbacks()
    {
        RootFolder = "documentFolder",
        CssFolder = "css",
        KeepCssStreamOpened = true,
        ImagesFolder = "images",
        FontsFolder = "fonts"
    };

    // Zadejte možnosti uložení HTML
    var options = new HtmlSaveOptions
    {
        FontFaceTypes = FontFaceType.Ttf,
        CssSavingCallback = savingCallbacks,
        FontSavingCallback = savingCallbacks,
        ImageSavingCallback = savingCallbacks
    };

    // Načtěte dokument OneNotu
    string dataDir = "Your Document Directory";
    var document = new Document(Path.Combine(dataDir, "Aspose.one"));

    // Uložte dokument do formátu HTML se zdroji spravovanými uživatelem definovaným zpětným voláním
    using (var stream = File.Create(Path.Combine(savingCallbacks.RootFolder, "document.html")))
    {
        document.Save(stream, options);
    }

    // Ručně připojte data do streamu CSS
    using (var writer = new StreamWriter(savingCallbacks.CssStream))
    {
        writer.WriteLine();
        writer.WriteLine("/* This line is appended to stream manually by user */");
    }
}
```

Zde ukazujeme, jak uložit dokument OneNotu do formátu HTML se zdroji spravovanými uživatelem definovaným zpětným voláním.

## Závěr

V tomto článku jsme prozkoumali, jak pracovat s dokumenty OneNotu a ukládat je do formátu HTML pomocí Aspose.Note pro .NET. Podle podrobného průvodce to snadno zvládnete

 integrujte tuto funkci do svých aplikací .NET, což vám umožní efektivně manipulovat se soubory OneNotu.

## FAQ

### Q1: Mohu upravit vzhled uloženého souboru HTML?

Odpověď 1: Ano, vzhled můžete přizpůsobit úpravou šablon stylů CSS generovaných během procesu převodu.

### Q2: Podporuje Aspose.Note převod do jiných formátů kromě HTML?

Odpověď 2: Ano, Aspose.Note podporuje převod do různých formátů, jako jsou PDF, obrázky a dokumenty Microsoft Word.

### Q3: Je Aspose.Note kompatibilní s aplikacemi .NET Core?

Odpověď 3: Ano, Aspose.Note je kompatibilní s aplikacemi .NET Framework i .NET Core.

### Q4: Mohu extrahovat text a obrázky z dokumentů OneNotu pomocí Aspose.Note?

A4: Ano, můžete extrahovat text a obrázky, stejně jako provádět různé další manipulace pomocí Aspose.Note API.

### Q5: Je k dispozici zkušební verze pro testování funkcí Aspose.Note?

 A5: Ano, můžete si stáhnout bezplatnou zkušební verzi z[tady](https://releases.aspose.com/).