---
date: 2025-12-18
description: Naučte se, jak exportovat stránky OneNote do PDF pomocí Aspose.Note pro
  Java. Vyberte algoritmy rozdělení, nastavte rozdělení stránek a snadno generujte
  PDF soubory.
linktitle: Export OneNote Pages with Splitting Algorithm Method – Aspose.Note
second_title: Aspose.Note Java API
title: Exportovat stránky OneNote pomocí metody rozdělovacího algoritmu – Aspose.Note
url: /cs/java/onenote-document-saving/use-splitting-algorithm-method/
weight: 26
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Exportovat stránky OneNote pomocí metody rozdělovacího algoritmu – Aspose.Note

## Úvod

Pokud potřebujete **exportovat stránky OneNote** do PDF dokumentu programově, Aspose.Note pro Java to usnadňuje. V tomto tutoriálu projdeme metodou rozdělovacího algoritmu, která vám umožní řídit, jak je obsah rozdělen mezi stránky, a zajistit tak čistý a čitelný PDF výstup. Uvidíte, jak nastavit možnosti uložení PDF, vybrat správný algoritmus rozdělení stránky a nakonec vygenerovat PDF soubor – vše pomocí několika řádků Java kódu.

## Rychlé odpovědi
- **Co dělá rozdělovací algoritmus?** Určuje, jak jsou objekty, které přesahují hranice stránky, zpracovány při exportu stránek OneNote do PDF.  
- **Která knihovna je vyžadována?** Aspose.Note pro Java (stáhněte z oficiálního webu Aspose).  
- **Potřebuji licenci?** Pro produkční použití je vyžadována dočasná nebo plná licence; k dispozici je bezplatná zkušební verze.  
- **Mohu exportovat velké sešity OneNote?** Ano – knihovna efektivně zpracovává velké soubory a umožňuje nastavit pravidla rozdělení stránky.  
- **Jaké výstupní formáty jsou podporovány?** PDF, JPEG, PNG, XPS a další; tento průvodce se zaměřuje na export do PDF.

## Co je **export onenote pages**?
Exportování stránek OneNote znamená převod nativního formátu `.one` do přenosnějšího formátu, jako je PDF. To je užitečné pro sdílení, archivaci nebo tisk obsahu bez nutnosti aplikace OneNote.

## Proč použít rozdělovací algoritmus pro **export onenote pages**?
Algoritmus vám poskytuje jemnou kontrolu nad tím, jak jsou složité objekty (tabulky, obrázky, kresby) zpracovány při přechodu na novou stránku. Výběrem vhodného algoritmu můžete:

* Zachovat vizuální rozvržení každé stránky.  
* Předejít oříznutému obsahu, který by jinak byl oříznut.  
* Snížit počet vygenerovaných stránek, když lze objekty čistě přesunout na další stránku.  

## Požadavky

Než začneme, ujistěte se, že máte následující předpoklady:

1. Java Development Kit (JDK): Ujistěte se, že máte nainstalovaný JDK. Můžete jej stáhnout z [webu](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).
2. Aspose.Note pro Java knihovna: Stáhněte a nainstalujte knihovnu Aspose.Note pro Java z [odkazu ke stažení](https://releases.aspose.com/note/java/).

## Importovat balíčky

Ve vašem Java projektu importujte potřebné balíčky pro využití funkcí Aspose.Note.

```java
import java.io.IOException;
import com.aspose.note.AlwaysSplitObjectsAlgorithm;
import com.aspose.note.Document;
import com.aspose.note.KeepPartAndCloneSolidObjectToNextPageAlgorithm;
import com.aspose.note.KeepSolidObjectsAlgorithm;
import com.aspose.note.PdfSaveOptions;
```

## Krok 1: Definovat adresář dokumentu

Nastavte adresář, kde se nachází váš OneNote dokument.

```java
String dataDir = "Your Document Directory";
```

## Krok 2: Načíst OneNote dokument

Načtěte OneNote dokument pomocí třídy `Document` z Aspose.Note.

```java
Document doc = new Document(dataDir + "Sample1.one");
```

## Krok 3: Nastavit možnosti uložení PDF

Vytvořte instanci `PdfSaveOptions` pro specifikaci možností ukládání dokumentu jako PDF. Zde nastavíte chování **rozdělení stránky** a další nastavení související s PDF.

```java
PdfSaveOptions pdfSaveOptions = new PdfSaveOptions();
```

## Krok 4: Nastavit algoritmus rozdělení stránky

Vyberte vhodný algoritmus rozdělení podle vašich požadavků. Zde používáme `KeepPartAndCloneSolidObjectToNextPageAlgorithm`, který zachová část objektu na aktuální stránce a zbytek klonuje na následující stránku.

```java
pdfSaveOptions.setPageSplittingAlgorithm(new KeepPartAndCloneSolidObjectToNextPageAlgorithm(100));
```

## Krok 5: Uložit dokument

Uložte dokument s určenými možnostmi uložení PDF. Tento krok **generuje PDF onenote** výstup, který můžete otevřít, sdílet nebo vytisknout.

```java
try {
    doc.save(dataDir + "UsingSplittingAlgorithmMethod_out.Jpeg", pdfSaveOptions);
} catch (Exception ex) {
    System.out.println("Exception: " + ex.getMessage());
}
```

## Časté problémy a řešení

| Problém | Řešení |
|-------|----------|
| **Objekty jsou oříznuty na hranicích stránky** | Vyzkoušejte jiný algoritmus, například `AlwaysSplitObjectsAlgorithm`, nebo zvýšte prahovou hodnotu v `KeepPartAndCloneSolidObjectToNextPageAlgorithm`. |
| **Výstupní PDF je prázdný** | Ověřte, že zdrojový soubor `.one` není poškozený a že cesta `dataDir` je správná. |
| **Výkon je pomalý u velkých sešitů** | Použijte `pdfSaveOptions.setCompressImages(true)` ke snížení využití paměti a zvažte zpracování sešitu po menších částech. |

## Často kladené otázky

**Q: Mohu použít Aspose.Note pro Java s jinými programovacími jazyky?**  
A: Ano, Aspose.Note je k dispozici také pro .NET, C++ a Python.

**Q: Je Aspose.Note vhodný pro zpracování velkých souborů OneNote?**  
A: Rozhodně. Knihovna je optimalizována pro efektivní práci s velkými sešity.

**Q: Kde najdu další zdroje a podporu pro Aspose.Note?**  
A: Můžete se podívat na [dokumentaci](https://reference.aspose.com/note/java/) a [forum](https://forum.aspose.com/c/note/28) pro podporu a vedení.

**Q: Můžu vyzkoušet Aspose.Note před zakoupením?**  
A: Ano, můžete využít [bezplatnou zkušební verzi](https://releases.aspose.com/) a prozkoumat funkce před nákupem.

**Q: Jak získat dočasnou licenci pro Aspose.Note?**  
A: Můžete požádat o [dočasnou licenci](https://purchase.aspose.com/temporary-license/) k vyhodnocení produktu během zkušebního období.

---

**Poslední aktualizace:** 2025-12-18  
**Testováno s:** Aspose.Note 24.12 pro Java  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}