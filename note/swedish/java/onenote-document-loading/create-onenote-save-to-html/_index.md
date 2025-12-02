---
date: 2025-12-02
description: Lär dig hur du exporterar teckensnitt när du sparar OneNote som HTML
  med Aspose.Note för Java. Den här guiden visar hur du skapar OneNote programatiskt
  och bäddar in teckensnitt, CSS och bilder.
language: sv
linktitle: How to Export Fonts When Saving OneNote as HTML – Java
second_title: Aspose.Note Java API
title: Hur man exporterar typsnitt när man sparar OneNote som HTML – Java
url: /java/onenote-document-loading/create-onenote-save-to-html/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hur man exporterar teckensnitt när man sparar OneNote som HTML – Java

## Introduktion

I den här handledningen kommer du att upptäcka **hur man exporterar teckensnitt** när du **sparar OneNote som HTML** med Aspose.Note för Java. Vi går igenom hur man skapar ett OneNote‑dokument programatiskt, konfigurerar HTML‑spara‑alternativen och bäddar in de nödvändiga teckensnitts‑filerna så att den resulterande HTML‑filen ser exakt ut som de ursprungliga OneNote‑sidorna. Detta tillvägagångssätt är perfekt när du behöver bevara den visuella integriteten i OneNote‑innehållet i ett webbvänligt format.

## Snabba svar
- **Vilket bibliotek hanterar exporten?** Aspose.Note for Java  
- **Kan teckensnitt bäddas in i HTML?** Ja – sätt `ExportFonts` till `ExportEmbedded`  
- **Behöver jag en licens för produktion?** En giltig Aspose.Note‑licens krävs för kommersiell användning  
- **Vilken Java‑version stöds?** Java 8 eller högre  
- **Är det möjligt att spara resurser i separata filer?** Absolut – konfigurera `ResourceExportType` därefter  

## Vad betyder “hur man exporterar teckensnitt” i samband med OneNote‑HTML‑konvertering?

När du konverterar en OneNote‑anteckningsbok till HTML beror det visuella utseendet på CSS, bilder och särskilt de teckensnitt som används på de ursprungliga sidorna. **Exportering av teckensnitt** innebär att bädda in teckensnitts‑filerna (t.ex. TTF) direkt i HTML‑paketet så att webbläsare kan rendera texten exakt som den visas i OneNote, även om slutanvändaren inte har dessa teckensnitt installerade lokalt.

## Varför skapa OneNote programatiskt och spara det som HTML?

- **Automation:** Generera rapporter, dokumentation eller kunskapsbasartiklar från OneNote utan manuell kopiering och inklistring.  
- **Konsistens:** Bevara layout, stil och anpassade teckensnitt över enheter.  
- **Portabilitet:** HTML kan visas universellt—ingen OneNote‑klient behövs.  

## Förutsättningar

1. Java Development Kit (JDK) 8 eller nyare installerat.  
2. Aspose.Note för Java‑biblioteket – ladda ner från [here](https://releases.aspose.com/note/java/).  
3. En exempel‑OneNote‑fil (`.one`) att läsa in, eller så kan du skapa en ny programatiskt.  

## Importera paket

Först, importera de nödvändiga klasserna i ditt Java‑projekt:

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

Denna rad laddar en befintlig `.one`‑fil. Om du behöver **skapa OneNote programatiskt**, kan du instansiera ett nytt `Document`‑objekt och lägga till sektioner/sidor via API‑et (visas inte här för att hålla fokus på export av teckensnitt).

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

- `setExportFonts(ResourceExportType.ExportEmbedded)` talar om för Aspose.Note att **exportera teckensnitt** direkt in i HTML‑paketet.  
- `setFontFaceTypes(FontFaceType.Ttf)` säkerställer att TrueType‑teckensnitt används, vilket har bred stöd i webbläsare.

### Steg 3: Spara som HTML med separata resursfiler (fortfarande exporterar teckensnitt)  

```java
HtmlSaveOptions options = new HtmlSaveOptions();
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);

document.save("output_directory/document.html", options);
```

Även om CSS och bilder är inbäddade kan du ändra `ResourceExportType` till `ExportExternal` om du föredrar separata filer för enklare cachning. Huvuddelen—**export av teckensnitt**—förblir oförändrad.

### Steg 4: Använd återanrop för att kontrollera var varje resurs lagras  

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

`UserSavingCallbacks`‑klassen (du måste implementera `ICssSavingCallback`, `IImageSavingCallback` och `IFontSavingCallback`) ger dig full kontroll över mappstrukturen, så att du kan hålla teckensnitt i en dedikerad `fonts`‑katalog samtidigt som du **exporterar teckensnitt** korrekt.

## Vanliga problem & tips

- **Saknade teckensnitt i resultatet:** Verifiera att `setExportFonts(ResourceExportType.ExportEmbedded)` är satt och att käll‑OneNote‑filen faktiskt använder inbäddade teckensnitt.  
- **Stora HTML‑filer:** Inbäddning av teckensnitt kan öka storleken. Om bandbredd är ett problem, byt `ExportFonts` till `ExportExternal` och hosta teckensnitten på en CDN.  
- **Fel i återanrops‑implementation:** Säkerställ att dina återanropsklasser korrekt skriver strömmen och stänger resurser för att undvika filkorruption.  

## Vanliga frågor

**Q: Kan jag konvertera flera OneNote‑dokument till HTML på en gång?**  
A: Ja, loopa igenom varje `Document`‑instans och applicera samma `HtmlSaveOptions`.  

**Q: Stöder Aspose.Note för Java andra utdataformat förutom HTML?**  
A: Absolut. Du kan exportera till PDF, DOCX, PNG, JPEG och mer med lämpliga spara‑alternativ.  

**Q: Finns det en provversion av Aspose.Note för Java?**  
A: Ja, ladda ner en gratis provversion från [here](https://releases.aspose.com/).  

**Q: Var kan jag få support för Aspose.Note för Java?**  
A: Besök [Aspose.Note forum](https://forum.aspose.com/c/note/28) för community‑ och officiell hjälp.  

**Q: Hur kan jag köpa en licens för Aspose.Note för Java?**  
A: Licenser finns på [Aspose website](https://purchase.aspose.com/buy).  

## Slutsats

Du vet nu **hur man exporterar teckensnitt** när du **sparar OneNote som HTML** med Aspose.Note för Java. Genom att konfigurera `HtmlSaveOptions` och eventuellt använda återanrop kan du bevara exakt utseende på dina OneNote‑sidor—inklusive anpassade teckensnitt—när du levererar dem på webben. Känn dig fri att experimentera med olika `ResourceExportType`‑inställningar för att passa ditt projekts prestanda‑ och lagringskrav.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Senast uppdaterad:** 2025-12-02  
**Testat med:** Aspose.Note for Java 24.12  
**Författare:** Aspose  

---