---
date: 2026-10-26
description: Ismerje meg, hogyan lehet kinyerni a tags-et a OneNote fájlokból az Aspose.Note
  for Java használatával. Ez az útmutató bemutatja, hogyan töltsön be egy OneNote
  fájlt, szerezze meg a OneNote tags-et, és módosítsa a OneNote tags-et hatékonyan.
keywords:
- how to extract tags
- Aspose.Note Java
- OneNote tag extraction
- Java OneNote API
lastmod: 2026-10-26
linktitle: Hogyan nyerjünk ki tags-et a OneNote-ból – Aspose.Note
og_description: Ismerje meg, hogyan nyerhet ki tags-et a OneNote fájlokból az Aspose.Note
  for Java használatával. Kövesse a lépésről‑lépésre kódot a betöltéshez, olvasáshoz
  és a tags hatékony módosításához.
og_image_alt: Screenshot of Java code extracting OneNote tags with Aspose.Note
og_title: Hogyan nyerjünk ki tags-et a OneNote-ból az Aspose.Note segítségével – Java
  útmutató
schemas:
- author: Aspose
  dateModified: '2026-10-26'
  description: Learn how to extract tags from OneNote files using Aspose.Note for
    Java. This tutorial shows how to load OneNote file, get OneNote tags, and modify
    OneNote tags efficiently.
  headline: How to extract tags from OneNote with Aspose.Note
  type: TechArticle
- questions:
  - answer: '`Document`'
    question: What is the primary class for opening a OneNote file?
  - answer: '`doc.getChildNodes(RichText.class)`'
    question: Which method returns all RichText nodes?
  - answer: Yes, via `noteTag.getCreationTime()`
    question: Can you read a NoteTag’s creation time?
  - answer: Yes, a valid Aspose.Note license is required
    question: Do I need a license for production use?
  - answer: Absolutely, it supports modern Java versions
    question: Is the API compatible with Java 8 and later?
  type: FAQPage
second_title: Aspose.Note Java API
tags:
- OneNote
- Aspose.Note
- Java tag extraction
- document processing
- note tags
title: Hogyan lehet kinyerni a tags-et a OneNote-ból az Aspose.Note segítségével
url: /hu/java/onenote-tag-operations/get-node-tags/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hogyan lehet címkéket kinyerni a OneNote-ból az Aspose.Note segítségével

## Bevezetés
Ha **címkék kinyerésére** van szüksége egy OneNote dokumentumból, jó helyen jár. Ebben az útmutatóban végigvezetjük a OneNote fájl betöltésének, a OneNote címkék lekérésének, és még a címkék módosításának folyamatát az Aspose.Note for Java segítségével. A tutorial végére magabiztosan be tudja illeszteni a címke‑kinyerést bármely Java alkalmazásba.

## Gyors válaszok
- **Mi a fő osztály a OneNote fájl megnyitásához?** `Document`
- **Melyik metódus adja vissza az összes RichText csomópontot?** `doc.getChildNodes(RichText.class)`
- **Kiolvasható egy NoteTag létrehozási ideje?** Igen, a `noteTag.getCreationTime()` segítségével
- **Szükség van licencre a termelésben való használathoz?** Igen, érvényes Aspose.Note licenc szükséges
- **Az API kompatibilis a Java 8‑al és újabb verziókkal?** Teljesen, támogatja a modern Java verziókat

## Mi az a „címkék kinyerése” a OneNote-ban?
A címkék kinyerése azt jelenti, hogy a `NoteTag` metaadatot olvassuk ki, amely a OneNote tartalomelemekhez (például bekezdésekhez, jelölőnégyzetekhez vagy listaelemekhez) van csatolva. Ezek a címkék állapotot, címkét, ikont és időbélyegeket tárolnak, és `NoteTag` objektumokként jelennek meg a `RichText` csomópontokban, lehetővé téve a programozott vizsgálatot vagy módosítást.

## Miért használja az Aspose.Note-ot a címkék kinyeréséhez?
Feldolgozhat OneNote fájlokat anélkül, hogy telepítené a OneNote asztali alkalmazást, ezáltal akár 150 MB‑kal is csökkentve a telepítési méretet. A könyvtár Windows, macOS és Linux rendszereken fut, támogatja a Java 8‑tól a Java 17 LTS‑ig, így valódi keresztplatformos megoldást nyújt. Emellett teljes olvasási/írási hozzáférést biztosít több mint 50 címkéhez kapcsolódó tulajdonsághoz, lehetővé téve a tömeges elemzést vagy migrációs forgatókönyveket.

## Előfeltételek
- Java fejlesztői környezet (JDK 8+).
- Aspose.Note könyvtár letöltve a [Aspose.Note for Java letöltési oldalról](https://releases.aspose.com/note/java/).
- Egy minta OneNote dokumentum (pl. `Sample1.one`) egy ismert könyvtárban.

## Csomagok importálása
Kezdje el a szükséges osztályok importálásával. Ezek az importok hozzáférést biztosítanak a dokumentumkezeléshez, a címke‑interfészekhez és a rich‑text csomópontokhoz.

```java
import java.io.IOException;
import java.util.List;
import com.aspose.note.Document;
import com.aspose.note.ITag;
import com.aspose.note.NoteTag;
import com.aspose.note.RichText;
```

## Hogyan töltsünk be OneNote fájlt
Töltsük be a `.one` fájlt egy új `Document` példány létrehozásával, például: `Document doc = new Document(dataDir + "Sample1.one");`. Ez a jegyzetfüzetet memóriába olvassa, és előkészíti a címke‑műveletekhez.

A `Document` osztály egy OneNote fájlt képvisel memóriában, és módszereket biztosít a tartalom olvasásához és módosításához.

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

> **Pro tip:** Tartsa a `dataDir` útvonalat abszolútként, vagy használja a `Paths.get(...)`‑t az útvonallal kapcsolatos hibák elkerülése érdekében.

## Hogyan szerezzünk OneNote címkéket
Szerezze be az összes `RichText` csomópontot a `doc.getChildNodes(RichText.class)` hívással, amely egy gyűjteményt ad vissza, amely egy vagy több `NoteTag` objektumot tartalmazhat. Ezután iterálhat a gyűjteményen, hogy megvizsgálja minden csomópont címkéit.

Egy `RichText` csomópont egy bekezdést vagy szövegtömböt jelent a OneNote-ban, és több címkét is tárolhat.

```java
// Get all RichText nodes
List<RichText> nodes = doc.getChildNodes(RichText.class);
```

## Iterálás minden csomóponton
Használjon egy for‑each ciklust a `RichText` gyűjteményen, ellenőrizve minden csomópont címkelistáját, hogy feldolgozza a csatolt `NoteTag` objektumokat. A cikluson belül olvashatja például az állapotot vagy a létrehozási időt, vagy szükség esetén módosíthatja azokat.

```java
// Iterate through each node
for (RichText richText : nodes) {
    // Process each node here
}
```

## Jegycímkék lekérése (hogyan módosítsuk a OneNote címkéket)
A csomópont cikluson belül használja a `richText.getTags()`‑t a címkelista lekéréséhez, szűrje le a `NoteTag` példányokat, majd olvassa vagy állítsa be a `setStatus` vagy `setLabel` tulajdonságokat, mielőtt elmenti a dokumentumot.

A `NoteTag` osztály egy OneNote címkét kapszuláz, és olyan tulajdonságokat tesz elérhetővé, mint állapot, címke, ikon, létrehozási idő és szerző.

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

> **Warning:** Egy címke módosítása megváltoztatja a dokumentum alapját. Ne felejtse el elmenteni a dokumentumot a módosítások után.

## Összegzés
Most már tudja, **hogyan kell címkéket kinyerni**, **hogyan kell OneNote fájlt betölteni**, **hogyan kell OneNote címkéket lekérni**, és még **hogyan kell OneNote címkéket módosítani** az Aspose.Note for Java segítségével. Illessze be ezeket a kódrészleteket saját projektjeibe a jegyzet‑elemzés, jelentéskészítés vagy migráció automatizálásához.

## GYIK
### Az Aspose.Note kompatibilis-e a OneNote minden verziójával?
Az Aspose.Note különböző OneNote fájlformátumokat támogat, biztosítva a kompatibilitást a különböző verziók között.

### Módosíthatom a lekért NoteTag tulajdonságokat?
Igen, az Aspose.Note lehetővé teszi a NoteTag tulajdonságok programozott módosítását és frissítését.

### Elérhető próba verzió az Aspose.Note‑hoz?
Természetesen! A ingyenes próba verziót elérheti a [Aspose ingyenes próba letöltési oldalán](https://releases.aspose.com/).

### Hol találhatók a részletes dokumentációk az Aspose.Note for Java‑hoz?
Fedezze fel a részletes dokumentációt a [Aspose.Note Java API dokumentációban](https://reference.aspose.com/note/java/).

### Hogyan kaphatok támogatást bármilyen problémához vagy kérdéshez?
Látogasson el a támogatási fórumra: [Aspose.Note támogatási fórum](https://forum.aspose.com/c/note/28), ahol az Aspose közösség segíthet.

## Gyakran Ismételt Kérdések
**Q:** *Kinyerhetek címkéket jelszóval védett OneNote fájlokból?*  
**A:** Igen, adja meg a jelszót a `Document` objektum létrehozásakor.

**Q:** *Meg kell hívnom egy mentési metódust a címkék módosítása után?*  
**A:** Teljesen igaz. Használja a `doc.save("UpdatedSample.one");` parancsot a változások mentéséhez.

**Q:** *Lehet szűrni a címkéket állapot szerint?*  
**A:** A ciklusban ellenőrizheti a `noteTag.getStatus()` értékét, és csak a kívánt állapotokat dolgozhatja fel.

**Q:** *Mi történik, ha egy RichText csomópontnak nincs címkéje?*  
**A:** A `richText.getTags()` egy üres gyűjteményt ad vissza; a ciklus egyszerűen átugorja azt.

**Q:** *Tömegesen feldolgozhatok több OneNote fájlt?*  
**A:** Csomagolja be a fenti logikát egy fájl‑iterációs rutinba, és kezelje a dokumentumokat sorban.

---

**Last Updated:** 2026-10-26  
**Tested With:** Aspose.Note for Java 24.12  
**Author:** Aspose

## Kapcsolódó oktatóanyagok

- [Create Notebook Object Java – Load OneNote File with Options - Aspose.Note](/note/java/onenote-notebook-operations/load-notebook-file-with-load-options/)
- [Convert OneNote to Plain Text – Extract All Text with Aspose.Note for Java](/note/java/onenote-text-manipulation/extract-all-text/)
- [Retrieve OneNote attachments using Aspose.Note for Java](/note/java/onenote-java-integration/retrieve-attachment/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}