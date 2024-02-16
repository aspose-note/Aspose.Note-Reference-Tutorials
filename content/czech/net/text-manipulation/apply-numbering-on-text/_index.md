---
title: Použít číslování na text v Aspose.Note
linktitle: Použít číslování na text v Aspose.Note
second_title: Aspose.Note .NET API
description: Naučte se, jak používat číslování textu v Aspose.Note pro .NET pomocí tohoto komplexního kurzu. Vylepšete formátování dokumentu bez námahy.
type: docs
weight: 12
url: /cs/net/text-manipulation/apply-numbering-on-text/
---
## Úvod
Aspose.Note for .NET poskytuje výkonné nástroje pro manipulaci s dokumenty v aplikacích C#. V tomto tutoriálu prozkoumáme proces použití číslování na text pomocí Aspose.Note. Postupujte podle těchto podrobných pokynů a vylepšete formátování dokumentu bez námahy.
## Předpoklady
Než se pustíte do výukového programu, ujistěte se, že máte splněny následující předpoklady:
- Základní znalost programovacího jazyka C#.
-  Aspose.Note pro .NET nainstalován. Můžete si jej stáhnout[tady](https://releases.aspose.com/note/net/).
- Integrované vývojové prostředí (IDE), jako je Visual Studio.
## Import jmenných prostorů
Chcete-li začít, nezapomeňte importovat potřebné jmenné prostory do svého projektu C#:
```csharp
using System;
using System.Globalization;
using System.IO;
using Aspose.Note;
using System.Drawing;
using System.Collections.Generic;
```
## Krok 1: Nastavte svůj dokument
Začněte vytvořením nového dokumentu a inicializací požadovaných objektů:
```csharp
// Cesta k adresáři dokumentů.
string dataDir = "Your Document Directory";
//Vytvořte objekt třídy Document
Document doc = new Document();
// Inicializujte objekt třídy Page
Aspose.Note.Page page = new Aspose.Note.Page(doc);
// Inicializovat objekt třídy Outline
Outline outline = new Outline(doc);
```
## Krok 2: Definujte výchozí styl
Nastavte výchozí styl pro svůj text pomocí třídy SectionStyle:
```csharp
ParagraphStyle defaultStyle = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
```
## Krok 3: Použijte číslování
Inicializujte objekty třídy OutlineElement a použijte číslování na každý prvek:
```csharp
OutlineElement outlineElem1 = new OutlineElement(doc) { NumberList = new NumberList("{0})", NumberFormat.DecimalNumbers, "Arial", 10) };
RichText text1 = new RichText(doc) { Text = "First", ParagraphStyle = defaultStyle };
outlineElem1.AppendChildLast(text1);
OutlineElement outlineElem2 = new OutlineElement(doc) { NumberList = new NumberList("{0})", NumberFormat.DecimalNumbers, "Arial", 10) };
RichText text2 = new RichText(doc) { Text = "Second", ParagraphStyle = defaultStyle };
outlineElem2.AppendChildLast(text2);
OutlineElement outlineElem3 = new OutlineElement(doc) { NumberList = new NumberList("{0})", NumberFormat.DecimalNumbers, "Arial", 10) };
RichText text3 = new RichText(doc) { Text = "Third", ParagraphStyle = defaultStyle };
outlineElem3.AppendChildLast(text3);
```
## Krok 4: Přidejte prvky osnovy
Připojte prvky obrysu k obrysu:
```csharp
outline.AppendChildLast(outlineElem1);
outline.AppendChildLast(outlineElem2);
outline.AppendChildLast(outlineElem3);
```
## Krok 5: Uložte dokument
Uložte dokument OneNotu s použitým číslováním:
```csharp
dataDir = dataDir + "ApplyNumberingOnText_out.one"; 
doc.Save(dataDir);
Console.WriteLine("\nNumbering applied successfully on a text.\nFile saved at " + dataDir); 
```
## Závěr
Gratulujeme! Úspěšně jste se naučili, jak použít číslování na text v Aspose.Note pro .NET. Experimentujte s různými možnostmi formátování a vytvořte vizuálně přitažlivé dokumenty bez námahy.
## FAQ
### 1. Mohu přizpůsobit formát číslování?
Ano, třída NumberList vám umožňuje upravit formát číslování podle vašich preferencí.
### 2. Jsou k dispozici další možnosti formátování?
Aspose.Note poskytuje širokou škálu možností formátování, včetně stylu písma, barvy a dalších.
### 3. Je Aspose.Note kompatibilní se sadou Visual Studio?
Absolutně! Aspose.Note se hladce integruje se sadou Visual Studio pro hladký vývoj.
### 4. Mohu Aspose.Note před nákupem vyzkoušet?
 Rozhodně! Můžete prozkoumat bezplatnou zkušební verzi[tady](https://releases.aspose.com/).
### 5. Kde mohu získat podporu pro Aspose.Note?
 Pro jakoukoli pomoc nebo dotazy navštivte stránku[Aspose.Note fórum](https://forum.aspose.com/c/note/28).