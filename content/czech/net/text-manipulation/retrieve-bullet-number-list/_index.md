---
title: Načíst seznam odrážek nebo čísel v textu Aspose.Note
linktitle: Načíst seznam odrážek nebo čísel v textu Aspose.Note
second_title: Aspose.Note .NET API
description: Odemkněte potenciál Aspose.Note pro .NET pomocí našeho podrobného průvodce pro získávání seznamů odrážek nebo čísel. Zvyšte své dovednosti v manipulaci s dokumenty ve OneNotu!
type: docs
weight: 23
url: /cs/net/text-manipulation/retrieve-bullet-number-list/
---
## Úvod
Vítejte ve světě Aspose.Note for .NET, robustní a všestranné knihovny, která umožňuje vývojářům zvládnout manipulaci s dokumenty OneNote bez námahy. V tomto tutoriálu se ponoříme do procesu získávání seznamů odrážek nebo čísel pomocí Aspose.Note pro .NET. Ať už jste zkušený vývojář nebo nadšenec do kódování, tato příručka vás vybaví znalostmi, které vám umožní procházet složitostmi práce se seznamy v Aspose.Note.
## Předpoklady
Než se pustíme do této kódovací cesty, ujistěte se, že máte splněny následující předpoklady:
-  Aspose.Note pro .NET: Ujistěte se, že máte nainstalovanou knihovnu Aspose.Note. Pokud ne, můžete si jej stáhnout z[Aspose.Note pro dokumentaci .NET](https://reference.aspose.com/note/net/).
- Vývojové prostředí: Mějte na svém počítači nastavené funkční vývojové prostředí, nejlépe Microsoft Visual Studio.
- Základní znalost C#: Seznamte se s C#, protože tento tutoriál je napsán v tomto jazyce.
## Importovat jmenné prostory
Abyste mohli komunikovat s Aspose.Note pro .NET, musíte do svého projektu importovat potřebné jmenné prostory. Na začátek kódu uveďte následující jmenné prostory:
```csharp
using System;
using System.Globalization;
using System.IO;
using Aspose.Note;
using System.Collections.Generic;
```
Nyní si rozeberme proces získávání seznamů odrážek nebo čísel krok za krokem:
## Krok 1: Nastavte adresář dokumentů
```csharp
// Cesta k adresáři dokumentů.
string dataDir = "Your Document Directory";
```
 Nahradit`"Your Document Directory"` se skutečnou cestou, kde se nachází váš dokument Aspose.Note.
## Krok 2: Vložte dokument
```csharp
// Vložte dokument do Aspose.Note.
Document oneFile = new Document(dataDir + "ApplyNumberingOnText.one");
```
 Ujistěte se, že jste vyměnili`"ApplyNumberingOnText.one"` s názvem vašeho konkrétního dokumentu OneNotu.
## Krok 3: Načtení kolekce uzlů
```csharp
// Načtěte kolekci uzlů prvku osnovy.
IList<OutlineElement> nodes = oneFile.GetChildNodes<OutlineElement>();
```
Tento krok načte kolekci uzlů osnovy z načteného dokumentu.
## Krok 4: Iterujte přes každý uzel
```csharp
// Iterujte každý uzel.
foreach (OutlineElement node in nodes)
{
    if (node.NumberList != null)
    {
        NumberList list = node.NumberList;
        // Pokračujte dalšími kroky...
    }
}
```
Tato smyčka zajišťuje, že se zabýváme pouze uzly, které obsahují číselný seznam.
## Krok 5: Načtěte informace o písmu
```csharp
// Načíst název písma
Console.WriteLine("Font Name: " + list.Font);
// Načíst délku písma
Console.WriteLine("Font Length: " + list.Font.Length);
// Načíst velikost písma
Console.WriteLine("Font Size: " + list.FontSize);
// Načíst barvu písma
Console.WriteLine("Font Color: " + list.FontColor);
// Načíst formát
Console.WriteLine("Font format: " + list.Format);
// Zaškrtněte tučně
Console.WriteLine("Is bold: " + list.IsBold);
// Zkontrolujte kurzívu
Console.WriteLine("Is italic: " + list.IsItalic);
Console.WriteLine();
```
Tyto řádky kódu extrahují různé informace související s písmy z číselného seznamu.
## Závěr
 Gratulujeme! Úspěšně jste se naučili, jak získat seznamy odrážek nebo čísel pomocí Aspose.Note pro .NET. Jak budete pokračovat v průzkumu, podívejte se na[dokumentace](https://reference.aspose.com/note/net/) pro podrobnější informace a funkce.
## FAQ
### Mohu používat Aspose.Note pro .NET s jinými programovacími jazyky?
Aspose.Note primárně podporuje .NET, ale existují i další verze knihovny přizpůsobené pro různé platformy a jazyky.
### Je Aspose.Note kompatibilní s nejnovějšími formáty OneNote?
Ano, Aspose.Note podporuje širokou škálu formátů OneNote, což zajišťuje kompatibilitu s nejnovějšími verzemi.
### Jak mohu získat dočasnou licenci pro Aspose.Note?
 Návštěva[tento odkaz](https://purchase.aspose.com/temporary-license/) získat dočasnou licenci pro účely hodnocení.
### Jaké možnosti podpory jsou k dispozici pro uživatele Aspose.Note?
 Můžete prozkoumat a vyhledat pomoc v[Aspose.Note fórum](https://forum.aspose.com/c/note/28) pro jakékoli dotazy nebo problémy, se kterými se můžete setkat.
### Existuje bezplatná zkušební verze Aspose.Note pro .NET?
 Ano, máte přístup k bezplatné zkušební verzi Aspose.Note pro .NET[tady](https://releases.aspose.com/).