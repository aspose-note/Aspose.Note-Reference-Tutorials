---
title: Apri e chiudi progetti con tag in Aspose.Note
linktitle: Apri e chiudi progetti con tag in Aspose.Note
second_title: Aspose.Note API .NET
description: Scopri come manipolare i file Microsoft OneNote a livello di codice utilizzando Aspose.Note per .NET. Apri e chiudi progetti con tag in modo efficiente.
type: docs
weight: 15
url: /it/net/tag-management/open-close-projects-tags/
---
## introduzione

In questo tutorial impareremo come utilizzare Aspose.Note per .NET per aprire e chiudere progetti con tag. Aspose.Note è una potente API che consente agli sviluppatori di lavorare con i file Microsoft OneNote a livello di codice, abilitando attività come la manipolazione di testo, immagini e tag all'interno dei documenti.

## Prerequisiti

Prima di iniziare, assicurati di aver configurato i seguenti prerequisiti:

## Importa spazi dei nomi

```csharp
using System.IO;
using System.Linq;
```

Ora suddividiamo ciascun esempio in più passaggi:

## Passaggio 1: caricare il documento

Innanzitutto, dobbiamo caricare il documento in Aspose.Note.

```csharp
string dataDir = "Your Document Directory";
var oneFile = new Document(Path.Combine(dataDir, "ProjectNotes.one"));
```

## Passaggio 2: chiudere gli elementi del progetto C

Ora chiudiamo tutte le caselle di controllo relative al "Progetto C".

```csharp
foreach (var node in oneFile.GetChildNodes<ITaggable>())
{
    foreach (var checkBox in node.Tags.OfType<CheckBox>())
    {
        if (checkBox.Label.Contains("Project C") && !checkBox.Checked)
        {
            checkBox.SetCompleted();
        }
    }
}
```

## Passaggio 3: salvare le note del progetto C chiuso

Salva il documento modificato con gli elementi "Progetto C" chiusi.

```csharp
oneFile.Save("Path to save the closed Project C notes");
```

## Passaggio 4: aprire gli elementi del progetto C

Successivamente, apriamo tutte le caselle di controllo relative al "Progetto C".

```csharp
var oneFile = new Document("Path to the closed Project C notes");

foreach (var node in oneFile.GetChildNodes<ITaggable>())
{
    foreach (var checkBox in node.Tags.OfType<CheckBox>())
    {
        if (checkBox.Label.Contains("Project C") && checkBox.Checked)
        {
            checkBox.SetOpen();
        }
    }
}
```

## Passaggio 5: salvare le note di Open Project C

Salva il documento modificato con gli elementi "Progetto C" aperti.

```csharp
oneFile.Save(Path.Combine(dataDir, "ProjectNoteWithOpenProjectC.one"));
```

Ora hai imparato come aprire e chiudere progetti con tag in Aspose.Note utilizzando .NET.

## Conclusione

Aspose.Note per .NET fornisce un modo conveniente per manipolare i documenti OneNote a livello di codice. Seguendo questo tutorial, puoi gestire in modo efficiente i tuoi progetti aprendo e chiudendo gli elementi utilizzando i tag.

## Domande frequenti

### Q1: Aspose.Note è compatibile con tutte le versioni di OneNote?

A1: Aspose.Note supporta Microsoft OneNote 2010 e versioni successive.

### Q2: Posso utilizzare Aspose.Note per progetti commerciali?

 A2: Sì, puoi utilizzare Aspose.Note sia per progetti personali che commerciali. Visita[Qui](https://purchase.aspose.com/buy) per acquistare una licenza.

### Q3: Aspose.Note offre una prova gratuita?

 R3: Sì, puoi ottenere una prova gratuita[Qui](https://releases.aspose.com/).

### Q4: Dove posso trovare la documentazione per Aspose.Note?

 A4: È possibile trovare la documentazione[Qui](https://reference.aspose.com/note/net/).

### Q5: Dove posso ottenere supporto per Aspose.Note?

 R5: Per supporto, è possibile visitare Aspose.Note[Forum](https://forum.aspose.com/c/note/28).