---
title: Vytvořte dokument s kořenovými a podřízenými stránkami ve OneNotu
linktitle: Vytvořte dokument s kořenovými a podřízenými stránkami ve OneNotu
second_title: Aspose.Note Java API
description: Vytvořte dokument s kořenovými a podřízenými stránkami ve OneNotu pomocí Aspose.Note for Java. Postupujte podle podrobného průvodce pro efektivní uspořádání poznámek.
type: docs
weight: 11
url: /cs/java/onenote-page-manipulation/create-document-with-root-and-sub-pages/
---
## Úvod

V tomto kurzu vás provedeme procesem vytváření dokumentu s kořenovými a podřízenými stránkami ve OneNotu pomocí Aspose.Note for Java. Podle těchto kroků budete moci efektivně organizovat své dokumenty OneNotu pomocí hierarchické struktury.

## Předpoklady

Než začnete, ujistěte se, že máte následující předpoklady:

1. Java Development Kit (JDK): Ujistěte se, že máte v systému nainstalovaný JDK.
2. Aspose.Note for Java: Stáhněte a nainstalujte Aspose.Note for Java z[webová stránka](https://purchase.aspose.com/buy).
3. Integrované vývojové prostředí (IDE): Vyberte Java IDE, jako je IntelliJ IDEA, Eclipse nebo NetBeans.

## Importujte balíčky

Začněte importováním potřebných balíčků do vašeho projektu Java:

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

## Krok 1: Nastavte adresář dokumentů

Definujte adresář, kam chcete uložit dokument OneNotu:

```java
String dataDir = "Your Document Directory";
```

## Krok 2: Vytvořte objekt dokumentu

 Instantovat a`Document` objekt:

```java
Document doc = new Document();
```

## Krok 3: Vytvořte stránky

Inicializujte objekty stránky a nastavte jejich úrovně:

```java
Page page1 = new Page();
page1.setLevel((byte) 1);

Page page2 = new Page();
page2.setLevel((byte) 2);

Page page3 = new Page();
page3.setLevel((byte) 1);
```

## Krok 4: Přidejte uzly na stránky

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

## Krok 5: Přidejte stránky do dokumentu

```java
doc.appendChildLast(page1);
doc.appendChildLast(page2);
doc.appendChildLast(page3);
```

## Krok 6: Uložte dokument

Uložte dokument OneNotu:

```java
try {
    doc.save(dataDir + "GenerateRootAndSubLevelPagesInOneNote_out.bmp", SaveFormat.Bmp);
} catch (IOException e) {
    // Zpracovat výjimku
}
```

Gratulujeme! Úspěšně jste vytvořili dokument s kořenovými a podřízenými stránkami ve OneNotu pomocí Aspose.Note for Java.

## Závěr

Uspořádání dokumentů OneNotu pomocí hierarchické struktury je nezbytné pro lepší správu a navigaci. S Aspose.Note for Java můžete efektivně vytvářet dokumenty s kořenovými a podstránkami, které poskytují jasné a organizované rozvržení poznámek.

## FAQ

### Q1: Mohu vytvořit více úrovní podstránek pomocí Aspose.Note pro Java?

Odpověď 1: Ano, můžete vytvořit více úrovní podstránek nastavením příslušné úrovně pro každou stránku.

### Q2: Je Aspose.Note for Java kompatibilní s různými Java IDE?

Odpověď 2: Ano, Aspose.Note for Java je kompatibilní s populárními Java IDE, jako jsou IntelliJ IDEA, Eclipse a NetBeans.

### Q3: Mohu přizpůsobit formátování textu v dokumentu OneNote?

Odpověď 3: Ano, můžete upravit písmo, barvu, velikost a další možnosti formátování pomocí funkce Aspose.Note pro funkce formátovaného textu Java.

### Q4: Podporuje Aspose.Note pro Java ukládání dokumentů v různých formátech?

Odpověď 4: Ano, Aspose.Note pro Java podporuje ukládání dokumentů v různých formátech včetně BMP, PDF, PNG a dalších.

### Q5: Je k dispozici zkušební verze pro Aspose.Note pro Java?

Odpověď 5: Ano, z webu si můžete stáhnout bezplatnou zkušební verzi Aspose.Note pro Javu.