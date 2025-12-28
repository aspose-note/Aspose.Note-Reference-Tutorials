---
date: 2025-12-28
description: Naučte se, jak převést OneNote na obrázek a uložit OneNote jako PNG pomocí
  Aspose.Note pro Javu. Snadno integrujte tuto funkci do svých Java aplikací.
linktitle: Convert Notebook to Image in OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: Převod OneNote na obrázek – převod OneNote na obrázek pomocí Aspose.Note
url: /cs/java/onenote-notebook-operations/convert-notebook-to-image/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Převod OneNote na obrázek – převod onenote na obrázek pomocí Aspose.Note

## Úvod

V tomto tutoriálu se naučíte **jak převést onenote na obrázek** pomocí knihovny Aspose.Note pro Java. Převod poznámkového bloku OneNote na obrázek (PNG, JPEG atd.) je užitečný, když potřebujete sdílet poznámky s lidmi, kteří nemají OneNote, vložit je do zpráv nebo je zařadit do prezentací. Provedeme celý proces krok za krokem, takže tuto funkci můžete přidat do svých Java aplikací během několika minut.

## Rychlé odpovědi
- **Co znamená „convert onenote to image“?** Znamená to vykreslení stránky poznámkového bloku OneNote jako rastrového souboru obrázku, např. PNG.  
- **Který formát je doporučený pro nejlepší kvalitu?** PNG je bezztrátový a zachovává ostrý text i grafiku.  
- **Potřebuji licenci pro použití Aspose.Note?** Bezplatná zkušební verze funguje pro vývoj; pro produkci je vyžadována komerční licence.  
- **Mohu hromadně převádět více poznámkových bloků?** Ano – stačí projít soubory ve smyčce a znovu použít stejný konverzní kód.  
- **Jaká verze Javy je vyžadována?** Java 8 nebo novější (v tutoriálu je použito JDK 15 jako příklad).

## Co je „convert onenote to image“?
Konverze poznámkového bloku OneNote na obrázek extrahuje vizuální reprezentaci každé stránky a zapíše ji do standardního souboru obrázku. Tento proces zachovává rozvržení, písma a vložené objekty, takže je obsah zobrazitelný na jakémkoli zařízení bez potřeby OneNote.

## Proč použít Aspose.Note pro tuto konverzi?
- **Žádná závislost na Microsoft Office** – funguje na jakémkoli OS, který podporuje Javu.  
- **Vysoká věrnost** – vykreslený obrázek odpovídá původní stránce OneNote pixel po pixelu.  
- **Více výstupních formátů** – PNG, JPEG, BMP, GIF, TIFF.  
- **Jednoduché API** – několik řádků kódu zvládne načítání, konfiguraci a ukládání.

## Předpoklady

Než začneme, ujistěte se, že máte následující:

1. **Java Development Kit (JDK)** – Nainstalujte nejnovější JDK z [webu](https://www.oracle.com/java/technologies/javase-jdk15-downloads.html).  
2. **Aspose.Note for Java knihovna** – Stáhněte JAR z [webu Aspose](https://releases.aspose.com/note/java/) a přidejte jej do classpath vašeho projektu.

## Import balíčků

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.SaveFormat;
```

Nyní rozdělíme proces konverze do přehledných číslovaných kroků.

## Krok 1: Načtení dokumentu poznámkového bloku

```java
// Specify the directory where your notebook file is located
String dataDir = "Your Document Directory";

// Load the document into Aspose.Note
Document oneFile = new Document(dataDir + "Sample1.one");
```

V tomto kroku nasměrujeme API na složku obsahující soubor `.one` a načteme jej do objektu `Document`.

## Krok 2: Inicializace ImageSaveOptions

```java
// Initialize PdfSaveOptions object
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);
```

Zde vytvoříme instanci `ImageSaveOptions` a řekneme Aspose.Note, že chceme výstup ve formátu **PNG** – to splňuje sekundární klíčové slovo *save onenote as png*.

## Krok 3: Uložení dokumentu jako obrázek

```java
// Save the document as PNG
oneFile.save(dataDir + "ConvertToImage_out.png", options);
```

Volání `save()` zapíše stránku poznámkového bloku do `ConvertToImage_out.png`. Můžete změnit `SaveFormat.Png` na `SaveFormat.Jpeg`, pokud chcete výstup kompatibilní s **convert onenote to png** ve formátu JPEG.

## Krok 4: Vytištění potvrzení

```java
System.out.println("File saved: " + dataDir + "ConvertToImage_out.png");
```

Jednoduchá zpráva v konzoli potvrzuje, že operace **convert onenote to image** byla úspěšná.

## Časté problémy a tipy

- **Soubor nenalezen** – Zkontrolujte cestu `dataDir` a ujistěte se, že `Sample1.one` existuje.  
- **Chyby nedostatku paměti** – Pro velmi velké poznámkové bloky zvyšte haldu JVM (`-Xmx`) nebo zpracovávejte stránky jednotlivě.  
- **Kvalita obrázku** – Můžete upravit DPI pomocí `options.setResolution(300);` pro PNG s vyšším rozlišením.

## Často kladené otázky

**Q: Mohu převádět poznámkové bloky do jiných formátů obrázků kromě PNG?**  
A: Ano. Knihovna Aspose.Note podporuje JPEG, BMP, GIF, TIFF a další. Stačí změnit výčtový typ `SaveFormat` v `ImageSaveOptions`.

**Q: Je Aspose.Note kompatibilní se všemi verzemi OneNote?**  
A: Aspose.Note poskytuje komplexní podporu různých formátů souborů OneNote, což zajišťuje kompatibilitu napříč různými verzemi OneNote.

**Q: Mohu během konverze přizpůsobit nastavení výstupu obrázku?**  
A: Rozhodně. Pomocí objektu `ImageSaveOptions` můžete řídit rozlišení, kvalitu, barevnou hloubku a další parametry.

**Q: Podporuje Aspose.Note hromadnou konverzi více poznámkových bloků?**  
A: Ano. Projděte kolekci souborů `.one` a v cyklu aplikujte stejné kroky konverze.

**Q: Kde najdu další zdroje a podporu pro Aspose.Note?**  
A: Navštivte [forum Aspose.Note](https://forum.aspose.com/c/note/28) a prozkoumejte kompletní [dokumentaci](https://reference.aspose.com/note/java/).

## Závěr

Nyní máte kompletní, připravený příklad pro produkci, jak **convert onenote to image** a **save onenote as png** pomocí Aspose.Note pro Java. Začleňte tyto několik řádků do svého existujícího kódu a budete moci na vyžádání generovat vysoce kvalitní obrázky z poznámkových bloků OneNote.

---

**Last Updated:** 2025-12-28  
**Tested With:** Aspose.Note 24.11 for Java  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}