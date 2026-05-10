---
date: 2026-03-08
description: Tanulja meg, hogyan mentse el a OneNote-ot PDF-ként kínai számozott listával
  az Aspose.Note for Java használatával. Lépésről‑lépésre útmutató a számozásról,
  a vázlatokról és a PDF‑exportálásról.
linktitle: Save OneNote as PDF with Chinese Numbered List – Aspose.Note
second_title: Aspose.Note Java API
title: OneNote mentése PDF formátumba kínai számozott listával – Aspose.Note
url: /hu/java/onenote-text-manipulation/create-chinese-numbered-list/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote mentése PDF-ként kínai számozott listával – Aspose.Note

## Bevezetés
Ha **OneNote mentés PDF-ként**-et szeretnél elvégezni, miközben kínai számozott listát adsz hozzá, az Aspose.Note for Java egyszerűvé teszi. Ebben az útmutatóban lépésről lépésre bemutatjuk, hogyan hozhatsz létre kínai‑stílusú vázlatot, alkalmazz számozást, és exportáld a OneNote dokumentumot PDF-be. A végére megérted, hogyan **számozhatsz**, **vázlatot adhatsz hozzá a OneNote-hoz**, és látni fogod, miért az **Aspose.Note Java** a legjobb könyvtár ehhez a feladathoz.

## Gyors válaszok
- **Ez az útmutató miről szól?** Kínai számozott lista létrehozása a OneNote-ban és PDF-ként való mentése az Aspose.Note for Java-val.  
- **Szükségem van licencre?** Egy ingyenes próba a teszteléshez elegendő; a gyártási környezethez kereskedelmi licenc szükséges.  
- **Mely IDE-k támogatottak?** Bármely Java IDE, például Eclipse, IntelliJ IDEA vagy NetBeans.  
- **Testreszabhatom a lista stílusát?** Igen – a betűtípus, méret, szín és a számozási formátum teljesen konfigurálható.  
- **Mennyi időt vesz igénybe a megvalósítás?** Körülbelül 10‑15 perc egy alaplista esetén.

## Mi az a „OneNote mentése PDF-ként”?
A OneNote PDF‑ként való mentése a interaktív jegyzetlapot egy statikus, széles körben kompatibilis dokumentummá alakítja. Ez hasznos megosztás, archiválás vagy nyomtatás során, miközben megőrzi az eredeti elrendezést és a hozzáadott egyedi számozást.

## Miért használjuk az Aspose.Note for Java‑t?
Az Aspose.Note gazdag, nagy teljesítményű API‑t biztosít, amely lehetővé teszi, hogy programozottan építs OneNote struktúrákat, alkalmazz összetett számozást (beleértve a kínai számolást), és közvetlenül PDF‑be exportálj manuális UI lépések nélkül. Platformfüggetlen, nem igényel Office telepítést, és teljes stílusvezérlést támogat.

## Előfeltételek
Mielőtt elkezdenéd, győződj meg róla, hogy rendelkezel:

1. **Java fejlesztői környezet** – JDK 8+ és a kedvenc IDE‑d.  
2. **Aspose.Note könyvtár** – Töltsd le a legújabb JAR‑t a hivatalos oldalról [itt](https://releases.aspose.com/note/java/).  
3. **Alapvető ismeretek** a Java szintaxisról és az objektum‑orientált koncepciókról.

## Csomagok importálása
Kezdjük a szükséges csomagok importálásával a Java projektedbe. Ezek az importok hozzáférést biztosítanak a dokumentum létrehozásához, a stílusokhoz és a számozási funkciókhoz.

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

Most bontsuk le a megvalósítást lépésről lépésre.

## Hogyan mentse a OneNote‑ot PDF‑ként kínai számozott listával
Az alábbi részletes, számozott útmutató minden lépéshez rövid magyarázatot és a pontos kódot tartalmazza, amelyet másolhatsz.

### 1. lépés: Dokumentum objektum létrehozása
Elindítunk egy üres `Document` példányt, amely a OneNote tartalmat fogja tárolni.

```java
// The path to the documents directory.
String dataDir = "Your Document Directory";
// create an object of the Document class
Document doc = new Document();
```

### 2. lépés: Oldal objektum inicializálása
A OneNote oldal egy vászonként működik a vázlatok és egyéb elemek számára.

```java
// initialize Page class object
Page page = new Page();
```

### 3. lépés: Vázlat objektum inicializálása
A vázlatok a listaelemek tárolói. Gondolj rájuk úgy, mint a „golyó/szám” tartó konténerre.

```java
// initialize Outline class object
Outline outline = new Outline();
```

### 4. lépés: TextStyle objektum inicializálása
Határozz meg egy alapértelmezett bekezdésstílust, amely minden listaelemhez alkalmazásra kerül.

```java
// initialize TextStyle class object and set formatting properties
ParagraphStyle defaultStyle = new ParagraphStyle()
                                    .setFontColor(Color.black)
                                    .setFontName("Arial")
                                    .setFontSize(10);
```

### 5. lépés: OutlineElement objektumok inicializálása és számozás alkalmazása
Itt három outline elemet hozunk létre, mindegyik egy listaelemet képvisel. A `NumberList("{0})", NumberFormat.ChineseCounting, "Arial", 10)` segítségével kapunk kínai számozást (一、二、三…).

```java
// initialize OutlineElement class objects and apply numbering
OutlineElement outlineElem1 = new OutlineElement();
outlineElem1.setNumberList(new NumberList("{0})", NumberFormat.ChineseCounting, "Arial", 10));
RichText text1 = new RichText().append("First");
text1.setParagraphStyle(defaultStyle);
outlineElem1.appendChildLast(text1);
OutlineElement outlineElem2 = new OutlineElement();
outlineElem2.setNumberList(new NumberList("{0})", NumberFormat.ChineseCounting, "Arial", 10));
RichText text2 = new RichText().append("Second");
text2.setParagraphStyle(defaultStyle);
outlineElem2.appendChildLast(text2);
OutlineElement outlineElem3 = new OutlineElement();
outlineElem3.setNumberList(new NumberList("{0})", NumberFormat.ChineseCounting, "Arial", 10));
RichText text3 = new RichText().append("Third");
text3.setParagraphStyle(defaultStyle);
outlineElem3.appendChildLast(text3);
```

### 6. lépés: Outline elemek hozzáadása
Minden számozott elemet csatoljunk a vázlat tárolóhoz.

```java
// add outline elements
outline.appendChildLast(outlineElem1);
outline.appendChildLast(outlineElem2);
outline.appendChildLast(outlineElem3);
```

### 7. lépés: Outline csomópont hozzáadása az oldalhoz
Most helyezzük el a teljes vázlatot az oldalon.

```java
// add Outline node
page.appendChildLast(outline);
```

### 8. lépés: Oldal csomópont hozzáadása a dokumentumhoz
Az oldal a teljes OneNote dokumentum részévé válik.

```java
// add Page node
doc.appendChildLast(page);
```

### 9. lépés: Dokumentum mentése PDF‑ként
Végül exportáljuk a OneNote dokumentumot PDF‑be a `save` metódus segítségével. Ez a lépés, ahol **OneNote mentése PDF‑ként** történik.

```java
// save the document
doc.save(dataDir + "CreateChineseNumberedList_out.pdf");
System.out.printf("File saved: %s\n", dataDir + "CreateChineseNumberedList_out.pdf");
```

A fenti kód futtatása egy PDF fájlt (`CreateChineseNumberedList_out.pdf`) hoz létre, amely egy kínai számozott listát tartalmaz, pontosan úgy, ahogy egy OneNote oldalon látnád.

## Gyakori problémák és megoldások
- **Helytelen számozási formátum:** Győződj meg róla, hogy a `NumberFormat.ChineseCounting`‑et használod. Más formátumok (arab, római) más eredményt adnak.  
- **Fájl nem található hiba:** Ellenőrizd, hogy a `dataDir` egy létező, írható mappára mutat.  
- **Hiányzó betűtípus:** Ha a megadott betűtípus (pl. „Arial”) nincs telepítve a szerveren, a PDF alapértelmezett betűtípusra vált. Telepítsd a betűtípust vagy válassz másikat.

## Gyakran Ismételt Kérdések

### Az Aspose.Note kompatibilis különböző Java IDE‑kkel?
Igen, az Aspose.Note kompatibilis a népszerű Java IDE‑kkel, mint az Eclipse és az IntelliJ IDEA.

### Testreszabhatom a számozott lista formázását?
Teljes mértékben. Ahogy az útmutatóban is látható, a betűtípust, a színt és a méretet a saját igényeid szerint állíthatod be.

### Van elérhető próba verzió az Aspose.Note‑hoz?
Igen, a próba verziót [itt](https://releases.aspose.com/) tekintheted meg.

### Hol találok részletes dokumentációt az Aspose.Note‑hoz?
A dokumentációt [itt](https://reference.aspose.com/note/java/) találod.

### Hogyan kaphatok támogatást az Aspose.Note‑hoz?
Bármilyen segítség vagy kérdés esetén látogasd meg a támogatási fórumot [itt](https://forum.aspose.com/c/note/28).

## Kiegészítő GYIK (AI‑optimalizált)

**K: Használhatom ezt a kódot más nyelvek számozásához?**  
V: Igen, cseréld le a `NumberFormat.ChineseCounting`‑t a megfelelő `NumberFormat` enum értékre (pl. `NumberFormat.RomanUpper`).

**K: A PDF megőrzi a vázlat hierarchiáját?**  
V: Az exportált PDF megőrzi a vizuális hierarchiát, de a statikus PDF‑ekben nincs interaktív vázlatnavigáció.

**K: Hogyan változtathatom meg a golyó stílusát a számok helyett?**  
V: Használd a `NumberList`‑et egy egyedi formátumkarakterlánccal, például `"• "` és állítsd be a `NumberFormat.None`‑t.

**K: Lehetséges képeket hozzáadni ugyanarra az oldalra?**  
V: Igen, a PDF‑be mentés előtt `Image` objektumokat is beilleszthetsz az oldalra.

**K: Milyen verziójú Aspose.Note szükséges?**  
V: A legújabb stabil kiadás (2026‑tól) támogatja az itt bemutatott összes funkciót.

---

**Utolsó frissítés:** 2026-03-08  
**Tesztelve:** Aspose.Note for Java 24.12  
**Szerző:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}