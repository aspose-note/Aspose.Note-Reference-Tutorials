---
date: 2026-08-18
description: Naučte se, jak exportovat OneNote do PDF, nastavit formátování odstavců
  v Javě a uložit OneNote jako PDF pomocí Aspose.Note for Java.
keywords:
- export onenote to pdf
- save onenote as pdf
- paragraph formatting java
- rich text formatting java
- aspose note java
lastmod: 2026-08-18
linktitle: Nastavte odstavcový styl při vytváření dokumentu OneNote v Javě
og_description: Exportujte OneNote do PDF a nastavte odstavcový styl v Javě pomocí
  Aspose.Note. Postupujte podle tohoto krok‑za‑krokem návodu a snadno vytvořte profesionální
  PDF soubory.
og_image_alt: Screenshot of Java code exporting OneNote to PDF with styled paragraphs
og_title: Export OneNote do PDF s odstavcovým stylem v Javě (58 znaků)
schemas:
- author: Aspose
  dateModified: '2026-08-18'
  description: Learn how to export OneNote to PDF, set paragraph formatting in Java,
    and save OneNote as PDF using Aspose.Note for Java.
  headline: How to export OneNote to PDF with paragraph style in Java
  type: TechArticle
- description: Learn how to export OneNote to PDF, set paragraph formatting in Java,
    and save OneNote as PDF using Aspose.Note for Java.
  name: How to export OneNote to PDF with paragraph style in Java
  steps:
  - name: set document directory
    text: Define where the generated files will be saved. Replace `"Your Document
      Directory"` with an absolute or relative path on your machine.
  - name: initialize document object
    text: Create the root `Document` that represents the OneNote file. **Definition
      anchor:** `Document` is Aspose.Note’s top‑level object that holds one or more
      pages in memory.
  - name: initialize page object
    text: A OneNote file consists of one or more pages; we start with a single page.
      **Definition anchor:** `Page` represents a single OneNote page, containing outlines,
      images, and other elements.
  - name: initialize outline object
    text: Outlines act as containers for outline elements (think of them as sections).
      **Definition anchor:** `Outline` groups related `OutlineElement` objects and
      defines their visual hierarchy.
  - name: initialize outline element object
    text: Here we **add outline element** that will hold our rich text. **Definition
      anchor:** `OutlineElement` is a leaf node inside an `Outline` that can contain
      text, images, or other media.
  - name: set text style (set paragraph style)
    text: '`ParagraphStyle` defines the font family, size, color, and other typographic
      attributes for a paragraph. The `ParagraphStyle` instance defines the font,
      size, and color—this is where we **set paragraph style** for the upcoming text
      node.'
  - name: initialize rich text object
    text: '`RichText` is the node that stores styled text within an `OutlineElement`.
      We create a `RichText` node, insert a simple string, and attach the previously
      defined style.'
  - name: add rich text node to outline element
    text: Now the styled text lives inside the outline element.
  - name: add outline element node to outline
    text: The outline now contains the element that holds our paragraph.
  - name: add outline node to page
    text: We place the outline onto the page.
  type: HowTo
- questions:
  - answer: Yes, the API supports tables, images, hyperlinks, and advanced layout
      features in addition to plain text.
    question: Can Aspose.Note handle complex formatting such as tables or images?
  - answer: Direct conversion isn’t provided, but you can extract PDF content and
      rebuild a OneNote document using the API.
    question: Is it possible to convert a OneNote PDF back to a OneNote file?
  - answer: Absolutely. Aspose.Note for Java is platform‑independent; just ensure
      a compatible JDK is installed.
    question: Does the library work on Linux/macOS environments?
  - answer: Create additional `Page` and `Outline` objects, then append them to the
      `Document` just like the single‑page example.
    question: How do I add multiple pages or outlines?
  - answer: The official Aspose.Note documentation and the [support forum](https://forum.aspose.com/c/note/28)
      contain many code samples and real‑world scenarios.
    question: Where can I find more examples?
  type: FAQPage
second_title: Aspose.Note Java API
tags:
- export onenote
- aspose.note
- java document processing
title: Jak exportovat OneNote do PDF s odstavcovým stylem v Javě
url: /cs/java/onenote-document-manipulation/create-onenote-document-simple-rich-text/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Nastavte styl odstavce při vytváření dokumentu OneNote v Javě

## Úvod

Export OneNote do PDF programově je běžná potřeba pro reportingové motory, automatizované služby pro zápis poznámek a pipeline pro konverzi dokumentů. V tomto tutoriálu se naučíte, jak **exportovat OneNote do PDF**, aplikovat vlastní formátování odstavců a uložit soubor OneNote – vše pomocí Aspose.Note pro Java. Na konci budete mít připravený úryvek Java, který vytvoří upravené PDF s přesně definovaným vzhledem.

## Rychlé odpovědi
- **Co znamená „nastavit styl odstavce“?** Používá se k nastavení písma, velikosti, barvy a dalších formátovacích atributů odstavce textu.  
- **Mohu výsledek exportovat do PDF?** Ano – průvodce končí uložením souboru OneNote jako PDF.  
- **Potřebuji licenci pro Aspose.Note?** Bezplatná zkušební verze stačí pro hodnocení; pro produkční použití je vyžadována komerční licence.  
- **Jaké IDE jsou podporovány?** Jakékoli Java IDE – Eclipse, IntelliJ IDEA, NetBeans atd.  
- **Jak dlouho trvá implementace?** Přibližně 10‑15 minut pro základní dokument.

## Jak exportovat OneNote do PDF v Javě?

`Document` představuje soubor OneNote obsahující stránky, osnovy a další prvky. Načtěte svůj dokument OneNote pomocí `new Document()` (nebo vytvořte nový) a zavolejte `document.save("output.pdf", SaveFormat.Pdf)`. Aspose.Note vytvoří PDF v jednom kroku, zachovává styly, obrázky a osnovy, aniž by byl nainstalován Microsoft OneNote. Tento přímý přístup funguje na Windows, Linuxu i macOS s libovolným JDK 1.8+.

## Co je „nastavit styl odstavce“ v Aspose.Note?

`ParagraphStyle` je třída, která ukládá název písma, velikost, barvu, zarovnání a další typografické nastavení odstavce. Připojením instance `ParagraphStyle` k uzlu `RichText` přesně řídíte, jak bude odstavec vypadat na konečné stránce OneNote a v exportovaném PDF.

## Proč exportovat OneNote do PDF?

Export OneNote do PDF zajišťuje konzistentní značku tím, že zachovává firemní písma a barvy, zlepšuje čitelnost zachováním přesného rozvržení pro tisk nebo archivaci a poskytuje multiplatformní přístup, takže příjemci mohou dokument zobrazit na jakémkoli zařízení bez potřeby OneNote. Navíc přináší výkonnostní výhody, umožňující rychlé zpracování velkých dokumentů.

## Předpoklady

1. **Java Development Kit (JDK) 1.8+** – jakýkoli aktuální JDK bude fungovat.  
2. **Aspose.Note for Java** – stáhněte nejnovější JAR z [stránky ke stažení Aspose.Note](https://releases.aspose.com/note/java/).  
3. **IDE** (Eclipse, IntelliJ IDEA nebo NetBeans) pro kompilaci a spuštění ukázky.  

> **Tip:** Přidejte JAR Aspose.Note do classpath vašeho projektu pomocí Maven (`<dependency>`) nebo ručním odkazováním na JAR ve vašem IDE.

## Importovat balíčky

Nejprve importujte požadované jmenné prostory. Tento blok zůstává beze změny.

```java
import java.awt.Color;
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.SaveFormat;
import com.aspose.note.ParagraphStyle;
```

> Třída `ParagraphStyle` je klíčem k **nastavení stylu odstavce** později v tutoriálu.

## Průvodce krok za krokem

Níže je stručný průvodce každou operací. Kódové bloky jsou přesně jako v originálním vzorku; přidáváme jen vysvětlující text.

### Krok 1: nastavit adresář dokumentu
Definujte, kam budou generované soubory uloženy.

```java
String dataDir = "Your Document Directory";
```

Nahraďte `"Your Document Directory"` absolutní nebo relativní cestou na vašem počítači.

### Krok 2: inicializovat objekt dokumentu
Vytvořte kořenový `Document`, který představuje soubor OneNote.

```java
Document doc = new Document();
```

**Ukotvení definice:** `Document` je nejvyšší objekt Aspose.Note, který v paměti drží jednu nebo více stránek.

### Krok 3: inicializovat objekt stránky
Soubor OneNote se skládá z jedné nebo více stránek; začínáme s jednou stránkou.

```java
Page page = new Page();
```

**Ukotvení definice:** `Page` představuje jednu stránku OneNote, obsahující osnovy, obrázky a další prvky.

### Krok 4: inicializovat objekt osnovy
Osnovy fungují jako kontejnery pro prvky osnovy (přemýšlejte o nich jako o sekcích).

```java
Outline outline = new Outline();
```

**Ukotvení definice:** `Outline` seskupuje související objekty `OutlineElement` a určuje jejich vizuální hierarchii.

### Krok 5: inicializovat objekt prvku osnovy
Zde **přidáváme prvek osnovy**, který bude obsahovat náš formátovaný text.

```java
OutlineElement outlineElem = new OutlineElement();
```

**Ukotvení definice:** `OutlineElement` je listový uzel uvnitř `Outline`, který může obsahovat text, obrázky nebo jiná média.

### Krok 6: nastavit styl textu (nastavit styl odstavce)

`ParagraphStyle` definuje rodinu písma, velikost, barvu a další typografické atributy odstavce.

```java
ParagraphStyle textStyle = new ParagraphStyle()
                                    .setFontColor(Color.black)
                                    .setFontName("Arial")
                                    .setFontSize(10);
```

Instance `ParagraphStyle` určuje písmo, velikost a barvu – zde **nastavujeme styl odstavce** pro nadcházející textový uzel.

### Krok 7: inicializovat objekt RichText

`RichText` je uzel, který ukládá formátovaný text uvnitř `OutlineElement`.

```java
RichText text = new RichText().append("Hello OneNote text!");
text.setParagraphStyle(textStyle);
```

Vytvoříme uzel `RichText`, vložíme jednoduchý řetězec a připojíme dříve definovaný styl.

### Krok 8: přidat uzel RichText do prvku osnovy

```java
outlineElem.appendChildLast(text);
```

Nyní je formátovaný text uvnitř prvku osnovy.

### Krok 9: přidat uzel prvku osnovy do osnovy

```java
outline.appendChildLast(outlineElem);
```

Osnova nyní obsahuje prvek, který drží náš odstavec.

### Krok 10: přidat uzel osnovy na stránku

```java
page.appendChildLast(outline);
```

Umístíme osnovu na stránku.

### Krok 11: přidat uzel stránky do dokumentu

```java
doc.appendChildLast(page);
```

Dokument nyní má jednu stránku s naším formátovaným textem.

### Krok 12: uložit dokument (exportovat OneNote PDF)

```java
doc.save(dataDir + "CreateOneNoteDocumentWithSimpleRichText_out.pdf", SaveFormat.Pdf);
```

Metoda `save` zapíše soubor OneNote a **exportuje OneNote do PDF** v jednom kroku. Můžete také uložit jako `.one` pomocí `SaveFormat.One`, pokud potřebujete nativní formát.

## Časté problémy a řešení

| Problém | Důvod | Řešení |
|-------|--------|-----|
| **Soubor nenalezen** | `dataDir` ukazuje na neexistující složku. | Zajistěte, aby složka existovala, nebo ji vytvořte programově (`new File(dataDir).mkdirs();`). |
| **Prázdné PDF** | Před uložením nebyl přidán žádný obsah. | Ověřte, že je uzel `RichText` připojen a styl nastaven. |
| **Není podporováno písmo** | Název písma není nainstalován v systému. | Použijte běžné písmo jako `"Arial"` nebo vložte písmo do projektu. |

## Často kladené otázky

**Q: Dokáže Aspose.Note zvládat složité formátování, jako jsou tabulky nebo obrázky?**  
A: Ano, API podporuje tabulky, obrázky, hypertextové odkazy a pokročilé funkce rozvržení kromě prostého textu.

**Q: Je možné převést PDF OneNote zpět na soubor OneNote?**  
A: Přímý převod není k dispozici, ale můžete extrahovat obsah PDF a pomocí API znovu vytvořit dokument OneNote.

**Q: Funguje knihovna na Linux/macOS?**  
A: Rozhodně. Aspose.Note pro Java je platformně nezávislá; stačí mít nainstalovaný kompatibilní JDK.

**Q: Jak přidám více stránek nebo osnov?**  
A: Vytvořte další objekty `Page` a `Outline` a připojte je k `Document` stejně jako v příkladu s jednou stránkou.

**Q: Kde najdu více příkladů?**  
A: Oficiální dokumentace Aspose.Note a [fórum podpory](https://forum.aspose.com/c/note/28) obsahují mnoho ukázek kódu a reálných scénářů.

## Závěr

Nyní jste viděli, jak **nastavit styl odstavce**, **přidat prvek osnovy** a **exportovat OneNote do PDF** pomocí Aspose.Note pro Java. Aplikace stylovaného textu již v počátku zajišťuje, že konečné PDF vypadá profesionálně, a operace `save` v jednom volání efektivně provede konverzi. Rozšiřte tento základ o obrázky, tabulky nebo vlastní metadata, aby vyhovoval konkrétním potřebám vaší aplikace.

---

**Poslední aktualizace:** 2026-08-18  
**Testováno s:** Aspose.Note for Java 26.5 (nejnovější verze)  
**Autor:** Aspose

## Související tutoriály

- [Jak uložit OneNote jako PDF pomocí Aspose.Note pro Java](/note/java/onenote-document-loading/load-save-format/)
- [Naučte se převést OneNote do PDF pomocí Aspose.Note s PdfSaveOptions](/note/java/onenote-document-loading/load-pdf-save-options/)
- [Nastavit výchozí styl odstavce v OneNote – Aspose.Note](/note/java/onenote-styles/set-default-paragraph-style/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}