---
date: 2026-03-21
description: Naučte se, jak zploštit poznámkový blok převodem OneNote na PNG pomocí
  Aspose.Note pro Javu. Tento průvodce pokrývá nastavení rozlišení obrázku, uložení
  OneNote jako obrázku a efektivní zploštění poznámkových bloků.
linktitle: How to Flatten Notebook – Convert OneNote to PNG
second_title: Aspose.Note Java API
title: Jak zploštit poznámkový blok – převést OneNote na PNG
url: /cs/java/onenote-notebook-operations/convert-notebook-to-flattened-image/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak zploštit poznámkový blok – převést OneNote na PNG

## Úvod

V tomto tutoriálu objevíte **jak zploštit poznámkový blok** převodem poznámkového bloku OneNote na vysoce kvalitní PNG obrázek pomocí Aspose.Note pro Java. Ať už potřebujete vložit snímek poznámkového bloku do zprávy, sdílet jen‑pro‑čtení pohled s kolegy, nebo archivovat souladný obrázek, tento krok‑za‑krokem průvodce vám přesně ukáže, jak uložit OneNote jako obrázek při řízení rozlišení.

## Rychlé odpovědi
- **Co znamená „flatten notebook“?** Sloučí všechny prvky stránky do jednoho rastrového obrazu.  
- **Jaký formát se používá?** PNG je výchozí, poskytuje bezztrátovou kvalitu.  
- **Mohu změnit DPI?** Ano, použijte `setResolution` na `ImageSaveOptions`.  
- **Potřebuji licenci?** Bezplatná zkušební verze funguje pro hodnocení; pro produkční nasazení je vyžadována komerční licence.  
- **Je to podporováno na všech operačních systémech?** Java API běží kdekoliv, kde běží Java.  

## Co je převod OneNote na PNG?

Převod OneNote na PNG vytvoří bitmapovou reprezentaci každé stránky v poznámkovém bloku, zachovávající text, kresby a vložené objekty v jediném souboru obrázku. To je zvláště užitečné pro dokumentaci, prezentace nebo archivaci pro shodu.

## Proč převádět OneNote na PNG pomocí Aspose.Note?

- **Plná věrnost** – Všechny vizuální prvky jsou zachovány.  
- **Výstup v jednom souboru** – Není potřeba spravovat soubory pro jednotlivé stránky.  
- **Přizpůsobitelná rozlišení** – Nastavte DPI podle požadavků na kvalitu.  
- **Bez instalace Office** – Funguje zcela nezávisle na Microsoft OneNote.  

## Požadavky

Před zahájením se ujistěte, že máte následující:

1. Java Development Kit (JDK) nainstalovaný ve vašem systému.  
2. Knihovna Aspose.Note pro Java stažená a nastavená ve vašem Java projektu. Knihovnu můžete stáhnout [zde](https://releases.aspose.com/note/java/).  
3. Základní znalost programování v Javě.  

## Import balíčků

Pro zahájení je potřeba importovat nezbytné balíčky z Aspose.Note pro Java:

```java
import java.io.IOException;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.Notebook;
import com.aspose.note.NotebookImageSaveOptions;
import com.aspose.note.SaveFormat;
```

## Průvodce krok za krokem

### Krok 1: Nastavení adresáře dokumentu

Nejprve definujte adresář, kde se nachází soubor vašeho poznámkového bloku:

```java
String dataDir = "Your Document Directory";
```

Nahraďte `"Your Document Directory"` cestou k souboru vašeho poznámkového bloku.

### Krok 2: Načtení poznámkového bloku

Dále načtěte soubor poznámkového bloku pomocí třídy `Notebook`:

```java
Notebook notebook = new Notebook(dataDir + "test.onetoc2");
```

Ujistěte se, že jste nahradili `"test.onetoc2"` názvem vašeho souboru poznámkového bloku.

### Krok 3: Nastavení možností uložení obrázku (nastavení rozlišení obrázku java)

Nyní nastavte možnosti pro uložení poznámkového bloku jako obrázku. Specifikujeme formát uložení jako PNG a nastavíme rozlišení na 400 DPI:

```java
NotebookImageSaveOptions saveOptions = new NotebookImageSaveOptions(SaveFormat.Png);
ImageSaveOptions documentSaveOptions = saveOptions.getDocumentSaveOptions();
documentSaveOptions.setResolution(400);
```

Můžete upravit rozlišení podle svých požadavků. Zde **nastavujete rozlišení obrázku**, abyste kontrolovali kvalitu výstupu.

### Krok 4: Zploštění poznámkového bloku (jak zploštit poznámkový blok)

Aby byly všechny prvky zploštěny do jediného obrázku, nastavte možnost `flatten` na `true`:

```java
saveOptions.setFlatten(true);
```

Nastavení `flatten` na `true` zaručuje, že výsledné PNG zachová přesné rozvržení vašeho poznámkového bloku.

### Krok 5: Uložení obrázku (uložit OneNote jako obrázek)

Nakonec uložte poznámkový blok jako zploštělý obrázek:

```java
notebook.save(dataDir + "ExportImageasFlattenedNotebook_out.png", saveOptions);
```

Nahraďte `"ExportImageasFlattenedNotebook_out.png"` požadovaným názvem výstupního souboru. Tento krok **uloží OneNote jako obrázek**, který můžete kdekoliv sdílet nebo vložit.

## Běžné případy použití

- **Dokumentace:** Vložte obrázek poznámkového bloku do technických příruček nebo uživatelských příruček.  
- **Prezentace:** Použijte snímek ve vysokém rozlišení PNG v PowerPointu bez obav o kompatibilitu fontů nebo objektů.  
- **Archivace:** Uložte snímek poznámkového bloku pouze pro čtení pro audity shody.  

## Tipy pro řešení problémů

- **Soubor nenalezen:** Zkontrolujte cestu `dataDir` a ujistěte se, že soubor `.onetoc2` existuje.  
- **Nízká kvalita obrázku:** Zvyšte DPI změnou `documentSaveOptions.setResolution(600);`.  
- **Chybějící prvky:** Ověřte, že je povoleno `saveOptions.setFlatten(true);`; jinak některé vrstvy mohou zůstat oddělené.  

## Často kladené otázky

**Q1: Mohu upravit rozlišení výstupního obrázku?**  
A1: Ano, můžete upravit rozlišení podle svých požadavků úpravou parametru metody `setResolution`.

**Q2: Podporuje Aspose.Note další formáty obrázků pro export?**  
A2: Ano, Aspose.Note podporuje různé formáty obrázků, jako PNG, JPEG, BMP atd., pro export poznámkových bloků.

**Q3: Mohu dále přizpůsobit výstupní obrázek?**  
A3: Ano, Aspose.Note poskytuje rozsáhlé možnosti pro přizpůsobení výstupního obrázku, včetně velikosti stránky, orientace a nastavení kvality.

**Q4: Je k dispozici zkušební verze Aspose.Note pro Java?**  
A4: Ano, můžete získat bezplatnou zkušební verzi [zde](https://releases.aspose.com/).

**Q5: Kde mohu najít podporu pro Aspose.Note pro Java?**  
A5: Podporu a zdroje najdete na fóru Aspose.Note [zde](https://forum.aspose.com/c/note/28).

---

**Last Updated:** 2026-03-21  
**Tested With:** Aspose.Note for Java 24.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}