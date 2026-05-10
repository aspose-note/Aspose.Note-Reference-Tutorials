---
date: 2026-03-08
description: Naučte se, jak uložit OneNote jako PDF s čínským číslovaným seznamem
  pomocí Aspose.Note pro Javu. Podrobný krok‑za‑krokem průvodce, který pokrývá číslování,
  osnovy a export do PDF.
linktitle: Save OneNote as PDF with Chinese Numbered List – Aspose.Note
second_title: Aspose.Note Java API
title: Uložit OneNote jako PDF s čínským číslovaným seznamem – Aspose.Note
url: /cs/java/onenote-text-manipulation/create-chinese-numbered-list/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Uložte OneNote jako PDF s čínským číslovaným seznamem – Aspose.Note

## Úvod
Pokud chcete **uložit OneNote jako PDF** a přidat čínský číslovaný seznam, Aspose.Note pro Java to usnadňuje. V tomto tutoriálu vás provedeme přesné kroky k vytvoření čínského stylu osnovy, aplikaci číslování a exportu dokumentu OneNote do PDF. Na konci pochopíte **jak přidat číslování**, **přidat osnovu do OneNote** a uvidíte, proč je **Aspose.Note Java** knihovna volbou pro tento úkol.

## Rychlé odpovědi
- **Co tento tutoriál pokrývá?** Vytvoření čínského číslovaného seznamu v OneNote a uložení jako PDF pomocí Aspose.Note pro Java.  
- **Potřebuji licenci?** Bezplatná zkušební verze funguje pro testování; pro produkci je vyžadována komerční licence.  
- **Jaké IDE jsou podporovány?** Jakékoli Java IDE, jako Eclipse, IntelliJ IDEA nebo NetBeans.  
- **Mohu přizpůsobit styl seznamu?** Ano – písmo, velikost, barva a formát číslování jsou plně konfigurovatelné.  
- **Jak dlouho trvá implementace?** Přibližně 10‑15 minut pro základní seznam.

## Co je „uložit OneNote jako PDF“?
Uložení OneNote jako PDF převádí interaktivní stránku poznámkového bloku na statický, široce kompatibilní dokument. To je užitečné pro sdílení, archivaci nebo tisk při zachování původního rozvržení a jakéhokoli vlastního číslování, které jste použili.

## Proč použít Aspose.Note pro Java?
Aspose.Note poskytuje bohaté, výkonné API, které vám umožní programově vytvářet struktury OneNote, aplikovat složité číslování (včetně čínského číslování) a exportovat přímo do PDF bez ručních kroků v uživatelském rozhraní. Funguje napříč platformami, nevyžaduje instalaci Office a podporuje plnou kontrolu stylování.

## Předpoklady
1. **Java vývojové prostředí** – JDK 8+ a vaše oblíbené IDE.  
2. **Aspose.Note knihovna** – Stáhněte nejnovější JAR z oficiální stránky [here](https://releases.aspose.com/note/java/).  
3. **Základní znalost** syntaxe Java a objektově orientovaných konceptů.

## Import balíčků
Začněte importováním potřebných balíčků do vašeho Java projektu. Tyto importy vám poskytují přístup k funkcím vytváření dokumentů, stylování a číslování.

```java
import java.awt.Color;
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.NumberFormat;
import com.aspose.note.NumberList;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.ParagraphStyle;
```

Nyní si rozebráme implementaci krok po kroku.

## Jak uložit OneNote jako PDF s čínským číslovaným seznamem
Níže je podrobný, číslovaný průvodce. Každý krok obsahuje krátké vysvětlení následované přesným kódem, který je třeba zkopírovat.

### Krok 1: Vytvořit objekt Document
Začínáme vytvořením prázdné instance `Document`, která bude obsahovat obsah OneNote.

```java
// The path to the documents directory.
String dataDir = "Your Document Directory";
// create an object of the Document class
Document doc = new Document();
```

### Krok 2: Inicializovat objekt Page
Stránka OneNote funguje jako plátno pro osnovy a další prvky.

```java
// initialize Page class object
Page page = new Page();
```

### Krok 3: Inicializovat objekt Outline
Osnovy jsou kontejnery pro položky seznamu. Považujte je za držáky „odrážek/číslic“.

```java
// initialize Outline class object
Outline outline = new Outline();
```

### Krok 4: Inicializovat objekt TextStyle
Definujte výchozí styl odstavce, který bude aplikován na každou položku seznamu.

```java
// initialize TextStyle class object and set formatting properties
ParagraphStyle defaultStyle = new ParagraphStyle()
                                    .setFontColor(Color.black)
                                    .setFontName("Arial")
                                    .setFontSize(10);
```

### Krok 5: Inicializovat objekty OutlineElement a aplikovat číslování
Zde vytvoříme tři objekty OutlineElement, z nichž každý představuje položku seznamu. Používáme `NumberList("{0})", NumberFormat.ChineseCounting, "Arial", 10)`, abychom získali čínské číslování (一、二、三…).

```java
// initialize OutlineElement class objects and apply numbering
OutlineElement outlineElem1 = new OutlineElement();
outlineElem1.setNumberList(new NumberList("{0})", NumberFormat.ChineseCounting, "Arial", 10));
RichText text1 = new RichText().append("First");
text1.setParagraphStyle(defaultStyle);
outlineElem1.appendChildLast(text1);
OutlineElement outlineElem2 = new OutlineElement();
outlineElem2.setNumberList(new NumberList("{0})", NumberFormat.ChineseCounting, "Arial", 10));
RichText text2 = new RichText().append("Second");
text2.setParagraphStyle(defaultStyle);
outlineElem2.appendChildLast(text2);
OutlineElement outlineElem3 = new OutlineElement();
outlineElem3.setNumberList(new NumberList("{0})", NumberFormat.ChineseCounting, "Arial", 10));
RichText text3 = new RichText().append("Third");
text3.setParagraphStyle(defaultStyle);
outlineElem3.appendChildLast(text3);
```

### Krok 6: Přidat OutlineElementy
Připojte každý očíslovaný prvek k kontejneru osnovy.

```java
// add outline elements
outline.appendChildLast(outlineElem1);
outline.appendChildLast(outlineElem2);
outline.appendChildLast(outlineElem3);
```

### Krok 7: Přidat uzel Outline na stránku
Nyní umístíme celou osnovu na stránku.

```java
// add Outline node
page.appendChildLast(outline);
```

### Krok 8: Přidat uzel Page do dokumentu
Stránka se stane součástí celkového dokumentu OneNote.

```java
// add Page node
doc.appendChildLast(page);
```

### Krok 9: Uložit dokument jako PDF
Nakonec exportujeme dokument OneNote do PDF pomocí metody `save`. Toto je krok, kde **uložíme OneNote jako PDF**.

```java
// save the document
doc.save(dataDir + "CreateChineseNumberedList_out.pdf");
System.out.printf("File saved: %s\n", dataDir + "CreateChineseNumberedList_out.pdf");
```

Spuštěním výše uvedeného kódu vznikne PDF soubor (`CreateChineseNumberedList_out.pdf`), který obsahuje čínsky očíslovaný seznam, přesně tak, jak byste jej viděli na stránce OneNote.

## Časté problémy a řešení
- **Nesprávný formát číslování:** Ujistěte se, že používáte `NumberFormat.ChineseCounting`. Ostatní formáty (arabské, římské) vytvoří jiné výsledky.  
- **Chyba souboru nenalezen:** Ověřte, že `dataDir` ukazuje na existující, zapisovatelnou složku.  
- **Chybějící písmo:** Pokud není zadané písmo (např. „Arial“) nainstalováno na serveru, PDF může použít výchozí písmo. Nainstalujte písmo nebo vyberte jiné.

## Často kladené otázky

### Je Aspose.Note kompatibilní s různými Java IDE?
Ano, Aspose.Note je kompatibilní s populárními Java IDE, jako jsou Eclipse a IntelliJ IDEA.

### Mohu přizpůsobit formátování číslovaného seznamu?
Rozhodně. Jak je ukázáno v tutoriálu, můžete upravit písmo, barvu a velikost podle svých konkrétních požadavků.

### Je k dispozici zkušební verze pro Aspose.Note?
Ano, můžete prozkoumat zkušební verzi [zde](https://releases.aspose.com/).

### Kde najdu podrobnou dokumentaci pro Aspose.Note?
Odkaz na dokumentaci najdete [zde](https://reference.aspose.com/note/java/).

### Jak mohu získat podporu pro Aspose.Note?
Navštivte fórum podpory [zde](https://forum.aspose.com/c/note/28) pro jakoukoli pomoc nebo dotazy.

## Další FAQ (AI‑optimalizováno)

**Q: Mohu použít tento kód k přidání číslování v jiných jazycích?**  
A: Ano, nahraďte `NumberFormat.ChineseCounting` vhodnou hodnotou výčtu `NumberFormat` (např. `NumberFormat.RomanUpper`).

**Q: Zachovává PDF hierarchii osnovy?**  
A: Exportované PDF zachovává vizuální hierarchii, ale interaktivní navigace v osnově není ve statických PDF k dispozici.

**Q: Jak změním styl odrážek místo čísel?**  
A: Použijte `NumberList` s vlastním formátovacím řetězcem, např. `"• "` a nastavte `NumberFormat.None`.

**Q: Je možné přidat obrázky na stejnou stránku?**  
A: Ano, můžete vložit objekty `Image` na stránku před uložením do PDF.

**Q: Jaká verze Aspose.Note je vyžadována?**  
A: Nejnovější stabilní verze (k roku 2026) podporuje všechny zde předvedené funkce.

---

**Poslední aktualizace:** 2026-03-08  
**Testováno s:** Aspose.Note for Java 24.12  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}