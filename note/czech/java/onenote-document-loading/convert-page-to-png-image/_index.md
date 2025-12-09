---
date: 2025-11-29
description: Naučte se, jak exportovat stránku OneNote do PNG pomocí Aspose.Note pro
  Javu. Postupujte podle krok‑za‑krokem návodu, jak nastavit index stránky, převést
  stránku a uložit obrázek.
linktitle: Export OneNote Page to PNG Image in Java
second_title: Aspose.Note Java API
title: Exportovat stránku OneNote do PNG obrázku v Javě pomocí Aspose.Note
url: /cs/java/onenote-document-loading/convert-page-to-png-image/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Exportovat stránku OneNote do PNG obrázku v Javě pomocí Aspose.Note

## Úvod

V tomto tutoriálu se dozvíte **jak exportovat stránku OneNote** do PNG obrázku pomocí knihovny Aspose.Note pro Javu. Provedeme vás vším, co potřebujete—od přípravy prostředí po nastavení indexu stránky a nakonec uložení stránky jako vysoce kvalitního PNG souboru. Na konci budete schopni přidat tuto funkci do jakékoli Java aplikace pracující s dokumenty OneNote.

## Rychlé odpovědi
- **Jaká knihovna je potřeba?** Aspose.Note for Java.  
- **Mohu exportovat jedinou stránku?** Ano—použijte `setPageIndex` k cílení konkrétní stránky.  
- **Podporované formáty obrázků?** PNG, JPEG, GIF, BMP, TIFF (zde je ukázáno PNG).  
- **Potřebuji licenci?** K dispozici je bezplatná zkušební verze; licence je vyžadována pro produkční použití.  
- **Jak dlouho trvá implementace?** Obvykle méně než 10 minut pro základní konverzi.

## Co znamená „exportovat stránku OneNote“?
Exportování stránky OneNote znamená převod konkrétní stránky uvnitř dokumentu `.one` na samostatný soubor obrázku (v tomto případě PNG). To je užitečné, když potřebujete sdílet, vložit nebo zpracovat obsah OneNote mimo prostředí OneNote.

## Proč použít Aspose.Note pro Javu k převodu OneNote na PNG?
- **Žádná závislost na Microsoft Office** – funguje na jakékoli platformě, která spouští Javu.  
- **Detailní kontrola** – můžete vybrat libovolnou stránku pomocí `setPageIndex`.  
- **Výstup ve vysoké kvalitě** – PNG zachovává vektorovou grafiku a čitelnost textu.  
- **Připraveno pro dávkové zpracování** – snadné procházení stránek pro hromadnou konverzi.

## Požadavky

Před začátkem se ujistěte, že máte:

1. **Java Development Kit (JDK)** – verze 8 nebo vyšší.  
2. **Aspose.Note pro Javu** – stáhněte nejnovější JAR z [webu Aspose](https://releases.aspose.com/note/java/).  
3. **Dokument OneNote** (`.one`), který obsahuje stránku, kterou chcete exportovat.

## Import balíčků

Nejprve importujte potřebné třídy Javy:

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.LoadOptions;
import com.aspose.note.SaveFormat;
```

## Postup krok za krokem

### Krok 1: Načíst dokument OneNote

```java
// Load the document into Aspose.Note.
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Sample1.one", new LoadOptions());
```

Používáme třídu `Document` k načtení souboru OneNote z disku. Objekt `LoadOptions` vám umožní přizpůsobit chování načítání, pokud je to potřeba.

### Krok 2: Inicializovat ImageSaveOptions

```java
// Initialize ImageSaveOptions object
ImageSaveOptions opts = new ImageSaveOptions(SaveFormat.Png);
```

`ImageSaveOptions` říká Aspose.Note, že chceme výstup ve formátu **PNG**. Můžete přepnout na JPEG, BMP atd. změnou `SaveFormat`.

### Krok 3: Nastavit index stránky (Jak převést stránku OneNote)

```java
// set page index
opts.setPageIndex(0);
```

Metoda `setPageIndex` vybírá, kterou stránku exportovat. Číslování stránek začíná na **0**, takže `0` odkazuje na první stránku. Upravením této hodnoty můžete exportovat jinou stránku.

### Krok 4: Uložit dokument jako PNG (Uložit OneNote jako PNG)

```java
// Save the document as PNG.
oneFile.save(dataDir + "ConvertSpecificPageToPngImage_out.png", opts);
```

Volání `save` zapíše vybranou stránku do PNG souboru na disku. Název souboru `ConvertSpecificPageToPngImage_out.png` je jen příklad—můžete jej pojmenovat libovolně.

## Časté problémy a tipy

- **Nesprávný index stránky** – Pamatujte, že indexování začíná na 0. Pokud získáte prázdný obrázek, ověřte hodnotu indexu.  
- **Chybějící Aspose.Note JAR** – Ujistěte se, že JAR je ve vaší classpath; jinak se zobrazí `ClassNotFoundException`.  
- **Velké stránky** – Pro velmi velké stránky zvažte zvýšení velikosti haldy JVM (`-Xmx`), aby se předešlo `OutOfMemoryError`.

## Často kladené otázky

### Q1: Můžu převést více stránek na PNG obrázky najednou pomocí Aspose.Note pro Javu?
A1: Ano, můžete procházet stránky dokumentu, aktualizovat `opts.setPageIndex(i)` a volat `save` pro každou iteraci.

### Q2: Podporuje Aspose.Note pro Javu jiné formáty obrázků kromě PNG?
A2: Rozhodně. V `ImageSaveOptions` můžete nastavit `SaveFormat.Jpeg`, `SaveFormat.Gif`, `SaveFormat.Bmp` nebo `SaveFormat.Tiff`.

### Q3: Je k dispozici bezplatná zkušební verze Aspose.Note pro Javu?
A3: Ano, můžete si stáhnout bezplatnou zkušební verzi z [webu](https://releases.aspose.com/).

### Q4: Mohu získat technickou podporu, pokud narazím na problémy s Aspose.Note pro Javu?
A4: Rozhodně, můžete získat podporu na fóru komunity Aspose [zde](https://forum.aspose.com/c/note/28).

### Q5: Kde mohu zakoupit licenci pro Aspose.Note pro Javu?
A5: Licenci můžete zakoupit na [stránce nákupu](https://purchase.aspose.com/buy).

### Q6: Jak exportovat stránku, která obsahuje vložené obrázky?
A6: Vložené obrázky jsou automaticky vykresleny v PNG výstupu; není potřeba žádný další kód.

### Q7: Mohu nastavit DPI nebo rozlišení obrázku?
A7: Ano, použijte `opts.setResolution(int dpi)` před voláním `save` pro kontrolu kvality výstupu.

---

**Last Updated:** 2025-11-29  
**Tested With:** Aspose.Note for Java 24.11 (latest)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}