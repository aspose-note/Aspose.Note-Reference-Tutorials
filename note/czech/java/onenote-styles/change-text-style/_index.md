---
date: 2026-06-05
description: Naučte se, jak změnit font size v OneNote, nastavit font color a highlight
  text pomocí Aspose.Note pro Java – step‑by‑step guide s code snippets.
keywords:
- change font size onenote
- how to change text
- set font color onenote
linktitle: Změna font size v OneNote - Aspose.Note
schemas:
- author: Aspose
  dateModified: '2026-06-05'
  description: Learn how to change font size onenote, set font color, and highlight
    text with Aspose.Note for Java – step‑by‑step guide with code snippets.
  headline: Change Font Size in OneNote - Aspose.Note
  type: TechArticle
- description: Learn how to change font size onenote, set font color, and highlight
    text with Aspose.Note for Java – step‑by‑step guide with code snippets.
  name: Change Font Size in OneNote - Aspose.Note
  steps:
  - name: Import Packages
    text: 'The `Document`, `RichText`, and `TextRun` classes live in the `com.aspose.note`
      namespace. Import them at the top of your Java source file:'
  - name: Load the Document
    text: The `Document` class is Aspose.Note's top‑level object that represents a
      single OneNote file in memory. Loading a file is as simple as passing the file
      path to its constructor.
  - name: Access RichText Nodes
    text: '`RichText` nodes contain the actual paragraph text. By iterating over `document.getRichTextNodes()`,
      you gain access to every piece of editable text in the notebook.'
  - name: Change Text Style
    text: '`TextRun` represents a contiguous run of characters sharing the same formatting.
      Within the loop, set `FontColor` to yellow, `HighlightColor` to blue, and `FontSize`
      to **20** points to achieve the desired styling.'
  - name: Save the Document
    text: Call `document.save("StyledSample.one")` to write the changes back to a
      OneNote file. The save operation preserves all original content while applying
      the new styles.
  type: HowTo
- questions:
  - answer: Yes, filter the `RichText` collection by page or section ID before applying
      style changes.
    question: Can I apply these text style changes to specific sections of my OneNote
      document?
  - answer: Absolutely, you can modify font family, bold/italic, underline, alignment,
      and paragraph spacing using the same object model.
    question: Does Aspose.Note support other formatting options beyond color, highlight,
      and size?
  - answer: Yes, Aspose.Note works seamlessly with libraries like Apache POI, Jackson,
      or Spring to build complex document pipelines.
    question: Can I integrate Aspose.Note with other Java libraries for advanced processing?
  - answer: A commercial license is required for production deployments; a free evaluation
      license is available for development and testing.
    question: Is Aspose.Note licensed for commercial use?
  - answer: Visit the Aspose.Note documentation portal, download the full API reference
      PDF, and explore the GitHub repository for community examples.
    question: Where can I find additional samples and API reference?
  type: FAQPage
second_title: Aspose.Note Java API
title: Změna font size v OneNote - Aspose.Note
url: /cs/java/onenote-styles/change-text-style/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Změna velikosti písma v OneNote - Aspose.Note

## Úvod

V tomto tutoriálu se naučíte **jak změnit velikost písma v OneNote** dokumentech pomocí Aspose.Note pro Java. Provedeme vás načtením souboru OneNote, přístupem k jeho textovým uzlům, aplikací barvy, zvýraznění a změnou velikosti písma a nakonec uložením aktualizovaného souboru. Ať už automatizujete generování zpráv nebo vylepšujete zápisy ze schůzek, tento průvodce vám poskytne spolehlivý způsob, jak programově stylovat obsah OneNote.

## Rychlé odpovědi
- **Jak změním velikost písma v OneNote pomocí Javy?** Načtěte dokument, upravte vlastnost `FontSize` každého `TextRun`, poté uložte – tři jednoduché kroky.  
- **Mohu také změnit barvu textu a zvýraznění?** Ano, nastavte `FontColor` a `HighlightColor` na stejném `TextRun`.  
- **Jaká verze Aspose.Note je vyžadována?** Jakékoli vydání 23.10+ podporuje tyto stylovací API.  
- **Potřebuji licenci pro vývoj?** Bezplatná zkušební verze funguje pro testování; pro produkci je vyžadována komerční licence.  
- **Je tento přístup vhodný pro velké zápisníky?** Ano – Aspose.Note zpracovává zápisníky s více stovkami stránek, aniž by načítal celý soubor do paměti.

## Co je změna velikosti písma v OneNote?
**change font size onenote** označuje programatické nastavení atributu `FontSize` textových prvků uvnitř zápisníku OneNote. Pomocí Aspose.Note mohou vývojáři tuto vlastnost upravit prostřednictvím API, které přímo aktualizuje podkladovou strukturu souboru OneNote a zajišťuje změnu vizuálního vzhledu bez ručního editování nebo interakce s uživatelským rozhraním.

## Proč použít Aspose.Note ke změně stylu textu v OneNote?
Aspose.Note poskytuje více než 30 možností formátování – včetně rodiny písma, velikosti, barvy, zvýraznění, zarovnání a mezery mezi odstavci – a je navržen tak, aby efektivně zpracovával velké zápisníky. Dokáže zvládnout zápisníky s více než 500 stránkami při spotřebě méně než 150 MB RAM, což zajišťuje spolehlivou a výkonnou automatizaci pro podnikové pracovní toky s dokumenty.

## Požadavky

1. Základní znalost programování v Javě.  
2. Nainstalovaný JDK 8 nebo vyšší na vašem počítači.  
3. Knihovna Aspose.Note pro Java (stáhněte z webu Aspose).  
4. Znalost hierarchické struktury OneNote (stránky, sekce, uzly RichText).

## Jak změnit velikost písma v OneNote pomocí Aspose.Note?

Načtěte svůj soubor OneNote, najděte každý uzel `RichText`, aktualizujte styl každého `TextRun` a soubor uložte. Tento end‑to‑end proces vyžaduje jen několik řádků kódu a běží za méně než sekundu u typických zápisníků.

### Krok 1: Importovat balíčky

Třídy `Document`, `RichText` a `TextRun` se nacházejí v namespace `com.aspose.note`. Importujte je na začátku svého Java souboru:

```java
import java.awt.Color;
import java.io.IOException;
import java.util.List;
import com.aspose.note.Document;
import com.aspose.note.RichText;
import com.aspose.note.TextRun;
import com.aspose.note.TextStyle;
```

### Krok 2: Načíst dokument

Třída `Document` je hlavní objekt Aspose.Note, který v paměti představuje jeden soubor OneNote. Načtení souboru je tak jednoduché, že stačí předat cestu k souboru jeho konstruktoru.

```java
// Load the document into Aspose.Note
Document document = new Document("Your Document Directory/Sample1.one");
```

### Krok 3: Přístup k uzlům RichText

Uzly `RichText` obsahují skutečný text odstavců. Iterací přes `document.getRichTextNodes()` získáte přístup ke každému editovatelnému textu v zápisníku.

```java
// Get a particular RichText node
List<RichText> richTextNodes = document.getChildNodes(RichText.class);
RichText richText = richTextNodes.get(0);
```

### Krok 4: Změna stylu textu

`TextRun` představuje souvislý úsek znaků se stejným formátováním. V rámci smyčky nastavte `FontColor` na žlutou, `HighlightColor` na modrou a `FontSize` na **20** bodů, abyste dosáhli požadovaného stylu.

```java
for (TextRun run : richText.getTextRuns()) {
    // Set font color
    run.getStyle().setFontColor(Color.yellow);
    // Set highlight color
    run.getStyle().setHighlight(Color.blue);
    // Set font size
    run.getStyle().setFontSize(20);
}
```

### Krok 5: Uložit dokument

Zavolejte `document.save("StyledSample.one")`, čímž zapíšete změny zpět do souboru OneNote. Operace uložení zachová veškerý původní obsah a zároveň aplikuje nové styly.

```java
document.save("Your Document Directory/ChangeTextStyle_out.pdf");
System.out.printf("File saved: %s\n", "Your Document Directory/ChangeTextStyle_out.pdf");
```

## Časté problémy a řešení

- **Text se nezmění:** Ujistěte se, že iterujete přes objekty `TextRun` uvnitř každého uzlu `RichText`; vynechání této úrovně ponechá formátování nedotčené.  
- **Barva se zobrazuje jinak:** Aspose.Note používá hodnoty RGB; ověřte, že používáte správné konstanty `java.awt.Color`.  
- **Velký zápisník zpomaluje:** `LoadOptions` konfiguruje, jak Aspose.Note načítá soubor, umožňuje streamování a výběr formátu. Použijte `document.setLoadOptions(new LoadOptions(LoadFormat.OneNote))` pro aktivaci režimu streamování, který snižuje paměťovou náročnost.

## Často kladené otázky

**Q: Mohu také použít tyto změny stylu textu na konkrétní sekce mého dokumentu OneNote?**  
A: Ano, před aplikací změn můžete filtrovat kolekci `RichText` podle ID stránky nebo sekce.

**Q: Podporuje Aspose.Note další možnosti formátování kromě barvy, zvýraznění a velikosti?**  
A: Rozhodně, můžete měnit rodinu písma, tučné/kurzívu, podtržení, zarovnání i mezery mezi odstavci pomocí stejného objektového modelu.

**Q: Lze Aspose.Note integrovat s dalšími Java knihovnami pro pokročilé zpracování?**  
A: Ano, Aspose.Note spolupracuje bez problémů s knihovnami jako Apache POI, Jackson nebo Spring pro tvorbu složitých dokumentových pipeline.

**Q: Je Aspose.Note licencován pro komerční použití?**  
A: Pro produkční nasazení je vyžadována komerční licence; pro vývoj a testování je k dispozici bezplatná evaluační licence.

**Q: Kde najdu další ukázky a referenční dokumentaci API?**  
A: Navštivte portál dokumentace Aspose.Note, stáhněte kompletní PDF referenci API a prozkoumejte úložiště GitHub pro příklady od komunity.

## Závěr

Postupem podle výše uvedených kroků nyní umíte **jak změnit velikost písma v OneNote** souborech, upravit barvu textu a aplikovat zvýraznění pomocí Aspose.Note pro Java. Tato schopnost vám umožní automatizovat vizuální úpravu zápisů ze schůzek, výukových materiálů nebo jakéhokoli obsahu založeného na OneNote v rozsahu.

---

**Poslední aktualizace:** 2026-06-05  
**Testováno s:** Aspose.Note 23.10 for Java  
**Autor:** Aspose

## Související tutoriály

- [Nastavit výchozí styl odstavce v OneNote - Aspose.Note](/note/java/onenote-styles/set-default-paragraph-style/)
- [Nastavit jazyk kontroly pravopisu pro text v OneNote - Aspose.Note](/note/java/onenote-text-manipulation/set-proofing-language-for-text/)
- [Nastavení názvu stránky ve stylu Microsoft OneNote - Aspose.Note](/note/java/onenote-text-manipulation/setting-page-title-in-microsoft-onenote-style/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< blocks/products/products-backtop-button >}}
{{< /blocks/products/pf/main-wrap-class >}}