---
title: Szúrja be a kínai számlistát az Aspose.Note szövegbe
linktitle: Szúrja be a kínai számlistát az Aspose.Note szövegbe
second_title: Aspose.Note .NET API
description: Ismerje meg, hogyan illeszthet be könnyedén kínai számlistákat az Aspose.Note-ba .NET dokumentumokhoz. Növelje dokumentumformázási készségeit ezzel a lépésenkénti útmutatóval.
weight: 20
url: /hu/net/text-manipulation/insert-chinese-number-list/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Szúrja be a kínai számlistát az Aspose.Note szövegbe

## Bevezetés
Bővíteni szeretné Aspose.Note for .NET készségeit azáltal, hogy kínai számlistákat épít be dokumentumaiba? Ha igen, akkor jó helyen jársz! Ebben az oktatóanyagban végigvezetjük a kínai számlisták beszúrásának folyamatán az Aspose.Note for .NET használatával. Ez a hatékony könyvtár lehetővé teszi a OneNote-dokumentumok zökkenőmentes kezelését.
## Előfeltételek
Mielőtt belevágnánk az oktatóanyagba, győződjön meg arról, hogy a következő előfeltételek teljesülnek:
- C# programozási alapismeretek.
-  Aspose.Note for .NET telepítve. Letöltheti[itt](https://releases.aspose.com/note/net/).
## Névterek importálása
A kezdéshez importálja a szükséges névtereket a projektbe:
```csharp
using System;
using System.Globalization;
using System.IO;
using Aspose.Note;
using System.Drawing;
using System.Collections.Generic;
```
## 1. lépés: Inicializálja a OneNote-dokumentumot
```csharp
string dataDir = "Your Document Directory";
Aspose.Note.Document doc = new Aspose.Note.Document();
```
## 2. lépés: Inicializálja a OneNote oldalt
```csharp
Aspose.Note.Page page = new Aspose.Note.Page(doc);
Outline outline = new Outline(doc);
```
## 3. lépés: Alkalmazza a szövegstílus-beállításokat
```csharp
ParagraphStyle defaultStyle = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
```
## 4. lépés: Vázlatelemek létrehozása
Most hozzunk létre három vázlatelemet kínai számlistákkal:
### 4.1. lépés: Első elem
```csharp
OutlineElement outlineElem1 = new OutlineElement(doc) { NumberList = new NumberList("{0})", NumberFormat.ChineseCounting, "Arial", 10) };
RichText text1 = new RichText(doc) { Text = "First", ParagraphStyle = defaultStyle };
outlineElem1.AppendChildLast(text1);
```
### 4.2. lépés: Második elem
```csharp
OutlineElement outlineElem2 = new OutlineElement(doc) { NumberList = new NumberList("{0})", NumberFormat.ChineseCounting, "Arial", 10) };
RichText text2 = new RichText(doc) { Text = "Second", ParagraphStyle = defaultStyle };
outlineElem2.AppendChildLast(text2);
```
### 4.3. lépés: Harmadik elem
```csharp
OutlineElement outlineElem3 = new OutlineElement(doc) { NumberList = new NumberList("{0})", NumberFormat.ChineseCounting, "Arial", 10) };
RichText text3 = new RichText(doc) { Text = "Third", ParagraphStyle = defaultStyle };
outlineElem3.AppendChildLast(text3);
```
## 5. lépés: fűzze hozzá az elemeket az Outline-hoz
```csharp
outline.AppendChildLast(outlineElem1);
outline.AppendChildLast(outlineElem2);
outline.AppendChildLast(outlineElem3);
```
## 6. lépés: Vázlat hozzáfűzése az oldalhoz
```csharp
page.AppendChildLast(outline);
```
## 7. lépés: Oldal hozzáfűzése a dokumentumhoz
```csharp
doc.AppendChildLast(page);
```
## 8. lépés: Mentse el a OneNote-dokumentumot
```csharp
dataDir = dataDir + "InsertChineseNumberList_out.one"; 
doc.Save(dataDir);
Console.WriteLine("\nChinese number list inserted successfully.\nFile saved at " + dataDir);
```
Gratulálunk! Sikeresen beszúrta a kínai számlistákat az Aspose.Note dokumentumba a .NET könyvtár használatával.
## Következtetés
Ebben az oktatóanyagban lépésről lépésre bemutattuk a kínai számlisták Aspose.Note for .NET dokumentumokba való beépítésének folyamatát. Fejlessze dokumentumformázási készségeit, és tegye vonzóbbá tartalmát ezekkel a technikákkal.
## GYIK
### K: Testreszabhatom a kínai számlisták formázását?
 V: Igen, testreszabhatja a formázást a paraméterek beállításával a`NumberList` konstruktőr.
### K: Az Aspose.Note kompatibilis a .NET legújabb verziójával?
V: Igen, az Aspose.Note rendszeresen frissül, hogy támogassa a .NET legújabb verzióit.
### K: Hol találhatok további példákat és dokumentációt?
V: Fedezze fel az átfogó[Aspose.Note dokumentáció](https://reference.aspose.com/note/net/).
### K: Hogyan szerezhetek ideiglenes licencet az Aspose.Note számára?
 V: Szerezzen ideiglenes engedélyt[itt](https://purchase.aspose.com/temporary-license/).
### K: Hol kérhetek segítséget vagy vitathatom meg az Aspose.Note-tal kapcsolatos kérdéseket?
 V: Látogassa meg a[Aspose.Note támogatási fórum](https://forum.aspose.com/c/note/28) közösségi támogatásért.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
