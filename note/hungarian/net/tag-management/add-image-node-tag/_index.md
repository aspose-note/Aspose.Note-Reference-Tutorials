---
title: Képcsomópont hozzáadása címkével az Aspose.Note-ban
linktitle: Képcsomópont hozzáadása címkével az Aspose.Note-ban
second_title: Aspose.Note .NET API
description: Ismerje meg, hogyan javíthatja OneNote-dokumentumait egyéni címkékkel ellátott képek hozzáadásával az Aspose.Note for .NET segítségével.
weight: 10
url: /hu/net/tag-management/add-image-node-tag/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Képcsomópont hozzáadása címkével az Aspose.Note-ban

## Bevezetés

Ebben az oktatóanyagban megvizsgáljuk, hogyan adhat hozzá képcsomópontot címkével az Aspose.Note for .NET segítségével. Ez a funkció lehetővé teszi a OneNote-dokumentumok fejlesztését egyéni címkékkel ellátott képek hozzáadásával.

## Előfeltételek

Mielőtt elkezdené, győződjön meg arról, hogy rendelkezik az alábbiakkal:

1. Visual Studio: Telepítse a Visual Studio IDE-t a rendszerére.
2.  Aspose.Note for .NET: Töltse le és telepítse az Aspose.Note for .NET könyvtárat a[letöltési link](https://releases.aspose.com/note/net/).
3. Alapvető ismeretek: Ismerkedjen meg a C# programozási nyelvvel és a .NET keretrendszerrel.

## Névterek importálása

Először győződjön meg arról, hogy a szükséges névtereket tartalmazza a C# kódban:

```csharp
using System.Drawing;
using System.IO;
using Aspose.Note;
using System;
using System.Collections.Generic;
```

## 1. lépés: Inicializálja a dokumentum- és oldalobjektumokat

 Kezdje a példány létrehozásával a`Document` osztály és a`Page` tárgy:

```csharp
Document doc = new Document();
Aspose.Note.Page page = new Aspose.Note.Page(doc);
```

## 2. lépés: Inicializálja az Outline és OutlineElement objektumokat

 Ezután inicializálja`Outline` és`OutlineElement` objektumok:

```csharp
Outline outline = new Outline(doc);
OutlineElement outlineElem = new OutlineElement(doc);
```

## 3. lépés: Töltse be és helyezze be a képet

Töltse be a kívánt képet, és helyezze be a dokumentum csomópontjába:

```csharp
Aspose.Note.Image image = new Aspose.Note.Image(doc, "path_to_your_image.jpg");
outlineElem.AppendChildLast(image);
```

## 4. lépés: Adjon hozzá címkét a képhez

Adjon hozzá egyéni címkét a képhez:

```csharp
image.Tags.Add(NoteTag.CreateYellowStar());
```

## 5. lépés: Vázlatelem és oldalcsomópontok hozzáfűzése

A vázlatelem és a vázlatcsomópontok hozzáfűzése az oldalhoz:

```csharp
outline.AppendChildLast(outlineElem);
page.AppendChildLast(outline);
```

## 6. lépés: Mentse el a dokumentumot

Mentse el a módosított OneNote-dokumentumot:

```csharp
doc.AppendChildLast(page);
string outputFilePath = "output_path/AddImageNodeWithTag_out.one";
doc.Save(outputFilePath);
```

## Következtetés

Az alábbi lépések követésével zökkenőmentesen hozzáadhat egy képcsomópontot egyéni címkével az Aspose.Note for .NET segítségével, így személyre szabott látványelemekkel gazdagítja OneNote-dokumentumait.

## GYIK

### 1. kérdés: Hozzáadhatok több képet különböző címkékkel egyetlen dokumentumhoz az Aspose.Note segítségével?

1. válasz: Igen, több képet is hozzáadhat különböző címkékkel, ha minden egyes képhez hasonló lépéseket követ.

### 2. kérdés: Az Aspose.Note kompatibilis a OneNote összes verziójával?

2. válasz: Az Aspose.Note a OneNote különféle verzióit támogatja, biztosítva a kompatibilitást a különböző környezetekben.

### 3. kérdés: Testreszabhatom a képhez hozzáadott címke megjelenését?

3. válasz: Igen, az Aspose.Note rugalmasságot biztosít a címke megjelenésének az Ön preferenciáinak megfelelő testreszabásában.

### 4. kérdés: Az Aspose.Note támogatja képek URL-ekből való hozzáadását?

4. válasz: Az Aspose.Note elsősorban a helyi könyvtárakból származó képek hozzáadását támogatja, de külső képeket is beépíthet, ha először helyileg tölti le őket.

### 5. kérdés: Vannak-e korlátozások a hozzáadható képek méretére vagy formátumára vonatkozóan?

5. válasz: Az Aspose.Note a képformátumok széles skáláját támogatja, és nem szab szigorú korlátozásokat a képméretre vonatkozóan, lehetővé téve, hogy változatos látványelemeket építsen be dokumentumaiba.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
