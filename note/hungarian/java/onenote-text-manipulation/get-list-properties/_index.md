---
date: 2026-03-08
description: Tanulja meg, hogyan lehet kinyerni a listajellemzőket a OneNote dokumentumokból
  az Aspose.Note for Java segítségével. Ez a lépésről‑lépésre útmutató megmutatja
  a szükséges pontos kódot és tippeket.
linktitle: How to Extract List Properties in OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: Hogyan lehet kinyerni a lista tulajdonságait a OneNote-ban – Aspose.Note
url: /hu/java/onenote-text-manipulation/get-list-properties/
weight: 19
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hogyan vonjunk ki lista tulajdonságokat a OneNote-ból – Aspose.Note

## Bevezetés
Ebben az útmutatóban megtudja, **hogyan vonjon ki lista** tulajdonságokat egy OneNote fájlból az Aspose.Note for Java segítségével. Akár betűtípus‑adatokra, listaformázásra vagy stílusattribútumokra van szüksége, ez a leírás minden lépésen végigvezet – a dokumentum betöltésétől a kinyert értékek kiírásáig. A végére egy kész, használatra kész kódrészletet kap, amely bármely Java‑alapú dokumentumfeldolgozó csővezetékbe integrálható.

## Gyors válaszok
- **Mit jelent a „lista kinyerése”?** A számozott vagy felsorolásos listák formázási részleteinek (betűtípus, méret, szín, stílus) olvasását jelenti, amelyek egy OneNote vázlatban tárolódnak.  
- **Melyik könyvtár szükséges?** Aspose.Note for Java (legújabb verzió).  
- **Szükségem van licencre a teszteléshez?** Igen, egy ideiglenes licenc ajánlott nem‑produkciós futtatásokhoz.  
- **Futtatható ez bármely operációs rendszeren?** A Java API Windows, Linux és macOS rendszereken működik.  
- **Mennyi időt vesz igénybe a megvalósítás?** Általában 10 perc alatt elvégezhető egy alapbeállítás.

## Mi a „lista kinyerése” a OneNote kontextusában?
A OneNote minden listaelemet egy `OutlineElement`‑ként tárol, amely tartalmazhat egy `NumberList` objektumot. A lista kinyerése azt jelenti, hogy hozzáférünk ennek az objektumnak a tulajdonságaihoz – például betűtípus‑név, méret, szín és formázás – hogy programozottan elemezhessük vagy módosíthassuk őket.

## Miért használjuk az Aspose.Note for Java‑t a lista tulajdonságok kinyeréséhez?
- **Nincs COM interop** – Teljesen Java‑ban működik, anélkül, hogy a Windows OneNote kliensre lenne szükség.  
- **Teljes hűség** – Megőrzi az összes formázási részletet, beleértve az egyedi betűtípusokat és színeket.  
- **Kereszt‑platform** – Ugyanaz a kód futtatható bármely szerver‑oldali környezetben.  
- **Gazdag API** – Közvetlen hozzáférést biztosít a listaobjektumokhoz, így a tulajdonságok kinyerése egyszerű.

## Előfeltételek
Mielőtt elkezdené, győződjön meg róla, hogy a következők rendelkezésre állnak:

- Aspose.Note for Java: Töltse le a legújabb kiadást **[itt](https://releases.aspose.com/note/java/)**.  
- Java fejlesztői környezet (JDK 8 vagy újabb).  
- OneNote dokumentum (pl. `Sample1.one`) egy ismert könyvtárban elhelyezve.

## Csomagok importálása
Először importálja a szükséges osztályokat. Ez hozzáférést biztosít az Aspose.Note alapfunkcióihoz.

```java
import java.io.IOException;
import java.util.List;
import com.aspose.note.Document;
import com.aspose.note.NumberList;
import com.aspose.note.OutlineElement;
```

Most lépésről lépésre végigvezetjük a megvalósításon.

## Lista tulajdonságok kinyerése – Lépésről lépésre útmutató

### 1. lépés: OneNote dokumentum betöltése
Adja meg a `.one` fájl helyes elérési útját, és hozza létre a `Document` példányt.

```java
// The path to the documents directory.
String dataDir = "Your Document Directory";

// Load the document into Aspose.Note
Document oneFile = new Document(dataDir + "Sample1.one");
```

> **Pro tipp:** Használjon abszolút útvonalakat, vagy állítson be relatív útvonalat a projekt erőforrásmappája alapján, hogy elkerülje a `FileNotFoundException` hibát.

### 2. lépés: Az outline csomópontok gyűjteményének lekérése
Minden lista egy `OutlineElement`‑ben található. Húzza ki az összes ilyen elemet a dokumentumból.

```java
// Retrieve a collection of nodes of the outline element
List<OutlineElement> nodes = oneFile.getChildNodes(OutlineElement.class);
```

### 3. lépés: Iteráljon a csomópontokon, és keresse meg a listákat
Iteráljon minden csomóponton, ellenőrizve, hogy tartalmaz‑e `NumberList`‑et. Ha igen, tárolja a hivatkozást a későbbi kinyeréshez.

```java
// Iterate through each node
for (OutlineElement node : nodes) {
    if (node.getNumberList() != null) {
        NumberList list = node.getNumberList();
        // Continue with further operations on list properties
    }
}
```

### 4. lépés: A kívánt lista tulajdonságok kinyerése
A cikluson belül most már olvashat bármely attribútumot, amelyet a `NumberList` osztály biztosít.

```java
// Retrieve font name
System.out.println("Font Name: " + list.getFont());
// Retrieve font length (character count)
System.out.println("Font Length: " + list.getFont());
// Retrieve font size
System.out.println("Font Size: " + list.getFontSize());
// Retrieve font color
System.out.println("Font Color: " + list.getFontColor());
// Retrieve format (e.g., decimal, lowerLetter)
System.out.println("Font format: " + list.getFormat());
// Check bold style
System.out.println("Is bold: " + list.isBold());
// Check italic style
System.out.println("Is italic: " + list.isItalic());
```

A konzol kimenete megjeleníti minden tulajdonságot, lehetővé téve a naplózást, elemzést vagy a lista stílusinformációinak további feldolgozását.

## Gyakori problémák és hibaelhárítás
| Tünet | Valószínű ok | Megoldás |
|-------|--------------|----------|
| `NullPointerException` a `list.getFont()`‑nál | A csomópont nem tartalmaz `NumberList`‑et. | Adjon hozzá null‑ellenőrzést (`if (node.getNumberList() != null)`). |
| Nem jelenik meg kimenet | `dataDir` a rossz mappára mutat. | Ellenőrizze az útvonalat, és győződjön meg róla, hogy a `Sample1.one` létezik. |
| A betűszín `null`‑ként jelenik meg | A lista az alapértelmezett téma színét használja. | Használja a `list.getFontColor()`‑t, és adjon meg tartalékot a dokumentum témájából. |

## Gyakran Ismételt Kérdések

**Q: Az Aspose.Note kompatibilis a különböző OneNote verziókkal?**  
A: Igen, az Aspose.Note széles körű OneNote fájlformátumot támogat, a régebbi 2007‑es verzióktól a legújabb Office 365 kiadásokig.

**Q: Testreszabhatom, hogy mely betűtípus‑attribútumok legyenek lekérve?**  
A: Természetesen. Hívhatja csak a szükséges gettereket (pl. `getFontSize()` vagy `isBold()`), a többit pedig figyelmen kívül hagyhatja.

**Q: Hol találok további támogatást vagy segítséget?**  
A: Bármilyen kérdés vagy probléma esetén látogassa meg az [Aspose.Note fórumot](https://forum.aspose.com/c/note/28) a gyors segítségért.

**Q: Szükségem van licencre a teszteléshez?**  
A: Igen, ideiglenes licencet szerezhet **[itt](https://purchase.aspose.com/temporary-license/)** értékelési célokra.

**Q: Mit tehetek, ha meg akarom vásárolni az Aspose.Note for Java‑t?**  
A: A terméket **[itt](https://purchase.aspose.com/buy)** vásárolhatja meg, hogy teljes körűen kiaknázza a projektjei számára.

---

**Utolsó frissítés:** 2026-03-08  
**Tesztelve a következővel:** Aspose.Note for Java (legújabb kiadás)  
**Szerző:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}