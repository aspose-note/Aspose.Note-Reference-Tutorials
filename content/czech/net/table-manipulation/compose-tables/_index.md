---
title: Skládání tabulek pomocí Aspose.Poznámka
linktitle: Skládání tabulek pomocí Aspose.Poznámka
second_title: Aspose.Note .NET API
description: Naučte se skládat strukturované tabulky s bohatým textovým obsahem pomocí Aspose.Note pro .NET. Vylepšete organizaci a čitelnost dokumentů bez námahy.
type: docs
weight: 11
url: /cs/net/table-manipulation/compose-tables/
---
## Úvod

Tabulky jsou základní součástí dokumentů, které umožňují strukturovanou prezentaci informací. Aspose.Note for .NET poskytuje robustní nástroje pro snadné vytváření tabulek. V tomto tutoriálu vás provedeme procesem vytváření tabulek s bohatým textovým obsahem pomocí Aspose.Note.

## Předpoklady

Než se ponoříte do kompozice tabulky s Aspose.Note pro .NET, ujistěte se, že máte následující předpoklady:

1. Nastavení prostředí: Ujistěte se, že máte nastavené vhodné vývojové prostředí s .NET Framework nebo .NET Core.
2.  Instalace: Stáhněte a nainstalujte Aspose.Note pro .NET z[webová stránka](https://releases.aspose.com/note/net/).
3. Základní znalosti: Seznamte se se základními pojmy programování v C# a manipulaci s dokumenty.

## Importovat jmenné prostory

Než začnete sestavovat tabulky, ujistěte se, že jste importovali potřebné jmenné prostory:

```csharp
using System;
using System.Drawing;
using System.IO;
using System.Linq;
```

Rozdělme uvedený příklad do zvládnutelných kroků:

## Krok 1: Nastavte adresář dokumentů

Před sestavením tabulky definujte adresář, kam bude dokument uložen.

```csharp
string dataDir = "Your Document Directory";
```

## Krok 2: Vytvořte text záhlaví

Definujte text záhlaví pomocí specifických stylů, jako je velikost písma a tučné písmo.

```csharp
var headerText = new RichText() { ParagraphStyle = new ParagraphStyle() { FontSize = 18, IsBold = true }, Alignment = HorizontalAlignment.Center }
					.Append("Super contest for suppliers.");
```

## Krok 3: Vytvořte stránku a osnovu

Inicializujte stránku a osnovu pro strukturování obsahu.

```csharp
var page = new Page();
var outline = page.AppendChildLast(new Outline() { HorizontalOffset = 50 });
outline.AppendChildLast(new OutlineElement()).AppendChildLast(headerText);
```

## Krok 4: Přidejte souhrnný text

Před tabulku vložte souhrnný text.

```csharp
var bodyTextHeader = outline.AppendChildLast(new OutlineElement()).AppendChildLast(new RichText() { ParagraphStyle = ParagraphStyle.Default });
bodyTextHeader.Append("This is the final ranking of proposals got from our suppliers.");
```

## Krok 5: Vytvořte tabulku

Inicializací tabulky uspořádejte data do řádků a sloupců.

```csharp
var ranking = outline.AppendChildLast(new OutlineElement()).AppendChildLast(new Table());
```

## Krok 6: Přidejte řádek záhlaví

Naplňte tabulku řádkem záhlaví obsahujícím názvy sloupců.

```csharp
var headerRow = ranking.AppendChildFirst(new TableRow());
foreach (var header in new[] { "Supplier", "Contacts", "Score A", "Score B", "Score C", "Final score", "Attached materials", "Comments" })
{
   ranking.Columns.Add(new TableColumn());
   headerRow.AppendChildLast(new TableCell() { BackgroundColor = backGroundColor })
			 .AppendChildLast(new OutlineElement())
			 .AppendChildLast(new RichText() { ParagraphStyle = headerStyle })
			 .Append(header);
}
```

## Krok 7: Přidejte prázdné řádky

Vložte prázdné řádky a připravte se na vkládání dat.

```csharp
for (int i = 0; i < 5; i++)
{
   backGroundColor = backGroundColor.IsEmpty ? Color.LightGray : Color.Empty;
   var row = ranking.AppendChildLast(new TableRow());
   for (int j = 0; j < ranking.Columns.Count(); j++)
   {
	   row.AppendChildLast(new TableCell() { BackgroundColor = backGroundColor })
		  .AppendChildLast(new OutlineElement())
		  .AppendChildLast(new RichText() { ParagraphStyle = ParagraphStyle.Default });
   }
}
```

## Krok 8: Přidejte kontaktní informace

Vyplňte sloupec 'Kontakty' obsahem šablony.

```csharp
foreach (var row in ranking.Skip(1))
{
   var contactsCell = row.ElementAt(1);
   contactsCell.AppendChildLast(new OutlineElement())
			   .AppendChildLast(new RichText() { ParagraphStyle = ParagraphStyle.Default })
			   .Append("Web: ").Append("link", new TextStyle() { HyperlinkAddress = "www.link.com", IsHyperlink = true });
   contactsCell.AppendChildLast(new OutlineElement())
			   .AppendChildLast(new RichText() { ParagraphStyle = ParagraphStyle.Default })
			   .Append("E-mail: ").Append("mail", new TextStyle() { HyperlinkAddress = "mailto:hi@link.com", IsHyperlink = true });
}
```

## Krok 9: Uložte dokument

Uložte složený dokument tabulky.

```csharp
var d = new Document();
d.AppendChildLast(page);
d.Save(Path.Combine(dataDir, "ComposeTable_out.one"));
```

## Krok 10: Potvrzení

Potvrďte úspěšné složení dokumentu.

```csharp
Console.WriteLine("\nThe document is composed successfully.");
```

## Závěr

tomto tutoriálu jsme prozkoumali, jak skládat tabulky s bohatým textovým obsahem pomocí Aspose.Note pro .NET. Dodržováním těchto podrobných pokynů můžete efektivně vytvářet strukturované tabulky ve svých dokumentech, což zlepšuje čitelnost a organizaci.

## FAQ

### Q1: Mohu přizpůsobit styl prvků tabulky?
   
A1: Ano, můžete přizpůsobit různé aspekty, jako je velikost písma, barva a zarovnání, aby vyhovovaly vašim požadavkům.

### Q2: Je Aspose.Note kompatibilní s jinými knihovnami .NET?
   
Odpověď 2: Aspose.Note se hladce integruje s ostatními knihovnami .NET a nabízí rozsáhlou flexibilitu při manipulaci s dokumenty.

### Q3: Podporuje Aspose.Note export tabulek do různých formátů?
   
A3: Absolutně, Aspose.Note umožňuje exportovat tabulky do různých formátů včetně PDF, DOCX a HTML.

### Q4: Mohu dynamicky naplňovat tabulky daty z externích zdrojů?
   
Odpověď 4: Ano, tabulky můžete dynamicky plnit načítáním dat z databází, rozhraní API nebo uživatelských vstupů.

### Q5: Je pro uživatele Aspose.Note k dispozici technická podpora?
   
A5: Ano, Aspose poskytuje komplexní technickou podporu prostřednictvím svých fór a vyhrazených kanálů podpory.