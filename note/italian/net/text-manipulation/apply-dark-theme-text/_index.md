---
title: Trasformazione del tema scuro con Aspose.Note per .NET
linktitle: Applica il tema scuro al testo in Aspose.Note
second_title: Aspose.Note API .NET
description: Trasforma i tuoi documenti OneNote con Aspose.Note per .NET! Applica un tema scuro elegante senza sforzo. Scaricalo ora e migliora la tua esperienza nel prendere appunti.
type: docs
weight: 11
url: /it/net/text-manipulation/apply-dark-theme-text/
---
## introduzione
Benvenuti nella nostra guida passo passo sull'applicazione di un tema scuro al testo in Aspose.Note per .NET. Aspose.Note è una potente API .NET che consente agli sviluppatori di lavorare con i file Microsoft OneNote a livello di codice. In questo tutorial esploreremo come conferire ai tuoi documenti OneNote un aspetto elegante e moderno applicando un tema scuro al testo.
## Prerequisiti
Prima di immergerci nel tutorial, assicurati di disporre dei seguenti prerequisiti:
-  Aspose.Note per .NET: assicurati di avere Aspose.Note per .NET installato. In caso contrario, puoi scaricarlo da[Documentazione Aspose.Note](https://reference.aspose.com/note/net/).
- Ambiente di sviluppo: configura il tuo ambiente di sviluppo .NET preferito, come Visual Studio.
- Directory dei documenti: prepara la directory in cui si trova il documento OneNote.
## Importa spazi dei nomi
Nel tuo progetto .NET, importa gli spazi dei nomi necessari per lavorare con Aspose.Note:
```csharp
    using System;
    using System.Drawing;
    using System.IO;
```
## Passaggio 1: caricare il documento OneNote
Carica il tuo documento OneNote in Aspose.Note utilizzando il seguente codice:
```csharp
// Il percorso della directory dei documenti.
string dataDir = "Your Document Directory";
// Caricare il documento in Aspose.Note.
Document doc = new Document(Path.Combine(dataDir, "Aspose.one"));
```
## Passaggio 2: imposta il colore di sfondo
Imposta il colore di sfondo di ciascuna pagina su nero:
```csharp
foreach (var page in doc)
{
    page.BackgroundColor = Color.Black;
}
```
## Passaggio 3: regola il colore del testo
Regola il colore del carattere del testo su bianco per una migliore visibilità:
```csharp
foreach (var node in doc.GetChildNodes<RichText>())
{
    var c = node.ParagraphStyle.FontColor;
    if (c.IsEmpty || Math.Abs(c.R - Color.Black.R) + Math.Abs(c.G - Color.Black.G) + Math.Abs(c.B - Color.Black.B) <= 30)
    {
        node.ParagraphStyle.FontColor = Color.White;
    }
}
```
## Passaggio 4: salva il documento
Salva il documento OneNote modificato come PDF:
```csharp
doc.Save(Path.Combine(dataDir, "AsposeDarkTheme.pdf"));
```
## Conclusione
Congratulazioni! Hai applicato con successo un tema scuro al testo nel tuo documento Aspose.Note. Questo miglioramento semplice ma efficace può conferire ai tuoi file OneNote un aspetto più sofisticato.
## Domande frequenti
### Posso applicare un tema scuro a sezioni specifiche del mio documento OneNote?
Sì, puoi personalizzare il codice per indirizzare pagine o sezioni specifiche all'interno del tuo documento.
### Aspose.Note supporta altri formati di esportazione oltre al PDF?
Assolutamente! Aspose.Note supporta vari formati di esportazione, incluse immagini e Microsoft Word.
### Esiste un limite alla dimensione del documento che Aspose.Note può gestire?
Aspose.Note può gestire documenti di varie dimensioni e le sue prestazioni sono ottimizzate per l'efficienza.
### Posso ripristinare il tema originale dopo aver applicato il tema scuro?
Sì, puoi modificare il codice per passare da un tema all'altro in base alle tue preferenze.
### Dove posso ottenere supporto per le query relative ad Aspose.Note?
 Per qualsiasi assistenza, visitare il[Forum Aspose.Note](https://forum.aspose.com/c/note/28) o esplora il[documentazione](https://reference.aspose.com/note/net/).