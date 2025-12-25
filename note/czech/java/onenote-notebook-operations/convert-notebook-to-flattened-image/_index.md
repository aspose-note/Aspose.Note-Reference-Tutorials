---
date: 2025-12-25
description: Naučte se, jak převést OneNote na PNG pomocí Aspose.Note pro Javu. Tento
  průvodce ukazuje, jak nastavit rozlišení obrázku, zploštit poznámkový blok a efektivně
  uložit OneNote jako obrázek.
linktitle: How to Convert OneNote to PNG – Flatten Notebook to Image with Aspose.Note
second_title: Aspose.Note Java API
title: Jak převést OneNote na PNG – Zploštit poznámkový blok do obrázku s Aspose.Note
url: /cs/java/onenote-notebook-operations/convert-notebook-to-flattened-image/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Převod poznámkového bloku na plochý obrázek v OneNote - Aspose.Note

## Úvod

V tomto tutoriálu se dozvíte, jak **převést OneNote na PNG** tím, že celý poznámkový blok převedete na jeden plochý obrázek pomocí Aspose.Note pro Java. Tento přístup je ideální, když potřebujete sdílet poznámkový blok jako statický obrázek, vložit jej do zpráv nebo archivovat bez ztráty vizuálních detailů.

## Rychlé odpovědi
- **Co znamená „flatten notebook“?** Sloučí všechny prvky stránky do jednoho rastrového obrázku.  
- **Jaký formát se používá?** PNG je výchozí, poskytuje bezztrátovou kvalitu.  
- **Mohu změnit DPI?** Ano, použijte `setResolution` na `ImageSaveOptions`.  
- **Potřebuji licenci?** Bezplatná zkušební verze funguje pro hodnocení; pro produkční nasazení je vyžadována komerční licence.  
- **Je to podporováno na všech OS?** Java API běží kdekoliv, kde běží Java.  

## Co je převod OneNote na PNG?

Převod OneNote na PNG vytvoří bitmapovou reprezentaci každé stránky v poznámkovém bloku, zachovává text, kresby a vložené objekty v jednom souboru obrázku. To je zvláště užitečné pro dokumentaci, prezentace nebo archivaci pro soulad.

## Proč převádět OneNote na PNG pomocí Aspose.Note?

- **Plná věrnost** – Všechny vizuální prvky jsou zachovány.  
- **Výstup v jednom souboru** – Není nutné spravovat soubory více stránek.  
- **Přizpůsobitelné rozlišení** – Nastavte DPI podle požadavků na kvalitu.  
- **Bez instalace Office** – Funguje zcela nezávisle na Microsoft OneNote.

## Požadavky

Před začátkem se ujistěte, že máte následující:

1. Java Development Kit (JDK) nainstalovaný ve vašem systému.  
2. Knihovnu Aspose.Note pro Java staženou a nastavenou ve vašem Java projektu. Knihovnu můžete stáhnout [zde](https://releases.aspose.com/note/java/).  
3. Základní znalost programování v Javě.

## Import balíčků

Pro začátek musíte importovat potřebné balíčky z Aspose.Note pro Java:

```java
import java.io.IOException;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.Notebook;
import com.aspose.note.NotebookImageSaveOptions;
import com.aspose.note.SaveFormat;
```

## Krok 1: Nastavení adresáře dokumentu

Nejprve definujte adresář, kde se nachází soubor vašeho poznámkového bloku:

```java
String dataDir = "Your Document Directory";
```

Nahraďte `"Your Document Directory"` cestou k souboru vašeho poznámkového bloku.

## Krok 2: Načtení poznámkového bloku

Dále načtěte soubor poznámkového bloku pomocí třídy `Notebook`:

```java
Notebook notebook = new Notebook(dataDir + "test.onetoc2");
```

Ujistěte se, že jste nahradili `"test.onetoc2"` názvem vašeho souboru poznámkového bloku.

## Krok 3: Nastavení možností uložení obrázku

Nyní nastavte možnosti pro uložení poznámkového bloku jako obrázku. Určíme formát uložení jako PNG a nastavíme rozlišení na 400 DPI:

```java
NotebookImageSaveOptions saveOptions = new NotebookImageSaveOptions(SaveFormat.Png);
ImageSaveOptions documentSaveOptions = saveOptions.getDocumentSaveOptions();
documentSaveOptions.setResolution(400);
```

Rozlišení můžete upravit podle svých požadavků. Zde **nastavujete rozlišení obrázku**, aby se kontrolovala kvalita výstupu.

## Krok 4: Zploštění poznámkového bloku

Aby byly všechny prvky zploštěny do jednoho obrázku, nastavte volbu `flatten` na `true`:

```java
saveOptions.setFlatten(true);
```

Nastavení `flatten` na `true` zaručuje, že výsledné PNG zachová přesné rozložení vašeho poznámkového bloku.

## Krok 5: Uložení obrázku

Nakonec uložte poznámkový blok jako zploštělý obrázek:

```java
notebook.save(dataDir + "ExportImageasFlattenedNotebook_out.png", saveOptions);
```

Nahraďte `"ExportImageasFlattenedNotebook_out.png"` požadovaným názvem výstupního souboru. Tento krok **ukládá OneNote jako obrázek**, který můžete sdílet nebo vložit kamkoli.

## Běžné případy použití

- **Dokumentace:** Vložte obrázek poznámkového bloku do technických manuálů nebo uživatelských příruček.  
- **Prezentace:** Použijte snímek PNG ve vysokém rozlišení v PowerPointu bez obav o kompatibilitu fontů nebo objektů.  
- **Archivace:** Uložte pouze‑ke‑čtení snímek poznámkového bloku pro audity souladu.

## Tipy pro řešení problémů

- **Soubor nenalezen:** Zkontrolujte cestu `dataDir` a ujistěte se, že soubor `.onetoc2` existuje.  
- **Nízká kvalita obrázku:** Zvyšte DPI změnou `documentSaveOptions.setResolution(600);`.  
- **Chybějící prvky:** Ověřte, že je povoleno `saveOptions.setFlatten(true);`; jinak některé vrstvy mohou zůstat oddělené.

## Často kladené otázky

**Q1: Mohu upravit rozlišení výstupního obrázku?**  
A1: Ano, můžete upravit rozlišení podle svých požadavků úpravou parametru metody `setResolution`.

**Q2: Podporuje Aspose.Note pro export i jiné formáty obrázků?**  
A2: Ano, Aspose.Note podporuje různé formáty obrázků, jako PNG, JPEG, BMP atd., pro export poznámkových bloků.

**Q3: Mohu dále přizpůsobit výstupní obrázek?**  
A3: Ano, Aspose.Note poskytuje rozsáhlé možnosti pro přizpůsobení výstupního obrázku, včetně velikosti stránky, orientace a nastavení kvality.

**Q4: Je k dispozici zkušební verze Aspose.Note pro Java?**  
A4: Ano, můžete získat bezplatnou zkušební verzi [zde](https://releases.aspose.com/).

**Q5: Kde mohu najít podporu pro Aspose.Note pro Java?**  
A5: Podporu a zdroje najdete na fóru Aspose.Note [zde](https://forum.aspose.com/c/note/28).

---

**Poslední aktualizace:** 2025-12-25  
**Testováno s:** Aspose.Note pro Java 24.12  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}