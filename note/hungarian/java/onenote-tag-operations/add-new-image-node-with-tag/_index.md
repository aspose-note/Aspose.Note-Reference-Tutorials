---
date: 2026-08-13
description: Ismerje meg, hogyan szúrhat be képet a OneNote-ba, adhat hozzá címkét
  a képhez, és mentheti a OneNote-ot PDF formátumban az Aspose.Note for Java segítségével.
keywords:
- insert image into onenote
- save onenote as pdf
- java add tag to image
lastmod: 2026-08-13
linktitle: Címke hozzáadása a képhez a OneNote-ban – Aspose.Note
og_description: Kép beszúrása a OneNote-ba, sárga‑csillag címke hozzáadása a képhez,
  és a jegyzetfüzet exportálása PDF formátumba az Aspose.Note for Java használatával.
  Kövesse a lépésről‑lépésre útmutatót a gyors megvalósításhoz.
og_image_alt: Guide showing how to insert an image and tag it in OneNote using Aspose.Note
  for Java
og_title: Kép beszúrása a OneNote-ba és címke hozzáadása – Aspose.Note Java
schemas:
- author: Aspose
  dateModified: '2026-08-13'
  description: Learn how to insert image into OneNote, add a tag to the image, and
    save OneNote as PDF using Aspose.Note for Java.
  headline: Insert image into OneNote and add tag with Aspose.Note – Java
  type: TechArticle
- description: Learn how to insert image into OneNote, add a tag to the image, and
    save OneNote as PDF using Aspose.Note for Java.
  name: Insert image into OneNote and add tag with Aspose.Note – Java
  steps:
  - name: create document object
    text: The `Document` class is Aspose.Note's top‑level object that represents a
      OneNote notebook in memory. After instantiation, all subsequent operations flow
      through this object.
  - name: initialize page class object
    text: The `Page` class defines a single page inside the notebook. You can set
      page properties such as title and size before adding content.
  - name: initialize outline class object
    text: The `Outline` class groups related content blocks on a page. Outlines are
      containers for `OutlineElement` objects.
  - name: initialize outline element class object
    text: The `OutlineElement` class represents an individual block inside an outline,
      such as a paragraph, image, or table.
  - name: load and insert image
    text: '*(This step demonstrates **insert image into OneNote**)* The `Image` class
      encapsulates image data to be placed on a OneNote page.'
  - name: add note tag to image
    text: '*(Here we answer **how to add image tag**)* The `NoteTag` class defines
      a visual tag that can be attached to page elements.'
  - name: add outline element node
    text: Attach the image (now tagged) to the outline element so it appears in the
      correct order on the page.
  - name: add outline node
    text: Insert the outline into the page’s collection of outlines.
  - name: add page node
    text: Add the fully built page to the document’s page collection.
  type: HowTo
- questions:
  - answer: You can find the documentation at the **[Aspose.Note Java API reference](https://reference.aspose.com/note/java/)**.
    question: Where can I find Aspose.Note documentation?
  - answer: You can download it from the releases page **[Aspose.Note Java release
      page](https://releases.aspose.com/note/java/)**.
    question: How do I download Aspose.Note for Java?
  - answer: Yes, you can access the free trial at the **[Aspose free trial page](https://releases.aspose.com/)**.
    question: Is there a free trial available?
  - answer: Visit the community forum **[Aspose.Note community forum](https://forum.aspose.com/c/note/28)**
      for support.
    question: Where can I get support for Aspose.Note?
  - answer: If required, you can obtain a temporary license from the **[temporary
      license request page](https://purchase.aspose.com/temporary-license/)**.
    question: Do I need a temporary license?
  type: FAQPage
second_title: Aspose.Note Java API
tags:
- onenote automation
- aspose.note java
- insert image into onenote
- add tag to image
- export onenote pdf
title: Kép beszúrása a OneNote-ba és címke hozzáadása az Aspose.Note – Java használatával
url: /hu/java/onenote-tag-operations/add-new-image-node-with-tag/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Kép beszúrása a OneNote-ba és címke hozzáadása az Aspose.Note – Java

## Bevezetés
Ha **képet kell beszúrni a OneNote-ba** Java-val dolgozva, az Aspose.Note egyszerűvé teszi a teljes folyamatot. Ebben az útmutatóban végigvezetünk a kép egy OneNote oldalra való beszúrásán, a sárga csillag címke alkalmazásán a képre, és végül a **OneNote mentésén PDF‑ként**. A végére pontosan látni fogja, hogyan kell címkét hozzáadni a képhez, képet beszúrni a OneNote-ba, és a OneNote‑t PDF‑be konvertálni – mindezt néhány kódsorral.

## Gyors válaszok
- **Mit jelent a „címke hozzáadása a képhez”?** Egy vizuális jegyzetcímkét (pl. egy sárga csillagot) csatol egy képcsomóponthoz egy OneNote oldalon.  
- **Melyik könyvtár kezeli ezt?** Aspose.Note for Java.  
- **Szükségem van licencre a teszteléshez?** Egy ingyenes próba működik fejlesztéshez; a termeléshez kereskedelmi licenc szükséges.  
- **Exportálhatom az eredményt PDF‑ként?** Igen – használja a `doc.save(..., SaveFormat.Pdf)`‑t a **OneNote PDF‑ként mentéséhez**.  
- **Mennyi időt vesz igénybe a megvalósítás?** Általában 10 percnél kevesebb egy alap szcenárióhoz.

## Mi a „címke hozzáadása a képhez” a OneNote-ban?
A `NoteTag` elem egy metaadat-objektum, amely vizuálisan megjelöli a képet egy ikon (például csillag vagy zászló) segítségével. Megjelenik a OneNote felhasználói felületén, és kereshető vagy szűrhető, lehetővé téve a felhasználók számára, hogy gyorsan megtalálják a címkézett vizuális elemeket a nagy jegyzetfüzetekben.

## Miért érdemes címkét hozzáadni a képhez a OneNote-ban?
A képek címkézése könnyű módot biztosít a kontextus hozzáadására a kép módosítása nélkül. A címkék a lap struktúrájának részeként tárolódnak, lehetővé téve a gyors keresést, vizuális jelzéseket és kategorizálást, ami különösen hasznos kutatásban, projektkövetésben vagy oktatási jegyzetfüzetekben.

- A vizuális tartalom szervezése a kép módosítása nélkül.  
- Fontos grafikák gyors megtalálása a OneNote címke keresésével.  
- Kontextus biztosítása (pl. „későbbi átnézés”, „fontos hivatkozás”) közvetlenül az oldalon.  

## Előfeltételek
Mielőtt belemerülnénk, győződjön meg, hogy a következőkkel rendelkezik:

1. Aspose.Note for Java: Győződjön meg róla, hogy az Aspose.Note könyvtár telepítve van. Ha nincs, letöltheti a **[Aspose.Note for Java letöltési oldalról](https://releases.aspose.com/note/java/)**.  
2. Java fejlesztői környezet: működő JDK (8 vagy újabb) és egy IDE vagy a választott build eszköz.

Most, hogy az előfeltételek rendben vannak, lépjünk a következő lépésekre.

## Csomagok importálása
A Java projektjében kezdje a szükséges csomagok importálásával:

A `Document` osztály egy OneNote jegyzetfüzetet képvisel a memóriában.  
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

## Hogyan szúrhat be képet a OneNote-ba?

Töltse be a célkép fájlt, hozzon létre egy `Image` csomópontot, és adja hozzá az oldal vázához. A beszúrás csak három API hívást igényel, és megőrzi az eredeti kép felbontását. Ez a megközelítés PNG, JPEG, BMP és GIF formátumoknál működik további konverzió nélkül.

### 1. lépés: dokumentumobjektum létrehozása
A `Document` osztály az Aspose.Note legfelső szintű objektuma, amely egy OneNote jegyzetfüzetet képvisel a memóriában. Az példányosítás után minden további művelet ezen az objektumon keresztül történik.

```java
// The path to the documents directory.
String dataDir = "Your Document Directory";
// create an object of the Document class
Document doc = new Document();
```

### 2. lépés: oldal osztály objektum inicializálása
A `Page` osztály egyetlen oldalt definiál a jegyzetfüzetben. Tartalom hozzáadása előtt beállíthatja az oldal tulajdonságait, például a címet és a méretet.

```java
// initialize Page class object
Page page = new Page();
```

### 3. lépés: váz osztály objektum inicializálása
Az `Outline` osztály a kapcsolódó tartalmi blokkokat csoportosítja egy oldalon. A vázak konténerek az `OutlineElement` objektumok számára.

```java
// initialize Outline class object
Outline outline = new Outline();
```

### 4. lépés: váz elem osztály objektum inicializálása
Az `OutlineElement` osztály egy egyedi blokkot képvisel egy vázon belül, például bekezdést, képet vagy táblázatot.

```java
// initialize OutlineElement class object
OutlineElement outlineElem = new OutlineElement();
```

## Hogyan adhat hozzá címkét egy képhez a OneNote-ban?

Hozzon létre egy `NoteTag` objektumot, állítsa be a típusát (pl. sárga csillag), és csatolja a korábban létrehozott `Image` csomóponthoz. A címke a kép metaadatai részévé válik, és a OneNote automatikusan megjeleníti.

A címke csatolásához példányosítson egy `NoteTag` objektumot, állítsa be a `TagIcon`-t a kívánt szimbólumra (például `TagIcon.YellowStar`), és a `addTag` metódussal társítsa az `Image` csomóponthoz. A címke a kép metaadatai részévé válik, és a OneNote automatikusan megjeleníti.

### 5. lépés: kép betöltése és beszúrása  
*(Ez a lépés bemutatja a **képet a OneNote-ba beszúrni**)*
A `Image` osztály a OneNote oldalra helyezendő kép adatokat tartalmazza.  
```java
// load an image
Image image = new Image(dataDir + "Input.jpg");
// insert image in the document node
outlineElem.appendChildLast(image);
```

### 6. lépés: jegyzetcímke hozzáadása a képhez  
*(Itt válaszolunk arra, **hogyan adjon hozzá képcímkét**)*
A `NoteTag` osztály egy vizuális címkét definiál, amely az oldal elemeihez csatolható.  
```java
// add a yellow star note tag to the image
NoteTag noteTag = NoteTag.createYellowStar();
image.getTags().add(noteTag);
```

### 7. lépés: váz elem csomópont hozzáadása
Csatolja a (most már címkézett) képet a váz elemhez, hogy a megfelelő sorrendben jelenjen meg az oldalon.  
```java
// add outline element node
outline.appendChildLast(outlineElem);
```

### 8. lépés: váz csomópont hozzáadása
Illessze be a vázat az oldal vázgyűjteményébe.  
```java
// add outline node
page.appendChildLast(outline);
```

### 9. lépés: oldal csomópont hozzáadása
Adja hozzá a teljesen felépített oldalt a dokumentum oldalgyűjteményéhez.  
```java
// add page node
doc.appendChildLast(page);
```

## Hogyan mentse a OneNote-ot PDF‑ként?

Hívja meg a `save` metódust a `Document` példányon, megadva a `SaveFormat.Pdf` értéket. Az Aspose.Note minden oldal elemet – beleértve a képeket, címkéket és vázakat – hű PDF ábrázolássá konvertál, anélkül, hogy a Microsoft OneNote telepítve lenne.

A `SaveFormat` felsorolt típus (enum) határozza meg a dokumentum mentésének kimeneti formátumát.  
```java
// save OneNote document as a PDF
doc.save(dataDir + "AddNewImageNodeWithTag_out.pdf", SaveFormat.Pdf);
```

Gratulálunk! Sikeresen **címkét adtál a képhez**, képet szúrtál be a OneNote-ba, és exportáltad a jegyzetfüzetet PDF‑ként az Aspose.Note for Java segítségével.

## Gyakori problémák és megoldások
| Probléma | Megoldás |
|----------|----------|
| **A kép nem jelenik meg** | Ellenőrizze, hogy a `dataDir + \"Input.jpg\"` útvonal helyes-e, és a fájl elérhető. |
| **A címke nem látható** | Győződjön meg róla, hogy olyan OneNote verziót használ, amely támogatja a jegyzetcímkéket (a legújabb verziók igen). |
| **A PDF kimenet üres** | Ellenőrizze, hogy a dokumentum legalább egy oldalt/vázat tartalmaz-e a `save` hívása előtt. |

## Gyakran ismételt kérdések

**K: Hol találom az Aspose.Note dokumentációt?**  
V: A dokumentáció megtalálható a **[Aspose.Note Java API referencia](https://reference.aspose.com/note/java/)** oldalon.

**K: Hogyan tölthetem le az Aspose.Note for Java-t?**  
V: Letöltheti a kiadási oldalról **[Aspose.Note Java kiadási oldal](https://releases.aspose.com/note/java/)**.

**K: Van ingyenes próba?**  
V: Igen, az ingyenes próbát a **[Aspose ingyenes próba oldal](https://releases.aspose.com/)** érheti el.

**K: Hol kaphatok támogatást az Aspose.Note-hoz?**  
V: Látogassa meg a közösségi fórumot **[Aspose.Note közösségi fórum](https://forum.aspose.com/c/note/28)** támogatásért.

**K: Szükségem van ideiglenes licencre?**  
V: Ha szükséges, ideiglenes licencet kérhet a **[ideiglenes licenc kérelem oldalról](https://purchase.aspose.com/temporary-license/)**.

## Következtetés
Az Aspose.Note for Java elsajátítása izgalmas lehetőségeket nyit a OneNote dokumentumkezelésben. Az útmutató követésével megtanulta, **hogyan adjon címkét a képhez**, **hogyan szúrjon be képet a OneNote-ba**, és **hogyan mentse a OneNote-ot PDF‑ként** – olyan készségeket, amelyeket számos automatizálási projektben alkalmazhat. Fedezze fel továbbra is az Aspose.Note dokumentációt a **[Aspose.Note Java dokumentációban](https://reference.aspose.com/note/java/)** a fejlettebb funkciók és lehetőségek megismeréséhez.

---

**Legutóbb frissítve:** 2026-08-13  
**Tesztelve ezzel:** Aspose.Note 24.11 for Java  
**Szerző:** Aspose

## Kapcsolódó útmutatók

- [Hogyan adjunk képet a OneNote-hoz Java-val – Dokumentum építése és kép beszúrása](/note/java/onenote-hyperlinks-images/build-doc-insert-image/)
- [Hogyan mentse a OneNote-ot PDF‑ként az Aspose.Note for Java segítségével](/note/java/onenote-document-loading/load-save-format/)
- [Táblázatsor beszúrása Java - Táblázat csomópont hozzáadása címkével a OneNote-ban - Aspose.Note](/note/java/onenote-tag-operations/add-new-table-node-with-tag/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}