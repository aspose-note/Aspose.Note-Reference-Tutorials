---
title: Fedezze fel az Aspose.Note dokumentumok oldalváltozatait
linktitle: Fedezze fel az Aspose.Note dokumentumok oldalváltozatait
second_title: Aspose.Note .NET API
description: Ismerje meg, hogyan fedezheti fel az Aspose.Note dokumentumok oldalváltozatait a .NET-keretrendszer használatával, lépésről lépésre.
type: docs
weight: 14
url: /hu/net/note-manipulation/page-revisions-exploration/
---
## Bevezetés

Ebben az oktatóanyagban az Aspose.Note dokumentumok oldalváltozatainak feltárásával foglalkozunk a .NET keretrendszer használatával. Az Aspose.Note egy hatékony könyvtár, amely lehetővé teszi a fejlesztők számára, hogy programozottan dolgozzanak a Microsoft OneNote fájlokkal, és különféle funkciókat kínál az adatok manipulálására és kinyerésére ezekből a fájlokból.

## Előfeltételek

Mielőtt elkezdené, győződjön meg arról, hogy beállította a következő előfeltételeket:

### 1. Töltse le és telepítse az Aspose.Note for .NET programot

 Meglátogatni a[letöltési oldal](https://releases.aspose.com/note/net/) és töltse le az Aspose.Note for .NET könyvtárat. Kövesse a kapott telepítési utasításokat a könyvtár beállításához a fejlesztői környezetben.

### 2. Töltse be a szükséges névtereket

Ügyeljen arra, hogy importálja a szükséges névtereket a .NET-projektbe az Aspose.Note funkciók zökkenőmentes eléréséhez.

```csharp
using System.IO;
using Aspose.Note;
using System;
using System.Collections.Generic;
```

Most pedig bontsuk le az oldalváltozatok feltárásának folyamatát lépésről lépésre:

## 1. lépés: Töltse be a dokumentumot

Először is be kell töltenünk az Aspose.Note dokumentumot, biztosítva a dokumentumelőzmények betöltését.

```csharp
string dataDir = "Your Document Directory";
Document document = new Document(dataDir + "Aspose.one", new LoadOptions { LoadHistory = true });
```

## 2. lépés: Töltse le az oldalváltozatokat

A dokumentum betöltése után le tudjuk kérni egy adott oldal revízióit. Ebben a példában az első oldal átdolgozásait kapjuk meg.

```csharp
Page firstPage = document.FirstChild;
foreach (Page pageRevision in document.GetPageHistory(firstPage))
{
    /*Use pageRevision like a regular page.*/
    Console.WriteLine("LastModifiedTime: {0}", pageRevision.LastModifiedTime);
    Console.WriteLine("CreationTime: {0}", pageRevision.CreationTime);
    Console.WriteLine("Title: {0}", pageRevision.Title);
    Console.WriteLine("Level: {0}", pageRevision.Level);
    Console.WriteLine("Author: {0}", pageRevision.Author);
    Console.WriteLine();
}
```

## 3. lépés: Iterálás átdolgozáson keresztül

A cikluson belül ismételje meg az oldal minden változatát, és érje el annak tulajdonságait, például az utolsó módosítás idejét, a létrehozási időt, a címet, a szintet és a szerzőt.

## Következtetés

Az Aspose.Note dokumentumok oldalváltozatainak feltárása .NET használatával egyszerű folyamat. Az oktatóanyagban ismertetett lépések követésével hatékonyan lekérheti és programozottan elemezheti a OneNote-fájlok felülvizsgálati előzményeit.

## GYIK

### 1. kérdés: Használhatom az Aspose.Note for .NET programot új OneNote-dokumentumok létrehozására?

1. válasz: Igen, az Aspose.Note for .NET lehetővé teszi a OneNote-dokumentumok programozott létrehozását, szerkesztését és kezelését.

### 2. kérdés: Az Aspose.Note támogatja a betöltési előzményeket minden típusú OneNote-fájlhoz?

2. válasz: Az Aspose.Note támogatja a .one és .onepkg fájlformátumok betöltési előzményeit.

### 3. kérdés: Elérhető ingyenes próbaverzió az Aspose.Note for .NET számára?

 3. válasz: Igen, letöltheti az Aspose.Note .NET-hez ingyenes próbaverzióját a webhelyről[itt](https://releases.aspose.com/).

### 4. kérdés: Hogyan szerezhetek ideiglenes licencet az Aspose.Note for .NET számára?

 V4: Ideiglenes licencet kérhetsz a címtől[ez a link](https://purchase.aspose.com/temporary-license/).

### 5. kérdés: Hol találok támogatást az Aspose.Note for .NET számára?

 5. válasz: Támogatást és forrásokat találhat a[Aspose.Note fórum](https://forum.aspose.com/c/note/28).