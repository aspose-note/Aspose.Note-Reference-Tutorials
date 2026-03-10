---
date: 2025-12-21
description: Naučte se, jak vytvořit dokument OneNote v Javě a snadno vkládat obrázky
  pomocí Aspose.Note pro Javu. Krok za krokem průvodce pro vývojáře Javy.
linktitle: How to create onenote document java – Build Doc and Insert Image with Stream
second_title: Aspose.Note Java API
title: Jak vytvořit dokument OneNote v Javě – vytvořit dokument a vložit obrázek pomocí
  streamu
url: /cs/java/onenote-hyperlinks-images/build-doc-insert-image-stream/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak vytvořit onenote dokument java – Vytvořit dokument a vložit obrázek pomocí streamu

## Úvod

Vítejte! V tomto tutoriálu **vytvoříte onenote dokument java** od nuly a naučíte se, jak vkládat obrázky pomocí image streamu. Provedeme vás každým krokem, vysvětlíme, proč je každá část důležitá, a poskytneme praktické tipy, abyste techniku mohli použít v reálných projektech. Na konci budete schopni programově generovat stránky OneNote a vkládat obrázky přesně tam, kde je potřebujete.

## Rychlé odpovědi
- **Jaká knihovna je potřeba?** Aspose.Note for Java  
- **Mohu vkládat obrázky ze streamu?** Ano – stačí předat `InputStream` konstruktoru `Image`.  
- **Do jakého formátu mohu exportovat?** Jakýkoli formát podporovaný Aspose.Note, např. PDF, DOCX, HTML.  
- **Potřebuji licenci pro vývoj?** Pro hodnocení stačí bezplatná dočasná licence; pro produkci je vyžadována plná licence.  
- **Jaká verze Javy je požadována?** Java 8 nebo vyšší.

## Co je “create onenote document java”?

Vytvoření OneNote dokumentu v Javě znamená použití API Aspose.Note k programatickému sestavení struktury poznámkového bloku – stránky, obrysy a prvky – bez otevření desktopového klienta OneNote. Tento přístup je ideální pro automatizovanou generaci reportů, hromadné zpracování poznámek nebo integraci obsahu OneNote do větších Java aplikací.

## Proč použít Aspose.Note for Java k vytvoření onenote dokument java?

- **Úplná kontrola** nad rozvržením stránky, umístěním obrysu a stylováním prvků.  
- **Žádná COM interop** – funguje na jakémkoli OS, který podporuje Javu.  
- **Bohaté možnosti exportu** – převod stejného dokumentu do PDF, DOCX, HTML atd. jedním voláním.  
- **Stream‑přátelské** – můžete načítat obrázky přímo z paměti, sítě nebo cloudového úložiště.

## Požadavky

Než začneme, ujistěte se, že máte nastaveno následující:

### Java Development Kit (JDK)

Aktuální JDK (8 nebo novější) nainstalované na vašem počítači.

### Aspose.Note for Java Library

Stáhněte knihovnu z oficiální stránky vydání Aspose: [https://releases.aspose.com/note/java/](https://releases.aspose.com/note/java/).

### Nastavení IDE

Nakonfigurujte své oblíbené IDE (IntelliJ IDEA, Eclipse, VS Code) tak, aby zahrnovalo soubory JAR Aspose.Note v classpath projektu.

## Import balíčků

Pro začátek importujte potřebné třídy Java a Aspose.Note. Tyto importy vám umožní vytvářet dokumenty, pracovat se stránkami, spravovat obrysy a vkládat obrázky.

```java
import java.io.FileInputStream;
import java.io.FileNotFoundException;
import java.io.IOException;
import java.io.InputStream;
import com.aspose.note.Document;
import com.aspose.note.HorizontalAlignment;
import com.aspose.note.Image;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.SaveFormat;
```

## Krok 1: Nastavení adresáře dokumentu

Definujte složku, která obsahuje vaše zdrojové obrázky a kam bude uložen výstupní soubor. Nahraďte zástupný text skutečnou cestou na vašem počítači.

```java
String dataDir = "Your Document Directory";
```

## Krok 2: Vytvoření objektu Document

Vytvořte novou instanci `Document`. Tento objekt představuje OneNote notebook, který budujete.

```java
Document doc = new Document();
```

## Krok 3: Inicializace objektu Page

Vytvořte `Page`, která bude obsahovat všechny obrysy a prvky pro tuto stránku notebooku.

```java
Page page = new Page();
```

## Krok 4: Vytvoření Outline

`Outline` funguje jako kontejner pro umístěné prvky. Zde nastavíme vertikální a horizontální offsety pro umístění obrysu na stránce.

```java
Outline outline1 = new Outline();
outline1.setVerticalOffset(600);
outline1.setHorizontalOffset(0);
```

## Krok 5: Vytvoření Outline Element

`OutlineElement` bude hostit obrázek, který se chystáme vložit.

```java
OutlineElement outlineElem1 = new OutlineElement();
```

## Krok 6: Načtení Image Streamu

Otevřete soubor s obrázkem jako stream. Použití streamu vám umožní číst obrázek z libovolného zdroje (souborový systém, síť, databáze) bez nutnosti nejprve jej ukládat na disk.

```java
InputStream fs = null;
try {
    fs = new FileInputStream(dataDir + "image.jpg");
} catch (FileNotFoundException e) {
    e.printStackTrace();
}
```

## Krok 7: Vložení obrázku

Vytvořte objekt `Image`. První argument může být `null`, když později poskytnete stream, ale pro jednoduchost zde odkazujeme na cestu k souboru a nastavíme jeho zarovnání na pravou stranu stránky.

```java
Image image = new Image(null, dataDir + "image1.jpg");
image.setAlignment(HorizontalAlignment.Right);
```

## Krok 8: Přidání obrázku do Outline Element

Přidejte obrázek do elementu obrysu, aby se stal součástí vizuální hierarchie stránky.

```java
outlineElem1.appendChildLast(image);
```

## Krok 9: Připojení Outline Element k Outline

Nyní připojte element obrysu (který obsahuje obrázek) k obalovému kontejneru obrysu.

```java
outline1.appendChildLast(outlineElem1);
```

## Krok 10: Připojení Outline k Page

Umístěte obrys na stránku.

```java
page.appendChildLast(outline1);
```

## Krok 11: Připojení Page k Document

Přidejte plně vytvořenou stránku do objektu dokumentu.

```java
doc.appendChildLast(page);
```

## Krok 12: Uložení dokumentu

Nakonec uložte OneNote dokument ve formátu, který potřebujete. V tomto příkladu exportujeme do PDF, ale můžete zvolit libovolný formát podporovaný Aspose.Note.

```java
try {
    doc.save("D://Aspose_JavaProjects//OneNote//out3.pdf", SaveFormat.Pdf);
} catch (IOException e) {
    e.printStackTrace();
}
```

Podle těchto kroků jste úspěšně **vytvořili onenote dokument java** a vložili obrázek pomocí vstupního streamu.

## Časté problémy a tipy

- **Stream není uzavřen** – V produkčním scénáři vždy uzavřete `InputStream` v bloku `finally` nebo použijte try‑with‑resources.  
- **Nesprávná cesta k souboru** – Ověřte, že `dataDir` končí správným oddělovačem (`/` nebo `\`).  
- **Zarovnání obrázku** – Pokud se obrázek zobrazuje mimo obrazovku, upravte hodnoty `VerticalOffset`/`HorizontalOffset` obrysu.  
- **Licence a výjimky** – Použití evaluační verze může do výstupu přidat vodoznak; aplikujte platnou licenci pro jeho odstranění.

## Často kladené otázky

### Q1: Je Aspose.Note for Java kompatibilní se všemi verzemi OneNote?

A1: Aspose.Note for Java podporuje různé formáty souborů OneNote, což zajišťuje kompatibilitu napříč desktopovými, online i mobilními verzemi.

### Q2: Mohu přizpůsobit vzhled vložených obrázků v OneNote dokumentech pomocí Aspose.Note for Java?

A2: Ano, můžete měnit zarovnání, velikost, rotaci a dokonce aplikovat oříznutí pomocí odpovídajících vlastností objektu `Image`.

### Q3: Poskytuje Aspose.Note for Java podporu i pro jiné formáty dokumentů kromě PDF?

A3: Rozhodně. API umí exportovat do DOCX, HTML, XPS a několika dalších formátů, což vám dává flexibilitu při sdílení nebo archivaci poznámek.

### Q4: Kde najdu další zdroje a podporu pro Aspose.Note for Java?

A4: Oficiální web Aspose nabízí rozsáhlou dokumentaci, ukázkové kódy, fóra a dočasné licence pro hodnocení.

### Q5: Je k dispozici zkušební verze Aspose.Note for Java?

A5: Ano, můžete si stáhnout bezplatnou zkušební verzi z stránky vydání Aspose a vyzkoušet všechny funkce před zakoupením.

---

**Poslední aktualizace:** 2025-12-21  
**Testováno s:** Aspose.Note for Java 24.12 (nejnovější v době psaní)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}