---
date: 2026-01-05
description: Naučte se, jak nastavit výchozí jazykové nastavení, načíst dokument OneNote,
  nastavit licenci Aspose, převést OneNote na PNG a uložit OneNote jako obrázek pomocí
  Aspose.Note pro Javu.
linktitle: Working with Locales in OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: Nastavit výchozí národní prostředí v OneNote – Aspose.Note Java
url: /cs/java/onenote-notebook-operations/working-with-locales/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Nastavení výchozího národního prostředí v OneNote – Aspose.Note Java

## Úvod

Pokud potřebujete **nastavit výchozí národní prostředí** při zpracování souborů OneNote, Aspose.Note pro Java to usnadňuje. V tomto tutoriálu vás provedeme vším, co potřebujete – od licencování produktu po načtení dokumentu OneNote, změnu národního prostředí a nakonec převod souboru do PNG obrázku. Na konci budete schopni přizpůsobit nastavení jazyka a generovat výstupy specifické pro národní prostředí pomocí několika řádků kódu.

## Rychlé odpovědi
- **Co dělá “nastavit výchozí národní prostředí”?** Definuje jazyk a regionální formátování používané Aspose.Note při čtení nebo zápisu souborů OneNote.  
- **Potřebuji licenci?** Ano – nastavte licenci Aspose, aby se odemnuly všechny funkce.  
- **Jaká verze Javy je vyžadována?** Jakákoli JDK 8+ je podporována.  
- **Mohu převést OneNote do PNG?** Ano; API vám umožní uložit stránky jako obrázky.  
- **Je proces thread‑safe?** Nastavení výchozího národního prostředí je globální, takže jej nastavte jednou při spuštění aplikace.

## Co je “nastavit výchozí národní prostředí” v Aspose.Note?
Nastavení výchozího národního prostředí říká Aspose.Note, jaký jazyk a kulturní konvence má použít při parsování dat, čísel a textu. To je nezbytné pro multi‑regionální aplikace, které potřebují konzistentní formátování napříč různými uživatelskými národními prostředími.

## Proč nastavit výchozí národní prostředí při práci s OneNote?
- **Přesná reprezentace dat:** Data a čísla se zobrazují správně pro cílové publikum.  
- **Konzistentní řetězce UI:** Text extrahovaný z OneNote respektuje nastavení jazyka.  
- **Zjednodušený převod:** Když později převádíte soubor OneNote do PNG nebo jiných formátů, vizuální rozvržení odpovídá očekávanému národnímu prostředí.

## Předpoklady

- **Java vývojové prostředí:** Nainstalovaná JDK a nastavená proměnná `JAVA_HOME`.  
- **Knihovna Aspose.Note:** Stáhněte nejnovější JAR z [odkaz ke stažení](https://releasespose.com/note/java/).  
- **Platný soubor licence Aspose** (bezplatná zkušební verze funguje pro testování).

## Import balíčků

Před psaním jakéhokoli kódu importujte třídy, které poskytují požadovanou funkčnost.

```java
import java.io.IOException;
import java.nio.file.Path;
import java.util.Locale;
import com.aspose.note.Document;
import com.aspose.note.License;
import com.aspose.note.LocaleOptions;
```

## Krok 1: Nastavit licenci Aspose

```java
License license = new License();
license.setLicense("licenseFile");
```

Nastavení licence Aspose odemkne všechny funkce, včetně zpracování národního prostředí a konverze obrázků.

## Krok 2: Nastavit výchozí národní prostředí

```java
java.util.Locale.setDefault(new java.util.Locale("en", "rs"));
```

Zde **nastavujeme výchozí národní prostředí** na angličtinu (`en`) s kódem země `rs`. Přizpůsobte kódy jazyka a země tak, aby odpovídaly vaší cílové oblasti.

## Krok 3: Načíst dokument OneNote

```java
String inputFile = "Sample1.one";
Path inputPath = Paths.get(inputFile);

Document oneFile = new Document(inputPath.toString());
```

Tento krok **načte dokument OneNote** do objektu `Document`, abyste s ním mohli pracovat.

## Krok 4: Převést OneNote do PNG (konverze souboru OneNote)

```java
oneFile.save("sample.png");
```

Metoda `save` provádí **konverzi souboru onenote**, exportuje notebook (nebo konkrétní stránku) jako PNG obrázek – v podstatě **převádí onenote na png** a **ukládá onenote jako obrázek**.

## Časté problémy a tipy

- **Licence nenalezena:** Ujistěte se, že cesta k `licenseFile` je správná a soubor má oprávnění ke čtení.  
- **Národní prostředí nebylo použito:** Zavolejte `Locale.setDefault` **před** načtením dokumentu.  
- **Chybí výstup obrázku:** Ověřte, že soubor OneNote skutečně obsahuje vykreslovatelné stránky; prázdné notebooky vytvoří prázdný PNG.

## Často kladené otázky

**Q: Je Aspose.Note kompatibilní s různými verzemi Javy?**  
A: Ano, Aspose.Note podporuje Javu 8 a novější, což zajišťuje širokou kompatibilitu napříč vývojovými prostředími.

**Q: Mohu integrovat Aspose.Note s jinými knihovnami Javy?**  
A: Rozhodně. API funguje hladce s populárními knihovnami jako Apache POI, Jackson a Spring.

**Q: Nabízí Aspose.Note podporu pro různé formáty souborů?**  
A: I když je jeho hlavní zaměření na soubory OneNote, knihovna může exportovat do PNG, JPEG, PDF a dalších formátů obrázků.

**Q: Existuje komunitní fórum pro uživatele Aspose.Note, kde mohou požádat o pomoc a sdílet znalosti?**  
A: Ano, komunitní fórum Aspose poskytuje platformu pro uživatele, aby se spojili s odborníky, kladli otázky a spolupracovali na řešeních. Navštivte [fórum podpory](https://forum.aspose.com/c/note/28) pro pomoc.

**Q: Můžu vyzkoušet Aspose.Note před zakoupením?**  
A: Samozřejmě, můžete prozkoumat možnosti Aspose.Note využitím bezplatné zkušební verze nabízené na webových stránkách.

## Závěr

Podle těchto kroků jste se naučili, jak **nastavit výchozí národní prostředí**, **načíst dokument OneNote**, **nastavit licenci Aspose** a **převést OneNote do PNG** pomocí Aspose.Note pro Java. Tento postup vám umožní vytvářet zprávy a obrázky citlivé na národní prostředí, které osloví globální publikum.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Last Updated:** 2026-01-05  
**Tested With:** Aspose.Note 24.11 for Java  
**Author:** Aspose