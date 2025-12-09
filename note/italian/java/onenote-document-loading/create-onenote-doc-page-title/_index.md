---
date: 2025-12-02
description: Scopri come creare una pagina OneNote con un titolo in Java usando Aspose.Note
  per Java. Questa guida mostra come impostare il titolo della pagina OneNote e personalizzare
  il carattere del titolo.
linktitle: How to Create OneNote Page with Title - Java
second_title: Aspose.Note Java API
title: Come creare una pagina OneNote con titolo - Java
url: /it/java/onenote-document-loading/create-onenote-doc-page-title/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Come creare una pagina OneNote con titolo - Java

## Introduzione

Se hai bisogno di **come creare una pagina OneNote** programmaticamente, Aspose.Note per Java lo rende semplice. In questo tutorial imparerai a generare un file OneNote, impostare il titolo della pagina e persino personalizzare il font del titolo, tutto dal codice Java. Alla fine avrai un documento OneNote pronto all'uso che potrai integrare in qualsiasi applicazione Java.

## Risposte rapide
- **Quale libreria è necessaria?** Aspose.Note per Java.
- **Posso impostare un font personalizzato per il titolo?** Sì – usa `ParagraphStyle` per definire il nome del font, la dimensione e il colore.
- **Quale versione di Java è supportata?** Qualsiasi JDK 8+ (l'API è retrocompatibile).
- **È necessaria una licenza per lo sviluppo?** Una versione di prova gratuita funziona per i test; è necessaria una licenza per la produzione.
- **Dove viene salvato l'output?** Definisci il percorso nella variabile `dataDir`.

## Cos'è il titolo di una pagina OneNote?
Il titolo di una pagina OneNote è l'intestazione visualizzata nella parte superiore di ogni pagina. Tipicamente include il nome della pagina, la data di creazione e l'ora. Impostare questo titolo programmaticamente ti aiuta a creare notebook coerenti e ben strutturati.

## Perché impostare il titolo della pagina OneNote programmaticamente?
- **Automazione:** Genera report o note di riunioni senza modifiche manuali.  
- **Coerenza:** Applica una convenzione di denominazione su tutte le pagine.  
- **Integrazione:** Combina OneNote con altri sistemi (ad es., CRM, strumenti di gestione progetti).  

## Prerequisiti

- **Java Development Kit (JDK)** – versione 8 o superiore.  
- **Aspose.Note for Java** – scarica dal sito ufficiale **[qui](https://releases.aspose.com/note/java/)**.  
- **IDE** – IntelliJ IDEA, Eclipse o NetBeans (a tua scelta).

## Importa i pacchetti

Per prima cosa, importa le classi necessarie dalla libreria Aspose.Note.

```java
import com.aspose.note.*;
import java.awt.*;
import java.io.IOException;
import java.util.Calendar;
```

### Passo 1: Configura la directory del documento  
Definisci dove verrà salvato il file OneNote generato.

```java
// The path to the documents directory.
String dataDir = "Your Document Directory";
```

### Passo 2: Crea l'oggetto Document  
Istanzia un nuovo `Document` – rappresenta il file OneNote che costruirai.

```java
// Create an object of the Document class
Document doc = new Document();
```

### Passo 3: Inizializza l'oggetto Page  
Crea un oggetto `Page` che conterrà il titolo e qualsiasi contenuto.

```java
// Initialize Page class object
Page page = new Page();
```

### Passo 4: Imposta lo stile di testo predefinito  
Definisci un `ParagraphStyle` predefinito che verrà applicato al testo del titolo. Qui è dove **personalizziamo il font del titolo OneNote**.

```java
// Default style for all text in the document.
ParagraphStyle textStyle = new ParagraphStyle()
                            .setFontColor(Color.BLACK)
                            .setFontName("Arial")
                            .setFontSize(10);
```

### Passo 5: Imposta le proprietà del titolo della pagina  
Qui **impostiamo i dettagli del titolo della pagina OneNote** – il testo del titolo, la data e l'ora. Sentiti libero di modificare le stringhe per adattarle al tuo caso d'uso.

```java
// Set page title properties
Title title = new Title();

RichText titleText = new RichText().append("Title text.");
titleText.setParagraphStyle(textStyle);
title.setTitleText(titleText);

Calendar cal = Calendar.getInstance();
cal.set(2018, 04, 03);
RichText titleDate = new RichText().append(cal.getTime().toString());
titleDate.setParagraphStyle(textStyle);
title.setTitleDate(titleDate);

RichText titleTime = new RichText().append("12:34");
titleTime.setParagraphStyle(textStyle);
title.setTitleText(titleTime);
```

### Passo 6: Assegna il titolo alla pagina  
Ora **aggiungiamo il titolo a OneNote** collegando l'oggetto `Title` con la `Page`.

```java
page.setTitle(title);
```

### Passo 7: Aggiungi la pagina al documento  
Aggiungi la pagina configurata alla struttura del documento.

```java
doc.appendChildLast(page);
```

### Passo 8: Salva il documento OneNote  
Specifica il nome del file di output e salva il notebook. Questo completa il processo di **creazione di file onenote in java**.

```java
dataDir = dataDir + "load//CreateDocWithPageTitle_out.one";

// Save OneNote document
doc.save(dataDir);
```

## Problemi comuni e suggerimenti

| Problema | Soluzione |
|----------|-----------|
| **Percorso file non valido** | Assicurati che `dataDir` termini con un separatore corretto (`/` o `\\`) e che la cartella esista. |
| **Titolo non visibile** | Verifica che `ParagraphStyle` sia applicato a ogni elemento `RichText`. |
| **Eccezione di licenza** | Usa una licenza di prova per i test; applica una licenza completa prima del rilascio. |
| **La data mostra il mese sbagliato** | I mesi in Java partono da zero; `cal.set(2018, 04, 03)` imposta in realtà maggio. Regola di conseguenza. |

## Domande frequenti

**D: Aspose.Note per Java è compatibile con diverse versioni di Java?**  
R: Sì, la libreria funziona con Java 8 e versioni successive, offrendoti flessibilità in tutti gli ambienti.

**D: Posso personalizzare lo stile e la dimensione del font del titolo della pagina?**  
R: Assolutamente! Usa `ParagraphStyle` (come mostrato al Passo 4) per impostare qualsiasi nome di font, dimensione e colore.

**D: Come aggiungo più contenuti (ad es., paragrafi, immagini) alla pagina?**  
R: Crea ulteriori oggetti `RichText` o `Image`, imposta i loro stili e aggiungili alla `Page` con `page.appendChildLast(yourObject)`.

**D: È disponibile una versione di prova per Aspose.Note per Java?**  
R: Sì, puoi scaricare una prova gratuita dal sito Aspose per valutare tutte le funzionalità.

**D: Dove posso ottenere supporto se incontro problemi?**  
R: Visita il [forum Aspose.Note](https://forum.aspose.com/c/note/28) per aiuto dalla community o apri un ticket di supporto con Aspose.

---

**Ultimo aggiornamento:** 2025-12-02  
**Testato con:** Aspose.Note for Java 24.12 (ultima versione al momento della scrittura)  
**Autore:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}