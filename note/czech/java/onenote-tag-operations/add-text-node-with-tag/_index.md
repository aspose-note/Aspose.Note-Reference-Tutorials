---
title: Přidat textový uzel s tagem ve OneNotu – Aspose.Note
linktitle: Přidat textový uzel s tagem ve OneNotu – Aspose.Note
second_title: Aspose.Note Java API
description: Prozkoumejte, jak přidat textové uzly se značkami ve OneNotu pomocí Aspose.Note pro Java. Snadné, efektivní a přátelské pro vývojáře. Stáhněte si knihovnu nyní!
weight: 13
url: /cs/java/onenote-tag-operations/add-text-node-with-tag/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Přidat textový uzel s tagem ve OneNotu – Aspose.Note

## Úvod
V tomto tutoriálu prozkoumáme, jak přidat textový uzel se značkou ve OneNotu pomocí Aspose.Note pro Java. Aspose.Note je výkonná knihovna Java, která umožňuje vývojářům pracovat se soubory Microsoft OneNote programově. Přidávání textových uzlů pomocí značek je běžným požadavkem při zpracování dokumentů a Aspose.Note tento úkol zjednodušuje.
## Předpoklady
Než se pustíme do výukového programu, ujistěte se, že máte následující předpoklady:
- Základní znalost programování v Javě.
-  Nainstalovaná knihovna Aspose.Note pro Java. Můžete si jej stáhnout[tady](https://releases.aspose.com/note/java/).
- Integrované vývojové prostředí (IDE) nastavené pro vývoj v Javě.
## Importujte balíčky
Začněte importem potřebných balíčků pro váš projekt Java. Do kódu zahrňte následující importy:
```java
import java.awt.Color;
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.NoteTag;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.TagIcon;
import com.aspose.note.ParagraphStyle;
```
## Krok 1: Vytvořte objekt dokumentu
Inicializujte objekt třídy Document, aby reprezentoval dokument OneNotu:
```java
// Cesta k adresáři dokumentů.
String dataDir = "Your Document Directory";
//Vytvořte objekt třídy Document
Document doc = new Document();
```
## Krok 2: Inicializujte objekt třídy stránky
Inicializujte objekt třídy Page, aby reprezentoval stránku v dokumentu:
```java
// Inicializujte objekt třídy Page
Page page = new Page();
```
## Krok 3: Inicializujte objekt třídy osnovy
Inicializujte objekt třídy Outline, abyste strukturovali obsah na stránce:
```java
// Inicializovat objekt třídy Outline
Outline outline = new Outline();
```
## Krok 4: Inicializujte objekt třídy OutlineElement
Inicializujte objekt třídy OutlineElement, aby reprezentoval prvek v rámci osnovy:
```java
// Inicializujte objekt třídy OutlineElement
OutlineElement outlineElem = new OutlineElement();
```
## Krok 5: Přizpůsobte styl textu
Nastavte styl pro textový uzel, jako je barva písma, název a velikost:
```java
// Přizpůsobte styl textu
ParagraphStyle textStyle = new ParagraphStyle()
                                .setFontColor(Color.BLACK)
                                .setFontName("Arial")
                                .setFontSize(10);
```
## Krok 6: Vytvořte objekt RichText
Vytvořte objekt RichText a připojte k němu požadovaný text:
```java
// Vytvořte objekt RichText
RichText text = new RichText().append("OneNote text.");
text.setParagraphStyle(textStyle);
```
## Krok 7: Přidejte poznámku
Přidejte k textu značku poznámky, například žlutou hvězdu:
```java
// Přidat značku poznámky
NoteTag noteTag = NoteTag.createYellowStar();
text.getTags().add(noteTag);
```
## Krok 8: Přidejte textový uzel
Přidejte textový uzel do prvku osnovy:
```java
// Přidat textový uzel
outlineElem.appendChildLast(text);
```
## Krok 9: Přidejte prvek obrysu do obrysu
Přidejte prvek obrysu do obrysu:
```java
// Přidejte uzel prvku obrysu
outline.appendChildLast(outlineElem);
```
## Krok 10: Přidejte obrys na stránku
Přidejte obrys na stránku:
```java
// Přidat obrysový uzel
page.appendChildLast(outline);
```
## Krok 11: Přidejte stránku do dokumentu
Přidejte stránku do dokumentu:
```java
// Přidat uzel stránky
doc.appendChildLast(page);
```
## Krok 12: Uložte dokument OneNotu
Uložte dokument OneNotu do určeného adresáře:
```java
// Uložte dokument OneNotu
doc.save(dataDir + "AddTextNodeWithTag_out.one");
```
Gratulujeme! Úspěšně jste přidali textový uzel se značkou ve OneNotu pomocí Aspose.Note pro Java.
## Závěr
V tomto tutoriálu jsme se zabývali procesem přidávání textového uzlu se značkou ve OneNotu krok za krokem pomocí knihovny Aspose.Note for Java. Tato výkonná knihovna zjednodušuje úlohy zpracování dokumentů a usnadňuje vývojářům programově manipulovat se soubory OneNotu.
## Často kladené otázky
### Otázka: Mohu používat Aspose.Note pro Javu s jinými Java knihovnami?
Odpověď: Ano, Aspose.Note for Java lze bez problémů integrovat s jinými knihovnami Java, aby se zlepšily možnosti zpracování dokumentů.
### Otázka: Je k dispozici bezplatná zkušební verze pro Aspose.Note pro Java?
 Odpověď: Ano, máte přístup k bezplatné zkušební verzi[tady](https://releases.aspose.com/).
### Otázka: Jak mohu získat podporu pro Aspose.Note pro Java?
Odpověď: Můžete požádat o podporu komunitu Aspose.Note[Fórum](https://forum.aspose.com/c/note/28).
### Otázka: Jsou k dispozici dočasné licence pro Aspose.Note pro Java?
 Odpověď: Ano, můžete získat dočasné licence[tady](https://purchase.aspose.com/temporary-license/).
### Otázka: Kde najdu dokumentaci k Aspose.Note pro Java?
 Odpověď: Dokumentace je k dispozici[tady](https://reference.aspose.com/note/java/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
