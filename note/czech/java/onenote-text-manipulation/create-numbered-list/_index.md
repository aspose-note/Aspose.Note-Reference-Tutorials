---
title: Vytvořit číslovaný seznam ve OneNotu - Aspose.Note
linktitle: Vytvořit číslovaný seznam ve OneNotu - Aspose.Note
second_title: Aspose.Note Java API
description: Naučte se, jak snadno vytvořit číslovaný seznam ve OneNotu pomocí Aspose.Note pro Java. Stáhněte si bezplatnou zkušební verzi a ponořte se do světa vývoje Java!
type: docs
weight: 14
url: /cs/java/onenote-text-manipulation/create-numbered-list/
---
## Úvod
Aspose.Note for Java umožňuje vývojářům Java hladce pracovat se soubory Microsoft OneNote. V tomto tutoriálu vás provedeme procesem vytváření číslovaného seznamu ve OneNotu pomocí výkonné knihovny Aspose.Note pro Java.
## Předpoklady
Než se pustíte do výukového programu, ujistěte se, že jsou splněny následující předpoklady:
- Na vašem počítači je nainstalována sada Java Development Kit (JDK).
-  Aspose.Note pro knihovnu Java staženou z[tady](https://releases.aspose.com/note/java/).
## Import balíčků
Nejprve importujme potřebné balíčky do vašeho projektu Java, abyste co nejlépe využili funkce Aspose.Note. Zahrňte do svého projektu následující kód:
```java
import java.awt.Color;
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.NumberFormat;
import com.aspose.note.NumberList;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.ParagraphStyle;
```
## Krok 1: Inicializace objektů dokumentu, stránky a osnovy
```java
// Váš adresář dokumentů
String dataDir = "Your Document Directory";
// Vytvářejte objekty Dokument, Stránka a Osnova
Document doc = new Document();
Page page = new Page();
Outline outline = new Outline();
// Nastavit výchozí styl textu
ParagraphStyle defaultStyle = new ParagraphStyle()
                                        .setFontColor(Color.black)
                                        .setFontName("Arial")
                                        .setFontSize(10);
Document doc = new Document();
Page page = new Page();
Outline outline = new Outline();
```
## Krok 2: Nastavení výchozího stylu textu
```java
ParagraphStyle defaultStyle = new ParagraphStyle()
                                        .setFontColor(Color.black)
                                        .setFontName("Arial")
                                        .setFontSize(10);
```
## Krok 3: Vytvoření prvků osnovy
Nyní vytvoříme prvky pro váš číslovaný seznam.
```java
OutlineElement outlineElem1 = new OutlineElement();
outlineElem1.setNumberList(new NumberList("{0})", NumberFormat.DecimalNumbers, "Arial", 10));
RichText text1 = new RichText().append("First");
text1.setParagraphStyle(defaultStyle);
outlineElem1.appendChildLast(text1);
// Opakujte pro další prvky (outlineElem2 a outlineElem3)
```
## Krok 4: Přidání prvků osnovy do osnovy
```java
outline.appendChildLast(outlineElem1);
outline.appendChildLast(outlineElem2);
outline.appendChildLast(outlineElem3);
```
## Krok 5: Přidání osnovy na stránku
```java
page.appendChildLast(outline);
```
## Krok 6: Uložení dokumentu
```java
doc.appendChildLast(page);
doc.save(dataDir + "CreateNumberedList_out.pdf");
System.out.printf("File saved: %s\n", dataDir + "CreateNumberedList_out.pdf");
```
Postupujte pečlivě podle těchto kroků a bez námahy vytvoříte číslovaný seznam ve OneNotu pomocí Aspose.Note pro Java.
## Závěr
tomto tutoriálu jsme prozkoumali bezproblémový proces vytváření číslovaného seznamu ve OneNotu pomocí Aspose.Note pro Java. Robustní funkce knihovny z ní činí neocenitelný nástroj pro vývojáře v jazyce Java pracující se soubory Microsoft OneNote.
## Často kladené otázky
### Otázka: Mohu přizpůsobit formát číslování v seznamu OneNotu?
A: Rozhodně! Formát číslování můžete přizpůsobit pomocí třídy NumberList poskytované Aspose.Note pro Java.
### Otázka: Je k dispozici zkušební verze pro Aspose.Note pro Javu?
 Odpověď: Ano, můžete si stáhnout bezplatnou zkušební verzi[tady](https://releases.aspose.com/).
### Otázka: Jak mohu získat podporu pro Aspose.Note pro Java?
 A: Navštivte[Aspose.Note for Java forum](https://forum.aspose.com/c/note/28) za podporu komunity.
### Otázka: Kde najdu podrobnou dokumentaci k Aspose.Note pro Javu?
 A: Viz[dokumentace](https://reference.aspose.com/note/java/) pro komplexní informace.
### Otázka: Jak si koupím licenci pro Aspose.Note pro Java?
 A: Můžete si koupit licenci[tady](https://purchase.aspose.com/buy).