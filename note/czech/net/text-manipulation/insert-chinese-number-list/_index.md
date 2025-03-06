---
title: Vložte seznam čínských čísel do textu Aspose.Note
linktitle: Vložte seznam čínských čísel do textu Aspose.Note
second_title: Aspose.Note .NET API
description: Naučte se, jak snadno vložit čínské číselné seznamy do dokumentů Aspose.Note pro .NET. Zvyšte své dovednosti v oblasti formátování dokumentů pomocí tohoto podrobného průvodce.
weight: 20
url: /cs/net/text-manipulation/insert-chinese-number-list/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Vložte seznam čínských čísel do textu Aspose.Note

## Úvod
Chcete zlepšit své dovednosti Aspose.Note for .NET začleněním čínských číselných seznamů do vašich dokumentů? Pokud ano, jste na správném místě! V tomto tutoriálu vás provedeme procesem vkládání čínských číselných seznamů pomocí Aspose.Note pro .NET. Tato výkonná knihovna umožňuje bezproblémovou manipulaci s dokumenty OneNotu.
## Předpoklady
Než se pustíme do výukového programu, ujistěte se, že máte splněny následující předpoklady:
- Základní znalost programování v C#.
-  Aspose.Note pro .NET nainstalován. Můžete si jej stáhnout[tady](https://releases.aspose.com/note/net/).
## Import jmenných prostorů
Chcete-li začít, importujte do projektu potřebné jmenné prostory:
```csharp
using System;
using System.Globalization;
using System.IO;
using Aspose.Note;
using System.Drawing;
using System.Collections.Generic;
```
## Krok 1: Inicializujte dokument OneNotu
```csharp
string dataDir = "Your Document Directory";
Aspose.Note.Document doc = new Aspose.Note.Document();
```
## Krok 2: Inicializujte stránku OneNotu
```csharp
Aspose.Note.Page page = new Aspose.Note.Page(doc);
Outline outline = new Outline(doc);
```
## Krok 3: Použijte nastavení stylu textu
```csharp
ParagraphStyle defaultStyle = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
```
## Krok 4: Vytvořte prvky obrysu
Nyní vytvoříme tři prvky osnovy s čínskými číselnými seznamy:
### Krok 4.1: První prvek
```csharp
OutlineElement outlineElem1 = new OutlineElement(doc) { NumberList = new NumberList("{0})", NumberFormat.ChineseCounting, "Arial", 10) };
RichText text1 = new RichText(doc) { Text = "First", ParagraphStyle = defaultStyle };
outlineElem1.AppendChildLast(text1);
```
### Krok 4.2: Druhý prvek
```csharp
OutlineElement outlineElem2 = new OutlineElement(doc) { NumberList = new NumberList("{0})", NumberFormat.ChineseCounting, "Arial", 10) };
RichText text2 = new RichText(doc) { Text = "Second", ParagraphStyle = defaultStyle };
outlineElem2.AppendChildLast(text2);
```
### Krok 4.3: Třetí prvek
```csharp
OutlineElement outlineElem3 = new OutlineElement(doc) { NumberList = new NumberList("{0})", NumberFormat.ChineseCounting, "Arial", 10) };
RichText text3 = new RichText(doc) { Text = "Third", ParagraphStyle = defaultStyle };
outlineElem3.AppendChildLast(text3);
```
## Krok 5: Připojte prvky k osnově
```csharp
outline.AppendChildLast(outlineElem1);
outline.AppendChildLast(outlineElem2);
outline.AppendChildLast(outlineElem3);
```
## Krok 6: Připojte obrys na stránku
```csharp
page.AppendChildLast(outline);
```
## Krok 7: Připojte stránku k dokumentu
```csharp
doc.AppendChildLast(page);
```
## Krok 8: Uložte dokument OneNotu
```csharp
dataDir = dataDir + "InsertChineseNumberList_out.one"; 
doc.Save(dataDir);
Console.WriteLine("\nChinese number list inserted successfully.\nFile saved at " + dataDir);
```
Gratulujeme! Úspěšně jste vložili čínské číselné seznamy do svého dokumentu Aspose.Note pomocí knihovny .NET.
## Závěr
V tomto tutoriálu jsme se zabývali procesem začlenění čínských číselných seznamů do vašich dokumentů Aspose.Note for .NET krok za krokem. Vylepšete své dovednosti v oblasti formátování dokumentů a zajistěte, aby byl váš obsah poutavější pomocí těchto technik.
## Nejčastější dotazy
### Otázka: Mohu přizpůsobit formátování seznamů čínských čísel?
 Odpověď: Ano, formátování si můžete přizpůsobit úpravou parametrů v`NumberList` konstruktér.
### Otázka: Je Aspose.Note kompatibilní s nejnovější verzí .NET?
Odpověď: Ano, Aspose.Note je pravidelně aktualizován, aby podporoval nejnovější verze .NET.
### Otázka: Kde najdu další příklady a dokumentaci?
Odpověď: Prozkoumejte komplexní[Aspose.Note dokumentaci](https://reference.aspose.com/note/net/).
### Otázka: Jak mohu získat dočasnou licenci pro Aspose.Note?
 A: Získejte dočasnou licenci[tady](https://purchase.aspose.com/temporary-license/).
### Otázka: Kde mohu vyhledat pomoc nebo prodiskutovat dotazy týkající se Aspose.Note?
 A: Navštivte[Fórum podpory Aspose.Note](https://forum.aspose.com/c/note/28) za podporu komunity.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
