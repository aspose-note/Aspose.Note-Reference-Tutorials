---
date: 2026-02-18
description: Naučte se, jak vytvořit dokument OneNote, formátovat bohatý text a uložit
  jej jako PDF v Javě pomocí Aspose.Note. Průvodce krok za krokem pro bezproblémovou
  automatizaci.
linktitle: Create OneNote document and save as PDF in Java
second_title: Aspose.Note Java API
title: Vytvořte dokument OneNote a uložte jej jako PDF v Javě
url: /cs/java/onenote-document-manipulation/create-onenote-document-formatted-rich-text/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Vytvořte dokument OneNote a uložte jej jako PDF v Javě

## Úvod

Pokud potřebujete **vytvořit dokument OneNote** a **uložit OneNote jako PDF** při zachování formátování rich‑textu, jste na správném místě. V tomto tutoriálu vás provedeme vytvořením dokumentu OneNote, aplikací vlastních stylů a přímým exportem do PDF pomocí Aspose.Note pro Java. Na konci budete mít znovupoužitelný úryvek, který můžete vložit do libovolného Java projektu a automatizovat tak profesionální konverze OneNote‑na‑PDF.

## Rychlé odpovědi
- **Co se v tomto tutoriálu učí?** Jak vytvořit dokument OneNote se stylovaným textem a uložit jej jako PDF.  
- **Která knihovna je vyžadována?** Aspose.Note pro Java (ke stažení z oficiální stránky).  
- **Potřebuji licenci?** Dočasná licence funguje pro testování; plná licence je vyžadována pro produkci.  
- **Jaké IDE mohu použít?** Jakékoli Java IDE — IntelliJ IDEA, Eclipse nebo NetBeans.  
- **Mohu změnit výstupní formát?** Ano, Aspose.Note podporuje PDF, HTML, PNG a další.

## Co je „uložit onenote pdf“?
Uložení OneNote jako PDF znamená převod struktury stránky OneNote — včetně textu, obrázků a formátování — do statického souboru PDF, který lze zobrazit na jakékoli platformě bez potřeby OneNote.

## Proč formátovat rich text v Javě?
Aplikace **formátování rich textu** přímo v Javě vám umožní generovat dokumenty, které vypadají profesionálně a odpovídají vašim firemním směrnicím, bez nutnosti ruční úpravy.

## Předpoklady

1. **Java Development Kit (JDK)** – libovolná aktuální verze (8 nebo vyšší).  
2. **Aspose.Note pro Java JAR** – stáhněte jej z [odkazu ke stažení](https://releases.aspose.com/note/java/).  
3. **IDE** – IntelliJ IDEA, Eclipse nebo libovolný editor, který preferujete.  

## Import balíčků

Než začneme, importujte potřebné třídy do vašeho Java souboru:

```java
import java.awt.Color;
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.SaveFormat;
import com.aspose.note.TextStyle;
import com.aspose.note.ParagraphStyle;
import com.aspose.note.Title;
```

## Jak vytvořit dokument OneNote – krok za krokem

### Krok 1: Nastavení dokumentu a stránky

Inicializujte objekty `Document` a `Page`, které budou obsahovat veškerý obsah:

```java
String dataDir = "Your Document Directory";
Document doc = new Document();
Page page = new Page();
```

### Krok 2: Vytvoření titulku s formátováním

Přidejte prvek titulku a použijte **set paragraph style** pro kontrolu jeho vzhledu:

```java
Title title = new Title();
ParagraphStyle defaultTextStyle = new ParagraphStyle()
                                        .setFontColor(Color.black)
                                        .setFontName("Arial")
                                        .setFontSize(10);

RichText titleText = new RichText().append("Title!");
titleText.setParagraphStyle(defaultTextStyle);
title.setTitleText(titleText);
```

### Krok 3: Vytvoření rich textu s formátováním

Zde vytváříme obsah rich‑textu pomocí několika objektů `TextStyle`, abychom demonstrovali **formátování rich textu**:

```java
Outline outline = new Outline();
OutlineElement outlineElem = new OutlineElement();

TextStyle textStyleForHelloWord = new TextStyle()
                                        .setFontColor(Color.red)
                                        .setFontName("Arial")
                                        .setFontSize(10);

TextStyle textStyleForOneNoteWord = new TextStyle()
                                        .setFontColor(Color.green)
                                        .setFontName("Calibri")
                                        .setFontSize(10)
                                        .setItalic(true);

TextStyle textStyleForTextWord = new TextStyle()
                                        .setFontColor(Color.blue)
                                        .setFontName("Arial")
                                        .setFontSize(15)
                                        .setBold(true)
                                        .setItalic(true);

RichText text = new RichText()
        .append("Hello", textStyleForHelloWord)
        .append(" OneNote", textStyleForOneNoteWord)
        .append(" text", textStyleForTextWord)
        .append("!", TextStyle.getDefault());
text.setParagraphStyle(defaultTextStyle);
```

### Krok 4: Přidání prvků na stránku a do dokumentu

Zkombinujte titulek a rich text do hierarchie stránky:

```java
outlineElem.appendChildLast(text);
outline.appendChildLast(outlineElem);
page.setTitle(title);
page.appendChildLast(outline);
doc.appendChildLast(page);
```

### Krok 5: Uložení dokumentu – export onenote pdf

Nakonec exportujte dokument OneNote jako soubor PDF:

```java
doc.save(dataDir + "CreateOneNoteDocument_out.pdf", SaveFormat.Pdf);
```

## Časté problémy a řešení

| Problém | Řešení |
|-------|----------|
| **Soubor nenalezen** | Ověřte, že `dataDir` ukazuje na existující složku a že máte oprávnění k zápisu. |
| **Chybějící fonty** | Ujistěte se, že fonty, na které odkazujete (např. *Calibri*), jsou nainstalovány na hostitelském počítači. |
| **Licence nebyla použita** | Načtěte svou Aspose licenci před vytvořením `Document`, aby se zabránilo vodoznakům z evaluační verze. |

## Často kladené otázky

**Q: Mohu dále přizpůsobit styly fontů?**  
A: Ano, můžete upravit další vlastnosti, jako podtržení, přeškrtnutí a zarovnání textu pomocí tříd `TextStyle` a `ParagraphStyle`.

**Q: Je Aspose.Note pro Java kompatibilní se všemi Java IDE?**  
A: Naprosto. Dokud IDE podporuje standardní vývoj v Javě, můžete přidat Aspose.Note JAR do classpath projektu.

**Q: Mohu tuto funkčnost integrovat do webových aplikací?**  
A: Ano, stejný kód funguje v servlet‑based nebo Spring Boot aplikacích, což umožňuje dynamické generování OneNote‑na‑PDF na straně serveru.

**Q: Existují licenční požadavky pro používání Aspose.Note pro Java?**  
A: Pro produkční použití je vyžadována komerční licence. Dočasná licence je k dispozici pro hodnocení a testování.

**Q: Podporuje Aspose.Note pro Java i jiné formáty dokumentů kromě OneNote?**  
A: Podporuje PDF, HTML, PNG, JPEG a několik dalších exportních formátů, což vám poskytuje flexibilitu převádět stránky OneNote do požadovaného formátu.

## Závěr

V tomto průvodci jsme ukázali, jak **vytvořit dokument OneNote**, aplikovat **formátování rich textu** a **uložit OneNote jako PDF** pomocí Aspose.Note pro Java. Dodržením krok‑za‑krokem instrukcí můžete automatizovat tvorbu profesionálních OneNote dokumentů a převádět je do PDF v jakémkoli řešení založeném na Javě.

---

**Poslední aktualizace:** 2026-02-18  
**Testováno s:** Aspose.Note pro Java 24.11 (nejnovější v době psaní)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}