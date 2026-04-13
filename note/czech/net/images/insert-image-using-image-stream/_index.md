---
date: 2026-04-13
description: Naučte se, jak přidávat obrázky do dokumentů OneNote pomocí streamů obrázků
  v .NET s Aspose.Note. Tento krok‑za‑krokem průvodce pokrývá načítání obrázků ze
  streamu, jejich přidávání do osnov a ukládání souboru.
keywords:
- add image to onenote
- how to insert image
- load image from stream
- append image to outline
- image stream .net
linktitle: Přidat obrázek do OneNote pomocí proudu obrázku s využitím Aspose.Note
second_title: Aspose.Note .NET API
title: Přidat obrázek do OneNote pomocí Image Stream s využitím Aspose.Note
url: /cs/net/images/insert-image-using-image-stream/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Přidání obrázku do OneNote pomocí Image Stream s Aspose.Note

## Úvod

V tomto tutoriálu se dozvíte **jak přidat obrázek do OneNote** dokumentů načtením obrázku ze streamu a připojením jej k obrysu pomocí Aspose.Note pro .NET. Ať už vytváříte nástroj pro reportování, aplikaci pro psaní poznámek nebo automatizujete dokumentaci, vkládání obrázků programově učiní vaše soubory OneNote mnohem poutavější a užitečnější.

## Rychlé odpovědi
- **Jaká knihovna je potřeba?** Aspose.Note pro .NET (k dispozici bezplatná zkušební verze).  
- **Které verze .NET jsou podporovány?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6+.  
- **Mohu načíst obrázky ze streamu?** Ano – použijte `FileStream` nebo libovolnou implementaci `Stream`.  
- **Jak mohu ovládat zarovnání obrázku?** Nastavte vlastnost `Alignment` (např. `HorizontalAlignment.Right`).  
- **Jaký formát souboru je vytvořen?** Soubor OneNote (`.one`), který lze otevřít v Microsoft OneNote.

## Co znamená “přidat obrázek do OneNote”?

Přidání obrázku do souboru OneNote znamená vložení vizuálního prvku přímo do hierarchie obsahu stránky. S Aspose.Note pracujete s objekty jako `Document`, `Page`, `Outline` a `OutlineElement`. Vložení objektu `Image` do `OutlineElement` způsobí, že se obrázek stane součástí rozvržení stránky OneNote.

## Proč použít Aspose.Note pro vkládání obrázků?

- **Není vyžadována instalace Office** – generujte nebo upravujte soubory OneNote na serveru.  
- **Plná kontrola nad rozvržením** – zarovnávejte, měňte velikost a umisťujte obrázky přesně tam, kde je potřebujete.  
- **Přátelské ke streamům** – funguje s libovolným `Stream`, ideální pro cloudové úložiště nebo scénáře pouze v paměti.  
- **Cross‑platform** – kompatibilní s .NET runtime na Windows, Linuxu a macOS.

## Předpoklady

Než se pustíme dál, ujistěte se, že máte:

1. **Vývojové prostředí** – Visual Studio 2022 nebo jakékoli IDE kompatibilní s .NET.  
2. **Knihovna Aspose.Note** – stáhněte ji z oficiální stránky [here](https://releases.aspose.com/note/net/).  
3. **Obrázkové soubory** – alespoň jeden obrázek (JPG, PNG, BMP, GIF nebo TIFF), který chcete vložit.  
4. **Základní znalost C#** – znalost práce se soubory a objektově orientovaného kódu.

## Importování jmenných prostorů
Nejprve importujte jmenné prostory, které poskytují přístup ke třídám Aspose.Note a standardním .NET I/O utilitám.

```csharp
using System.IO;
using Aspose.Note;
using System.Collections.Generic;
using System.Drawing;
using System;
```

Nyní projděme proces krok za krokem.

### Krok 1: Inicializace objektu Document
Začínáme vytvořením nové instance `Document`, která bude obsahovat soubor OneNote.

```csharp
// The path to the documents directory.
string dataDir = "Your Document Directory";
Document doc = new Document();
```

### Krok 2: Vytvoření objektu Page
Soubor OneNote se skládá z jedné nebo více stránek. Zde vytvoříme novou stránku, která bude hostovat náš obsah.

```csharp
Aspose.Note.Page page = new Aspose.Note.Page(doc);
```

### Krok 3: Inicializace objektů Outline a OutlineElement
Obrysy jsou kontejnery pro bohatý obsah (text, obrázky, tabulky). `OutlineElement` je podřízený prvek, který skutečně obsahuje položky.

```csharp
Outline outline1 = new Outline(doc);
OutlineElement outlineElem1 = new OutlineElement(doc);
```

### Krok 4: Načtení obrázku ze streamu
Pomocí `FileStream` (nebo libovolného `Stream`) načteme soubor obrázku a vytvoříme objekt `Image`. Zde se ukáže síla klíčového slova **load image from stream**.

```csharp
using (FileStream fs = File.OpenRead(dataDir + "image.jpg"))
{
    Aspose.Note.Image image1 = new Aspose.Note.Image(doc, "Penguins.jpg", fs)
    {
        Alignment = HorizontalAlignment.Right
    };
    outlineElem1.AppendChildLast(image1);
}
```

### Krok 5: Připojení obrázku k OutlineElement
Obrázek je nyní součástí `OutlineElement`. Tento krok demonstruje funkci **append image to outline**.

```csharp
outlineElem1.AppendChildLast(image1);
```

### Krok 6: Připojení OutlineElement k Outline
Nyní připojíme prvek (s obrázkem) k obalujícímu kontejneru Outline.

```csharp
outline1.AppendChildLast(outlineElem1);
```

### Krok 7: Připojení Outline k Page
Outline, který obsahuje obrázek, je přidán na stránku.

```csharp
page.AppendChildLast(outline1);
```

### Krok 8: Připojení Page k Document
Po připravení stránky ji vložíme do hierarchie dokumentu.

```csharp
doc.AppendChildLast(page);
```

### Krok 9: Uložení dokumentu
Nakonec uložíme soubor OneNote na disk. Výsledný soubor lze otevřít v Microsoft OneNote.

```csharp
doc.Save(dataDir + "BuildDocAndInsertImageUsingImageStream_out.one");
```

## Časté problémy a řešení

| Problém | Proč se vyskytuje | Řešení |
|-------|----------------|-----|
| **Obrázek se nezobrazuje** | Stream byl uzavřen před tím, než byl obrázek přidán. | Udržujte blok `using` kolem volání `AppendChildLast` (jak je ukázáno). |
| **Nesprávné zarovnání** | Vlastnost `Alignment` nebyla nastavena nebo byla později přepsána. | Nastavte `Alignment` při vytváření `Image` nebo upravte `image1.Alignment` před připojením. |
| **Není podporovaný formát obrázku** | Pokus o načtení formátu, který Aspose.Note nepozná. | Předtím převést obrázek na JPG, PNG, BMP, GIF nebo TIFF. |
| **Chyby cesty k souboru** | `dataDir` ukazuje na neexistující složku. | Použijte `Path.Combine` a ověřte, že složka existuje před spuštěním. |

## Často kladené otázky

**Q: Mohu pomocí této metody vložit do jednoho dokumentu více obrázků?**  
A: Ano. Stačí opakovat kroky *Load Image from Stream* a *Append Image to OutlineElement* pro každý obrázek.

**Q: Podporuje Aspose.Note další formáty obrázků kromě JPG?**  
A: Ano. PNG, BMP, GIF a TIFF jsou všechny podporovány.

**Q: Mohu přizpůsobit zarovnání a velikost vložených obrázků?**  
A: Ano. Kromě `Alignment` můžete nastavit vlastnosti `Width`, `Height` a `Scale` u objektu `Image`.

**Q: Je Aspose.Note kompatibilní se všemi verzemi .NET?**  
A: Funguje s .NET Framework 4.5+, .NET Core 3.1+, .NET 5 a .NET 6+.

**Q: Kde mohu najít další zdroje a podporu pro Aspose.Note?**  
A: Kompletní dokumentaci, fóra a podporu najdete na [Aspose Forum](https://forum.aspose.com/c/note/28).

**Poslední aktualizace:** 2026-04-13  
**Testováno s:** Aspose.Note 24.11 for .NET  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}