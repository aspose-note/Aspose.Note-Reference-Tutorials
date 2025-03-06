---
title: Genera documento dal modello in Aspose.Note
linktitle: Genera documento dal modello in Aspose.Note
second_title: Aspose.Note API .NET
description: Genera documenti dinamici senza sforzo con Aspose.Note per .NET. Segui la nostra guida passo passo per la creazione di documenti personalizzati e basati sui dati.
weight: 18
url: /it/net/text-manipulation/generate-document-from-template/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Genera documento dal modello in Aspose.Note

## introduzione
Nel panorama in continua evoluzione della creazione di documenti, Aspose.Note per .NET si distingue come un potente strumento per generare documenti dinamici senza sforzo. Che tu abbia a che fare con report, fatture o documenti personalizzati, questo tutorial ti guiderà attraverso il processo di generazione di un documento da un modello utilizzando Aspose.Note per .NET.
## Prerequisiti
Prima di immergerti nella guida passo passo, assicurati di disporre dei seguenti prerequisiti:
1.  Aspose.Note per la libreria .NET: scaricare e installare la libreria da[Aspose.Note per la documentazione .NET](https://reference.aspose.com/note/net/).
2. Modello di documento: prepara un documento modello nel formato OneNote (con estensione .one). Questo servirà come base per il tuo documento generato dinamicamente.
## Importa spazi dei nomi
Assicurati di includere gli spazi dei nomi necessari nel tuo progetto:
```csharp
    using System;
    using System.Collections.Generic;
    using System.IO;
```
Ora analizziamo ogni passaggio della guida.
## Passaggio 1: definire la directory dei documenti
```csharp
string dataDir = "Your Document Directory";
```
Sostituisci "La tua directory dei documenti" con il percorso in cui desideri salvare il documento generato.
## Passaggio 2: crea un dizionario con valori sostitutivi
```csharp
var templateData = new Dictionary<string, string>
{
    { "Company", "Atlas Shrugged Ltd" },
    { "CandidateName", "John Galt" },
    { "JobTitle", "Chief Entrepreneur Officer" },
    { "Department", "Sales" },
    { "Salary", "123456 USD" },
    { "Vacation", "30" },
    { "StartDate", "29 Feb 2024" },
    { "YourName", "Ayn Rand" }
};
```
Definisci un dizionario in cui le chiavi sono segnaposto nel tuo modello e i valori sono i dati con cui desideri sostituirli.

## Passaggio 3: caricare il documento modello
```csharp
var templateDocument = new Document(Path.Combine(dataDir, "JobOffer.one"));
```
Carica il tuo documento modello OneNote in Aspose.Note.

## Passaggio 4: sostituisci le parole modello con dati dinamici
```csharp
foreach (var paragraph in templateDocument.GetChildNodes<RichText>())
{
    foreach (var replacement in templateData)
    {
        paragraph.Replace($"${{{replacement.Key}}}", replacement.Value);
    }
}
```
Scorri ogni paragrafo del modello, sostituendo i segnaposto con dati dinamici.

## Passaggio 5: salva il documento generato
```csharp
templateDocument.Save(Path.Combine(dataDir, "JobOffer_out.one"));
```
Salva il documento generato dinamicamente nella directory specificata.

## Conclusione
Congratulazioni! Hai generato con successo un documento dinamico utilizzando Aspose.Note per .NET. Questo processo apre un mondo di possibilità per creare documenti personalizzati e basati sui dati senza soluzione di continuità.

## Domande frequenti
### Posso utilizzare Aspose.Note per .NET con altri formati di documenti?
Sì, Aspose.Note per .NET si occupa principalmente di documenti OneNote, ma Aspose fornisce varie librerie per diversi formati.
### È disponibile una prova gratuita per Aspose.Note per .NET?
Sì, puoi esplorare le funzionalità di Aspose.Note per .NET con una prova gratuita. Visita[Qui](https://releases.aspose.com/) per maggiori informazioni.
### Come posso ottenere supporto per Aspose.Note per .NET?
 Visitare il[Aspose.Note per il forum .NET](https://forum.aspose.com/c/note/28) per ottenere assistenza dalla comunità e dagli esperti.
### Sono disponibili licenze temporanee per Aspose.Note per .NET?
 Sì, puoi ottenere una licenza temporanea[Qui](https://purchase.aspose.com/temporary-license/) a scopo di test e valutazione.
### Dove posso trovare la documentazione completa per Aspose.Note per .NET?
 Fare riferimento al[documentazione](https://reference.aspose.com/note/net/) per informazioni approfondite sull'utilizzo di Aspose.Note per .NET.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
