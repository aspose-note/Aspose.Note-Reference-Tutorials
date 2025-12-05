---
date: 2025-12-04
description: Naučte se, jak uložit OneNote jako PNG obrázek pomocí Aspose.Note pro
  Javu. Tento průvodce také ukazuje, jak převést OneNote na obrázek a PDF.
language: cs
linktitle: How to Save OneNote as PNG Image with Aspose.Note for Java
second_title: Aspose.Note Java API
title: Jak uložit OneNote jako PNG obrázek s Aspose.Note pro Javu
url: /java/onenote-document-loading/convert-to-image/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak uložit OneNote jako PNG obrázek pomocí Aspose.Note pro Java

## Úvod

V tomto tutoriálu se dozvíte **jak uložit OneNote** dokumenty jako vysoce kvalitní PNG obrázky pomocí knihovny **Aspose.Note pro Java**. Převod OneNote do obrazových formátů (např. PNG) je častý požadavek, když potřebujete vložit poznámky na webové stránky, generovat náhledy nebo vytvářet tisknutelné materiály. Provedeme vás každým krokem – od nastavení prostředí po export souboru – abyste tuto funkci mohli rychle začlenit do svých Java aplikací.

## Rychlé odpovědi
- **Jakou knihovnu potřebuji?** Aspose.Note pro Java.  
- **Mohu převádět i do jiných formátů?** Ano – můžete také převést OneNote do PDF, JPEG, BMP atd.  
- **Potřebuji internetové připojení?** Ne, převod probíhá lokálně.  
- **Jaký obrazový formát se v tomto návodu používá?** PNG (můžete přepnout na JPEG nebo BMP změnou `SaveFormat`).  
- **Jak dlouho převod trvá?** Obvykle méně než sekunda pro standardní OneNote soubor.

## Co v praxi znamená „jak uložit OneNote“?
Uložení OneNote jako obrázku znamená vykreslení každé stránky souboru `.one` do rastrového formátu (PNG, JPEG, …). To je užitečné pro sdílení poznámek s uživateli, kteří nemají OneNote nainstalovaný, nebo pro tvorbu statických vizuálních materiálů.

## Proč použít Aspose.Note pro Java k převodu OneNote na PNG?
- **Žádné externí závislosti** – funguje čistě v Javě.  
- **Plná věrnost** – zachovává barvy, písma i rozvržení.  
- **Flexibilní výstup** – podporuje PNG, JPEG, BMP, PDF, HTML a další.  
- **Enterprise‑ready** – běží na jakékoli platformě, která podporuje Java 8+.

## Předpoklady

Než začneme, ujistěte se, že máte:

1. **Java Development Kit (JDK)** – verze 8 nebo vyšší.  
2. **Aspose.Note pro Java** knihovnu – stáhněte nejnovější JAR z oficiální stránky: [Aspose.Note for Java download](https://releases.aspose.com/note/java/).  
3. Existující **OneNote (.one)** soubor, který chcete převést (např. `Sample1.one`).

## Import balíčků

Nejprve importujte třídy, které budeme potřebovat. Tento kódový blok zůstává beze změny:

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.SaveFormat;
```

## Průvodce krok za krokem

### Krok 1: Nastavte adresář dokumentu  
Definujte složku, která obsahuje váš OneNote soubor. Nahraďte zástupný text skutečnou cestou na vašem počítači.

```java
String dataDir = "Your Document Directory";
```

### Krok 2: Načtěte OneNote dokument  
Vytvořte objekt `Document` načtením souboru `.one`.

```java
Document oneFile = new Document(dataDir + "Sample1.one");
```

> **Tip:** Pokud později potřebujete **převést OneNote do PDF**, můžete znovu použít stejnou instanci `Document` s jinými `SaveOptions`.

### Krok 3: Inicializujte ImageSaveOptions  
Řekněte Aspose.Note, v jakém obrazovém formátu chcete výstup. Zde volíme PNG, ale můžete také použít `SaveFormat.Jpeg` nebo `SaveFormat.Bmp`.

```java
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);
```

> Tento řádek také splňuje sekundární klíčová slova **convert onenote to png** a **save onenote as png**.

### Krok 4: Uložte dokument jako obrázek  
Exportujte stránku(y) OneNote do PNG souboru.

```java
oneFile.save(dataDir + "ConvertToImage_out.png", options);
```

> Metoda `save` automaticky zpracuje více‑stránkové dokumenty vytvořením samostatných obrazových souborů pro každou stránku.

### Krok 5: Vytiskněte potvrzení  
Dejte uživateli vědět, kam byl výstup zapsán.

```java
System.out.println("File saved: " + dataDir + "ConvertToImage_out.png");
```

## Časté problémy a řešení

| Problém | Důvod | Řešení |
|---------|-------|--------|
| **FileNotFoundException** | Nesprávná cesta `dataDir` | Ověřte, že cesta ke složce končí lomítkem (`/` nebo `\\`) a název souboru je správný. |
| **Unsupported format** | Pokus o uložení do staršího obrazového formátu, který knihovna nepodporuje | Aktualizujte Aspose.Note na nejnovější verzi nebo zvolte podporovaný `SaveFormat`. |
| **Large OneNote files cause OutOfMemoryError** | Nedostatečný heap paměť | Zvyšte JVM heap (`-Xmx2g`) nebo zpracovávejte stránky jednotlivě pomocí smyčky `Document.getPages()`. |

## Často kladené otázky

**Q: Mohu převádět více OneNote souborů najednou?**  
A: Ano. Projděte kolekci názvů souborů, načtěte každý pomocí `new Document(...)` a opakujte kroky pro uložení.

**Q: Podporuje Aspose.Note převod OneNote do PDF?**  
A: Rozhodně. Použijte `PdfSaveOptions` místo `ImageSaveOptions` pro **convert onenote to pdf**.

**Q: Jak mohu změnit rozlišení PNG výstupu?**  
A: Před voláním `save` upravte `options.setResolutionX(int)` a `options.setResolutionY(int)`.

**Q: Existuje způsob, jak převést OneNote do jiných obrazových formátů, jako je JPEG?**  
A: Ano, nahraďte `SaveFormat.Png` za `SaveFormat.Jpeg` nebo `SaveFormat.Bmp` v konstruktoru `ImageSaveOptions`.

**Q: Potřebuji pro převod internetové připojení?**  
A: Ne. Aspose.Note provádí veškeré zpracování lokálně; nevolá žádné externí služby.

## Závěr

Po absolvování těchto jednoduchých kroků nyní víte **jak uložit OneNote** soubory jako PNG obrázky pomocí **Aspose.Note pro Java**. Tato schopnost otevírá mnoho scénářů – vkládání poznámek na webové stránky, generování tisknutelných materiálů nebo jednoduché archivování vašich sešitů jako statických obrázků. Nebojte se experimentovat s dalšími výstupními formáty, jako je PDF nebo JPEG, a začlenit kód do větších automatizačních pipeline.

---

**Poslední aktualizace:** 2025-12-04  
**Testováno s:** Aspose.Note pro Java 24.12  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}