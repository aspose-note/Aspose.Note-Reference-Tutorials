---
date: 2026-02-07
description: Lär dig hur du exporterar teckensnitt när du sparar OneNote som HTML
  med Aspose.Note för Java. Den här guiden visar hur du skapar OneNote programmässigt
  och bäddar in teckensnitt, CSS och bilder.
linktitle: How to Export Fonts When Saving OneNote as HTML – Java
second_title: Aspose.Note Java API
title: Hur man exporterar teckensnitt när man sparar OneNote som HTML – Java
url: /sv/java/onenote-document-loading/create-onenote-save-to-html/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hur man exporterar teckensnitt när man sparar OneNote som HTML – Java

## Introduktion

I den här handledningen får du veta **hur man exporterar teckensnitt** när du **sparar OneNote som HTML** med Aspose.Note för Java. Vi går igenom hur du skapar ett OneNote‑dokument programatiskt, konfigurerar HTML‑sparalternativen och bäddar in de nödvändiga teckensnitts‑filerna så att den resulterande HTML‑filen ser exakt likadan ut som de ursprungliga OneNote‑sidorna. Detta tillvägagångssätt är perfekt när du behöver bevara den visuella integriteten i OneNote‑innehållet i ett webbvänligt format.

## Snabba svar
- **Vilket bibliotek hanterar exporten?** Aspose.Note för Java  
- **Kan teckensnitt bäddas in i HTML?** Ja – sätt `ExportFonts` till `ExportEmbedded`  
- **Behöver jag en licens för produktion?** En giltig Aspose.Note‑licens krävs för kommersiell användning  
- **Vilken Java‑version stöds?** Java 8 eller högre  
- **Är det möjligt att spara resurser i separata filer?** Absolut – konfigurera `ResourceExportType` därefter  

## Vad betyder “exportera teckensnitt” i samband med OneNote HTML‑konvertering?

När du konverterar en OneNote‑anteckningsbok till HTML beror det visuella utseendet på CSS, bilder och särskilt de teckensnitt som används i de ursprungliga sidorna. **Exportera teckensnitt** innebär att bädda in teckensnitts‑filerna (t.ex. TTF) direkt i HTML‑paketet så att webbläsare kan rendera texten exakt som den visas i OneNote, även om slutanvändaren inte har dessa teckensnitt installerade lokalt.

## Varför skapa OneNote programatiskt och spara det som HTML?

- **Automation:** Generera rapporter, dokumentation eller kunskapsbas‑artiklar från OneNote utan manuellt kopierande.  
- **Konsistens:** Bevara layout, styling och anpassade teckensnitt över enheter.  
- **Portabilitet:** HTML kan visas överallt – ingen OneNote‑klient behövs.  

## Förutsättningar

1. Java Development Kit (JDK) 8 eller nyare installerat.  
2. Aspose.Note för Java‑biblioteket – ladda ner från [här](https://releases.aspose.com/note/java/).  
3. En exempel‑OneNote‑fil (`.one`) att läsa in, eller så kan du skapa en ny programatiskt.  

## Importera paket

Importera först de nödvändiga klasserna i ditt Java‑projekt:

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

## Hur man exporterar teckensnitt när man sparar OneNote som HTML?

Nedan följer en steg‑för‑steg‑guide som visar dig **hur man exporterar teckensnitt** och andra resurser.

### Steg 1: Skapa ett OneNote‑dokument programatiskt  

```java
Document document = new Document("Path_to_your_sample_one_file");
```

Den här raden laddar en befintlig `.one`‑fil. Om du behöver **skapa OneNote programatiskt**, kan du instansiera ett nytt `Document`‑objekt och lägga till sektioner/sidor via API‑et (visas inte här för att hålla fokus på export av teckensnitt).

### Steg 2: Spara till ett minnesström med inbäddade teckensnitt  

```java
HtmlSaveOptions options = new HtmlSaveOptions();
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);
options.setFontFaceTypes(FontFaceType.Ttf);

ByteArrayOutputStream outputStream = new ByteArrayOutputStream();
document.save(outputStream, options);
```

- `setExportFonts(ResourceExportType.ExportEmbedded)` instruerar Aspose.Note att **exportera teckensnitt** direkt in i HTML‑paketet.  
- `setFontFaceTypes(FontFaceType.Ttf)` säkerställer att TrueType‑teckensnitt används, vilket har bred stöd i webbläsare.

### Steg 3: Spara som HTML med separata resursfiler (fortfarande exporterar teckensnitt)  

```java
HtmlSaveOptions options = new HtmlSaveOptions();
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);

document.save("output_directory/document.html", options);
```

Även om CSS och bilder är inbäddade kan du ändra `ResourceExportType` till `ExportExternal` om du föredrar separata filer för enklare cachning. Huvuddelen – **exportera teckensnitt** – förblir oförändrad.

### Steg 4: Använd callbacks för att styra var varje resurs lagras  

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

Klassen `UserSavingCallbacks` (du måste implementera `ICssSavingCallback`, `IImageSavingCallback` och `IFontSavingCallback`) ger dig full kontroll över mappstrukturen, så att du kan hålla teckensnitt i en dedikerad `fonts`‑katalog samtidigt som du **exporterar teckensnitt** korrekt.

## Hur man bäddar in anpassade teckensnitt vid konvertering av OneNote till HTML

Att bädda in anpassade teckensnitt garanterar att HTML‑renderingen matchar den ursprungliga OneNote‑layouten, även på enheter som inte har dessa teckensnitt installerade. Genom att använda `ExportEmbedded` tillsammans med `FontFaceType.Ttf` kodas TrueType‑filerna som base‑64 och infogas direkt i den genererade CSS‑filen, vilket eliminerar behovet av extern teckensnittshosting.

## Användning av ResourceExportType för att styra resursexport

`ResourceExportType` låter dig bestämma om CSS, bilder och teckensnitt lagras **inuti** HTML‑filen (`ExportEmbedded`) eller sparas som **externa** filer (`ExportExternal`). Välj `ExportEmbedded` för en en‑filslösning, eller `ExportExternal` när du vill utnyttja webbläsarcachning för stora tillgångar.

## Skapa OneNote programatiskt för HTML‑export

Om du börjar från början kan du bygga ett OneNote‑dokument helt i kod, lägga till sektioner, sidor och rik text, och sedan tillämpa samma `HtmlSaveOptions` som visas ovan. Detta ger dig helautomatisering: från datagenerering till ett fullt stylat HTML‑utdata med inbäddade anpassade teckensnitt.

## Vanliga problem & tips

- **Saknade teckensnitt i utdata:** Verifiera att `setExportFonts(ResourceExportType.ExportEmbedded)` är satt och att käll‑OneNote‑filen faktiskt använder inbäddade teckensnitt.  
- **Stora HTML‑filer:** Inbäddning av teckensnitt kan öka filstorleken. Om bandbredd är ett problem, byt `ExportFonts` till `ExportExternal` och hosta teckensnitten på ett CDN.  
- **Fel i callback‑implementation:** Säkerställ att dina callback‑klasser korrekt skriver strömmen och stänger resurser för att undvika filkorruption.  

## Vanliga frågor

**Q: Kan jag konvertera flera OneNote‑dokument till HTML på en gång?**  
A: Ja, loopa igenom varje `Document`‑instans och tillämpa samma `HtmlSaveOptions`.  

**Q: Stöder Aspose.Note för Java andra utdataformat än HTML?**  
A: Absolut. Du kan exportera till PDF, DOCX, PNG, JPEG och mer med motsvarande sparalternativ.  

**Q: Finns det en provversion av Aspose.Note för Java?**  
A: Ja, ladda ner en gratis provversion från [här](https://releases.aspose.com/).  

**Q: Var kan jag få support för Aspose.Note för Java?**  
A: Besök [Aspose.Note‑forumet](https://forum.aspose.com/c/note/28) för community‑ och officiell hjälp.  

**Q: Hur kan jag köpa en licens för Aspose.Note för Java?**  
A: Licenser finns tillgängliga på [Aspose‑webbplatsen](https://purchase.aspose.com/buy).  

## Slutsats

Du vet nu **hur man exporterar teckensnitt** när du **sparar OneNote som HTML** med Aspose.Note för Java. Genom att konfigurera `HtmlSaveOptions` och eventuellt använda callbacks kan du bevara exakt utseende på dina OneNote‑sidor — inklusive anpassade teckensnitt — när du levererar dem på webben. Känn dig fri att experimentera med olika `ResourceExportType`‑inställningar för att passa ditt projekts prestanda‑ och lagringskrav.

---

**Last Updated:** 2026-02-07  
**Tested With:** Aspose.Note för Java 24.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}