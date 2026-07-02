---
date: 2025-12-18
description: Lär dig hur du exporterar OneNote‑sidor till PDF med Aspose.Note för
  Java. Välj uppdelningsalgoritmer, ställ in sidindelning och generera PDF‑filer enkelt.
linktitle: Export OneNote Pages with Splitting Algorithm Method – Aspose.Note
second_title: Aspose.Note Java API
title: Exportera OneNote-sidor med delningsalgoritmmetod – Aspose.Note
url: /sv/java/onenote-document-saving/use-splitting-algorithm-method/
weight: 26
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Exportera OneNote-sidor med delningsalgoritm-metoden – Aspose.Note

## Introduktion

Om du behöver **exportera OneNote-sidor** till ett PDF-dokument programmatiskt, gör Aspose.Note för Java det enkelt. I den här handledningen går vi igenom delningsalgoritmmetoden, som låter dig kontrollera hur innehåll delas upp över sidor, vilket säkerställer en ren och läsbar PDF-utdata. Du får se hur du ställer in PDF-sparalternativ, väljer rätt siddelningsalgoritm och slutligen genererar PDF-filen – allt med bara några rader Java-kod.

## Snabba svar
- **Vad gör delningsalgoritmen?** Den avgör hur objekt som sträcker sig över sidgränser hanteras vid export av OneNote-sidor till PDF.

- **Vilket bibliotek krävs?** Aspose.Note för Java (ladda ner från den officiella Aspose-webbplatsen).

- **Behöver jag en licens?** En tillfällig eller fullständig licens krävs för produktionsanvändning; en gratis provversion finns tillgänglig.

- **Kan jag exportera stora OneNote-anteckningsböcker?** Ja – biblioteket bearbetar effektivt stora filer och låter dig ställa in regler för siddelning.

- **Vilka utdataformat stöds?** PDF, JPEG, PNG, XPS med mera; den här guiden fokuserar på PDF-export.

## Vad är **exportera OneNote-sidor**?
Att exportera OneNote-sidor innebär att konvertera det ursprungliga `.one`-filformatet till ett mer portabelt format som PDF. Detta är användbart för att dela, arkivera eller skriva ut innehåll utan att OneNote-programmet krävs.

## Varför använda delningsalgoritmen för **exportera OneNote-sidor**?
Algoritmen ger dig finkornig kontroll över hur komplexa objekt (tabeller, bilder, ritningar) hanteras vid sidbrytningar. Genom att välja lämplig algoritm kan du:

* Bevara den visuella layouten för varje sida.

* Undvika klippt innehåll som annars skulle beskäras.

* Minska antalet genererade sidor när objekt kan flyttas till nästa sida utan problem.

## Förutsättningar

Innan vi börjar, se till att du har följande förutsättningar:

1. Java Development Kit (JDK): Se till att du har JDK installerat på ditt system. Du kan ladda ner det från [webbplatsen](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).

2. Aspose.Note för Java-biblioteket: Ladda ner och installera Aspose.Note för Java-biblioteket från [nedladdningslänken](https://releases.aspose.com/note/java/).

## Importera paket

Importera de nödvändiga paketen i ditt Java-projekt för att använda Aspose.Note-funktionerna.

```java
import java.io.IOException;
import com.aspose.note.AlwaysSplitObjectsAlgorithm;
import com.aspose.note.Document;
import com.aspose.note.KeepPartAndCloneSolidObjectToNextPageAlgorithm;
import com.aspose.note.KeepSolidObjectsAlgorithm;
import com.aspose.note.PdfSaveOptions;
```

## Steg 1: Definiera dokumentkatalog

Konfigurera katalogen där ditt OneNote-dokument finns.

```java
String dataDir = "Your Document Directory";
```

## Steg 2: Läs in OneNote-dokumentet

Ladda in OneNote-dokumentet med Aspose.Notes klass `Document`.

```java
Document doc = new Document(dataDir + "Sample1.one");
```

## Steg 3: Ställ in PDF-sparalternativ

Skapa en instans av `PdfSaveOptions` för att ange alternativ för att spara dokumentet som PDF. Det är här du **ställer in beteendet för siddelning** och andra PDF-relaterade inställningar.

```java
PdfSaveOptions pdfSaveOptions = new PdfSaveOptions();
```

## Steg 4: Ställ in algoritmen för siddelning

Välj lämplig delningsalgoritm enligt dina behov. Här använder vi `KeepPartAndCloneSolidObjectToNextPageAlgorithm`, som behåller en del av ett objekt på den aktuella sidan och klonar resten till nästa sida.

```java
pdfSaveOptions.setPageSplittingAlgorithm(new KeepPartAndCloneSolidObjectToNextPageAlgorithm(100));
```

## Steg 5: Spara dokumentet

Spara dokumentet med de angivna PDF-sparalternativen. Detta steg **genererar PDF onenote**-utdata som du kan öppna, dela eller skriva ut.

```java
try {
    doc.save(dataDir + "UsingSplittingAlgorithmMethod_out.Jpeg", pdfSaveOptions);
} catch (Exception ex) {
    System.out.println("Exception: " + ex.getMessage());
}
```

## Vanliga problem och lösningar

| Problem | Lösning |
|-------|----------|
| **Objekt är avskurna vid sidgränser** | Prova en annan algoritm, till exempel `AlwaysSplitObjectsAlgorithm`, eller öka tröskelvärdet i `KeepPartAndCloneSolidObjectToNextPageAlgorithm`. |
| **Utdata-PDF:n är tom** | Kontrollera att källfilen `.one` inte är skadad och att sökvägen till `dataDir` är korrekt. |
| **Prestandan är långsam med stora anteckningsböcker** | Använd `pdfSaveOptions.setCompressImages(true)` för att minska minnesanvändningen och överväg att bearbeta anteckningsboken i mindre avsnitt. |

## Vanliga frågor

**F: Kan jag använda Aspose.Note för Java med andra programmeringsspråk?**
S: Ja, Aspose.Note är även tillgängligt för .NET, C++ och Python.

**F: Är Aspose.Note lämpligt för att bearbeta stora OneNote-filer?**
S: Absolut. Biblioteket är optimerat för att hantera stora anteckningsböcker effektivt.

**F: Var kan jag hitta ytterligare resurser och support för Aspose.Note?**
S: Du kan se [dokumentationen](https://reference.aspose.com/note/java/) och [forumet](https://forum.aspose.com/c/note/28) för support och vägledning.

**F: Kan jag prova Aspose.Note innan jag köper?**
S: Ja, du kan använda en [kostnadsfri testversion](https://releases.aspose.com/) för att utforska funktionerna innan du gör ett köp.

**F: Hur kan jag få en tillfällig licens för Aspose.Note?**
S: Du kan begära en [tillfällig licens](https://purchase.aspose.com/temporary-license/) för att utvärdera produkten under en testperiod.

---

**Senast uppdaterad:** 2025-12-18
**Testad med:** Aspose.Note 26.4 för Java
**Författare:** Aspose 

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}