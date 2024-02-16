---
title: Ändra tabellstil i OneNote - Aspose.Note
linktitle: Ändra tabellstil i OneNote - Aspose.Note
second_title: Aspose.Note Java API
description: Förbättra dina OneNote-tabeller utan ansträngning med Aspose.Note för Java. Följ vår steg-för-steg-guide för att ändra bordsstil. Ladda ner biblioteket nu!
type: docs
weight: 10
url: /sv/java/onenote-table-manipulation/change-table-style/
---
## Introduktion
Aspose.Note för Java är ett kraftfullt bibliotek som låter utvecklare manipulera OneNote-filer utan ansträngning. I den här handledningen kommer vi att fokusera på att ändra tabellstilen i ett OneNote-dokument med Aspose.Note för Java. Följ steg-för-steg-guiden för att förbättra dina bords visuella tilltalande.
## Förutsättningar
Innan du börjar, se till att du har följande på plats:
- Java-utvecklingsmiljö: Se till att du har en Java-utvecklingsmiljö inställd på din maskin.
-  Aspose.Note for Java Library: Ladda ner och installera Aspose.Note for Java-biblioteket från[nedladdningssida](https://releases.aspose.com/note/java/).
- Dokumentkatalog: Förbered en katalog för att lagra dina OneNote-dokument.
## Importera paket
ditt Java-projekt, importera de nödvändiga paketen för att arbeta med Aspose.Note:
```java
import com.aspose.note.*;
import java.awt.Color;
import java.io.IOException;
import java.nio.file.Paths;
import java.util.List;
```
## Steg 1: Konfigurera dokumentet
Ladda OneNote-dokumentet i Aspose.Note och hämta listan över tabellnoder
```java
// Ställ in dokumentet och få listan över tabellnoder
String dataDir = "Your Document Directory";
Document document = new Document(dataDir + "ChangeTableStyleIn.one");
List<Table> nodes = document.getChildNodes(Table.class);
```
## Steg 2: Ställ in radstilar
Iterera genom varje tabell och ställ in stilen för varje rad, inklusive att markera den första raden efter rubriken.

```java
// Ställ in radstilar för varje tabell i dokumentet
for (Table table : nodes) {
    setRowStyle(table.getFirstChild(), Color.GRAY, true, true);
    // Markera första raden efter huvudet.
    boolean flag = false;
    List<TableRow> rows = table.getChildren();
    for (int i = 1; i < rows.size(); ++i) {
        setRowStyle(rows.get(i), flag ? Color.lightGray : new java.awt.Color(-1, true), false, false);
        flag = !flag;
    }
}
```
## setRowStyle-metod
```java
    private static void setRowStyle(TableRow row, Color highlightColor, boolean bold, boolean italic) {
        for (TableCell cell: row)
        {
            cell.setBackgroundColor(highlightColor);
            for (RichText node: cell.getChildNodes(RichText.class))
            {
                node.getParagraphStyle().setBold(bold);
                node.getParagraphStyle().setItalic(italic);
                for (TextRun run: node.getTextRuns())
                {
                    run.getStyle().setBold(bold);
                    run.getStyle().setItalic(italic);
                }
            }
        }
    }
```
## Steg 3: Spara dokumentet
Spara det ändrade dokumentet med de nya tabellstilarna.
Genom att följa dessa steg kan du enkelt ändra tabellstilen i ett OneNote-dokument med Aspose.Note för Java.

```java
// Spara det ändrade dokumentet
document.save(Paths.get(dataDir, "ChangeTableStyleOut.one").toString());
```
## Slutsats
Aspose.Note för Java förenklar processen att manipulera OneNote-filer. Genom att utnyttja bibliotekets möjligheter kan du förbättra den visuella presentationen av dina bord utan ansträngning.

## Vanliga frågor
### Var kan jag hitta dokumentationen för Aspose.Note för Java?
 Besök[dokumentation](https://reference.aspose.com/note/java/) för omfattande vägledning.
### Hur kan jag få en tillfällig licens för Aspose.Note för Java?
 Följ detta[länk](https://purchase.aspose.com/temporary-license/) att förvärva en tillfällig licens.
### Finns det en gratis testversion tillgänglig för Aspose.Note för Java?
 Ja, du kan ladda ner en gratis testversion från[här](https://releases.aspose.com/).
### Var kan jag få support för Aspose.Note för Java?
 Gå med i[Aspose.Note forum](https://forum.aspose.com/c/note/28) att söka hjälp från samhället.
### Hur köper jag Aspose.Note för Java?
 Du kan köpa biblioteket[här](https://purchase.aspose.com/buy).