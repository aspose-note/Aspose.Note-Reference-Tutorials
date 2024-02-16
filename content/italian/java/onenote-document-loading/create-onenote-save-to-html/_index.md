---
title: Crea un documento OneNote e salva in HTML - Java
linktitle: Crea un documento OneNote e salva in HTML - Java
second_title: Aspose.Note API Java
description: Impara a creare e salvare documenti OneNote come HTML utilizzando Aspose.Note per Java. Integrazione in applicazioni Java per la gestione programmatica dei file OneNote.

type: docs
weight: 18
url: /it/java/onenote-document-loading/create-onenote-save-to-html/
---
## introduzione

Aspose.Note per Java è una potente libreria che consente agli sviluppatori di lavorare con i file Microsoft OneNote a livello di codice. In questo tutorial esploreremo come creare un documento OneNote e salvarlo in formato HTML utilizzando Aspose.Note per Java.

## Prerequisiti

Prima di iniziare, assicurati di avere quanto segue:

1. Java Development Kit (JDK) installato sul tuo sistema.
2.  Aspose.Note per la libreria Java. Puoi scaricarlo da[Qui](https://releases.aspose.com/note/java/).
3. Conoscenza base della programmazione Java.

## Importa pacchetti

Innanzitutto, importa i pacchetti necessari nel tuo progetto Java:

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

## Passaggio 1: crea un oggetto documento OneNote

```java
Document document = new Document("Path_to_your_sample_one_file");
```

 Questo codice inizializza a`Document` oggetto caricando un file OneNote di esempio.

## Passaggio 2: salva come HTML nel flusso di memoria

```java
HtmlSaveOptions options = new HtmlSaveOptions();
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);
options.setFontFaceTypes(FontFaceType.Ttf);

ByteArrayOutputStream outputStream = new ByteArrayOutputStream();
document.save(outputStream, options);
```

Qui impostiamo le opzioni di salvataggio HTML e salviamo il documento in un flusso di memoria.

## Passaggio 3: salva come HTML con le risorse in file separati

```java
HtmlSaveOptions options = new HtmlSaveOptions();
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);

document.save("output_directory/document.html", options);
```

Questo passaggio salva il documento come HTML con risorse come CSS, caratteri e immagini in file separati.

## Passaggio 4: salva come HTML nel flusso di memoria con richiamate per salvare risorse

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

Qui salviamo il documento come HTML in un flusso di memoria utilizzando i callback per gestire il risparmio delle risorse.

## Conclusione

Congratulazioni! Hai imparato come creare un documento OneNote e salvarlo in formato HTML utilizzando Aspose.Note per Java. Ora puoi integrare questa funzionalità nelle tue applicazioni Java per lavorare con i file OneNote a livello di codice.

## Domande frequenti

### Q1: posso convertire più documenti OneNote in HTML in una volta sola?

R1: Sì, è possibile scorrere più documenti e applicare il processo di salvataggio in modo iterativo.

### Q2: Aspose.Note per Java supporta altri formati di output oltre all'HTML?

A2: Sì, Aspose.Note per Java supporta vari formati di output tra cui PDF, DOCX e formati di immagine.

### Q3: È disponibile una versione di prova per Aspose.Note per Java?

R3: Sì, puoi scaricare una versione di prova gratuita da[Qui](https://releases.aspose.com/).

### Q4: Dove posso ottenere supporto per Aspose.Note per Java?

 A4: Puoi ottenere supporto da[Forum Aspose.Note](https://forum.aspose.com/c/note/28).

### Q5: Come posso acquistare una licenza per Aspose.Note per Java?

 A5: È possibile acquistare una licenza da[Sito web Aspose](https://purchase.aspose.com/buy).