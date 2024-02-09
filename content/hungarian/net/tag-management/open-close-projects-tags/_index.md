---
title: Projektek megnyitása és bezárása címkékkel az Aspose.Note-ban
linktitle: Projektek megnyitása és bezárása címkékkel az Aspose.Note-ban
second_title: Aspose.Note .NET API
description: Ismerje meg, hogyan kezelheti programozottan a Microsoft OneNote fájlokat az Aspose.Note for .NET használatával. Hatékonyan nyithat meg és zárhat be projekteket címkékkel.
type: docs
weight: 15
url: /hu/net/tag-management/open-close-projects-tags/
---
## Bevezetés

Ebben az oktatóanyagban megtudjuk, hogyan használhatja az Aspose.Note for .NET-et projektek címkékkel való megnyitásához és bezárásához. Az Aspose.Note egy hatékony API, amely lehetővé teszi a fejlesztők számára, hogy programozottan dolgozzanak Microsoft OneNote fájlokkal, lehetővé téve olyan feladatok elvégzését, mint például a szövegek, képek és címkék manipulálása a dokumentumokon belül.

## Előfeltételek

Mielőtt elkezdené, győződjön meg arról, hogy beállította a következő előfeltételeket:

## Névterek importálása

```csharp
using System.IO;
using System.Linq;
```

Most bontsuk le az egyes példákat több lépésre:

## 1. lépés: Töltse be a dokumentumot

Először is be kell töltenünk a dokumentumot az Aspose.Note-ba.

```csharp
string dataDir = "Your Document Directory";
var oneFile = new Document(Path.Combine(dataDir, "ProjectNotes.one"));
```

## 2. lépés: Zárja be a C projekt elemeit

Most zárjunk be minden, a „C projekthez” kapcsolódó jelölőnégyzetet.

```csharp
foreach (var node in oneFile.GetChildNodes<ITaggable>())
{
    foreach (var checkBox in node.Tags.OfType<CheckBox>())
    {
        if (checkBox.Label.Contains("Project C") && !checkBox.Checked)
        {
            checkBox.SetCompleted();
        }
    }
}
```

## 3. lépés: Mentse el a lezárt projekt C jegyzeteit

Mentse el a módosított dokumentumot lezárt „C projekt” elemekkel.

```csharp
oneFile.Save("Path to save the closed Project C notes");
```

## 4. lépés: Nyissa meg a C projekt elemeit

Ezután nyissuk meg a „C projekthez” kapcsolódó összes jelölőnégyzetet.

```csharp
var oneFile = new Document("Path to the closed Project C notes");

foreach (var node in oneFile.GetChildNodes<ITaggable>())
{
    foreach (var checkBox in node.Tags.OfType<CheckBox>())
    {
        if (checkBox.Label.Contains("Project C") && checkBox.Checked)
        {
            checkBox.SetOpen();
        }
    }
}
```

## 5. lépés: Mentse el az Open Project C Notes fájlt

Mentse el a módosított dokumentumot a megnyitott „C projekt” elemekkel.

```csharp
oneFile.Save(Path.Combine(dataDir, "ProjectNoteWithOpenProjectC.one"));
```

Most már megtanulta, hogyan nyithat meg és zárhat be projekteket címkékkel az Aspose.Note-ban .NET használatával.

## Következtetés

Az Aspose.Note for .NET kényelmes módot kínál a OneNote-dokumentumok programozott kezelésére. Az oktatóanyag követésével hatékonyan kezelheti projektjeit az elemek címkék használatával történő megnyitásával és bezárásával.

## GYIK

### 1. kérdés: Az Aspose.Note kompatibilis a OneNote összes verziójával?

1. válasz: Az Aspose.Note támogatja a Microsoft OneNote 2010 és újabb verzióit.

### 2. kérdés: Használhatom az Aspose.Note-ot kereskedelmi projektekhez?

 2. válasz: Igen, használhatja az Aspose.Note-ot személyes és kereskedelmi projektekhez is. Látogatás[itt](https://purchase.aspose.com/buy) licencet vásárolni.

### 3. kérdés: Az Aspose.Note ingyenes próbaverziót kínál?

V3: Igen, ingyenes próbaverziót kaphat[itt](https://releases.aspose.com/).

### 4. kérdés: Hol találom az Aspose.Note dokumentációját?

 V4: Megtalálható a dokumentáció[itt](https://reference.aspose.com/note/net/).

### 5. kérdés: Hol kaphatok támogatást az Aspose.Note-hoz?

5. válasz: Támogatásért keresse fel az Aspose.Note oldalt[fórum](https://forum.aspose.com/c/note/28).