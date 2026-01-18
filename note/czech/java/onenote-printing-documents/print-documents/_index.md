---
date: 2026-01-18
description: Naučte se, jak tisknout dokumenty OneNote pomocí Aspose.Note pro Javu.
  Tento průvodce ukazuje, jak tisknout do PDF, přizpůsobit nastavení tisku a používat
  možnosti virtuální tiskárny v Javě.
linktitle: Print Documents in OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: Jak vytisknout OneNote – Aspose.Note
url: /cs/java/onenote-printing-documents/print-documents/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Tisk dokumentů v OneNote - Aspose.Note

## Úvod

Tisk stránek OneNote z Java aplikace je častý požadavek, ať už potřebujete tištěné zprávy, PDF archivy nebo integraci s virtuálními tiskárnami. V tomto tutoriálu **se naučíte, jak tisknout** dokumenty OneNote pomocí Aspose.Note pro Java, včetně jednoduchého tisku, přizpůsobení nastavení tisku, tisku do PDF a využití workflow s virtuální tiskárnou v Javě.

## Rychlé odpovědi
- **Mohu tisknout OneNote přímo do PDF z Javy?** Ano – použijte `DocumentPrintAttributeSet` s PDF virtuální tiskárnou jako „Microsoft XPS Document Writer“ nebo „doPDF 8“.  
- **Potřebuji licenci pro tisk?** Platná licence Aspose.Note pro Java je vyžadována pro produkční použití.  
- **Jak omezím tisknuté stránky?** Nastavte rozsah tisku pomocí `asposeAttr.setPrintRange(startPage, endPage)`.  
- **Mohu změnit počet kopií?** Ano, použijte `asposeAttr.setCopies(numberOfCopies)`.  
- **Je podporována virtuální tiskárna?** Rozhodně – Aspose.Note funguje s libovolnou nainstalovanou virtuální tiskárnou, ke které má Java přístup.

## Co znamená „jak tisknout onenote“?
Tento výraz odkazuje na proces odeslání obsahu stránky OneNote z vaší aplikace na tiskárnu nebo do souborového formátu (např. PDF) programově. Aspose.Note pro Java abstrahuje nízkoúrovňová tisková API, takže se můžete soustředit na obchodní logiku místo manipulace se zařízeními.

## Proč použít Aspose.Note pro Java k tisku OneNote?
- **Plná kontrola** nad možnostmi tisku (rozsah, kopie, výběr tiskárny).  
- **Bezproblémové generování PDF** s podporou „print to pdf java“ prostřednictvím virtuálních tiskáren.  
- **Žádná COM interop** – čistá Java, ideální pro multiplatformní servery.  
- **Robustní zpracování chyb** s `PrintException` a podrobnými třídami atributů.

## Požadavky

Než začnete, ujistěte se, že máte:

1. **Java Development Kit (JDK)** – verze 8 nebo vyšší nainstalovanou.  
2. **Aspose.Note pro Java JAR** – stáhněte jej z oficiálního webu **[zde](https://releases.aspose.com/note/java/)**.  
3. **OneNote dokument** – soubor `.one`, který chcete vytisknout.  
4. (Volitelné) **Virtuální PDF tiskárna** nainstalovaná (např. Microsoft XPS Document Writer, doPDF).

## Import balíčků

Nejprve importujte potřebné třídy do svého Java zdrojového souboru:

```java
import javax.print.PrintException;

import com.aspose.note.Document;
import com.aspose.note.DocumentPrintAttributeSet;
import com.aspose.note.PrintOptions;
```

## Průvodce krok za krokem

### Krok 1: Tisk dokumentu (základní)

Tento příklad vytiskne celý soubor OneNote pomocí výchozí tiskárny.

```java
public static void PrintDocument() throws PrintException {
    // Specify the directory where your document is located
    String dataDir = "Your Document Directory";
    
    // Load the OneNote document
    Document document = new Document(dataDir + "YourDocument.one");
    
    // Print the document
    document.print();
}
```

**Proč je to důležité:** Ukazuje nejjednodušší způsob, jak spustit tisk bez jakékoli další konfigurace.

### Krok 2: Tisk dokumentu s vlastními nastaveními tisku

Pokud potřebujete **přizpůsobit nastavení tisku** – například tisknout jen stránky 1‑2 – můžete použít `DocumentPrintAttributeSet`.

```java
public static void PrintDocumentWithPrintOptions() throws PrintException {
    // Specify the directory where your document is located
    String dataDir = "Your Document Directory";

    // Load the OneNote document
    Document document = new Document(dataDir + "YourDocument.one");

    // Define print options
    final DocumentPrintAttributeSet asposeAttr = new DocumentPrintAttributeSet("Microsoft XPS Document Writer");
    asposeAttr.setPrintRange(1, 2);

    // Print the document with specified options
    document.print(asposeAttr);
}
```

**Tip:** Nahraďte `"Microsoft XPS Document Writer"` názvem libovolné nainstalované tiskárny, aby výstup směřoval jinam.

### Krok 3: Tisk dokumentů pomocí virtuální tiskárny (tisk do PDF v Javě)

Virtuální tiskárny vám umožní generovat PDF soubory přímo z Javy. Níže používáme **doPDF 8** jako příklad.

```java
public static void PrintDocumentsWithVirtualPrinter() throws PrintException {
    // Specify the directory where your document is located
    String dataDir = "Your Document Directory";
    Document doc = new Document(dataDir + "YourDocument.one");
     
    // Define print options for virtual printer
    final DocumentPrintAttributeSet asposeAttr = new DocumentPrintAttributeSet("doPDF 8");
    asposeAttr.setPrintRange(1, 2);
    asposeAttr.setCopies(3);
     
    PrintOptions printOptions = new PrintOptions();
    printOptions.setDocumentName("YourDocument.one");
    printOptions.setPrinterSettings(asposeAttr);
      
    // Print the document using virtual printer
    doc.print(printOptions);
}
```

**Profesionální tip:** Upravit `asposeAttr.setCopies()` pro řízení počtu PDF kopií generovaných během jednoho spuštění.

## Časté problémy a řešení

| Problém | Řešení |
|-------|----------|
| **Tiskárna nebyla nalezena** | Ověřte, že název tiskárny přesně odpovídá tomu, jak je zobrazen ve Windows > Zařízení a tiskárny. |
| **Vyhozena `PrintException`** | Ujistěte se, že soubor OneNote není zamčený a JRE má oprávnění přistupovat k tiskárně. |
| **PDF výstup je prázdný** | Zkontrolujte, že ovladač virtuální tiskárny je správně nainstalován a nastaven jako výchozí pro danou tiskovou úlohu. |
| **Nesprávný rozsah stránek** | Pamatujte, že čísla stránek jsou 1‑základní; `setPrintRange(1, 2)` vytiskne první dvě stránky. |

## Často kladené otázky

### Q1: Mohu tisknout konkrétní stránky dokumentu OneNote?
**A:** Ano, použijte `asposeAttr.setPrintRange(startPage, endPage)` pro omezení výstupu na požadované stránky.

### Q2: Je Aspose.Note pro Java kompatibilní s virtuálními tiskárnami?
**A:** Rozhodně. Knihovna funguje s jakoukoli tiskárnou, kterou Windows zpřístupní, včetně virtuálních PDF tiskáren.

### Q3: Mohu přizpůsobit nastavení tisku, například počet kopií?
**A:** Ano, zavolejte `asposeAttr.setCopies(numberOfCopies)` před voláním `print()`.

### Q4: Vyžaduje Aspose.Note pro Java licenci pro tisk dokumentů?
**A:** Platná licence je vyžadována pro produkční nasazení; pro hodnocení je k dispozici dočasná zkušební licence.

### Q5: Kde najdu další podporu a zdroje pro Aspose.Note pro Java?
**A:** Navštivte oficiální stránku podpory na **[Aspose.Note pro Java podpora](https://forum.aspose.com/c/note/28)** pro fóra, dokumentaci a příklady.

---

**Poslední aktualizace:** 2026-01-18  
**Testováno s:** Aspose.Note pro Java 24.12 (nejnovější v době psaní)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}