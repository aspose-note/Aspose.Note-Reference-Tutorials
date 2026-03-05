---
date: 2026-03-05
description: Ismerje meg, hogyan menthet OneNote-ot PDF formátumban, miközben számozott
  listát hoz létre az Aspose.Note for Java segítségével. Tartalmazza az alapértelmezett
  szövegstílus beállításának és a számozás testreszabásának lépéseit.
linktitle: Save OneNote as PDF – Create Numbered List with Aspose.Note
second_title: Aspose.Note Java API
title: OneNote mentése PDF‑ként – Számozott lista létrehozása az Aspose.Note segítségével
url: /hu/java/onenote-text-manipulation/create-numbered-list/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote mentése PDF‑ként – Számozott lista létrehozása az Aspose.Note segítségével

## Bevezetés
Az Aspose.Note for Java felhatalmazza a Java fejlesztőket, hogy **OneNote‑t PDF‑ként mentse** és gazdagítsa a dokumentumot fejlett formázással, például számozott listákkal. Ebben az útmutatóban végigvezetjük a teljes folyamaton – az alapértelmezett szövegstílus beállításától a számozási formátum testreszabásáig – hogy professzionális megjelenésű PDF‑be exportálhassa a OneNote‑t.

## Gyors válaszok
- **Miről szól ez az útmutató?** Számozott lista létrehozása a OneNote‑ban és a fájl PDF‑ként mentése az Aspose.Note for Java használatával.  
- **Melyik elsődleges kulcsszót célozza?** *save onenote as pdf*  
- **Szükségem van licencre?** Elérhető egy ingyenes próba, a kereskedelmi licenc a termeléshez kötelező.  
- **Milyen Java verzió szükséges?** JDK 8 vagy újabb.  
- **Mennyi időt vesz igénybe a megvalósítás?** Körülbelül 10–15 perc egy alaplista esetén.

## Mi az a „OneNote mentése PDF‑ként”?
A OneNote PDF‑ként mentése a gazdag szöveges OneNote‑oldalt egy hordozható, rögzített elrendezésű dokumentummá alakítja, amely platformok között megosztható OneNote telepítése nélkül. Ez különösen hasznos archiváláshoz, jelentéskészítéshez vagy tartalom terjesztéséhez olyan felhasználók számára, akiknek nincs telepítve a OneNote.

## Miért érdemes számozott listát létrehozni exportálás előtt?
A számozott lista struktúrát és olvashatóságot ad, így az exportált PDF egy kifinomult jelentésnek tűnik. Az Aspose.Note segítségével **testreszabhatja a számozási formátumot**, beállíthat betűtípusokat és szabályozhatja a távolságokat – mindezt az eredeti OneNote‑elrendezés megőrzésével.

## Előfeltételek
- Java Development Kit (JDK) telepítve a gépén.  
- Aspose.Note for Java library downloaded from [here](https://releases.aspose.com/note/java/).  

## Csomagok importálása
Először importálja a szükséges osztályokat, hogy a OneNote objektumokkal és a PDF konverzióval dolgozhasson.

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

## Hogyan mentse a OneNote‑t PDF‑ként számozott listával?
Az alábbi lépésről‑lépésre útmutató bemutatja, hogyan **hozzon létre lista** elemeket, **állítson be alapértelmezett szövegstílust**, és végül **exportálja a OneNote‑t PDF‑be**.

### 1. lépés: Dokumentum, oldal és vázlat objektumok inicializálása
Először létrehozzuk a OneNote alapvető struktúráit. Ez emellett bemutatja a **add outline element java** használatát.

```java
// Your Document Directory
String dataDir = "Your Document Directory";
// Create Document, Page, and Outline objects
Document doc = new Document();
Page page = new Page();
Outline outline = new Outline();
// Set default text style
ParagraphStyle defaultStyle = new ParagraphStyle()
                                        .setFontColor(Color.black)
                                        .setFontName("Arial")
                                        .setFontSize(10);
Document doc = new Document();
Page page = new Page();
Outline outline = new Outline();
```

> **Pro tipp:** Tartsa a `dataDir` útvonalat abszolútként, vagy használja a `System.getProperty("user.dir")`‑t az útvonalproblémák elkerülése érdekében.

### 2. lépés: Alapértelmezett szövegstílus beállítása
```java
ParagraphStyle defaultStyle = new ParagraphStyle()
                                        .setFontColor(Color.black)
                                        .setFontName("Arial")
                                        .setFontSize(10);
```

### 3. lépés: Vázlat elemek létrehozása (számozott lista)
Itt **testreszabjuk a számozási formátumot** a `NumberList` használatával. A `"{0})"` minta „1)”, „2)” stb. eredményt ad.

```java
OutlineElement outlineElem1 = new OutlineElement();
outlineElem1.setNumberList(new NumberList("{0})", NumberFormat.DecimalNumbers, "Arial", 10));
RichText text1 = new RichText().append("First");
text1.setParagraphStyle(defaultStyle);
outlineElem1.appendChildLast(text1);
// Repeat for other elements (outlineElem2 and outlineElem3)
```

> **Miért fontos:** Ha egy `NumberList`‑t csatol minden `OutlineElement`‑hez, teljes irányítást kap a számozási stílus, a betűtípus és a méret felett.

### 4. lépés: Vázlat elemek hozzáadása a vázlathoz
```java
outline.appendChildLast(outlineElem1);
outline.appendChildLast(outlineElem2);
outline.appendChildLast(outlineElem3);
```

### 5. lépés: Vázlat csatolása az oldalhoz
```java
page.appendChildLast(outline);
```

### 6. lépés: Dokumentum mentése PDF‑ként
Végül **mentjük a OneNote‑t PDF‑ként**. A kimeneti fájl pontosan a meghatározott számozott listát fogja tartalmazni.

```java
doc.appendChildLast(page);
doc.save(dataDir + "CreateNumberedList_out.pdf");
System.out.printf("File saved: %s\n", dataDir + "CreateNumberedList_out.pdf");
```

A fenti kód futtatása egy `CreateNumberedList_out.pdf` nevű PDF‑et hoz létre a megadott könyvtárban, megőrizve a számozott lista formátumát.

## Gyakori problémák és megoldások
| Probléma | Megoldás |
|----------|----------|
| **PDF üres** | Győződjön meg róla, hogy a `doc.appendChildLast(page);` hívás megtörtént a `doc.save()` előtt. |
| **A számozás nem jelenik meg** | Ellenőrizze, hogy a `NumberList` minta és a `NumberFormat` helyesen van beállítva. |
| **Fájl nem található hiba** | Használjon abszolút útvonalat a `dataDir`‑hez, vagy hozza létre a könyvtárat előre. |
| **Betűtípus eltérés** | Telepítse a betűtípust (pl. Arial) a kódot futtató gépre. |

## Gyakran ismételt kérdések
### K: Testreszabhatom a számozási formátumot a OneNote listámban?
A: Természetesen! A `NumberList` osztály segítségével, amelyet az Aspose.Note for Java biztosít, testreszabhatja a számozási formátumot.

### K: Elérhető próba verzió az Aspose.Note for Java-hoz?
A: Igen, egy ingyenes próbaverziót letölthet [ide](https://releases.aspose.com/).

### K: Hogyan kaphatok támogatást az Aspose.Note for Java-hoz?
A: Látogassa meg az [Aspose.Note for Java fórumot](https://forum.aspose.com/c/note/28) a közösségi támogatásért.

### K: Hol találhatók részletes dokumentációk az Aspose.Note for Java-hoz?
A: Tekintse meg a [dokumentációt](https://reference.aspose.com/note/java/) a átfogó információkért.

### K: Hogyan vásárolhatok licencet az Aspose.Note for Java-hoz?
A: Licencet vásárolhat [itt](https://purchase.aspose.com/buy).

## Következtetés
Ebben az útmutatóban bemutattuk, hogyan **menthetjük a OneNote‑t PDF‑ként**, miközben tiszta, számozott listát hozunk létre az Aspose.Note for Java segítségével. Alapértelmezett szövegstílus beállításával, a számozási formátum testreszabásával és a lépésről‑lépésre útmutató követésével gyorsan és megbízhatóan generálhat professzionális PDF‑eket a OneNote‑oldalakból.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Utolsó frissítés:** 2026-03-05  
**Tesztelve a következővel:** Aspose.Note for Java 24.11  
**Szerző:** Aspose  

---