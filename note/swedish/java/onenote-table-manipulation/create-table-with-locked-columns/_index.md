---
date: 2026-01-23
description: Lär dig hur du låser kolumnbredden när du lägger till en tabell i OneNote
  med Aspose.Note för Java. Steg‑för‑steg‑guide med kod, tips och vanliga frågor.
linktitle: How to Lock Column in OneNote Table – Aspose.Note
second_title: Aspose.Note Java API
title: Hur man låser en kolumn i OneNote‑tabell – Aspose.Note
url: /sv/java/onenote-table-manipulation/create-table-with-locked-columns/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hur man låser kolumn i OneNote‑tabell – Aspose.Note

## Introduction
OneNote är en mångsidig anteckningsplattform, och Aspose.Note för Java gör det enkelt att **låsa kolumn**‑bredd när du lägger till en tabell i OneNote. I den här handledningen ser du ett komplett, praktiskt exempel som visar hur bredden och anpassar OneNote‑tabellens kanterNote.  
- ** bredd- **What version of Java is supported?** Java 6 och senare.

## What is “how to lock column” in a OneNote table?
Att låsa en kolumn innebär att tilldela en fast bredd till ett `TableColumn`‑objekt och sätta dess `LockedWidth`‑egenskap till `true`. Detta förhindrar oavsiktlig storleksändring av slutanvändare och håller din layout konsekvent.

## Why lock column width in OneNote?
- **Consistent layout** – Dina anteckningar ser likadana ut på alla enheter.  
- **Better readability** – Lång text radbryts inom en förutsägbar kolumnstorlek.  
- **Professional appearance** – Låsta kolumner ger ett polerat, rapportlikt intryck.

## Prerequisites
Innan du börjar, se till att följande är redo:

- [Java Development Kit (JDK)](https://www.oracle.com/java/technologies/javase-downloads.html) installerat på din maskin.  
- [Aspose.Note for Java](https://downloads.aspose.com/note/java)‑biblioteket nedladdat och tillagt i ditt projekts classpath.

## Import Packages
I ditt Java‑projekt importerar du de nödvändiga paketen för att arbeta med Aspose.Note:

```java
import com.aspose.note.*;
import java.io.IOException;
```

## Step 1: Set Up Your Project
Skapa ett nytt Java‑projekt (eller använd ett befintligt) och lägg till Aspose.Note‑JAR‑filerna i byggsökvägen. Se till att projektet kompileras med den JDK du installerade.

## Step 2: Initialize Document and Page Objects
Vi börjar med att skapa ett nytt `Document` och en `Page` där tabellen ska placeras.

```java
// The path to the documents directory.
String dataDir = "Your Document Directory";
// Create an object of the Document class
Document doc = new Document();
// Initialize Page class object
Page page = new Page();
```

## Step 3: Create Table Rows and Cells
Här bygger vi två rader, var och en med en enda cell som innehåller lite exempeltext. Detta demonstrerar hur den låsta kolumnen beter sig med kort och lång text.

```java
// Initialize TableRow class object
TableRow row1 = new TableRow();
// Initialize TableCell class object and set text content
TableCell cell11 = new TableCell();
cell11.appendChildLast(InsertTable.GetOutlineElementWithText("Small text"));
row1.appendChildLast(cell11);
// Initialize TableRow class object
TableRow row2 = new TableRow();
// Initialize TableCell class object and set text content
TableCell cell21 = new TableCell();
cell21.appendChildLast(InsertTable.GetOutlineElementWithText("Long   text    with    several   words and    spaces."));
row2.appendChildLast(cell21);
```

## Step 4: Create and Customize the Table
Nu skapar vi tabellen, **set table column width**, **lock the column**, och **customize OneNote table borders**.

```java
// Initialize Table class object
Table table = new Table();
table.setBordersVisible(true);               // customize onenote table borders
TableColumn col = new TableColumn();
col.setWidth(200);                           // set table column width
col.setLockedWidth(true);                    // onenote table locked width
table.getColumns().addItem(col);
// Add rows
table.appendChildLast(row1);
table.appendChildLast(row2);
```

## Step 5: Add Table to Outline and Page
Vi fäster nu tabellen på ett `OutlineElement` och lägger slutligen till den på sidan – detta är steget **add outline element java**.

```java
Outline outline = new Outline();
OutlineElement outlineElem = new OutlineElement();
// Add table node
outlineElem.appendChildLast(table);
// Add outline element node
outline.appendChildLast(outlineElem);
// Add outline node
page.appendChildLast(outline);
// Add page node
doc.appendChildLast(page);
```

## Step 6: Save the Document
Spara OneNote‑filen (`.one`) till den katalog du angav tidigare.

```java
dataDir = dataDir + "CreateTableWithLockedColumns_out.one";
doc.save(dataDir);
```

Congratulations! You have successfully **add table to OneNote** with a locked column, fixed width, and customized borders using Aspose.Note for Java.

## Common Issues and Solutions
| Issue | Solution |
|-------|----------|
| Table appears with no borders | Ensure `table.setBordersVisible(true);` is called. |
| Column width changes after adding rows | Verify `col.setLockedWidth(true);` is set **before** rows are appended. |
| File not saved | Check that `dataDir` points to a writable folder and ends with a valid filename. |

## Frequently Asked Questions

**Q: Is Aspose.Note for Java compatible with all Java versions?**  
A: Yes, it works with Java 6 and later, including Java 11 and Java 17.

**Q: Can I customize the appearance of the table further?**  
A: Absolutely! You can modify border styles, cell padding, background colors, and more through the `Table` and `TableCell` properties.

**Q: Is there a trial version available before purchasing?**  
A: Yes, you can [download a free trial](https://releases.aspose.com/) to explore the capabilities of Aspose.Note for Java.

**Q: Where can I find additional support or community discussions?**  
A: Visit the [Aspose.Note forum](https://forum.aspose.com/c/note/28) for support and community discussions.

**Q: How can I obtain a temporary license for Aspose.Note for Java?**  
A: Visit [this link](https://purchase.aspose.com/temporary-license/) to obtain a temporary license for testing purposes.

---

**Last Updated:** 2026-01-23  
**Tested With:** Aspose.Note for Java 24.11  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}