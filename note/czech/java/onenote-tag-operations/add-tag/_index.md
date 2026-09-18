---
date: 2026-01-28
description: Naučte se, jak vytvořit osnovu v OneNote, přidat značku do OneNote a
  vygenerovat PDF z OneNote pomocí Aspose.Note pro Javu.
linktitle: Create Outline in OneNote and Add Tag – Aspose.Note
second_title: Aspose.Note Java API
title: Vytvořit osnovu v OneNote a přidat značku – Aspose.Note
url: /cs/java/onenote-tag-operations/add-tag/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Vytvořit osnovu v OneNote a přidat značku – Aspose.Note

## Úvod
Hledáte, jak **vytvořit osnovu v OneNote** a podpořit spolupráci pomocí značek v Javě? Aspose.Note pro Java umožňuje snadno přidávat značky, strukturovat vaše poznámky a dokonce **vytvořit PDF z OneNote** soubory. V tomto tutoriálu projdeme každý krok, vysvětlíme *proč* je jednotlivá část důležitá a ukážeme vám, jak na konci vytvořit profesionální PDF.

## Rychlé odpovědi
- **Co znamená “create outline in OneNote”?** Vytváří hierarchickou strukturu (osnovy), která organizuje obsah jako nadpisy a podsekce.
- **Která knihovna přidává značky do OneNote?** Aspose.Note pro Java poskytuje třídu `NoteTag` pro vizuální značky.
- **Mohu výsledek exportovat do PDF?** Ano – použijte `SaveFormat.Pdf` k **vytvoření PDF z OneNote**.
- **Potřebuji licence pro produkční nasazení?** Dočasná licence je k dispozici pro testování; plná licence je vyžadována pro komerční použití.
- **Jaké jsou hlavní předpoklady?** Nainstalovaný JDK, knihovna Aspose.Note pro Java a základní znalosti Javy.

## Co je to „vytvořit osnovu ve OneNotu“?
Vytvoření osnovy v OneNote znamená přidání objektů `Outline` a `OutlineElement`, které definují stromovou strukturu vašich poznámek. Tato hierarchie vám umožňuje sbalit, rozbalit a organizovat informace podobně jako nadpisy v dokumentu.

## Proč přidat štítek do OneNotu?
Značky jako hvězdičky, zaškrtávací políčka nebo vlastní ikony poskytují čtenářům vizuální vodítka, zlepšují vyhledatelnost a pomáhají týmům upřednostňovat položky. S Aspose.Note můžete programově připojit `NoteTag` k libovolnému úseku textu.

## Předpoklady
Před tím, než se pustíte dál, ověřte, že máte:
- Nainstalovaný Java Development Kit (JDK).
- Staženou knihovnu Aspose.Note pro Java. Můžete ji získat [zde](https://releases.aspose.com/note/java/).
- Základní znalosti programování v Javě.

## Importujte balíčky
dobře se, že importujete potřebné balíčky pro zahájení projektu:
```java
import java.awt.Color;
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.NoteTag;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.SaveFormat;
import com.aspose.note.TagIcon;
import com.aspose.note.ParagraphStyle;
```
Rozložme výše uvedený kód na krok‑za‑krokem průvodce.

## Krok 1: Nastavení dokumentu a stránky
Začněte vytvořením nového objektu `Document` a inicializací objektu `Page`:
```java
String dataDir = "Your Document Directory";
Document doc = new Document();
Page page = new Page();
```
Zde nastavujeme cestu k adresáři s dokumenty, vytváříme nový `Document` a inicializujeme `Page`.

## Krok 2: Vytvoření osnovy
Dále vytvořte objekt `Outline`, který strukturuje váš obsah:
```java
Outline outline = new Outline();
```
Osnovy poskytují hierarchickou strukturu vašemu dokumentu, což usnadňuje **vytvořit osnovu v OneNote** a udržet informace uspořádané.

## Krok 3: Inicializace OutlineElement a ParagraphStyle
Nyní inicializujte `OutlineElement` a nastavte `ParagraphStyle` pro formátování textu:
```java
OutlineElement outlineElem = new OutlineElement();
ParagraphStyle textStyle = new ParagraphStyle()
                                .setFontColor(Color.black)
                                .setFontName("Arial")
                                .setFontSize(10);
```
`OutlineElement` představuje prvek v rámci osnovy a `ParagraphStyle` definuje vlastnosti formátování textu.

## Krok 4: Přidání RichTextu s NoteTag
Vytvořte objekt `RichText`, připojte svůj OneNote text a přidejte `NoteTag`:
```java
RichText text = new RichText().append("OneNote text.");
text.setParagraphStyle(textStyle);
NoteTag noteTag = NoteTag.createYellowStar();
text.getTags().add(noteTag);
```
`RichText` vám umožňuje vkládat formátovaný text a `NoteTag` **přidává značku do OneNote** jako vizuální vodítko.

## Krok 5: Vytvoření struktury osnovy
Přidejte uzel textu, uzel elementu osnovy a uzel samotné osnovy pro vytvoření struktury dokumentu:
```java
outlineElem.appendChildLast(text);
outline.appendChildLast(outlineElem);
page.appendChildLast(outline);
doc.appendChildLast(page);
```
Tento krok zajišťuje, že je váš obsah v dokumentu uspořádán, čímž dokončuje proces **vytvořit osnovu v OneNote**.

## Krok 6: Uložení dokumentu
Uložte dokument ve formátu PDF, který **vytváří PDF z OneNote**:
```java
doc.save(dataDir + "AddTag_out.pdf", SaveFormat.Pdf);
System.out.printf("File Saved: %s\n", dataDir + "AddTag_out.pdf");
```
Nyní je váš OneNote dokument s přidanými značkami uložen jako PDF.

Postupováním těmito kroky můžete snadno vylepšit své OneNote dokumenty pomocí Aspose.Note pro Java.

## Závěr
V tomto tutoriálu jsme prozkoumali, jak **vytvořit osnovu v OneNote**, přidat značku do OneNote a následně **vytvořit PDF z OneNote** pomocí Aspose.Note pro Java. Využití Javy vám dává plnou kontrolu nad strukturou poznámek, vizuálním označováním a možnostmi exportu, což vaše poznámky uvádějí organizovanějšími a snadněji sdílenými.

## Nejčastější dotazy
### 1. Mohu použít Aspose.Note pro Javu s jinými programovacími jazyky?
Aspose.Note primárně podporuje Javu, ale jsou také dostupné verze pro .NET.

### 2. Je Aspose.Note pro Java vhodný pro začátečníky?
Ano, Ase.Note poskytuje komplexní dokumentaci a podporu, což činí přístupným jak začátečníky, tak pro Java poskytuje zkušené pro začátečníky.

### 3. Jak mohu získat dočasnou licenci pro Aspose.Note pro Java?
Dočasnou licenci můžete získat [zde](https://purchase.aspose.com/temporary-license/).

### 4. Kde najdu další podporu?
Pro jakékoliv dotazy nebo pomoc navštivte [forum Aspose.Note](https://forum.aspose.com/c/note/28).

### 5. Je k dispozici bezplatná zkušební verze?
Ano, bezplatnou zkušební verzi můžete vyzkoušet [zde](https://releases.aspose.com/).

**Další otázky a odpovědi**

**O: Mohu upravit ikonu značky?**
A: Ano – Aspose.Note poskytuje mnoho předdefinovaných ikon prostřednictvím `TagIcon` a také umožňuje použít vlastní obrázky.

**Q: Jak změním nastavení výstupu PDF?**
A: Použijte `PdfSaveOptions` k nastavení kvality obrázků, komprese a zabezpečení před voláním `doc.save`.

**Q: Je možné přidat více značek ke stejnému textu?**
A: Rozhodně. Zavolejte `text.getTags().d()` s různými instancemi `NoteTag`.

---

**Poslední aktualizace:** 28. 1. 2026
**Testováno s:** Aspose.Note pro Java 24.12
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}