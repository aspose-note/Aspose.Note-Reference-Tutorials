---
title: Přidejte uzel tabulky s tagem v Aspose.Note
linktitle: Přidejte uzel tabulky s tagem v Aspose.Note
second_title: Aspose.Note .NET API
description: Naučte se přidávat tabulky se značkami v Aspose.Note pro .NET. Vylepšete své dovednosti v manipulaci s dokumenty programově.
type: docs
weight: 11
url: /cs/net/tag-management/add-table-node-tag/
---
## Úvod

V tomto tutoriálu vás provedeme procesem přidání uzlu tabulky se značkou pomocí Aspose.Note pro .NET. Chcete-li toho dosáhnout, postupujte podle níže uvedených kroků.

## Import jmenných prostorů

Než začnete, ujistěte se, že jste importovali potřebné jmenné prostory pro práci s Aspose. Poznámka:

```csharp
using System.Drawing;
using System.IO;
using Aspose.Note;
using System;
using System.Collections.Generic;
using Aspose.Note.Examples.CSharp.Tables;
```

## Předpoklady

Než budete pokračovat, ujistěte se, že máte nastaveny následující předpoklady:

1.  Instalace: Stáhněte a nainstalujte knihovnu Aspose.Note for .NET z[tady](https://releases.aspose.com/note/net/).
2.  Licence: Získejte licenci nebo použijte a[dočasná licence](https://purchase.aspose.com/temporary-license/) používat knihovnu.
3. Vývojové prostředí: Mějte nastavené kompatibilní vývojové prostředí, jako je Visual Studio.

## Krok 1: Inicializujte objekty dokumentu a stránky

 Začněte vytvořením instance souboru`Document` třídy a inicializace a`Page` objekt:

```csharp
Document doc = new Document();
Aspose.Note.Page page = new Aspose.Note.Page(doc);
```

## Krok 2: Vytvořte objekty tabulky, řádku a buňky

 Inicializujte`Table`, `TableRow` , a`TableCell` objekty:

```csharp
TableRow row = new TableRow(doc);
TableCell cell = new TableCell(doc);
```

## Krok 3: Vložte obsah do buňky

 Přidejte obsah do buňky pomocí`AppendChildLast` metoda:

```csharp
cell.AppendChildLast(InsertTable.GetOutlineElementWithText(doc, "Single cell."));
```

## Krok 4: Inicializujte uzel tabulky

 Inicializujte`Table` objekt se specifikovanými vlastnostmi:

```csharp
Table table = new Table(doc)
{
    IsBordersVisible = true,
    Columns = { new TableColumn { Width = 70 } }
};
```

## Krok 5: Přidejte řádek do tabulky

Přidejte uzel řádku do tabulky:

```csharp
table.AppendChildLast(row);
```

## Krok 6: Přidejte značku do uzlu tabulky

Zahrnout značku pro uzel tabulky:

```csharp
table.Tags.Add(NoteTag.CreateQuestionMark());
```

## Krok 7: Přidejte uzel tabulky do prvku osnovy

 Vytvořit`Outline` a`OutlineElement` přidat uzel tabulky:

```csharp
Outline outline = new Outline(doc);
OutlineElement outlineElem = new OutlineElement(doc);
outlineElem.AppendChildLast(table);
outline.AppendChildLast(outlineElem);
page.AppendChildLast(outline);
doc.AppendChildLast(page);
```

## Krok 8: Uložte dokument

Uložte dokument OneNotu:

```csharp
string dataDir = "Your Document Directory";
dataDir = dataDir + "AddTableNodeWithTag_out.one";
doc.Save(dataDir);
Console.WriteLine("\nTable node with tag added successfully.\nFile saved at " + dataDir);
```

Po provedení těchto kroků byste měli úspěšně přidat uzel tabulky se značkou pomocí Aspose.Note pro .NET.

## Závěr

V tomto tutoriálu jsme probrali proces přidávání uzlu tabulky pomocí značky v Aspose.Note pro .NET. Pomocí těchto kroků můžete efektivně manipulovat s dokumenty OneNotu programově a vylepšit tak možnosti správy dokumentů.

## FAQ

### Q1: Je Aspose.Note kompatibilní se všemi verzemi .NET?

Odpověď 1: Aspose.Note pro .NET podporuje rozhraní .NET Framework verze 2.0 a vyšší, včetně .NET Core a .NET Standard.

### Q2: Mohu vyzkoušet Aspose.Note před zakoupením licence?

 A2: Ano, můžete získat bezplatnou zkušební verzi Aspose.Note od[tady](https://releases.aspose.com/).

### Q3: Jak získám dočasnou licenci pro Aspose.Note?

 A3: Můžete získat dočasnou licenci od[tento odkaz](https://purchase.aspose.com/temporary-license/), který má platnost 30 dnů.

### Q4: Podporuje Aspose.Note šifrování dokumentů?

Odpověď 4: Ano, Aspose.Note poskytuje podporu pro šifrování dokumentů OneNotu, aby byla zajištěna bezpečnost dat.

### Q5: Je pro uživatele Aspose.Note k dispozici technická podpora?

 Odpověď 5: Ano, technická podpora je poskytována prostřednictvím fór Aspose[tady](https://forum.aspose.com/c/note/28), kde můžete vyhledat pomoc od odborníků.