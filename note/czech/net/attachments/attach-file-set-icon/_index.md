---
date: 2026-04-03
description: Naučte se, jak nastavit vlastní ikonu a připojit soubory v Aspose.Note
  pro .NET, včetně ukládání souborů OneNote a používání obrázků jako ikon.
keywords:
- set custom icon
- attach multiple files
- use image as icon
- save onenote file
- embed text file
linktitle: Připojit soubor a nastavit ikonu v Aspose.Note
second_title: Aspose.Note .NET API
title: Nastavit vlastní ikonu a připojit soubor v Aspose.Note
url: /cs/net/attachments/attach-file-set-icon/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Nastavte vlastní ikonu a připojte soubor v Aspose.Note

## Úvod

Pokud potřebujete **nastavit vlastní ikonu** pro přílohu na stránce OneNote, Aspose.Note pro .NET to usnadňuje. Připojením souboru a přiřazením obrázku jako jeho ikony můžete vytvořit bohatší, informativnější poznámky, které vypadají přesně tak, jak chcete. V tomto tutoriálu projdeme kompletním procesem – od vytvoření nového dokumentu, přidání přílohy, aplikování vlastní JPEG ikony až po uložení souboru OneNote.

## Rychlé odpovědi
- **Co znamená „nastavit vlastní ikonu“?** Umožňuje vám nahradit výchozí miniaturu přílohy obrázkem, který poskytnete.  
- **Mohu připojit více souborů?** Ano, opakujte kroky pro připojení pro každý soubor.  
- **Jaké formáty obrázků jsou podporovány pro ikony?** Jakýkoli formát kompatibilní s .NET, například JPEG, PNG, BMP nebo GIF.  
- **Potřebuji licenci?** Pro produkční použití je vyžadována platná licence Aspose.Note; pro hodnocení stačí bezplatná zkušební verze.  
- **Jak uložit soubor OneNote?** Použijte `Document.Save()` a zadejte cestu k souboru s příponou *.one*.

## Co znamená „nastavit vlastní ikonu“ v Aspose.Note?
Nastavení vlastní ikony znamená přiřazení konkrétního obrázku (např. JPEG) k reprezentaci připojeného souboru na stránce OneNote. To zlepšuje vizuální vodítka pro uživatele a může být použito k zobrazení loga typu souboru nebo značkové grafiky.

## Proč nastavit vlastní ikonu pro přílohy?
- **Lepší vizuální kontext:** Uživatelé okamžitě rozpoznají typ nebo účel připojeného souboru.  
- **Konzistence značky:** Použijte logo vaší společnosti jako ikonu pro všechny související dokumenty.  
- **Vylepšená uživatelská zkušenost:** Poznámky vypadají uhlazeně a profesionálně, zejména ve sdílených sešitech.

## Požadavky

- Základní znalost programování v C#.
- Nainstalovaná knihovna Aspose.Note pro .NET.
- Visual Studio (nebo jakékoli IDE kompatibilní s .NET) připravené pro vývoj.

## Importování jmenných prostorů

Nejprve načtěte požadované jmenné prostory, aby byly k dispozici pro práci se soubory, obrázky a objekty OneNote.

```csharp
using System.IO;
using Aspose.Note;
using System;
using System.Collections.Generic;
using System.Drawing.Imaging;
```

## Průvodce krok za krokem: připojení souboru a nastavení jeho ikony

### Krok 1: Vytvoření objektu Document
Nová instance `Document` představuje soubor OneNote, který budete vytvářet.

```csharp
Document doc = new Document();
```

### Krok 2: Inicializace objektu Page
Každý soubor OneNote obsahuje jednu nebo více stránek. Zde vytvoříme první stránku.

```csharp
Aspose.Note.Page page = new Aspose.Note.Page(doc);
```

### Krok 3: Inicializace objektu Outline
Outlines fungují jako kontejnery pro obsahové bloky na stránce.

```csharp
Outline outline = new Outline(doc);
```

### Krok 4: Inicializace objektu OutlineElement
Tento prvek bude obsahovat připojený soubor a jeho vlastní ikonu.

```csharp
OutlineElement outlineElem = new OutlineElement(doc);
```

### Krok 5: Načtení obrázku ikony a inicializace objektu AttachedFile
Otevřeme stream obrázku (vlastní ikonu) a ukážeme na soubor, který chceme vložit.

```csharp
string dataDir = "Your Document Directory";
using (var stream = File.OpenRead(dataDir + "icon.jpg"))
{
    AttachedFile attachedFile = new AttachedFile(doc, dataDir + "attachment.txt", stream, ImageFormat.Jpeg);
}
```

> **Tip:** Nahraďte `ImageFormat.Jpeg` za `ImageFormat.Png`, pokud dáváte přednost PNG ikoně.

### Krok 6: Připojení souboru k OutlineElement
Nyní se soubor (s jeho ikonou) stane podřízeným prvkem outline elementu.

```csharp
outlineElem.AppendChildLast(attachedFile);
```

### Krok 7: Připojení OutlineElement k Outline
Tím se prvek vloží do kontejneru outline.

```csharp
outline.AppendChildLast(outlineElem);
```

### Krok 8: Připojení Outline k Page
Připojte celou hierarchii outline k stránce.

```csharp
page.AppendChildLast(outline);
```

### Krok 9: Připojení Page k Document
Přidejte dokončenou stránku do struktury dokumentu.

```csharp
doc.AppendChildLast(page);
```

### Krok 10: Uložení dokumentu OneNote
Nakonec zapište dokument na disk jako soubor s příponou *.one*.

```csharp
dataDir = dataDir + "AttachFileAndSetIcon_out.one";
doc.Save(dataDir);
```

## Běžné případy použití
- **Vkládání smluv:** Připojte PDF a použijte ikonu s logem smlouvy.  
- **Sdílení útržků kódu:** Připojte soubor `.txt` s vlastní ikonou „kód“.  
- **Dokumentace projektu:** Připojte návrhové soubory a nastavte miniaturu odpovídající typu souboru.

## Běžné problémy a řešení
| Problém | Řešení |
|-------|----------|
| **Ikona se nezobrazuje** | Ověřte, že formát obrázku odpovídá `ImageFormat`, který jste zadali (např. JPEG vs PNG). |
| **Chyby cesty k souboru** | Použijte `Path.Combine(dataDir, \"file.ext\")` k zabránění problémům s chybějícími lomítky. |
| **Velké přílohy způsobují zpomalení výkonu** | Předem soubor komprimujte nebo rozdělte na více menších příloh. |

## Často kladené otázky

**Q: Mohu připojit více souborů k jedné poznámce pomocí Aspose.Note pro .NET?**  
A: Ano. Jednoduše opakujte blok „Načtení obrázku ikony a inicializace objektu AttachedFile“ pro každý soubor a připojte každý `AttachedFile` ke stejnému `OutlineElement` nebo vytvořte samostatné prvky.

**Q: Je možné nastavit vlastní ikony pro souborové přílohy?**  
A: Rozhodně. Konstruktor `AttachedFile` vám umožní předat stream obrázku a specifikovat formát obrázku, což vám dává plnou kontrolu nad ikonou.

**Q: Podporuje Aspose.Note další formáty obrázků pro nastavení ikon?**  
A: Ano. Kromě JPEG můžete použít PNG, BMP, GIF nebo jakýkoli formát podporovaný `System.Drawing.Imaging.ImageFormat`.

**Q: Mohu připojit soubory z externích URL?**  
A: I když Aspose.Note pracuje s lokálními streamy, můžete soubor stáhnout pomocí `HttpClient`, uložit jej do `MemoryStream` a poté předat tento stream konstruktoru `AttachedFile`.

**Q: Existuje limit velikosti pro souborové přílohy?**  
A: Aspose.Note sám o sobě neklade pevný limit, ale velmi velké soubory mohou ovlivnit využití paměti a výkon. Zvažte kompresi velkých příloh.

---

**Poslední aktualizace:** 2026-04-03  
**Testováno s:** Aspose.Note 24.11 pro .NET  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}