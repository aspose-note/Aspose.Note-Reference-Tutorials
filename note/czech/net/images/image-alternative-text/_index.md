---
date: 2026-04-09
description: Naučte se snadno přidávat alternativní text k obrázkům v Aspose.Note
  pro .NET. Zvyšte přístupnost a zlepšete uživatelský zážitek pomocí tohoto krok‑za‑krokem
  průvodce.
keywords:
- how to add alt text
- add alternative text image
- append image to page
linktitle: Přidat alternativní text k obrázkům v Aspose.Note
second_title: Aspose.Note .NET API
title: Jak přidat alternativní text k obrázkům v Aspose.Note
url: /cs/net/images/image-alternative-text/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak přidat alternativní text k obrázkům v Aspose.Note

## Úvod

Pokud potřebujete **jak přidat alternativní text** k obrázkům ve svých dokumentech ve stylu OneNote, jste na správném místě. Tento tutoriál vás provede přesné kroky, jak pomocí Aspose.Note pro .NET přidat alternativní text (jak titul, tak popis) k obrázku. Přidání alternativního textu nejen zvyšuje přístupnost pro uživatele čteček obrazovky, ale také zlepšuje SEO pro jakýkoli webově publikovaný obsah, který později vkládá tyto obrázky.

## Rychlé odpovědi
- **Co znamená „alt text“?** Textový popis, který představuje obrázek, když nelze zobrazit.  
- **Proč použít Aspose.Note pro alt text?** Poskytuje jednoduché API pro nastavení jak titulku, tak popisu programově.  
- **Jaké jsou předpoklady?** .NET vývojové prostředí, Visual Studio a Aspose.Note pro .NET nainstalované.  
- **Mohu přidat alt text k existujícím obrázkům?** Ano – můžete načíst objekt obrázku, nastavit jeho vlastnosti a dokument uložit.  
- **Kam se ukládá výstup?** Do cesty, kterou určíte pomocí `document.Save(...)`.

## Co je „jak přidat alt text“ v Aspose.Note?

Přidání alt textu znamená přiřazení vlastností `AlternativeTextTitle` a `AlternativeTextDescription` objektu `Image`. Tyto vlastnosti jsou čteny čtečkami obrazovky a dalšími asistenčními technologiemi, aby předaly význam obrázku.

## Proč přidat alternativní text k obrázku ve vašem dokumentu?

- **Soulad s přístupností** – splňuje směrnice WCAG a Section 508.  
- **Vylepšené SEO** – vyhledávače indexují popisný text.  
- **Lepší uživatelská zkušenost** – uživatelé s vypnutými obrázky stále rozumí obsahu.

## Požadavky

Before you begin, make sure you have:

- Základní znalost C# a .NET vývoje.  
- Nainstalované Visual Studio na vašem počítači.  
- Aspose.Note pro .NET stažený a referencovaný ve vašem projektu – můžete jej získat [zde](https://releases.aspose.com/note/net/).  
- Soubor obrázku (např. `image.jpg`), který chcete vložit.

## Importovat jmenné prostory

Nejprve zahrňte jmenné prostory potřebné pro práci se soubory a objekty Aspose.Note.

```csharp
using System.IO;
using Aspose.Note;
using System.Collections.Generic;
using System.Drawing;
using System;
```

## Krok 1: Inicializovat dokument a stránku

Vytvořte novou instanci `Document` a přidejte `Page`, na kterou bude obrázek umístěn.

```csharp
var document = new Document();
var page = new Page(document);
```

## Krok 2: Načíst obrázek

Odkazujte na složku, která obsahuje váš obrázek, a vytvořte objekt `Image`.

```csharp
string dataDir = "Your Document Directory";
var image = new Image(document, dataDir + "image.jpg");
```

## Krok 3: Nastavit alternativní text

Zde **přidáváme alternativní text k obrázku** vyplněním polí titulku i popisu.

```csharp
image.AlternativeTextTitle = "This is an image's title!";
image.AlternativeTextDescription = "And this is an image's description!";
```

## Krok 4: Připojit obrázek ke stránce

Nyní **připojujeme obrázek ke stránce** pomocí metody `AppendChildLast`.

```csharp
page.AppendChildLast(image);
```

## Krok 5: Uložit dokument

Zadejte název výstupního souboru a uložte OneNote dokument.

```csharp
dataDir = dataDir + "ImageAlternativeText_out.one";
document.Save(dataDir);
```

## Krok 6: Zobrazit zprávu o úspěchu

Jednoduchá zpráva v konzoli potvrzuje, že operace byla úspěšná.

```csharp
Console.WriteLine("\nImage alternative text setup successfully.\nFile saved at " + dataDir); 
```

## Časté problémy a řešení

| Problém | Příčina | Řešení |
|-------|-------|-----|
| **Alt text se nezobrazuje** | `AlternativeTextTitle` nebo `AlternativeTextDescription` jsou prázdné | Ujistěte se, že jsou před uložením nastaveny obě vlastnosti. |
| **Soubor nenalezen** | Špatná cesta `dataDir` | Použijte absolutní cestu nebo ověřte, že relativní složka existuje. |
| **Výjimka při ukládání** | Nedostatečná oprávnění k zápisu | Spusťte Visual Studio jako administrátor nebo vyberte složku s oprávněním k zápisu. |

## Často kladené otázky

### Q1: Proč je alternativní text důležitý pro obrázky?

A1: Alternativní text poskytuje textový popis obrázků, což je činí přístupnými pro uživatele, kteří používají čtečky obrazovky nebo mají obrázky vypnuté.

### Q2: Mohu přidat alternativní text k existujícím obrázkům v dokumentu?

A2: Ano, můžete snadno přidat alternativní text k obrázkům, které jsou již v dokumentu, pomocí Aspose.Note pro .NET.

### Q3: Je Aspose.Note kompatibilní s jinými .NET knihovnami?

A3: Aspose.Note se bez problémů integruje s dalšími .NET knihovnami a poskytuje komplexní funkce pro manipulaci s dokumenty.

### Q4: Jak mohu získat podporu pro Aspose.Note?

A4: Podporu pro Aspose.Note můžete získat návštěvou [fóra Aspose.Note](https://forum.aspose.com/c/note/28), kde můžete klást otázky a najít řešení.

### Q5: Je k dispozici bezplatná zkušební verze Aspose.Note?

A5: Ano, můžete získat bezplatnou zkušební verzi Aspose.Note návštěvou [zde](https://releases.aspose.com/).

## Závěr

Přidání alt textu k obrázkům je malý krok, který má velký dopad na přístupnost, SEO a celkovou uživatelskou zkušenost. S Aspose.Note pro .NET je proces jednoduchý – stačí nastavit vlastnosti `AlternativeTextTitle` a `AlternativeTextDescription`, připojit obrázek a dokument uložit.

---

**Poslední aktualizace:** 2026-04-09  
**Testováno s:** Aspose.Note 24.11 for .NET  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}