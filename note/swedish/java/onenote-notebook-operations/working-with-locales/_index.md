---
date: 2026-01-05
description: Lär dig hur du ställer in standardlocale, laddar OneNote‑dokument, anger
  Aspose‑licens, konverterar OneNote till PNG och sparar OneNote som bild med Aspose.Note
  för Java.
linktitle: Working with Locales in OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: Ange standardlokal i OneNote – Aspose.Note Java
url: /sv/java/onenote-notebook-operations/working-with-locales/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Ställ in standardlokal i OneNote – Aspose.Note Java

## Introduktion

Om du behöver **ställa in standardlokal** när du bearbetar OneNote‑filer, gör Aspose.Note för Java det enkelt. I den här handledningen går vi igenom allt du behöver – från licensiering av produkten till inläsning av ett OneNote‑dokument, ändring av lokalen och slutligen konvertering av filen till en PNG‑bild. När du är klar kan du anpassa språkinställningarna och generera lokal‑specifika resultat med bara några rader kod.

## Snabba svar
- **Vad gör “set default locale”?** Det definierar språk‑ och region‑formatering som Aspose.Note använder när den läser eller skriver OneNote‑filer.  
- **Behöver jag en licens?** Ja – ställ in Aspose‑licensen för att låsa upp full funktionalitet.  
- **Vilken Java‑version krävs?** Alla JDK 8+ stöds.  
- **Kan jag konvertera OneNote till PNG?** Absolut; API‑et låter dig spara sidor som bilder.  
- **Är processen trådsäker?** Att ställa in standardlokal är globalt, så konfigurera den en gång vid applikationens start.

## Vad är “set default locale” i Aspose.Note?
Att ställa in standardlokal talar om för Aspose.Note vilket språk och vilka kulturella konventioner som ska tillämpas när datum, tal och text parsas. Detta är viktigt för multiregionella applikationer som behöver konsekvent formatering över olika användarlokaler.

## Varför ställa in standardlokal när du arbetar med OneNote?
- **Korrekt datavisning:** Datum och tal visas korrekt för målgruppen.  
- **Enhetliga UI‑strängar:** Text som extraheras från OneNote respekterar språk‑inställningarna.  
- **Förenklad konvertering:** När du senare konverterar en OneNote‑fil till PNG eller andra format matchar den visuella layouten den förväntade lokalen.

## Förutsättningar

- **Java‑utvecklingsmiljö:** JDK installerad och `JAVA_HOME` konfigurerad.  
- **Aspose.Note‑bibliotek:** Ladda ner den senaste JAR‑filen från [download link](https://releases.aspose.com/note/java/).  
- **En giltig Aspose‑licensfil** (gratis provversion fungerar för testning).

## Importera paket

Innan du skriver någon kod, importera de klasser som tillhandahåller den nödvändiga funktionaliteten.

```java
import java.io.IOException;
import java.nio.file.Path;
import java.util.Locale;
import com.aspose.note.Document;
import com.aspose.note.License;
import com.aspose.note.LocaleOptions;
```

## Steg 1: Ställ in Aspose‑licens

```java
License license = new License();
license.setLicense("licenseFile");
```

Att ställa in Aspose‑licensen låser upp alla funktioner, inklusive hantering av lokal och bildkonvertering.

## Steg 2: Ställ in standardlokal

```java
java.util.Locale.setDefault(new java.util.Locale("en", "rs"));
```

Här **ställer vi in standardlokal** till engelska (`en`) med landskoden `rs`. Justera språk‑ och landskoderna så att de matchar din målregion.

## Steg 3: Ladda OneNote‑dokument

```java
String inputFile = "Sample1.one";
Path inputPath = Paths.get(inputFile);

Document oneFile = new Document(inputPath.toString());
```

Detta steg **laddar OneNote‑dokumentet** i `Document`‑objektet så att du kan arbeta med dess innehåll.

## Steg 4: Konvertera OneNote till PNG (OneNote‑filkonvertering)

```java
oneFile.save("sample.png");
```

`save`‑metoden utför en **onenote‑filkonvertering**, exporterar anteckningsboken (eller en specifik sida) som en PNG‑bild – i praktiken **convert onenote to png** och **save onenote as image**.

## Vanliga problem & tips

- **Licens hittades inte:** Kontrollera att sökvägen till `licenseFile` är korrekt och att filen har läsbehörighet.  
- **Lokal tillämpas inte:** Anropa `Locale.setDefault` **innan** du laddar dokumentet.  
- **Bildutdata saknas:** Verifiera att OneNote‑filen faktiskt innehåller renderbara sidor; tomma anteckningsböcker ger en tom PNG.

## Vanliga frågor

**Q: Är Aspose.Note kompatibel med olika versioner av Java?**  
A: Ja, Aspose.Note stödjer Java 8 och senare, vilket säkerställer bred kompatibilitet över utvecklingsmiljöer.

**Q: Kan jag integrera Aspose.Note med andra Java‑bibliotek?**  
A: Absolut. API‑et fungerar sömlöst med populära bibliotek som Apache POI, Jackson och Spring.

**Q: Erbjuder Aspose.Note stöd för olika filformat?**  
A: Även om huvudfokus är OneNote‑filer kan biblioteket exportera till PNG, JPEG, PDF och andra bildformat.

**Q: Finns det ett community‑forum för Aspose.Note‑användare att söka hjälp och dela kunskap?**  
A: Ja, Aspose‑community‑forumet erbjuder en plattform för användare att interagera med experter, ställa frågor och samarbeta på lösningar. Besök [support forum](https://forum.aspose.com/c/note/28) för hjälp.

**Q: Kan jag prova Aspose.Note innan jag köper?**  
A: Självklart, du kan utforska funktionerna i Aspose.Note genom att utnyttja den kostnadsfria provversionen som erbjuds på webbplatsen.

## Slutsats

Genom att följa dessa steg har du lärt dig hur du **ställer in standardlokal**, **laddar OneNote‑dokument**, **ställer in Aspose‑licens** och **konverterar OneNote till PNG** med Aspose.Note för Java. Detta arbetsflöde ger dig möjlighet att skapa lokal‑anpassade rapporter och bilder som riktar sig till en global publik.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Senast uppdaterad:** 2026-01-05  
**Testad med:** Aspose.Note 24.11 för Java  
**Författare:** Aspose  

---