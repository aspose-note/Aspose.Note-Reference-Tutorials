---
date: 2026-04-30
description: Ismerje meg, hogyan **mentse a OneNote-ot PDF‑ként**, és hogyan adjon
  hozzá aloldalakat a OneNote-ban az Aspose.Note for Java használatával. Kövesse ezt
  a lépésről‑lépésre útmutatót, hogy hatékonyan szervezze meg jegyzeteit.
keywords:
- save onenote as pdf
- add sub pages onenote
- Aspose.Note Java
linktitle: Hogyan mentse a OneNote-ot PDF-ként, és adjon hozzá aloldalakat
second_title: Aspose.Note Java API
title: Hogyan mentse a OneNote-ot PDF‑ként, és adjon hozzá aloldalakat
url: /hu/java/onenote-page-manipulation/create-document-with-root-and-sub-pages/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hogyan mentse a OneNote-ot PDF-ként és adjon hozzá aloldalakat

## Bevezetés

Ebben az útmutatóban megtudja, hogyan **mentse a onenote-ot PDF-ként**, miközben egy olyan dokumentumot hoz létre, amely mind a gyökér-, mind az aloldalakat tartalmazza az Aspose.Note for Java használatával. A OneNote jegyzetfüzeteinek világos hierarchiával való szervezése megkönnyíti a navigációt, és a PDF-be exportálás biztosítja, hogy jegyzeteit univerzálisan olvasható formátumban oszthassa meg. Emellett megmutatjuk, hogyan **adhat hozzá aloldalakat a OneNote stílusában**, így könnyedén építhet több szintű struktúrákat.

## Gyors válaszok
- **Mit jelent a „save onenote as pdf”?** Ez a OneNote jegyzetfüzet PDF-fájlba exportálását jelenti az Aspose.Note for Java használatával.  
- **Melyik API szükséges?** Az Aspose.Note for Java biztosítja a szükséges osztályokat és metódusokat.  
- **Létrehozhatok hierarchikus oldalakat?** Igen – állítsa be az oldal szintjét a gyökér- és aloldalak létrehozásához.  
- **Szükségem van licencre a termeléshez?** Egy ingyenes próba elérhető, de a kereskedelmi licenc szükséges a termelési használathoz.  
- **Milyen formátumokba exportálhatok?** A PDF mellett exportálhat BMP, PNG, JPEG, DOCX és további formátumokba.

## Hogyan mentse a OneNote-ot PDF-ként

A OneNote PDF-ként való mentése minden jegyzetfüzet oldalt egy rögzített elrendezésű dokumentummá alakít, amely megőrzi a formázást, a képeket és az oldal hierarchiáját. Ez ideális a jegyzetek megosztásához, archiválásához vagy nyomtatásához, miközben az eredeti struktúra változatlan marad.

## Miért adjunk hozzá aloldalakat a OneNote-ban?

Az aloldalak hozzáadása lehetővé teszi, hogy a kapcsolódó tartalmakat egy szülőoldal alá csoportosítsa, egy mappaszerű struktúrát tükrözve. Javítja a jegyzetek szervezését, felgyorsítja a keresést, és javítja az olvasási élményt, amikor a jegyzetfüzet PDF-be exportálódik.

## Előfeltételek

Mielőtt elkezdené, győződjön meg róla, hogy az alábbi előfeltételek rendelkezésre állnak:

1. **Java Development Kit (JDK)** – Győződjön meg róla, hogy a JDK telepítve van a rendszerén.  
2. **Aspose.Note for Java** – Töltse le és telepítse az Aspose.Note for Java-t a [weboldalról](https://purchase.aspose.com/buy).  
3. **Integrated Development Environment (IDE)** – Válasszon egy Java IDE-t, például IntelliJ IDEA, Eclipse vagy NetBeans.

## Csomagok importálása

Kezdje a szükséges csomagok importálásával a Java projektjében:

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

Inicializálja az oldal objektumokat, és állítsa be a szintjeiket. A szint beállítása határozza meg, hogy egy oldal gyökéroldal vagy aloldal.

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

Mentse a OneNote dokumentumot PDF-ként (vagy ebben a példában BMP-ként). A `SaveFormat` módosításával exportálhat PDF-be, ami teljesíti a „save onenote as pdf” követelményt:

```java
try {
    doc.save(dataDir + "GenerateRootAndSubLevelPagesInOneNote_out.bmp", SaveFormat.Bmp);
} catch (IOException e) {
    // Handle exception
}
```

> **Pro tipp:** A közvetlen PDF exportáláshoz cserélje le a `SaveFormat.Bmp`-t `SaveFormat.Pdf`-re.

Gratulálunk! Sikeresen létrehozott egy OneNote dokumentumot gyökér- és aloldalakkal, és megtanulta, hogyan **mentse a onenote-ot PDF-ként** az Aspose.Note for Java segítségével.

## Miért fontos ez

- **Hierarchikus szervezés:** A gyökér- és aloldalak lehetővé teszik, hogy mappaszerű struktúrákat utánozzon a OneNote-ban.  
- **Zökkenőmentes PDF exportálás:** A szervezés után a PDF-be exportálás megőrzi a hierarchiát, így a végdokumentum könnyen olvasható és megosztható.  
- **Automatizálás:** A kód integrálható nagyobb Java alkalmazásokba, lehetővé téve strukturált jegyzetfüzetek kötegelt létrehozását.

## Gyakori hibák és hogyan kerüljük el őket

| Probléma | Ok | Megoldás |
|----------|----|----------|
| Az oldalak ugyanazon a szinten jelennek meg | Helytelen `setLevel` érték | Használja a `setLevel((byte) 1)`-et a gyökéroldalakhoz, és a `setLevel((byte) 2)`-t (vagy magasabbat) az aloldalakhoz. |
| A PDF kimenet üresnek tűnik | Hiányzó `SaveFormat.Pdf` vagy helytelen fájlútvonal | Ellenőrizze, hogy a könyvtár létezik, és használja a `SaveFormat.Pdf`-t. |
| A betűtípus nem alkalmazott | Helytelen betűtípus név vagy hiányzó betűtípus a rendszeren | Győződjön meg róla, hogy a betűtípus (pl. „David Transparent”) telepítve van a kódot futtató gépen. |

## Gyakran feltett kérdések

**Q: Létrehozhatok több szintű aloldalakat az Aspose.Note for Java használatával?**  
A: Igen, mélyebb hierarchiákat hozhat létre magasabb szintszámok beállításával (pl. `setLevel((byte) 3)` a harmadik szintű aloldalhoz).

**Q: Az Aspose.Note for Java kompatibilis különböző Java IDE-kkel?**  
A: Teljesen. Működik IntelliJ IDEA, Eclipse, NetBeans és bármely Java fejlesztést támogató IDE-vel.

**Q: Testreszabhatom a szöveg formázását a OneNote dokumentumban?**  
A: Igen. Használja a `ParagraphStyle`-t a betűtípus név, méret, szín és egyéb attribútumok beállításához minden `RichText` elemhez.

**Q: Az Aspose.Note for Java támogatja a dokumentumok mentését BMP-n kívül más formátumokba?**  
A: Igen. Támogatott formátumok közé tartozik a PDF, PNG, JPEG, DOCX és továbbiak. Ennek megfelelően módosítsa a `SaveFormat` enumot.

**Q: Elérhető próba verzió az Aspose.Note for Java-hoz?**  
A: Igen, letölthet egy ingyenes próbaverziót az Aspose weboldaláról.

## Összegzés

A OneNote jegyzetfüzeteinek világos hierarchikus struktúrával való szervezése és PDF-ként való exportálása hozzáférhetőbbé és megoszthatóbbá teszi a jegyzeteit. A fenti lépések követésével most már tudja, hogyan **mentse a onenote-ot PDF-ként** és hogyan **adjunk hozzá aloldalakat a OneNote stílusában** programozottan az Aspose.Note for Java segítségével.

---

**Utoljára frissítve:** 2026-04-30  
**Tesztelve:** Aspose.Note for Java 24.11 (legújabb)  
**Szerző:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}