---
title: Zárolt oszlopokat tartalmazó táblázat létrehozása a OneNote-ban – Aspose.Note
linktitle: Zárolt oszlopokat tartalmazó táblázat létrehozása a OneNote-ban – Aspose.Note
second_title: Aspose.Note Java API
description: Növelje OneNote-élményét az Aspose.Note for Java segítségével. A lépésenkénti útmutató segítségével megtudhatja, hogyan hozhat létre zárolt oszlopokat tartalmazó táblázatokat. Töltse le ingyenes próbaverzióját most!
weight: 12
url: /hu/java/onenote-table-manipulation/create-table-with-locked-columns/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Zárolt oszlopokat tartalmazó táblázat létrehozása a OneNote-ban – Aspose.Note

## Bevezetés
A OneNote egy hatékony eszköz az információk rendszerezésére, és az Aspose.Note for Java továbbfejleszti képességeit azáltal, hogy zökkenőmentesen hozhat létre zárolt oszlopokat tartalmazó táblázatokat. Ebben az oktatóanyagban végigvezetjük az Aspose.Note for Java használatával a OneNote-ban zárolt oszlopokat tartalmazó táblázat létrehozásához.
## Előfeltételek
Mielőtt elkezdené, győződjön meg arról, hogy a következő előfeltételeket teljesítette:
- [Java fejlesztőkészlet (JDK)](https://www.oracle.com/java/technologies/javase-downloads.html)telepítve van a gépedre.
- [Aspose.Note a Java számára](https://downloads.aspose.com/note/java) könyvtár letöltve és hozzáadva a projekthez.
## Csomagok importálása
Java-projektjében importálja az Aspose-val való munkához szükséges csomagokat.Megjegyzés:
```java
import com.aspose.note.*;
import java.io.IOException;
```
## 1. lépés: Állítsa be projektjét
Kezdje azzal, hogy hozzon létre egy új Java-projektet, és adja hozzá az Aspose.Note könyvtárat az osztályútvonalhoz. Győződjön meg arról, hogy projektje a JDK használatára van konfigurálva.
## 2. lépés: Inicializálja a dokumentum- és oldalobjektumokat
```java
// A dokumentumok könyvtárának elérési útja.
String dataDir = "Your Document Directory";
//Hozzon létre egy objektumot a Dokumentum osztályból
Document doc = new Document();
// Oldal osztály objektum inicializálása
Page page = new Page();
```
## 3. lépés: Hozzon létre táblázatsorokat és cellákat
```java
// Inicializálja a TableRow osztályobjektumot
TableRow row1 = new TableRow();
// Inicializálja a TableCell osztály objektumot és állítsa be a szöveges tartalmat
TableCell cell11 = new TableCell();
cell11.appendChildLast(InsertTable.GetOutlineElementWithText("Small text"));
row1.appendChildLast(cell11);
// Inicializálja a TableRow osztályobjektumot
TableRow row2 = new TableRow();
// Inicializálja a TableCell osztály objektumot és állítsa be a szöveges tartalmat
TableCell cell21 = new TableCell();
cell21.appendChildLast(InsertTable.GetOutlineElementWithText("Long   text    with    several   words and    spaces."));
row2.appendChildLast(cell21);
```
## 4. lépés: A táblázat létrehozása és testreszabása
```java
// Inicializálja a Table osztály objektumot
Table table = new Table();
table.setBordersVisible(true);
TableColumn col = new TableColumn();
col.setWidth(200);
col.setLockedWidth(true);
table.getColumns().addItem(col);
// Sorok hozzáadása
table.appendChildLast(row1);
table.appendChildLast(row2);
```
## 5. lépés: Adjon hozzá táblázatot a vázlathoz és az oldalhoz
```java
Outline outline = new Outline();
OutlineElement outlineElem = new OutlineElement();
// Táblázat csomópont hozzáadása
outlineElem.appendChildLast(table);
// Vázlatelem csomópont hozzáadása
outline.appendChildLast(outlineElem);
// Vázlat csomópont hozzáadása
page.appendChildLast(outline);
// Oldalcsomópont hozzáadása
doc.appendChildLast(page);
```
## 6. lépés: Mentse el a dokumentumot
```java
dataDir = dataDir + "CreateTableWithLockedColumns_out.one";
doc.save(dataDir);
```
Gratulálunk! Sikeresen létrehozott egy táblázatot zárolt oszlopokkal a OneNote-ban az Aspose.Note for Java használatával.
## Következtetés
Ebben az oktatóanyagban megvizsgáltuk az Aspose.Note for Java használatának folyamatát, hogy javítsa a OneNote-élményt azáltal, hogy zárolt oszlopokat tartalmazó táblázatokat hoz létre. Ez a funkció új rendszerezési és szerkezeti réteget ad a jegyzetekhez.
## GYIK
### Az Aspose.Note for Java kompatibilis az összes Java-verzióval?
Igen, az Aspose.Note for Java kompatibilis a Java 6 és újabb verzióival.
### Testreszabhatom a táblázat megjelenését?
Teljesen! Az Aspose.Note for Java kiterjedt lehetőségeket kínál a táblázatok testreszabásához, például a szegélyek, a cellaközök és egyebek beállításához.
### Vásárlás előtt van próbaverzió?
 Igen tudsz[ingyenes próbaverzió letöltése](https://releases.aspose.com/) hogy feltárja az Aspose.Note for Java képességeit.
### Hol találhatok további támogatást vagy közösségi beszélgetéseket?
 Meglátogatni a[Aspose.Note fórum](https://forum.aspose.com/c/note/28) támogatásra és közösségi megbeszélésekre.
### Hogyan szerezhetek ideiglenes licencet az Aspose.Note for Java számára?
 Látogatás[ez a link](https://purchase.aspose.com/temporary-license/) tesztelési célból ideiglenes engedélyt szerezni.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
