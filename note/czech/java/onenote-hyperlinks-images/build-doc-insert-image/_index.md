---
date: 2025-12-20
description: Naučte se, jak přidat obrázek do OneNote pomocí Aspose.Note pro Javu.
  Krok za krokem průvodce tvorbou dokumentů OneNote a programovým vkládáním obrázků.
linktitle: How to add picture to OneNote using Java – Build Document and Insert Image
second_title: Aspose.Note Java API
title: Jak přidat obrázek do OneNote pomocí Javy – vytvořit dokument a vložit obrázek
url: /cs/java/onenote-hyperlinks-images/build-doc-insert-image/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak přidat obrázek do OneNote pomocí Javy – vytvořit dokument a vložit obrázek

## Úvod

V tomto tutoriálu se naučíte **jak přidat obrázek do OneNote** pomocí Aspose.Note Java API. Provedeme vás vytvořením OneNote dokumentu od nuly, vložením obrázku a uložením výsledku jako PDF. Ať už vytváříte nástroj pro reportování, automatizujete zápis poznámek, nebo jen potřebujete programově vložit grafiku, tento průvodce vám poskytne jasnou praktickou cestu.

## Rychlé odpovědi
- **Jaká knihovna je potřeba?** Aspose.Note for Java.
- **Mohu vložit libovolný formát obrázku?** JPEG, PNG, BMP, GIF a další jsou podporovány.
- **Jaké výstupní formáty jsou k dispozici?** Můžete uložit jako OneNote, PDF, XPS, HTML atd.
- **Potřebuji licenci pro produkční použití?** Ano, pro ne‑zkušební použití je vyžadována komerční licence.
- **Je kód multiplatformní?** Rozhodně – Java běží na Windows, Linuxu i macOS.

## Co znamená „přidat obrázek do OneNote“?
Přidání obrázku do OneNote znamená programově vložit soubor s obrázkem na stránku OneNote tak, aby se zobrazoval vedle textu, osnov nebo dalších prvků. Aspose.Note API abstrahuje formát souboru OneNote, což vám umožní soustředit se na obsah místo na podkladovou strukturu XML.

## Proč přidávat obrázek do OneNote pomocí Javy?
- **Automatizace:** Automaticky generovat zápisy ze schůzek se screenshoty.
- **Konzistence:** Zajistit, aby každá stránka měla stejný rozvržení a branding.
- **Integrace:** Kombinovat data z jiných systémů (např. grafy) přímo do notebooků OneNote.
- **Multiplatformní:** Java vám umožní spustit stejný kód na jakémkoli serveru nebo desktopovém prostředí.

## Předpoklady

Než začneme, ujistěte se, že máte následující:

1. **Java Development Kit (JDK)** – jakákoli aktuální verze (8 nebo novější).  
2. **Aspose.Note pro Java knihovna** – stáhněte ji z [webu](https://releases.aspose.com/note/java/).  
3. **IDE** – IntelliJ IDEA, Eclipse nebo jakýkoli jiný Java‑kompatibilní editor, který preferujete.  

## Import balíčků

Začněte importováním potřebných tříd ve vašem Java zdrojovém souboru:

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.HorizontalAlignment;
import com.aspose.note.Image;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.SaveFormat;
```

## Průvodce krok za krokem

### Krok 1: Nastavení dokumentu

Vytvořte nový OneNote dokument a kontejner stránky, kde bude obsah umístěn.

```java
String dataDir = "Your Document Directory";
Document doc = new Document();
Page page = new Page();
```

### Krok 2: Inicializace osnovy

*Osnova* funguje jako kontejner pro prvky jako text a obrázky. Nastavíme její offsety na nulu, aby obsah začínal v levém horním rohu.

```java
Outline outline = new Outline();
outline.setVerticalOffset(0);
outline.setHorizontalOffset(0);
```

### Krok 3: Načtení a zarovnání obrázku

Načtěte obrázek, který chcete vložit, a zarovnejte jej na pravou stranu stránky. Zde skutečně **přidáváme obrázek do OneNote**.

```java
Image image = new Image(null, dataDir + "Input.jpg");
image.setAlignment(HorizontalAlignment.Right);
```

### Krok 4: Připojení obrázku k elementu osnovy

Zabalte obrázek do `OutlineElement`. Tento krok propojí vizuální objekt s hierarchií osnovy dokumentu.

```java
OutlineElement outlineElem = new OutlineElement();
outlineElem.appendChildLast(image);
```

### Krok 5: Sestavení struktury dokumentu

Přidejte element osnovy do osnovy, poté připojte osnovu k stránce a nakonec přidejte stránku do dokumentu.

```java
outline.appendChildLast(outlineElem);
page.appendChildLast(outline);
doc.appendChildLast(page);
```

### Krok 6: Uložení OneNote dokumentu

Uložte dokument na disk. V tomto příkladu exportujeme do PDF, ale můžete také uložit jako nativní OneNote soubor (`.one`) změnou `SaveFormat`.

```java
try {
    doc.save(dataDir + "NewOneNotedocument_out", SaveFormat.Pdf);
} catch (IOException e) {
    e.printStackTrace();
}
```

## Časté problémy a řešení

| Problém | Proč se stane | Řešení |
|---------|----------------|--------|
| **Obrázek se nezobrazuje** | Špatná cesta k souboru nebo nepodporovaný formát. | Ověřte, že `dataDir` ukazuje na správnou složku a použijte podporovaný typ obrázku (JPEG, PNG atd.). |
| **Dokument uložen jako prázdné PDF** | Offsety osnovy jsou nastaveny nesprávně. | Ujistěte se, že jsou zavolány `setVerticalOffset(0)` a `setHorizontalOffset(0)`, nebo upravte offsety tak, aby obsah byl uvnitř hranic stránky. |
| **IOException při ukládání** | Cílová složka neexistuje nebo nemá oprávnění k zápisu. | Vytvořte složku předem nebo spusťte program s odpovídajícími oprávněními. |

## Často kladené otázky

**Q1: Kde mohu najít dokumentaci pro Aspose.Note pro Java?**  
A1: Dokumentaci můžete získat [zde](https://reference.aspose.com/note/java/).

**Q2: Jak si mohu stáhnout Aspose.Note pro Java?**  
A2: Aspose.Note pro Java si můžete stáhnout ze [stránky ke stažení](https://releases.aspose.com/note/java/).

**Q3: Je k dispozici bezplatná zkušební verze Aspose.Note pro Java?**  
A3: Ano, bezplatnou zkušební verzi získáte na [webu](https://releases.aspose.com/).

**Q4: Kde mohu získat podporu pro Aspose.Note pro Java?**  
A4: Pro podporu navštivte [forum Aspose.Note](https://forum.aspose.com/c/note/28).

**Q5: Mohu získat dočasnou licenci pro Aspose.Note pro Java?**  
A5: Ano, dočasnou licenci můžete požádat [zde](https://purchase.aspose.com/temporary-license/).

---

**Poslední aktualizace:** 2025-12-20  
**Testováno s:** Aspose.Note for Java 24.12 (nejnovější)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}