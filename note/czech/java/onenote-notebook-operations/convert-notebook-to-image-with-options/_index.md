---
date: 2025-12-28
description: Naučte se, jak **převést OneNote na obrázek** a nastavit rozlišení obrázku
  v Javě pomocí Aspose.Note. Tento krok‑za‑krokem průvodce také ukazuje, jak exportovat
  soubory OneNote PNG.
linktitle: Convert OneNote to Image with Options - Aspose.Note
second_title: Aspose.Note Java API
title: Převod OneNote na obrázek s možnostmi – Aspose.Note
url: /cs/java/onenote-notebook-operations/convert-notebook-to-image-with-options/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Převod OneNote na obrázek s možnostmi – Aspose.Note

## Úvod

V tomto tutoriálu se naučíte, jak **převést OneNote na obrázek** s řadou možností pomocí Aspose.Note pro Java. Ať už potřebujete vysoce rozlišený PNG pro reportování nebo rychlou JPEG miniaturu, níže uvedené kroky vám přesně ukážou, jak to dosáhnout a integrovat proces do vašich Java aplikací.

## Rychlé odpovědi
- **Co znamená „převod OneNote na obrázek“?** Převádí celý OneNote notebook na rastrové soubory obrázků (PNG, JPEG atd.).
- **Jaký formát je doporučen pro bezztrátovou kvalitu?** PNG, protože zachovává všechny detaily bez kompresních artefaktů.
- **Jak mohu nastavit rozlišení obrázku v Javě?** Použijte `ImageSaveOptions.setResolution(int dpi)` přes `NotebookImageSaveOptions`.
- **Mohu exportovat OneNote notebook jako PNG v jednom kroku?** Ano, Aspose.Note poskytuje jediný volání `save` s příslušnými možnostmi.
- **Potřebuji licenci pro produkční použití?** Pro produkci je vyžadována komerční licence; pro vyhodnocení je k dispozici bezplatná zkušební verze.

## Co je „převod OneNote na obrázek“?
Převod OneNote notebooku na obrázek znamená vykreslení každé stránky notebooku jako bitmapového souboru. To je užitečné pro vytváření statických náhledů, archivaci obsahu nebo vkládání stránek notebooku do reportů, kde není podporován původní formát OneNote.

## Proč použít Aspose.Note pro Java?
- **Plná kontrola** nad výstupním formátem, rozlišením a barevnou hloubkou.  
- **Žádná závislost na Microsoft Office** – funguje v jakémkoli serverovém Java prostředí.  
- **Podporuje složité notebooky** s vloženými soubory, inkoustem a bohatým textem.

## Předpoklady

1. **Java Development Kit (JDK)** – verze 8 nebo vyšší.  
2. **Aspose.Note for Java JAR soubory** – stáhněte nejnovější knihovnu z [here](https://releases.aspose.com/note/java/) a přidejte ji do classpath vašeho projektu.  

## Import balíčků

Nejprve importujte třídy, které budeme potřebovat pro načtení notebooku a nastavení výstupu obrázku.

```java
import java.io.IOException;

import com.aspose.note.ImageSaveOptions;
import com.aspose.note.Notebook;
import com.aspose.note.NotebookImageSaveOptions;
import com.aspose.note.SaveFormat;
```

## Krok 1: Načtení notebooku

Načtěte OneNote notebook, který chcete převést. Nahraďte cestu umístěním vašeho souboru `.onetoc2`.

```java
String dataDir = "Your Document Directory";
// Load a OneNote Notebook
Notebook notebook = new Notebook(dataDir + "test.onetoc2");
```

## Krok 2: Nastavení možností uložení (Jak **nastavit rozlišení obrázku v Javě**)

Vytvořte instanci `NotebookImageSaveOptions`, vyberte výstupní formát a zadejte požadované rozlišení. V tomto příkladu používáme PNG s 400 dpi.

```java
NotebookImageSaveOptions notebookSaveOptions = new NotebookImageSaveOptions(SaveFormat.Png);

ImageSaveOptions documentSaveOptions = notebookSaveOptions.getDocumentSaveOptions();

documentSaveOptions.setResolution(400);
```

> **Tip:** Pro rychlejší zpracování velkých notebooků snižte rozlišení (např. 150 dpi). Zvýšte jej pro grafiku připravenou k tisku.

## Krok 3: Uložení notebooku jako obrázek (Jak **exportovat OneNote PNG**)

Definujte název výstupního souboru a zavolejte `save`. Stejné možnosti jsou použity na každou stránku v notebooku.

```java
dataDir = dataDir + "ExportNotebooktoImagewithOptions_out.png";

// Save the Notebook
notebook.save(dataDir, notebookSaveOptions);
```

Výše uvedený kód vygeneruje soubor PNG (nebo sérii souborů PNG, jeden na stránku) s nastaveným rozlišením.

## Časté problémy a řešení

| Problém | Řešení |
|-------|----------|
| **OutOfMemoryError** u velkých notebooků | Zvyšte velikost haldy JVM (`-Xmx2g`) nebo snižte rozlišení. |
| **Prázdné stránky ve výstupu** | Ujistěte se, že notebook není chráněn heslem; použijte `Notebook.load(path, password)` pokud je potřeba. |
| **Nepodporovaný formát obrázku** | Používejte pouze `SaveFormat.Png`, `SaveFormat.Jpeg` nebo `SaveFormat.Bmp` – ostatní formáty nejsou pro export notebooku podporovány. |

## Často kladené otázky

**Q: Dokáže Aspose.Note zpracovat složité OneNote soubory?**  
A: Ano, efektivně zpracovává notebooky s vloženými soubory, inkoustovými anotacemi a bohatým formátováním.

**Q: Je Aspose.Note pro Java snadno integrovat do existujících projektů?**  
A: Rozhodně. API je přímočaré a stačí přidat JAR do classpath.

**Q: Mohu přizpůsobit výstup obrázku při převodu notebooku?**  
A: Ano. Můžete nastavit rozlišení, formát a dokonce i barevnou hloubku pomocí `ImageSaveOptions`.

**Q: Nabízí Aspose.Note podporu pro vývojáře?**  
A: Ano. Aspose poskytuje rozsáhlou dokumentaci, fóra a rychlé podpůrné kanály.

**Q: Je k dispozici bezplatná zkušební verze Aspose.Note pro Java?**  
A: Ano, můžete si stáhnout zkušební verzi z [here](https://releases.aspose.com/).

---

**Poslední aktualizace:** 2025-12-28  
**Testováno s:** Aspose.Note 24.11 pro Java  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}