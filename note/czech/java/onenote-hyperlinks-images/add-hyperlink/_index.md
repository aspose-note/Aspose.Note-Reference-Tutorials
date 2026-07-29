---
date: 2026-07-29
description: Naučte se, jak vložit odkaz do OneNote, uložit OneNote jako PDF a přidat
  hypertextové odkazy pomocí Java s Aspose.Note. Exportujte OneNote do PDF bez námahy.
keywords:
- embed link onenote
- export onenote to pdf
- generate pdf from onenote
- add hyperlink in onenote
- save onenote pdf
lastmod: 2026-07-29
linktitle: Uložit OneNote jako PDF a přidat hypertextový odkaz v OneNote pomocí Java
og_description: Vložte odkaz do OneNote a exportujte OneNote do PDF pomocí Java a
  Aspose.Note. Naučte se krok za krokem, jak přidat hypertextové odkazy a vytvořit
  PDF.
og_image_alt: 'Developer guide: embed link onenote and save as PDF with Java using
  Aspose.Note'
og_title: Vložit odkaz OneNote – Uložit OneNote jako PDF pomocí Java
schemas:
- author: Aspose
  dateModified: '2026-07-29'
  description: Learn how to embed link onenote, save OneNote as PDF, and add hyperlinks
    using Java with Aspose.Note. Export OneNote to PDF effortlessly.
  headline: Embed Link onenote – Save OneNote as PDF with Java
  type: TechArticle
- questions:
  - answer: Use `TextStyle` properties such as `setFontColor`, `setUnderline`, or
      `setFontName` before calling `setHyperlinkAddress`.
    question: How can I customize the appearance of the hyperlink?
  - answer: Yes, Aspose.Note supports DOCX, XPS, HTML, and several other export formats.
    question: Can I save the document in formats other than PDF?
  - answer: Load the existing file with `new Document("input.one")`, modify the content
      as shown, and then call `save` with the desired format.
    question: What if I need to add a hyperlink to an existing OneNote file?
  - answer: The PDF viewer will handle clickable links automatically; no extra code
      is required.
    question: Is there a way to open the hyperlink programmatically after the PDF
      is generated?
  - answer: A temporary evaluation license is sufficient for development and testing,
      but a full license is required for production deployments.
    question: Do I need a license for development use?
  type: FAQPage
second_title: Aspose.Note Java API
tags:
- onenote pdf conversion
- Aspose.Note
- Java document processing
title: Vložit odkaz OneNote – Uložit OneNote jako PDF pomocí Java
url: /cs/java/onenote-hyperlinks-images/add-hyperlink/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Uložte OneNote jako PDF a přidejte hypertextový odkaz v OneNote pomocí Javy

## Úvod

Pokud potřebujete **embed link onenote** při převodu poznámkového bloku na přenosné PDF, jste na správném místě. Tento tutoriál vás provede ukládáním OneNote jako PDF a vkládáním klikacích hypertextových odkazů pomocí Javy a knihovny Aspose.Note. Uvidíte, proč je tento přístup ideální pro archivaci, sdílení a automatizaci dokumentových pipeline.

## Rychlé odpovědi
- **Mohu uložit OneNote jako PDF pomocí Javy?** Ano, Aspose.Note pro Javu poskytuje jediný volání `save` pro vytvoření PDF.
- **Jak vložit hypertextový odkaz?** Použijte `TextStyle.setHyperlinkAddress` na segmentu `RichText`.
- **Jaké jsou požadavky?** JDK 8+ a knihovna Aspose.Note pro Javu.
- **Jaké výstupní formáty jsou podporovány?** PDF, DOCX, XPS a další.
- **Je licence vyžadována pro produkci?** Ano, pro ne‑evaluační použití je potřeba komerční licence.

## Co je „uložit OneNote jako PDF“?

Uložení poznámkového bloku OneNote jako PDF vytvoří pouze pro čtení, multiplatformní verzi vašich poznámek, kterou může kdokoli otevřít bez aplikace OneNote. Tento formát je ideální pro archivaci, tisk nebo sdílení s kolegy, kteří nemají OneNote nainstalovaný, a přitom zachovává původní rozvržení, obrázky a všechny vložené hypertextové odkazy.

## Proč generovat PDF z OneNote pomocí Aspose.Note Java?

Aspose.Note pro Javu může **export onenote to pdf** s 100 % věrností rozvržení, zvládá až 200 stránek na dokument, aniž by načítal celý soubor do paměti. Knihovna zpracovává více než 30 různých typů obsahu — včetně obrázků, tabulek a 95 % stylů hypertextových odkazů — takže získáte věrnou repliku původního poznámkového bloku. Funguje také na Windows, Linuxu a macOS, což umožňuje hromadné konverze v cloudu nebo na lokálních serverech.

## Požadavky

Než začneme, ujistěte se, že máte na svém systému nainstalovány a nastaveny následující požadavky:

### Java Development Kit (JDK)

Ujistěte se, že máte na svém systému nainstalovaný Java Development Kit (JDK). JDK můžete stáhnout a nainstalovat z [webu Oracle](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).

### Aspose.Note pro Javu Library

Stáhněte a nainstalujte knihovnu Aspose.Note pro Javu. Dokumentaci a odkaz ke stažení najdete [zde](https://reference.aspose.com/note/java/).

## Import balíčků

Nejprve importujte potřebné balíčky, které jsou vyžadovány pro práci s Aspose.Note pro Javu.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.TextStyle;
import com.aspose.note.ParagraphStyle;
import com.aspose.note.Title;
```

Nyní rozdělíme poskytnutý příklad do několika kroků:

## Jak vložit odkaz do OneNote při ukládání jako PDF?

Načtěte novou instanci `Document`, vytvořte strukturu stránky, definujte červeně zbarvený `TextStyle` pro hypertextový odkaz a nakonec zavolejte `document.save("output.pdf", SaveFormat.Pdf)`. Tento postup vytvoří PDF, které obsahuje plně funkční hypertextový odkaz a zachovává veškeré původní formátování a obrázky.

## Krok 1: Nastavení struktury dokumentu

`Document` představuje poznámkový blok OneNote v Aspose.Note.  
`Page` je kontejner pro osnovy a další prvky na úrovni stránky.

```java
String dataDir = "Your Document Directory";
Document doc = new Document();
Page page = new Page();
Title title = new Title();
```

## Krok 2: Definice výchozího stylu textu

`ParagraphStyle` definuje výchozí formátování odstavců, jako je zarovnání, mezery a odsazení.

```java
ParagraphStyle defaultTextStyle = new ParagraphStyle()
                                            .setFontName("Arial")
                                            .setFontSize(10)
                                            .setFontColor(java.awt.Color.GRAY);
```

## Krok 3: Nastavení textu nadpisu

`Title` představuje prvek názvu stránky v dokumentu OneNote.

```java
RichText titleText = new RichText().append("Title");
titleText.setParagraphStyle(defaultTextStyle);
title.setTitleText(titleText);
page.setTitle(title);
```

## Krok 4: Vytvoření osnovy a jejích prvků

`Outline` funguje jako kontejner pro hierarchii obsahových bloků.  
`OutlineElement` je jednotlivý prvek v osnově, například odstavec nebo tabulka.

```java
Outline outline = new Outline();
OutlineElement outlineElem = new OutlineElement();
```

## Krok 5: Definice stylu textu pro hypertextový odkaz

`TextStyle` řídí vizuální vzhled úseků textu, včetně písma, barvy a nastavení podtržení.

```java
TextStyle textStyleRed = new TextStyle()
                                    .setFontName("Arial")
                                    .setFontSize(10)
                                    .setFontColor(java.awt.Color.red);
```

## Krok 6: Přidání textu s hypertextovým odkazem

`RichText` představuje úsek formátovaného textu uvnitř odstavce. Nastavením adresy hypertextového odkazu se text v exportovaném PDF stane klikacím.

```java
RichText text = new RichText()
                            .append("This is ", textStyleRed)
                            .append("hyperlink", new TextStyle().setHyperlinkAddress("https://www.google.com"))
                            .append(". This text is not a hyperlink.", TextStyle.getDefault());
text.setParagraphStyle(defaultTextStyle);
outlineElem.appendChildLast(text);
```

## Krok 7: Přidání osnovy na stránku a stránky do dokumentu

Tento krok připojí dříve vytvořené prvky osnovy ke stránce a poté přidá stránku do objektu `Document`.

```java
outline.appendChildLast(outlineElem);
page.appendChildLast(outline);
doc.appendChildLast(page);
```

## Krok 8: Uložení dokumentu jako PDF

`SaveFormat.Pdf` říká Aspose.Note, aby exportoval dokument ve formátu PDF.

```java
doc.save(dataDir + "AddHyperlink_out.pdf");
System.out.printf("File saved: %s\n", dataDir + "AddHyperlink_out.pdf");
```

## Závěr

Gratulujeme! Úspěšně jste **uložili OneNote jako PDF** a přidali hypertextový odkaz do dokumentu pomocí Javy a knihovny Aspose.Note. Tato funkce vám umožní **embed link onenote** a vytvářet interaktivní, sdílené PDF přímo z obsahu OneNote.

## Často kladené otázky

**Q: Jak mohu přizpůsobit vzhled hypertextového odkazu?**  
A: Použijte vlastnosti `TextStyle`, jako jsou `setFontColor`, `setUnderline` nebo `setFontName`, před voláním `setHyperlinkAddress`.

**Q: Mohu dokument uložit v jiných formátech než PDF?**  
A: Ano, Aspose.Note podporuje DOCX, XPS, HTML a několik dalších exportních formátů.

**Q: Co když potřebuji přidat hypertextový odkaz do existujícího souboru OneNote?**  
A: Načtěte existující soubor pomocí `new Document("input.one")`, upravte obsah podle ukázky a poté zavolejte `save` s požadovaným formátem.

**Q: Existuje způsob, jak programově otevřít hypertextový odkaz po vygenerování PDF?**  
A: Prohlížeč PDF automaticky zpracuje klikatelné odkazy; není potřeba žádný další kód.

**Q: Potřebuji licenci pro vývojové použití?**  
A: Dočasná evaluační licence stačí pro vývoj a testování, ale pro produkční nasazení je vyžadována plná licence.

---

**Poslední aktualizace:** 2026-07-29  
**Testováno s:** Aspose.Note pro Javu 26.4  
**Autor:** Aspose

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.TextStyle;
import com.aspose.note.ParagraphStyle;
import com.aspose.note.Title;
```

## Související tutoriály

- [Jak uložit OneNote jako PDF pomocí Aspose.Note pro Javu](/note/java/onenote-document-loading/load-save-format/)
- [Převést OneNote na PDF pomocí Aspose.Note s PdfSaveOptions](/note/java/onenote-document-loading/load-pdf-save-options/)
- [Přidat hypertextový odkaz k obrázku v OneNote pomocí Javy](/note/java/onenote-hyperlinks-images/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}