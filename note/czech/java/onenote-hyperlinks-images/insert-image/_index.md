---
date: 2026-03-19
description: Naučte se, jak přidat obrázek do OneNote pomocí Javy s Aspose.Note pro
  Javu, včetně toho, jak nastavit rozměry obrázku v Javě a uložit OneNote jako PDF.
linktitle: Insert an Image in OneNote Document with Java
second_title: Aspose.Note Java API
title: Přidat obrázek do OneNote pomocí Javy
url: /cs/java/onenote-hyperlinks-images/insert-image/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Vložení obrázku do dokumentu OneNote pomocí Javy

## Úvod

V tomto tutoriálu se naučíte **jak přidat obrázek do OneNote** programově pomocí Javy a knihovny Aspose.Note pro Java. Vkládání obrázků na stránky OneNote je užitečné, když potřebujete generovat zápisy ze schůzek, automatizované zprávy nebo dokumentaci, která kombinuje text s vizuálními daty. Na konci průvodce budete schopni načíst existující soubor OneNote, vložit obrázek, případně upravit jeho velikost a umístění a dokonce **uložit OneNote jako PDF** – vše bez otevření uživatelského rozhraní OneNote.

## Rychlé odpovědi
- **Jaký je nejjednodušší způsob, jak přidat obrázek do OneNote pomocí Javy?**  
  Použijte třídu `Image` z Aspose.Note pro Java a připojte ji k stránce.
- **Potřebuji licenci pro produkční použití?**  
  Ano, pro produkční nasazení je vyžadována komerční licence.
- **Mohu nastavit vlastní rozměry obrázku?**  
  Samozřejmě – zavolejte `setWidth()` a `setHeight()` na objektu `Image`.
- **Je možné po přidání obrázku uložit soubor OneNote jako PDF?**  
  Ano, zavolejte `save(..., SaveFormat.Pdf)` pro **uložení OneNote jako PDF**.
- **Jaká verze Javy je podporována?**  
  Aspose.Note pro Java funguje s JDK 8 a novějšími.

## Proč přidávat obrázek do OneNote?

Vizuální prvky usnadňují pochopení poznámek a činí je poutavějšími. Obrázky mohou ilustrovat diagramy, snímky obrazovky nebo datové grafy, které by jinak vyžadovaly dlouhé textové popisy. Automatizace tohoto kroku šetří čas, zejména při generování velkých objemů poznámek z datových zdrojů.

## Předpoklady

Než začneme, ujistěte se, že máte připraveno následující:

### 1. Java Development Kit (JDK)
Nainstalujte JDK 8 nebo novější. Můžete jej stáhnout z webu Oracle nebo použít distribuci OpenJDK.

### 2. Knihovna Aspose.Note pro Java
Stáhněte si nejnovější knihovnu Aspose.Note pro Java a přidejte ji do classpath vašeho projektu. Podrobné pokyny k nastavení najdete v oficiální [dokumentaci](https://reference.aspose.com/note/java/).

## Import balíčků

Začněte importováním potřebných tříd. Tyto importy vám umožní přístup k základní funkčnosti Aspose.Note i k běžným utilitám Javy.

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.HorizontalAlignment;
import com.aspose.note.Image;
import com.aspose.note.LoadOptions;
import com.aspose.note.Page;
import com.aspose.note.SaveFormat;
```

## Průvodce krok za krokem

Níže je stručný, číslovaný návod. Každý krok obsahuje krátké vysvětlení a přesný kód, který je potřeba zkopírovat.

### Krok 1: Načtení dokumentu OneNote

Vytvoříme instanci `LoadOptions` (užitečnou pro budoucí úpravy) a otevřeme existující soubor s příponou `.one`.

```java
LoadOptions options = new LoadOptions();
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Sample1.one", options);
```

### Krok 2: Získání cílové stránky

Pro zjednodušení pracujeme s první stránkou v dokumentu, ale můžete přejít na libovolnou stránku, kterou potřebujete.

```java
Page page = oneFile.getFirstChild();
```

### Krok 3: Načtení obrázku, který chcete vložit

Vytvořte objekt `Image` tak, že předáte odkaz na dokument a cestu k souboru obrázku.

```java
Image image = new Image(oneFile, dataDir + "Input.jpg");
```

### Krok 4: Nastavení rozměrů obrázku v Javě (volitelné)

Pokud potřebujete, aby obrázek zapadl do konkrétní oblasti, upravte jeho šířku, výšku a posuny. Zde se uplatní sekundární klíčové slovo **set image dimensions java**.

```java
image.setWidth(100);
image.setHeight(100);
image.setVerticalOffset(400);
image.setHorizontalOffset(100);
image.setAlignment(HorizontalAlignment.Right);
```

### Krok 5: Připojení obrázku k stránce

Metoda `appendChildLast` přidá obrázek jako poslední prvek na vybrané stránce.

```java
page.appendChildLast(image);
```

### Krok 6: Uložení dokumentu – můžete také uložit OneNote jako PDF

Nakonec změny uložíte. Příklad ukazuje, jak soubor uložit jako PDF, čímž splňuje sekundární klíčové slovo **save onenote as pdf**.

```java
try {
    oneFile.save(dataDir + "InsertanImage_out.pdf", SaveFormat.Pdf);
} catch (IOException e) {
    e.printStackTrace();
}
```

## Časté problémy a řešení

| Problém | Pravděpodobná příčina | Řešení |
|---------|-----------------------|--------|
| `FileNotFoundException` při načítání obrázku | Nesprávná cesta k obrázku | Ověřte, že `dataDir` a název souboru obrázku jsou správné. |
| Obrázek je deformovaný | Šířka/výška nastavená nesprávně | Použijte původní rozměry obrázku nebo vypočítejte správný poměr stran před voláním `setWidth`/`setHeight`. |
| Výstupní PDF je prázdný | Chybí licence pro Aspose.Note | Aplikujte platnou licenci před voláním `save`. |

## Často kladené otázky

### Q1: Mohu pomocí této metody vložit do jednoho dokumentu OneNote více obrázků?

**A:** Ano. Stačí opakovat kroky 3‑5 pro každý obrázek, který chcete přidat, a to buď na stejnou, nebo na jinou stránku.

### Q2: Je Aspose.Note pro Java kompatibilní se všemi verzemi OneNote?

**A:** Aspose.Note pro Java podporuje soubory OneNote vytvořené v Microsoft OneNote 2010 a novějších verzích.

### Q3: Mohu do dokumentu OneNote vkládat obrázky různých formátů, například PNG nebo GIF?

**A:** Rozhodně. Knihovna akceptuje PNG, JPEG, GIF, BMP a několik dalších běžných formátů.

### Q4: Existuje zkušební verze Aspose.Note pro Java pro testovací účely?

**A:** Ano, můžete si stáhnout bezplatnou zkušební verzi z webu Aspose a vyzkoušet API před zakoupením.

### Q5: Jak získám technickou podporu pro Aspose.Note pro Java?

**A:** Pomoc získáte na [fóru](https://forum.aspose.com/c/note/28) věnovaném produktům Aspose.Note.

## Závěr

Nyní máte kompletní, připravený příklad, který ukazuje **jak přidat obrázek do OneNote** pomocí Javy, přizpůsobit jeho vzhled a případně **uložit OneNote jako PDF**. Klidně upravte kód podle svých potřeb – ať už budujete reportingový engine, automatizovaný systém dokumentace nebo vlastní aplikaci pro psaní poznámek.

---

**Poslední aktualizace:** 2026-03-19  
**Testováno s:** Aspose.Note pro Java 24.10  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}