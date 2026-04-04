---
date: 2026-03-05
description: Naučte se, jak uložit OneNote jako PDF při vytváření číslovaného seznamu
  pomocí Aspose.Note pro Javu. Obsahuje kroky pro nastavení výchozího stylu textu
  a přizpůsobení číslování.
linktitle: Save OneNote as PDF – Create Numbered List with Aspose.Note
second_title: Aspose.Note Java API
title: Uložit OneNote jako PDF – Vytvořit číslovaný seznam pomocí Aspose.Note
url: /cs/java/onenote-text-manipulation/create-numbered-list/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Uložte OneNote jako PDF – Vytvořte číslovaný seznam pomocí Aspose.Note

## Úvod
Aspose.Note for Java umožňuje vývojářům Java **uložit OneNote jako PDF** a obohatit dokument o pokročilé formátování, například číslované seznamy. V tomto tutoriálu vás provedeme celým procesem – od nastavení výchozího textového stylu po přizpůsobení formátu číslování – abyste mohli exportovat OneNote do PDF s profesionálním vzhledem.

## Rychlé odpovědi
- **Co tento tutoriál pokrývá?** Vytvoření číslovaného seznamu v OneNote a uložení souboru jako PDF pomocí Aspose.Note for Java.  
- **Jaké primární klíčové slovo je cílem?** *save onenote as pdf*  
- **Potřebuji licenci?** K dispozici je bezplatná zkušební verze; pro produkční nasazení je vyžadována komerční licence.  
- **Jaká verze Javy je vyžadována?** JDK 8 nebo novější.  
- **Jak dlouho trvá implementace?** Přibližně 10–15 minut pro základní seznam.

## Co je „uložit OneNote jako PDF“?
Uložení OneNote jako PDF převádí bohatý textový stránku OneNote do přenosného dokumentu s pevnou rozložením, který lze sdílet napříč platformami bez nutnosti mít OneNote. To je zvláště užitečné pro archivaci, reportování nebo distribuci obsahu uživatelům, kteří nemají OneNote nainstalovaný.

## Proč vytvořit číslovaný seznam před exportem?
Číslovaný seznam přidává strukturu a čitelnost, což způsobí, že exportované PDF vypadá jako upravená zpráva. S Aspose.Note můžete **přizpůsobit formát číslování**, nastavit písma a řídit mezery – vše při zachování původního rozložení OneNote.

## Požadavky
Než se pustíte do práce, ujistěte se, že máte:

- Java Development Kit (JDK) nainstalovaný na vašem počítači.  
- Knihovnu Aspose.Note for Java staženou z [zde](https://releases.aspose.com/note/java/).

## Importování balíčků
Nejprve importujte požadované třídy, abyste mohli pracovat s objekty OneNote a konverzí do PDF.

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

## Jak uložit OneNote jako PDF s číslovaným seznamem?
Níže je krok‑za‑krokem průvodce, který ukazuje **jak vytvořit prvky seznamu**, **nastavit výchozí textový styl** a nakonec **exportovat OneNote do PDF**.

### Krok 1: Inicializace objektů Document, Page a Outline
Začínáme vytvořením základních struktur OneNote. Toto také ukazuje použití **add outline element java**.

```java
// Your Document Directory
String dataDir = "Your Document Directory";
// Create Document, Page, and Outline objects
Document doc = new Document();
Page page = new Page();
Outline outline = new Outline();
// Set default text style
ParagraphStyle defaultStyle = new ParagraphStyle()
                                        .setFontColor(Color.black)
                                        .setFontName("Arial")
                                        .setFontSize(10);
Document doc = new Document();
Page page = new Page();
Outline outline = new Outline();
```

> **Tip:** Uchovávejte cestu `dataDir` jako absolutní nebo použijte `System.getProperty("user.dir")`, abyste se vyhnuli problémům s cestou.

### Krok 2: Nastavení výchozího textového stylu
Konzistentní styl zajišťuje, že seznam vypadá jednotně napříč všemi položkami.

```java
ParagraphStyle defaultStyle = new ParagraphStyle()
                                        .setFontColor(Color.black)
                                        .setFontName("Arial")
                                        .setFontSize(10);
```

### Krok 3: Vytvoření Outline prvků (číslovaný seznam)
Zde **přizpůsobujeme formát číslování** pomocí `NumberList`. Vzor `"{0})"` vytváří „1)“, „2)“ atd.

```java
OutlineElement outlineElem1 = new OutlineElement();
outlineElem1.setNumberList(new NumberList("{0})", NumberFormat.DecimalNumbers, "Arial", 10));
RichText text1 = new RichText().append("First");
text1.setParagraphStyle(defaultStyle);
outlineElem1.appendChildLast(text1);
// Repeat for other elements (outlineElem2 and outlineElem3)
```

> **Proč je to důležité:** Připojením `NumberList` k jednotlivým `OutlineElement` získáte plnou kontrolu nad stylem číslování, písmem a velikostí.

### Krok 4: Přidání Outline prvků do Outline
Nyní seskupíme jednotlivé položky seznamu do jednoho outline.

```java
outline.appendChildLast(outlineElem1);
outline.appendChildLast(outlineElem2);
outline.appendChildLast(outlineElem3);
```

### Krok 5: Připojení Outline k stránce
Outline se stane součástí hierarchie stránky OneNote.

```java
page.appendChildLast(outline);
```

### Krok 6: Uložení dokumentu jako PDF
Nakonec **uložíme OneNote jako PDF**. Výstupní soubor bude obsahovat číslovaný seznam přesně tak, jak byl definován.

```java
doc.appendChildLast(page);
doc.save(dataDir + "CreateNumberedList_out.pdf");
System.out.printf("File saved: %s\n", dataDir + "CreateNumberedList_out.pdf");
```

Spuštěním výše uvedeného kódu se vygeneruje PDF pojmenované `CreateNumberedList_out.pdf` ve vámi určeném adresáři, přičemž zachová formát číslovaného seznamu.

## Časté problémy a řešení
| Problém | Řešení |
|-------|----------|
| **PDF je prázdný** | Ujistěte se, že `doc.appendChildLast(page);` je voláno před `doc.save()`. |
| **Číslování se nezobrazuje** | Ověřte, že je správně nastaven vzor `NumberList` a `NumberFormat`. |
| **Chyba soubor nenalezen** | Použijte absolutní cestu pro `dataDir` nebo vytvořte adresář předem. |
| **Neshoda písma** | Nainstalujte písmo (např. Arial) na počítači, kde kód běží. |

## Často kladené otázky
### Q: Mohu přizpůsobit formát číslování v mém OneNote seznamu?
A: Rozhodně! Můžete přizpůsobit formát číslování pomocí třídy `NumberList`, kterou poskytuje Aspose.Note for Java.

### Q: Je k dispozici zkušební verze pro Aspose.Note for Java?
A: Ano, můžete si stáhnout bezplatnou zkušební verzi [zde](https://releases.aspose.com/).

### Q: Jak mohu získat podporu pro Aspose.Note for Java?
A: Navštivte [forum Aspose.Note for Java](https://forum.aspose.com/c/note/28) pro komunitní podporu.

### Q: Kde najdu podrobnou dokumentaci pro Aspose.Note for Java?
A: Podívejte se na [dokumentaci](https://reference.aspose.com/note/java/) pro komplexní informace.

### Q: Jak si mohu zakoupit licenci pro Aspose.Note for Java?
A: Licenci můžete zakoupit [zde](https://purchase.aspose.com/buy).

## Závěr
V tomto tutoriálu jsme ukázali, jak **uložit OneNote jako PDF** a zároveň vytvořit čistý číslovaný seznam pomocí Aspose.Note for Java. Nastavením výchozího textového stylu, přizpůsobením formátu číslování a následováním krok‑za‑krokem průvodce můžete rychle a spolehlivě generovat profesionální PDF z OneNote stránek.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Last Updated:** 2026-03-05  
**Tested With:** Aspose.Note for Java 24.11  
**Author:** Aspose