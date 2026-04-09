---
date: 2026-04-09
description: Tanulja meg, hogyan lehet kinyerni a képek metaadatait és lekérni a képméreteket
  OneNote-fájlokból az Aspose.Note for .NET segítségével. Lépésről lépésre útmutató
  C# fejlesztőknek.
keywords:
- extract image metadata
- how to extract images
- get image dimensions
- load onenote document
- c# get image properties
linktitle: Hogyan lehet képadatokat kinyerni a OneNote-ból az Aspose.Note segítségével
second_title: Aspose.Note .NET API
title: Hogyan lehet képadatokat kinyerni a OneNote-ból az Aspose.Note segítségével
url: /hu/net/images/get-info-of-images/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Kép metaadatok kinyerése az Aspose.Note for .NET segítségével

Ebben a gyakorlati útmutatóban megtanulja, **hogyan kell kinyerni a kép metaadatokat** – beleértve a szélességet, magasságot, az eredeti méretet, a fájlnevet és a módosítási időt – a Microsoft OneNote fájlokból az Aspose.Note C# könyvtár segítségével. Akár képkicsiket kell megjelenítenie, képméreteket ellenőriznie, vagy beágyazott eszközök katalógusát építené, a metaadatok programozott kinyerése rengeteg manuális lépést takarít meg.

## Gyors válaszok
- **Mi jelent a „kép metaadatok kinyerése”?** A képekhez tartozó tulajdonságok, például méretek, fájlnév és időbélyegek lekérése egy OneNote dokumentumban tárolt képekből.  
- **Melyik könyvtár kezeli ezt?** Aspose.Note for .NET.  
- **Szükségem van licencre?** A fejlesztéshez ingyenes próba verzió működik; a termeléshez kereskedelmi licenc szükséges.  
- **Támogatott platformok?** .NET Framework 4.6+, .NET Core 3.1+, .NET 5/6+.  
- **Tipikus futási idő?** Kevesebb mint egy másodperc egy standard .one fájl esetén.

## Mi az a kép metaadatok kinyerése?
A kép metaadatok kinyerése azt jelenti, hogy programozottan beolvassuk a leíró attribútumokat (szélesség, magasság, eredeti méretek, fájlnév, utolsó módosítás időpontja stb.), amelyek minden képobjektumhoz tartoznak egy OneNote oldalán. Ezek az adatok hasznosak az ellenőrzéshez, jelentéskészítéshez vagy további képfeldolgozáshoz.

## Miért kell kinyerni a kép metaadatokat a OneNote-ból?
- **Automatizálás** – Olyan eszközök építése, amelyek automatikusan generálják a kép leltárakat.  
- **Érvényesítés** – Biztosítsa, hogy a képek megfeleljenek a méretkövetelményeknek a közzététel előtt.  
- **Integráció** – A OneNote tartalom kombinálása más rendszerekkel, amelyeknek szükségük van a kép részleteire (CMS, DAM stb.).  
- **Teljesítmény** – Kerülje el a teljes kép binárisok betöltését, ha csak a méretekre van szükség.

## Előfeltételek
1. **C# alapok** – Kényelmesen kell tudnia alap C# kódot írni.  
2. **Aspose.Note for .NET** – Töltse le és telepítse a könyvtárat a hivatalos oldalról [itt](https://releases.aspose.com/note/net/).  
3. **OneNote (.one) fájl** – Bármely meglévő OneNote dokumentum, amely képeket tartalmaz.

## Névtér importálása
Mielőtt elkezdenénk, importálja a szükséges névtereket:

```csharp
using System.IO;
using Aspose.Note;
using System.Collections.Generic;
using System;
```

## 1. lépés: OneNote dokumentum betöltése
Először töltse be a cél OneNote fájlt egy `Aspose.Note.Document` objektumba. Ez a **load onenote document** lépés, amely előkészíti az API-t a további lekérdezésekhez.

```csharp
// The path to the documents directory.
string dataDir = "Your Document Directory";

// Load the document into Aspose.Note.
Document oneFile = new Document(dataDir + "Aspose.one");
```

Cserélje le a `"Your Document Directory"` értéket a tényleges mappára, amely a `.one` fájlt tartalmazza.

## 2. lépés: Az összes képcsomópont lekérése
Most **how to extract images**-t fogjuk végrehajtani, az összes `Image` csomópont lekérésével a dokumentumból.

```csharp
// Get all Image nodes
IList<Aspose.Note.Image> images = oneFile.GetChildNodes<Aspose.Note.Image>();
```

A `GetChildNodes<T>()` metódus átvizsgálja az egész jegyzetfüzet hierarchiáját, és egy képobjektumok gyűjteményét adja vissza.

## 3. lépés: Végigiterálás minden képen és **c# get image properties**
Végigiterálunk a gyűjteményen, és kiírjuk a metaadatokat, beleértve a **get image dimensions** és **extract original image size** értékeket.

```csharp
foreach (Aspose.Note.Image image in images)
{
    Console.WriteLine("Width: {0}", image.Width);
    Console.WriteLine("Height: {0}", image.Height);
    Console.WriteLine("OriginalWidth: {0}", image.OriginalWidth);
    Console.WriteLine("OriginalHeight: {0}", image.OriginalHeight);
    Console.WriteLine("FileName: {0}", image.FileName);
    Console.WriteLine("LastModifiedTime: {0}", image.LastModifiedTime);
    Console.WriteLine();
}
```

A kimenet megjeleníti minden kép aktuális szélességét/magasságát (ahogyan az oldalon megjelenik), a fájlban tárolt eredeti méreteket, a fájlnevet és az utolsó módosítás időbélyegét.

## Gyakori problémák és megoldások
| Probléma | Ok | Megoldás |
|----------|----|----------|
| **NullReferenceException** when `images` is empty | A dokumentum nem tartalmaz képeket | Ellenőrizze, hogy a forrás `.one` fájl valóban beágyazott képeket tartalmaz. |
| **Incorrect dimensions** | A képek mérete a OneNote-ban skálázott | Használja az `OriginalWidth`/`OriginalHeight` értékeket a valódi méret meghatározásához. |
| **FileName is empty** | A kép a vágólapról lett beillesztve | Az API esetleg nem rendelkezik fájlnévvel; kezelje a `null` vagy üres karakterláncokat a kódban. |

## Gyakran ismételt kérdések

**K: Az Aspose.Note kompatibilis a Microsoft OneNote minden verziójával?**  
A: Az Aspose.Note támogatja a .one, .onepkg és .onetoc2 formátumokat, amelyek lefedik a legtöbb OneNote verziót 2007-től napjainkig.

**K: Módosíthatom a kép tulajdonságait a kinyerés után?**  
A: Igen, módosíthatja a `Width`, `Height` vagy `FileName` tulajdonságokat, majd elmentheti a dokumentumot.

**K: Az Aspose.Note működik .NET Core‑dal?**  
A: Teljesen. A könyvtár teljes mértékben kompatibilis a .NET Core, .NET 5 és .NET 6 verziókkal.

**K: Elérhető ingyenes próba?**  
A: Igen, letölthet egy próba verziót az Aspose weboldaláról, hogy felfedezze az összes funkciót.

**K: Hol kaphatok további segítséget vagy közösségi támogatást?**  
A: Látogassa meg az Aspose.Note fórumot [itt](https://forum.aspose.com/c/note/28) tippek, minta kódok és a közösség válaszaiért.

---

**Utoljára frissítve:** 2026-04-09  
**Tesztelve:** Aspose.Note 24.11 for .NET  
**Szerző:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}