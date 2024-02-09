---
title: Jelölje ki az összes legutóbbi változást az Aspose.Note szövegben
linktitle: Jelölje ki az összes legutóbbi változást az Aspose.Note szövegben
second_title: Aspose.Note .NET API
description: Javítsa Note dokumentumait az Aspose.Note for .NET segítségével! Ebből a lépésről lépésre mutató oktatóanyagból megtudhatja, hogyan emelheti ki a legutóbbi módosításokat a szövegben.
type: docs
weight: 19
url: /hu/net/text-manipulation/highlight-recent-changes/
---
## Bevezetés
Dinamikus és tetszetős funkciókat szeretne hozzáadni Note dokumentumaihoz .NET használatával? Az Aspose.Note for .NET egy hatékony megoldás, amely lehetővé teszi a Note-fájlok zökkenőmentes kezelését és javítását. Ebben az oktatóanyagban egy konkrét szempontot fejtünk ki: kiemeljük az Aspose.Note szövegben legutóbbi módosításokat.
## Előfeltételek
Mielőtt nekivágnánk ennek az útnak, győződjön meg arról, hogy a következő előfeltételeket teljesíti:
-  Aspose.Note .NET esetén: Győződjön meg arról, hogy telepítve van az Aspose.Note könyvtár. Letöltheti a[Aspose.Note a .NET dokumentációhoz](https://reference.aspose.com/note/net/).
- Fejlesztői környezet: Állítson be .NET fejlesztői környezetet, beleértve a Visual Studio-hoz hasonló IDE-t.
- Mintadokumentum: Készítsen jegyzetdokumentumot (jelen esetben "Aspose.one"), amely tartalmazza a kiemelni kívánt szöveget.
## Névterek importálása
A kezdéshez importálja a szükséges névtereket a .NET-projektbe:
```csharp
    using System;
    using System.Drawing;
    using System.IO;
    using System.Linq;
```
## 1. lépés: Töltse be a dokumentumot
Először töltse be a Note dokumentumot az Aspose-ba.Note:
```csharp
string dataDir = "Your Document Directory";
Document document = new Document(dataDir + "Aspose.one");
```
## 2. lépés: A legutóbbi módosítások azonosítása
Ezután azonosítsa az elmúlt héten módosított RichText csomópontokat:
```csharp
var richTextNodes = document.GetChildNodes<RichText>().Where(e => e.LastModifiedTime >= DateTime.Today.Subtract(TimeSpan.FromDays(7)));
```
## 3. lépés: Állítsa be a kiemelési színeket
Most állítsa be a kiemelés színét az azonosított csomópontokhoz és a szövegfuttatásokhoz:
```csharp
foreach (var node in richTextNodes)
{
    // Állítsa be a bekezdés kiemelési színét
    node.ParagraphStyle.Highlight = Color.DarkGreen;
    // Állítsa be a kiemelés színét minden szövegfuttatáshoz
    foreach (var run in node.TextRuns)
    {
        run.Style.Highlight = Color.DarkSeaGreen;
    }
}
```
## 4. lépés: Mentse el a módosított dokumentumot
Mentse el a dokumentumot a legutóbbi kiemelt módosításokkal:
```csharp
document.Save(Path.Combine(dataDir, "HighlightAllRecentChanges.pdf"));
```
## 5. lépés: Jelenítse meg a sikeres üzenetet
Végül jelenítsen meg egy sikerüzenetet, amely tájékoztatja a felhasználót:
```csharp
Console.WriteLine("\nText's recent changes are highlighted successfully.");
```
## Következtetés
Ebben az oktatóanyagban megvizsgáltuk, hogyan használhatja az Aspose.Note for .NET-et a Note-dokumentum szövegében a legutóbbi változások kiemelésére. Ez a funkció javítja a dokumentumok láthatóságát, és értékes kiegészítője a Note fájlokkal való munkavégzés eszköztárának.
## GYIK
### Alkalmazhatok különböző kiemelési színeket különböző időszakokra?
Igen, testreszabhatja a kódot, hogy az Ön egyedi igényei alapján különböző kiemelési színeket állítson be.
### Az Aspose.Note kompatibilis a legújabb .NET keretrendszerekkel?
Az Aspose.Note rendszeresen frissíti a könyvtárait, hogy biztosítsa a kompatibilitást a legújabb .NET-keretrendszerekkel.
### Hogyan kezelhetem a hibákat a funkció alkalmazása során?
Beépíthet try-catch blokkokat a kivételek kezelésére és a zökkenőmentes felhasználói élmény biztosítására.
### Az Aspose.Note támogat más szövegformázási funkciókat?
Teljesen! Az Aspose.Note szolgáltatások széles skáláját kínálja a szöveg formázásához, beleértve a betűstílusokat, -méreteket és egyebeket.
### Integrálhatom ezt a megoldást egy webalkalmazásba?
Igen, az Aspose.Note for .NET webalkalmazásokba integrálható a dokumentumfeldolgozási képességek javítása érdekében.