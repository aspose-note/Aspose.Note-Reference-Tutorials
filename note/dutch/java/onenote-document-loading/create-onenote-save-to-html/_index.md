---
title: Maak een OneNote-document en sla het op in HTML - Java
linktitle: Maak een OneNote-document en sla het op in HTML - Java
second_title: Aspose.Note Java-API
description: Leer OneNote-documenten maken en opslaan als HTML met Aspose.Note voor Java. Integreer in Java-applicaties voor programmatische verwerking van OneNote-bestanden.

type: docs
weight: 18
url: /nl/java/onenote-document-loading/create-onenote-save-to-html/
---
## Invoering

Aspose.Note voor Java is een krachtige bibliotheek waarmee ontwikkelaars programmatisch met Microsoft OneNote-bestanden kunnen werken. In deze zelfstudie onderzoeken we hoe u een OneNote-document kunt maken en dit in HTML-indeling kunt opslaan met Aspose.Note voor Java.

## Vereisten

Voordat we beginnen, zorg ervoor dat u over het volgende beschikt:

1. Java Development Kit (JDK) op uw systeem geïnstalleerd.
2.  Aspose.Note voor Java-bibliotheek. Je kunt het downloaden van[hier](https://releases.aspose.com/note/java/).
3. Basiskennis van Java-programmeren.

## Pakketten importeren

Importeer eerst de benodigde pakketten in uw Java-project:

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

## Stap 1: Maak een OneNote-documentobject

```java
Document document = new Document("Path_to_your_sample_one_file");
```

 Deze code initialiseert een`Document` object door een voorbeeld van een OneNote-bestand te laden.

## Stap 2: Opslaan als HTML in Memory Stream

```java
HtmlSaveOptions options = new HtmlSaveOptions();
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);
options.setFontFaceTypes(FontFaceType.Ttf);

ByteArrayOutputStream outputStream = new ByteArrayOutputStream();
document.save(outputStream, options);
```

Hier stellen we de HTML-opslagopties in en slaan we het document op in een geheugenstroom.

## Stap 3: Opslaan als HTML met bronnen in afzonderlijke bestanden

```java
HtmlSaveOptions options = new HtmlSaveOptions();
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);

document.save("output_directory/document.html", options);
```

Met deze stap wordt het document opgeslagen als HTML met bronnen zoals CSS, lettertypen en afbeeldingen in afzonderlijke bestanden.

## Stap 4: Opslaan als HTML in Memory Stream met callbacks om bronnen op te slaan

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

Hier slaan we het document op als HTML in een geheugenstroom met behulp van callbacks om de besparing van bronnen te verwerken.

## Conclusie

Gefeliciteerd! U hebt geleerd hoe u een OneNote-document kunt maken en dit in HTML-indeling kunt opslaan met Aspose.Note voor Java. U kunt deze functionaliteit nu in uw Java-toepassingen integreren om programmatisch met OneNote-bestanden te werken.

## Veelgestelde vragen

### V1: Kan ik meerdere OneNote-documenten in één keer naar HTML converteren?

A1: Ja, u kunt meerdere documenten doorlopen en het opslagproces iteratief toepassen.

### V2: Ondersteunt Aspose.Note voor Java naast HTML ook andere uitvoerformaten?

A2: Ja, Aspose.Note voor Java ondersteunt verschillende uitvoerformaten, waaronder PDF, DOCX en afbeeldingsformaten.

### V3: Is er een proefversie beschikbaar voor Aspose.Note voor Java?

A3: Ja, u kunt een gratis proefversie downloaden van[hier](https://releases.aspose.com/).

### V4: Waar kan ik ondersteuning krijgen voor Aspose.Note voor Java?

 A4: U kunt ondersteuning krijgen van de[Aspose.Note-forum](https://forum.aspose.com/c/note/28).

### V5: Hoe kan ik een licentie kopen voor Aspose.Note voor Java?

 A5: U kunt een licentie kopen bij de[Aspose-website](https://purchase.aspose.com/buy).