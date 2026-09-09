---
date: 2026-01-12
description: Naučte se, jak upravit historii stránky OneNote, změnit název stránky
  OneNote a smazat historii stránky OneNote pomocí Aspose.Note pro Javu.
linktitle: Modify Page History in OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: Jak upravit historii stránky OneNote pomocí Aspose.Note
url: /cs/java/onenote-page-manipulation/modify-page-history/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak upravit historii stránek OneNote pomocí Aspose.Note

V tomto tutoriálu objevíte **jak upravit onenote** dokumenty programově pomocí práce s historií stránek. Provedeme vás načtením souboru OneNote, úpravou jeho položek historie, změnou názvu stránky a nakonec uložením aktualizovaného sešitu — vše pomocí API Aspose.Note pro Java. Ať už potřebujete vyčistit staré revize nebo přejmenovat stránky, níže uvedené kroky vám poskytnou kompletní, připravené řešení pro produkci.

## Rychlé odpovědi
- **Co znamená „page history“ v OneNote?**  
  Jedná se o sbírku předchozích verzí stránky uložených v souboru OneNote.
- **Mohu smazat konkrétní položku historie?**  
  Ano, použijte metody `removeRange` nebo `removeItem` na objektu `PageHistory`.
- **Je změna názvu stránky součástí manipulace s historií?**  
  Rozhodně — každá položka historie má svůj vlastní název, který můžete upravit.
- **Potřebuji licenci pro spuštění tohoto kódu?**  
  Dočasná zkušební licence funguje pro testování; pro produkci je vyžadována plná licence.
- **Která verze Javy je podporována?**  
  Aspose.Note pro Java podporuje JDK 8 a novější.

## Požadavky

Než začnete, ujistěte se, že máte:

1. **Java Development Kit (JDK)** – JDK 8 nebo novější nainstalovaný na vašem počítači.  
2. **Aspose.Note for Java library** – stáhněte ji ze [stránky ke stažení](https://releases.aspose.com/note/java/).  
3. **Ukázkový dokument OneNote** – např. `Sample1.one`, který můžete bezpečně upravit.

## Import balíčků

Nejprve importujte třídy, které budete potřebovat. Níže uvedený blok kódu musí zůstat přesně tak, jak je.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.PageHistory;
```

## Průvodce krok za krokem

### Krok 1: Načtení dokumentu OneNote

```java
String dataDir = "Your Document Directory";
Document document = new Document(dataDir + "Sample1.one");
```

### Krok 2: Získání první stránky a její historie

```java
Page page = document.getFirstChild();
PageHistory pageHistory = document.getPageHistory(page);
```

### Krok 3: Smazání rozsahu položek historie

Pokud potřebujete **smazat položky historie stránky onenote**, zavolejte `removeRange`. Příklad odstraní první položku.

```java
pageHistory.removeRange(0, 1);
```

### Krok 4: Nahrazení položky historie

Můžete nahradit existující položku historie novým objektem `Page`.

```java
pageHistory.set_Item(0, new Page());
```

### Krok 5: Změna názvu stránky v historii

Změna názvu je častý požadavek, když chcete **změnit název stránky onenote** pro konkrétní revizi.

```java
pageHistory.get_Item(1).getTitle().getTitleText().clear().append("New Title");
```

### Krok 6: Přidání nové položky historie

Přidejte zcela novou stránku do kolekce historie.

```java
pageHistory.addItem(new Page());
```

### Krok 7: Vložení stránky na konkrétní pozici

Vložte stránku na index 1, čímž posunete existující položky dopředu.

```java
pageHistory.insertItem(1, new Page());
```

### Krok 8: Uložení upraveného sešitu

```java
document.save(dataDir + "ModifyPageHistory_out.one");
```

## Proč upravovat historii stránek OneNote?

- **Kontrola verzí:** Uchovávejte pouze relevantní revize a odstraňujte rušivé koncepty.  
- **Konzistence:** Slaďte názvy stránek napříč všemi historickými verzemi pro lepší navigaci.  
- **Výkon:** Menší kolekce historie snižují velikost souboru a zlepšují rychlost načítání.

## Časté úskalí a tipy

- **Index mimo rozsah:** Vždy ověřte velikost kolekce před voláním `removeRange` nebo `insertItem`.  
- **Null názvy:** Některé historické stránky mohou postrádat název; chraňte se před `null` při volání `getTitle()`.  
- **Umístění uložení:** Ujistěte se, že výstupní cesta (`ModifyPageHistory_out.one`) je zapisovatelná; jinak bude vyhozena `IOException`.

## Často kladené otázky

**Q: Mohu použít Aspose.Note pro Java s jinými Java frameworky?**  
A: Ano, Aspose.Note pro Java je kompatibilní s různými Java frameworky jako Spring, Hibernate atd.

**Q: Je Aspose.Note pro Java kompatibilní s různými verzemi souborů OneNote?**  
A: Aspose.Note pro Java podporuje práci jak se starými, tak i novými verzemi souborů OneNote.

**Q: Vyžaduje Aspose.Note pro Java nějaké další závislosti?**  
A: Ne, Aspose.Note pro Java je samostatná knihovna a nevyžaduje žádné další závislosti.

**Q: Mohu provádět hromadné úpravy na více souborech OneNote najednou?**  
A: Ano, Aspose.Note pro Java poskytuje API pro efektivní hromadné úpravy.

**Q: Existuje komunitní fórum pro Aspose.Note pro Java, kde se mohu zeptat na pomoc?**  
A: Ano, můžete navštívit [forum Aspose.Note](https://forum.aspose.com/c/note/28) pro jakoukoli pomoc nebo dotazy související s knihovnou.

---

**Poslední aktualizace:** 2026-01-12  
**Testováno s:** Aspose.Note pro Java 24.11 (nejnovější v době psaní)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}