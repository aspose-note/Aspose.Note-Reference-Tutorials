---
date: 2026-04-03
description: Scopri come impostare un'icona personalizzata e allegare file in Aspose.Note
  per .NET, inclusa la possibilità di salvare file OneNote e utilizzare immagini come
  icone.
keywords:
- set custom icon
- attach multiple files
- use image as icon
- save onenote file
- embed text file
linktitle: Allega file e imposta icona in Aspose.Note
second_title: Aspose.Note .NET API
title: Imposta icona personalizzata e allega file in Aspose.Note
url: /it/net/attachments/attach-file-set-icon/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Imposta icona personalizzata e allega file in Aspose.Note

## Introduzione

Se hai bisogno di **impostare un'icona personalizzata** per un allegato in una pagina OneNote, Aspose.Note per .NET lo rende semplice. Allegando un file e assegnando un'immagine come icona, puoi creare note più ricche e informative che hanno esattamente l'aspetto desiderato. In questo tutorial percorreremo l'intero processo—partendo da un documento nuovo, aggiungendo un allegato, applicando un'icona JPEG personalizzata e infine salvando il file OneNote.

## Risposte rapide
- **Che cosa significa “impostare icona personalizzata”?** Consente di sostituire la miniatura predefinita dell'allegato con un'immagine fornita.  
- **Posso allegare più file?** Sì, ripeti i passaggi di allegato per ogni file.  
- **Quali formati immagine sono supportati per le icone?** Qualsiasi formato compatibile con .NET, come JPEG, PNG, BMP o GIF.  
- **È necessaria una licenza?** È richiesta una licenza valida di Aspose.Note per l'uso in produzione; una versione di prova gratuita è sufficiente per la valutazione.  
- **Come salvo il file OneNote?** Usa `Document.Save()` e specifica un percorso di file *.one*.

## Cos'è “imposta icona personalizzata” in Aspose.Note?
Impostare un'icona personalizzata significa assegnare un'immagine specifica (ad esempio un JPEG) per rappresentare un file allegato all'interno di una pagina OneNote. Questo migliora gli indizi visivi per gli utenti e può essere usato per visualizzare loghi del tipo di file o immagini di branding.

## Perché impostare un'icona personalizzata per gli allegati?
- **Migliore contesto visivo:** Gli utenti riconoscono immediatamente il tipo o lo scopo del file allegato.  
- **Coerenza del brand:** Usa il logo della tua azienda come icona per tutti i documenti correlati.  
- **Esperienza utente migliorata:** Rende le note più curate e professionali, soprattutto nei notebook condivisi.

## Prerequisiti

- Conoscenza di base della programmazione C#.
- Libreria Aspose.Note per .NET installata.
- Visual Studio (o qualsiasi IDE compatibile con .NET) pronto per lo sviluppo.

## Importa namespace

Innanzitutto, importa i namespace necessari in modo da poter lavorare con file, immagini e oggetti OneNote.

```csharp
using System.IO;
using Aspose.Note;
using System;
using System.Collections.Generic;
using System.Drawing.Imaging;
```

## Guida passo‑passo per allegare un file e impostare la sua icona

### Passo 1: Crea un oggetto Document
Una nuova istanza di `Document` rappresenta il file OneNote che costruirai.

```csharp
Document doc = new Document();
```

### Passo 2: Inizializza un oggetto Page
Ogni file OneNote contiene una o più pagine. Qui creiamo la prima pagina.

```csharp
Aspose.Note.Page page = new Aspose.Note.Page(doc);
```

### Passo 3: Inizializza un oggetto Outline
Gli Outline fungono da contenitori per i blocchi di contenuto su una pagina.

```csharp
Outline outline = new Outline(doc);
```

### Passo 4: Inizializza un oggetto OutlineElement
Questo elemento conterrà il file allegato e la sua icona personalizzata.

```csharp
OutlineElement outlineElem = new OutlineElement(doc);
```

### Passo 5: Leggi l'immagine dell'icona e inizializza l'oggetto AttachedFile
Apriamo lo stream dell'immagine (l'icona personalizzata) e puntiamo al file che desideriamo incorporare.

```csharp
string dataDir = "Your Document Directory";
using (var stream = File.OpenRead(dataDir + "icon.jpg"))
{
    AttachedFile attachedFile = new AttachedFile(doc, dataDir + "attachment.txt", stream, ImageFormat.Jpeg);
}
```

> **Suggerimento:** Sostituisci `ImageFormat.Jpeg` con `ImageFormat.Png` se preferisci un'icona PNG.

### Passo 6: Aggiungi il file allegato all'OutlineElement
Ora il file (con la sua icona) diventa un figlio dell'elemento outline.

```csharp
outlineElem.AppendChildLast(attachedFile);
```

### Passo 7: Aggiungi l'OutlineElement all'Outline
Questo annida l'elemento all'interno del contenitore outline.

```csharp
outline.AppendChildLast(outlineElem);
```

### Passo 8: Aggiungi l'Outline alla Page
Allega l'intera gerarchia outline alla pagina.

```csharp
page.AppendChildLast(outline);
```

### Passo 9: Aggiungi la Page al Document
Aggiungi la pagina completata alla struttura del documento.

```csharp
doc.AppendChildLast(page);
```

### Passo 10: Salva il documento OneNote
Infine, scrivi il documento su disco come file *.one*.

```csharp
dataDir = dataDir + "AttachFileAndSetIcon_out.one";
doc.Save(dataDir);
```

## Casi d'uso comuni
- **Incorporare contratti:** Allega un PDF e utilizza un'icona con il logo del contratto.  
- **Condivisione di snippet di codice:** Allega un file `.txt` con un'icona “code” personalizzata.  
- **Documentazione di progetto:** Allega file di design e imposta una miniatura che corrisponde al tipo di file.

## Problemi comuni e soluzioni
| Problema | Soluzione |
|----------|-----------|
| **Icona non visualizzata** | Verifica che il formato dell'immagine corrisponda al `ImageFormat` fornito (ad esempio JPEG vs PNG). |
| **Errori di percorso file** | Usa `Path.Combine(dataDir, \"file.ext\")` per evitare problemi di slash mancanti. |
| **Allegati di grandi dimensioni causano rallentamenti** | Comprimi il file in anticipo o dividilo in più allegati più piccoli. |

## Domande frequenti

**D: Posso allegare più file a una singola nota usando Aspose.Note per .NET?**  
R: Sì. Basta ripetere il blocco “Leggi l'immagine dell'icona e inizializza l'oggetto AttachedFile” per ogni file e aggiungere ogni `AttachedFile` allo stesso `OutlineElement` oppure creare elementi separati.

**D: È possibile impostare icone personalizzate per gli allegati dei file?**  
R: Assolutamente. Il costruttore `AttachedFile` consente di passare uno stream di immagine e specificare il formato dell'immagine, offrendoti il pieno controllo sull'icona.

**D: Aspose.Note supporta altri formati immagine per impostare le icone?**  
R: Sì. Oltre a JPEG, puoi usare PNG, BMP, GIF o qualsiasi formato supportato da `System.Drawing.Imaging.ImageFormat`.

**D: Posso allegare file da URL esterni?**  
R: Sebbene Aspose.Note lavori con stream locali, puoi scaricare un file tramite `HttpClient`, memorizzarlo in un `MemoryStream` e poi passare quello stream a `AttachedFile`.

**D: Esiste un limite di dimensione per gli allegati dei file?**  
R: Aspose.Note di per sé non impone un limite rigido, ma file molto grandi possono influire sull'uso della memoria e sulle prestazioni. Considera di comprimere gli allegati di grandi dimensioni.

---

**Ultimo aggiornamento:** 2026-04-03  
**Testato con:** Aspose.Note 24.11 per .NET  
**Autore:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}