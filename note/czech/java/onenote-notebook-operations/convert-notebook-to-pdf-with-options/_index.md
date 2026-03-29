---
date: 2026-03-29
description: Převod sešitů OneNote do PDF s možnostmi, uložení sešitu jako PDF a přidání
  záhlaví a zápatí PDF pomocí Aspose.Note pro Javu.
linktitle: Convert Notebook to PDF with Options in OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: převést OneNote na PDF s možnostmi – Aspose.Note
url: /cs/java/onenote-notebook-operations/convert-notebook-to-pdf-with-options/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Převod OneNote do PDF s možnostmi pomocí Aspose.Note

## Úvod

V tomto tutoriálu se naučíte, jak **convert onenote to pdf** s úplnou kontrolou nad výstupem. Aspose.Note pro Java usnadňuje export notebooků OneNote do PDF, což vám umožní **save notebook as pdf** a přizpůsobit záhlaví, zápatí a chování rozdělování stránek. Ať už potřebujete generovat zprávy, archivovat poznámky ze schůzek nebo sdílet obsah s uživateli, kteří nemají OneNote, tento průvodce vás provede každým krokem.

## Rychlé odpovědi
- **Jaká knihovna provádí konverzi?** Aspose.Note for Java.
- **Mohu do PDF přidat záhlaví nebo zápatí?** Ano – použijte PDF save options k vložení vlastních záhlaví/zápatí.
- **Potřebuji licenci pro produkční použití?** Komerční licence je vyžadována pro ne‑zkušební použití.
- **Jaké verze Javy jsou podporovány?** Java 8 a novější.
- **Jak dlouho trvá konverze?** Obvykle několik sekund pro notebooky průměrné velikosti.

## Co je „convert onenote to pdf“?

Převod OneNote do PDF znamená převzít notebook OneNote (soubor *.onetoc2*) a vykreslit každou stránku jako PDF stránku. Výsledné PDF zachovává text, obrázky a rozvržení, což umožňuje jeho prohlížení na jakémkoli zařízení bez potřeby OneNote.

## Proč použít Aspose.Note k exportu notebooku OneNote do PDF?

- **Není vyžadována instalace Office** – API funguje samostatně.
- **Detailní kontrola** – můžete nastavit algoritmy rozdělování stránek, vložit písma a přidat záhlaví/zápatí.
- **Vysoká věrnost** – vizuální vzhled původního notebooku je zachován.
- **Cross‑platform** – funguje na Windows, Linuxu a macOS s jakýmkoli Java runtime.

## Požadavky

Než začneme, ujistěte se, že máte následující požadavky připravené:

1. Java Development Kit (JDK) – JDK 8 nebo novější nainstalováno.
2. Aspose.Note for Java – stáhněte a nainstalujte z [download link](https://releases.aspose.com/note/java/).
3. IDE (Integrated Development Environment) – IntelliJ IDEA, Eclipse nebo NetBeans jsou oblíbené volby.

## Import balíčků

Nejprve musíte do svého Java projektu importovat potřebné balíčky. Tyto balíčky poskytují třídy a metody potřebné pro práci s dokumenty OneNote.

```java
import com.aspose.note.Notebook;
import java.io.IOException;
import com.aspose.note.KeepSolidObjectsAlgorithm;
import com.aspose.note.Notebook;
import com.aspose.note.NotebookPdfSaveOptions;
import com.aspose.note.PdfSaveOptions;
```

## Krok 1: Načtení notebooku OneNote

Pro **convert onenote to pdf** musíte nejprve načíst notebook OneNote. Ujistěte se, že cesta k souboru notebooku je správně zadána.

```java
String dataDir = "Your Document Directory";
// Load a OneNote Notebook
Notebook notebook = new Notebook(dataDir + "Notizbuch �ffnen.onetoc2");
```

## Krok 2: Specifikace možností uložení PDF

Aspose.Note poskytuje různé možnosti pro přizpůsobení výstupu PDF. Můžete nastavit možnosti jako algoritmy rozdělování stránek, nastavení záhlaví/zápatí a další.

```java
// Specify PDF save options
NotebookPdfSaveOptions notebookSaveOptions = new NotebookPdfSaveOptions();
PdfSaveOptions documentSaveOptions = notebookSaveOptions.getDocumentSaveOptions();
documentSaveOptions.setPageSplittingAlgorithm(new KeepSolidObjectsAlgorithm());
```

## Krok 3: Uložení notebooku jako PDF

Jakmile jste načetli notebook a specifikovali možnosti uložení, je čas **save the notebook as pdf**.

```java
dataDir = dataDir + "ExportNotebooktoPDFwithOptions_out.pdf";
// Save the Notebook
notebook.save(dataDir, notebookSaveOptions);
```

## Časté problémy a řešení

| Problém | Příčina | Řešení |
|-------|-------|----------|
| PDF chybí obrázky | Obrázky uložené jako vložené objekty nejsou načteny | Ujistěte se, že soubor notebooku a všechny propojené zdroje jsou ve stejném adresáři před načtením. |
| Záhlaví/zápatí se nezobrazují | Možnosti záhlaví/zápatí nejsou nastaveny v `PdfSaveOptions` | Použijte `documentSaveOptions.setHeaderFooter()` k definování obsahu před uložením. |
| Chyba paměti u velkých notebooků | Celý notebook je načten do paměti | Zpracovávejte notebook po sekcích nebo zvětšete velikost haldy JVM (`-Xmx2g`). |

## Často kladené otázky

### Q1: Můžu přizpůsobit vzhled výstupu PDF?
A1: Ano, Aspose.Note poskytuje různé možnosti pro přizpůsobení výstupu PDF, včetně nastavení záhlaví/zápatí, algoritmů rozdělování stránek a dalších.

### Q2: Je Aspose.Note kompatibilní se všemi verzemi OneNote?
A2: Aspose.Note podporuje Microsoft OneNote 2010 a novější verze.

### Q3: Nabízí Aspose.Note bezplatnou zkušební verzi?
A3: Ano, můžete si stáhnout bezplatnou zkušební verzi Aspose.Note z [zde](https://releases.aspose.com/).

### Q4: Kde mohu najít dokumentaci k Aspose.Note?
A4: Můžete najít komplexní dokumentaci k Aspose.Note [zde](https://reference.aspose.com/note/java/).

### Q5: Jak mohu získat podporu pro Aspose.Note?
A5: Pro jakoukoli technickou pomoc nebo dotazy můžete navštívit fórum podpory Aspose.Note [zde](https://forum.aspose.com/c/note/28).

## Další často kladené otázky

**Q: Jak přidat vlastní PDF záhlaví nebo zápatí?**  
A: Vytvořte objekt `PdfHeaderFooterOptions`, nakonfigurujte text nebo obrázky a přiřaďte jej k `documentSaveOptions.setHeaderFooterOptions()` před voláním `save`.

**Q: Mohu exportovat pouze vybrané sekce notebooku?**  
A: Ano – načtěte notebook, získejte požadované objekty `Section` a zavolejte `section.save()` se stejnými PDF možnostmi.

**Q: Je možné šifrovat vygenerované PDF?**  
A: Rozhodně. Použijte `documentSaveOptions.setEncryptionPassword("yourPassword")` k ochraně PDF.

**Q: Jaké úvahy o výkonu bych měl mít na paměti?**  
A: U velmi velkých notebooků zvažte streamování výstupu do `FileOutputStream` a zvýšení velikosti haldy JVM, pokud narazíte na `OutOfMemoryError`.

---

**Poslední aktualizace:** 2026-03-29  
**Testováno s:** Aspose.Note for Java 24.12  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}