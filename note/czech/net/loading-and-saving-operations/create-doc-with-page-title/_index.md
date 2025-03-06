---
title: Vytvořte dokument s názvem stránky v Aspose.Note
linktitle: Vytvořte dokument s názvem stránky v Aspose.Note
second_title: Aspose.Note .NET API
description: Naučte se vytvářet dokumenty s titulkovými stránkami pomocí Aspose.Note pro .NET. Postupujte podle našeho podrobného průvodce pro bezproblémovou integraci.
weight: 13
url: /cs/net/loading-and-saving-operations/create-doc-with-page-title/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Vytvořte dokument s názvem stránky v Aspose.Note

## Úvod

V tomto tutoriálu vás provedeme procesem vytváření dokumentu s titulní stránkou pomocí Aspose.Note pro .NET. Aspose.Note je výkonné API, které umožňuje vývojářům pracovat se soubory Microsoft OneNote programově.

## Předpoklady

Než začneme, ujistěte se, že máte nainstalované a nastavené následující předpoklady:

### Instalace sady Visual Studio

1. Stáhnout Visual Studio: Pokud jste to ještě neudělali, stáhněte si a nainstalujte Visual Studio z webu Microsoftu.

2. Instalace .NET Development Workload: Během procesu instalace se ujistěte, že jste vybrali pracovní zátěž ".NET desktop development", abyste měli jistotu, že máte všechny potřebné komponenty pro .NET vývoj.

3. Vytvoření nového projektu: Otevřete Visual Studio a vytvořte nový projekt (konzolová aplikace nebo jakýkoli jiný typ, který preferujete).

### Instalace Aspose.Note

1.  Získejte Aspose.Note: Stáhněte si knihovnu Aspose.Note pro .NET z[webová stránka](https://releases.aspose.com/note/net/).

2. Instalace Aspose.Note přes NuGet: Alternativně můžete Aspose.Note pro .NET nainstalovat přes NuGet Package Manager ve Visual Studiu. Jednoduše vyhledejte „Aspose.Note“ a nainstalujte nejnovější verzi.

## Import jmenných prostorů

Nejprve musíte importovat potřebné jmenné prostory, abyste mohli používat Aspose.Note ve svém projektu.

```csharp
using System.IO;
using Aspose.Note;
using Aspose.Note.Saving;
using System;
using System.Drawing;
using System.Globalization;
```

Nyní si proces vytváření dokumentu s názvem stránky rozdělíme do několika kroků:

## Krok 1: Vytvořte objekt dokumentu

```csharp
//Vytvořte objekt třídy Document
Document doc = new Aspose.Note.Document();
```

## Krok 2: Inicializujte objekt třídy stránky

```csharp
// Inicializujte objekt třídy Page
Aspose.Note.Page page = new Aspose.Note.Page(doc);
```

## Krok 3: Nastavte výchozí styl pro text

```csharp
// Výchozí styl pro veškerý text v dokumentu.
ParagraphStyle textStyle = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
```

## Krok 4: Nastavte vlastnosti titulku stránky

```csharp
// Nastavte vlastnosti titulku stránky
page.Title = new Title(doc)
{
    TitleText = new RichText(doc) { Text = "Title text.", ParagraphStyle = textStyle },
    TitleDate = new RichText(doc) { Text = new DateTime(2011, 11, 11).ToString("D", CultureInfo.InvariantCulture), ParagraphStyle = textStyle },
    TitleTime = new RichText(doc) { Text = "12:34", ParagraphStyle = textStyle }
};
```

## Krok 5: Přidejte uzel stránky v dokumentu

```csharp
// Připojit uzel stránky v dokumentu
doc.AppendChildLast(page);
```

## Krok 6: Uložte dokument OneNotu

```csharp
// Uložte dokument OneNotu
string dataDir = "Your Document Directory";
dataDir = dataDir + "CreateDocWithPageTitle_out.one";
doc.Save(dataDir);
```

## Závěr

Gratulujeme! Úspěšně jste vytvořili dokument s titulní stránkou pomocí Aspose.Note pro .NET. Tento kurz poskytuje podrobného průvodce, který vám pomůže integrovat Aspose.Note do vašich aplikací .NET pro programovou správu souborů OneNotu.

## FAQ

### Q1: Mohu přizpůsobit styl textu nadpisu?

A1: Ano, můžete přizpůsobit barvu písma, název písma a velikost písma textu nadpisu podle vašich požadavků.

### Q2: Je Aspose.Note kompatibilní s .NET Core?

Odpověď 2: Ano, Aspose.Note podporuje .NET Core, což vám umožňuje vyvíjet aplikace pro různé platformy.

### Otázka 3: Mohu do dokumentu přidat obrázky a přílohy?

A3: Rozhodně! Aspose.Note poskytuje rozhraní API pro bezproblémové přidávání obrázků, příloh a dalších prvků do dokumentů OneNotu.

### Q4: Podporuje Aspose.Note čtení existujících souborů OneNotu?

Odpověď 4: Ano, Aspose.Note můžete použít ke snadnému čtení, úpravám a manipulaci se stávajícími soubory OneNotu.

### Q5: Kde najdu podporu, pokud narazím na nějaké problémy?

 A5: Podporu a pomoc najdete na[Aspose.Note fórum](https://forum.aspose.com/c/note/28), kde vám odborníci a členové komunity mohou pomoci s vašimi dotazy.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
