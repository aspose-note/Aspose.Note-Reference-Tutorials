---
title: Vytvořit tabulku s uzamčenými sloupci ve OneNotu – Aspose.Note
linktitle: Vytvořit tabulku s uzamčenými sloupci ve OneNotu – Aspose.Note
second_title: Aspose.Note Java API
description: Vylepšete své prostředí OneNote pomocí Aspose.Note pro Java. Naučte se vytvářet tabulky se zamčenými sloupci pomocí podrobného průvodce. Stáhněte si bezplatnou zkušební verzi nyní!
weight: 12
url: /cs/java/onenote-table-manipulation/create-table-with-locked-columns/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Vytvořit tabulku s uzamčenými sloupci ve OneNotu – Aspose.Note

## Úvod
OneNote je výkonný nástroj pro organizaci informací a Aspose.Note pro Java vylepšuje jeho možnosti tím, že poskytuje bezproblémový způsob vytváření tabulek se zamčenými sloupci. V tomto tutoriálu vás provedeme procesem použití Aspose.Note pro Java k vytvoření tabulky se zamčenými sloupci ve OneNotu.
## Předpoklady
Než začnete, ujistěte se, že máte splněny následující předpoklady:
- [Java Development Kit (JDK)](https://www.oracle.com/java/technologies/javase-downloads.html)nainstalovaný na vašem počítači.
- [Aspose.Poznámka pro Javu](https://downloads.aspose.com/note/java) knihovnu staženou a přidanou do vašeho projektu.
## Importujte balíčky
Do svého projektu Java importujte potřebné balíčky pro práci s Aspose. Poznámka:
```java
import com.aspose.note.*;
import java.io.IOException;
```
## Krok 1: Nastavte svůj projekt
Začněte vytvořením nového projektu Java a přidáním knihovny Aspose.Note do vaší třídy. Ujistěte se, že je váš projekt nakonfigurován pro použití sady JDK.
## Krok 2: Inicializujte objekty dokumentu a stránky
```java
// Cesta k adresáři dokumentů.
String dataDir = "Your Document Directory";
//Vytvořte objekt třídy Document
Document doc = new Document();
// Inicializujte objekt třídy Page
Page page = new Page();
```
## Krok 3: Vytvořte řádky a buňky tabulky
```java
// Inicializujte objekt třídy TableRow
TableRow row1 = new TableRow();
// Inicializujte objekt třídy TableCell a nastavte obsah textu
TableCell cell11 = new TableCell();
cell11.appendChildLast(InsertTable.GetOutlineElementWithText("Small text"));
row1.appendChildLast(cell11);
// Inicializujte objekt třídy TableRow
TableRow row2 = new TableRow();
// Inicializujte objekt třídy TableCell a nastavte obsah textu
TableCell cell21 = new TableCell();
cell21.appendChildLast(InsertTable.GetOutlineElementWithText("Long   text    with    several   words and    spaces."));
row2.appendChildLast(cell21);
```
## Krok 4: Vytvořte a přizpůsobte tabulku
```java
// Inicializovat objekt třídy Table
Table table = new Table();
table.setBordersVisible(true);
TableColumn col = new TableColumn();
col.setWidth(200);
col.setLockedWidth(true);
table.getColumns().addItem(col);
// Přidat řádky
table.appendChildLast(row1);
table.appendChildLast(row2);
```
## Krok 5: Přidejte tabulku do osnovy a stránky
```java
Outline outline = new Outline();
OutlineElement outlineElem = new OutlineElement();
// Přidat uzel tabulky
outlineElem.appendChildLast(table);
// Přidejte uzel prvku obrysu
outline.appendChildLast(outlineElem);
// Přidat obrysový uzel
page.appendChildLast(outline);
// Přidat uzel stránky
doc.appendChildLast(page);
```
## Krok 6: Uložte dokument
```java
dataDir = dataDir + "CreateTableWithLockedColumns_out.one";
doc.save(dataDir);
```
Gratulujeme! Úspěšně jste vytvořili tabulku se zamčenými sloupci ve OneNotu pomocí Aspose.Note pro Java.
## Závěr
tomto tutoriálu jsme prozkoumali proces využití Aspose.Note pro Javu k vylepšení vašeho prostředí OneNote vytvářením tabulek se zamčenými sloupci. Tato funkce přidává vašim poznámkám novou úroveň organizace a struktury.
## Nejčastější dotazy
### Je Aspose.Note for Java kompatibilní se všemi verzemi Java?
Ano, Aspose.Note for Java je kompatibilní s Java 6 a novějšími verzemi.
### Mohu si vzhled stolu dále upravit?
Absolutně! Aspose.Note for Java poskytuje rozsáhlé možnosti přizpůsobení tabulek, jako je úprava ohraničení, mezer mezi buňkami a další.
### Je před zakoupením k dispozici zkušební verze?
 Ano můžeš[stáhnout zkušební verzi zdarma](https://releases.aspose.com/) prozkoumat možnosti Aspose.Note pro Javu.
### Kde najdu další podporu nebo komunitní diskuse?
 Navštivte[Aspose.Note fórum](https://forum.aspose.com/c/note/28) za podporu a komunitní diskuse.
### Jak mohu získat dočasnou licenci pro Aspose.Note pro Java?
 Návštěva[tento odkaz](https://purchase.aspose.com/temporary-license/) získat dočasnou licenci pro testovací účely.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
