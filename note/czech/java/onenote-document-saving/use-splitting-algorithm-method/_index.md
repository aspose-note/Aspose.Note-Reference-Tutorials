---
date: 2026-03-16
description: Naučte se, jak exportovat PDF z OneNote pomocí Aspose.Note pro Javu s
  metodou rozdělovacího algoritmu, ovládat zalomení stránek a efektivně komprimovat
  obrázky v PDF.
linktitle: Export OneNote PDF with Splitting Algorithm Method – Aspose.Note
second_title: Aspose.Note Java API
title: Export PDF z OneNote pomocí metody rozdělovacího algoritmu – Aspose.Note
url: /cs/java/onenote-document-saving/use-splitting-algorithm-method/
weight: 26
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Export OneNote PDF pomocí metody rozdělovacího algoritmu – Aspose.Note

## Úvod

Pokud potřebujete **exportovat OneNote PDF** programově, Aspose.Note pro Java to usnadňuje. V tomto tutoriálu projdeme metodou rozdělovacího algoritmu, která vám umožní řídit, jak je obsah rozdělen mezi stránky, a zajistit tak čistý a čitelný výstup PDF. Uvidíte, jak nastavit možnosti uložení PDF, vybrat správný algoritmus rozdělení stránky a nakonec vygenerovat soubor PDF – vše pomocí několika řádků Java kódu.

## Rychlé odpovědi
- **Co dělá rozdělovací algoritmus?** Určuje, jak jsou objekty, které přesahují hranice stránky, zpracovány při exportu OneNote stránek do PDF.  
- **Která knihovna je vyžadována?** Aspose.Note pro Java (stáhněte z oficiálního webu Aspose).  
- **Potřebuji licenci?** Pro produkční použití je vyžadována dočasná nebo plná licence; je k dispozici bezplatná zkušební verze.  
- **Mohu exportovat velké OneNote sešity?** Ano – knihovna efektivně zpracovává velké soubory a umožňuje nastavit pravidla rozdělení stránky.  
- **Jaké výstupní formáty jsou podporovány?** PDF, JPEG, PNG, XPS a další; tento průvodce se zaměřuje na export do PDF.  
- **Jak mohu komprimovat obrázky v PDF?** Použijte `pdfSaveOptions.setCompressImages(true)`, aby se snížila velikost obrázků v generovaném PDF.  

## Jak exportovat OneNote PDF pomocí rozdělovacího algoritmu
Tato sekce vás provede přesnými kroky potřebnými k **převodu OneNote stránek** do PDF při inteligentním zpracování zalomení stránek.

## Co je export OneNote PDF?
Export OneNote PDF znamená převod nativního formátu souboru `.one` do přenosného PDF dokumentu. To je užitečné pro sdílení, archivaci nebo tisk obsahu bez nutnosti aplikace OneNote.

## Proč použít rozdělovací algoritmus pro export OneNote PDF?
Algoritmus vám poskytuje detailní kontrolu nad tím, jak jsou složité objekty (tabulky, obrázky, kresby) zpracovány při zalomení stránky. Výběrem vhodného algoritmu můžete:
* Zachovat vizuální rozvržení každé stránky.  
* Vyhnout se oříznutému obsahu, který by jinak byl odříznut.  
* Snížit počet generovaných stránek, když lze objekty čistě přesunout na další stránku.  

## Předpoklady

Předtím, než začneme, ujistěte se, že máte následující předpoklady:

1. Java Development Kit (JDK): Ujistěte se, že máte JDK nainstalovaný ve vašem systému. Můžete jej stáhnout z [webu](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).
2. Knihovna Aspose.Note pro Java: Stáhněte a nainstalujte knihovnu Aspose.Note pro Java z [odkazu ke stažení](https://releases.aspose.com/note/java/).

## Import balíčků

Ve vašem Java projektu importujte potřebné balíčky pro využití funkcí Aspose.Note.

```java
import java.io.IOException;
import com.aspose.note.AlwaysSplitObjectsAlgorithm;
import com.aspose.note.Document;
import com.aspose.note.KeepPartAndCloneSolidObjectToNextPageAlgorithm;
import com.aspose.note.KeepSolidObjectsAlgorithm;
import com.aspose.note.PdfSaveOptions;
```

## Krok 1: Definujte adresář dokumentu

Nastavte adresář, ve kterém se nachází váš OneNote dokument.

```java
String dataDir = "Your Document Directory";
```

## Krok 2: Načtěte OneNote dokument

Načtěte OneNote dokument pomocí třídy `Document` z Aspose.Note.

```java
Document doc = new Document(dataDir + "Sample1.one");
```

## Krok 3: Nastavte možnosti uložení PDF

Vytvořte instanci `PdfSaveOptions` pro určení možností uložení dokumentu jako PDF. Zde **nastavíte chování rozdělení stránky** a další nastavení související s PDF.

```java
PdfSaveOptions pdfSaveOptions = new PdfSaveOptions();
```

## Krok 4: Nastavte algoritmus rozdělení stránky

Vyberte vhodný algoritmus rozdělení podle vašich požadavků. Zde používáme `KeepPartAndCloneSolidObjectToNextPageAlgorithm`, který ponechá část objektu na aktuální stránce a zbytek zkopíruje na další stránku.

```java
pdfSaveOptions.setPageSplittingAlgorithm(new KeepPartAndCloneSolidObjectToNextPageAlgorithm(100));
```

## Krok 5: Uložte dokument

Uložte dokument s určenými možnostmi uložení PDF. Tento krok **vytvoří výstup PDF OneNote**, který můžete otevřít, sdílet nebo vytisknout.

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
| **Objekty jsou oříznuty na hranicích stránky** | Vyzkoušejte jiný algoritmus, například `AlwaysSplitObjectsAlgorithm`, nebo zvyšte prahovou hodnotu v `KeepPartAndCloneSolidObjectToNextPageAlgorithm`. |
| **Výstupní PDF je prázdné** | Ověřte, že zdrojový soubor `.one` není poškozený a že cesta `dataDir` je správná. |
| **Výkon je pomalý u velkých sešitů** | Použijte `pdfSaveOptions.setCompressImages(true)` ke snížení využití paměti a zvažte zpracování sešitu v menších částech. |

## Často kladené otázky

**Q: Mohu použít Aspose.Note pro Java s jinými programovacími jazyky?**  
A: Ano, Aspose.Note je také k dispozici pro .NET, C++ a Python.

**Q: Je Aspose.Note vhodný pro zpracování velkých OneNote souborů?**  
A: Rozhodně. Knihovna je optimalizována pro efektivní zpracování velkých sešitů.

**Q: Kde mohu najít další zdroje a podporu pro Aspose.Note?**  
A: Můžete se podívat na [dokumentaci](https://reference.aspose.com/note/java/) a [forum](https://forum.aspose.com/c/note/28) pro podporu a rady.

**Q: Můžu vyzkoušet Aspose.Note před zakoupením?**  
A: Ano, můžete využít [bezplatnou zkušební verzi](https://releases.aspose.com/), abyste prozkoumali funkce před nákupem.

**Q: Jak mohu získat dočasnou licenci pro Aspose.Note?**  
A: Můžete požádat o [dočasnou licenci](https://purchase.aspose.com/temporary-license/), abyste produkt vyhodnotili během zkušebního období.

---

**Poslední aktualizace:** 2026-03-16  
**Testováno s:** Aspose.Note 24.12 pro Java  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}