---
description: Tanulja meg, hogyan menthet OneNote PDF-et, és adhat hozzá aloldalakat
  a OneNote-ban az Aspose.Note for Java használatával. Kövesse ezt a lépésről‑lépésre
  útmutatót, hogy hatékonyan szervezze meg jegyzeteit.
linktitle: How to Save OneNote PDF and Add Sub Pages
second_title: Aspose.Note Java API
title: Hogyan mentse el a OneNote PDF-et, és adjon hozzá aloldalakat
url: /hu/java/onenote-page-manipulation/create-document-with-root-and-sub-pages/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hogyan mentsük el a OneNote PDF-et és adjunk hozzá aloldalakat

## Bevezetés

Ebben az útmutatóban megtanulja, **hogyan mentse el a OneNote PDF-et**, miközben egy olyan dokumentumot hoz létre, amely gyökér‑ és aloldalakat egyaránt tartalmaz az Aspose.Note for Java segítségével. A OneNote jegyzetfüzetek világos hierarchiával való rendezése megkönnyíti a navigációt, és a PDF‑be exportálás lehetővé teszi, hogy a jegyzeteket egy mindenki által olvasható formátumban ossza meg. Emellett megmutatjuk, hogyan **adjunk hozzá aloldalakat onenote** stílusban, így könnyedén építhet több szintű struktúrákat.

## Gyors válaszok
- **Mit jelent a fő kulcsszó?** A OneNote jegyzetfüzet PDF‑be exportálását jelenti az Aspose.Note segítségével.
- **Melyik API-t használja?** Aspose.Note for Java.
- **Létrehozhatok hierarchikus oldalakat?** Igen – állítsa be az oldal szintjét a gyökér‑ és aloldalak építéséhez.
- **Szükség van licencre?** Elérhető ingyenes próba, a kereskedelmi licenc a termeléshez kötelező.
- **Milyen kimeneti formátumok támogatottak?** BMP, PDF, PNG és továbbiak.

## Mi az a „hogyan mentsük el a OneNote PDF-et”?
A OneNote PDF‑ként való mentése a jegyzetfüzet oldalait egy rögzített elrendezésű dokumentummá alakítja, amely megőrzi a formázást, a képeket és a hierarchiát. Ideális megosztásra, archiválásra vagy nyomtatásra.

## Miért adjunk hozzá aloldalakat onenote?
Az aloldalak hozzáadása lehetővé teszi, hogy kapcsolódó tartalmakat egy szülőoldal alá csoportosítson, egy mappaszerű struktúrát tükrözve. Ez javítja a jegyzetek szervezését, felgyorsítja a keresést, és fokozza az olvasási élményt, amikor a jegyzetfüzet PDF‑be exportálódik.

## Előfeltételek

Mielőtt elkezdené, győződjön meg róla, hogy rendelkezik a következőkkel:

1. Java Development Kit (JDK): Győződjön meg, hogy a JDK telepítve van a rendszerén.  
2. Aspose.Note for Java: Töltse le és telepítse az Aspose.Note for Java‑t a [weboldalról](https://purchase.aspose.com/buy).  
3. Integrated Development Environment (IDE): Válasszon Java IDE‑t, például IntelliJ IDEA, Eclipse vagy NetBeans.

## Csomagok importálása

Importálja a szükséges csomagokat a Java projektjébe:

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.SaveFormat;
import com.aspose.note.ParagraphStyle;
```

## 1. lépés: Dokumentum könyvtár beállítása

Határozza meg a könyvtárat, ahová a OneNote dokumentumot menteni szeretné:

```java
String dataDir = "Your Document Directory";
```

## 2. lépés: Dokumentum objektum létrehozása

Hozzon létre egy `Document` objektumot:

```java
Document doc = new Document();
```

## 3. lépés: Oldalak létrehozása

Inicializálja az oldal objektumokat és állítsa be a szintjeiket. A szint beállítása határozza meg, hogy egy oldal gyökér‑ vagy aloldal legyen:

```java
Page page1 = new Page();
page1.setLevel((byte) 1);

Page page2 = new Page();
page2.setLevel((byte) 2);

Page page3 = new Page();
page3.setLevel((byte) 1);
```

## 4. lépés: Csomópontok hozzáadása az oldalakhoz

### Csomópontok hozzáadása az első oldalhoz

```java
Outline outline = new Outline();
OutlineElement outlineElem = new OutlineElement();
ParagraphStyle textStyle = new ParagraphStyle()
                                    .setFontColor(Color.black)
                                    .setFontName("David Transparent")
                                    .setFontSize(10);

RichText text = new RichText().append("First page.");
text.setParagraphStyle(textStyle);

outlineElem.appendChildLast(text);
outline.appendChildLast(outlineElem);
page1.appendChildLast(outline);
```

### Csomópontok hozzáadása a második oldalhoz

```java
Outline outline2 = new Outline();
OutlineElement outlineElem2 = new OutlineElement();
ParagraphStyle textStyle2 = new ParagraphStyle()
                                    .setFontColor(Color.black)
                                    .setFontName("David Transparent")
                                    .setFontSize(10);

RichText text2 = new RichText().append("Second page.");
text2.setParagraphStyle(textStyle2);

outlineElem2.appendChildLast(text2);
outline2.appendChildLast(outlineElem2);
page2.appendChildLast(outline2);
```

### Csomópontok hozzáadása a harmadik oldalhoz

```java
Outline outline3 = new Outline();
OutlineElement outlineElem3 = new OutlineElement();
ParagraphStyle textStyle3 = new ParagraphStyle()
                                    .setFontColor(Color.black)
                                    .setFontName("Broadway")
                                    .setFontSize(10);

RichText text3 = new RichText().append("Third page.");
text3.setParagraphStyle(textStyle3);

outlineElem3.appendChildLast(text3);
outline3.appendChildLast(outlineElem3);
page3.appendChildLast(outline3);
```

## 5. lépés: Oldalak hozzáadása a dokumentumhoz

```java
doc.appendChildLast(page1);
doc.appendChildLast(page2);
doc.appendChildLast(page3);
```

## 6. lépés: Dokumentum mentése

Mentse a OneNote dokumentumot PDF‑ként (vagy ebben a példában BMP‑ként). A `SaveFormat` módosításával exportálhat PDF‑be, ami teljesíti a „hogyan mentsük el a OneNote PDF-et” követelményt:

```java
try {
    doc.save(dataDir + "GenerateRootAndSubLevelPagesInOneNote_out.bmp", SaveFormat.Bmp);
} catch (IOException e) {
    // Handle exception
}
```

> **Hasznos tipp:** A közvetlen PDF exporthoz cserélje le a `SaveFormat.Bmp`‑et `SaveFormat.Pdf`‑re.

Gratulálunk! Sikeresen létrehozott egy OneNote dokumentumot gyökér‑ és aloldalakkal, és megtanulta, **hogyan mentsük el a OneNote PDF-et** az Aspose.Note for Java segítségével.

## Miért fontos ez

- **Hierarchikus szervezés:** A gyökér‑ és aloldalak lehetővé teszik a mappaszerű struktúrák utánzását a OneNote‑ban.  
- **Zökkenőmentes PDF export:** A megfelelő szervezés után a PDF export megőrzi a hierarchiát, így a végdokumentum könnyen olvasható és megosztható.  
- **Automatizálás:** A kód integrálható nagyobb Java alkalmazásokba, lehetővé téve strukturált jegyzetfüzetek tömeges létrehozását.

## Gyakori hibák és elkerülésük

| Probléma | Ok | Megoldás |
|----------|----|----------|
| Az oldalak ugyanazon a szinten jelennek meg | Hibás `setLevel` érték | Használja a `setLevel((byte) 1)`‑et a gyökéroldalakhoz és a `setLevel((byte) 2)`‑t (vagy magasabbat) az aloldalakhoz. |
| A PDF kimenet üres | Hiányzó `SaveFormat.Pdf` vagy helytelen fájlútvonal | Ellenőrizze, hogy a könyvtár létezik, és használja a `SaveFormat.Pdf`‑t. |
| A betűtípus nem alkalmazódik | Rossz betűtípus név vagy hiányzó betűtípus a rendszeren | Győződjön meg róla, hogy a betűtípus (pl. “David Transparent”) telepítve van a kódot futtató gépen. |

## Gyakran ismételt kérdések

**K: Létrehozhatok több szintű aloldalakat az Aspose.Note for Java‑val?**  
V: Igen, mélyebb hierarchiákat hozhat létre magasabb szintszámok beállításával (pl. `setLevel((byte) 3)` a harmadszintű aloldalhoz).

**K: Az Aspose.Note for Java kompatibilis-e különböző Java IDE‑kkel?**  
V: Teljesen. Működik IntelliJ IDEA, Eclipse, NetBeans és bármely, Java fejlesztést támogató IDE‑vel.

**K: Testreszabhatom a szöveg formázását a OneNote dokumentumban?**  
V: Igen. Használja a `ParagraphStyle`‑t a betűtípus, méret, szín és egyéb attribútumok beállításához minden `RichText` elemhez.

**K: Az Aspose.Note for Java támogatja-e a dokumentumok mentését a BMP‑n kívül más formátumokba?**  
V: Igen. Támogatott formátumok közé tartozik a PDF, PNG, JPEG, DOCX és továbbiak. Ennek megfelelően módosítsa a `SaveFormat` enum értékét.

**K: Elérhető-e próba verzió az Aspose.Note for Java‑hoz?**  
V: Igen, letölthet egy ingyenes próbaverziót az Aspose weboldaláról.

## Összegzés

A OneNote jegyzetfüzetek világos hierarchikus struktúrával való rendezése és PDF‑be exportálása hozzáférhetőbbé és megoszthatóbbá teszi a jegyzeteket. A fenti lépések követésével most már tudja, **hogyan mentsük el a OneNote PDF-et** és **aloldalakat adjon hozzá onenote** stílusban programozottan az Aspose.Note for Java segítségével.

---

**Utoljára frissítve:** 2026-01-07  
**Tesztelve a következővel:** Aspose.Note for Java 24.11 (legújabb)  
**Szerző:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}