---
title: Comporre tabelle con Aspose.Note
linktitle: Comporre tabelle con Aspose.Note
second_title: Aspose.Note API .NET
description: Scopri come comporre tabelle strutturate con contenuto RTF utilizzando Aspose.Note per .NET. Migliora l'organizzazione e la leggibilità dei documenti senza sforzo.
weight: 11
url: /it/net/table-manipulation/compose-tables/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Comporre tabelle con Aspose.Note

## introduzione

Le tabelle sono componenti fondamentali dei documenti e consentono la presentazione strutturata delle informazioni. Aspose.Note per .NET fornisce strumenti robusti per comporre tabelle senza sforzo. In questo tutorial ti guideremo attraverso il processo di creazione di tabelle con contenuto RTF utilizzando Aspose.Note.

## Prerequisiti

Prima di immergerti nella composizione della tabella con Aspose.Note per .NET, assicurati di avere i seguenti prerequisiti:

1. Configurazione dell'ambiente: assicurarsi di disporre di un ambiente di sviluppo adatto configurato con .NET Framework o .NET Core.
2.  Installazione: Scarica e installa Aspose.Note per .NET da[sito web](https://releases.aspose.com/note/net/).
3. Conoscenze di base: familiarizza con i concetti di base della programmazione C# e della manipolazione dei documenti.

## Importa spazi dei nomi

Prima di iniziare a comporre le tabelle, assicurati di importare gli spazi dei nomi necessari:

```csharp
using System;
using System.Drawing;
using System.IO;
using System.Linq;
```

Suddividiamo l'esempio fornito in passaggi gestibili:

## Passaggio 1: impostare la directory dei documenti

Prima di comporre la tabella definire la directory in cui verrà salvato il documento.

```csharp
string dataDir = "Your Document Directory";
```

## Passaggio 2: crea il testo dell'intestazione

Definisci il testo dell'intestazione con stili specifici come dimensione del carattere e grassetto.

```csharp
var headerText = new RichText() { ParagraphStyle = new ParagraphStyle() { FontSize = 18, IsBold = true }, Alignment = HorizontalAlignment.Center }
					.Append("Super contest for suppliers.");
```

## Passaggio 3: crea pagina e struttura

Inizializzare una pagina e una struttura per strutturare il contenuto.

```csharp
var page = new Page();
var outline = page.AppendChildLast(new Outline() { HorizontalOffset = 50 });
outline.AppendChildLast(new OutlineElement()).AppendChildLast(headerText);
```

## Passaggio 4: aggiungi testo di riepilogo

Includere un testo di riepilogo prima della tabella.

```csharp
var bodyTextHeader = outline.AppendChildLast(new OutlineElement()).AppendChildLast(new RichText() { ParagraphStyle = ParagraphStyle.Default });
bodyTextHeader.Append("This is the final ranking of proposals got from our suppliers.");
```

## Passaggio 5: crea tabella

Inizializza una tabella per organizzare i dati in righe e colonne.

```csharp
var ranking = outline.AppendChildLast(new OutlineElement()).AppendChildLast(new Table());
```

## Passaggio 6: aggiungi la riga di intestazione

Compila la tabella con una riga di intestazione contenente i titoli delle colonne.

```csharp
var headerRow = ranking.AppendChildFirst(new TableRow());
foreach (var header in new[] { "Supplier", "Contacts", "Score A", "Score B", "Score C", "Final score", "Attached materials", "Comments" })
{
   ranking.Columns.Add(new TableColumn());
   headerRow.AppendChildLast(new TableCell() { BackgroundColor = backGroundColor })
			 .AppendChildLast(new OutlineElement())
			 .AppendChildLast(new RichText() { ParagraphStyle = headerStyle })
			 .Append(header);
}
```

## Passaggio 7: aggiungi righe vuote

Inserisci righe vuote per preparare l'inserimento dei dati.

```csharp
for (int i = 0; i < 5; i++)
{
   backGroundColor = backGroundColor.IsEmpty ? Color.LightGray : Color.Empty;
   var row = ranking.AppendChildLast(new TableRow());
   for (int j = 0; j < ranking.Columns.Count(); j++)
   {
	   row.AppendChildLast(new TableCell() { BackgroundColor = backGroundColor })
		  .AppendChildLast(new OutlineElement())
		  .AppendChildLast(new RichText() { ParagraphStyle = ParagraphStyle.Default });
   }
}
```

## Passaggio 8: aggiungi le informazioni di contatto

Compila la colonna "Contatti" con il contenuto del modello.

```csharp
foreach (var row in ranking.Skip(1))
{
   var contactsCell = row.ElementAt(1);
   contactsCell.AppendChildLast(new OutlineElement())
			   .AppendChildLast(new RichText() { ParagraphStyle = ParagraphStyle.Default })
			   .Append("Web: ").Append("link", new TextStyle() { HyperlinkAddress = "www.link.com", IsHyperlink = true });
   contactsCell.AppendChildLast(new OutlineElement())
			   .AppendChildLast(new RichText() { ParagraphStyle = ParagraphStyle.Default })
			   .Append("E-mail: ").Append("mail", new TextStyle() { HyperlinkAddress = "mailto:hi@link.com", IsHyperlink = true });
}
```

## Passaggio 9: salva il documento

Salvare il documento della tabella composta.

```csharp
var d = new Document();
d.AppendChildLast(page);
d.Save(Path.Combine(dataDir, "ComposeTable_out.one"));
```

## Passaggio 10: conferma

Conferma la corretta composizione del documento.

```csharp
Console.WriteLine("\nThe document is composed successfully.");
```

## Conclusione

In questo tutorial, abbiamo esplorato come comporre tabelle con contenuto RTF utilizzando Aspose.Note per .NET. Seguendo queste istruzioni passo passo, puoi creare in modo efficiente tabelle strutturate all'interno dei tuoi documenti, migliorandone la leggibilità e l'organizzazione.

## Domande frequenti

### Q1: Posso personalizzare lo stile degli elementi della tabella?
   
R1: Sì, puoi personalizzare vari aspetti come la dimensione, il colore e l'allineamento del carattere in base alle tue esigenze.

### Q2: Aspose.Note è compatibile con altre librerie .NET?
   
A2: Aspose.Note si integra perfettamente con altre librerie .NET, offrendo ampia flessibilità nella manipolazione dei documenti.

### Q3: Aspose.Note supporta l'esportazione di tabelle in diversi formati?
   
A3: Assolutamente, Aspose.Note ti consente di esportare tabelle in vari formati tra cui PDF, DOCX e HTML.

### Q4: Posso popolare dinamicamente le tabelle con dati provenienti da origini esterne?
   
R4: Sì, puoi popolare dinamicamente le tabelle recuperando dati da database, API o input dell'utente.

### Q5: il supporto tecnico è disponibile per gli utenti Aspose.Note?
   
R5: Sì, Aspose fornisce supporto tecnico completo attraverso i propri forum e canali di supporto dedicati.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
