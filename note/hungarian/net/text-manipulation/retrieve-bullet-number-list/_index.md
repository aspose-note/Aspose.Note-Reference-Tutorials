---
title: Felsorolás vagy számlista lekérése Aspose.Note szövegben
linktitle: Felsorolás vagy számlista lekérése Aspose.Note szövegben
second_title: Aspose.Note .NET API
description: Kiaknázza az Aspose.Note for .NET-ben rejlő lehetőségeket a felsorolás- vagy számlisták lekéréséhez szükséges lépésről lépésre szóló útmutatónkkal. Növelje OneNote dokumentumkezelési készségeit!
weight: 23
url: /hu/net/text-manipulation/retrieve-bullet-number-list/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Felsorolás vagy számlista lekérése Aspose.Note szövegben

## Bevezetés
Üdvözöljük az Aspose.Note for .NET világában, egy robusztus és sokoldalú könyvtár, amely lehetővé teszi a fejlesztők számára, hogy könnyedén kezeljék a OneNote dokumentumkezelést. Ebben az oktatóanyagban a felsorolásjel- vagy számlisták lekérésének folyamatát mutatjuk be az Aspose.Note for .NET használatával. Akár tapasztalt fejlesztő, akár kódolás-rajongó, ez az útmutató felvértezi azokat a tudást, amelyek segítségével eligazodhat az Aspose.Note listákkal való munka során.
## Előfeltételek
Mielőtt nekivágnánk ennek a kódolási útnak, győződjön meg arról, hogy a következő előfeltételek teljesülnek:
-  Aspose.Note .NET esetén: Győződjön meg arról, hogy telepítve van az Aspose.Note könyvtár. Ha nem, akkor letöltheti a[Aspose.Note a .NET dokumentációhoz](https://reference.aspose.com/note/net/).
- Fejlesztési környezet: Állítson be egy működő fejlesztői környezetet, lehetőleg a Microsoft Visual Studio-t a gépén.
- Alapvető C# ismerete: Ismerkedjen meg a C# nyelvvel, mivel ez az oktatóanyag ezen a nyelven készült.
## Névterek importálása
Az Aspose.Note for.NET-hez való interakcióhoz importálnia kell a szükséges névtereket a projektbe. A kód elejére írja be a következő névtereket:
```csharp
using System;
using System.Globalization;
using System.IO;
using Aspose.Note;
using System.Collections.Generic;
```
Most bontsuk le a felsorolás- vagy számlisták lekérésének folyamatát lépésről lépésre:
## 1. lépés: Állítsa be a dokumentumkönyvtárat
```csharp
// A dokumentumok könyvtárának elérési útja.
string dataDir = "Your Document Directory";
```
 Cserélje ki`"Your Document Directory"` azzal a tényleges elérési úttal, ahol az Aspose.Note dokumentum található.
## 2. lépés: Töltse be a dokumentumot
```csharp
// Töltse be a dokumentumot az Aspose.Note-ba.
Document oneFile = new Document(dataDir + "ApplyNumberingOnText.one");
```
 Győződjön meg róla, hogy kicserélte`"ApplyNumberingOnText.one"` az adott OneNote-dokumentum nevével.
## 3. lépés: A csomópontok gyűjteményének lekérése
```csharp
// A körvonalelem csomópontjainak gyűjteményének lekérése.
IList<OutlineElement> nodes = oneFile.GetChildNodes<OutlineElement>();
```
Ez a lépés vázlatcsomópont-gyűjteményt kér le a betöltött dokumentumból.
## 4. lépés: Ismétlés minden csomóponton keresztül
```csharp
// Iteráljon minden csomóponton keresztül.
foreach (OutlineElement node in nodes)
{
    if (node.NumberList != null)
    {
        NumberList list = node.NumberList;
        // Folytassa a következő lépésekkel...
    }
}
```
Ez a ciklus biztosítja, hogy csak olyan csomópontokkal foglalkozzunk, amelyek számlistát tartalmaznak.
## 5. lépés: A betűtípus információinak lekérése
```csharp
// Betűtípus nevének lekérése
Console.WriteLine("Font Name: " + list.Font);
// Betűhossz lekérése
Console.WriteLine("Font Length: " + list.Font.Length);
// Betűméret lekérése
Console.WriteLine("Font Size: " + list.FontSize);
// Betűszín lekérése
Console.WriteLine("Font Color: " + list.FontColor);
// Formátum lekérése
Console.WriteLine("Font format: " + list.Format);
// Jelölje félkövér
Console.WriteLine("Is bold: " + list.IsBold);
// Jelölje be a dőlt betűt
Console.WriteLine("Is italic: " + list.IsItalic);
Console.WriteLine();
```
Ezek a kódsorok különféle betűtípusokkal kapcsolatos információkat vonnak ki a számlistából.
## Következtetés
 Gratulálunk! Sikeresen megtanulta a felsorolásjel- vagy számlisták lekérését az Aspose.Note for .NET használatával. Ahogy folytatja a felfedezést, tekintse meg a[dokumentáció](https://reference.aspose.com/note/net/) mélyebb betekintést és funkciókat.
## GYIK
### Használhatom az Aspose.Note for .NET programot más programozási nyelvekkel?
Az Aspose.Note elsősorban a .NET-et támogatja, de vannak a könyvtárnak más verziói is, amelyek különböző platformokhoz és nyelvekhez vannak szabva.
### Az Aspose.Note kompatibilis a legújabb OneNote-formátumokkal?
Igen, az Aspose.Note a OneNote formátumok széles skáláját támogatja, így biztosítja a kompatibilitást a legújabb verziókkal.
### Hogyan szerezhetek ideiglenes licencet az Aspose.Note számára?
 Látogatás[ez a link](https://purchase.aspose.com/temporary-license/) ideiglenes engedély megszerzésére értékelési célból.
### Milyen támogatási lehetőségek állnak rendelkezésre az Aspose.Note felhasználók számára?
Feltérképezheti és segítséget kérhet a[Aspose.Note fórum](https://forum.aspose.com/c/note/28) az esetlegesen felmerülő kérdésekre vagy problémákra.
### Létezik az Aspose.Note ingyenes próbaverziója .NET-hez?
 Igen, elérheti az Aspose.Note .NET ingyenes próbaverzióját[itt](https://releases.aspose.com/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
