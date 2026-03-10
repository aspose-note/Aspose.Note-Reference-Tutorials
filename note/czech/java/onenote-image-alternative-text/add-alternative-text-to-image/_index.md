---
date: 2025-12-23
description: Naučte se, jak přidat alternativní text k obrázkům v dokumentech OneNote
  pomocí Javy a Aspose.Note. Tento průvodce ukazuje, jak přidat alternativní text
  k obrázku pro lepší přístupnost.
linktitle: How to Add Alt Text to Image in OneNote using Java
second_title: Aspose.Note Java API
title: Jak přidat alternativní text k obrázku v OneNote pomocí Javy
url: /cs/java/onenote-image-alternative-text/add-alternative-text-to-image/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak přidat alternativní text k obrázku v OneNote pomocí Javy

## Úvod

V tomto tutoriálu se dozvíte **jak přidat alt** text k obrázkům v dokumentech OneNote pomocí Javy a API Aspose.Note. Přidání alternativního textu (alt text) zlepšuje přístupnost pro uživatele čteček obrazovky a zvyšuje celkovou inkluzivitu vašeho obsahu. Na konci tohoto průvodce budete schopni nastavit alt text obrázku v Javě, čímž učiníte své soubory OneNote více v souladu s normami přístupnosti.

## Rychlé odpovědi
- **Jaká knihovna je vyžadována?** Aspose.Note for Java  
- **Na jaké primární klíčové slovo se tento tutoriál zaměřuje?** how to add alt  
- **Potřebuji licenci pro produkční nasazení?** Ano, je vyžadována komerční licence (k dispozici je bezplatná zkušební verze).  
- **Mohu přidat alt text k více obrázkům?** Samozřejmě – stačí opakovat kroky pro každý obrázek.  
- **Jaká verze Javy je podporována?** Java 8 nebo vyšší.

## Co znamená „how to add alt“ v kontextu OneNote?

Přidání alt textu znamená poskytnutí textového popisu obrázku, který může být přečten asistenčními technologiemi. Tento popis pomáhá uživatelům, kteří obrázek nevidí, pochopit jeho účel.

## Proč přidávat alt text k obrázkům v OneNote?

- **Přístupnost:** Splňuje směrnice WCAG a zlepšuje zkušenost uživatelů se zrakovým postižením.  
- **Vyhledatelnost:** Vyhledávače mohou indexovat popis, což zvyšuje objevitelnost vašeho obsahu.  
- **Profesionalita:** Ukazuje závazek k inkluzivnímu designu.

## Předpoklady

Předtím, než se pustíte do tutoriálu, ujistěte se, že máte následující předpoklady:

1. Java Development Kit (JDK) – verze 8 nebo novější.  
2. Knihovna Aspose.Note for Java – stáhněte ji [zde](https://releases.aspose.com/note/java/).  
3. IDE, například IntelliJ IDEA nebo Eclipse.  
4. Základní znalosti programování v Javě.

## Import balíčků

Nejprve importujte potřebné balíčky do svého Java projektu, abyste mohli využívat funkce Aspose.Note.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Image;
import com.aspose.note.Page;
```

Nyní si rozebráme proces přidání **alternativního textu k obrázku** do dokumentu OneNote pomocí Javy a Aspose.Note krok za krokem.

## Jak přidat alt text k obrázkům v OneNote pomocí Javy

### Krok 1: Nastavení adresáře dokumentu

```java
String dataDir = "Your Document Directory";
```

Nahraďte `"Your Document Directory"` cestou ke složce, která obsahuje váš zdrojový obrázek a kam bude uložen výstupní soubor.

### Krok 2: Vytvoření objektu Document

```java
Document document = new Document();
```

Tímto vytvoříte nový, prázdný dokument OneNote.

### Krok 3: Vytvoření objektu Page

```java
Page page = new Page();
```

Stránka bude hostovat obrázek, který se chystáme přidat.

### Krok 4: Přidání obrázku na stránku

```java
Image image = new Image(null, dataDir + "image.jpg");
```

Konstruktor `Image` načte soubor obrázku ze zadané cesty.

### Krok 5: Nastavení titulu alternativního textu

```java
image.setAlternativeTextTitle("ImageAlternativeText Title");
```

Zde **přidáte alt text**, který slouží jako stručný titulek obrázku.

### Krok 6: Nastavení popisu alternativního textu

```java
image.setAlternativeTextDescription("ImageAlternativeText Description");
```

Tento popis poskytuje podrobnější vysvětlení – ideální pro čtečky obrazovky.

### Krok 7: Připojení obrázku k stránce

```java
page.appendChildLast(image);
```

Obrázek (nyní obohacený o alt text) je přidán na stránku.

### Krok 8: Připojení stránky k dokumentu

```java
document.appendChildLast(page);
```

Připojte stránku k dokumentu OneNote.

### Krok 9: Uložení dokumentu

```java
document.save(dataDir + "AlternativeText_out.one");
```

Dokument je uložen s vloženým alternativním textem v obrázku.

## Časté problémy a řešení

- **FileNotFoundException:** Ověřte, že `dataDir` ukazuje na správnou složku a že `image.jpg` existuje.  
- **NullPointerException při obrázku:** Ujistěte se, že cesta k obrázku je platná a soubor není poškozený.  
- **Chyby licence:** Použijte platný licenční soubor Aspose.Note nebo spusťte v režimu zkušební verze pro hodnocení.

## Často kladené otázky

**Q: Mohu přidat alt text k více obrázkům v jednom dokumentu?**  
A: Ano, stačí opakovat kroky 4‑6 pro každý obrázek, který chcete anotovat.

**Q: Jaké formáty obrázků jsou podporovány pro přidání alt textu?**  
A: Aspose.Note podporuje JPEG, PNG, GIF, BMP a několik dalších běžných formátů.

**Q: Je možné po nastavení alt textu jej upravit nebo odstranit?**  
A: Rozhodně. Zavolejte `setAlternativeTextTitle("")` nebo `setAlternativeTextDescription("")` pro vymazání hodnot, nebo poskytněte nové řetězce pro jejich aktualizaci.

**Q: Poskytuje Aspose.Note API i pro jiné jazyky než Java?**  
A: Ano, knihovna je také k dispozici pro .NET, C++ a Python.

**Q: Kde si mohu stáhnout zkušební verzi Aspose.Note?**  
A: Bezplatnou zkušební verzi získáte [zde](https://releases.aspose.com/).

## Závěr

Podle tohoto krok‑za‑krokem průvodce nyní víte **jak přidat alt** text k obrázkům v OneNote pomocí Javy. Implementace `add alternative text image` nejenže činí vaše dokumenty přístupnějšími, ale také zlepšuje jejich vyhledatelnost a celkovou kvalitu. Nebojte se experimentovat s různými tituly a popisy, aby co nejlépe vyjádřily význam každého obrázku.

---

**Poslední aktualizace:** 2025-12-23  
**Testováno s:** Aspose.Note for Java 24.11  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}