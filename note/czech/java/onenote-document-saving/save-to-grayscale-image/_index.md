---
date: 2025-12-17
description: Naučte se, jak exportovat OneNote uložením dokumentu jako černobílý PNG
  obrázek pomocí Aspose.Note pro Javu. Obsahuje kroky k načtení dokumentu OneNote
  a vytvoření černobílého obrázku.
linktitle: How to Export OneNote as Grayscale Image – Aspose.Note
second_title: Aspose.Note Java API
title: Jak exportovat OneNote jako obrázek v odstínech šedi – Aspose.Note
url: /cs/java/onenote-document-saving/save-to-grayscale-image/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Uložení do odstínů šedi v OneNote - Aspose.Note

## Úvod

V tomto tutoriálu vám ukážeme **jak exportovat onenote** uložením dokumentu jako obrázku v odstínech šedi pomocí Aspose.Note pro Java. Obrázky v odstínech šedi jsou monochromatické snímky, které obsahují pouze odstíny šedé, což může být užitečné pro tisk, archivaci nebo snížení velikosti souboru. Provedeme vás načtením dokumentu OneNote, nastavením možností uložení pro **vytvoření obrázku v odstínech šedi** a nakonec **uložením dokumentu jako PNG**.

## Rychlé odpovědi
- **Co znamená “jak exportovat onenote”?** Odkazuje na programatické převádění souboru OneNote do jiného formátu, například obrázku.  
- **Který formát je nejlepší pro výstup v odstínech šedi?** PNG funguje dobře, protože zachovává bezztrátovou kvalitu a podporuje režim odstínů šedi.  
- **Potřebuji licenci?** Platná licence Aspose.Note je vyžadována pro produkční použití; dočasná zkušební licence je k dispozici pro testování.  
- **Jaká verze Javy je požadována?** Doporučuje se Java 8 nebo novější.  
- **Mohu změnit velikost obrázku?** Ano, můžete před uložením upravit vlastnosti `ImageSaveOptions`, jako jsou `Resolution` nebo `PageSize`.

## Co je “jak exportovat onenote”?
Exportování OneNote znamená programatické převádění souboru OneNote `.one` do jiné podoby – například PDF, HTML nebo obrázku. V tomto průvodci se zaměřujeme na export do **obrázku PNG v odstínech šedi**, což je častý požadavek pro dokumentaci nebo tiskové workflowy.

## Proč exportovat OneNote jako obrázek v odstínech šedi?
- **Menší velikost souboru** – PNG v odstínech šedi jsou obvykle menší než plnobarevné obrázky.  
- **Lepší čitelnost** – Pro tištěné zprávy poskytuje odstín šedi často jasnější kontrast.  
- **Kompatibilita** – PNG je široce podporováno v prohlížečích, editorech i mobilních zařízeních.  

## Předpoklady

Před začátkem se ujistěte, že máte následující:

1. Nainstalovaný Java Development Kit (JDK) na vašem systému.  
2. Knihovnu Aspose.Note pro Java. Můžete ji stáhnout [zde](https://releases.aspose.com/note/java/).  
3. Základní znalost programování v Javě.  

## Import balíčků

Pro zahájení importujte potřebné balíčky:

```java
import com.aspose.note.ColorMode;
import com.aspose.note.Document;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.SaveFormat;
import java.io.IOException;
```

## Krok 1: Načtení dokumentu OneNote

Nejprve **načtěte onenote dokument** do Aspose.Note. Nahraďte `"Your Document Directory"` cestou k vaší lokální složce a `"Aspose.one"` názvem vašeho souboru OneNote.

```java
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Aspose.one");
```

## Krok 2: Nastavení výstupní cesty a možností

Definujte výstupní cestu pro obrázek v odstínech šedi a specifikujte možnosti uložení. Nastavíme `ColorMode` na `GrayScale` a použijeme formát **save document as png**.

```java
dataDir = dataDir + "SaveAsGrayscaleImage_out.png";
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);
options.setColorMode(ColorMode.GrayScale);
```

## Krok 3: Uložení dokumentu

Nakonec uložte dokument jako obrázek PNG v odstínech šedi pomocí nakonfigurovaných možností.

```java
oneFile.save(dataDir, options);
```

## Časté problémy a řešení
- **FileNotFoundException** – Ověřte, že `dataDir` ukazuje na správnou složku a že soubor `.one` existuje.  
- **LicenseException** – Ujistěte se, že jste před voláním `save` použili platnou licenci Aspose.Note.  
- **Nízké rozlišení výstupu** – Pokud je potřeba, upravte `options.setResolution(300)` pro zvýšení DPI.  

## Často kladené otázky

**Q1: Mohu uložit obrázek v odstínech šedi v jiném formátu?**  
A1: Ano, stačí změnit parametr `SaveFormat` v konstruktoru `ImageSaveOptions` na `Jpeg`, `Bmp` atd.

**Q2: Je Aspose.Note kompatibilní se všemi verzemi dokumentů OneNote?**  
A2: Aspose.Note podporuje Microsoft OneNote 2010 a novější verze.

**Q3: Vyžaduje Aspose.Note licenci k použití?**  
A3: Pro produkční použití je vyžadována platná licence, ale pro vyhodnocení lze získat dočasnou zkušební licenci.

**Q4: Mohu upravit jiné aspekty dokumentu před jeho uložením jako obrázek?**  
A4: Rozhodně! Aspose.Note poskytuje komplexní API pro úpravu sekcí, stránek a obsahu před exportem.

**Q5: Kde mohu najít podporu, pokud narazím na problémy?**  
A5: Podporu najdete na fóru Aspose.Note [zde](https://forum.aspose.com/c/note/28).

## Závěr

Nyní jste se naučili **jak exportovat onenote** načtením souboru OneNote, nastavením možností uložení pro **vytvoření obrázku v odstínech šedi** a **uložením dokumentu jako PNG**. Tato technika je užitečná pro vytváření lehkých, připravených k tisku vizuálů z poznámkových bloků OneNote. Nebojte se experimentovat s dalšími nastaveními `ColorMode` nebo formáty obrázků, aby vyhovovaly potřebám vašeho projektu.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Last Updated:** 2025-12-17  
**Tested With:** Aspose.Note 24.12 for Java  
**Author:** Aspose  

---