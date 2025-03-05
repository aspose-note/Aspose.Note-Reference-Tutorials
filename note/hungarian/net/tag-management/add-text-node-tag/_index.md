---
title: Szövegcsomópont hozzáadása címkével az Aspose.Note-ban
linktitle: Szövegcsomópont hozzáadása címkével az Aspose.Note-ban
second_title: Aspose.Note .NET API
description: Ismerje meg, hogyan adhat hozzá szöveges csomópontokat címkékkel a OneNote-dokumentumokhoz az Aspose.Note for .NET használatával.
type: docs
weight: 12
url: /hu/net/tag-management/add-text-node-tag/
---
## Bevezetés

Az Aspose.Note for .NET egy hatékony könyvtár, amely lehetővé teszi a fejlesztők számára Microsoft OneNote-fájlok létrehozását, kezelését és konvertálását programozottan a .NET-keretrendszer használatával. Ebben az oktatóanyagban megvizsgáljuk, hogyan adhatunk hozzá címkével ellátott szöveges csomópontot egy OneNote-dokumentumhoz az Aspose.Note for .NET használatával.

## Előfeltételek

Mielőtt elkezdené, győződjön meg arról, hogy rendelkezik a következő előfeltételekkel:

1. Visual Studio: Győződjön meg arról, hogy a Visual Studio telepítve van a rendszeren.
2.  Aspose.Note for .NET: Töltse le és telepítse az Aspose.Note for .NET programot a[weboldal](https://releases.aspose.com/note/net/).
3. C# alapismeretek: Ismerkedjen meg a C# programozási nyelv alapjaival.

## Névterek importálása

Először is importálnia kell a szükséges névtereket, hogy hozzáférjen az Aspose.Note for .NET használatához szükséges osztályokhoz és metódusokhoz.

```csharp
using System.Drawing;
using System.IO;
using Aspose.Note;
using System;
using System.Collections.Generic;
```

## 1. lépés: Hozzon létre egy dokumentumobjektumot

A OneNote-dokumentumokkal való munka megkezdéséhez inicializáljon egy dokumentumobjektumot.

```csharp
// A dokumentumok könyvtárának elérési útja.
string dataDir = "Your Document Directory";
Document doc = new Document();
```

## 2. lépés: Inicializálja az oldal- és vázlatobjektumokat

Hozzon létre Page és Outline objektumokat a OneNote-dokumentum tartalmának strukturálásához.

```csharp
Aspose.Note.Page page = new Aspose.Note.Page(doc);
Outline outline = new Outline(doc);
```

## 3. lépés: Adjon hozzá szövegcsomópontot címkével

Hozzon létre egy RichText objektumot a kívánt szöveggel és stílussal, majd adja hozzá az OutlineElementhez.

```csharp
OutlineElement outlineElem = new OutlineElement(doc);
ParagraphStyle textStyle = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
RichText text = new RichText(doc) { Text = "OneNote text.", ParagraphStyle = textStyle };
text.Tags.Add(NoteTag.CreateYellowStar());
outlineElem.AppendChildLast(text);
```

## 4. lépés: Vázlatelem és oldalcsomópontok hozzáfűzése

Illessze az OutlineElement elemet a vázlathoz, majd a Vázlatot az oldalhoz. Végül csatolja az oldalt a dokumentumhoz.

```csharp
outline.AppendChildLast(outlineElem);
page.AppendChildLast(outline);
doc.AppendChildLast(page);
```

## 5. lépés: Mentse el a dokumentumot

Mentse a módosított OneNote-dokumentumot egy megadott helyre.

```csharp
string dataDir = "Your Document Directory";
string outputPath = Path.Combine(dataDir, "AddTextNodeWithTag_out.one");
doc.Save(outputPath);
```

## Következtetés

Gratulálunk! Sikeresen megtanulta, hogyan adhat hozzá szöveges csomópontot címkével egy OneNote-dokumentumhoz az Aspose.Note for .NET használatával. Ezen ismeretek birtokában most már programozottan testreszabhatja és javíthatja OneNote-fájljait.

## GYIK

### 1. kérdés: Hozzáadhatok több szöveges csomópontot különböző címkékkel ugyanabban a dokumentumban?

1. válasz: Igen, több szövegcsomópontot is hozzáadhat különböző címkékkel, ha minden csomóponthoz ugyanazt a folyamatot követi.

### 2. kérdés: Az Aspose.Note for .NET kompatibilis a OneNote összes verziójával?

2. válasz: Az Aspose.Note for .NET a OneNote különféle verzióit támogatja, beleértve a 2010-es, 2013-as, 2016-os és újabb verziókat.

### 3. kérdés: Testreszabhatom a címke színeit és stílusait?

A3: Igen, testreszabhatja a címke színeit és stílusait az Ön igényei szerint.

### 4. kérdés: Az Aspose.Note for .NET támogatja a dokumentumtitkosítást?

4. válasz: Igen, az Aspose.Note for .NET támogatja a dokumentumtitkosítást az adatbiztonság biztosítása érdekében.

### 5. kérdés: Hol találok további forrásokat és támogatást az Aspose.Note for .NET-hez?

 A5: Felfedezheti a[Aspose.Note a .NET dokumentációhoz](https://reference.aspose.com/note/net/)és kérjen segítséget a[Aspose.Note fórum](https://forum.aspose.com/c/note/28).