---
date: 2025-12-28
description: Naučte se, jak exportovat OneNote do PDF s plnou kontrolou pomocí Aspose.Note
  pro Javu. Zahrnuje možnosti exportu poznámkového sešitu OneNote do PDF a průvodce
  konverzí poznámkového sešitu do PDF v Javě.
linktitle: How to Export OneNote to PDF with Options – Convert Notebook to PDF using
  Aspose.Note
second_title: Aspose.Note Java API
title: Jak exportovat OneNote do PDF s možnostmi – Převést poznámkový blok do PDF
  pomocí Aspose.Note
url: /cs/java/onenote-notebook-operations/convert-notebook-to-pdf-with-options/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak exportovat OneNote do PDF s možnostmi – Aspose.Note Java API

## Úvod

V tomto tutoriálu se naučíte **jak exportovat OneNote do PDF** s přizpůsobitelnými možnostmi pomocí Aspose.Note pro Java. Převod sešitu OneNote do PDF je častý požadavek – ať už potřebujete sdílet poznámky ze schůzky, archivovat dokumentaci nebo vytvořit tisknutelné zprávy. S Aspose.Note je proces jednoduchý, plně programovatelný a poskytuje jemnou kontrolu nad výsledným PDF.

## Rychlé odpovědi
- **Co API dělá?** Načte sešit OneNote a uloží jej jako PDF s volitelnými nastaveními.  
- **Jaký jazyk se používá?** Java – ideální pro server‑side nebo desktopové aplikace.  
- **Potřebuji licenci?** Bezplatná zkušební verze stačí pro vývoj; pro produkci je vyžadována komerční licence.  
- **Mohu ovládat rozvržení stránky?** Ano, můžete nastavit algoritmy rozdělení stránek, záhlaví, zápatí a další.  
- **Je ukázkový kód spustitelný?** Rozhodně – stačí nahradit zástupnou cestu skutečnou polohou vašeho sešitu.

## Co je „jak exportovat onenote do pdf“?

Exportování OneNote do PDF znamená převod nativního sešitu OneNote (`*.onetoc2` a souvisejících souborů sekcí) do přenosného, fixního PDF dokumentu. Tento převod zachovává formátování, obrázky a vložené objekty a zároveň umožňuje zobrazit obsah na jakémkoli zařízení bez nutnosti OneNote.

## Proč používat Aspose.Note pro Java?

- **Bez závislosti na Microsoft Office** – funguje na jakékoli platformě, která podporuje Javu.  
- **Bohaté možnosti PDF** – kontrola rozdělení stránek, záhlaví/zápatí a zpracování objektů.  
- **Vysoká věrnost** – výstupní PDF úzce odpovídá původnímu vzhledu OneNote.  
- **Škálovatelnost** – vhodné pro hromadné zpracování tisíců sešitů.

## Požadavky

Než začneme, ujistěte se, že máte:

1. **Java Development Kit (JDK)** – verze 8 nebo vyšší.  
2. **Aspose.Note pro Java** – stáhněte jej z [download link](https://releases.aspose.com/note/java/).  
3. **IDE** – IntelliJ IDEA, Eclipse nebo NetBeans (dle vaší volby).  
4. **Sešit OneNote**, který chcete převést (např. `Notizbuch öffnen.onetoc2`).

## Import balíčků

Nejprve importujte třídy, které poskytují manipulaci se sešitem a funkci uložení do PDF.

```java
import com.aspose.note.Notebook;
import java.io.IOException;
import com.aspose.note.KeepSolidObjectsAlgorithm;
import com.aspose.note.Notebook;
import com.aspose.note.NotebookPdfSaveOptions;
import com.aspose.note.PdfSaveOptions;
```

## Krok 1: Načtení OneNote sešitu

Načtěte soubor sešitu z disku. Nahraďte `Your Document Directory` skutečnou složkou, která obsahuje váš soubor `.onetoc2`.

```java
String dataDir = "Your Document Directory";
// Load a OneNote Notebook
Notebook notebook = new Notebook(dataDir + "Notizbuch �ffnen.onetoc2");
```

## Krok 2: Specifikace možností uložení PDF

Zde definujete, jak má být PDF vygenerováno. Příklad nastavuje algoritmus rozdělení stránek, který udržuje pevné objekty pohromadě – užitečné, pokud máte diagramy nebo tabulky, které musejí zůstat na stejné stránce.

```java
// Specify PDF save options
NotebookPdfSaveOptions notebookSaveOptions = new NotebookPdfSaveOptions();
PdfSaveOptions documentSaveOptions = notebookSaveOptions.getDocumentSaveOptions();
documentSaveOptions.setPageSplittingAlgorithm(new KeepSolidObjectsAlgorithm());
```

## Krok 3: Uložení sešitu jako PDF

Nakonec zapište sešit jako PDF soubor. Výstupní cesta může být libovolné místo, které preferujete.

```java
dataDir = dataDir + "ExportNotebooktoPDFwithOptions_out.pdf";
// Save the Notebook
notebook.save(dataDir, notebookSaveOptions);
```

## Časté problémy a řešení

| Problém | Proč se to děje | Řešení |
|-------|----------------|-----|
| **Soubor nenalezen** | Nesprávný `dataDir` nebo název souboru. | Zkontrolujte cestu a ujistěte se, že soubor sešitu existuje. |
| **Chybějící fonty** | PDF vykreslování vyžaduje stejné fonty jako OneNote. | Nainstalujte požadované fonty na server nebo je vložte pomocí dalších možností Aspose. |
| **Velké sešity způsobují OutOfMemoryError** | Celý sešit se načítá do paměti. | Zpracovávejte sekce jednotlivě nebo zvětšete velikost haldy JVM (`-Xmx`). |

## Závěr

Prošli jsme **jak exportovat OneNote do PDF** pomocí Aspose.Note pro Java, od načtení sešitu, přes konfiguraci PDF možností, až po uložení výsledku. Dodržením těchto kroků můžete integrovat převod sešitu na PDF do jakékoli Java aplikace, ať už jde o desktopový nástroj, webovou službu nebo hromadné zpracování na pozadí.

## Často kladené otázky

### Q1: Mohu přizpůsobit vzhled výstupního PDF?

A1: Ano, Aspose.Note nabízí různé možnosti pro úpravu PDF výstupu, včetně nastavení záhlaví/zápatí, algoritmů rozdělení stránek a dalších.

### Q2: Je Aspose.Note kompatibilní se všemi verzemi OneNote?

A2: Aspose.Note podporuje Microsoft OneNote 2010 a novější verze.

### Q3: Nabízí Aspose.Note bezplatnou zkušební verzi?

A3: Ano, bezplatnou zkušební verzi Aspose.Note si můžete stáhnout [zde](https://releases.aspose.com/).

### Q4: Kde najdu dokumentaci k Aspose.Note?

A4: Kompletní dokumentaci k Aspose.Note najdete [zde](https://reference.aspose.com/note/java/).

### Q5: Jak získám podporu pro Aspose.Note?

A5: Pro technickou pomoc nebo dotazy navštivte fórum podpory Aspose.Note [zde](https://forum.aspose.com/c/note/28).

## Další často kladené otázky

**Q: Jak exportovat sešit OneNote do PDF bez ztráty obrázků?**  
A: Ujistěte se, že je nastaven `KeepSolidObjectsAlgorithm` (jak je ukázáno) a že jsou soubory obrázků zdrojového sešitu přístupné ve stejné složce.

**Q: Můžu hromadně převádět více sešitů v jednom běhu?**  
A: Ano. Procházejte seznam cest k sešitům, vytvořte pro každý `Notebook`, aplikujte stejné `NotebookPdfSaveOptions` a zavolejte `save()`.

**Q: Existuje způsob, jak během převodu nastavit metadata PDF (autor, název)?**  
A: Použijte `PdfSaveOptions.setMetadata()` k definování autora, názvu, předmětu a klíčových slov před uložením.

**Q: Podporuje API šifrovaná PDF chráněná heslem?**  
A: Heslo můžete nastavit na `PdfSaveOptions` pomocí `setEncryptionPassword()` po konfiguraci ostatních možností.

**Q: Jaká verze Aspose.Note byla použita pro tento tutoriál?**  
A: Kód byl testován s Aspose.Note pro Java 23.12.

---

**Poslední aktualizace:** 2025-12-28  
**Testováno s:** Aspose.Note pro Java 23.12  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}