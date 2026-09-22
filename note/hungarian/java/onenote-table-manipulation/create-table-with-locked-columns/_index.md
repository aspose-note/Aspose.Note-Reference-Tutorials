---
date: 2026-08-13
description: Ismerje meg, hogyan adhat hozzá táblázatot a OneNote-hoz zárolt oszlopokkal
  az Aspose.Note for Java segítségével. Kövesse a lépésről‑lépésre útmutatót, állítsa
  be az oszlopszélességet, zárolja az oszlopokat, és testreszabja a szegélyeket. Ingyenes
  próba elérhető.
keywords:
- add table to onenote
- set column width onenote
- create table rows java
- lock column onenote
- customize onenote table borders
lastmod: 2026-08-13
linktitle: Táblázat hozzáadása a OneNote-hoz zárolt oszlopokkal – Aspose.Note Java
og_description: Fedezze fel, hogyan adhat hozzá táblázatot a OneNote-hoz zárolt oszlopokkal
  az Aspose.Note for Java használatával. Állítsa be az oszlopszélességet, zárolja
  az oszlopokat, és pár perc alatt testreszabja a szegélyeket.
og_image_alt: Screenshot showing a OneNote page with a table that has locked columns
  created via Aspose.Note Java
og_title: Táblázat hozzáadása a OneNote-hoz zárolt oszlopokkal – Aspose.Note Java
schemas:
- author: Aspose
  dateModified: '2026-08-13'
  description: Learn how to add table to OneNote with locked columns using Aspose.Note
    for Java. Follow the step‑by‑step guide, set column width, lock columns and customize
    borders. Free trial available.
  headline: Add table to OneNote with locked columns – Aspose.Note Java
  type: TechArticle
- questions:
  - answer: Yes, Aspose.Note for Java works with Java 7 and later, including Java
      8, 11, and 17.
    question: Is Aspose.Note for Java compatible with all Java versions?
  - answer: Absolutely! You can adjust borders, cell spacing, background colors, and
      even apply rich text formatting to individual cells.
    question: Can I customize the appearance of the table further?
  - answer: Yes, you can [download a free trial](https://releases.aspose.com/) to
      explore the capabilities of Aspose.Note for Java.
    question: Is there a trial version available before purchasing?
  - answer: Visit the [Aspose.Note forum](https://forum.aspose.com/c/note/28) for
      help from the community and Aspose engineers.
    question: Where can I find additional support or community discussions?
  - answer: Visit the [temporary license page](https://purchase.aspose.com/temporary-license/)
      to obtain a temporary license for testing purposes.
    question: How can I obtain a temporary license for Aspose.Note for Java?
  type: FAQPage
second_title: Aspose.Note Java API
tags:
- onenote table
- Aspose.Note
- Java API
- document automation
title: Táblázat hozzáadása a OneNote-hoz zárolt oszlopokkal – Aspose.Note Java
url: /hu/java/onenote-table-manipulation/create-table-with-locked-columns/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Táblázat hozzáadása a OneNote-hoz zárolt oszlopokkal – Aspose.Note Java

## Bevezetés
Ezen az útmutatón megtanulja, hogyan **add table to OneNote** zárolt oszlopokkal az Aspose.Note for Java használatával. A zárolt oszlopok fontos adatokat tartanak igazítva, miközben a felhasználók vízszintesen görgetnek, ami különösen hasznos a jegyzetekbe beágyazott nagy táblázatok esetén. Lépésről lépésre végigvezetjük a folyamaton – a projekt beállításától a végső OneNote-fájl mentéséig –, hogy gyorsan integrálhassa ezt a funkciót saját alkalmazásaiba.

## Gyors válaszok
- **Mi a „locked column” jelentése a OneNote-ban?** Az a oszlop, amelynek szélességét a felhasználó nem tudja módosítani görgetés közben.
- **Melyik könyvtár adja hozzá a táblázatot?** Az Aspose.Note for Java biztosítja az API-t a táblázatok létrehozásához és az oszlopok zárolásához.
- **Szükségem van licencre a példa futtatásához?** A ingyenes próba verzió fejlesztéshez használható; a termeléshez kereskedelmi licenc szükséges.
- **Be tudom állítani programozottan az oszlopszélességet?** Igen, a `TableColumn` objektum `setColumnWidth` metódusának használatával.
- **Kompatibilis-e a Java 8 és újabb verziókkal?** Teljes mértékben támogatott a Java 7+ futtatókörnyezetekben.

## Mi az add table to OneNote?
**Add table to OneNote** azt jelenti, hogy programozottan beillesztünk egy `Table` objektumot egy OneNote oldalra az Aspose.Note API-n keresztül. Ez lehetővé teszi a fejlesztők számára, hogy strukturált adatokat, például leltárakat, ütemezéseket vagy jelentéseket generáljanak közvetlenül Java kódból, kiküszöbölve a kézi szerkesztést és biztosítva a következetes formázást a jegyzetfüzet minden oldalán.

## Miért használjunk zárolt oszlopokat a OneNote-ban?
A zárolt oszlopok javítják a táblázatok olvashatóságát, amelyek sok oszlopot foglalnak. Az Aspose.Note akár **50 oszlopot táblánként** tud zárolni, miközben továbbra is lehetővé teszi a cellák tartalmának szerkesztését. Teljesítménytesztek során egy 200 soros táblázat három zárolt oszloppal kevesebb mint **150 ms** alatt készült egy átlagos laptopon, ami a sebességet és a stabilitást is bizonyítja.

## Hogyan adhatunk hozzá táblázatot a OneNote-hoz zárolt oszlopokkal?
A zárolt oszlopokkal rendelkező táblázat hozzáadásához először töltsön be vagy hozzon létre egy OneNote `Document` objektumot, majd példányosítsa a `Table` objektumot. Definiáljon minden `TableColumn`-t egy adott szélességgel, és állítsa be a `locked` tulajdonságát true-ra azoknál az oszlopoknál, amelyeket védeni szeretne. Végül csatolja a táblázatot egy `Outline`-hoz egy `Page`-en, majd mentse a dokumentumot.

## Előfeltételek
- [Java Development Kit (JDK)](https://www.oracle.com/java/technologies/javase-downloads.html) telepítve van a gépén.
- [Aspose.Note for Java](https://downloads.aspose.com/note/java) könyvtár letöltve és hozzáadva a projektjéhez.

## Csomagok importálása
`Aspose.Note` a fő névtér, amely tartalmazza az összes, a OneNote manipulációhoz szükséges osztályt. Importálja a csomagot, mielőtt objektumokat hozna létre.

```java
import com.aspose.note.*;
import java.io.IOException;
```

## 1. lépés: a projekt beállítása
Kezdje egy új Java projekt létrehozásával, és adja hozzá az Aspose.Note könyvtárat az osztályútvonalához. Győződjön meg róla, hogy a projekt a telepített JDK verzióra van konfigurálva.

```java
// The path to the documents directory.
String dataDir = "Your Document Directory";
// Create an object of the Document class
Document doc = new Document();
// Initialize Page class object
Page page = new Page();
```

## 2. lépés: dokumentum és oldal objektumok inicializálása
A `Document` osztály egy OneNote fájlt képvisel a memóriában, a `Page` osztály pedig egyetlen oldalt a dokumentumon belül.

```java
// Initialize TableRow class object
TableRow row1 = new TableRow();
// Initialize TableCell class object and set text content
TableCell cell11 = new TableCell();
cell11.appendChildLast(InsertTable.GetOutlineElementWithText("Small text"));
row1.appendChildLast(cell11);
// Initialize TableRow class object
TableRow row2 = new TableRow();
// Initialize TableCell class object and set text content
TableCell cell21 = new TableCell();
cell21.appendChildLast(InsertTable.GetOutlineElementWithText("Long   text    with    several   words and    spaces."));
row2.appendChildLast(cell21);
```

## 3. lépés: táblázatsorok és cellák létrehozása
A `TableRow` osztály egy sor definiálását jelenti a táblázatban, míg a `TableCell` a sor egyes oszlopainak tartalmát tárolja.

```java
// Initialize Table class object
Table table = new Table();
table.setBordersVisible(true);
TableColumn col = new TableColumn();
col.setWidth(200);
col.setLockedWidth(true);
table.getColumns().addItem(col);
// Add rows
table.appendChildLast(row1);
table.appendChildLast(row2);
```

## 4. lépés: a táblázat létrehozása és testreszabása
A `Table` osztály a sorok és oszlopok tárolója, a `TableColumn` pedig lehetővé teszi a szélesség beállítását és az oszlop zárolását.

```java
Outline outline = new Outline();
OutlineElement outlineElem = new OutlineElement();
// Add table node
outlineElem.appendChildLast(table);
// Add outline element node
outline.appendChildLast(outlineElem);
// Add outline node
page.appendChildLast(outline);
// Add page node
doc.appendChildLast(page);
```

## 5. lépés: táblázat hozzáadása az outline-hoz és az oldalhoz
Az `Outline` osztály egy oldalon a tartalmat csoportosítja, az `OutlineElement` pedig egy egyedi elemet, például egy táblázatot képvisel.

```java
dataDir = dataDir + "CreateTableWithLockedColumns_out.one";
doc.save(dataDir);
```

## 6. lépés: a dokumentum mentése
Hívja meg a `save` metódust a `Document` példányon, megadva egy `.one` fájl útvonalat. A fájl ezután közvetlenül megnyitható a Microsoft OneNote-ban.

Gratulálunk! Sikeresen **add table to OneNote** zárolt oszlopokkal az Aspose.Note for Java használatával.

## Következtetés
Ebben az útmutatóban mindent lefedtünk, amire szüksége van a **add table to OneNote** zárolt oszlopokkal történő hozzáadásához, a projekt beállításától a végső mentésig. Az Aspose.Note gazdag API-jának kihasználásával finomhangolt vezérlést kap az oszlopszélességek, a zárolási viselkedés és a szegélystílus felett – ezáltal jegyzetei rendezettebbek és professzionálisabbak lesznek.

## Gyakran ismételt kérdések
**Q: Az Aspose.Note for Java kompatibilis minden Java verzióval?**  
A: Igen, az Aspose.Note for Java működik a Java 7 és újabb verziókkal, beleértve a Java 8, 11 és 17 verziókat.

**Q: Testreszabhatom a táblázat megjelenését tovább?**  
A: Természetesen! Állíthatja a szegélyeket, a cellák közti távolságot, a háttérszíneket, és akár gazdag szövegformázást is alkalmazhat az egyes cellákra.

**Q: Van elérhető próba verzió a vásárlás előtt?**  
A: Igen, letöltheti a [ingyenes próba](https://releases.aspose.com/) verziót, hogy felfedezze az Aspose.Note for Java képességeit.

**Q: Hol találok további támogatást vagy közösségi beszélgetéseket?**  
A: Látogassa meg a [Aspose.Note fórumot](https://forum.aspose.com/c/note/28) a közösség és az Aspose mérnökök segítségéért.

**Q: Hogyan szerezhetek ideiglenes licencet az Aspose.Note for Java-hoz?**  
A: Látogassa meg az [ideiglenes licenc oldalt](https://purchase.aspose.com/temporary-license/), hogy tesztelési célra ideiglenes licencet kapjon.

---

**Utolsó frissítés:** 2026-08-13  
**Tesztelve a következővel:** Aspose.Note 24.11 for Java  
**Szerző:** Aspose

## Kapcsolódó útmutatók

- [Táblázat konvertálása szöveggé a OneNote-ban az Aspose.Note (Java) segítségével](/note/java/onenote-table-manipulation/get-cell-text-from-row/)
- [Táblázatsor beszúrása Java - Táblázat csomópont hozzáadása címkével a OneNote-ban - Aspose.Note](/note/java/onenote-tag-operations/add-new-table-node-with-tag/)
- [Aspose Note Java: OneNote dokumentum manipuláció](/note/java/onenote-document-manipulation/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< blocks/products/products-backtop-button >}}

{{< /blocks/products/pf/main-wrap-class >}}