---
date: 2025-12-28
description: Naučte se, jak z OneNote sešitu vytvořit plochý PDF pomocí Aspose.Note
  pro Javu. Tento průvodce ukazuje, jak převést OneNote do PDF, přizpůsobit možnosti
  exportu a použít možnosti uložení Aspose PDF.
linktitle: Convert Notebook to Flattened PDF in OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: Jak zploštit PDF z OneNote poznámkového bloku – tutoriál Aspose.Note
url: /cs/java/onenote-notebook-operations/convert-notebook-to-flattened-pdf/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak zploštit PDF z OneNote sešitu – Aspose.Note

## Úvod

Pokud potřebujete **flatten PDF** soubory generované z OneNote sešitů, tento tutoriál vás provede přesné kroky pomocí Aspose.Note pro Java. Převod OneNote sešitu na zploštělý PDF je běžná potřeba, když chcete statický, připravený k tisku dokument, který zachovává původní rozvržení bez interaktivních prvků. Pokryjeme vše od nastavení prostředí až po konfiguraci `NotebookPdfSaveOptions`, aby výsledný PDF byl plně zploštělý.

## Rychlé odpovědi
- **Co je “flatten PDF”?** Vytváří PDF, kde jsou všechny interaktivní prvky (poznámky, vrstvy) sloučeny do jediné statické stránky.
- **Která knihovna provádí konverzi?** Aspose.Note pro Java, používající její vestavěné možnosti uložení PDF.
- **Potřebuji licenci?** Bezplatná zkušební verze funguje pro hodnocení; pro produkční nasazení je vyžadována komerční licence.
- **Mohu hromadně konvertovat sešity?** Ano – můžete pomocí stejného kódu projít více souborů `.onetoc2`.
- **Je výstup skutečně zploštělý?** Nastavení `flatten` na `true` zaručuje neinteraktivní PDF.

## Předpoklady

Než se ponoříme do kódu, ujistěte se, že máte následující:

1. **Java Development Kit (JDK)** – jakákoli recentní verze (8 nebo vyšší) nainstalovaná a nakonfigurovaná.
2. **Aspose.Note pro Java knihovna** – stáhněte ji [zde](https://releases.aspose.com/note/java/).
3. **IDE** – IntelliJ IDEA, Eclipse nebo jakýkoli editor, který preferujete.
4. **OneNote sešit** (`.onetoc2` soubor), který chcete exportovat.

## Import balíčků

Nejprve importujte třídy potřebné pro práci se sešitem a export do PDF.

```java
import com.aspose.note.Notebook;
import com.aspose.note.NotebookPdfSaveOptions;
import java.io.IOException;
```

## Krok 1: Načtení OneNote sešitu

Načtěte sešit, který chcete převést. Nahraďte zástupnou cestu skutečnou polohou vašeho souboru `.onetoc2`.

```java
String dataDir = "Your Document Directory";
Notebook notebook = new Notebook(dataDir + "Notizbuch öffnen.onetoc2");
```

## Krok 2: Nastavení možností konverze

Nakonfigurujte možnosti uložení PDF. Nastavení `flatten` na `true` zajišťuje, že výstupní PDF bude zploštělý. Zde vstupují do hry **aspose pdf save options**.

```java
NotebookPdfSaveOptions notebookSaveOptions = new NotebookPdfSaveOptions();
notebookSaveOptions.setFlatten(true);
```

## Krok 3: Uložení sešitu jako zploštělého PDF

Definujte název výstupního souboru a zavolejte metodu `save` s možnostmi, které jsme právě nakonfigurovali.

```java
dataDir = dataDir + "ExportNotebookToPDFAsFlattened_out.pdf";
// Save the Notebook
notebook.save(dataDir, notebookSaveOptions);
```

## Proč je to důležité

Zploštění PDF je nezbytné, když bude dokument sdílen s uživateli, kteří nemusí mít původní aplikaci OneNote, nebo když potřebujete pevné rozvržení pro tisk, archivaci či právní soulad. Použití `NotebookPdfSaveOptions` z Aspose.Note vám poskytuje detailní kontrolu nad procesem exportu, což usnadňuje **převod OneNote na PDF** při zachování vizuální věrnosti.

## Časté problémy a řešení

| Příznak | Pravděpodobná příčina | Oprava |
|---------|-----------------------|--------|
| Prázdné stránky v PDF | Sešit nebyl načten správně | Ověřte cestu k souboru `.onetoc2` a ujistěte se, že soubor není poškozený. |
| PDF není zploštělý | `setFlatten(true)` nebylo zavoláno | Zkontrolujte, že instance `NotebookPdfSaveOptions` je předána metodě `save`. |
| Chyba nedostatku paměti u velkých sešitů | Nedostatečná velikost haldy JVM | Zvyšte velikost haldy (`-Xmx2g` nebo vyšší) při spouštění aplikace. |

## Často kladené otázky

**Q: Je Aspose.Note pro Java kompatibilní s různými verzemi OneNote?**  
A: Ano, Aspose.Note pro Java podporuje různé verze OneNote, což zajišťuje plynulou konverzi napříč prostředími.

**Q: Mohu přizpůsobit výstup PDF pomocí Aspose.Note pro Java?**  
A: Rozhodně. Můžete upravit velikost stránky, okraje, písma a další vlastnosti pomocí `NotebookPdfSaveOptions`.

**Q: Podporuje Aspose.Note pro Java hromadnou konverzi sešitů?**  
A: Ano, můžete projít více souborů sešitu a použít na každý stejné možnosti uložení.

**Q: Je k dispozici zkušební verze Aspose.Note pro Java?**  
A: Ano, můžete získat bezplatnou zkušební verzi Aspose.Note pro Java [zde](https://releases.aspose.com/).

**Q: Kde mohu najít podporu pro Aspose.Note pro Java?**  
A: Podporu a pomoc pro Aspose.Note pro Java najdete na [fóru Aspose.Note](https://forum.aspose.com/c/note/28).

---

**Poslední aktualizace:** 2025-12-28  
**Testováno s:** Aspose.Note pro Java 24.12  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}