---
title: Aggiungi nodo tabella con tag in Aspose.Note
linktitle: Aggiungi nodo tabella con tag in Aspose.Note
second_title: Aspose.Note API .NET
description: Scopri come aggiungere tabelle con tag in Aspose.Note per .NET. Migliora le tue capacità di manipolazione dei documenti a livello di codice.
weight: 11
url: /it/net/tag-management/add-table-node-tag/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aggiungi nodo tabella con tag in Aspose.Note

## introduzione

In questo tutorial ti guideremo attraverso il processo di aggiunta di un nodo di tabella con un tag utilizzando Aspose.Note per .NET. Seguire i passaggi seguenti per raggiungere questo obiettivo.

## Importa spazi dei nomi

Prima di iniziare, assicurati di importare gli spazi dei nomi necessari per lavorare con Aspose.Nota:

```csharp
using System.Drawing;
using System.IO;
using Aspose.Note;
using System;
using System.Collections.Generic;
using Aspose.Note.Examples.CSharp.Tables;
```

## Prerequisiti

Assicurati di avere i seguenti prerequisiti impostati prima di procedere:

1.  Installazione: scaricare e installare la libreria Aspose.Note per .NET da[Qui](https://releases.aspose.com/note/net/).
2.  Licenza: acquisire una licenza o utilizzare a[licenza temporanea](https://purchase.aspose.com/temporary-license/) per utilizzare la biblioteca.
3. Ambiente di sviluppo: disporre di un ambiente di sviluppo compatibile, come Visual Studio.

## Passaggio 1: inizializzare gli oggetti documento e pagina

 Inizia creando un'istanza di`Document` class e inizializzare a`Page` oggetto:

```csharp
Document doc = new Document();
Aspose.Note.Page page = new Aspose.Note.Page(doc);
```

## Passaggio 2: crea oggetti tabella, riga e cella

 Inizializza il`Table`, `TableRow` , E`TableCell` oggetti:

```csharp
TableRow row = new TableRow(doc);
TableCell cell = new TableCell(doc);
```

## Passaggio 3: inserisci il contenuto nella cella

 Aggiungi contenuto alla cella utilizzando il comando`AppendChildLast` metodo:

```csharp
cell.AppendChildLast(InsertTable.GetOutlineElementWithText(doc, "Single cell."));
```

## Passaggio 4: inizializza il nodo tabella

 Inizializza il`Table` oggetto con proprietà specificate:

```csharp
Table table = new Table(doc)
{
    IsBordersVisible = true,
    Columns = { new TableColumn { Width = 70 } }
};
```

## Passaggio 5: aggiungi riga alla tabella

Aggiungi il nodo riga alla tabella:

```csharp
table.AppendChildLast(row);
```

## Passaggio 6: aggiungi tag al nodo tabella

Includi un tag per il nodo della tabella:

```csharp
table.Tags.Add(NoteTag.CreateQuestionMark());
```

## Passaggio 7: aggiungi il nodo della tabella all'elemento del contorno

 Creare un`Outline` E`OutlineElement` per aggiungere il nodo della tabella:

```csharp
Outline outline = new Outline(doc);
OutlineElement outlineElem = new OutlineElement(doc);
outlineElem.AppendChildLast(table);
outline.AppendChildLast(outlineElem);
page.AppendChildLast(outline);
doc.AppendChildLast(page);
```

## Passaggio 8: salva il documento

Salva il documento OneNote:

```csharp
string dataDir = "Your Document Directory";
dataDir = dataDir + "AddTableNodeWithTag_out.one";
doc.Save(dataDir);
Console.WriteLine("\nTable node with tag added successfully.\nFile saved at " + dataDir);
```

Dopo aver seguito questi passaggi, dovresti aver aggiunto correttamente un nodo di tabella con un tag utilizzando Aspose.Note per .NET.

## Conclusione

In questo tutorial, abbiamo trattato il processo di aggiunta di un nodo di tabella con un tag in Aspose.Note per .NET. Seguendo questi passaggi è possibile manipolare in modo efficiente i documenti OneNote a livello di codice, migliorando le capacità di gestione dei documenti.

## Domande frequenti

### Q1: Aspose.Note è compatibile con tutte le versioni di .NET?

A1: Aspose.Note per .NET supporta .NET Framework versioni 2.0 e successive, inclusi .NET Core e .NET Standard.

### Q2: Posso provare Aspose.Note prima di acquistare una licenza?

 A2: Sì, puoi ottenere una prova gratuita di Aspose.Note da[Qui](https://releases.aspose.com/).

### Q3: Come posso acquisire una licenza temporanea per Aspose.Note?

 A3: Puoi ottenere una licenza temporanea da[questo link](https://purchase.aspose.com/temporary-license/), che ha validità 30 giorni.

### Q4: Aspose.Note supporta la crittografia dei documenti?

A4: Sì, Aspose.Note fornisce supporto per la crittografia dei documenti OneNote per garantire la sicurezza dei dati.

### Q5: il supporto tecnico è disponibile per gli utenti Aspose.Note?

 R5: Sì, il supporto tecnico viene fornito tramite i forum Aspose[Qui](https://forum.aspose.com/c/note/28), dove puoi chiedere assistenza agli esperti.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
