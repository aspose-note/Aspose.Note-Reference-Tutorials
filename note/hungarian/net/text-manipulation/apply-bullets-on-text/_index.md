---
title: Alkalmazzon felsorolásjeleket a szövegre az Aspose.Note-ban
linktitle: Alkalmazzon felsorolásjeleket a szövegre az Aspose.Note-ban
second_title: Aspose.Note .NET API
description: Ismerje meg, hogyan alkalmazhat felsorolásjeleket a szövegre az Aspose.Note for .NET-ben a OneNote-dokumentumok javítása érdekében. Kövesse ezt a lépésről lépésre szóló útmutatót a hatékony formázáshoz.
weight: 10
url: /hu/net/text-manipulation/apply-bullets-on-text/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Alkalmazzon felsorolásjeleket a szövegre az Aspose.Note-ban

## Bevezetés
Üdvözöljük ebben a lépésenkénti útmutatóban a felsorolásjelek szövegre történő alkalmazásáról az Aspose.Note for .NET használatával. Az Aspose.Note egy hatékony könyvtár, amely lehetővé teszi a fejlesztők számára, hogy zökkenőmentesen dolgozzanak a Microsoft OneNote fájlokkal .NET-alkalmazásaikban. Ebben az oktatóanyagban végigvezetjük a felsorolásjelek szövegre történő alkalmazásának folyamatán, ezzel javítva a OneNote-dokumentumok vizuális vonzerejét.
## Előfeltételek
Mielőtt belevágnánk az oktatóanyagba, győződjön meg arról, hogy rendelkezik a következő előfeltételekkel:
- C# és .NET programozási alapismeretek.
-  Aspose.Note for .NET könyvtár telepítve. Letöltheti[itt](https://releases.aspose.com/note/net/).
## Névterek importálása
Győződjön meg arról, hogy a C# kódban szerepelteti a szükséges névtereket:
```csharp
using System;
using System.Globalization;
using System.IO;
using Aspose.Note;
using System.Drawing;
using System.Collections.Generic;
```
## 1. lépés: Állítsa be a dokumentumot
```csharp
// A dokumentumok könyvtárának elérési útja.
string dataDir = "Your Document Directory";
//Hozzon létre egy objektumot a Dokumentum osztályból
Aspose.Note.Document doc = new Aspose.Note.Document();
```
## 2. lépés: Inicializálja az oldalt és a körvonalat
```csharp
// Oldal osztály objektum inicializálása
Aspose.Note.Page page = new Aspose.Note.Page(doc);
// Inicializálja az Outline osztály objektumot
Outline outline = new Outline(doc);
```
## 3. lépés: Állítsa be az alapértelmezett szövegstílust
```csharp
// Inicializálja a TextStyle osztályobjektumot, és állítsa be a formázási tulajdonságokat
ParagraphStyle defaultStyle = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
```
## 4. lépés: Vázlatelemek létrehozása felsorolásjelekkel
```csharp
// Inicializálja az OutlineElement osztályobjektumokat és alkalmazza a felsorolásjeleket
OutlineElement outlineElem1 = new OutlineElement(doc) { NumberList = new NumberList("*", "Arial", 10) };
RichText text1 = new RichText(doc) { Text = "First", ParagraphStyle = defaultStyle };
outlineElem1.AppendChildLast(text1);
// Ismételje meg a többi vázlatelemhez
```
## 5. lépés: Adjon hozzá vázlatelemeket a vázlathoz
```csharp
// Vázlatelemek hozzáadása
outline.AppendChildLast(outlineElem1);
// Ismételje meg a többi vázlatelemhez
```
## 6. lépés: Vázlat hozzáadása az oldalhoz
```csharp
// Vázlat csomópont hozzáadása
page.AppendChildLast(outline);
```
## 7. lépés: Oldal hozzáadása a dokumentumhoz
```csharp
//Oldalcsomópont hozzáadása
doc.AppendChildLast(page);
```
## 8. lépés: Mentse el a OneNote-dokumentumot
```csharp
// Mentse a OneNote-dokumentumot
dataDir = dataDir + "ApplyBulletsOnText_out.one"; 
doc.Save(dataDir);
Console.WriteLine("\nBullets applied successfully on a text.\nFile saved at " + dataDir); 
```
## Következtetés
Gratulálunk! Sikeresen megtanulta, hogyan lehet felsorolásjeleket alkalmazni a szövegre az Aspose.Note for .NET segítségével. Ez a funkció jelentősen javíthatja a OneNote-dokumentumok formázását, és látványosabbá teheti őket.
## GYIK
### Alkalmazhatok különböző felsorolás-stílusokat a lista minden elemére?
 Igen, testreszabhatja a felsorolásjel-stílusokat a`NumberList` tulajdonságok mindegyikhez`OutlineElement`.
### Az Aspose.Note kompatibilis a Microsoft OneNote legújabb verziójával?
Az Aspose.Note támogatja a Microsoft OneNote különféle verzióit, így biztosítja a kompatibilitást a régebbi és az újabb verziókkal egyaránt.
### Használhatom az Aspose.Note-ot kereskedelmi célokra?
 Igen, az Aspose.Note for .NET használható kereskedelmi projektekben. Engedély megszerzéséhez látogassa meg[itt](https://purchase.aspose.com/buy).
### Elérhető az Aspose.Note .NET-hez próbaverziója?
 Igen, letölthet egy ingyenes próbaverziót[itt](https://releases.aspose.com/).
### Hol találhatok további támogatást és forrásokat?
 Látogassa meg az Aspose.Note közösségi fórumot[itt](https://forum.aspose.com/c/note/28) támogatásért és megbeszélésekért.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
