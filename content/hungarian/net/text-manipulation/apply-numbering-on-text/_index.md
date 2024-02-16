---
title: Számozás alkalmazása a szövegen az Aspose.Note-ban
linktitle: Számozás alkalmazása a szövegen az Aspose.Note-ban
second_title: Aspose.Note .NET API
description: Ezzel az átfogó oktatóanyaggal megtudhatja, hogyan alkalmazhat szövegszámozást az Aspose.Note for .NET-ben. Fokozza a dokumentum formázását erőfeszítés nélkül.
type: docs
weight: 12
url: /hu/net/text-manipulation/apply-numbering-on-text/
---
## Bevezetés
Az Aspose.Note for .NET hatékony eszközöket biztosít a C# alkalmazások dokumentumkezeléséhez. Ebben az oktatóanyagban az Aspose.Note segítségével a számozás alkalmazásának folyamatát vizsgáljuk meg. Kövesse ezeket a lépésenkénti utasításokat, hogy könnyedén javítsa dokumentumformázását.
## Előfeltételek
Mielőtt belevágna az oktatóanyagba, győződjön meg arról, hogy a következő előfeltételek teljesülnek:
- A C# programozási nyelv alapvető ismerete.
-  Aspose.Note for .NET telepítve. Letöltheti[itt](https://releases.aspose.com/note/net/).
- Integrált fejlesztői környezet (IDE), például a Visual Studio.
## Névterek importálása
A kezdéshez feltétlenül importálja a szükséges névtereket a C# projektbe:
```csharp
using System;
using System.Globalization;
using System.IO;
using Aspose.Note;
using System.Drawing;
using System.Collections.Generic;
```
## 1. lépés: Állítsa be a dokumentumot
Kezdje egy új dokumentum létrehozásával és a szükséges objektumok inicializálásával:
```csharp
// A dokumentumok könyvtárának elérési útja.
string dataDir = "Your Document Directory";
//Hozzon létre egy objektumot a Dokumentum osztályból
Document doc = new Document();
// Oldal osztály objektum inicializálása
Aspose.Note.Page page = new Aspose.Note.Page(doc);
// Inicializálja az Outline osztály objektumot
Outline outline = new Outline(doc);
```
## 2. lépés: Határozza meg az alapértelmezett stílust
Állítsa be a szöveg alapértelmezett stílusát a ChapterStyle osztály segítségével:
```csharp
ParagraphStyle defaultStyle = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
```
## 3. lépés: Alkalmazza a számozást
Inicializálja az OutlineElement osztályobjektumokat, és alkalmazza az egyes elemek számozását:
```csharp
OutlineElement outlineElem1 = new OutlineElement(doc) { NumberList = new NumberList("{0})", NumberFormat.DecimalNumbers, "Arial", 10) };
RichText text1 = new RichText(doc) { Text = "First", ParagraphStyle = defaultStyle };
outlineElem1.AppendChildLast(text1);
OutlineElement outlineElem2 = new OutlineElement(doc) { NumberList = new NumberList("{0})", NumberFormat.DecimalNumbers, "Arial", 10) };
RichText text2 = new RichText(doc) { Text = "Second", ParagraphStyle = defaultStyle };
outlineElem2.AppendChildLast(text2);
OutlineElement outlineElem3 = new OutlineElement(doc) { NumberList = new NumberList("{0})", NumberFormat.DecimalNumbers, "Arial", 10) };
RichText text3 = new RichText(doc) { Text = "Third", ParagraphStyle = defaultStyle };
outlineElem3.AppendChildLast(text3);
```
## 4. lépés: Vázlatelemek hozzáadása
A vázlatelemek hozzáfűzése a vázlathoz:
```csharp
outline.AppendChildLast(outlineElem1);
outline.AppendChildLast(outlineElem2);
outline.AppendChildLast(outlineElem3);
```
## 5. lépés: Mentse el a dokumentumot
Mentse el a OneNote-dokumentumot az alkalmazott számozással:
```csharp
dataDir = dataDir + "ApplyNumberingOnText_out.one"; 
doc.Save(dataDir);
Console.WriteLine("\nNumbering applied successfully on a text.\nFile saved at " + dataDir); 
```
## Következtetés
Gratulálunk! Sikeresen megtanulta, hogyan kell számozást alkalmazni szövegeken az Aspose.Note for .NET-ben. Kísérletezzen a különböző formázási lehetőségekkel, hogy tetszetős dokumentumokat készítsen könnyedén.
## GYIK
### 1. Testreszabhatom a számozási formátumot?
Igen, a NumberList osztály lehetővé teszi a számozási formátum testreszabását az Ön preferenciái szerint.
### 2. Vannak más formázási lehetőségek is?
Az Aspose.Note a formázási lehetőségek széles skáláját kínálja, beleértve a betűtípus stílusát, színét és egyebeket.
### 3. Az Aspose.Note kompatibilis a Visual Studio programmal?
Teljesen! Az Aspose.Note zökkenőmentesen integrálható a Visual Studióval a zökkenőmentes fejlesztés érdekében.
### 4. Kipróbálhatom az Aspose.Note-t vásárlás előtt?
 Biztosan! Megtekintheti az ingyenes próbaverziót[itt](https://releases.aspose.com/).
### 5. Hol kaphatok támogatást az Aspose.Note-hoz?
 Bármilyen segítségre vagy kérdésre keresse fel a[Aspose.Note fórum](https://forum.aspose.com/c/note/28).