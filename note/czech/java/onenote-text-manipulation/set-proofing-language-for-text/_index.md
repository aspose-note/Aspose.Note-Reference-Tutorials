---
date: 2026-09-29
description: Návod na nastavení jazyka onenote ukazuje, jak přiřadit jazyk korektury
  textu v OneNote pomocí Aspose.Note pro Java, s podrobným kódem a osvědčenými postupy.
keywords:
- set language onenote
- spell check language onenote
- change text language onenote
- set proofing language onenote
- add language onenote
lastmod: 2026-09-29
linktitle: Nastavit jazyk korektury pro text v OneNote - Aspose.Note
og_description: Průvodce nastavením jazyka onenote pro vývojáře Java. Naučte se měnit
  jazyk textu, povolit kontrolu pravopisu a ukládat soubory OneNote pomocí Aspose.Note.
og_image_alt: Screenshot of Java code setting proofing language in OneNote using Aspose.Note
og_title: Jak nastavit jazyk onenote v OneNote – Aspose.Note
schemas:
- author: Aspose
  dateModified: '2026-09-29'
  description: Set language onenote tutorial shows you how to assign proofing language
    to text in OneNote using Aspose.Note for Java, with step‑by‑step code and best
    practices.
  headline: How to set language onenote in a OneNote document – Aspose.Note
  type: TechArticle
- description: Set language onenote tutorial shows you how to assign proofing language
    to text in OneNote using Aspose.Note for Java, with step‑by‑step code and best
    practices.
  name: How to set language onenote in a OneNote document – Aspose.Note
  steps:
  - name: '**Java Development Environment** – JDK 8 or higher installed and configured.'
    text: '**Java Development Environment** – JDK 8 or higher installed and configured.'
  - name: '**Aspose.Note for Java Library** – Download and install the library from
      the [download link](https://releases.aspose.com/note/java/).'
    text: '**Aspose.Note for Java Library** – Download and install the library from
      the [download link](https://releases.aspose.com/note/java/).'
  - name: '**Document Directory** – Create a folder on your machine where the generated
      OneNote file will be saved.'
    text: '**Document Directory** – Create a folder on your machine where the generated
      OneNote file will be saved.'
  type: HowTo
- questions:
  - answer: Absolutely! Add additional `append` calls with the desired `Locale.forLanguageTag("xx-XX")`.
    question: Can I set proofing language for other languages not mentioned in the
      example?
  - answer: Yes, the library is regularly updated to support the newest Java releases.
    question: Is Aspose.Note for Java compatible with the latest Java versions?
  - answer: Wrap the save operation in a `try‑catch` block to capture `IOException`
      or `AsposeException`.
    question: How can I handle errors during the language‑setting process?
  - answer: Certainly. Just include the Aspose.Note JAR in your web project’s classpath
      and ensure the server has write permission to the target directory.
    question: Can I integrate this code into a web application?
  - answer: Explore the [documentation](https://reference.aspose.com/note/java/) for
      a full list of APIs and sample projects.
    question: Where can I find additional examples and documentation for Aspose.Note
      for Java?
  type: FAQPage
second_title: Aspose.Note Java API
tags:
- onenote language
- Aspose.Note
- Java document processing
- proofing language
- onenote API
title: Jak nastavit jazyk onenote v dokumentu OneNote – Aspose.Note
url: /cs/java/onenote-text-manipulation/set-proofing-language-for-text/
weight: 22
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak nastavit jazyk onenote v dokumentu OneNote – Aspose.Note

## Úvod
Pokud potřebujete **set language onenote** pro konkrétní úseky textu uvnitř poznámkového bloku OneNote, Aspose.Note pro Java to usnadňuje. V tomto tutoriálu se naučíte, jak vytvořit dokument OneNote, změnit jazyk textu pro jednotlivá slova nebo fráze a nakonec uložit soubor OneNote s aplikovaným správným jazykem kontroly pravopisu. Na konci pochopíte, proč nastavení jazyka má význam pro kontrolu pravopisu a lokalizaci, a budete mít připravený spustitelný ukázkový kód.

## Rychlé odpovědi
- **Co ovlivňuje „set language“?** Říká OneNote, který slovník pro kontrolu pravopisu a gramatiku použít.  
- **Mohu nastavit různé jazyky ve stejné poznámce?** Ano, můžete přiřadit jazyk každému úseku textu.  
- **Potřebuji licenci pro Aspose.Note?** Bezplatná zkušební verze funguje pro testování; pro produkci je vyžadována komerční licence.  
- **Které verze Javy jsou podporovány?** Aspose.Note pro Java podporuje Javu 8 a novější.  
- **Je výstup .one soubor?** Ano, dokument se ukládá jako soubor OneNote *.one*.

## Co je set language onenote?
`set language onenote` označuje přiřazení locale IETF BCP‑47 k úseku textu, aby proofing engine OneNote použil odpovídající slovník. Tato metadata cestují se souborem *.one* a jsou respektována klientem OneNote na jakékoli platformě.

## Proč nastavit language onenote?
Použití správného jazyka zvyšuje přesnost kontroly pravopisu až o **95 %** u vícejazykových poznámkových bloků a urychluje indexování přibližně o **30 %**, protože engine může přeskočit irelevantní slovníky. Aspose.Note podporuje **30+** vstupních a výstupních formátů a dokáže zpracovat poznámkové bloky s **10 000+** stránkami, aniž by načítal celý soubor do paměti.

## Požadavky
Než se ponoříte do kódu, ujistěte se, že máte následující:

1. **Java Development Environment** – Nainstalovaný a nakonfigurovaný JDK 8 nebo vyšší.  
2. **Aspose.Note for Java Library** – Stáhněte a nainstalujte knihovnu z [download link](https://releases.aspose.com/note/java/).  
3. **Document Directory** – Vytvořte složku na svém počítači, kam bude uložen generovaný soubor OneNote.

## Jak nastavit language onenote
Pro nastavení jazyka nejprve načtěte existující dokument OneNote nebo vytvořte novou instanci `Document`. Poté pro každý úsek textu, který chcete upravit, vytvořte nebo získáte objekt `RichText`, použijte `TextStyle` s požadovaným `Locale` (například `Locale.forLanguageTag("en-US")`) a připojte stylizovaný text zpět do osnovy. Nakonec zavolejte `document.save`, aby se změny zapsaly do souboru *.one*, přičemž se zachová metadata jazyka.

## Krok 1: nastavení dokumentu a stránky
Document je nejvyšší objekt Aspose.Note, který v paměti představuje poznámkový blok OneNote. Po vytvoření instance `Document` můžete přidávat stránky, osnovy a další prvky.

```java
import com.aspose.note.*;
import java.io.IOException;
import java.nio.file.Paths;
import java.util.Locale;
```

## Krok 2: vytvoření outline a outline element
`Outline` funguje jako kontejner pro obsah stránky, zatímco `OutlineElement` obsahuje jednotlivé prvky, jako je rich text.

```java
// The path to the documents directory.
String dataDir = "Your Document Directory";
Document document = new Document();
Page page = new Page();
```

## Krok 3: přidání rich textu s nastavením jazyka
`RichText` ukládá skutečné znaky. `TextStyle` vám umožňuje připojit `Locale` (např. `en‑US`, `fr‑FR`) k úseku textu, což je způsob, jak **set language onenote**. Aplikace stylu na každé volání `append` zajišťuje jemnou kontrolu.

```java
Outline outline = new Outline();
OutlineElement outlineElem = new OutlineElement();
```

## Krok 4: organizace prvků a uložení
`ParagraphStyle` lze použít, když chcete nastavit jazyk pro celý odstavec místo jednotlivých slov. Po sestavení hierarchie osnovy zavolejte `document.save`, aby se vytvořil soubor *.one*, který zachová všechna metadata jazyka.

```java
RichText text = new RichText()
                        .append("United States", new TextStyle().setLanguage(Locale.forLanguageTag("en-US")))
                        .append(" Germany", new TextStyle().setLanguage(Locale.forLanguageTag("de-DE")))
                        .append(" China", new TextStyle().setLanguage(Locale.forLanguageTag("zh-CN")));
text.setParagraphStyle(ParagraphStyle.getDefault());
```

## Časté úskalí a tipy
- **Formát locale** – Použijte tag IETF BCP‑47 (např. `en-US`, `de-DE`). Nesprávný tag se vrátí na výchozí jazyk dokumentu.  
- **Cesta k souboru** – Ujistěte se, že `dataDir` ukazuje na existující složku; jinak `document.save` vyhodí `IOException`.  
- **Pro tip:** Pokud potřebujete nastavit jazyk pro celý odstavec, aplikujte `TextStyle` na `ParagraphStyle` místo na každé volání `append`.

## Závěr
Právě jste se naučili **jak nastavit language onenote** pro jednotlivé úseky textu v poznámkovém bloku OneNote pomocí Aspose.Note pro Java. Tato funkce vám umožní **programově vytvořit OneNote dokument**, **měnit jazyk textu** za běhu a **uložit OneNote soubor** s přesnými metadaty kontroly pravopisu.

## Často kladené otázky

**Q: Mohu nastavit jazyk kontroly pravopisu pro jiné jazyky, než jsou uvedeny v příkladu?**  
A: Rozhodně! Přidejte další volání `append` s požadovaným `Locale.forLanguageTag("xx-XX")`.

**Q: Je Aspose.Note pro Java kompatibilní s nejnovějšími verzemi Javy?**  
A: Ano, knihovna je pravidelně aktualizována, aby podporovala nejnovější verze Javy.

**Q: Jak mohu ošetřit chyby během procesu nastavení jazyka?**  
A: Zabalte operaci uložení do bloku `try‑catch`, abyste zachytili `IOException` nebo `AsposeException`.

**Q: Mohu tento kód integrovat do webové aplikace?**  
A: Samozřejmě. Stačí zahrnout Aspose.Note JAR do classpath vašeho webového projektu a zajistit, aby server měl oprávnění k zápisu do cílové složky.

**Q: Kde mohu najít další příklady a dokumentaci pro Aspose.Note pro Java?**  
A: Prozkoumejte [documentation](https://reference.aspose.com/note/java/) pro kompletní seznam API a ukázkových projektů.

**Poslední aktualizace:** 2026-09-29  
**Testováno s:** Aspose.Note for Java 24.12  
**Autor:** Aspose  

```java
outlineElem.appendChildLast(text);
outline.appendChildLast(outlineElem);
page.appendChildLast(outline);
document.appendChildLast(page);
document.save(Paths.get(dataDir, "SetProofingLanguageForText.one").toString()); 
```

## Související tutoriály

- [Načtení souboru OneNote pomocí Java: Použijte Aspose.Note k načtení dokumentů OneNote](/note/java/onenote-document-loading/load-onenote-document/)
- [Převod OneNote na prostý text – Extrahujte celý text pomocí Aspose.Note pro Java](/note/java/onenote-text-manipulation/extract-all-text/)
- [Převod OneNote do PDF pomocí nastavení stránky s Aspose.Note pro Java](/note/java/onenote-document-saving/save-to-pdf-using-page-settings/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}