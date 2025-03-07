---
title: Salva utilizzando i caratteri specificati in Aspose.Note
linktitle: Salva utilizzando i caratteri specificati in Aspose.Note
second_title: Aspose.Note API .NET
description: Scopri come salvare documenti con i caratteri specificati in Aspose.Note per .NET. Personalizza facilmente le impostazioni dei caratteri per una formattazione coerente dei documenti.
weight: 28
url: /it/net/loading-and-saving-operations/save-using-specified-fonts/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Salva utilizzando i caratteri specificati in Aspose.Note

## introduzione

In questo tutorial impareremo come salvare i documenti utilizzando i caratteri specificati in Aspose.Note per .NET. Esploreremo diversi metodi per raggiungere questo obiettivo, passo dopo passo.

## Prerequisiti

Prima di iniziare, assicurati di avere quanto segue:

1.  Aspose.Note per .NET: assicurati di aver installato Aspose.Note per .NET. Puoi scaricarlo da[Qui](https://releases.aspose.com/note/net/).

2. Ambiente di sviluppo: è necessario un ambiente di sviluppo configurato per lo sviluppo .NET.

## Importa spazi dei nomi

Innanzitutto, importiamo gli spazi dei nomi necessari:

```csharp
using System;
using System.IO;

using Aspose.Note.Fonts;
using Aspose.Note.Saving;

```

## Passaggio 1: salvataggio con nome carattere predefinito

In questo passaggio, salveremo un documento utilizzando il nome del carattere predefinito specificato.

```csharp
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontName()
{
    // Il percorso della directory dei documenti.
    string dataDir = "Your Document Directory";

    // Caricare il documento in Aspose.Note.
    Document oneFile = new Document(Path.Combine(dataDir, "missing-font.one"));

    // Salva il documento come PDF con il carattere predefinito specificato.
    dataDir = dataDir + "SaveUsingDocumentFontsSubsystemWithDefaultFontName_out.pdf";
    oneFile.Save(dataDir, new PdfSaveOptions()
                          {
                              FontsSubsystem = DocumentFontsSubsystem.UsingDefaultFont("Times New Roman")
                          });
}
```

## Passaggio 2: salvataggio con carattere predefinito dal file

Successivamente, salviamo un documento utilizzando un carattere predefinito caricato da un file.

```csharp
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontFromFile()
{
    // Il percorso della directory dei documenti.
    string dataDir = "Your Document Directory";

    string fontFile = Path.Combine(dataDir, "geo_1.ttf");

    // Caricare il documento in Aspose.Note.
    Document oneFile = new Document(Path.Combine(dataDir, "missing-font.one"));

    // Salva il documento come PDF con il carattere predefinito caricato dal file.
    dataDir = dataDir + "SaveUsingDocumentFontsSubsystemWithDefaultFontFromFile_out.pdf";
    oneFile.Save(dataDir, new PdfSaveOptions()
                          {
                              FontsSubsystem = DocumentFontsSubsystem.UsingDefaultFontFromFile(fontFile)
                          });
}
```

## Passaggio 3: salvataggio con carattere predefinito dallo stream

Infine, salviamo un documento utilizzando un carattere predefinito caricato da uno stream.

```csharp
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontFromStream()
{
    // Il percorso della directory dei documenti.
    string dataDir = "Your Document Directory";

    string fontFile = Path.Combine(dataDir, "geo_1.ttf");

    // Caricare il documento in Aspose.Note.
    Document oneFile = new Document(Path.Combine(dataDir, "missing-font.one"));

    // Salva il documento come PDF con il carattere predefinito caricato dallo stream.
    dataDir = dataDir + "SaveUsingDocumentFontsSubsystemWithDefaultFontFromStream_out.pdf";

    using (var stream = File.Open(fontFile, FileMode.Open, FileAccess.Read, FileShare.Read))
    {
        oneFile.Save(dataDir, new PdfSaveOptions()
                              {
                                  FontsSubsystem = DocumentFontsSubsystem.UsingDefaultFontFromStream(stream)
                              });
    }
}
```

## Conclusione

In questo tutorial, abbiamo esplorato come salvare i documenti utilizzando i caratteri specificati in Aspose.Note per .NET. Seguendo questi passaggi, puoi personalizzare le impostazioni dei caratteri in base alle tue esigenze, assicurandoti che i tuoi documenti siano formattati come desideri.

## Domande frequenti

### Q1: posso utilizzare qualsiasi tipo di carattere per salvare documenti in Aspose.Note?

A1: Sì, puoi specificare qualsiasi carattere per il salvataggio dei documenti. Assicurati solo che il file del carattere sia accessibile e caricato correttamente.

### Q2: Aspose.Note è compatibile con diversi formati di documenti?

A2: Aspose.Note funziona principalmente con i documenti OneNote ma fornisce opzioni per salvare in vari formati, incluso PDF.

### Q3: Come posso gestire i caratteri mancanti durante il salvataggio dei documenti?

A3: Aspose.Note offre opzioni per utilizzare i caratteri predefiniti nel caso in cui manchi il carattere specificato, garantendo una formattazione coerente del documento.

### Q4: Aspose.Note supporta l'incorporamento dei caratteri nei documenti di output?

A4: Sì, Aspose.Note consente di incorporare caratteri per garantire la portabilità dei documenti e un rendering coerente su diverse piattaforme.

### Q5: Dove posso ottenere ulteriore assistenza con Aspose.Note?

 R5: Per ulteriore assistenza o supporto tecnico, è possibile visitare il[Forum Aspose.Note](https://forum.aspose.com/c/note/28).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
