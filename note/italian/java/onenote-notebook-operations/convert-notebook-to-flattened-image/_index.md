---
date: 2025-12-25
description: Scopri come convertire OneNote in PNG usando Aspose.Note per Java. Questa
  guida mostra come impostare la risoluzione dell'immagine, appiattire un blocco appunti
  e salvare OneNote come immagine in modo efficiente.
linktitle: How to Convert OneNote to PNG – Flatten Notebook to Image with Aspose.Note
second_title: Aspose.Note Java API
title: Come convertire OneNote in PNG – Appiattire il blocco appunti in immagine con
  Aspose.Note
url: /it/java/onenote-notebook-operations/convert-notebook-to-flattened-image/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Converti Notebook in Immagine Appiattita in OneNote - Aspose.Note

## Introduzione

In questo tutorial scoprirai come **convertire OneNote in PNG** trasformando un intero notebook in un'unica immagine appiattita usando Aspose.Note per Java. Questo approccio è perfetto quando devi condividere un notebook come immagine statica, incorporarlo nei report o archiviarlo senza perdere alcun dettaglio visivo.

## Risposte Rapide
- **Cosa significa “flatten notebook”?** Unisce tutti gli elementi della pagina in un'unica immagine raster.  
- **Quale formato viene utilizzato?** PNG è il predefinito, garantendo qualità senza perdita.  
- **Posso cambiare il DPI?** Sì, usa `setResolution` su `ImageSaveOptions`.  
- **È necessaria una licenza?** Una versione di prova gratuita è sufficiente per la valutazione; è richiesta una licenza commerciale per la produzione.  
- **È supportato su tutti i sistemi operativi?** L'API Java funziona ovunque Java sia disponibile.

## Cos'è la conversione di OneNote in PNG?

Convertire OneNote in PNG crea una rappresentazione bitmap di ogni pagina del notebook, preservando testo, disegni e oggetti incorporati in un unico file immagine. Questo è particolarmente utile per documentazione, presentazioni o archivi di conformità.

## Perché convertire OneNote in PNG con Aspose.Note?

- **Fedele al 100 %** – Tutti gli elementi visivi sono conservati.  
- **Output in un unico file** – Non è necessario gestire più file di pagina.  
- **Risoluzione personalizzabile** – Regola il DPI per soddisfare i requisiti di qualità.  
- **Nessuna installazione di Office** – Funziona completamente indipendente da Microsoft OneNote.

## Prerequisiti

Prima di iniziare, assicurati di avere quanto segue:

1. Java Development Kit (JDK) installato sul tuo sistema.  
2. Libreria Aspose.Note per Java scaricata e configurata nel tuo progetto Java. Puoi scaricare la libreria da [qui](https://releases.aspose.com/note/java/).  
3. Conoscenze di base della programmazione Java.

## Importa Pacchetti

Per iniziare, devi importare i pacchetti necessari da Aspose.Note per Java:

```java
import java.io.IOException;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.Notebook;
import com.aspose.note.NotebookImageSaveOptions;
import com.aspose.note.SaveFormat;
```

## Passo 1: Configura la Directory del Documento

Innanzitutto, definisci la directory in cui si trova il tuo file notebook:

```java
String dataDir = "Your Document Directory";
```

Sostituisci `"Your Document Directory"` con il percorso del tuo file notebook.

## Passo 2: Carica il Notebook

Successivamente, carica il file notebook usando la classe `Notebook`:

```java
Notebook notebook = new Notebook(dataDir + "test.onetoc2");
```

Assicurati di sostituire `"test.onetoc2"` con il nome del tuo file notebook.

## Passo 3: Imposta le Opzioni di Salvataggio Immagine

Ora, imposta le opzioni per salvare il notebook come immagine. Specificheremo il formato di salvataggio come PNG e imposteremo la risoluzione a 400 DPI:

```java
NotebookImageSaveOptions saveOptions = new NotebookImageSaveOptions(SaveFormat.Png);
ImageSaveOptions documentSaveOptions = saveOptions.getDocumentSaveOptions();
documentSaveOptions.setResolution(400);
```

Puoi regolare la risoluzione secondo le tue esigenze. Qui è dove **imposti la risoluzione dell'immagine** per controllare la qualità dell'output.

## Passo 4: Appiattisci il Notebook

Per garantire che tutti gli elementi siano appiattiti in un'unica immagine, imposta l'opzione `flatten` su `true`:

```java
saveOptions.setFlatten(true);
```

Impostare `flatten` su `true` garantisce che il PNG risultante mantenga l'esatta disposizione del tuo notebook.

## Passo 5: Salva l'Immagine

Infine, salva il notebook come immagine appiattita:

```java
notebook.save(dataDir + "ExportImageasFlattenedNotebook_out.png", saveOptions);
```

Sostituisci `"ExportImageasFlattenedNotebook_out.png"` con il nome del file di output desiderato. Questo passo **salva OneNote come immagine** che puoi condividere o incorporare ovunque.

## Casi d'Uso Comuni

- **Documentazione:** Incorpora l'immagine del notebook nei manuali tecnici o nelle guide utente.  
- **Presentazioni:** Usa una diapositiva PNG ad alta risoluzione in PowerPoint senza preoccuparti della compatibilità di font o oggetti.  
- **Archiviazione:** Conserva uno snapshot in sola lettura di un notebook per audit di conformità.

## Suggerimenti per la Risoluzione dei Problemi

- **File non trovato:** Controlla nuovamente il percorso `dataDir` e assicurati che il file `.onetoc2` esista.  
- **Immagine di bassa qualità:** Aumenta il DPI modificando `documentSaveOptions.setResolution(600);`.  
- **Elementi mancanti:** Verifica che `saveOptions.setFlatten(true);` sia abilitato; altrimenti, alcuni livelli potrebbero rimanere separati.

## Domande Frequenti

**Q1: Posso regolare la risoluzione dell'immagine di output?**  
A1: Sì, puoi regolare la risoluzione secondo le tue esigenze modificando il parametro del metodo `setResolution`.

**Q2: Aspose.Note supporta altri formati immagine per l'esportazione?**  
A2: Sì, Aspose.Note supporta vari formati immagine come PNG, JPEG, BMP, ecc., per l'esportazione dei notebook.

**Q3: Posso personalizzare ulteriormente l'immagine di output?**  
A3: Sì, Aspose.Note offre ampie opzioni per personalizzare l'immagine di output, inclusi dimensioni della pagina, orientamento e impostazioni di qualità.

**Q4: È disponibile una versione di prova per Aspose.Note per Java?**  
A4: Sì, puoi ottenere una versione di prova gratuita da [qui](https://releases.aspose.com/).

**Q5: Dove posso trovare supporto per Aspose.Note per Java?**  
A5: Puoi trovare supporto e risorse sul forum di Aspose.Note [qui](https://forum.aspose.com/c/note/28).

---

**Ultimo aggiornamento:** 2025-12-25  
**Testato con:** Aspose.Note per Java 24.12  
**Autore:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}