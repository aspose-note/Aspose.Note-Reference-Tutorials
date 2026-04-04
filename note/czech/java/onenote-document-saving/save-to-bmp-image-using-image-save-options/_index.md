---
date: 2026-03-05
description: Zjistěte, jak exportovat dokumenty OneNote do BMP obrázků pomocí Image
  Save Options v Aspose.Note pro Javu. Také se podívejte, jak převést OneNote do PDF
  nebo uložit OneNote jako PNG.
linktitle: how to export onenote to BMP Image Using Image Save Options
second_title: Aspose.Note Java API
title: Jak exportovat OneNote do BMP obrázku pomocí možností uložení obrázku
url: /cs/java/onenote-document-saving/save-to-bmp-image-using-image-save-options/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# jak exportovat onenote do BMP obrázku pomocí Image Save Options

## Jak exportovat onenote do BMP obrázku

Aspose.Note for Java je výkonná knihovna, která umožňuje vývojářům Java pracovat s soubory Microsoft OneNote programově. **V tomto tutoriálu se naučíte, jak exportovat onenote dokumenty do BMP obrázků** pomocí funkce Image Save Options v Aspose.Note for Java. Provedeme vás jednotlivými kroky, vysvětlíme, proč můžete zvolit BMP místo jiných formátů, a ukážeme, jak tuto funkci integrovat do vašich aplikací.

## Rychlé odpovědi
- **Co dělá třída Image Save Options?** Umožňuje vám určit výstupní formát obrázku (BMP, PNG, JPEG atd.) při převodu stránky OneNote.  
- **Potřebuji licenci pro spuštění ukázky?** Bezplatná zkušební verze funguje pro hodnocení, ale pro produkční použití je vyžadována komerční licence.  
- **Mohu převést stránku OneNote do PDF nebo PNG místo BMP?** Ano – stačí změnit výčtový typ `SaveFormat` (např. `SaveFormat.Pdf` nebo `SaveFormat.Png`).  
- **Jaká verze Javy je podporována?** Java 8 a novější jsou plně podporovány.  
- **Existuje nějaké speciální zpracování pro velké dokumenty?** Můžete streamovat výstup, aby se předešlo vysoké spotřebě paměti.

## Co je “Image Save Options” v Aspose.Note?
`ImageSaveOptions` třída poskytuje detailní kontrolu nad tím, jak jsou stránky OneNote vykreslovány jako rastrové obrázky. Můžete nastavit formát obrázku, rozlišení, barevnou hloubku a další. Tato flexibilita usnadňuje **export obrázku stránky onenote** pro starší systémy (BMP) nebo moderní webové scénáře (PNG/JPEG).  

## Předpoklady

Než začnete, ujistěte se, že máte:

1. Základní znalosti programovacího jazyka Java.  
2. Nainstalovaný JDK (Java Development Kit) na vašem počítači.  
3. IDE, jako je Eclipse nebo IntelliJ IDEA.  
4. Knihovnu Aspose.Note for Java – stáhněte ji z [here](https://releases.aspose.com/note/java/).

## Import balíčků

First, import the necessary Aspose.Note classes and standard Java I/O utilities:

```java
import com.aspose.note.*;
import java.io.IOException;
```

## Krok 1: Načtení dokumentu OneNote

```java
// The path to the documents directory.
String dataDir = "Your Document Directory";

// Load the document into Aspose.Note.
Document oneFile = new Document(dataDir + "Aspose.one");
```

Zde ukazujeme na složku, která obsahuje zdrojový soubor OneNote (`Aspose.one`), a načteme jej do objektu `Document`. Tento objekt vám poskytuje plný přístup ke stránkám, sekcím a dalším prvkům v poznámkovém bloku.

## Krok 2: Uložení dokumentu jako BMP obrázek

```java
dataDir = dataDir + "SaveToBmpImageUsingImageSaveOptions_out.bmp";

// Save the document.
oneFile.save(dataDir, new ImageSaveOptions(SaveFormat.Bmp));
```

Spojíme název výstupního souboru a poté zavoláme `save` s instancí `ImageSaveOptions` nakonfigurovanou pro **BMP** (`SaveFormat.Bmp`).  
Pokud chcete **uložit stránku onenote** jako PNG, jednoduše nahraďte `SaveFormat.Bmp` za `SaveFormat.Png`. Podobně `SaveFormat.Pdf` vám umožní provést konverzi **onenote do pdf**.

## Proč zvolit BMP?

- **Bezeztrátová kvalita** – BMP ukládá surová data pixelů, zachovává přesný vzhled původní stránky.  
- **Kompatibilita** – Starší aplikace Windows často vyžadují soubory BMP.  
- **Jednoduchost** – Žádné artefakty komprese, což je ideální pro další zpracování obrázků.

## Časté problémy a tipy

- **Chyby cesty k souboru** – Ujistěte se, že `dataDir` končí správným oddělovačem souborů (`/` nebo `\`).  
- **Velké poznámkové bloky** – U velmi velkých souborů OneNote zvažte ukládání každé stránky samostatně, aby se snížila spotřeba paměti.  
- **Výjimky licence** – Spuštění kódu bez platné licence přidá vodoznak do vygenerovaného obrázku.

## Závěr

V tomto průvodci jsme ukázali **jak exportovat onenote** dokumenty do BMP obrázků pomocí `ImageSaveOptions` v Aspose.Note for Java. Výměnou výčtového typu `SaveFormat` můžete také generovat PNG, JPEG, PDF nebo jiné podporované formáty, což vám poskytuje flexibilní způsob exportu obsahu OneNote pro jakýkoli následný scénář.

## Často kladené otázky

**Q1: Mohu uložit OneNote dokumenty do jiných formátů obrázků kromě BMP?**  
A: Ano, můžete použít `ImageSaveOptions` s `SaveFormat.Png`, `SaveFormat.Jpeg`, `SaveFormat.Gif` nebo `SaveFormat.Tiff` pro export do těchto formátů.

**Q2: Podporuje Aspose.Note for Java konverzi mezi různými formáty dokumentů?**  
A: Rozhodně. Kromě formátů obrázků můžete konvertovat soubory OneNote do PDF, DOCX, HTML a dalších pomocí odpovídajícího `SaveFormat`.

**Q3: Je Aspose.Note for Java kompatibilní s nejnovějšími verzemi OneNote?**  
A: Ano, knihovna je pravidelně aktualizována, aby byla v souladu s nejnovějšími verzemi OneNote.

**Q4: Mohu programově manipulovat s obsahem OneNote dokumentů?**  
A: Ano, můžete přidávat, upravovat nebo mazat stránky, sekce a bohatý obsah (text, obrázky, tabulky) pomocí API.

**Q5: Poskytuje Aspose.Note for Java technickou podporu?**  
A: Ano, Aspose nabízí technickou podporu a vyhrazené fórum. Navštivte [Aspose.Note forum](https://forum.aspose.com/c/note/28) pro pomoc.

**Poslední aktualizace:** 2026-03-05  
**Testováno s:** Aspose.Note for Java 24.12  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}