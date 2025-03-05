---
title: Uživatelská zpětná volání v Aspose.Note
linktitle: Uživatelská zpětná volání v Aspose.Note
second_title: Aspose.Note .NET API
description: Zjistěte, jak implementovat zpětná volání šetřící uživatele v Aspose.Note pro .NET, abyste přizpůsobili ukládání písem, CSS a obrázků.
type: docs
weight: 31
url: /cs/net/loading-and-saving-operations/user-saving-callbacks/
---
## Úvod

tomto tutoriálu prozkoumáme, jak implementovat zpětná volání šetřící uživatele v Aspose.Note pro .NET. Tato zpětná volání vám umožňují přizpůsobit proces ukládání poskytnutím háčků pro zásah v různých fázích, jako je ukládání písem, šablon stylů CSS a obrázků. Využitím těchto zpětných volání můžete přizpůsobit chování při ukládání tak, aby vyhovovalo vašim konkrétním požadavkům, a zvýšit tak flexibilitu a kontrolu nad výstupem.

## Předpoklady

Než se ponoříte do implementace zpětných volání šetřících uživatele v Aspose.Note, ujistěte se, že máte splněny následující předpoklady:

1.  Aspose.Note for .NET SDK: Stáhněte si a nainstalujte Aspose.Note for .NET SDK ze[stránka ke stažení](https://releases.aspose.com/note/net/).
   
2. Vývojové prostředí: Mějte nastavené vhodné vývojové prostředí, jako je Visual Studio nebo jakékoli jiné vývojové prostředí .NET.

## Import jmenných prostorů

Chcete-li začít, ujistěte se, že jste do projektu importovali potřebné jmenné prostory, abyste získali přístup k požadovaným třídám a metodám z knihovny Aspose.Note:

```csharp
using Aspose.Note.Saving.Html;
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Text;
```

Nyní si rozdělme implementaci zpětných volání, která šetří uživatele, do několika kroků:

## Krok 1: Definujte vlastnosti zpětného volání

```csharp
public string RootFolder { get; set; }
public bool KeepCssStreamOpened { get; set; }
public string CssFolder { get; set; }
public Stream CssStream { get; private set; }
public string FontsFolder { get; set; }
public string ImagesFolder { get; set; }
```

Zde definujeme různé vlastnosti pro určení kořenové složky, složky CSS, složky písem, složky obrázků a další relevantní nastavení.

## Krok 2: Implementujte zpětné volání pro ukládání písma

```csharp
public void FontSaving(FontSavingArgs args)
{
    string uri;
    Stream stream;
    this.CreateResourceInFolder(this.FontsFolder, args.FileName, out uri, out stream);
    args.Stream = stream;
    args.Uri = Path.Combine("..", uri).Replace("\\", "\\\\");
}
```

 V tomto kroku implementujeme`FontSaving` metoda zpětného volání pro zpracování ukládání písem. Vytvoří prostředek v zadané složce písem a podle toho přiřadí stream a URI.

## Krok 3: Implementujte CSS Saving Callback

```csharp
public void CssSaving(CssSavingArgs args)
{
    string uri;
    Stream stream;
    this.CreateResourceInFolder(this.CssFolder, args.FileName, out uri, out stream);
    args.Stream = this.CssStream = stream;
    args.KeepStreamOpen = this.KeepCssStreamOpened;
    args.Uri = uri;
}
```

 Zde definujeme`CssSaving` metoda zpětného volání pro správu ukládání šablon stylů CSS. Vytvoří prostředek v zadané složce CSS a podle toho nastaví stream, URI a další vlastnosti.

## Krok 4: Implementujte zpětné volání funkce Image Saving

```csharp
public void ImageSaving(ImageSavingArgs args)
{
    string uri;
    Stream stream;
    this.CreateResourceInFolder(this.ImagesFolder, args.FileName, out uri, out stream);
    args.Stream = stream;
    args.Uri = uri;
}
```

 Nakonec implementujeme`ImageSaving` metoda zpětného volání pro zpracování ukládání obrázků. Podobně jako v předchozích krocích vytvoří prostředek v určené složce obrázků a přiřadí stream a identifikátor URI.

## Závěr

tomto tutoriálu jsme se naučili, jak implementovat zpětná volání šetřící uživatele v Aspose.Note pro .NET. Pomocí uvedených kroků můžete přizpůsobit proces ukládání písem, šablon stylů CSS a obrázků, což umožňuje větší flexibilitu a kontrolu nad výstupem.

## Nejčastější dotazy

### Q1: Mohu tato zpětná volání použít k přizpůsobení dalších aspektů procesu ukládání?

Odpověď 1: Ano, můžete tato zpětná volání rozšířit nebo implementovat další a přizpůsobit různé aspekty procesu ukládání podle svých potřeb.

### Otázka 2: Je Aspose.Note for .NET kompatibilní s jinými frameworky .NET?

Odpověď 2: Ano, Aspose.Note pro .NET je kompatibilní s různými rozhraními .NET, včetně .NET Core a .NET Standard.

### Q3: Jak mohu zpracovat chyby nebo výjimky během procesu ukládání?

Odpověď 3: V rámci každé metody zpětného volání můžete začlenit mechanismy zpracování chyb, abyste mohli bez problémů zpracovat všechny chyby nebo výjimky, které se mohou vyskytnout.

### Otázka 4: Existují při používání těchto zpětných volání nějaká hlediska týkající se výkonu?

A4: I když tato zpětná volání nabízejí flexibilitu, zajistěte jejich efektivní implementaci, abyste se vyhnuli jakékoli režii na výkon, zejména při práci s velkými dokumenty nebo zdroji.

### Q5: Mohu dynamicky změnit chování při ukládání na základě vstupu uživatele nebo jiných podmínek?

Odpověď 5: Ano, do metod zpětného volání můžete začlenit podmíněnou logiku a dynamicky upravit chování při ukládání na základě různých faktorů.