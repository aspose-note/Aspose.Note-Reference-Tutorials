---
title: Sestavte dokument a vložte obrázek pomocí streamu ve OneNotu - Java
linktitle: Sestavte dokument a vložte obrázek pomocí streamu ve OneNotu - Java
second_title: Aspose.Note Java API
description: Naučte se, jak bez námahy integrovat obrázky do dokumentů OneNotu pomocí Aspose.Note pro Java. Výukový program krok za krokem pro vývojáře v jazyce Java.
type: docs
weight: 13
url: /cs/java/onenote-hyperlinks-images/build-doc-insert-image-stream/
---
## Úvod

Vítejte v našem komplexním kurzu o používání Aspose.Note pro Java k vytváření dokumentů a vkládání obrázků pomocí proudů obrázků ve OneNotu! V tomto tutoriálu vás provedeme procesem krok za krokem a zajistíme, že budete jasně rozumět každé fázi. Na konci budete moci bez námahy integrovat obrázky do dokumentů OneNotu pomocí Javy.

## Předpoklady

Než se pustíme do výukového programu, ujistěte se, že máte splněny následující předpoklady:

### Java Development Kit (JDK)

Ujistěte se, že máte v systému nainstalovanou sadu Java Development Kit (JDK). Můžete si jej stáhnout z webu Oracle.

### Aspose.Note pro Java Library

 Stáhněte a nainstalujte knihovnu Aspose.Note for Java z poskytnutého souboru[odkaz](https://releases.aspose.com/note/java/).

### Nastavení IDE

Nastavte své integrované vývojové prostředí (IDE) s konfiguracemi nezbytnými pro práci s projekty Java.

## Importujte balíčky

Chcete-li začít, importujte požadované balíčky do svého projektu Java. Tyto balíčky poskytnou potřebné funkce pro práci s dokumenty a obrázky OneNotu.

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

## Krok 1: Nastavte adresář dokumentů

 Definujte adresář, kde se nachází váš dokument a obrázky. Nahradit`"Your Document Directory"` s cestou k vašemu adresáři.

```java
String dataDir = "Your Document Directory";
```

## Krok 2: Vytvořte objekt dokumentu

 Inicializujte instanci souboru`Document` třídy, abyste mohli začít pracovat s dokumentem OneNotu.

```java
Document doc = new Document();
```

## Krok 3: Inicializujte objekt stránky

 Vytvořit`Page` objekt reprezentující stránku v dokumentu.

```java
Page page = new Page();
```

## Krok 4: Vytvořte obrys

 Inicializujte an`Outline` objekt pro strukturování obsahu na stránce.

```java
Outline outline1 = new Outline();
outline1.setVerticalOffset(600);
outline1.setHorizontalOffset(0);
```

## Krok 5: Vytvořte prvek obrysu

 Vytvořit`OutlineElement` k přidržení obrázku a určení jeho polohy.

```java
OutlineElement outlineElem1 = new OutlineElement();
```

## Krok 6: Načtěte tok obrázků

 Načtěte obrazový tok pomocí`FileInputStream` pro požadovaný obrázek.

```java
InputStream fs = null;
try {
    fs = new FileInputStream(dataDir + "image.jpg");
} catch (FileNotFoundException e) {
    e.printStackTrace();
}
```

## Krok 7: Vložte obrázek

 Vložte obrázek do dokumentu vytvořením souboru`Image` objektu a nastavení jeho zarovnání.

```java
Image image = new Image(null, dataDir + "image1.jpg");
image.setAlignment(HorizontalAlignment.Right);
```

## Krok 8: Připojte obrázek k prvku obrysu

Připojte obrázek k prvku obrysu.

```java
outlineElem1.appendChildLast(image);
```

## Krok 9: Připojte prvek obrysu k obrysu

Přidejte prvek obrysu k obrysu.

```java
outline1.appendChildLast(outlineElem1);
```

## Krok 10: Připojte obrys na stránku

Přidejte obrys na stránku.

```java
page.appendChildLast(outline1);
```

## Krok 11: Připojte stránku k dokumentu

Nakonec připojte stránku k dokumentu.

```java
doc.appendChildLast(page);
```

## Krok 12: Uložte dokument

Uložte upravený dokument s uvedením požadovaného formátu (např. PDF).

```java
try {
    doc.save("D://Aspose_JavaProjects//OneNote//out3.pdf", SaveFormat.Pdf);
} catch (IOException e) {
    e.printStackTrace();
}
```

Podle těchto kroků můžete bez námahy vytvářet dokumenty a vkládat obrázky pomocí proudů obrázků ve OneNotu pomocí Aspose.Note for Java.

## Závěr

Závěrem lze říci, že zvládnutí integrace obrázků do vašich dokumentů OneNote pomocí Java může výrazně zlepšit váš proces vytváření dokumentů. S Aspose.Note pro Java máte k dispozici výkonný nástroj, který tento úkol bezproblémově provede.

## FAQ

### Q1: Je Aspose.Note for Java kompatibilní se všemi verzemi OneNotu?

Odpověď 1: Aspose.Note for Java podporuje různé verze OneNotu, což zajišťuje kompatibilitu v různých prostředích.

### Q2: Mohu upravit vzhled vložených obrázků v dokumentech OneNotu pomocí Aspose.Note pro Java?

Odpověď 2: Ano, můžete přizpůsobit různé aspekty vložených obrázků, jako je zarovnání, velikost a orientace, aby vyhovovaly vašim konkrétním požadavkům.

### Q3: Poskytuje Aspose.Note for Java podporu pro jiné formáty dokumentů kromě PDF?

Odpověď 3: Ano, Aspose.Note for Java podporuje širokou škálu formátů dokumentů, včetně DOCX, HTML a dalších, což vám poskytuje flexibilitu při úkolech správy dokumentů.

### Q4: Kde najdu další zdroje a podporu pro Aspose.Note pro Java?

Odpověď 4: Prostřednictvím uvedených odkazů můžete přistupovat k dokumentaci, odkazům ke stažení, fórům podpory a dočasným licencím pro Aspose.Note pro Java.

### Q5: Je k dispozici zkušební verze pro Aspose.Note pro Java?

Odpověď 5: Ano, můžete získat bezplatnou zkušební verzi Aspose.Note pro Java, abyste prozkoumali její funkce a možnosti před rozhodnutím o nákupu.
