---
date: 2025-12-09
description: Naučte se, jak uložit OneNote jako PDF s formátovaným bohatým textem
  v Javě pomocí Aspose.Note pro Javu. Postupujte podle našeho krok‑za‑krokem průvodce
  pro bezproblémovou automatizaci dokumentů.
linktitle: Save OneNote as PDF with Formatted Rich Text in Java
second_title: Aspose.Note Java API
title: Uložit OneNote jako PDF s formátovaným bohatým textem v Javě
url: /cs/java/onenote-document-manipulation/create-onenote-document-formatted-rich-text/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Uložte OneNote jako PDF s formátovaným bohatým textem v Javě

## Úvod

Pokud potřebujete **uložit OneNote jako PDF** a zachovat formátování bohatého textu, jste na správném místě. V tomto tutoriálu vás provedeme vytvořením dokumentu OneNote, aplikací vlastních stylů a exportem přímo do PDF pomocí Aspose.Note pro Java. Na konci budete mít znovupoužitelný úryvek kódu, který můžete vložit do libovolného Java projektu a automatizovat tak profesionální převody OneNote‑na‑PDF.

## Rychlé odpovědi
- **Co se v tomto tutoriálu učí?** Jak vytvořit dokument OneNote se stylovaným textem a uložit jej jako PDF.  
- **Která knihovna je vyžadována?** Aspose.Note pro Java (ke stažení z oficiálního webu).  
- **Potřebuji licenci?** Dočasná licence funguje pro testování; plná licence je vyžadována pro produkci.  
- **Jaké IDE mohu použít?** Jakékoli Java IDE – IntelliJ IDEA, Eclipse nebo NetBeans.  
- **Mohu změnit výstupní formát?** Ano, Aspose.Note podporuje PDF, HTML, PNG a další.

## Co znamená „uložit OneNote jako PDF“?
Uložení OneNote jako PDF znamená převod struktury stránky OneNote – včetně textu, obrázků a formátování – do statického PDF souboru, který lze zobrazit na jakékoli platformě bez potřeby OneNote.

## Proč formátovat bohatý text v Javě?
Aplikace formátování bohatého textu (písma, barvy, styly) přímo v Javě vám umožní generovat dokumenty, které vypadají profesionálně a odpovídají vašim firemním směrnicím, bez nutnosti ruční úpravy.

## Předpoklady

1. **Java Development Kit (JDK)** – jakákoli aktuální verze (8 nebo vyšší).  
2. **Aspose.Note pro Java JAR** – stáhněte jej z [odkaz ke stažení](https://releases.aspose.com/note/java/).  
3. **IDE** – IntelliJ IDEA, Eclipse nebo jakýkoli editor, který preferujete.  

## Import balíčků

Nejprve je třeba importovat potřebné balíčky do vašeho Java projektu. Přidejte následující importy na začátek vašeho Java souboru:

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

## Krok 1: Nastavení dokumentu a stránky

Začneme inicializací objektů `Document` a `Page`:

```java
String dataDir = "Your Document Directory";
Document doc = new Document();
Page page = new Page();
```

## Krok 2: Vytvoření nadpisu s formátováním

Nyní vytvoříme nadpis s formátovaným textem:

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

## Krok 3: Vytvoření bohatého textu s formátováním

Dále vytvoříme bohatý text s různými styly formátování:

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

## Krok 4: Přidání prvků na stránku a do dokumentu

Nyní přidáme nadpis a bohatý text na stránku a do struktury dokumentu:

```java
outlineElem.appendChildLast(text);
outline.appendChildLast(outlineElem);
page.setTitle(title);
page.appendChildLast(outline);
doc.appendChildLast(page);
```

## Krok 5: Uložení dokumentu

Nakonec uložíme vytvořený OneNote dokument jako PDF:

```java
doc.save(dataDir + "CreateOneNoteDocument_out.pdf", SaveFormat.Pdf);
```

## Časté problémy a řešení

| Problém | Řešení |
|-------|----------|
| **Soubor nenalezen** | Ověřte, že `dataDir` ukazuje na existující složku a máte oprávnění k zápisu. |
| **Chybějící písma** | Ujistěte se, že písma, na která odkazujete (např. *Calibri*), jsou nainstalována na hostitelském počítači. |
| **Licence nebyla použita** | Načtěte svou Aspose licenci před vytvořením `Document`, aby se předešlo vodoznakům z evaluační verze. |

## Často kladené otázky

**Otázka: Mohu dále přizpůsobit styly písma?**  
**Odpověď:** Ano, můžete upravit další vlastnosti, jako podtržení, přeškrtnutí a zarovnání textu pomocí tříd `TextStyle` a `ParagraphStyle`.

**Otázka: Je Aspose.Note pro Java kompatibilní se všemi Java IDE?**  
**Odpověď:** Ano. Dokud IDE podporuje standardní vývoj v Javě, můžete přidat Aspose.Note JAR do classpath projektu.

**Otázka: Mohu tuto funkci integrovat do webových aplikací?**  
**Odpověď:** Ano, stejný kód funguje v servlet‑based nebo Spring Boot aplikacích, což umožňuje dynamické generování OneNote‑na‑PDF na straně serveru.

**Otázka: Existují licenční požadavky pro používání Aspose.Note pro Java?**  
**Odpověď:** Ano, pro produkční použití je vyžadována komerční licence. Dočasná licence je k dispozici pro hodnocení a testování.

**Otázka: Podporuje Aspose.Note pro Java i jiné formáty dokumentů kromě OneNote?**  
**Odpověď:** Ano, podporuje PDF, HTML, PNG, JPEG a několik dalších exportních formátů, což vám poskytuje flexibilitu převádět stránky OneNote do požadovaného formátu.

## Závěr

V tomto průvodci jsme ukázali, jak **uložit OneNote jako PDF** a zároveň aplikovat formátování bohatého textu pomocí Aspose.Note pro Java. Dodržením krok za krokem můžete automatizovat tvorbu profesionálních OneNote dokumentů a převádět je do PDF v jakémkoli řešení založeném na Javě.

---

**Last Updated:** 2025-12-09  
**Testováno s:** Aspose.Note for Java 24.11 (latest at time of writing)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}