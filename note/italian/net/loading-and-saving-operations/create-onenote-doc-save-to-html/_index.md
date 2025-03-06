---
title: Crea un documento OneNote e salva in HTML in Aspose.Note
linktitle: Crea un documento OneNote e salva in HTML in Aspose.Note
second_title: Aspose.Note API .NET
description: Scopri come creare e salvare documenti Microsoft OneNote in formato HTML nelle applicazioni .NET utilizzando l'API Aspose.Note. Segui il nostro tutorial completo con esempi passo passo.
weight: 14
url: /it/net/loading-and-saving-operations/create-onenote-doc-save-to-html/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Crea un documento OneNote e salva in HTML in Aspose.Note

## introduzione

Aspose.Note per .NET è una potente API che consente agli sviluppatori di lavorare con documenti Microsoft OneNote a livello di codice nelle loro applicazioni .NET. Con Aspose.Note puoi creare, manipolare e convertire file OneNote senza sforzo. In questo tutorial, esploreremo come creare un documento OneNote e salvarlo in formato HTML utilizzando varie opzioni fornite dall'API Aspose.Note per .NET.

## Prerequisiti

Prima di iniziare, assicurati di possedere i seguenti prerequisiti:

- Conoscenza base del linguaggio di programmazione C#.
- Visual Studio installato nel sistema.
-  Aspose.Note per l'API .NET installata nel tuo progetto. Puoi scaricarlo da[Qui](https://releases.aspose.com/note/net/).
- Familiarità con la struttura dei documenti Microsoft OneNote.

## Importa spazi dei nomi

Prima di immergerci nella parte di codifica, importiamo gli spazi dei nomi necessari:

```csharp
using System;
using System.Drawing;
using System.Globalization;
using System.IO;

using Aspose.Note.Saving;
using Aspose.Note.Saving.Html;

```

Ora suddividiamo ogni esempio in più passaggi e vediamo come creare un documento OneNote e salvarlo in formato HTML utilizzando Aspose.Note per .NET.

## Passaggio 1: crea un documento OneNote con opzioni predefinite

```csharp
public static void CreateAndSaveToHTMLUsingDefaultOptions()
{
    // Inizializza il documento OneNote
    Document doc = new Document();
    Page page = doc.AppendChildLast(new Page());

    // Stile predefinito per tutto il testo nel documento.
    ParagraphStyle textStyle = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
    page.Title = new Title()
    {
        TitleText = new RichText() { Text = "Title text.", ParagraphStyle = textStyle },
        TitleDate = new RichText() { Text = new DateTime(2011, 11, 11).ToString("D", CultureInfo.InvariantCulture), ParagraphStyle = textStyle },
        TitleTime = new RichText() { Text = "12:34", ParagraphStyle = textStyle }
    };

    // Salva in formato HTML
    string dataDir = "Your Document Directory";
    string outputPath = Path.Combine(dataDir, "CreateOneNoteDocAndSaveToHTML_out.html");
    doc.Save(outputPath);

    Console.WriteLine("\nOneNote document created successfully.\nFile saved at " + outputPath);
}
```

In questo passaggio inizializziamo un nuovo documento OneNote, aggiungiamo una pagina con un titolo e la salviamo in formato HTML utilizzando le opzioni predefinite.

## Passaggio 2: crea e salva un intervallo di pagine specifico in HTML

```csharp
public static void CreateAndSavePageRange()
{
    // Inizializza il documento OneNote
    Document doc = new Document();
    Page page = doc.AppendChildLast(new Page());

    // Stile predefinito per tutto il testo nel documento.
    ParagraphStyle textStyle = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
    page.Title = new Title()
    {
        TitleText = new RichText() { Text = "Title text.", ParagraphStyle = textStyle },
        TitleDate = new RichText() { Text = new DateTime(2011, 11, 11).ToString("D", CultureInfo.InvariantCulture), ParagraphStyle = textStyle },
        TitleTime = new RichText() { Text = "12:34", ParagraphStyle = textStyle }
    };

    // Salva in formato HTML
    string dataDir = "Your Document Directory";
    string outputPath = Path.Combine(dataDir, "CreateAndSavePageRange_out.html");
    doc.Save(outputPath, new HtmlSaveOptions { PageCount = 1, PageIndex = 0 });

    Console.WriteLine("\nOneNote document created successfully and saved as page range.\nFile saved at " + outputPath);
}
```

Qui, dimostriamo come creare un documento e salvare un intervallo di pagine specifico in formato HTML.

## Passaggio 3: salva come HTML nel flusso di memoria con risorse incorporate

```csharp
public static void SaveAsHTMLToMemoryStreamWithEmbeddedResources()
{
    // Carica il documento OneNote
    string dataDir = "Your Document Directory";
    var document = new Document(Path.Combine(dataDir, "Aspose.one"));

    // Specifica le opzioni di salvataggio HTML
    var options = new HtmlSaveOptions()
    {
        ExportCss = ResourceExportType.ExportEmbedded,
        ExportFonts = ResourceExportType.ExportEmbedded,
        ExportImages = ResourceExportType.ExportEmbedded,
        FontFaceTypes = FontFaceType.Ttf
    };

    // Salvare il documento in un flusso di memoria
    var memoryStream = new MemoryStream();
    document.Save(memoryStream, options);
}
```

Questo passaggio illustra come salvare un documento OneNote in formato HTML con risorse incorporate (CSS, caratteri e immagini) in un flusso di memoria.

## Passaggio 4: salva come HTML in un file con risorse in file separati

```csharp
public static void SaveAsHTMLToFileWithResourcesInSeparateFiles()
{
    // Carica il documento OneNote
    string dataDir = "Your Document Directory";
    var document = new Document(Path.Combine(dataDir, "Aspose.one"));

    // Specifica le opzioni di salvataggio HTML
    var options = new HtmlSaveOptions()
    {
        ExportCss = ResourceExportType.ExportAsStream,
        ExportFonts = ResourceExportType.ExportAsStream,
        ExportImages = ResourceExportType.ExportAsStream,
        FontFaceTypes = FontFaceType.Ttf
    };

    // Salva il documento in un file HTML con le risorse archiviate in file separati
    document.Save(Path.Combine(dataDir, "document_out.html"), options);
}
```

In questo passaggio, salviamo un documento OneNote in formato HTML con tutte le risorse (CSS, caratteri e immagini) archiviate in file separati.

## Passaggio 5: salvare come HTML nel flusso di memoria con richiamate per salvare risorse

```csharp
public static void SaveAsHTMLToMemoryStreamWithCallBacksToSaveResources()
{
    // Specificare la configurazione di salvataggio delle richiamate
    var savingCallbacks = new UserSavingCallbacks()
    {
        RootFolder = "documentFolder",
        CssFolder = "css",
        KeepCssStreamOpened = true,
        ImagesFolder = "images",
        FontsFolder = "fonts"
    };

    // Specifica le opzioni di salvataggio HTML
    var options = new HtmlSaveOptions
    {
        FontFaceTypes = FontFaceType.Ttf,
        CssSavingCallback = savingCallbacks,
        FontSavingCallback = savingCallbacks,
        ImageSavingCallback = savingCallbacks
    };

    // Carica il documento OneNote
    string dataDir = "Your Document Directory";
    var document = new Document(Path.Combine(dataDir, "Aspose.one"));

    // Salva il documento in formato HTML con risorse gestite da callback definiti dall'utente
    using (var stream = File.Create(Path.Combine(savingCallbacks.RootFolder, "document.html")))
    {
        document.Save(stream, options);
    }

    // Aggiungi manualmente i dati al flusso CSS
    using (var writer = new StreamWriter(savingCallbacks.CssStream))
    {
        writer.WriteLine();
        writer.WriteLine("/* This line is appended to stream manually by user */");
    }
}
```

Qui, dimostriamo come salvare un documento OneNote in formato HTML con risorse gestite da callback definiti dall'utente.

## Conclusione

In questo articolo, abbiamo esplorato come lavorare con i documenti OneNote e salvarli in formato HTML utilizzando Aspose.Note per .NET. Seguendo la guida passo passo, puoi farlo facilmente

 integra questa funzionalità nelle tue applicazioni .NET, permettendoti di manipolare i file OneNote in modo efficiente.

## Domande frequenti

### Q1: Posso personalizzare l'aspetto del file HTML salvato?

R1: Sì, puoi personalizzare l'aspetto modificando i fogli di stile CSS generati durante il processo di conversione.

### Q2: Aspose.Note supporta la conversione in altri formati oltre all'HTML?

A2: Sì, Aspose.Note supporta la conversione in vari formati come PDF, immagini e documenti Microsoft Word.

### Q3: Aspose.Note è compatibile con le applicazioni .NET Core?

A3: Sì, Aspose.Note è compatibile sia con le applicazioni .NET Framework che .NET Core.

### Q4: posso estrarre testo e immagini dai documenti OneNote utilizzando Aspose.Note?

A4: Sì, puoi estrarre testo e immagini nonché eseguire varie altre manipolazioni utilizzando l'API Aspose.Note.

### Q5: È disponibile una versione di prova per testare le funzionalità di Aspose.Note?

 R5: Sì, puoi scaricare una versione di prova gratuita da[Qui](https://releases.aspose.com/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
