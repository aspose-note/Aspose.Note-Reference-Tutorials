---
title: Hozzon létre táblázatokat az Aspose segítségével.Megjegyzés
linktitle: Hozzon létre táblázatokat az Aspose segítségével.Megjegyzés
second_title: Aspose.Note .NET API
description: Ismerje meg, hogyan állíthat össze strukturált táblázatokat formázott szöveggel az Aspose.Note for .NET segítségével. Fokozatmentesen javítja a dokumentumok rendszerezését és olvashatóságát.
type: docs
weight: 11
url: /hu/net/table-manipulation/compose-tables/
---
## Bevezetés

A táblázatok a dokumentumok alapvető összetevői, amelyek lehetővé teszik az információk strukturált megjelenítését. Az Aspose.Note for .NET robusztus eszközöket kínál a táblázatok könnyű összeállításához. Ebben az oktatóanyagban végigvezetjük az Aspose.Note használatával formázott szöveget tartalmazó táblázatok létrehozásának folyamatán.

## Előfeltételek

Mielőtt belevágna a táblázatok összeállításába az Aspose.Note for .NET segítségével, győződjön meg arról, hogy rendelkezik a következő előfeltételekkel:

1. Környezet beállítása: Győződjön meg arról, hogy megfelelő fejlesztői környezet van beállítva .NET-keretrendszerrel vagy .NET Core-al.
2.  Telepítés: Töltse le és telepítse az Aspose.Note for .NET programot a[weboldal](https://releases.aspose.com/note/net/).
3. Alapvető ismeretek: Ismerkedjen meg a C# programozás és a dokumentumkezelés alapfogalmaival.

## Névterek importálása

Mielőtt elkezdené a táblázatok összeállítását, importálja a szükséges névtereket:

```csharp
using System;
using System.Drawing;
using System.IO;
using System.Linq;
```

Bontsuk fel a példát kezelhető lépésekre:

## 1. lépés: Állítsa be a dokumentumkönyvtárat

A táblázat összeállítása előtt határozza meg a könyvtárat, ahová a dokumentumot menteni szeretné.

```csharp
string dataDir = "Your Document Directory";
```

## 2. lépés: Hozzon létre fejlécszöveget

Határozza meg a fejléc szövegét meghatározott stílusokkal, például betűmérettel és félkövérséggel.

```csharp
var headerText = new RichText() { ParagraphStyle = new ParagraphStyle() { FontSize = 18, IsBold = true }, Alignment = HorizontalAlignment.Center }
					.Append("Super contest for suppliers.");
```

## 3. lépés: Oldal és vázlat létrehozása

A tartalom strukturálásához inicializáljon egy oldalt és egy vázlatot.

```csharp
var page = new Page();
var outline = page.AppendChildLast(new Outline() { HorizontalOffset = 50 });
outline.AppendChildLast(new OutlineElement()).AppendChildLast(headerText);
```

## 4. lépés: Összefoglaló szöveg hozzáadása

A táblázat elé foglaljon összefoglaló szöveget.

```csharp
var bodyTextHeader = outline.AppendChildLast(new OutlineElement()).AppendChildLast(new RichText() { ParagraphStyle = ParagraphStyle.Default });
bodyTextHeader.Append("This is the final ranking of proposals got from our suppliers.");
```

## 5. lépés: Hozzon létre táblázatot

Táblázat inicializálása az adatok sorokba és oszlopokba rendezéséhez.

```csharp
var ranking = outline.AppendChildLast(new OutlineElement()).AppendChildLast(new Table());
```

## 6. lépés: Adja hozzá a fejlécsort

Töltse fel a táblázatot egy oszlopcímeket tartalmazó fejlécsorral.

```csharp
var headerRow = ranking.AppendChildFirst(new TableRow());
foreach (var header in new[] { "Supplier", "Contacts", "Score A", "Score B", "Score C", "Final score", "Attached materials", "Comments" })
{
   ranking.Columns.Add(new TableColumn());
   headerRow.AppendChildLast(new TableCell() { BackgroundColor = backGroundColor })
			 .AppendChildLast(new OutlineElement())
			 .AppendChildLast(new RichText() { ParagraphStyle = headerStyle })
			 .Append(header);
}
```

## 7. lépés: Adjon hozzá üres sorokat

Szúrjon be üres sorokat az adatbeszúrás előkészítéséhez.

```csharp
for (int i = 0; i < 5; i++)
{
   backGroundColor = backGroundColor.IsEmpty ? Color.LightGray : Color.Empty;
   var row = ranking.AppendChildLast(new TableRow());
   for (int j = 0; j < ranking.Columns.Count(); j++)
   {
	   row.AppendChildLast(new TableCell() { BackgroundColor = backGroundColor })
		  .AppendChildLast(new OutlineElement())
		  .AppendChildLast(new RichText() { ParagraphStyle = ParagraphStyle.Default });
   }
}
```

## 8. lépés: Adja meg kapcsolatfelvételi adatait

Töltse fel a "Kapcsolatok" oszlopot sablontartalommal.

```csharp
foreach (var row in ranking.Skip(1))
{
   var contactsCell = row.ElementAt(1);
   contactsCell.AppendChildLast(new OutlineElement())
			   .AppendChildLast(new RichText() { ParagraphStyle = ParagraphStyle.Default })
			   .Append("Web: ").Append("link", new TextStyle() { HyperlinkAddress = "www.link.com", IsHyperlink = true });
   contactsCell.AppendChildLast(new OutlineElement())
			   .AppendChildLast(new RichText() { ParagraphStyle = ParagraphStyle.Default })
			   .Append("E-mail: ").Append("mail", new TextStyle() { HyperlinkAddress = "mailto:hi@link.com", IsHyperlink = true });
}
```

## 9. lépés: Mentse el a dokumentumot

Mentse el az összeállított táblázatdokumentumot.

```csharp
var d = new Document();
d.AppendChildLast(page);
d.Save(Path.Combine(dataDir, "ComposeTable_out.one"));
```

## 10. lépés: Megerősítés

Erősítse meg a dokumentum sikeres összeállítását.

```csharp
Console.WriteLine("\nThe document is composed successfully.");
```

## Következtetés

Ebben az oktatóanyagban megvizsgáltuk, hogyan hozhat létre formázott szöveget tartalmazó táblázatokat az Aspose.Note for .NET használatával. Ezeket a lépésről lépésre követve hatékonyan hozhat létre strukturált táblázatokat a dokumentumokon belül, javítva az olvashatóságot és a rendszerezést.

## GYIK

### 1. kérdés: Testreszabhatom az asztalelemek stílusát?
   
V1: Igen, testreszabhatja a különféle szempontokat, például a betűméretet, a színt és az igazítást az igényeinek megfelelően.

### 2. kérdés: Az Aspose.Note kompatibilis más .NET könyvtárakkal?
   
2. válasz: Az Aspose.Note zökkenőmentesen integrálódik más .NET-könyvtárakba, széles körű rugalmasságot kínálva a dokumentumkezelésben.

### 3. kérdés: Az Aspose.Note támogatja a táblázatok különböző formátumokba történő exportálását?
   
3. válasz: Természetesen az Aspose.Note lehetővé teszi a táblázatok exportálását különféle formátumokba, beleértve a PDF, DOCX és HTML formátumokat.

### 4. kérdés: Feltölthetek-e dinamikusan táblákat külső forrásból származó adatokkal?
   
4. válasz: Igen, dinamikusan feltöltheti a táblákat adatbázisokból, API-kból vagy felhasználói bemenetek adatainak lekérésével.

### 5. kérdés: Rendelkezésre áll műszaki támogatás az Aspose.Note felhasználói számára?
   
5. válasz: Igen, az Aspose átfogó technikai támogatást nyújt fórumain és dedikált támogatási csatornáin keresztül.