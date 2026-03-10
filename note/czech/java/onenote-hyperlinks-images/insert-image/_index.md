---
date: 2025-12-21
description: Naučte se, jak přidat obrázek do dokumentů OneNote pomocí Javy s Aspose.Note
  pro Javu. Postupujte podle našeho krok‑za‑krokem průvodce, jak vkládat obrázky a
  případně uložit OneNote jako PDF.
linktitle: Insert an Image in OneNote Document with Java
second_title: Aspose.Note Java API
title: Jak přidat obrázek do OneNote pomocí Javy
url: /cs/java/onenote-hyperlinks-images/insert-image/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Vložení obrázku do dokumentu OneNote pomocí Javy

## Úvod

V tomto tutoriálu se podíváme, jak vložit obrázek do dokumentu OneNote pomocí Javy s využitím Aspose.Note for Java. Aspose.Note for Java je výkonná knihovna, která umožňuje vývojářům programově pracovat se soubory Microsoft OneNote, což zahrnuje různé operace, jako je vytváření, čtení a manipulace s dokumenty OneNote.

## Rychlé odpovědi
- **Jaký je nejjednodušší způsob, jak přidat obrázek do OneNote pomocí Javy?**  
  Použijte třídu `Image` z Aspose.Note for Java a připojte ji k stránce.
- **Potřebuji licenci pro produkční použití?**  
  Ano, pro produkční nasazení je vyžadována komerční licence.
- **Mohu nastavit vlastní rozměry obrázku?**  
  Samozřejmě – zavolejte `setWidth()` a `setHeight()` na objektu `Image`.
- **Je možné uložit soubor OneNote jako PDF po přidání obrázku?**  
  Ano, zavolejte `save(..., SaveFormat.Pdf)` pro **uložení OneNote jako PDF**.
- **Která verze Javy je podporována?**  
  Aspose.Note for Java funguje s JDK 8 a novějšími.

## Jak přidat obrázek do OneNote pomocí Javy?

Než se pustíme do kódu, stručně si vysvětlíme, proč byste mohli chtít programově vkládat obrázky do OneNote. Ať už generujete zápisy ze schůzek, vytváříte automatizované reporty nebo budujete pipeline dokumentace, vkládání obrázků poskytuje vašim poznámkám vizuální kontext, který čistý text nedokáže poskytnout. S Aspose.Note for Java můžete vše provést čistě v kódu, bez nutnosti otevírat UI OneNote.

## Předpoklady

Než začneme, ujistěte se, že máte nastavené následující předpoklady:

### 1. Java Development Kit (JDK)
Ujistěte se, že máte nainstalovaný Java Development Kit (JDK). Můžete jej stáhnout a nainstalovat z webu Oracle.

### 2. Aspose.Note for Java Library
Stáhněte a nastavte knihovnu Aspose.Note for Java podle [dokumentace](https://reference.aspose.com/note/java/).

## Import balíčků

Začněte importováním potřebných balíčků do vašeho Java projektu. Tyto balíčky zahrnují knihovnu Aspose.Note a další požadované závislosti.

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.HorizontalAlignment;
import com.aspose.note.Image;
import com.aspose.note.LoadOptions;
import com.aspose.note.Page;
import com.aspose.note.SaveFormat;
```

Rozdělíme proces vkládání obrázku do dokumentu OneNote na několik kroků:

## Krok 1: Načtení dokumentu OneNote

Nejprve načtěte dokument OneNote, do kterého chcete obrázek vložit.

```java
LoadOptions options = new LoadOptions();
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Sample1.one", options);
```

## Krok 2: Získání stránky

Získejte stránku v dokumentu, kde chcete obrázek vložit.

```java
Page page = oneFile.getFirstChild();
```

## Krok 3: Načtení obrázku

Načtěte obrázek, který chcete vložit do dokumentu OneNote.

```java
Image image = new Image(oneFile, dataDir + "Input.jpg");
```

## Krok 4: Přizpůsobení atributů obrázku (volitelné)

Volitelně můžete přizpůsobit velikost, umístění a zarovnání obrázku podle svých požadavků. Zde můžete **nastavit rozměry obrázku v Javě**.

```java
image.setWidth(100);
image.setHeight(100);
image.setVerticalOffset(400);
image.setHorizontalOffset(100);
image.setAlignment(HorizontalAlignment.Right);
```

## Krok 5: Přidání obrázku na stránku

Přidejte obrázek na stránku v dokumentu OneNote.

```java
page.appendChildLast(image);
```

## Krok 6: Uložení dokumentu

Uložte upravený dokument, včetně vloženého obrázku. V tomto kroku můžete také **uložit OneNote jako PDF**.

```java
try {
    oneFile.save(dataDir + "InsertanImage_out.pdf", SaveFormat.Pdf);
} catch (IOException e) {
    e.printStackTrace();
}
```

## Závěr

V tomto tutoriálu jsme se naučili, jak vložit obrázek do dokumentu OneNote pomocí Javy s pomocí knihovny Aspose.Note for Java. Dodržením krok‑za‑krokem průvodce můžete snadno programově začlenit obrázky do svých OneNote dokumentů.

## Často kladené otázky

### Q1: Mohu pomocí této metody vložit do jednoho dokumentu OneNote více obrázků?

A1: Ano, můžete vložit více obrázků do jednoho dokumentu OneNote opakováním postupu popsaného v tomto tutoriálu pro každý obrázek.

### Q2: Je Aspose.Note for Java kompatibilní se všemi verzemi OneNote?

A2: Aspose.Note for Java podporuje práci se soubory OneNote vytvořenými v Microsoft OneNote 2010 a novějších verzích.

### Q3: Mohu do OneNote dokumentu vložit obrázky různých formátů, například PNG nebo GIF?

A3: Ano, Aspose.Note for Java podporuje vkládání obrázků v různých formátech, včetně PNG, JPEG, GIF a dalších.

### Q4: Existuje zkušební verze Aspose.Note for Java pro testovací účely?

A4: Ano, můžete si stáhnout bezplatnou zkušební verzi Aspose.Note for Java z webu pro evaluační účely.

### Q5: Jak mohu získat technickou podporu pro Aspose.Note for Java?

A5: Technickou podporu pro Aspose.Note for Java získáte na [fóru](https://forum.aspose.com/c/note/28) věnovaném produktům Aspose.Note.

---

**Poslední aktualizace:** 2025-12-21  
**Testováno s:** Aspose.Note for Java 24.10  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}