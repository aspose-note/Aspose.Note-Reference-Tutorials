---
title: Vytvářejte dokumenty s kořenovými a podřízenými stránkami pomocí Aspose.Note
linktitle: Vytvářejte dokumenty s kořenovými a podřízenými stránkami pomocí Aspose.Note
second_title: Aspose.Note .NET API
description: Naučte se používat Aspose.Note pro .NET k vytváření dynamických dokumentů OneNotu s hierarchickou strukturou.
type: docs
weight: 11
url: /cs/net/note-manipulation/create-documents-root-sub-pages/
---
## Úvod

Vítejte v našem tutoriálu o vytváření dokumentů s kořenovými a podstránkami pomocí Aspose.Note pro .NET! Aspose.Note je výkonná knihovna, která umožňuje vývojářům pracovat se soubory Microsoft OneNote programově, což umožňuje vytváření, manipulaci a převod dokumentů OneNotu.

tomto tutoriálu vás krok za krokem provedeme procesem vytváření dokumentu OneNote s kořenovými a podřízenými stránkami. Poskytneme podrobná vysvětlení a úryvky kódu pomocí Aspose.Note pro .NET, což vám usnadní sledování a implementaci do vašich vlastních projektů.

## Předpoklady

Než začneme, ujistěte se, že máte následující předpoklady:

1. Visual Studio: K psaní a kompilaci kódu .NET budete potřebovat Visual Studio nainstalované ve vašem systému.
2.  Aspose.Note pro .NET: Stáhněte a nainstalujte Aspose.Note pro .NET z[stránka ke stažení](https://releases.aspose.com/note/net/).
3. Základní znalost C#: Pro pochopení a implementaci příkladů kódu je nutná znalost programovacího jazyka C#.

Nyní, když máte vše nastaveno, pojďme se vrhnout na tutoriál!

## Importovat jmenné prostory

Nejprve importujme potřebné jmenné prostory do našeho projektu:

```csharp
using System.IO;
using Aspose.Note;
using System;
using System.Collections.Generic;
using System.Drawing;
```

## Krok 1: Inicializujte objekt dokumentu

```csharp
// Vytvořte objekt třídy Document
Document doc = new Document();
```

## Krok 2: Vytvořte kořenovou stránku a podstránky

```csharp
// Inicializujte objekty třídy Page a nastavte jejich úrovně
Page page1 = new Page(doc) { Level = 1 };
Page page2 = new Page(doc) { Level = 2 };
Page page3 = new Page(doc) { Level = 1 };
```

### Pro stránku 1:

```csharp
Outline outline1 = new Outline(doc);
OutlineElement outlineElem1 = new OutlineElement(doc);
ParagraphStyle textStyle1 = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
RichText text1 = new RichText(doc) { Text = "First page.", ParagraphStyle = textStyle1 };
outlineElem1.AppendChildLast(text1);
outline1.AppendChildLast(outlineElem1);
page1.AppendChildLast(outline1);
```

### Pro stránku 2:

```csharp
Outline outline2 = new Outline(doc);
OutlineElement outlineElem2 = new OutlineElement(doc);
ParagraphStyle textStyle2 = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
RichText text2 = new RichText(doc) { Text = "Second page.", ParagraphStyle = textStyle2 };
outlineElem2.AppendChildLast(text2);
outline2.AppendChildLast(outlineElem2);
page2.AppendChildLast(outline2);
```

### Pro stránku 3:

```csharp
Outline outline3 = new Outline(doc);
OutlineElement outlineElem3 = new OutlineElement(doc);
ParagraphStyle textStyle3 = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
RichText text3 = new RichText(doc) { Text = "Third page.", ParagraphStyle = textStyle3 };
outlineElem3.AppendChildLast(text3);
outline3.AppendChildLast(outlineElem3);
page3.AppendChildLast(outline3);
```

## Krok 4: Přidejte stránky do dokumentu

```csharp
// Přidejte stránky do dokumentu OneNotu
doc.AppendChildLast(page1);
doc.AppendChildLast(page2);
doc.AppendChildLast(page3);
```

## Krok 5: Uložte dokument

```csharp
// Uložte dokument OneNotu
string dataDir = "Your Document Directory";
dataDir = dataDir + "CreateDocWithRootAndSubPages_out.one";
doc.Save(dataDir);
```

## Závěr

Gratulujeme! Úspěšně jste se naučili, jak vytvářet dokumenty s kořenovými stránkami a podstránkami pomocí Aspose.Note pro .NET. Nyní můžete tyto znalosti využít k dynamickému generování složitých dokumentů OneNotu ve vašich aplikacích.

## FAQ

### Q1: Dokáže Aspose.Note zpracovat velké dokumenty OneNotu?

Odpověď 1: Ano, Aspose.Note je navržen tak, aby efektivně zpracovával velké dokumenty OneNote bez snížení výkonu.

### Q2: Je Aspose.Note kompatibilní s .NET Core?

Odpověď 2: Ano, Aspose.Note podporuje .NET Core spolu s tradičním .NET Framework.

### Q3: Mohu převést dokumenty OneNote do jiných formátů pomocí Aspose.Note?

A3: Absolutně, Aspose.Note poskytuje možnosti převodu do různých formátů včetně PDF, DOCX, HTML a dalších.

### Q4: Nabízí Aspose.Note integraci cloudu?

A4: Aspose.Note se primárně zaměřuje na místní vývoj, ale můžete jej použít v cloudových prostředích se správným nastavením.

### Q5: Je k dispozici technická podpora pro Aspose.Note?

A5: Ano, Aspose poskytuje vyhrazenou technickou podporu prostřednictvím svého fóra, kde můžete klást otázky a získat pomoc.