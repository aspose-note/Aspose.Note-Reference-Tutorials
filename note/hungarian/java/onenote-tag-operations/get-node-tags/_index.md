---
date: 2026-02-28
description: Tanulja meg, hogyan lehet kinyerni a címkéket OneNote‑fájlokból az Aspose.Note
  for Java segítségével. Ez az útmutató bemutatja, hogyan töltsön be OneNote‑fájlt,
  hogyan szerezze meg a OneNote‑címkéket, és hogyan módosítsa hatékonyan a OneNote‑címkéket.
linktitle: How to Extract Tags from OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: Hogyan vonjunk ki címkéket a OneNote‑ból az Aspose.Note használatával
url: /hu/java/onenote-tag-operations/get-node-tags/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hogyan lehet címkéket kinyerni a OneNote-ból az Aspose.Note segítségével

## Bevezetés
Ha **címkék kinyerésére** van szükséged egy OneNote dokumentumból, jó helyen jársz. Ebben az útmutatóban végigvezetünk a OneNote fájl betöltésének, a OneNote címkék lekérésének, és még a címkék módosításának folyamatán az Aspose.Note for Java használatával. A tutorial végére magabiztosan tudod majd integrálni a címkék kinyerését bármely Java alkalmazásba.

## Gyors válaszok
- **Mi a fő osztály a OneNote fájl megnyitásához?** `Document`
- **Melyik metódus adja vissza az összes RichText csomópontot?** `doc.getChildNodes(RichText.class)`
- **Olvasható a NoteTag létrehozási ideje?** Igen, a `noteTag.getCreationTime()` segítségével
- **Szükségem van licencre a termeléshez?** Igen, érvényes Aspose.Note licenc szükséges
- **Kompatibilis-e az API a Java 8 és újabb verziókkal?** Teljes mértékben, támogatja a modern Java verziókat

## Mi az a “címkék kinyerése” a OneNote-ban?
A címkék kinyerése azt jelenti, hogy elolvassuk a metaadatokat (például állapot, címke, ikon és időbélyegek), amelyeket a OneNote a bekezdésekhez, jelölőnégyzetekhez vagy egyéb tartalomelemekhez csatol. Ezek a címkék `NoteTag` objektumokként tárolódnak a `RichText` csomópontokban.

## Miért használjuk az Aspose.Note-ot a címkék kinyeréséhez?
- **Nincs szükség OneNote telepítésre** – közvetlenül .one fájlokkal dolgozhat.
- **Teljes irányítás** – címke tulajdonságok lekérése, olvasása és módosítása programozottan.
- **Keresztplatformos** – bármely, Java-t támogató operációs rendszeren működik.

## Előfeltételek
- Java fejlesztői környezet (JDK 8+).
- Aspose.Note könyvtár letöltése [innen](https://releases.aspose.com/note/java/).
- Minta OneNote dokumentum (pl. `Sample1.one`) egy ismert könyvtárban.

## Csomagok importálása
Kezdjük azzal, hogy importáljuk a szükséges osztályokat. Ezek az importok hozzáférést biztosítanak a dokumentumkezeléshez, a címke interfészekhez és a rich‑text csomópontokhoz.

```java
import java.io.IOException;
import java.util.List;
import com.aspose.note.Document;
import com.aspose.note.ITag;
import com.aspose.note.NoteTag;
import com.aspose.note.RichText;
```

## Hogyan töltsük be a OneNote fájlt
Az első lépés a OneNote fájl betöltése egy `Document` objektumba.

```java
// The path to the documents directory.
String dataDir = "Your Document Directory";
// Load the document into Aspose.Note
Document doc = new Document(dataDir + "Sample1.one");
// Get all RichText nodes
List<RichText> nodes = doc.getChildNodes(RichText.class);
// Load the document into Aspose.Note
Document doc = new Document(dataDir + "Sample1.one");
```

> **Pro tipp:** Tartsd a `dataDir` útvonalat abszolútként, vagy használd a `Paths.get(...)`‑t az útvonallal kapcsolatos hibák elkerülése érdekében.

## Hogyan szerezzük meg a OneNote címkéket
A dokumentum betöltése után kérjük le az összes `RichText` csomópontot. Minden csomópont egy vagy több címkét is tartalmazhat.

```java
// Get all RichText nodes
List<RichText> nodes = doc.getChildNodes(RichText.class);
```

## Iterálás minden csomóponton
Iteráljunk végig minden `RichText` csomóponton, hogy megvizsgáljuk a benne lévő címkéket.

```java
// Iterate through each node
for (RichText richText : nodes) {
    // Process each node here
}
```

## NoteTag-ek lekérése (Hogyan módosítsuk a OneNote címkéket)
A cikluson belül ellenőrizzük, hogy egy címke `NoteTag`‑e. Ha igen, olvashatjuk a tulajdonságait – vagy módosíthatjuk őket, ha szükséges.

```java
for (ITag tag : richText.getTags()) {
    if (tag.getClass() == NoteTag.class) {
        NoteTag noteTag = (NoteTag) tag;
        // Retrieve properties
        System.out.println("Completed Time: " + noteTag.getCompletedTime());
        System.out.println("Create Time: " + noteTag.getCreationTime());
        System.out.println("Font Color: " + noteTag.getFontColor());
        System.out.println("Status: " + noteTag.getStatus());
        System.out.println("Label: " + noteTag.getLabel());
        System.out.println("Icon: " + noteTag.getIcon());
        System.out.println("High Light: " + noteTag.getHighlight());
        // Example of modifying a property
        // noteTag.setLabel("Updated Label");
    }
}
```

> **Figyelmeztetés:** Egy címke módosítása megváltoztatja az alapdokumentumot. Ne felejtsd el menteni a dokumentumot a módosítások után.

## Összegzés
Most már tudod, hogyan **címkék kinyerése**, hogyan **OneNote fájl betöltése**, hogyan **OneNote címkék lekérése**, és még hogyan **OneNote címkék módosítása** az Aspose.Note for Java segítségével. Integráld ezeket a kódrészleteket saját projektjeidbe a jegyzetek elemzésének, jelentéskészítésnek vagy migrációnak az automatizálásához.

## Gyakran ismételt kérdések
### Az Aspose.Note kompatibilis-e a OneNote összes verziójával?
Az Aspose.Note különféle OneNote fájlformátumokat támogat, biztosítva a kompatibilitást a különböző verziók között.

### Módosíthatom a lekért NoteTag tulajdonságokat?
Igen, az Aspose.Note lehetővé teszi a NoteTag tulajdonságok programozott módosítását és frissítését.

### Elérhető-e próbaverzió az Aspose.Note-hoz?
Természetesen! A ingyenes próbaverziót [itt](https://releases.aspose.com/) érheted el.

### Hol találok átfogó dokumentációt az Aspose.Note for Java-hoz?
A részletes dokumentációt [itt](https://reference.aspose.com/note/java/) tekintheted meg.

### Hol kaphatok támogatást bármilyen problémához vagy kérdéshez?
Látogass el a támogatási fórumra [itt](https://forum.aspose.com/c/note/28) az Aspose közösség segítségéért.

## Gyakran feltett kérdések
**Q:** *Kinyerhetek címkéket jelszóval védett OneNote fájlokból?*  
**A:** Igen, add meg a jelszót a `Document` objektum létrehozásakor.

**Q:** *Szükséges-e mentési metódust hívni a címkék módosítása után?*  
**A:** Teljesen szükséges. Használd a `doc.save("UpdatedSample.one");` parancsot a változások mentéséhez.

**Q:** *Lehetséges-e a címkék szűrése állapot szerint?*  
**A:** A `noteTag.getStatus()` ellenőrzésével a ciklusban csak a kívánt állapotú címkéket dolgozhatod fel.

**Q:** *Mi történik, ha egy RichText csomópontnak nincs címkéje?*  
**A:** A `richText.getTags()` egy üres gyűjteményt ad vissza; a ciklus egyszerűen átugorja azt.

**Q:** *Kötegelt feldolgozást tudok végezni több OneNote fájlon?*  
**A:** Csomagold be a fenti logikát egy fájl‑iterációs rutinba, és kezeld sorban az egyes dokumentumokat.

---

**Utolsó frissítés:** 2026-02-28  
**Tesztelve:** Aspose.Note for Java 24.12  
**Szerző:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}