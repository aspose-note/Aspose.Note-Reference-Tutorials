---
date: 2025-12-02
description: Naučte se, jak vytvořit stránku OneNote s titulkem v Javě pomocí Aspose.Note
  pro Javu. Tento průvodce ukazuje, jak nastavit titulek stránky OneNote a přizpůsobit
  písmo titulku.
linktitle: How to Create OneNote Page with Title - Java
second_title: Aspose.Note Java API
title: Jak vytvořit stránku OneNote s názvem – Java
url: /cs/java/onenote-document-loading/create-onenote-doc-page-title/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak vytvořit stránku OneNote s názvem – Java

## Úvod

Pokud potřebujete **jak vytvořit stránku OneNote** programově, Aspose.Note pro Java to usnadňuje. V tomto tutoriálu se naučíte, jak vygenerovat soubor OneNote, nastavit název stránky a dokonce přizpůsobit písmo názvu – vše z Java kódu. Na konci budete mít připravený dokument OneNote, který můžete integrovat do jakékoli Java aplikace.

## Rychlé odpovědi
- **Jaká knihovna je vyžadována?** Aspose.Note pro Java.
- **Mohu nastavit vlastní písmo pro název?** Ano – použijte `ParagraphStyle` k definování názvu písma, velikosti a barvy.
- **Jaká verze Javy je podporována?** Jakákoli JDK 8+ (API je zpětně kompatibilní).
- **Potřebuji licenci pro vývoj?** Pro testování stačí bezplatná zkušební verze; pro produkci je licence vyžadována.
- **Kam se ukládá výstup?** Cestu definujete v proměnné `dataDir`.

## Co je název stránky OneNote?
Název stránky OneNote je záhlaví zobrazené v horní části každé stránky. Obvykle obsahuje název stránky, datum vytvoření a čas. Nastavení tohoto názvu programově vám pomůže vytvořit konzistentní a dobře strukturované poznámkové bloky.

## Proč nastavit název stránky OneNote programově?
- **Automatizace:** Generujte zprávy nebo zápisy ze schůzek bez ruční úpravy.  
- **Konzistence:** Vynucujte pojmenovací konvenci napříč všemi stránkami.  
- **Integrace:** Propojte OneNote s jinými systémy (např. CRM, nástroje pro řízení projektů).  

## Předpoklady

- **Java Development Kit (JDK)** – verze 8 nebo vyšší.  
- **Aspose.Note pro Java** – stáhněte ze oficiálního webu **[zde](https://releases.aspose.com/note/java/)**.  
- **IDE** – IntelliJ IDEA, Eclipse nebo NetBeans (dle vaší volby).

## Import balíčků

Nejprve importujte třídy, které budeme potřebovat z knihovny Aspose.Note.

```java
import com.aspose.note.*;
import java.awt.*;
import java.io.IOException;
import java.util.Calendar;
```

### Krok 1: Nastavení adresáře dokumentu  
Definujte, kam bude vygenerovaný soubor OneNote uložen.

```java
// The path to the documents directory.
String dataDir = "Your Document Directory";
```

### Krok 2: Vytvoření objektu Document  
Instancujte nový `Document` – představuje soubor OneNote, který budete budovat.

```java
// Create an object of the Document class
Document doc = new Document();
```

### Krok 3: Inicializace objektu Page  
Vytvořte objekt `Page`, který bude obsahovat název i další obsah.

```java
// Initialize Page class object
Page page = new Page();
```

### Krok 4: Nastavení výchozího stylu textu  
Definujte výchozí `ParagraphStyle`, který bude aplikován na text názvu. Zde **přizpůsobujete písmo názvu OneNote**.

```java
// Default style for all text in the document.
ParagraphStyle textStyle = new ParagraphStyle()
                            .setFontColor(Color.BLACK)
                            .setFontName("Arial")
                            .setFontSize(10);
```

### Krok 5: Nastavení vlastností názvu stránky  
Zde **nastavujete podrobnosti názvu stránky OneNote** – text názvu, datum a čas. Upravit řetězce podle potřeby.

```java
// Set page title properties
Title title = new Title();

RichText titleText = new RichText().append("Title text.");
titleText.setParagraphStyle(textStyle);
title.setTitleText(titleText);

Calendar cal = Calendar.getInstance();
cal.set(2018, 04, 03);
RichText titleDate = new RichText().append(cal.getTime().toString());
titleDate.setParagraphStyle(textStyle);
title.setTitleDate(titleDate);

RichText titleTime = new RichText().append("12:34");
titleTime.setParagraphStyle(textStyle);
title.setTitleText(titleTime);
```

### Krok 6: Přiřazení názvu ke stránce  
Nyní **přidáte název do OneNote** propojením objektu `Title` s objektem `Page`.

```java
page.setTitle(title);
```

### Krok 7: Připojení stránky k dokumentu  
Přidejte nakonfigurovanou stránku do struktury dokumentu.

```java
doc.appendChildLast(page);
```

### Krok 8: Uložení dokumentu OneNote  
Zadejte název výstupního souboru a uložte poznámkový blok. Tím se dokončí proces **java create onenote file**.

```java
dataDir = dataDir + "load//CreateDocWithPageTitle_out.one";

// Save OneNote document
doc.save(dataDir);
```

## Časté problémy a tipy

| Problém | Řešení |
|-------|----------|
| **Neplatná cesta k souboru** | Ujistěte se, že `dataDir` končí správným oddělovačem (`/` nebo `\\`) a že složka existuje. |
| **Název se nezobrazuje** | Ověřte, že `ParagraphStyle` je aplikován na každý `RichText` prvek. |
| **Výjimka licence** | Pro testování použijte zkušební licenci; před nasazením aplikujte plnou licenci. |
| **Špatný měsíc v datu** | Měsíce v Javě jsou nulově indexované; `cal.set(2018, 04, 03)` ve skutečnosti nastaví květen. Upravte podle potřeby. |

## Často kladené otázky

**Q: Je Aspose.Note pro Java kompatibilní s různými verzemi Javy?**  
A: Ano, knihovna funguje s Java 8 a novějšími, což vám poskytuje flexibilitu napříč prostředími.

**Q: Mohu přizpůsobit styl písma a velikost názvu stránky?**  
A: Rozhodně! Použijte `ParagraphStyle` (jak je ukázáno v kroku 4) k nastavení libovolného názvu písma, velikosti a barvy.

**Q: Jak přidám další obsah (např. odstavce, obrázky) na stránku?**  
A: Vytvořte další objekty `RichText` nebo `Image`, nastavte jejich styly a přidejte je na `Page` pomocí `page.appendChildLast(yourObject)`.

**Q: Existuje zkušební verze Aspose.Note pro Java?**  
A: Ano, můžete si stáhnout bezplatnou zkušební verzi z webu Aspose a vyzkoušet všechny funkce.

**Q: Kde mohu získat podporu, pokud narazím na problémy?**  
A: Navštivte [Aspose.Note fórum](https://forum.aspose.com/c/note/28) pro komunitní pomoc nebo otevřete tiket podpory u Aspose.

---

**Poslední aktualizace:** 2025-12-02  
**Testováno s:** Aspose.Note pro Java 24.12 (nejnovější v době psaní)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}