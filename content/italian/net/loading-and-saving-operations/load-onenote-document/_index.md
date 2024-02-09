---
title: Carica il documento OneNote in Aspose.Note
linktitle: Carica il documento OneNote in Aspose.Note
second_title: Aspose.Note API .NET
description: Scopri come caricare, crittografare e decrittografare i documenti OneNote a livello di codice in .NET utilizzando Aspose.Note.
type: docs
weight: 16
url: /it/net/loading-and-saving-operations/load-onenote-document/
---
## introduzione

Aspose.Note per .NET è una potente API che consente agli sviluppatori di lavorare con i file Microsoft OneNote a livello di codice nelle loro applicazioni .NET. Se hai bisogno di caricare, manipolare o convertire documenti OneNote, Aspose.Note per .NET fornisce funzionalità complete per semplificare il flusso di lavoro.

## Prerequisiti

Prima di immergerti nel tutorial, assicurati di possedere i seguenti prerequisiti:

1. Visual Studio: installa Visual Studio, un ambiente di sviluppo integrato (IDE) completo per lo sviluppo .NET.
2.  Aspose.Note per .NET: Scarica e installa Aspose.Note per .NET da[pagina di download](https://releases.aspose.com/note/net/).
3. Conoscenza di base di C#: la familiarità con i fondamenti del linguaggio di programmazione C# è necessaria per comprendere e implementare gli esempi forniti in questo tutorial.

## Importa spazi dei nomi

Prima di iniziare a lavorare con Aspose.Note per .NET, assicurati di importare gli spazi dei nomi richiesti nel tuo progetto C#:

```csharp
using System;
using System.IO;
```

Suddividiamo ogni esempio in più passaggi:

## Carica il documento OneNote in Aspose.Note

### Passaggio 1: caricamento semplice del notebook:
   -  Inizia creando una nuova istanza di`Notebook` class, passando il percorso al documento OneNote.
   - Scorrere i nodi figlio del notebook utilizzando un ciclo foreach.
   - Visualizza il nome visualizzato di ogni nodo figlio.
   - Esegui azioni specifiche a seconda che il nodo figlio sia un documento o un altro taccuino.

```csharp
public static void SimpleLoadNotebook()
{
    // Il percorso della directory dei documenti.
    string dataDir = "Your Document Directory";
    string fileName = "Open Notebook.onetoc2";
    try
    {
        var notebook = new Notebook(Path.Combine(dataDir, fileName));
        foreach (var notebookChildNode in notebook)
        {
            Console.WriteLine(notebookChildNode.DisplayName);
            if (notebookChildNode is Document)
            {
                // Fai qualcosa con il documento figlio
            }
            else if (notebookChildNode is Notebook)
            {
                // Fai qualcosa con il taccuino per bambini
            }
        }
    }
    catch (Exception ex)
    {
        Console.WriteLine(ex.Message);
    }
}
```

### Passaggio 2: verificare se il documento è crittografato e caricare:
   - Controlla se il documento OneNote è crittografato chiamando il file`Document.IsEncrypted` metodo, passando il nome del file.
   - Se non crittografato, procedere con l'elaborazione del documento.
   - Se crittografato, chiedi all'utente di fornire una password per la decrittografia.

```csharp
public static void Document_CheckIfEncryptedAndLoad()
{
    // Il percorso della directory dei documenti.
    string dataDir = "Your Document Directory";
    string fileName = Path.Combine(dataDir, "Aspose.one");

    Document document;
    if (!Document.IsEncrypted(fileName, out document))
    {
        Console.WriteLine("The document is loaded and ready to be processed.");
    }
    else
    {
        Console.WriteLine("The document is encrypted. Provide a password.");
    }
}
```

### Passaggio 3: verificare se il documento è crittografato tramite password e caricare:
   - Analogamente al passaggio precedente, controlla se il documento è crittografato con una password specifica.
   - Se crittografato e viene fornita la password corretta, procedere con l'elaborazione del documento.
   - Se viene crittografata ma viene fornita una password errata, richiedere all'utente la password non valida.

```csharp
public static void Document_CheckIfEncryptedByPasswordAndLoad()
{
    // Il percorso della directory dei documenti.
    string dataDir = "Your Document Directory";
    string fileName = Path.Combine(dataDir, "Aspose.one");

    Document document;
    if (Document.IsEncrypted(fileName, "VerySecretPassword", out document))
    {
        if (document != null)
        {
            Console.WriteLine("The document is decrypted. It is loaded and ready to be processed.");
        }
        else
        {
            Console.WriteLine("The document is encrypted. Invalid password was provided.");
        }
    }
    else
    {
        Console.WriteLine("The document is NOT encrypted. It is loaded and ready to be processed.");
    }
}
```

### Passaggio 4: gestire il formato OneNote 2007 non supportato:
   - Tentativo di caricare un documento OneNote nel formato 2007.
   -  Se il formato non è supportato, prendi il file`UnsupportedFileFormatException` e gestirlo in modo appropriato, informando l'utente sul formato non supportato.

```csharp
public static void Document_OneNote2007_Is_NotSupported()
{
    // Il percorso della directory dei documenti.
    string dataDir = "Your Document Directory";
    string fileName = Path.Combine(dataDir, "OneNote2007.one");

    try
    {
        new Document(fileName);
    }
    catch (UnsupportedFileFormatException e)
    {
        if (e.FileFormat == FileFormat.OneNote2007)
        {
            Console.WriteLine("It looks like the provided file is in OneNote 2007 format that is not supported.");
        }
        else
            throw;
    }
}
```

## Conclusione

In questo tutorial, abbiamo esplorato come caricare documenti OneNote in Aspose.Note per .NET utilizzando vari metodi. Seguendo queste istruzioni dettagliate, puoi integrare perfettamente le funzionalità di elaborazione dei documenti di OneNote nelle tue applicazioni .NET.

## Domande frequenti

### Q1: Aspose.Note per .NET è compatibile con tutte le versioni di Microsoft OneNote?

A1: Aspose.Note per .NET supporta varie versioni di OneNote. Tuttavia, potrebbero esserci limitazioni con formati precedenti come OneNote 2007.

### Q2: posso crittografare e decrittografare i documenti OneNote a livello di codice con Aspose.Note per .NET?

A2: Sì, puoi verificare se un documento è crittografato e decrittografarlo utilizzando Aspose.Note per .NET.

### Q3: Dove posso trovare ulteriori risorse e supporto per Aspose.Note per .NET?

 A3: Puoi visitare il[Aspose.Note per la documentazione .NET](https://reference.aspose.com/note/net/) per guide ed esempi completi. Inoltre, puoi chiedere assistenza a[Aspose.Note per il forum .NET](https://forum.aspose.com/c/note/28).

### Q4: È disponibile una prova gratuita per Aspose.Note per .NET?

 R4: Sì, puoi scaricare una versione di prova gratuita da[Sito web Aspose](https://releases.aspose.com/).

### Q5: Come posso ottenere una licenza temporanea per Aspose.Note per .NET?

 R5: È possibile richiedere una licenza temporanea da[Aspose la pagina di acquisto](https://purchase.aspose.com/temporary-license/).