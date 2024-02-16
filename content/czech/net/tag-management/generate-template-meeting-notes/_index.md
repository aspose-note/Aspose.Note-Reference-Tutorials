---
title: Vygenerujte šablonu pro poznámky ze schůzky s Aspose.Note
linktitle: Vygenerujte šablonu pro poznámky ze schůzky s Aspose.Note
second_title: Aspose.Note .NET API
description: Naučte se generovat strukturované poznámky ze schůzek pomocí Aspose.Note pro .NET. Tento kurz poskytuje podrobného průvodce s příklady kódu.
type: docs
weight: 13
url: /cs/net/tag-management/generate-template-meeting-notes/
---
## Úvod

tomto tutoriálu projdeme procesem generování šablony pro poznámky ke schůzce pomocí Aspose.Note pro .NET. Tato knihovna poskytuje výkonné nástroje pro vytváření, úpravy a manipulaci s dokumenty OneNote programově.

## Předpoklady

Než začneme, ujistěte se, že máte následující:

1. Visual Studio: Ujistěte se, že máte v systému nainstalované Visual Studio.
2.  Aspose.Note pro .NET: Stáhněte a nainstalujte Aspose.Note pro .NET z[tento odkaz](https://releases.aspose.com/note/net/).
3. Základní porozumění C#: Spolu s příklady je vyžadována znalost programovacího jazyka C#.

## Import jmenných prostorů

Chcete-li začít, musíte do svého projektu C# importovat potřebné jmenné prostory. Tyto jmenné prostory poskytují přístup k funkcím poskytovaným Aspose.Note pro .NET.

```csharp
using System;
using System.IO;
```

Nyní si rozdělme proces generování šablony pro poznámky ke schůzce do několika kroků:

## Krok 1: Vytvořte styl číslování seznamu čísel

Nejprve definujeme metodu pro vytvoření stylu číslování pro náš seznam. Tato metoda vytvoří číselný seznam s desítkovým formátem číslování.

```csharp
private static NumberList CreateListNumberingStyle(ParagraphStyle bodyStyle, bool restart)
{
    return new NumberList("{0}.", NumberFormat.DecimalNumbers, bodyStyle.FontName, bodyStyle.FontSize.GetValueOrDefault()) { Restart = restart ? 1 : 0 };
}
```

## Krok 2: Definujte strukturu dokumentu

Dále definujeme strukturu našeho dokumentu s poznámkami ze schůzky. To zahrnuje nastavení stylů pro odstavce záhlaví a těla, vytvoření nového dokumentu a přidání názvu pro týdenní schůzku.

```csharp
// Cesta k adresáři dokumentů.
string dataDir = "Your Document Directory";
var headerStyle = new ParagraphStyle() { FontName = "Calibri", FontSize = 16 };
var bodyStyle = new ParagraphStyle() { FontName = "Calibri", FontSize = 12 };

var d = new Document();
var outline = d.AppendChildLast(new Page()
                                    {
                                        Title = new Title() { TitleText = new RichText() { Text = $"Weekly meeting {DateTime.Today:d}", ParagraphStyle = ParagraphStyle.Default } }
                                    })
               .AppendChildLast(new Outline() { VerticalOffset = 30, HorizontalOffset = 30 });
```

## Krok 3: Přidejte sekci Důležité body

Nyní přidáváme sekci pro důležité body projednávané během setkání. Procházíme seznam důležitých bodů a přidáváme je do dokumentu.

```csharp
outline.AppendChildLast(new OutlineElement())
       .AppendChildLast(new RichText() { Text = "Important", ParagraphStyle = headerStyle });

foreach (var e in new[] { "First", "Second", "Third" })
{
    outline.AppendChildLast(new OutlineElement() { NumberList = CreateListNumberingStyle(bodyStyle, restartFlag) })
           .AppendChildLast(new RichText() { Text = e, ParagraphStyle = bodyStyle });
    restartFlag = false;
}
```

## Krok 4: Přidejte sekci TO DO

Nakonec přidáme sekci pro úkoly, které je třeba udělat. Podobně jako v sekci důležité body iterujeme seznam úkolů a přidáváme zaškrtávací políčka pro každý úkol.

```csharp
outline.AppendChildLast(new OutlineElement())
       .AppendChildLast(new RichText() { Text = "TO DO", ParagraphStyle = headerStyle, SpaceBefore = 15 });

restartFlag = true;
foreach (var e in new[] { "First", "Second", "Third" })
{
    outline.AppendChildLast(new OutlineElement() { NumberList = CreateListNumberingStyle(bodyStyle, restartFlag) })
           .AppendChildLast(new RichText() { Text = e, ParagraphStyle = bodyStyle, Tags = { NoteCheckBox.CreateBlueCheckBox() } });
    restartFlag = false;
}
```

## Krok 5: Uložte dokument

Nakonec vygenerovaný dokument poznámek ze schůzky uložíme do určeného adresáře.

```csharp
d.Save(Path.Combine(dataDir, "meetingNotes.one"));
```

## Závěr

V tomto tutoriálu jsme se naučili, jak vygenerovat šablonu pro poznámky ke schůzce pomocí Aspose.Note pro .NET. Podle podrobného průvodce můžete snadno vytvářet strukturované a organizované dokumenty s poznámkami ze schůzek programově.

## FAQ

### Q1: Mohu přizpůsobit styly odstavců záhlaví a těla?

A1: Ano, můžete upravit název písma, velikost písma a další atributy stylu podle vašich požadavků.

### Q2: Je Aspose.Note for .NET kompatibilní se sadou Visual Studio?

Odpověď 2: Ano, Aspose.Note for .NET se hladce integruje se sadou Visual Studio pro snadný vývoj.

### Otázka 3: Mohu do dokumentu poznámek ze schůzky přidat obrázky nebo tabulky?

Odpověď 3: Ano, Aspose.Note pro .NET poskytuje rozhraní API pro přidávání obrázků, tabulek a dalších prvků do vašeho dokumentu.

### Q4: Podporuje Aspose.Note pro .NET jiné formáty dokumentů kromě OneNotu?

Odpověď 4: Ano, Aspose.Note pro .NET podporuje různé formáty dokumentů, včetně OneNote (*.one) a PDF.

### Q5: Je k dispozici bezplatná zkušební verze pro Aspose.Note pro .NET?

 A5: Ano, můžete si stáhnout bezplatnou zkušební verzi z[tento odkaz](https://releases.aspose.com/).
   