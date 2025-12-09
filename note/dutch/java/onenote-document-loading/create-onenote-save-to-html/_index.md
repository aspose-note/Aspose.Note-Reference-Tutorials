---
date: 2025-12-02
description: Leer hoe u lettertypen kunt exporteren terwijl u OneNote opslaat als
  HTML met Aspose.Note voor Java. Deze gids laat zien hoe u OneNote via code kunt
  maken en lettertypen, CSS en afbeeldingen kunt insluiten.
linktitle: How to Export Fonts When Saving OneNote as HTML – Java
second_title: Aspose.Note Java API
title: Hoe lettertypen exporteren bij het opslaan van OneNote als HTML – Java
url: /nl/java/onenote-document-loading/create-onenote-save-to-html/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hoe lettertypen exporteren bij het opslaan van OneNote als HTML – Java

## Introductie

In deze tutorial ontdek je **hoe je lettertypen kunt exporteren** wanneer je **OneNote opslaat als HTML** met Aspose.Note for Java. We lopen stap voor stap door het programmatically maken van een OneNote-document, het configureren van de HTML-opslagopties, en het insluiten van de benodigde lettertypebestanden zodat de resulterende HTML er precies uitziet als de oorspronkelijke OneNote-pagina's. Deze aanpak is perfect wanneer je de visuele getrouwheid van OneNote-inhoud in een web‑vriendelijk formaat moet behouden.

## Snelle antwoorden
- **Welke bibliotheek behandelt de export?** Aspose.Note for Java  
- **Kunnen lettertypen in de HTML worden ingesloten?** Ja – stel `ExportFonts` in op `ExportEmbedded`  
- **Heb ik een licentie nodig voor productie?** Een geldige Aspose.Note-licentie is vereist voor commercieel gebruik  
- **Welke Java‑versie wordt ondersteund?** Java 8 of hoger  
- **Is het mogelijk om bronnen op te slaan in afzonderlijke bestanden?** Absoluut – configureer `ResourceExportType` dienovereenkomstig  

## Wat betekent “hoe lettertypen exporteren” in de context van OneNote HTML-conversie?

Wanneer je een OneNote-notebook converteert naar HTML, hangt het visuele uiterlijk af van CSS, afbeeldingen en vooral de lettertypen die in de oorspronkelijke pagina's worden gebruikt. **Lettertypen exporteren** betekent dat de lettertypebestanden (bijv. TTF) direct in het HTML‑pakket worden ingesloten zodat browsers de tekst precies kunnen weergeven zoals deze in OneNote verschijnt, zelfs als de eindgebruiker die lettertypen niet lokaal geïnstalleerd heeft.

## Waarom OneNote programmatically maken en opslaan als HTML?

- **Automatisering:** Genereer rapporten, documentatie of kennisbank‑artikelen vanuit OneNote zonder handmatig kopiëren‑en‑plakken.  
- **Consistentie:** Behoud lay-out, styling en aangepaste lettertypen op verschillende apparaten.  
- **Portabiliteit:** HTML is universeel te bekijken—geen OneNote‑client nodig.  

## Voorvereisten

1. Java Development Kit (JDK) 8 of nieuwer geïnstalleerd.  
2. Aspose.Note for Java‑bibliotheek – download van [here](https://releases.aspose.com/note/java/).  
3. Een voorbeeld OneNote‑bestand (`.one`) om te laden, of je kunt programmatically een nieuw bestand maken.  

## Importeer pakketten

First, import the required classes into your Java project:

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

## Hoe lettertypen exporteren bij het opslaan van OneNote als HTML?

Hieronder vind je een stapsgewijze handleiding die je **hoe lettertypen te exporteren** en andere bronnen laat zien.

### Step 1: Create a OneNote document programmatically  

```java
Document document = new Document("Path_to_your_sample_one_file");
```

Deze regel laadt een bestaand `.one`‑bestand. Als je **OneNote programmatically wilt maken**, kun je een nieuw `Document`‑object instantieren en secties/pagina's toevoegen via de API (niet getoond hier om de focus op het exporteren van lettertypen te behouden).

### Step 2: Save to a memory stream with embedded fonts  

```java
HtmlSaveOptions options = new HtmlSaveOptions();
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);
options.setFontFaceTypes(FontFaceType.Ttf);

ByteArrayOutputStream outputStream = new ByteArrayOutputStream();
document.save(outputStream, options);
```

- `setExportFonts(ResourceExportType.ExportEmbedded)` vertelt Aspose.Note om **lettertypen te exporteren** direct in het HTML‑pakket.  
- `setFontFaceTypes(FontFaceType.Ttf)` zorgt ervoor dat TrueType‑lettertypen worden gebruikt, die brede browserondersteuning hebben.

### Step 3: Save as HTML with separate resource files (still exporting fonts)  

```java
HtmlSaveOptions options = new HtmlSaveOptions();
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);

document.save("output_directory/document.html", options);
```

Hoewel CSS en afbeeldingen zijn ingesloten, kun je `ResourceExportType` wijzigen naar `ExportExternal` als je afzonderlijke bestanden verkiest voor eenvoudigere caching. Het belangrijkste onderdeel—**lettertypen exporteren**—blijft ongewijzigd.

### Step 4: Use callbacks to control where each resource is stored  

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

De `UserSavingCallbacks`‑klasse (je moet `ICssSavingCallback`, `IImageSavingCallback` en `IFontSavingCallback` implementeren) geeft je volledige controle over de mapstructuur, waardoor je lettertypen in een aparte `fonts`‑directory kunt bewaren terwijl je nog steeds **lettertypen correct exporteert**.

## Veelvoorkomende problemen & tips

- **Ontbrekende lettertypen in de output:** Controleer of `setExportFonts(ResourceExportType.ExportEmbedded)` is ingesteld en of het bron‑OneNote‑bestand daadwerkelijk ingesloten lettertypen gebruikt.  
- **Grote HTML‑bestanden:** Het insluiten van lettertypen kan de grootte verhogen. Als bandbreedte een zorg is, schakel `ExportFonts` naar `ExportExternal` en host de lettertypen op een CDN.  
- **Fouten in callback‑implementatie:** Zorg ervoor dat je callback‑klassen de stream correct schrijven en bronnen sluiten om bestandscorruptie te voorkomen.  

## Veelgestelde vragen

**V: Kan ik meerdere OneNote‑documenten in één keer naar HTML converteren?**  
A: Ja, loop door elke `Document`‑instantie en pas dezelfde `HtmlSaveOptions` toe.

**V: Ondersteunt Aspose.Note for Java andere uitvoerformaten naast HTML?**  
A: Absoluut. Je kunt exporteren naar PDF, DOCX, PNG, JPEG en meer met de juiste opslagopties.

**V: Is er een proefversie beschikbaar voor Aspose.Note for Java?**  
A: Ja, download een gratis proefversie van [here](https://releases.aspose.com/).

**V: Waar kan ik ondersteuning krijgen voor Aspose.Note for Java?**  
A: Bezoek het [Aspose.Note‑forum](https://forum.aspose.com/c/note/28) voor community‑ en officiële hulp.

**V: Hoe kan ik een licentie aanschaffen voor Aspose.Note for Java?**  
A: Licenties zijn verkrijgbaar op de [Aspose‑website](https://purchase.aspose.com/buy).

## Conclusie

Je weet nu **hoe je lettertypen kunt exporteren** terwijl je **OneNote opslaat als HTML** met Aspose.Note for Java. Door `HtmlSaveOptions` te configureren en eventueel callbacks te gebruiken, kun je het exacte uiterlijk van je OneNote‑pagina's behouden — inclusief aangepaste lettertypen — bij het leveren op het web. Voel je vrij om te experimenteren met verschillende `ResourceExportType`‑instellingen om te voldoen aan de prestatie‑ en opslagvereisten van je project.

---

**Last Updated:** 2025-12-02  
**Tested With:** Aspose.Note for Java 24.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}