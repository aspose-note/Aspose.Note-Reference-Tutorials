---
title: Použít odrážky na text v Aspose.Note
linktitle: Použít odrážky na text v Aspose.Note
second_title: Aspose.Note .NET API
description: Naučte se používat odrážky na text v Aspose.Note pro .NET, abyste vylepšili své dokumenty OneNotu. Pro efektivní formátování postupujte podle tohoto podrobného průvodce.
type: docs
weight: 10
url: /cs/net/text-manipulation/apply-bullets-on-text/
---
## Úvod
Vítejte v tomto podrobném návodu k použití odrážek na text pomocí Aspose.Note pro .NET. Aspose.Note je výkonná knihovna, která umožňuje vývojářům bezproblémově pracovat se soubory Microsoft OneNote v jejich aplikacích .NET. V tomto kurzu vás provedeme procesem použití odrážek na text, čímž zvýšíme vizuální přitažlivost vašich dokumentů OneNotu.
## Předpoklady
Než se pustíme do výukového programu, ujistěte se, že máte následující předpoklady:
- Základní znalost programování v C# a .NET.
-  Nainstalovaná knihovna Aspose.Note pro .NET. Můžete si jej stáhnout[tady](https://releases.aspose.com/note/net/).
## Import jmenných prostorů
V kódu C# nezapomeňte zahrnout potřebné jmenné prostory:
```csharp
using System;
using System.Globalization;
using System.IO;
using Aspose.Note;
using System.Drawing;
using System.Collections.Generic;
```
## Krok 1: Nastavte svůj dokument
```csharp
// Cesta k adresáři dokumentů.
string dataDir = "Your Document Directory";
//Vytvořte objekt třídy Document
Aspose.Note.Document doc = new Aspose.Note.Document();
```
## Krok 2: Inicializujte stránku a obrys
```csharp
// Inicializujte objekt třídy Page
Aspose.Note.Page page = new Aspose.Note.Page(doc);
// Inicializovat objekt třídy Outline
Outline outline = new Outline(doc);
```
## Krok 3: Nastavte výchozí styl textu
```csharp
// Inicializujte objekt třídy TextStyle a nastavte vlastnosti formátování
ParagraphStyle defaultStyle = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
```
## Krok 4: Vytvořte prvky obrysu s odrážkami
```csharp
// Inicializujte objekty třídy OutlineElement a použijte odrážky
OutlineElement outlineElem1 = new OutlineElement(doc) { NumberList = new NumberList("*", "Arial", 10) };
RichText text1 = new RichText(doc) { Text = "First", ParagraphStyle = defaultStyle };
outlineElem1.AppendChildLast(text1);
// Opakujte pro další prvky obrysu
```
## Krok 5: Přidejte prvky osnovy do osnovy
```csharp
// Přidejte prvky obrysu
outline.AppendChildLast(outlineElem1);
// Opakujte pro další prvky obrysu
```
## Krok 6: Přidejte na stránku obrys
```csharp
// Přidat uzel osnovy
page.AppendChildLast(outline);
```
## Krok 7: Přidejte stránku do dokumentu
```csharp
//Přidat uzel stránky
doc.AppendChildLast(page);
```
## Krok 8: Uložte dokument OneNotu
```csharp
// Uložte dokument OneNotu
dataDir = dataDir + "ApplyBulletsOnText_out.one"; 
doc.Save(dataDir);
Console.WriteLine("\nBullets applied successfully on a text.\nFile saved at " + dataDir); 
```
## Závěr
Gratulujeme! Úspěšně jste se naučili, jak aplikovat odrážky na text pomocí Aspose.Note pro .NET. Tato funkce může výrazně vylepšit formátování vašich dokumentů OneNote a učinit je vizuálně přitažlivějšími.
## FAQ
### Mohu na každou položku v seznamu použít různé styly odrážek?
 Ano, styly odrážek můžete upravit úpravou`NumberList` vlastnosti pro každého`OutlineElement`.
### Je Aspose.Note kompatibilní s nejnovější verzí Microsoft OneNote?
Aspose.Note podporuje různé verze Microsoft OneNote a zajišťuje kompatibilitu se staršími i novějšími verzemi.
### Mohu používat Aspose.Note pro komerční účely?
 Ano, Aspose.Note pro .NET můžete používat v komerčních projektech. Chcete-li získat licenci, navštivte[tady](https://purchase.aspose.com/buy).
### Je k dispozici zkušební verze pro Aspose.Note pro .NET?
 Ano, můžete si stáhnout bezplatnou zkušební verzi[tady](https://releases.aspose.com/).
### Kde najdu další podporu a zdroje?
 Můžete navštívit fórum komunity Aspose.Note[tady](https://forum.aspose.com/c/note/28) za podporu a diskuze.