---
date: 2026-02-07
description: Leer hoe je lettertypen kunt exporteren terwijl je OneNote opslaat als
  HTML met Aspose.Note voor Java. Deze gids laat zien hoe je OneNote programmatisch
  kunt maken en lettertypen, CSS en afbeeldingen kunt insluiten.
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

## Inleiding

In deze tutorial ontdek je **hoe je lettertypen kunt exporteren** wanneer je **OneNote opslaat als HTML** met Aspose.Note voor Java. We lopen stap voor stap door het programmatic maken van een OneNote‑document, het configureren van de HTML‑opslaan‑opties en het insluiten van de benodigde lettertypebestanden zodat de resulterende HTML er precies uitziet als de oorspronkelijke OneNote‑pagina's. Deze aanpak is perfect wanneer je de visuele getrouwheid van OneNote‑inhoud in een web‑vriendelijk formaat wilt behouden.

## Snelle antwoorden
- **Welke bibliotheek behandelt de export?** Aspose.Note voor Java  
- **Kunnen lettertypen in de HTML worden ingesloten?** Ja – stel `ExportFonts` in op `ExportEmbedded`  
- **Heb ik een licentie nodig voor productie?** Een geldige Aspose.Note‑licentie is vereist voor commercieel gebruik  
- **Welke Java‑versie wordt ondersteund?** Java 8 of hoger  
- **Is het mogelijk om bronnen naar aparte bestanden op te slaan?** Absoluut – configureer `ResourceExportType` dienovereenkomstig  

## Wat betekent “hoe lettertypen exporteren” in de context van OneNote‑HTML‑conversie?

Wanneer je een OneNote‑notitieboek converteert naar HTML, hangt het visuele uiterlijk af van CSS, afbeeldingen en vooral de lettertypen die in de oorspronkelijke pagina's worden gebruikt. **Lettertypen exporteren** betekent dat de lettertypebestanden (bijv. TTF) direct in het HTML‑pakket worden ingebed zodat browsers de tekst exact kunnen weergeven zoals deze in OneNote verschijnt, zelfs als de eindgebruiker die lettertypen niet lokaal geïnstalleerd heeft.

## Waarom OneNote programmatic maken en opslaan als HTML?

- **Automatisering:** Genereer rapporten, documentatie of kennisbank‑artikelen vanuit OneNote zonder handmatig kopiëren‑plakken.  
- **Consistentie:** Behoud lay‑out, styling en aangepaste lettertypen op verschillende apparaten.  
- **Draagbaarheid:** HTML is universeel bekijkbaar—geen OneNote‑client nodig.  

## Voorvereisten

1. Java Development Kit (JDK) 8 of nieuwer geïnstalleerd.  
2. Aspose.Note voor Java‑bibliotheek – download van [hier](https://releases.aspose.com/note/java/).  
3. Een voorbeeld‑OneNote‑bestand (`.one`) om te laden, of je kunt een nieuw bestand programmatic maken.  

## Importpakketten

Importeer eerst de benodigde klassen in je Java‑project:

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

## Hoe lettertypen exporteren tijdens het opslaan van OneNote als HTML?

Hieronder vind je een stapsgewijze handleiding die laat zien **hoe je lettertypen exporteert** en andere bronnen.

### Stap 1: Een OneNote‑document programmatic maken  

```java
Document document = new Document("Path_to_your_sample_one_file");
```

Deze regel laadt een bestaand `.one`‑bestand. Als je **OneNote programmatic wilt maken**, kun je een nieuw `Document`‑object instantieren en secties/pagina's toevoegen via de API (niet getoond om de focus op het exporteren van lettertypen te houden).

### Stap 2: Opslaan naar een geheugen‑stream met ingesloten lettertypen  

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

### Stap 3: Opslaan als HTML met aparte bronbestanden (nog steeds lettertypen exporterend)  

```java
HtmlSaveOptions options = new HtmlSaveOptions();
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);

document.save("output_directory/document.html", options);
```

Hoewel CSS en afbeeldingen zijn ingesloten, kun je `ResourceExportType` wijzigen naar `ExportExternal` als je aparte bestanden wilt voor eenvoudigere caching. Het cruciale onderdeel—**lettertypen exporteren**—blijft ongewijzigd.

### Stap 4: Callbacks gebruiken om te bepalen waar elke bron wordt opgeslagen  

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

De `UserSavingCallbacks`‑klasse (je moet `ICssSavingCallback`, `IImageSavingCallback` en `IFontSavingCallback` implementeren) geeft je volledige controle over de mapstructuur, zodat je lettertypen in een aparte `fonts`‑directory kunt plaatsen terwijl je **lettertypen correct exporteert**.

## Hoe aangepaste lettertypen insluiten bij het converteren van OneNote naar HTML

Het insluiten van aangepaste lettertypen garandeert dat de HTML‑rendering overeenkomt met de oorspronkelijke OneNote‑lay‑out, zelfs op apparaten die die lettertypen niet geïnstalleerd hebben. Door `ExportEmbedded` te combineren met `FontFaceType.Ttf` worden de TrueType‑bestanden base‑64 gecodeerd en direct in de gegenereerde CSS geplaatst, waardoor externe hosting van lettertypen overbodig wordt.

## ResourceExportType gebruiken om bronexport te regelen

`ResourceExportType` laat je kiezen of CSS, afbeeldingen en lettertypen **binnen** het HTML‑bestand worden opgeslagen (`ExportEmbedded`) of als **externe** bestanden (`ExportExternal`). Kies `ExportEmbedded` voor een één‑bestand‑oplossing, of `ExportExternal` wanneer je browser‑caching wilt benutten voor grote assets.

## OneNote programmatic maken voor HTML‑export

Als je vanaf nul begint, kun je een OneNote‑document volledig in code bouwen, secties, pagina's en rich text toevoegen, en vervolgens dezelfde `HtmlSaveOptions` toepassen als hierboven getoond. Dit biedt end‑to‑end automatisering: van gegevensgeneratie tot een volledig gestylede HTML‑output met ingesloten aangepaste lettertypen.

## Veelvoorkomende problemen & tips

- **Lettertypen ontbreken in de output:** Controleer of `setExportFonts(ResourceExportType.ExportEmbedded)` is ingesteld en of het bron‑OneNote‑bestand daadwerkelijk ingesloten lettertypen gebruikt.  
- **Grote HTML‑bestanden:** Het insluiten van lettertypen kan de bestandsgrootte verhogen. Als bandbreedte een zorg is, schakel `ExportFonts` over naar `ExportExternal` en host de lettertypen op een CDN.  
- **Fouten in callback‑implementatie:** Zorg ervoor dat je callback‑klassen de stream correct schrijven en resources sluiten om bestandscorruptie te voorkomen.  

## Veelgestelde vragen

**V: Kan ik meerdere OneNote‑documenten in één keer naar HTML converteren?**  
A: Ja, loop door elke `Document`‑instantie en pas dezelfde `HtmlSaveOptions` toe.  

**V: Ondersteunt Aspose.Note voor Java andere uitvoerformaten naast HTML?**  
A: Absoluut. Je kunt exporteren naar PDF, DOCX, PNG, JPEG en meer met de juiste opslaan‑opties.  

**V: Is er een proefversie beschikbaar voor Aspose.Note voor Java?**  
A: Ja, download een gratis proefversie van [hier](https://releases.aspose.com/).  

**V: Waar kan ik ondersteuning krijgen voor Aspose.Note voor Java?**  
A: Bezoek het [Aspose.Note‑forum](https://forum.aspose.com/c/note/28) voor community‑ en officiële hulp.  

**V: Hoe kan ik een licentie aanschaffen voor Aspose.Note voor Java?**  
A: Licenties zijn verkrijgbaar op de [Aspose‑website](https://purchase.aspose.com/buy).  

## Conclusie

Je weet nu **hoe je lettertypen exporteert** terwijl je **OneNote opslaat als HTML** met Aspose.Note voor Java. Door `HtmlSaveOptions` te configureren en eventueel callbacks te gebruiken, kun je het exacte uiterlijk van je OneNote‑pagina's – inclusief aangepaste lettertypen – behouden bij het leveren op het web. Experimenteer gerust met verschillende `ResourceExportType`‑instellingen om te voldoen aan de prestatie‑ en opslagvereisten van je project.

---

**Laatst bijgewerkt:** 2026-02-07  
**Getest met:** Aspose.Note voor Java 24.12  
**Auteur:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}