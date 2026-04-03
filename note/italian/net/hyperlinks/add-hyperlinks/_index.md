---
date: 2026-04-03
description: Scopri come aggiungere collegamenti ipertestuali nei documenti Aspose.Note
  usando Aspose.Note per .NET, personalizzare l’aspetto dei collegamenti ipertestuali
  e inserire più collegamenti ipertestuali per file OneNote più ricchi.
keywords:
- how to add hyperlink
- insert multiple hyperlinks
- add hyperlink to onenote
- customize hyperlink appearance
- generate one file hyperlink
linktitle: Come aggiungere un collegamento ipertestuale nei documenti Aspose.Note
second_title: Aspose.Note .NET API
title: Come aggiungere un collegamento ipertestuale nei documenti Aspose.Note
url: /it/net/hyperlinks/add-hyperlinks/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Come aggiungere un collegamento ipertestuale nei documenti Aspose.Note

## Introduzione

In questo tutorial scoprirai **come aggiungere un collegamento ipertestuale** al testo all'interno dei documenti Aspose.Note con l'API .NET. Aggiungere un collegamento ipertestuale trasforma le note statiche in contenuti interattivi e cliccabili—perfetti per collegare a risorse web, sezioni interne o file esterni. Ti guideremo passo passo, ti mostreremo come **personalizzare l'aspetto del collegamento ipertestuale** e spiegheremo come **inserire più collegamenti ipertestuali** quando hai bisogno di pagine OneNote più ricche.

## Risposte rapide
- **Qual è la classe principale per creare un file OneNote?** `Document` di Aspose.Note.
- **Quale proprietà fa sì che il testo si comporti da collegamento ipertestuale?** `IsHyperlink = true` su `TextStyle`.
- **Posso collegarmi a siti web esterni?** Sì, imposta `HyperlinkAddress` a un URL come `https://www.google.com`.
- **È necessaria una licenza per l'uso in produzione?** È richiesta una licenza valida di Aspose.Note per build non‑di valutazione.
- **Quali versioni di .NET sono supportate?** .NET Framework 4.6+, .NET Core 3.1+, .NET 5/6+.

## Che cosa significa “come aggiungere un collegamento ipertestuale” in Aspose.Note?
Aggiungere un collegamento ipertestuale significa associare un URL a un frammento di testo in modo che, quando un utente lo clicca all'interno di OneNote, la risorsa collegata si apra in un browser o in un'altra applicazione. Aspose.Note espone il flag `TextStyle.IsHyperlink` e la proprietà `HyperlinkAddress` per rendere possibile ciò programmaticamente.

## Perché aggiungere collegamenti ipertestuali ai documenti OneNote?
- **Navigazione migliorata:** Salta direttamente a pagine web o sezioni correlate.
- **Documentazione migliorata:** Fornisci riferimenti, tutorial o file sorgente senza lasciare la nota.
- **Aspetto professionale:** Colori e stili personalizzabili permettono ai collegamenti ipertestuali di integrarsi con il design del documento.

## Prerequisiti

1. Conoscenza di base di C# e Visual Studio.
2. Libreria Aspose.Note per .NET installata – scaricala da [qui](https://releases.aspose.com/note/net/).
3. Comprensione della struttura dei documenti Aspose.Note (pagine, outline, rich text).

## Importa gli spazi dei nomi

Per prima cosa, importa gli spazi dei nomi che ti danno accesso alle classi core di Aspose.Note e ai tipi .NET di base.

```csharp
using System;
using System.Drawing;
```

## Guida passo‑passo

### Passo 1: Crea un nuovo oggetto Document

Istanzia un `Document` che conterrà tutte le tue pagine e il contenuto.

```csharp
Document doc = new Document();
```

### Passo 2: Definisci gli stili di testo (incluso lo stile del collegamento ipertestuale)

Crea due oggetti `TextStyle` – uno per il testo normale e uno per il collegamento ipertestuale.  
Qui personalizziamo anche **l'aspetto del collegamento ipertestuale** impostando il colore del carattere.

```csharp
TextStyle textStyleRed = new TextStyle
{
    FontColor = Color.Red,
    FontName = "Arial",
    FontSize = 10,
};

TextStyle textStyleHyperlink = new TextStyle
{
    IsHyperlink = true,
    HyperlinkAddress = "www.google.com"
};
```

> **Consiglio professionale:** Per inserire **più collegamenti ipertestuali**, definisci ulteriori oggetti `TextStyle` con valori `HyperlinkAddress` diversi e riutilizzali nei segmenti `RichText` successivi.

### Passo 3: Crea oggetti RichText

Costruisci il paragrafo che mescola testo normale e il collegamento ipertestuale. Il metodo `Append` ti consente di concatenare frammenti con stile.

```csharp
RichText text = new RichText() { ParagraphStyle = ParagraphStyle.Default }
                    .Append("This is ", textStyleRed)
                    .Append("hyperlink", textStyleHyperlink)
                    .Append(". This text is not a hyperlink.", TextStyle.Default);
```

### Passo 4: Crea Outline e elemento Outline

Gli Outline fungono da contenitori per gli elementi visivi su una pagina. Imposta dimensioni e posizione secondo necessità.

```csharp
Outline outline = new Outline()
{
    MaxWidth = 200,
    MaxHeight = 200,
    VerticalOffset = 100,
    HorizontalOffset = 100
};

OutlineElement outlineElem = new OutlineElement();
outlineElem.AppendChildLast(text);
```

### Passo 5: Aggiungi elementi a una pagina

Ogni file OneNote è composto da pagine. Creiamo un `Title` e una `Page`, quindi colleghiamo l'outline.

```csharp
Title title = new Title() { TitleText = titleText };
Page page = new Note.Page() { Title = title };

page.AppendChildLast(outline);
doc.AppendChildLast(page);
```

### Passo 6: Salva il documento

Scegli una cartella, compila il nome completo del file e chiama `Save`. Il file di output sarà un file OneNote `.one` valido contenente il tuo collegamento ipertestuale.

```csharp
string dataDir = "Your Document Directory";
string outputFilePath = Path.Combine(dataDir, "AddHyperlink_out.one");
doc.Save(outputFilePath);
```

## Problemi comuni e soluzioni

| Problema | Soluzione |
|----------|-----------|
| Il collegamento ipertestuale non si apre | Assicurati che `HyperlinkAddress` includa il protocollo (`http://` o `https://`). |
| Il colore del testo non viene applicato | Imposta `FontColor` sul `TextStyle` usato per il collegamento ipertestuale. |
| Necessità di più collegamenti in una pagina | Crea più oggetti `TextStyle`, ognuno con il proprio `HyperlinkAddress`, e aggiungili allo stesso o a diversi oggetti `RichText`. |
| Il documento non si carica in OneNote | Verifica di utilizzare una versione di OneNote supportata (2010+). |

## Domande frequenti

**D: Posso aggiungere più collegamenti ipertestuali nello stesso documento usando Aspose.Note?**  
R: Sì, basta creare ulteriori istanze `TextStyle` con valori `HyperlinkAddress` diversi e aggiungerle ai tuoi oggetti `RichText`.

**D: Come posso personalizzare l'aspetto dei collegamenti ipertestuali?**  
R: Usa proprietà come `FontColor`, `FontName` e `FontSize` sul `TextStyle` che ha `IsHyperlink = true`. Questo ti permette di abbinare lo stile al branding del tuo documento.

**D: Aspose.Note supporta i collegamenti ipertestuali a siti web esterni?**  
R: Assolutamente. Imposta `HyperlinkAddress` su qualsiasi URL valido (inclusi `http://` o `https://`) per collegare fuori dal file OneNote.

**D: È possibile generare un unico file OneNote che contiene molti collegamenti ipertestuali?**  
R: Sì. Aggiungendo ripetutamente segmenti `RichText` con stili e diversi indirizzi di collegamento, puoi **generare una collezione di collegamenti ipertestuali in un unico file**.

**D: Aspose.Note è compatibile con le versioni più recenti di OneNote?**  
R: La libreria funziona con OneNote 2010 e successive, inclusa la versione UWP di Windows 10.

---

**Ultimo aggiornamento:** 2026-04-03  
**Testato con:** Aspose.Note for .NET 24.11  
**Autore:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}