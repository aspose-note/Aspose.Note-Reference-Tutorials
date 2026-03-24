---
date: 2026-03-24
description: Naučte se, jak uložit OneNote jako obrázek a převést OneNote na obrázek
  pomocí Aspose.Note pro Javu. Podrobný návod krok po kroku pro vývojáře Javy.
linktitle: Save OneNote as Image – Convert Notebook to Image with Aspose.Note
second_title: Aspose.Note Java API
title: Uložit OneNote jako obrázek – převést poznámkový blok na obrázek pomocí Aspose.Note
url: /cs/java/onenote-notebook-operations/convert-notebook-to-image/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Uložte OneNote jako obrázek – Převod poznámkového bloku na obrázek pomocí Aspise.Note

## Úvod

V tomto tutoriálu se naučíte **jak uložit OneNote jako obrázek** převodem poznámkového bloku OneNote na PNG (nebo jiný formát obrázku) pomocí knihovny Aspose.Note pro Java. Převod stránek poznámkového bloku na obrázky je užitečný, když potřebujete sdílet poznámky na platformách, které nepodporují soubory OneNote, vložit je do PDF nebo zahrnout do prezentací.

## Rychlé odpovědi
- **Jaká knihovna je potřeba?** Aspose.Note for Java.  
- **Jaké formáty obrázků jsou podporovány?** PNG, JPEG, BMP, GIF, TIFF, atd.  
- **Potřebuji licenci?** Bezplatná zkušební verze funguje pro testování; pro produkční nasazení je vyžadována komerční licence.  
- **Jak dlouho trvá převod?** Obvykle několik sekund na poznámkový blok, v závislosti na velikosti.  
- **Mohu zpracovávat poznámkové bloky hromadně?** Ano – stačí projít soubory ve smyčce a znovu použít stejný kód.

## Co znamená **save OneNote as image**?

Uložení OneNote jako obrázek znamená vykreslení každé stránky poznámkového bloku `.one` do rastrového souboru obrázku (např. PNG). Vytvoří to přenosnou, pouze‑pro‑zobrazení reprezentaci, kterou lze zobrazit kdekoliv bez potřeby OneNote.

## Proč převádět OneNote na obrázek?

- **Sdílení napříč platformami** – Příjemci mohou obsah zobrazit na jakémkoli zařízení.  
- **Vkládání do dokumentů** – Vložte obrázek do Wordu, PowerPointu nebo PDF.  
- **Archivace** – Uložte vizuální snímek, který se nezmění, i když je původní poznámkový blok upraven.  
- **Připraveno pro prezentaci** – Použijte vysoce rozlišené PNG přímo v slidech.

## Požadavky

Před začátkem se ujistěte, že máte:

1. **Java Development Kit (JDK)** – Stáhněte nejnovější JDK z [webu](https://www.oracle.com/java/technologies/javase-jdk15-downloads.html).  
2. **Knihovna Aspose.Note pro Java** – Stáhněte JAR z [webu Aspose](https://releases.aspose.com/note/java/) a přidejte jej do classpath vašeho projektu.

## Import balíčků

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.SaveFormat;
```

Nyní projděme proces převodu krok za krokem.

## Krok 1: Načtení dokumentu poznámkového bloku

```java
// Specify the directory where your notebook file is located
String dataDir = "Your Document Directory";

// Load the document into Aspose.Note
Document oneFile = new Document(dataDir + "Sample1.one");
```

Ukážeme API na složku, která obsahuje `Sample1.one`, a načteme ji do objektu `Document`. Odtud můžete přistupovat ke stránkám, sekcím a dalším prvkům poznámkového bloku.

## Krok 2: Inicializace ImageSaveOptions

```java
// Initialize PdfSaveOptions object
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);
```

`ImageSaveOptions` říká Aspose.Note, jak má být výstup vykreslen. V tomto příkladu volíme PNG, ale můžete nahradit `SaveFormat.Png` za `SaveFormat.Jpeg`, `SaveFormat.Bmp` atd., abyste **převáděli OneNote na obrázek** v jiném formátu.

## Krok 3: Uložení dokumentu jako obrázek

```java
// Save the document as PNG
oneFile.save(dataDir + "ConvertToImage_out.png", options);
```

Volání `save()` zapíše vykreslené stránky poznámkového bloku do `ConvertToImage_out.png`. Pokud poznámkový blok obsahuje více stránek, Aspose.Note automaticky vygeneruje samostatné soubory obrázků (např. `ConvertToImage_out_1.png`, `ConvertToImage_out_2.png`).

## Krok 4: Vytištění potvrzení

```java
System.out.println("File saved: " + dataDir + "ConvertToImage_out.png");
```

Jednoduchá zpráva v konzoli potvrzuje, že operace **save OneNote as image** byla úspěšná a uvádí, kde najdete výstupní soubor.

## Časté problémy a tipy

- **Velké poznámkové bloky** – Zvyšte haldu JVM (`-Xmx`), pokud narazíte na `OutOfMemoryError`.  
- **Řízení rozlišení** – Použijte `options.setResolution(300);` pro zvýšení DPI pro obrázky v tiskové kvalitě.  
- **Hromadný převod** – Zabalte výše uvedené kroky do `for` smyčky, která iteruje přes seznam souborů `.one`.

## Často kladené otázky

### Q1: Mohu převádět poznámkové bloky do jiných formátů obrázků než PNG?

A1: Ano, můžete. Knihovna Aspose.Note podporuje různé formáty obrázků jako JPEG, BMP, GIF, TIFF atd. Požadovaný formát můžete v objektu `ImageSaveOptions` nastavit podle potřeby.

### Q2: Je Aspose.Note kompatibilní se všemi verzemi OneNote?

A2: Aspose.Note poskytuje komplexní podporu pro různé verze OneNote, což zajišťuje kompatibilitu napříč různými prostředími a formáty souborů.

### Q3: Mohu během převodu přizpůsobit nastavení výstupního obrázku?

A3: Rozhodně. Aspose.Note nabízí široké možnosti přizpůsobení výstupního obrázku, včetně rozlišení, kvality, barevné hloubky a dalších. Tato nastavení můžete upravit podle svých požadavků.

### Q4: Podporuje Aspose.Note hromadný převod více poznámkových bloků?

A4: Ano, můžete hromadně převádět více poznámkových bloků na obrázky efektivně pomocí Aspose.Note. Stačí projít seznam vašich souborů poznámkových bloků a aplikovat proces převodu popsaný v tomto tutoriálu.

### Q5: Kde mohu najít další zdroje a podporu pro Aspose.Note?

A5: Pro další dokumentaci, příklady a komunitní podporu navštivte [forum Aspose.Note](https://forum.aspose.com/c/note/28) a prozkoumejte [dokumentaci](https://reference.aspose.com/note/java/).

---

**Last Updated:** 2026-03-24  
**Tested With:** Aspose.Note for Java 24.8  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}