---
date: 2026-02-05
description: Naučte se, jak exportovat stránky OneNote a uložit OneNote jako obrázek.
  Tento průvodce ukazuje, jak převést .one na png, nastavit index stránky a exportovat
  obrázek stránky OneNote pomocí Aspose.Note pro Javu.
linktitle: Export OneNote Page to PNG Image in Java
second_title: Aspose.Note Java API
title: Jak exportovat stránku OneNote do PNG obrázku v Javě pomocí Aspose.Note
url: /cs/java/onenote-document-loading/convert-page-to-png-image/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Exportovat stránku OneNote do PNG obrázku v Javě pomocí Aspose.Note

## Úvod

V tomto tutoriálu objevíte **jak exportovat stránku OneNote** do PNG obrázku pomocí knihovny Aspose.Note pro Java. **Jak exportovat stránky OneNote** je častá potřeba, když chcete sdílet poznámky mimo ekosystém OneNote, vložit je do reportů nebo zpracovat pomocí nástrojů pro zpracování obrázků. Provedeme vás vším, co potřebujete — od přípravy prostředí po nastavení indexu stránky, konverzi stránky a uložení výsledku jako vysoce kvalitního PNG souboru. Na konci budete schopni **uložit OneNote jako obrázek** v jakékoli Java aplikaci.

## Rychlé odpovědi
- **Jaká knihovna je potřeba?** Aspose.Note for Java.  
- **Mohu exportovat jedinou stránku?** Ano — použijte `setPageIndex` k výběru konkrétní stránky.  
- **Podporované formáty obrázků?** PNG, JPEG, GIF, BMP, TIFF (zde ukázáno PNG).  
- **Potřebuji licenci?** K dispozici je bezplatná zkušební verze; licence je vyžadována pro produkční použití.  
- **Jak dlouho trvá implementace?** Obvykle méně než 10 minut pro základní konverzi.  
- **Jak převést .one na png?** Načtěte soubor `.one` pomocí `Document`, nastavte index stránky a uložte pomocí `ImageSaveOptions`.  

## Co je „export OneNote stránky“?
Exportování stránky OneNote znamená převod konkrétní stránky uvnitř dokumentu `.one` na samostatný soubor obrázku (v tomto případě PNG). To je užitečné, když potřebujete **exportovat obrázek stránky OneNote** pro sdílení, vložení nebo další analýzu založenou na obrázcích.

## Proč použít Aspose.Note pro Java k převodu OneNote na PNG?
- **Žádná závislost na Microsoft Office** — funguje na jakékoli platformě, která spouští Javu.  
- **Detailní kontrola** — můžete vybrat libovolnou stránku pomocí `setPageIndex`.  
- **Výstup ve vysoké kvalitě** — PNG zachovává vektorovou grafiku a čitelnost textu.  
- **Připraveno pro dávkové zpracování** — snadné procházení stránek pro hromadnou konverzi, což usnadňuje **převod OneNote na png** pro mnoho stránek najednou.  

## Požadavky

Před začátkem se ujistěte, že máte:

1. **Java Development Kit (JDK)** — verze 8 nebo vyšší.  
2. **Aspose.Note for Java** — stáhněte nejnovější JAR z [webu Aspose](https://releases.aspose.com/note/java/).  
3. **Dokument OneNote** (`.one`), který obsahuje stránku, kterou chcete exportovat.

## Import balíčků

Nejprve importujte potřebné třídy Java:

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.LoadOptions;
import com.aspose.note.SaveFormat;
```

Tyto importy vám poskytují přístup k jádru Aspose.Note API, včetně načítání dokumentů a konfigurace možností ukládání obrázků.

## Postupný průvodce

### Krok 1: Načíst dokument OneNote

```java
// Load the document into Aspose.Note.
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Sample1.one", new LoadOptions());
```

Používáme třídu `Document` k načtení souboru OneNote z disku. Objekt `LoadOptions` vám umožní přizpůsobit chování načítání podle potřeby. Tento krok je základem pro **převod .one na png**.

### Krok 2: Inicializovat ImageSaveOptions

```java
// Initialize ImageSaveOptions object
ImageSaveOptions opts = new ImageSaveOptions(SaveFormat.Png);
```

`ImageSaveOptions` říká Aspose.Note, že chceme výstup ve formátu **PNG**. Můžete přepnout na JPEG, BMP atd. změnou `SaveFormat`. Tento objekt vám také umožní řídit DPI, barevnou hloubku a další nastavení specifická pro obrázek.

### Krok 3: Nastavit index stránky (Jak převést stránku OneNote)

```java
// set page index
opts.setPageIndex(0);
```

Metoda `setPageIndex` vybírá, kterou stránku exportovat. Číslování stránek začíná na **0**, takže `0` odkazuje na první stránku. Upravením této hodnoty **exportujete jinou stránku** nebo můžete procházet stránky, když potřebujete **uložit OneNote jako obrázek** pro každou z nich.

### Krok 4: Uložit dokument jako PNG (Uložit OneNote jako PNG)

```java
// Save the document as PNG.
oneFile.save(dataDir + "ConvertSpecificPageToPngImage_out.png", opts);
```

Voláním `save` zapíšete vybranou stránku do souboru PNG na disku. Název souboru `ConvertSpecificPageToPngImage_out.png` je jen příklad — můžete jej pojmenovat libovolně. Tento poslední krok **exportuje obrázek stránky OneNote** připravený k použití v reportech, webových stránkách nebo dalším zpracování.

## Časté problémy a tipy

- **Nesprávný index stránky** — Pamatujte, že indexování začíná na 0. Pokud získáte prázdný obrázek, ověřte hodnotu indexu.  
- **Chybějící Aspose.Note JAR** — Ujistěte se, že je JAR ve vaší classpath; jinak se zobrazí `ClassNotFoundException`.  
- **Velké stránky** — Pro velmi velké stránky zvažte zvýšení velikosti haldy JVM (`-Xmx`), aby nedošlo k `OutOfMemoryError`.  
- **Řízení rozlišení** — Použijte `opts.setResolution(300)` (nebo jakékoliv DPI, které potřebujete) před voláním `save` pro zlepšení ostrosti obrázku.  

## Často kladené otázky

### Q1: Mohu pomocí Aspose.Note pro Java převést více stránek na PNG obrázky najednou?
A1: Ano, můžete procházet stránky dokumentu, aktualizovat `opts.setPageIndex(i)` a volat `save` pro každou iteraci.

### Q2: Podporuje Aspose.Note pro Java další formáty obrázků kromě PNG?
A2: Rozhodně. V `ImageSaveOptions` můžete nastavit `SaveFormat.Jpeg`, `SaveFormat.Gif`, `SaveFormat.Bmp` nebo `SaveFormat.Tiff`.

### Q3: Je k dispozici bezplatná zkušební verze Aspose.Note pro Java?
A3: Ano, můžete si stáhnout bezplatnou zkušební verzi z [webu](https://releases.aspose.com/).

### Q4: Můžu získat technickou podporu, pokud narazím na problémy s Aspose.Note pro Java?
A4: Rozhodně, můžete požádat o podporu na fóru komunity Aspose [zde](https://forum.aspose.com/c/note/28).

### Q5: Kde si mohu zakoupit licenci pro Aspose.Note pro Java?
A5: Licenci si můžete zakoupit na [stránce nákupu](https://purchase.aspose.com/buy).

### Q6: Jak exportovat stránku, která obsahuje vložené obrázky?
A6: Vložené obrázky jsou automaticky vykresleny v PNG výstupu; není potřeba žádný další kód.

### Q7: Můžu nastavit DPI nebo rozlišení obrázku?
A7: Ano, použijte `opts.setResolution(int dpi)` před voláním `save` pro kontrolu kvality výstupu.

---

**Poslední aktualizace:** 2026-02-05  
**Testováno s:** Aspose.Note for Java 24.11 (latest)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}