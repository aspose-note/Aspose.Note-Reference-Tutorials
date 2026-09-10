---
date: 2026-04-30
description: Naučte se, jak **uložit OneNote jako PDF** a přidávat podstránky v OneNote
  pomocí Aspose.Note pro Javu. Postupujte podle tohoto krok‑za‑krokem průvodce a efektivně
  organizujte své poznámky.
keywords:
- save onenote as pdf
- add sub pages onenote
- Aspose.Note Java
linktitle: Jak uložit OneNote jako PDF a přidat podstránky
second_title: Aspose.Note Java API
title: Jak uložit OneNote jako PDF a přidat podstránky
url: /cs/java/onenote-page-manipulation/create-document-with-root-and-sub-pages/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak uložit OneNote jako PDF a přidat podstránky

## Úvod

V tomto tutoriálu se dozvíte **jak uložit onenote jako pdf** a vytvoříte dokument, který obsahuje jak kořenové, tak podstránky pomocí Aspose.Note for Java. Organizace vašich OneNote sešitů s jasnou hierarchií usnadňuje navigaci a export do PDF zajišťuje, že můžete své poznámky sdílet v univerzálně čitelném formátu. Také vám ukážeme, jak **přidat podstránky onenote** styl, abyste mohli snadno budovat víceúrovňové struktury.

## Rychlé odpovědi
- **Co znamená „save onenote as pdf“?** Odkazuje na export OneNote notebooku do PDF souboru pomocí Aspose.Note for Java.  
- **Které API je vyžadováno?** Aspose.Note for Java poskytuje potřebné třídy a metody.  
- **Mohu vytvořit hierarchické stránky?** Ano – nastavte úroveň stránky pro vytvoření kořenových stránek a podstránek.  
- **Potřebuji licenci pro produkční použití?** K dispozici je bezplatná zkušební verze, ale pro produkční použití je vyžadována komerční licence.  
- **Do jakých formátů mohu exportovat?** Kromě PDF můžete exportovat do BMP, PNG, JPEG, DOCX a dalších.

## Jak uložit OneNote jako PDF

Ukládání OneNote jako PDF převádí každou stránku sešitu do dokumentu s pevnou rozložením, který zachovává formátování, obrázky a hierarchii stránek. To je ideální pro sdílení, archivaci nebo tisk poznámek při zachování původní struktury.

## Proč přidávat podstránky onenote?

Přidání podstránek vám umožní seskupit související obsah pod nadřazenou stránkou, což napodobuje strukturu složek. Zlepšuje organizaci poznámek, urychluje vyhledávání a zvyšuje čitelnost při exportu sešitu do PDF.

## Požadavky

Před zahájením se ujistěte, že máte následující předpoklady:

1. **Java Development Kit (JDK)** – Ujistěte se, že máte nainstalovaný JDK ve vašem systému.  
2. **Aspose.Note for Java** – Stáhněte a nainstalujte Aspose.Note for Java z [webu](https://purchase.aspose.com/buy).  
3. **Integrated Development Environment (IDE)** – Vyberte Java IDE, jako je IntelliJ IDEA, Eclipse nebo NetBeans.

## Import balíčků

Začněte importováním potřebných balíčků ve vašem Java projektu:

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.SaveFormat;
import com.aspose.note.ParagraphStyle;
```

## Krok 1: Nastavení adresáře dokumentu

Definujte adresář, kam chcete uložit svůj OneNote dokument:

```java
String dataDir = "Your Document Directory";
```

## Krok 2: Vytvoření objektu Document

Vytvořte instanci objektu `Document`:

```java
Document doc = new Document();
```

## Krok 3: Vytvoření stránek

Inicializujte objekty stránek a nastavte jejich úrovně. Nastavení úrovně určuje, zda je stránka kořenová nebo podstránka:

```java
Page page1 = new Page();
page1.setLevel((byte) 1);

Page page2 = new Page();
page2.setLevel((byte) 2);

Page page3 = new Page();
page3.setLevel((byte) 1);
```

## Krok 4: Přidání uzlů na stránky

### Přidání uzlů na první stránku

```java
Outline outline = new Outline();
OutlineElement outlineElem = new OutlineElement();
ParagraphStyle textStyle = new ParagraphStyle()
                                    .setFontColor(Color.black)
                                    .setFontName("David Transparent")
                                    .setFontSize(10);

RichText text = new RichText().append("First page.");
text.setParagraphStyle(textStyle);

outlineElem.appendChildLast(text);
outline.appendChildLast(outlineElem);
page1.appendChildLast(outline);
```

### Přidání uzlů na druhou stránku

```java
Outline outline2 = new Outline();
OutlineElement outlineElem2 = new OutlineElement();
ParagraphStyle textStyle2 = new ParagraphStyle()
                                    .setFontColor(Color.black)
                                    .setFontName("David Transparent")
                                    .setFontSize(10);

RichText text2 = new RichText().append("Second page.");
text2.setParagraphStyle(textStyle2);

outlineElem2.appendChildLast(text2);
outline2.appendChildLast(outlineElem2);
page2.appendChildLast(outline2);
```

### Přidání uzlů na třetí stránku

```java
Outline outline3 = new Outline();
OutlineElement outlineElem3 = new OutlineElement();
ParagraphStyle textStyle3 = new ParagraphStyle()
                                    .setFontColor(Color.black)
                                    .setFontName("Broadway")
                                    .setFontSize(10);

RichText text3 = new RichText().append("Third page.");
text3.setParagraphStyle(textStyle3);

outlineElem3.appendChildLast(text3);
outline3.appendChildLast(outlineElem3);
page3.appendChildLast(outline3);
```

## Krok 5: Přidání stránek do dokumentu

```java
doc.appendChildLast(page1);
doc.appendChildLast(page2);
doc.appendChildLast(page3);
```

## Krok 6: Uložení dokumentu

Uložte OneNote dokument jako PDF (nebo BMP v tomto příkladu). Změna `SaveFormat` vám umožní exportovat do PDF, což splňuje požadavek „save onenote as pdf“:

```java
try {
    doc.save(dataDir + "GenerateRootAndSubLevelPagesInOneNote_out.bmp", SaveFormat.Bmp);
} catch (IOException e) {
    // Handle exception
}
```

> **Tip:** Pro přímý export do PDF nahraďte `SaveFormat.Bmp` za `SaveFormat.Pdf`.

Gratulujeme! Úspěšně jste vytvořili OneNote dokument s kořenovými a podstránkami a naučili se **jak uložit onenote jako pdf** pomocí Aspose.Note for Java.

## Proč je to důležité

- **Hierarchická organizace:** Kořenové a podstránky vám umožní napodobit strukturu složek v OneNote.  
- **Bezproblémový export do PDF:** Po organizaci export do PDF zachová hierarchii, což usnadňuje čtení a sdílení finálního dokumentu.  
- **Automatizace:** Kód lze integrovat do větších Java aplikací, což umožňuje hromadné vytváření strukturovaných sešitů.

## Časté problémy a jak se jim vyhnout

| Problém | Příčina | Řešení |
|-------|-------|----------|
| Stránky se zobrazují na stejné úrovni | Nesprávná hodnota `setLevel` | Použijte `setLevel((byte) 1)` pro kořenové stránky a `setLevel((byte) 2)` (nebo vyšší) pro podstránky. |
| Výstup PDF je prázdný | Chybí `SaveFormat.Pdf` nebo nesprávná cesta k souboru | Ověřte, že adresář existuje, a použijte `SaveFormat.Pdf`. |
| Písmo se neaplikuje | Špatný název písma nebo chybějící písmo v systému | Ujistěte se, že písmo (např. “David Transparent”) je nainstalováno na počítači, na kterém kód běží. |

## Často kladené otázky

**Q: Mohu vytvořit více úrovní podstránek pomocí Aspose.Note for Java?**  
A: Ano, můžete vytvářet hlubší hierarchie nastavením vyšších čísel úrovně (např. `setLevel((byte) 3)` pro třetí úroveň podstránky).

**Q: Je Aspose.Note for Java kompatibilní s různými Java IDE?**  
A: Rozhodně. Funguje s IntelliJ IDEA, Eclipse, NetBeans a jakýmkoli IDE, které podporuje vývoj v Javě.

**Q: Mohu přizpůsobit formátování textu v mém OneNote dokumentu?**  
A: Ano. Použijte `ParagraphStyle` k nastavení názvu písma, velikosti, barvy a dalších atributů pro každý prvek `RichText`.

**Q: Podporuje Aspose.Note for Java ukládání dokumentů v jiných formátech než BMP?**  
A: Ano. Podporované formáty zahrnují PDF, PNG, JPEG, DOCX a další. Změňte příslušně výčtový typ `SaveFormat`.

**Q: Je k dispozici zkušební verze Aspose.Note for Java?**  
A: Ano, můžete si stáhnout bezplatnou zkušební verzi z webu Aspose.

## Závěr

Organizace vašich OneNote sešitů s jasnou hierarchickou strukturou a jejich export jako PDF činí vaše poznámky přístupnějšími a snadněji sdílenými. Dodržením výše uvedených kroků nyní víte **jak uložit onenote jako pdf** a **přidat podstránky onenote** styl programově pomocí Aspose.Note for Java.

---

**Poslední aktualizace:** 2026-04-30  
**Testováno s:** Aspose.Note for Java 24.11 (latest)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}