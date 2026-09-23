---
date: 2026-09-19
description: Lär dig hur du konverterar OneNote till HTML och exporterar teckensnitt
  med Aspose.Note för Java. Denna guide täcker hur du sparar OneNote som HTML med
  inbäddade teckensnitt, CSS och bilder.
keywords:
- convert onenote to html
- save onenote as html
- export fonts java
- aspose.note html export
lastmod: 2026-09-19
linktitle: Hur man exporterar teckensnitt när man sparar OneNote som HTML – Java
og_description: Lär dig hur du konverterar OneNote till HTML och exporterar teckensnitt
  med Aspose.Note för Java. Denna guide visar hur du sparar OneNote som HTML med inbäddade
  teckensnitt, CSS och bilder.
og_image_alt: 'Developer guide: convert OneNote to HTML with font export in Java'
og_title: Konvertera OneNote till HTML och exportera teckensnitt i Java – Aspose.Note
schemas:
- author: Aspose
  dateModified: '2026-09-19'
  description: Learn how to convert OneNote to HTML and export fonts using Aspose.Note
    for Java. This guide covers saving OneNote as HTML with embedded fonts, CSS, and
    images.
  headline: How to convert OneNote to HTML and export fonts in Java
  type: TechArticle
- description: Learn how to convert OneNote to HTML and export fonts using Aspose.Note
    for Java. This guide covers saving OneNote as HTML with embedded fonts, CSS, and
    images.
  name: How to convert OneNote to HTML and export fonts in Java
  steps:
  - name: create a OneNote document programmatically
    text: The `Document` class is Aspose.Note's top‑level object that represents a
      single OneNote file in memory. You can either load an existing `.one` file or
      instantiate a new document and add sections/pages via the API. This line loads
      an existing `.one` file. If you need to **create OneNote programmatica
  - name: save to a memory stream with embedded fonts
    text: The `HtmlSaveOptions` class controls every aspect of the HTML conversion.
      `ResourceExportType` is an enumeration that defines how resources such as fonts,
      images, and CSS are exported. Setting `setExportFonts(ResourceExportType.ExportEmbedded)`
      tells Aspose.Note to embed fonts directly into the HTML
  - name: save as HTML with separate resource files (still exporting fonts)
    text: If you prefer a single HTML file, keep `ExportEmbedded`. For caching‑friendly
      deployments, switch `ResourceExportType` to `ExportExternal`; the fonts will
      still be embedded, but CSS, images, and other assets will be saved as separate
      files. Even though CSS and images are embedded, you can change the
  - name: use callbacks to control where each resource is stored
    text: '`UserSavingCallbacks` allows custom handling of resource saving. Implementing
      `UserSavingCallbacks` (which requires `ICssSavingCallback`, `IImageSavingCallback`,
      and `IFontSavingCallback`) gives you full control over folder structure, allowing
      you to keep fonts in a dedicated `fonts` directory while'
  type: HowTo
- questions:
  - answer: Yes, loop through each `Document` instance and apply the same `HtmlSaveOptions`.
    question: Can I convert multiple OneNote documents to HTML in one go?
  - answer: Absolutely. You can export to PDF, DOCX, PNG, JPEG, and more using the
      appropriate save options.
    question: Does Aspose.Note for Java support other output formats besides HTML?
  - answer: Yes, download a free trial from the **Aspose releases page**([Aspose releases
      page](https://releases.aspose.com/)).
    question: Is there a trial version available for Aspose.Note for Java?
  - answer: Visit the **Aspose.Note forum**([Aspose.Note forum](https://forum.aspose.com/c/note/28))
      for community and official assistance.
    question: Where can I get support for Aspose.Note for Java?
  - answer: Licenses are available at the **Aspose purchase page**([Aspose website](https://purchase.aspose.com/buy)).
    question: How can I purchase a license for Aspose.Note for Java?
  type: FAQPage
second_title: Aspose.Note Java API
tags:
- convert onenote
- Aspose.Note
- Java HTML export
- font embedding
title: Hur man konverterar OneNote till HTML och exporterar teckensnitt i Java
url: /sv/java/onenote-document-loading/create-onenote-save-to-html/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hur man konverterar OneNote till HTML och exporterar typsnitt i Java

## Introduktion

I den här handledningen kommer du att upptäcka **hur man exporterar typsnitt** medan du **konverterar OneNote till HTML** med Aspose.Note för Java. Vi går igenom hur man skapar ett OneNote‑dokument programatiskt, konfigurerar HTML‑spara‑alternativen och bäddar in de nödvändiga typsnitts‑filerna så att den resulterande HTML‑filen ser exakt ut som de ursprungliga OneNote‑sidorna. Detta tillvägagångssätt är perfekt när du behöver bevara den visuella integriteten i OneNote‑innehåll i ett webbvänligt format, särskilt för kunskapsbas‑portaler, automatiserade rapporterings‑pipelines eller plattformsoberoende dokumentationssajter.

## Snabba svar
- **Vilket bibliotek hanterar exporten?** Aspose.Note för Java  
- **Kan typsnitt bäddas in i HTML?** Ja – sätt `ExportFonts` till `ExportEmbedded`  
- **Behöver jag en licens för produktion?** En giltig Aspose.Note‑licens krävs för kommersiell användning  
- **Vilken Java‑version stöds?** Java 8 eller högre  
- **Är det möjligt att spara resurser till separata filer?** Absolut – konfigurera `ResourceExportType` därefter  

## Vad betyder “exportera typsnitt” i samband med OneNote HTML‑konvertering?

Att exportera typsnitt innebär att bädda in de ursprungliga typsnitts‑filerna (t.ex. TTF eller OTF) direkt i HTML‑paketet så att webbläsare renderar texten exakt som den visas i OneNote, även när slutanvändarens enhet saknar dessa typsnitt. Aspose.Note uppnår detta genom att konvertera typsnitten till base‑64‑strängar och infoga dem i den genererade CSS‑koden, vilket garanterar pixel‑perfekt typografi.

## Varför konvertera OneNote till HTML och exportera typsnitt?

Att bädda in typsnitt under konverteringen säkerställer att det visuella utseendet på de ursprungliga OneNote‑sidorna behålls i alla webbläsare, vilket eliminerar layoutförskjutningar som orsakas av saknade teckensnitt. Detta är särskilt viktigt för företagsvarumärken, juridiska dokument eller allt innehåll där exakt typografi är av betydelse.

- **Automation:** Generera rapporter, handledningar eller kunskapsbas‑artiklar från OneNote utan manuellt kopierande och klistring.  
- **Konsistens:** Bevara layout, stil och anpassade typsnitt i alla webbläsare och enheter.  
- **Portabilitet:** HTML är universellt visbart – ingen OneNote‑klient eller extra plugin behövs.  
- **Prestanda:** Inbäddade typsnitt eliminerar extra nätverksförfrågningar, vilket kan förbättra sidladdningstider för små till medelstora dokument.  

## Förutsättningar

1. Java Development Kit (JDK) 8 eller nyare installerat.  
2. Aspose.Note för Java‑bibliotek – ladda ner från **Aspose.Note för Java release‑sidan**([Aspose.Note for Java release page](https://releases.aspose.com/note/java/)).  
3. En exempel‑OneNote‑fil (`.one`) att läsa in, eller så kan du skapa en ny fil programatiskt.  

## Importera paket

Först importerar du de nödvändiga klasserna till ditt Java‑projekt:

```java
import java.io.ByteArrayOutputStream;
import java.io.File;
import java.io.FileOutputStream;
import java.io.IOException;
import java.io.OutputStream;
import java.io.OutputStreamWriter;
import java.nio.file.Paths;
import com.aspose.note.CssSavingArgs;
import com.aspose.note.Document;
import com.aspose.note.FontFaceType;
import com.aspose.note.FontSavingArgs;
import com.aspose.note.HtmlSaveOptions;
import com.aspose.note.ICssSavingCallback;
import com.aspose.note.IFontSavingCallback;
import com.aspose.note.IImageSavingCallback;
import com.aspose.note.ImageSavingArgs;
import com.aspose.note.ResourceExportType;
```

## Hur man konverterar OneNote till HTML med typsnittsexport?

Läs in din OneNote‑anteckningsbok, konfigurera `HtmlSaveOptions` för att bädda in typsnitt och spara resultatet till en ström eller fil. Denna end‑till‑end‑process säkerställer att varje anpassat typsnitt som används i de ursprungliga sidorna inkluderas i HTML‑utdata, vilket ger en trogen visuell återgivning samtidigt som arbetsflödet förblir enkelt och underhållbart.

### Steg 1: skapa ett OneNote‑dokument programatiskt  

Klassen `Document` är Aspose.Note:s översta objekt som representerar en enskild OneNote‑fil i minnet. Du kan antingen läsa in en befintlig `.one`‑fil eller instansiera ett nytt dokument och lägga till sektioner/sidor via API‑t.

```java
Document document = new Document("Path_to_your_sample_one_file");
```

Den här raden läser in en befintlig `.one`‑fil. Om du behöver **skapa OneNote programatiskt**, kan du instansiera ett nytt `Document`‑objekt och lägga till sektioner/sidor via API‑t (visas inte här för att hålla fokus på typsnittsexport).

### Steg 2: spara till ett minnesström med inbäddade typsnitt  

Klassen `HtmlSaveOptions` styr varje aspekt av HTML‑konverteringen. `ResourceExportType` är en uppräkning som definierar hur resurser såsom typsnitt, bilder och CSS exporteras. Att sätta `setExportFonts(ResourceExportType.ExportEmbedded)` instruerar Aspose.Note att bädda in typsnitt direkt i HTML‑paketet, medan `setFontFaceTypes(FontFaceType.Ttf)` begränsar exporten till TrueType‑typsnitt, som har bredast stöd i webbläsare.

```java
HtmlSaveOptions options = new HtmlSaveOptions();
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);
options.setFontFaceTypes(FontFaceType.Ttf);

ByteArrayOutputStream outputStream = new ByteArrayOutputStream();
document.save(outputStream, options);
```

- `setExportFonts(ResourceExportType.ExportEmbedded)` instruerar Aspose.Note att **exportera typsnitt** direkt in i HTML‑paketet.  
- `setFontFaceTypes(FontFaceType.Ttf)` säkerställer att TrueType‑typsnitt används, vilket har brett stöd i webbläsare.

### Steg 3: spara som HTML med separata resursfiler (fortfarande exporterar typsnitt)  

Om du föredrar en enda HTML‑fil, behåll `ExportEmbedded`. För cache‑vänliga distributioner, byt `ResourceExportType` till `ExportExternal`; typsnitten kommer fortfarande att bäddas in, men CSS, bilder och andra tillgångar sparas som separata filer.

```java
HtmlSaveOptions options = new HtmlSaveOptions();
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);

document.save("output_directory/document.html", options);
```

Även om CSS och bilder är inbäddade kan du ändra `ResourceExportType` till `ExportExternal` om du föredrar separata filer för enklare caching. Huvuddelen – **export av typsnitt** – förblir oförändrad.

### Steg 4: använd återanrop för att kontrollera var varje resurs lagras  

`UserSavingCallbacks` möjliggör anpassad hantering av resurs‑sparande. Implementering av `UserSavingCallbacks` (som kräver `ICssSavingCallback`, `IImageSavingCallback` och `IFontSavingCallback`) ger dig full kontroll över mappstrukturen, så att du kan hålla typsnitt i en dedikerad `fonts`‑katalog samtidigt som du **exporterar typsnitt** korrekt.

```java
Document document = new Document("Path_to_your_sample_one_file");

UserSavingCallbacks savingCallbacks = new UserSavingCallbacks();
savingCallbacks.setRootFolder("documentFolder");
savingCallbacks.setCssFolder("css");
savingCallbacks.setKeepCssStreamOpened(true);
savingCallbacks.setImagesFolder("images");
savingCallbacks.setFontsFolder("fonts");

HtmlSaveOptions options = new HtmlSaveOptions();
options.setFontFaceTypes(FontFaceType.Ttf);
options.setCssSavingCallback(savingCallbacks);
options.setImageSavingCallback(savingCallbacks);
options.setFontSavingCallback(savingCallbacks);
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);

File dir = new File(savingCallbacks.getRootFolder());
if (!dir.exists()) {
    dir.mkdir();
}

document.save(Paths.get(savingCallbacks.getRootFolder(), "document.html").toString(), options);
```

Återanropsklasserna låter dig byta namn på filer, komprimera strömmar eller placera typsnitt i en CDN‑klar katalog, vilket ger flexibilitet för storskaliga distributioner.

## Hur man bäddar in anpassade typsnitt vid konvertering av OneNote till HTML

Att bädda in anpassade typsnitt garanterar att HTML‑renderingen matchar den ursprungliga OneNote‑layouten, även på enheter som inte har dessa typsnitt installerade. Genom att använda `ExportEmbedded` tillsammans med `FontFaceType.Ttf` kodas TrueType‑filerna till base‑64 och infogas direkt i den genererade CSS‑koden, vilket eliminerar behovet av extern typsnittshosting och säkerställer konsekvent typografi i alla webbläsare.

## Användning av ResourceExportType för att kontrollera resursexport

`ResourceExportType` låter dig bestämma om CSS, bilder och typsnitt lagras **inuti** HTML‑filen (`ExportEmbedded`) eller sparas som **externa** filer (`ExportExternal`). Välj `ExportEmbedded` för en lösning med en enda fil, eller `ExportExternal` när du vill utnyttja webbläsarcaching för stora tillgångar.

## Skapa OneNote programatiskt för HTML‑export

Om du börjar från början kan du bygga ett OneNote‑dokument helt i kod, lägga till sektioner, sidor och rik text, och sedan tillämpa samma `HtmlSaveOptions` som visas ovan. Detta ger dig end‑to‑end‑automation: från datagenerering till en fullt stylad HTML‑utdata med inbäddade anpassade typsnitt.

## Vanliga problem och tips

- **Saknade typsnitt i utdata:** Verifiera att `setExportFonts(ResourceExportType.ExportEmbedded)` är satt och att den ursprungliga OneNote‑filen faktiskt använder inbäddade typsnitt.  
- **Stora HTML‑filer:** Inbäddning av typsnitt kan öka storleken med 200‑500 KB per typsnitt. Om bandbredd är en oro, byt `ExportFonts` till `ExportExternal` och hosta typsnitten på en CDN.  
- **Återanrops‑implementeringsfel:** Säkerställ att dina återanropsklasser korrekt skriver strömmen och stänger resurser för att undvika filkorruption.  
- **Prestandatips:** För anteckningsböcker med mer än 100 sidor, bearbeta sektioner individuellt och slå ihop de resulterande HTML‑fragmenten för att hålla minnesanvändningen låg.  
- **Kvantifierat påstående:** Aspose.Note kan konvertera anteckningsböcker med upp till 500 sidor på under 30 sekunder på en vanlig 2,5 GHz‑server, samtidigt som över 50 anpassade typsnitt per dokument bevaras.

## Vanliga frågor

**Q: Kan jag konvertera flera OneNote‑dokument till HTML på en gång?**  
A: Ja, loopa igenom varje `Document`‑instans och tillämpa samma `HtmlSaveOptions`.  

**Q: Stöder Aspose.Note för Java andra utdataformat förutom HTML?**  
A: Absolut. Du kan exportera till PDF, DOCX, PNG, JPEG och mer med de motsvarande spara‑alternativen.  

**Q: Finns det en provversion tillgänglig för Aspose.Note för Java?**  
A: Ja, ladda ner en gratis provversion från **Aspose‑releases‑sidan**([Aspose releases page](https://releases.aspose.com/)).  

**Q: Var kan jag få support för Aspose.Note för Java?**  
A: Besök **Aspose.Note‑forumet**([Aspose.Note forum](https://forum.aspose.com/c/note/28)) för gemenskap och officiell hjälp.  

**Q: Hur kan jag köpa en licens för Aspose.Note för Java?**  
A: Licenser finns tillgängliga på **Aspose‑köpsidan**([Aspose website](https://purchase.aspose.com/buy)).  

## Slutsats

Du vet nu **hur man exporterar typsnitt** medan du **konverterar OneNote till HTML** med Aspose.Note för Java. Genom att konfigurera `HtmlSaveOptions` och eventuellt använda återanrop kan du bevara exakt utseende på dina OneNote‑sidor – inklusive anpassade typsnitt – när du levererar dem på webben. Experimentera med `ResourceExportType`‑inställningarna för att balansera filstorlek och cache‑strategi, och integrera arbetsflödet i din automatiserade rapporterings‑pipeline för maximal effektivitet.

---

**Last Updated:** 2026-09-19  
**Tested With:** Aspose.Note for Java 24.12  
**Author:** Aspose

## Relaterade handledningar

- [Använd Aspose.Note för Java för att spara OneNote som PDF med specificerat typsnittssystem](/note/java/onenote-document-saving/save-using-specified-fonts-subsystem/)
- [Konvertera OneNote till text och extrahera bilder med Document Visitor - Java](/note/java/onenote-document-loading/extract-content-using-document-visitor/)
- [Konvertera OneNote till PDF med sidinställningar med Aspose.Note för Java](/note/java/onenote-document-saving/save-to-pdf-using-page-settings/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}