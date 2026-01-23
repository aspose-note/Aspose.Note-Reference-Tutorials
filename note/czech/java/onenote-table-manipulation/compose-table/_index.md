---
date: 2026-01-23
description: Naučte se, jak programově přidat tabulku do OneNote pomocí Aspose.Note
  pro Javu. Krok za krokem průvodce pro efektivní tvorbu dokumentů.
linktitle: How to add table to OneNote with Aspose.Note for Java
second_title: Aspose.Note Java API
title: Jak přidat tabulku do OneNote pomocí Aspose.Note pro Javu
url: /cs/java/onenote-table-manipulation/compose-table/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak přidat tabulku do OneNote pomocí Aspose.Note pro Java

## Úvod
V tomto tutoriálu se naučíte, jak **přidat tabulku do OneNote** pomocí Aspose.Note pro Java, což vám umožní programově vytvářet bohaté, strukturované dokumenty, které zlepšují spolupráci a reportování. Aspose.Note poskytuje výkonné API pro tvorbu stránek OneNote, osnov a tabulek bez ručního editování.

## Rychlé odpovědi
- **Co tento tutoriál pokrývá?** Přidání tabulky do OneNote pomocí Aspose.Note pro Java.  
- **Kolik času je potřeba?** Přibližně 10‑15 minut pro základní implementaci.  
- **Potřebuji licenci?** Bezplatná zkušební verze stačí pro hodnocení; pro produkční nasazení je vyžadována komerční licence.  
- **Jaká verze Javy je podporována?** Java 8 a novější.  
- **Mohu přizpůsobit styly tabulky?** Ano – můžete pomocí API měnit písma, barvy a okraje buněk.

## Požadavky
Před zahájením tutoriálu se ujistěte, že máte následující předpoklady:
- Základní znalosti programování v Javě.  
- Knihovnu Aspose.Note pro Java nainstalovanou. Můžete ji stáhnout [zde](https://releases.aspose.com/note/java/).  
- Integrované vývojové prostředí (IDE) nastavené pro vývoj v Javě.

## Import balíčků
Ujistěte se, že importujete potřebné balíčky pro rozjezd vašeho projektu. Přidejte následující importy do vaší Java třídy:

```java
import com.aspose.note.*;
import java.awt.*;
import java.io.IOException;
import java.nio.file.Paths;
import java.util.stream.StreamSupport;
```

## Krok 1: Nastavte adresář dokumentu
```java
String dataDir = "Your Document Directory";
```
Nahraďte `"Your Document Directory"` skutečnou cestou, kam chcete uložit svůj OneNote dokument.

## Krok 2: Vytvořte záhlaví
```java
RichText headerText = new RichText().append("Super contest for suppliers.");
headerText.setParagraphStyle(new ParagraphStyle().setFontSize(18).setBold(true));
headerText.setAlignment(HorizontalAlignment.Center);
```
Vytvořte poutavé záhlaví pro váš dokument. Podle potřeby upravte velikost písma, tučnost a zarovnání.

## Krok 3: Vytvořte stránku a osnovu
```java
Page page = new Page();
Outline outline = page.appendChildLast(new Outline());
outline.setHorizontalOffset(50);
outline.appendChildLast(new OutlineElement()).appendChildLast(headerText);
```
Nastavte novou stránku a osnovu, poté přidejte dříve vytvořené záhlaví do osnovy.

## Krok 4: Přidejte souhrnný text
```java
RichText bodyTextHeader = outline.appendChildLast(new OutlineElement()).appendChildLast(new RichText());
bodyTextHeader.setParagraphStyle(ParagraphStyle.getDefault());
bodyTextHeader.append("This is the final ranking of proposals got from our suppliers.");
```
Vložte stručný souhrnný text, který poskytne kontext pro tabulku.

## Krok 5: Přidejte tabulku do OneNote
```java
Table ranking = outline.appendChildLast(new OutlineElement()).appendChildLast(new Table());
// Remaining steps are involved in setting up the table structure, header row, and adding empty rows.
// Refer to the provided code for detailed implementation.
```
Sestavte strukturu tabulky a naplňte ji relevantními informacemi. Poskytnutý kód zahrnuje přidání sloupců, řádku záhlaví, prázdných řádků a šablonového obsahu pro sloupec „Contacts“.

## Krok 6: Uložte dokument
```java
Document d = new Document();
d.appendChildLast(page);
d.save(Paths.get(dataDir, "ComposeTable_out.one").toString());
```
Uložte svůj vytvořený dokument se zadaným názvem souboru a cestou k adresáři.

## Závěr
Gratulujeme! Úspěšně jste **přidali tabulku do OneNote** pomocí Aspose.Note pro Java. Tento tutoriál vám ukázal krok‑za‑krokem proces, který vám umožní programově rozšířit možnosti tvorby dokumentů.

## Často kladené otázky
### Q: Kde najdu dokumentaci k Aspose.Note pro Java?
Dokumentaci najdete [zde](https://reference.aspose.com/note/java/).

### Q: Jak si mohu stáhnout Aspose.Note pro Java?
Stáhnout ji můžete z [tohoto odkazu](https://releases.aspose.com/note/java/).

### Q: Je k dispozici bezplatná zkušební verze?
Ano, bezplatnou zkušební verzi získáte [zde](https://releases.aspose.com/).

### Q: Kde mohu získat podporu pro Aspose.Note pro Java?
Navštivte fórum podpory [zde](https://forum.aspose.com/c/note/28).

### Q: Mohu získat dočasnou licenci?
Ano, dočasnou licenci můžete získat [zde](https://purchase.aspose.com/temporary-license/).

---

**Poslední aktualizace:** 2026-01-23  
**Testováno s:** Aspose.Note pro Java (nejnovější verze)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}