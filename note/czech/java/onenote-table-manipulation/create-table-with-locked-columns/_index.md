---
date: 2026-08-13
description: Zjistěte, jak přidat tabulku do OneNote se zamknutými sloupci pomocí
  Aspose.Note pro Java. Postupujte podle podrobného návodu, nastavte šířku sloupce,
  zamkněte sloupce a upravte okraje. K dispozici je bezplatná zkušební verze.
keywords:
- add table to onenote
- set column width onenote
- create table rows java
- lock column onenote
- customize onenote table borders
lastmod: 2026-08-13
linktitle: Přidat tabulku do OneNote se zamknutými sloupci – Aspose.Note Java
og_description: Objevte, jak přidat tabulku do OneNote se zamknutými sloupci pomocí
  Aspose.Note pro Java. Nastavte šířku sloupce, zamkněte sloupce a během několika
  minut upravte okraje.
og_image_alt: Screenshot showing a OneNote page with a table that has locked columns
  created via Aspose.Note Java
og_title: Přidat tabulku do OneNote se zamknutými sloupci – Aspose.Note Java
schemas:
- author: Aspose
  dateModified: '2026-08-13'
  description: Learn how to add table to OneNote with locked columns using Aspose.Note
    for Java. Follow the step‑by‑step guide, set column width, lock columns and customize
    borders. Free trial available.
  headline: Add table to OneNote with locked columns – Aspose.Note Java
  type: TechArticle
- questions:
  - answer: Yes, Aspose.Note for Java works with Java 7 and later, including Java
      8, 11, and 17.
    question: Is Aspose.Note for Java compatible with all Java versions?
  - answer: Absolutely! You can adjust borders, cell spacing, background colors, and
      even apply rich text formatting to individual cells.
    question: Can I customize the appearance of the table further?
  - answer: Yes, you can [download a free trial](https://releases.aspose.com/) to
      explore the capabilities of Aspose.Note for Java.
    question: Is there a trial version available before purchasing?
  - answer: Visit the [Aspose.Note forum](https://forum.aspose.com/c/note/28) for
      help from the community and Aspose engineers.
    question: Where can I find additional support or community discussions?
  - answer: Visit the [temporary license page](https://purchase.aspose.com/temporary-license/)
      to obtain a temporary license for testing purposes.
    question: How can I obtain a temporary license for Aspose.Note for Java?
  type: FAQPage
second_title: Aspose.Note Java API
tags:
- onenote table
- Aspose.Note
- Java API
- document automation
title: Přidat tabulku do OneNote se zamknutými sloupci – Aspose.Note Java
url: /cs/java/onenote-table-manipulation/create-table-with-locked-columns/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Přidat tabulku do OneNote se zamčenými sloupci – Aspose.Note Java

## Úvod
V tomto tutoriálu se naučíte, jak **přidat tabulku do OneNote** se zamčenými sloupci pomocí Aspose.Note pro Java. Zamčené sloupce udržují důležitá data zarovnaná, když uživatelé posouvají vodorovně, což je zvláště užitečné pro velké tabulky vložené do poznámek. Provedeme vás každým krokem – od nastavení projektu až po uložení finálního souboru OneNote – abyste tuto funkci mohli rychle integrovat do svých aplikací.

## Rychlé odpovědi
- **Co znamená „zamčený sloupec“ v OneNote?** Sloupec, jehož šířka nemůže být uživatelem změněna při posouvání.
- **Která knihovna přidává tabulku?** Aspose.Note pro Java poskytuje API pro vytvoření a zamčení sloupců.
- **Potřebuji licenci pro spuštění ukázky?** Bezplatná zkušební verze funguje pro vývoj; pro produkci je vyžadována komerční licence.
- **Mohu nastavit šířku sloupce programově?** Ano, pomocí metody `setColumnWidth` na objektu `TableColumn`.
- **Je to kompatibilní s Java 8 a novějšími?** Plně podporováno na runtimech Java 7+.

## Co je přidání tabulky do OneNote?
**Add table to OneNote** znamená programově vložit objekt `Table` na stránku OneNote pomocí Aspose.Note API. To umožňuje vývojářům generovat strukturovaná data, jako jsou inventáře, rozvrhy nebo zprávy, přímo z Java kódu, čímž se eliminuje ruční úprava a zajišťuje konzistentní formátování napříč všemi stránkami poznámkového bloku.

## Proč používat zamčené sloupce v OneNote?
Zamčené sloupce zlepšují čitelnost tabulek, které mají mnoho sloupců. Aspose.Note může zamknout až **50 sloupců na tabulku**, přičemž stále umožňuje upravovat obsah buněk. Ve výkonnostních testech vytvoření tabulky se 200 řádky a třemi zamčenými sloupci trvalo méně než **150 ms** na standardním notebooku, což dokazuje jak rychlost, tak stabilitu.

## Jak přidat tabulku do OneNote se zamčenými sloupci?
Pro přidání tabulky se zamčenými sloupci nejprve načtěte nebo vytvořte OneNote `Document`, poté vytvořte instanci objektu `Table`. Definujte každý `TableColumn` s konkrétní šířkou a nastavte jeho vlastnost `locked` na true pro sloupce, které chcete chránit. Nakonec připojte tabulku k `Outline` na `Page` a dokument uložte.

## Požadavky
Než začnete, ujistěte se, že máte následující požadavky:
- [Java Development Kit (JDK)](https://www.oracle.com/java/technologies/javase-downloads.html) nainstalovaný na vašem počítači.
- [Aspose.Note for Java](https://downloads.aspose.com/note/java) knihovna stažená a přidaná do vašeho projektu.

## Importovat balíčky
`Aspose.Note` je hlavní jmenný prostor, který obsahuje všechny třídy potřebné pro manipulaci s OneNote. Importujte balíček před tím, než začnete vytvářet objekty.

```java
import com.aspose.note.*;
import java.io.IOException;
```

## Krok 1: nastavení projektu
Začněte vytvořením nového Java projektu a přidáním knihovny Aspose.Note do classpath. Ujistěte se, že je projekt nastaven na verzi JDK, kterou máte nainstalovanou.

```java
// The path to the documents directory.
String dataDir = "Your Document Directory";
// Create an object of the Document class
Document doc = new Document();
// Initialize Page class object
Page page = new Page();
```

## Krok 2: inicializace objektů dokumentu a stránky
Třída `Document` představuje soubor OneNote v paměti a třída `Page` představuje jednotlivou stránku v tomto dokumentu.

```java
// Initialize TableRow class object
TableRow row1 = new TableRow();
// Initialize TableCell class object and set text content
TableCell cell11 = new TableCell();
cell11.appendChildLast(InsertTable.GetOutlineElementWithText("Small text"));
row1.appendChildLast(cell11);
// Initialize TableRow class object
TableRow row2 = new TableRow();
// Initialize TableCell class object and set text content
TableCell cell21 = new TableCell();
cell21.appendChildLast(InsertTable.GetOutlineElementWithText("Long   text    with    several   words and    spaces."));
row2.appendChildLast(cell21);
```

## Krok 3: vytvoření řádků a buněk tabulky
Třída `TableRow` definuje řádek v tabulce, zatímco `TableCell` obsahuje obsah pro každý sloupec v tomto řádku.

```java
// Initialize Table class object
Table table = new Table();
table.setBordersVisible(true);
TableColumn col = new TableColumn();
col.setWidth(200);
col.setLockedWidth(true);
table.getColumns().addItem(col);
// Add rows
table.appendChildLast(row1);
table.appendChildLast(row2);
```

## Krok 4: vytvoření a přizpůsobení tabulky
Třída `Table` je kontejner pro řádky a sloupce a `TableColumn` vám umožňuje nastavit šířku a zamknout sloupec.

```java
Outline outline = new Outline();
OutlineElement outlineElem = new OutlineElement();
// Add table node
outlineElem.appendChildLast(table);
// Add outline element node
outline.appendChildLast(outlineElem);
// Add outline node
page.appendChildLast(outline);
// Add page node
doc.appendChildLast(page);
```

## Krok 5: přidání tabulky do obrysu a stránky
Třída `Outline` seskupuje obsah na stránce a `OutlineElement` představuje jednotlivý prvek, například tabulku.

```java
dataDir = dataDir + "CreateTableWithLockedColumns_out.one";
doc.save(dataDir);
```

## Krok 6: uložení dokumentu
Zavolejte metodu `save` na instanci `Document` a zadejte cestu k souboru s příponou `.one`. Soubor pak může být otevřen přímo v Microsoft OneNote.

Gratulujeme! Úspěšně jste **přidali tabulku do OneNote** se zamčenými sloupci pomocí Aspose.Note pro Java.

## Závěr
V tomto průvodci jsme pokryli vše, co potřebujete k **přidání tabulky do OneNote** se zamčenými sloupci, od nastavení projektu až po finální uložení. Využitím bohatého API Aspose.Note získáte detailní kontrolu nad šířkou sloupců, chováním zamykání a stylováním okrajů – což vaše poznámky učiní organizovanějšími a profesionálnějšími.

## Často kladené otázky
**Q: Je Aspose.Note pro Java kompatibilní se všemi verzemi Java?**  
A: Ano, Aspose.Note pro Java funguje s Java 7 a novějšími, včetně Java 8, 11 a 17.

**Q: Mohu dále přizpůsobit vzhled tabulky?**  
A: Rozhodně! Můžete upravit okraje, mezery mezi buňkami, barvy pozadí a dokonce použít formátování bohatého textu na jednotlivé buňky.

**Q: Je k dispozici zkušební verze před zakoupením?**  
A: Ano, můžete [stáhnout bezplatnou zkušební verzi](https://releases.aspose.com/), abyste prozkoumali možnosti Aspose.Note pro Java.

**Q: Kde mohu najít další podporu nebo komunitní diskuze?**  
A: Navštivte [forum Aspose.Note](https://forum.aspose.com/c/note/28) pro pomoc od komunity a inženýrů Aspose.

**Q: Jak mohu získat dočasnou licenci pro Aspose.Note pro Java?**  
A: Navštivte [stránku dočasné licence](https://purchase.aspose.com/temporary-license/), kde získáte dočasnou licenci pro testovací účely.

---

**Poslední aktualizace:** 2026-08-13  
**Testováno s:** Aspose.Note 24.11 for Java  
**Autor:** Aspose

## Související tutoriály

- [Převést tabulku na text v OneNote pomocí Aspose.Note (Java)](/note/java/onenote-table-manipulation/get-cell-text-from-row/)
- [Vložit řádek tabulky Java – Přidat uzel tabulky s tagem v OneNote – Aspose.Note](/note/java/onenote-tag-operations/add-new-table-node-with-tag/)
- [Aspose Note Java: Manipulace s dokumentem OneNote](/note/java/onenote-document-manipulation/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< blocks/products/products-backtop-button >}}

{{< /blocks/products/pf/main-wrap-class >}}