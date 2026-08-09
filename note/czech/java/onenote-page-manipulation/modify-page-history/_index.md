---
date: 2026-05-31
description: Naučte se, jak upravit historii stránek OneNote, změnit název stránky
  OneNote a smazat historii stránek OneNote pomocí Aspose.Note pro Java.
keywords:
- modify onenote page history
- change onenote page title
- Aspose.Note Java
linktitle: Upravit historii stránek v OneNote – Aspise.Note
schemas:
- author: Aspose
  dateModified: '2026-05-31'
  description: Learn how to modify onenote page history, change onenote page title,
    and delete page history onenote using Aspose.Note for Java.
  headline: How to modify onenote page history with Aspose.Note
  type: TechArticle
- description: Learn how to modify onenote page history, change onenote page title,
    and delete page history onenote using Aspose.Note for Java.
  name: How to modify onenote page history with Aspose.Note
  steps:
  - name: Load the OneNote Document
    text: '`Document` loads a OneNote file into memory and provides access to its
      pages and history.'
  - name: Retrieve the First Page and Its History
    text: '`PageHistory` is the Aspose.Note class that stores a notebook’s revision
      list. It offers methods to query, add, or remove historic pages.'
  - name: Delete a Range of History Items
    text: '`removeRange(int start, int count)` removes a consecutive block of history
      entries starting at the specified index.'
  - name: Replace a History Item
    text: '`set_Item(int index, Page page)` replaces the history entry at the given
      position with a new `Page` object.'
  - name: Change the Title of a History Page
    text: '`setTitle(String title)` updates the title of a historic `Page` instance.'
  - name: Add a New History Entry
    text: '`addItem(Page page)` appends a new page to the end of the history collection.'
  - name: Insert a Page at a Specific Position
    text: '`insertItem(int index, Page page)` inserts a page at the specified index,
      shifting subsequent items forward.'
  - name: Save the Modified Notebook
    text: '`save(String path)` writes the updated notebook to the given file location.'
  type: HowTo
- questions:
  - answer: Yes, Aspose.Note for Java integrates seamlessly with Spring, Hibernate,
      Android, and other Java ecosystems.
    question: Can I use Aspose.Note for Java with other Java frameworks?
  - answer: Absolutely—Aspose.Note supports both legacy OneNote 2007 files and the
      modern OneNote 2016/Online formats.
    question: Is Aspose.Note for Java compatible with different versions of OneNote
      files?
  - answer: No, the library is self‑contained; you only need the core JAR and a Java
      runtime.
    question: Does Aspose.Note for Java require any additional dependencies?
  - answer: Yes, you can loop through a directory of `.one` files and apply the same
      history‑editing logic to each notebook.
    question: Can I perform bulk modifications on multiple OneNote files simultaneously?
  - answer: Yes, you can visit the [Aspose.Note forum](https://forum.aspose.com/c/note/28)
      for assistance and to share examples.
    question: Is there a community forum for Aspose.Note for Java where I can ask
      for help?
  type: FAQPage
second_title: Aspose.Note Java API
title: Jak upravit historii stránek OneNote pomocí Aspose.Note
url: /cs/java/onenote-page-manipulation/modify-page-history/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak upravit historii stránky OneNote pomocí Aspose.Note

V tomto tutoriálu se naučíte **jak upravit historii stránky OneNote** krok za krokem pomocí API Aspose.Note pro Java. Ať už potřebujete smazat staré revize, přejmenovat historickou stránku nebo vložit nový záznam, průvodce vás provede připraveným pracovním postupem, který funguje s jakýmkoli sešitem OneNote.

## Rychlé odpovědi
- **Co znamená „historie stránky“ v OneNote?**  
  Jedná se o sbírku předchozích verzí stránky uložených v souboru OneNote.
- **Mohu smazat konkrétní položku historie?**  
  Ano, použijte metody `removeRange` nebo `removeItem` na objektu `PageHistory`.
- **Je změna názvu stránky součástí manipulace s historií?**  
  Rozhodně—každá položka historie má svůj vlastní název, který můžete upravit.
- **Potřebuji licenci pro spuštění tohoto kódu?**  
  Dočasná zkušební licence funguje pro testování; pro produkci je vyžadována plná licence.
- **Která verze Javy je podporována?**  
  Aspose.Note pro Java podporuje JDK 8 a novější.

## Co je úprava historie stránky OneNote?
*Úprava historie stránky OneNote* označuje programové editování, přidávání nebo odstraňování položek v interním seznamu revizí sešitu OneNote. To vám umožní zachovat pouze relevantní verze, přejmenovat historické názvy a optimalizovat velikost sešitu při snížení celkového objemu souboru.

## Proč upravovat historii stránky OneNote?
Úprava historie stránky může výrazně zlepšit spravovatelnost a výkon sešitu. Odstraňováním nepoužívaných revizí zmenšíte velikost souboru, urychlíte načítání a učiníte navigaci pro koncové uživatele konzistentnější. Tyto výhody jsou obzvláště patrné u velkých sešitů se stovkami stránek.

Aspose.Note podporuje **více než 50 vstupních a výstupních formátů** a dokáže zpracovat sešity obsahující **až 10 000 stránek** bez načítání celého souboru do paměti, což zajišťuje vysoce výkonné operace.

## Požadavky

Než začnete, ujistěte se, že máte:

1. **Java Development Kit (JDK)** – JDK 8 nebo novější nainstalovaný na vašem počítači.  
2. **Aspose.Note for Java library** – stáhněte ji ze [stránky ke stažení](https://releases.aspose.com/note/java/).  
3. **Ukázkový dokument OneNote** – např. `Sample1.one`, který můžete bezpečně upravit.

## Import balíčků

Následující třídy jsou vyžadovány: `Document` představuje celý sešit, `Page` představuje jednotlivou stránku a `PageHistory` spravuje kolekci historických stránek.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.PageHistory;
```

## Jak upravit historii stránky OneNote?

Načtěte sešit, získejte jeho kolekci `PageHistory` a poté použijte poskytnuté metody k mazání, nahrazování nebo vkládání položek. Všechny operace probíhají v paměti a na konci stačí jednou zavolat `save`, aby se změny uložily.

### Krok 1: Načtení dokumentu OneNote

`Document` načte soubor OneNote do paměti a poskytuje přístup k jeho stránkám a historii.

```java
String dataDir = "Your Document Directory";
Document document = new Document(dataDir + "Sample1.one");
```

### Krok 2: Získání první stránky a její historie

`PageHistory` je třída Aspose.Note, která ukládá seznam revizí sešitu. Nabízí metody pro dotazování, přidávání nebo odstraňování historických stránek.

```java
Page page = document.getFirstChild();
PageHistory pageHistory = document.getPageHistory(page);
```

### Krok 3: Smazání rozsahu položek historie

`removeRange(int start, int count)` odstraňuje souvislý blok položek historie začínající na zadaném indexu.

```java
pageHistory.removeRange(0, 1);
```

### Krok 4: Nahrazení položky historie

`set_Item(int index, Page page)` nahrazuje položku historie na dané pozici novým objektem `Page`.

```java
pageHistory.set_Item(0, new Page());
```

### Krok 5: Změna názvu historické stránky

`setTitle(String title)` aktualizuje název historické instance `Page`.

```java
pageHistory.get_Item(1).getTitle().getTitleText().clear().append("New Title");
```

### Krok 6: Přidání nové položky historie

`addItem(Page page)` přidá novou stránku na konec kolekce historie.

```java
pageHistory.addItem(new Page());
```

### Krok 7: Vložení stránky na konkrétní pozici

`insertItem(int index, Page page)` vloží stránku na zadaný index a posune následující položky dopředu.

```java
pageHistory.insertItem(1, new Page());
```

### Krok 8: Uložení upraveného sešitu

`save(String path)` zapíše aktualizovaný sešit na zadané umístění souboru.

```java
document.save(dataDir + "ModifyPageHistory_out.one");
```

## Časté úskalí a tipy
- **Index mimo rozsah:** Vždy ověřte velikost kolekce před voláním `removeRange` nebo `insertItem`.  
- **Null názvy:** Některé historické stránky mohou postrádat název; chraňte se před `null` při volání `getTitle()`.  
- **Umístění uložení:** Ujistěte se, že výstupní cesta (`ModifyPageHistory_out.one`) je zapisovatelná; jinak bude vyvolána `IOException`.  
- **Tip pro výkon:** Při práci s velmi velkými sešity zavolejte `document.setLoadOptions(new LoadOptions(LoadFormat.OneNote))`, abyste povolili líné načítání a udrželi nízkou spotřebu paměti.

## Často kladené otázky

**Q: Mohu použít Aspose.Note pro Java s jinými Java frameworky?**  
A: Ano, Aspose.Note pro Java se bez problémů integruje se Spring, Hibernate, Android a dalšími Java ekosystémy.

**Q: Je Aspose.Note pro Java kompatibilní s různými verzemi souborů OneNote?**  
A: Rozhodně—Aspose.Note podporuje jak starší soubory OneNote 2007, tak moderní formáty OneNote 2016/Online.

**Q: Vyžaduje Aspose.Note pro Java nějaké další závislosti?**  
A: Ne, knihovna je samostatná; potřebujete jen hlavní JAR a Java runtime.

**Q: Mohu provádět hromadné úpravy na více souborech OneNote najednou?**  
A: Ano, můžete projít adresář s `.one` soubory a aplikovat stejnou logiku úpravy historie na každý sešit.

**Q: Existuje komunitní fórum pro Aspose.Note pro Java, kde se mohu zeptat na pomoc?**  
A: Ano, můžete navštívit [forum Aspose.Note](https://forum.aspose.com/c/note/28) pro pomoc a sdílení příkladů.

---

**Poslední aktualizace:** 2026-05-31  
**Testováno s:** Aspose.Note for Java 24.11 (latest at time of writing)  
**Autor:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Související tutoriály

- [aspose.note tutoriál revizí stránek – Získání revizí stránek v OneNote](/note/java/onenote-page-manipulation/get-page-revisions/)
- [Jak uložit verzi stránky OneNote – Odeslat aktuální verzi stránky v OneNote - Aspose.Note](/note/java/onenote-page-manipulation/push-current-page-version/)
- [sledování změn onenote – Správa revizí stránek pomocí Aspose.Note](/note/java/onenote-page-manipulation/working-with-page-revisions/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}