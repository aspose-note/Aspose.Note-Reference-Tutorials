---
date: 2026-03-21
description: Naučte se, jak vytvořit dokument OneNote a nastavit alternativní text
  obrázku pomocí Javy s Aspose.Note. Tento průvodce také ukazuje, jak uložit soubor
  OneNote a zlepšit přístupnost.
linktitle: Create OneNote Document & Add Alt Text to Images in Java
second_title: Aspose.Note Java API
title: Vytvořte dokument OneNote a přidejte alternativní text k obrázkům v Javě
url: /cs/java/onenote-image-alternative-text/add-alternative-text-to-image/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Vytvoření dokumentu OneNote a přidání alternativního textu k obrázkům v Javě

## Úvod

V tomto tutoriálu se naučíte **jak vytvořit dokument OneNote** programově a **nastavit alternativní text obrázku** pomocí Javy a Aspose.Note API. Přidání alternativního textu činí vaše stránky OneNote přístupnými pro uživatele čteček obrazovky, zlepšuje vyhledatelnost a pomáhá vám **uložit soubor OneNote** s bohatšími metadaty. Na konci průvodce budete schopni **přidat obrázek onenote** stránek, nastavit jak název, tak popis obrázku, a soubor uložit na disk.

## Rychlé odpovědi
- **Jaká knihovna je vyžadována?** Aspose.Note for Java  
- **Na jaké primární klíčové slovo je tento tutoriál zaměřen?** create onenote document  
- **Potřebuji licenci pro produkci?** Ano, je vyžadována komerční licence (k dispozici je bezplatná zkušební verze).  
- **Mohu přidat alternativní text k více obrázkům?** Rozhodně – stačí opakovat kroky pro každý obrázek.  
- **Jaká verze Javy je podporována?** Java 8 nebo vyšší.

## Co znamená „create onenote document“ v kontextu OneNote?

Vytvoření dokumentu OneNote znamená programově vytvořit soubor `.one`, který může obsahovat stránky, text, obrázky a další bohatý obsah. S Aspose.Note můžete tento soubor generovat od nuly, přidávat prvky a pak **uložit soubor OneNote** na libovolné místo.

## Proč přidávat alternativní text k obrázkům v OneNote?

- **Přístupnost:** Splňuje směrnice WCAG a pomáhá uživatelům se zrakovým postižením.  
- **Vyhledatelnost:** Vyhledávače mohou indexovat popis, což zvyšuje objevitelnost vašeho obsahu.  
- **Profesionalita:** Ukazuje závazek k inkluzivnímu designu a kvalitě dokumentace.

## Požadavky

Před ponořením se do tutoriálu se ujistěte, že máte následující požadavky:

1. Java Development Kit (JDK) – verze 8 nebo novější.  
2. Aspose.Note for Java Library – stáhněte ji z [zde](https://releases.aspose.com/note/java/).  
3. IDE, například IntelliJ IDEA nebo Eclipse.  
4. Základní znalost programování v Javě.

## Import balíčků

Nejprve importujte potřebné balíčky do svého Java projektu, abyste mohli využívat funkce Aspose.Note.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Image;
import com.aspose.note.Page;
```

Nyní projděme **průvodce krok za krokem** k **vytvoření dokumentu OneNote**, přidání obrázku a **nastavení alternativního textu obrázku**.

## Jak vytvořit dokument OneNote a nastavit alternativní text obrázku v Javě

### Krok 1: Nastavení adresáře dokumentu

```java
String dataDir = "Your Document Directory";
```

Nahraďte `"Your Document Directory"` absolutní cestou, kde se nachází váš zdrojový obrázek a kam chcete uložit výstupní soubor `.one`.

### Krok 2: Vytvoření objektu Document

```java
Document document = new Document();
```

Tento řádek **vytváří nový dokument OneNote**, který později **uložíte jako soubor OneNote** s přidaným obsahem.

### Krok 3: Vytvoření objektu Page

```java
Page page = new Page();
```

Stránka slouží jako plátno pro obrázek a jakékoli další prvky, které chcete přidat.

### Krok 4: Přidání obrázku na stránku

```java
Image image = new Image(null, dataDir + "image.jpg");
```

Konstruktor `Image` načte soubor obrázku ze zadané cesty. Toto je místo, kde **přidáte obrázek onenote**.

### Krok 5: Nastavení titulku alternativního textu (nastavení alternativního textu obrázku)

```java
image.setAlternativeTextTitle("ImageAlternativeText Title");
```

Zde **nastavujeme alternativní text obrázku**, který slouží jako stručný titulek obrázku.

### Krok 6: Nastavení popisu alternativního textu (nastavení popisu alt textu)

```java
image.setAlternativeTextDescription("ImageAlternativeText Description");
```

Popis poskytuje podrobnější vysvětlení – ideální pro čtečky obrazovky.

### Krok 7: Přidání obrázku na stránku

```java
page.appendChildLast(image);
```

Nyní je obrázek, obohacený o alternativní text, **přidán na stránku OneNote**.

### Krok 8: Přidání stránky do dokumentu

```java
document.appendChildLast(page);
```

Připojte stránku k dokumentu OneNote, který jste vytvořili dříve.

### Krok 9: Uložení dokumentu (uložení souboru OneNote)

```java
document.save(dataDir + "AlternativeText_out.one");
```

Volání `save` **zapíše soubor OneNote** na disk a zachová veškerá metadata alt‑textu.

## Časté problémy a řešení

- **FileNotFoundException:** Ověřte, že `dataDir` ukazuje na správnou složku a že `image.jpg` existuje.  
- **NullPointerException on image:** Ujistěte se, že cesta k obrázku je platná a soubor není poškozený.  
- **License errors:** Použijte platný licenční soubor Aspose.Note nebo spusťte v režimu zkušební verze pro hodnocení.

## Často kladené otázky

**Q: Mohu přidat alternativní text k více obrázkům v jednom dokumentu?**  
A: Ano, stačí opakovat kroky 4‑6 pro každý obrázek, který chcete anotovat.

**Q: Jaké formáty obrázků jsou podporovány pro přidání alt textu?**  
A: Aspose.Note podporuje JPEG, PNG, GIF, BMP a několik dalších běžných formátů.

**Q: Je možné upravit nebo odstranit alt text po jeho nastavení?**  
A: Rozhodně. Zavolejte `setAlternativeTextTitle("")` nebo `setAlternativeTextDescription("")` pro vymazání hodnot, nebo poskytněte nové řetězce pro jejich aktualizaci.

**Q: Poskytuje Aspose.Note API i pro jiné jazyky kromě Javy?**  
A: Ano, knihovna je také k dispozici pro .NET, C++ a Python.

**Q: Kde si mohu stáhnout zkušební verzi Aspose.Note?**  
A: Bezplatnou zkušební verzi můžete získat z [zde](https://releases.aspose.com/).

**Q: Jak programově **uložit soubor OneNote** po přidání více stránek?**  
A: Zavolejte `document.save(<outputPath>)` jednou po přidání všech stránek a obrázků; API provede kompletní vytvoření souboru.

**Q: Mohu použít stejný kód k **přidání obrázku onenote** v existujícím dokumentu?**  
A: Ano. Načtěte existující dokument pomocí `new Document(<filePath>)` a poté postupujte podle kroků 3‑7 pro přidání nových obrázků a alt textu.

## Závěr

Po absolvování tohoto průvodce nyní víte **jak vytvořit dokument OneNote**, **přidat obrázek onenote** a **nastavit alternativní text obrázku** pomocí Javy. Implementace těchto kroků nejenže činí vaše soubory OneNote přístupnějšími, ale také zlepšuje jejich vyhledatelnost a celkovou kvalitu. Nebojte se experimentovat s různými tituly a popisy, abyste co nejlépe vyjádřili význam každého obrázku.

---

**Poslední aktualizace:** 2026-03-21  
**Testováno s:** Aspose.Note for Java 24.11  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}