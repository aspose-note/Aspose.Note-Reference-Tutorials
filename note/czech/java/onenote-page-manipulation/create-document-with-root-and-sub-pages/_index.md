---
description: Naučte se, jak pomocí Aspose.Note pro Javu uložit PDF z OneNote a přidat
  podstránky v OneNote. Postupujte podle tohoto krok‑za‑krokem průvodce a efektivně
  organizujte své poznámky.
linktitle: How to Save OneNote PDF and Add Sub Pages
second_title: Aspose.Note Java API
title: Jak uložit PDF z OneNote a přidat podstránky
url: /cs/java/onenote-page-manipulation/create-document-with-root-and-sub-pages/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak uložit OneNote PDF a přidat podstránky

## Úvod

V tomto tutoriálu se dozvíte **how to save OneNote PDF** a zároveň vytvoříte dokument, který obsahuje jak kořenové, tak podstránky pomocí Aspose.Note for Java. Organizace vašich OneNote sešitů s jasnou hierarchií usnadňuje navigaci a možnost exportu do PDF zajišťuje, že své poznámky můžete sdílet v univerzálně čitelném formátu. Také vám ukážeme, jak **add sub pages onenote** styl, takže můžete snadno vytvářet víceúrovňové struktury.

## Rychlé odpovědi
- **Co znamená primární klíčové slovo?** Odkazuje na export OneNote sešitu do PDF pomocí Aspose.Note.  
- **Které API se používá?** Aspose.Note for Java.  
- **Mohu vytvářet hierarchické stránky?** Ano – nastavte úroveň stránky pro vytvoření kořenových a podstránek.  
- **Potřebuji licenci?** K dispozici je bezplatná zkušební verze; pro produkční použití je vyžadována komerční licence.  
- **Jaké výstupní formáty jsou podporovány?** BMP, PDF, PNG a další.

## Co je “how to save OneNote PDF”?
Ukládání OneNote jako PDF převádí stránky sešitu do dokumentu s pevnou rozvržením, který zachovává formátování, obrázky a hierarchii. To je ideální pro sdílení, archivaci nebo tisk poznámek.

## Proč přidávat podstránky onenote?
Přidání podstránek vám umožní seskupit související obsah pod nadřazenou stránkou, což napodobuje strukturu složek. Zlepšuje organizaci poznámek, urychluje vyhledávání a zvyšuje čitelnost při exportu sešitu do PDF.

## Požadavky

Než začnete, ujistěte se, že máte následující požadavky:

1. Java Development Kit (JDK): Ujistěte se, že máte JDK nainstalovaný ve svém systému.  
2. Aspose.Note for Java: Stáhněte a nainstalujte Aspose.Note for Java z [webové stránky](https://purchase.aspose.com/buy).  
3. Integrované vývojové prostředí (IDE): Vyberte si Java IDE, například IntelliJ IDEA, Eclipse nebo NetBeans.

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

Uložte OneNote dokument jako PDF (nebo BMP v tomto příkladu). Změna `SaveFormat` vám umožní exportovat do PDF, což splňuje požadavek “how to save OneNote PDF”:

```java
try {
    doc.save(dataDir + "GenerateRootAndSubLevelPagesInOneNote_out.bmp", SaveFormat.Bmp);
} catch (IOException e) {
    // Handle exception
}
```

> **Tip:** Pro přímý export do PDF nahraďte `SaveFormat.Bmp` za `SaveFormat.Pdf`.

Gratulujeme! Úspěšně jste vytvořili OneNote dokument s kořenovými a podstránkami a naučili se **how to save OneNote PDF** pomocí Aspose.Note for Java.

## Proč je to důležité

- **Hierarchická organizace:** Kořenové a podstránky vám umožní napodobit strukturu složek uvnitř OneNote.  
- **Plynulý export do PDF:** Po uspořádání export do PDF zachová hierarchii, což usnadňuje čtení a sdílení finálního dokumentu.  
- **Automatizace:** Kód může být integrován do větších Java aplikací, což umožňuje hromadné vytváření strukturovaných sešitů.

## Časté problémy a jak se jim vyhnout

| Problém | Příčina | Řešení |
|---------|---------|--------|
| Stránky se zobrazují na stejné úrovni | Nesprávná hodnota `setLevel` | Použijte `setLevel((byte) 1)` pro kořenové stránky a `setLevel((byte) 2)` (nebo vyšší) pro podstránky. |
| Výstup PDF je prázdný | Chybí `SaveFormat.Pdf` nebo nesprávná cesta k souboru | Ověřte, že adresář existuje, a použijte `SaveFormat.Pdf`. |
| Písmo se neaplikuje | Špatný název písma nebo chybějící písmo v systému | Ujistěte se, že písmo (např. “David Transparent”) je nainstalováno na počítači, kde kód běží. |

## Často kladené otázky

**Q: Mohu pomocí Aspose.Note for Java vytvořit více úrovní podstránek?**  
A: Ano, můžete vytvářet hlubší hierarchie nastavením vyšších čísel úrovně (např. `setLevel((byte) 3)` pro třetí úroveň podstránky).

**Q: Je Aspose.Note for Java kompatibilní s různými Java IDE?**  
A: Rozhodně. Funguje s IntelliJ IDEA, Eclipse, NetBeans i s jakýmkoli IDE, které podporuje vývoj v Javě.

**Q: Můžu přizpůsobit formátování textu v mém OneNote dokumentu?**  
A: Ano. Použijte `ParagraphStyle` k nastavení názvu písma, velikosti, barvy a dalších atributů pro každý prvek `RichText`.

**Q: Podporuje Aspose.Note for Java ukládání dokumentů v jiných formátech než BMP?**  
A: Ano. Podporované formáty zahrnují PDF, PNG, JPEG, DOCX a další. Změňte příslušně enum `SaveFormat`.

**Q: Existuje zkušební verze Aspose.Note for Java?**  
A: Ano, můžete si stáhnout bezplatnou zkušební verzi z webu Aspose.

## Závěr

Organizace vašich OneNote sešitů s jasnou hierarchickou strukturou a jejich export do PDF činí vaše poznámky přístupnějšími a snadněji sdílenými. Dodržením výše uvedených kroků nyní víte, **how to save OneNote PDF** a **add sub pages onenote** styl programově pomocí Aspose.Note for Java.

---

**Poslední aktualizace:** 2026-01-07  
**Testováno s:** Aspose.Note for Java 24.11 (latest)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}