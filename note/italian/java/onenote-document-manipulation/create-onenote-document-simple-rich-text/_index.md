---
date: 2026-02-18
description: Scopri come impostare lo stile del paragrafo e aggiungere un elemento
  di outline quando crei documenti OneNote in Java usando Aspose.Note. Esporta OneNote
  in PDF, salva OneNote come PDF e genera file OneNote senza sforzo.
linktitle: Set Paragraph Style while Creating OneNote Document in Java
second_title: Aspose.Note Java API
title: Esporta OneNote in PDF – Imposta lo stile del paragrafo durante la creazione
  di un documento OneNote in Java
url: /it/java/onenote-document-manipulation/create-onenote-document-simple-rich-text/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Imposta lo Stile del Paragrafo durante la Creazione di un Documento OneNote in Java

## Introduzione

Nel panorama di sviluppo odierno, in rapido movimento, la possibilità di **esportare OneNote in PDF** programmaticamente è essenziale per produrre documenti rifiniti e pronti per la condivisione. Questo tutorial ti guida nella creazione di un file OneNote, nell'applicazione di uno stile di paragrafo personalizzato e infine nell'**esportare OneNote in PDF** usando Aspose.Note per Java. Che tu stia costruendo un motore di reporting, una soluzione automatizzata per prendere appunti o un servizio di conversione di documenti, le tecniche trattate qui ti aiuteranno a **salvare OneNote come PDF** con un controllo preciso della formattazione.

## Risposte Rapide
- **Cosa significa “set paragraph style”?** Applica font, dimensione, colore e altre formattazioni a un paragrafo di testo.  
- **Posso esportare il risultato in PDF?** Sì – il tutorial termina con il salvataggio del file OneNote come PDF.  
- **È necessaria una licenza per Aspose.Note?** Una prova gratuita è sufficiente per la valutazione; è necessaria una licenza per la produzione.  
- **Quali IDE sono supportati?** Qualsiasi IDE Java – Eclipse, IntelliJ IDEA, NetBeans, ecc.  
- **Quanto tempo richiede l'implementazione?** Circa 10‑15 minuti per un documento di base.

## Cos'è “set paragraph style” in Aspose.Note?
Impostare lo stile del paragrafo si riferisce alla configurazione di un oggetto `ParagraphStyle` (nome del font, dimensione, colore, ecc.) e al suo collegamento a un nodo `RichText`. Questo ti dà il pieno controllo su come il testo appare all'interno di una pagina OneNote.

## Come Impostare lo Stile del Paragrafo in OneNote?
Applicare uno stile è semplice come creare un'istanza `ParagraphStyle`, personalizzare le sue proprietà e assegnarla a un elemento `RichText`. L'API rende questa un'operazione a una riga una volta che l'oggetto stile è pronto.

## Perché Esportare OneNote in PDF?
- **Branding coerente:** Conserva i font e i colori aziendali quando condividi le note all'esterno.  
- **Leggibilità:** Il PDF mantiene la disposizione esatta, rendendolo ideale per la stampa o l'archiviazione.  
- **Accesso cross‑platform:** I destinatari possono visualizzare il PDF su qualsiasi dispositivo senza necessità di OneNote.  

## Prerequisiti

Prima di iniziare, assicurati di avere:

1. **Java Development Kit (JDK) 1.8+** – qualsiasi JDK recente funzionerà.  
2. **Aspose.Note for Java** – scarica l'ultimo JAR dalla [pagina di download di Aspose.Note](https://releases.aspose.com/note/java/).  
3. **Un IDE** (Eclipse, IntelliJ IDEA o NetBeans) per compilare ed eseguire il campione.  

> **Suggerimento professionale:** Aggiungi il JAR di Aspose.Note al classpath del tuo progetto tramite Maven o facendo riferimento manualmente al JAR nel tuo IDE.

## Importa i Pacchetti

Per prima cosa, importa le classi di cui avremo bisogno. Questo blocco rimane invariato.

```java
import java.awt.Color;
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.SaveFormat;
import com.aspose.note.ParagraphStyle;
```

> La classe `ParagraphStyle` è la chiave per **set paragraph style** più avanti nel tutorial.

## Guida Passo‑Passo

Di seguito trovi una guida concisa di ogni operazione. I blocchi di codice sono esattamente come nell'esempio originale; aggiungiamo solo testo esplicativo.

### Passo 1: Imposta la Directory del Documento
Definisci dove verranno salvati i file generati.

```java
String dataDir = "Your Document Directory";
```

Sostituisci `"Your Document Directory"` con un percorso assoluto o relativo sulla tua macchina.

### Passo 2: Inizializza l'Oggetto Document
Crea il `Document` radice che rappresenta il file OneNote.

```java
Document doc = new Document();
```

### Passo 3: Inizializza l'Oggetto Page
Un file OneNote è composto da una o più pagine; iniziamo con una singola pagina.

```java
Page page = new Page();
```

### Passo 4: Inizializza l'Oggetto Outline
Gli outline fungono da contenitori per gli elementi outline (pensali come sezioni).

```java
Outline outline = new Outline();
```

### Passo 5: Inizializza l'Oggetto OutlineElement
Qui **aggiungiamo l'elemento outline** che conterrà il nostro testo formattato.

```java
OutlineElement outlineElem = new OutlineElement();
```

### Passo 6: Imposta lo Stile del Testo (Set Paragraph Style)

```java
ParagraphStyle textStyle = new ParagraphStyle()
                                    .setFontColor(Color.black)
                                    .setFontName("Arial")
                                    .setFontSize(10);
```

L'istanza `ParagraphStyle` definisce il font, la dimensione e il colore—qui **impostiamo lo stile del paragrafo** per il prossimo nodo di testo.

### Passo 7: Inizializza l'Oggetto RichText

```java
RichText text = new RichText().append("Hello OneNote text!");
text.setParagraphStyle(textStyle);
```

Creiamo un nodo `RichText`, inseriamo una stringa semplice e colleghiamo lo stile definito in precedenza.

### Passo 8: Aggiungi il Nodo RichText a OutlineElement

```java
outlineElem.appendChildLast(text);
```

Ora il testo formattato vive all'interno dell'elemento outline.

### Passo 9: Aggiungi il Nodo OutlineElement a Outline

```java
outline.appendChildLast(outlineElem);
```

L'outline ora contiene l'elemento che contiene il nostro paragrafo.

### Passo 10: Aggiungi il Nodo Outline alla Pagina

```java
page.appendChildLast(outline);
```

Posizioniamo l'outline sulla pagina.

### Passo 11: Aggiungi il Nodo Page al Document

```java
doc.appendChildLast(page);
```

Il documento ora ha una singola pagina con il nostro testo formattato.

### Passo 12: Salva il Documento (Export OneNote PDF)

```java
doc.save(dataDir + "CreateOneNoteDocumentWithSimpleRichText_out.pdf", SaveFormat.Pdf);
```

Il metodo `save` scrive il file OneNote e **esporta OneNote PDF** in un unico passaggio. Puoi anche salvare come `.one` usando `SaveFormat.One` se ti serve il formato nativo.

## Problemi Comuni & Soluzioni

| Problema | Motivo | Soluzione |
|----------|--------|-----------|
| **File non trovato** | `dataDir` punta a una cartella inesistente. | Assicurati che la directory esista o creala programmaticamente (`new File(dataDir).mkdirs();`). |
| **PDF vuoto** | Nessun contenuto è stato aggiunto prima del salvataggio. | Verifica che il nodo `RichText` sia stato aggiunto e che lo stile sia impostato. |
| **Font non supportato** | Nome del font non installato sul sistema. | Usa un font comune come `"Arial"` o incorpora il font nel progetto. |

## Domande Frequenti

**D: Aspose.Note può gestire formattazioni complesse come tabelle o immagini?**  
R: Sì, l'API supporta tabelle, immagini, collegamenti ipertestuali e funzionalità di layout più avanzate.

**D: È possibile **convertire OneNote PDF** nuovamente in un file OneNote?**  
R: La conversione diretta non è fornita, ma puoi estrarre il contenuto del PDF e ricostruire un documento OneNote usando l'API.

**D: La libreria funziona su ambienti Linux/macOS?**  
R: Assolutamente. Aspose.Note per Java è indipendente dalla piattaforma; basta assicurarsi che il JDK sia installato.

**D: Come aggiungo più pagine o outline?**  
R: Crea ulteriori oggetti `Page` e `Outline`, quindi aggiungili al `Document` proprio come nell'esempio a pagina singola.

**D: Dove posso trovare più esempi?**  
R: La documentazione ufficiale di Aspose.Note e il [forum di supporto](https://forum.aspose.com/c/note/28) contengono molti esempi di codice.

## Conclusione

Ora hai visto come **impostare lo stile del paragrafo**, **aggiungere l'elemento outline** e **generare un file OneNote** che può essere **esportato in PDF** usando Aspose.Note per Java. Incorporare testo formattato fin dall'inizio del processo di creazione garantisce che il documento finale abbia un aspetto professionale e che qualsiasi successiva operazione di **convert OneNote PDF** mantenga la formattazione. Sentiti libero di ampliare questa base con immagini, tabelle o metadati personalizzati per soddisfare le esigenze del tuo progetto.

---

**Last Updated:** 2026-02-18  
**Tested With:** Aspose.Note for Java 24.11 (latest release)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}