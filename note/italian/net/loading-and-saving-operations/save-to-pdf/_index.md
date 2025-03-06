---
title: Salva in PDF in Aspose.Note
linktitle: Salva in PDF in Aspose.Note
second_title: Aspose.Note API .NET
description: Scopri come salvare i documenti Microsoft OneNote in formato PDF utilizzando Aspose.Note per .NET. Tutorial passo passo con esempi di codice per layout di pagina Letter e A4.
weight: 26
url: /it/net/loading-and-saving-operations/save-to-pdf/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Salva in PDF in Aspose.Note

## introduzione

In questo tutorial esploreremo come salvare documenti in formato PDF utilizzando Aspose.Note per .NET. Aspose.Note è una potente libreria che consente agli sviluppatori di lavorare con i file Microsoft OneNote a livello di codice. Tratteremo i prerequisiti, importeremo gli spazi dei nomi e forniremo guide dettagliate per salvare documenti in PDF in vari layout di pagina.

## Prerequisiti

Prima di iniziare, assicurati di avere quanto segue:

- Visual Studio installato nel sistema.
-  Aspose.Note per la libreria .NET scaricata e installata. Puoi scaricarlo da[Qui](https://releases.aspose.com/note/net/).
- Conoscenza base del linguaggio di programmazione C#.

## Importa spazi dei nomi

Innanzitutto, importiamo gli spazi dei nomi necessari nel nostro codice C#:

```csharp
using System;
using System.IO;

using Aspose.Note.Saving;
```

Ora che abbiamo coperto i prerequisiti e importato gli spazi dei nomi, procediamo con il salvataggio dei documenti in PDF in diversi layout di pagina.

## Passaggio 1: salva in PDF utilizzando le impostazioni della pagina Letter


```csharp
public static void SaveToPdfUsingLetterPageSettings()
{
    // Il percorso della directory dei documenti.
    string dataDir = "Your Document Directory";

    // Caricare il documento in Aspose.Note.
    Document oneFile = new Document(dataDir + "OneNote.one");

    var dst = Path.Combine(dataDir, "SaveToPdfUsingLetterPageSettings.pdf");

    // Salva il documento.
    oneFile.Save(dst, new PdfSaveOptions() { PageSettings = PageSettings.Letter });

    Console.WriteLine("\nOneNote document saved successfully.\nFile saved at " + dst);
}
```

### Spiegazione:

- Carichiamo il documento OneNote in Aspose.Note.
- Definire il percorso di destinazione per il file PDF salvato.
-  Salvare il documento in PDF utilizzando`PdfSaveOptions` con`PageSettings` impostato`Letter`.

## Passaggio 2: salva in PDF utilizzando le impostazioni della pagina A4 senza limite di altezza

```csharp
public static void SaveToPdfUsingA4PageSettingsWithoutHeightLimit()
{
    // Il percorso della directory dei documenti.
    string dataDir = "Your Document Directory";

    // Caricare il documento in Aspose.Note.
    Document oneFile = new Document(dataDir + "OneNote.one");

    var dst = Path.Combine(dataDir, "SaveToPdfUsingA4PageSettingsWithoutHeightLimit.pdf");

    // Salva il documento.
    oneFile.Save(dst, new PdfSaveOptions() { PageSettings = PageSettings.A4NoHeightLimit });

    Console.WriteLine("\nOneNote document saved successfully.\nFile saved at " + dst);
}
```

### Spiegazione:

- Similmente al passaggio precedente, carichiamo il documento OneNote in Aspose.Note.
- Definire il percorso di destinazione per il file PDF salvato.
-  Salvare il documento in PDF utilizzando`PdfSaveOptions` con`PageSettings` impostato`A4NoHeightLimit`.

## Conclusione

In questo tutorial, abbiamo imparato come salvare documenti in formato PDF utilizzando Aspose.Note per .NET. Abbiamo trattato due diversi layout di pagina: Lettera e A4 senza limiti di altezza. Con Aspose.Note, gli sviluppatori possono facilmente manipolare i file OneNote a livello di codice, fornendo flessibilità ed efficienza nelle attività di gestione dei documenti.

## Domande frequenti

### Q1: Aspose.Note può gestire file OneNote complessi?

A1: Sì, Aspose.Note supporta varie caratteristiche e funzionalità per gestire in modo efficace file OneNote complessi.

### Q2: Aspose.Note è adatto a progetti commerciali?

 A2: Assolutamente, Aspose.Note può essere utilizzato facilmente in progetti commerciali. È possibile acquistare una licenza[Qui](https://purchase.aspose.com/buy).

### Q3: Aspose.Note offre una prova gratuita?

 A3: Sì, puoi esplorare Aspose.Note con una prova gratuita disponibile[Qui](https://releases.aspose.com/).

### Q4: Dove posso trovare la documentazione per Aspose.Note?

 R4: È possibile trovare documentazione dettagliata[Qui](https://reference.aspose.com/note/net/).

### Q5: Hai bisogno di ulteriore assistenza?

 A5: Sentiti libero di porre domande o cercare supporto sul forum Aspose.Note[Qui](https://forum.aspose.com/c/note/28).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
