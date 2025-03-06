---
title: Přidat nový uzel obrázku se značkou ve OneNotu – Aspose.Note
linktitle: Přidat nový uzel obrázku se značkou ve OneNotu – Aspose.Note
second_title: Aspose.Note Java API
description: Přečtěte si, jak přidat nový uzel obrázku se značkou ve OneNotu pomocí Aspose.Note pro Java. Zvyšte své znalosti programování v Javě bez námahy.
weight: 10
url: /cs/java/onenote-tag-operations/add-new-image-node-with-tag/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Přidat nový uzel obrázku se značkou ve OneNotu – Aspose.Note

## Úvod
oblasti programování Java vyniká Aspose.Note jako výkonný nástroj pro snadnou manipulaci s dokumenty OneNote. Pokud chcete zlepšit své dovednosti a naučit se přidat nový uzel obrázku se značkou ve OneNotu pomocí Aspose.Note, jste na správném místě. Tento průvodce vás krok za krokem provede celým procesem a zajistí, že důkladně pochopíte každý koncept.
## Předpoklady
Než se vrhneme na tutoriál, ujistěte se, že máte vše, co potřebujete:
1.  Aspose.Note pro Java: Ujistěte se, že máte nainstalovanou knihovnu Aspose.Note. Pokud ne, můžete si jej stáhnout[tady](https://releases.aspose.com/note/java/).
2. Vývojové prostředí Java: Ujistěte se, že máte na svém počítači nastavené funkční vývojové prostředí Java.
Nyní, když máme připravené předpoklady, přejděme k dalším krokům.
## Importujte balíčky
Ve svém projektu Java začněte importováním potřebných balíčků:
```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.Image;
import com.aspose.note.NoteTag;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.SaveFormat;
import com.aspose.note.TagIcon;
```
## Krok 1: Vytvořte objekt dokumentu
```java
// Cesta k adresáři dokumentů.
String dataDir = "Your Document Directory";
// vytvořit objekt třídy Document
Document doc = new Document();
```
## Krok 2: Inicializujte objekt třídy stránky
```java
// inicializovat objekt třídy Page
Page page = new Page();
```
## Krok 3: Inicializujte objekt třídy osnovy
```java
// inicializovat objekt třídy Outline
Outline outline = new Outline();
```
## Krok 4: Inicializujte objekt třídy OutlineElement
```java
// inicializovat objekt třídy OutlineElement
OutlineElement outlineElem = new OutlineElement();
```
## Krok 5: Načtěte a vložte obrázek
```java
// načíst obrázek
Image image = new Image(null, dataDir + "Input.jpg");
// vložit obrázek do uzlu dokumentu
outlineElem.appendChildLast(image);
```
## Krok 6: Přidejte poznámkový štítek k obrázku
```java
// přidejte k obrázku značku poznámky se žlutou hvězdou
NoteTag noteTag = NoteTag.createYellowStar();
image.getTags().add(noteTag);
```
## Krok 7: Přidejte uzel prvku obrysu
```java
// přidat uzel prvku obrysu
outline.appendChildLast(outlineElem);
```
## Krok 8: Přidejte uzel obrysu
```java
// přidat obrysový uzel
page.appendChildLast(outline);
```
## Krok 9: Přidejte uzel stránky
```java
// přidat uzel stránky
doc.appendChildLast(page);
```
## Krok 10: Uložte dokument OneNotu
```java
// uložit dokument OneNotu jako PDF
doc.save(dataDir + "AddNewImageNodeWithTag_out.pdf", SaveFormat.Pdf);
```
Gratulujeme! Úspěšně jste přidali nový uzel obrázku se značkou ve OneNotu pomocí Aspose.Note pro Java.
## Závěr
 Zvládnutí Aspose.Note pro Java otevírá úžasné možnosti v manipulaci s dokumenty OneNote. Sledováním tohoto návodu jste získali praktickou dovednost, kterou lze aplikovat na různé projekty. Pokračujte v prozkoumávání dokumentace Aspose.Note[tady](https://reference.aspose.com/note/java/)pro pokročilejší funkce a možnosti.
## Nejčastější dotazy
### Kde najdu dokumentaci Aspose.Note?
 Dokumentaci najdete[tady](https://reference.aspose.com/note/java/).
### Jak si stáhnu Aspose.Note pro Javu?
 Můžete si jej stáhnout ze stránky vydání[tady](https://releases.aspose.com/note/java/).
### Je k dispozici bezplatná zkušební verze?
 Ano, máte přístup k bezplatné zkušební verzi[tady](https://releases.aspose.com/).
### Kde mohu získat podporu pro Aspose.Note?
 Navštivte komunitní fórum[tady](https://forum.aspose.com/c/note/28) pro podporu.
### Potřebuji dočasnou licenci?
 V případě potřeby můžete získat dočasnou licenci[tady](https://purchase.aspose.com/temporary-license/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
