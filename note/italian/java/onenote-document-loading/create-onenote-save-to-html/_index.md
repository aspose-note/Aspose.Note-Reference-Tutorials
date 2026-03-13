---
date: 2026-02-07
description: Scopri come esportare i caratteri mentre salvi OneNote in formato HTML
  usando Aspose.Note per Java. Questa guida ti mostra come creare OneNote programmaticamente
  e incorporare caratteri, CSS e immagini.
linktitle: How to Export Fonts When Saving OneNote as HTML – Java
second_title: Aspose.Note Java API
title: Come esportare i font quando si salva OneNote come HTML – Java
url: /it/java/onenote-document-loading/create-onenote-save-to-html/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Come esportare i font quando si salva OneNote come HTML – Java

## Introduzione

In questo tutorial scoprirai **come esportare i font** quando **salvi OneNote come HTML** utilizzando Aspose.Note per Java. Ti guideremo nella creazione di un documento OneNote programmaticamente, nella configurazione delle opzioni di salvataggio HTML e nell'incorporamento dei file di font necessari affinché l'HTML risultante abbia esattamente lo stesso aspetto delle pagine originali di OneNote. Questo approccio è perfetto quando è necessario preservare la fedeltà visiva del contenuto di OneNote in un formato adatto al web.

## Risposte rapide
- **Quale libreria gestisce l'esportazione?** Aspose.Note per Java  
- **I font possono essere incorporati nell'HTML?** Sì – imposta `ExportFonts` su `ExportEmbedded`  
- **È necessaria una licenza per la produzione?** È richiesta una licenza valida di Aspose.Note per uso commerciale  
- **Quale versione di Java è supportata?** Java 8 o superiore  
- **È possibile salvare le risorse in file separati?** Assolutamente – configura `ResourceExportType` di conseguenza  

## Cos'è “come esportare i font” nel contesto della conversione HTML di OneNote?

Quando converti un blocco note OneNote in HTML, l'aspetto visivo dipende da CSS, immagini e soprattutto dai font utilizzati nelle pagine originali. **Esportare i font** significa incorporare i file dei font (ad esempio TTF) direttamente nel pacchetto HTML affinché i browser possano renderizzare il testo esattamente come appare in OneNote, anche se l'utente finale non ha quei font installati localmente.

## Perché creare OneNote programmaticamente e salvarlo come HTML?

- **Automazione:** Generare report, documentazione o articoli di knowledge‑base da OneNote senza copia‑incolla manuale.  
- **Coerenza:** Preservare layout, stile e font personalizzati su tutti i dispositivi.  
- **Portabilità:** HTML è visualizzabile universalmente—non è necessario il client OneNote.  

## Prerequisiti

1. Java Development Kit (JDK) 8 o più recente installato.  
2. Libreria Aspose.Note per Java – scarica da [here](https://releases.aspose.com/note/java/).  
3. Un file OneNote di esempio (`.one`) da caricare, oppure è possibile crearne uno nuovo programmaticamente.  

## Importa pacchetti

Per prima cosa, importa le classi necessarie nel tuo progetto Java:

```java
import java.io.ByteArrayOutputStream;
import java.io.File;
import java.io.FileOutputStream;
import java.io.IOException;
import java.io.OutputStream;
import java.io.OutputStreamWriter;
import java.nio.file.Paths;
import com.aspose.note.CssSavingArgs;
import com.aspose.note.Document;
import com.aspose.note.FontFaceType;
import com.aspose.note.FontSavingArgs;
import com.aspose.note.HtmlSaveOptions;
import com.aspose.note.ICssSavingCallback;
import com.aspose.note.IFontSavingCallback;
import com.aspose.note.IImageSavingCallback;
import com.aspose.note.ImageSavingArgs;
import com.aspose.note.ResourceExportType;
```

## Come esportare i font durante il salvataggio di OneNote come HTML?

Di seguito trovi una guida passo‑passo che mostra **come esportare i font** e altre risorse.

### Passo 1: Crea un documento OneNote programmaticamente  

```java
Document document = new Document("Path_to_your_sample_one_file");
```

Questa riga carica un file `.one` esistente. Se devi **creare OneNote programmaticamente**, puoi istanziare un nuovo oggetto `Document` e aggiungere sezioni/pagine tramite l'API (non mostrato qui per mantenere il focus sull'esportazione dei font).

### Passo 2: Salva su uno stream di memoria con i font incorporati  

```java
HtmlSaveOptions options = new HtmlSaveOptions();
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);
options.setFontFaceTypes(FontFaceType.Ttf);

ByteArrayOutputStream outputStream = new ByteArrayOutputStream();
document.save(outputStream, options);
```

- `setExportFonts(ResourceExportType.ExportEmbedded)` indica ad Aspose.Note di **esportare i font** direttamente nel pacchetto HTML.  
- `setFontFaceTypes(FontFaceType.Ttf)` garantisce che vengano utilizzati font TrueType, i quali hanno ampio supporto nei browser.

### Passo 3: Salva come HTML con file di risorse separati (continua a esportare i font)  

```java
HtmlSaveOptions options = new HtmlSaveOptions();
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);

document.save("output_directory/document.html", options);
```

Anche se CSS e immagini sono incorporati, puoi cambiare `ResourceExportType` in `ExportExternal` se preferisci file separati per una più facile cache. La parte chiave—**esportare i font**—rimane invariata.

### Passo 4: Usa i callback per controllare dove viene memorizzata ogni risorsa  

```java
Document document = new Document("Path_to_your_sample_one_file");

UserSavingCallbacks savingCallbacks = new UserSavingCallbacks();
savingCallbacks.setRootFolder("documentFolder");
savingCallbacks.setCssFolder("css");
savingCallbacks.setKeepCssStreamOpened(true);
savingCallbacks.setImagesFolder("images");
savingCallbacks.setFontsFolder("fonts");

HtmlSaveOptions options = new HtmlSaveOptions();
options.setFontFaceTypes(FontFaceType.Ttf);
options.setCssSavingCallback(savingCallbacks);
options.setImageSavingCallback(savingCallbacks);
options.setFontSavingCallback(savingCallbacks);
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);

File dir = new File(savingCallbacks.getRootFolder());
if (!dir.exists()) {
    dir.mkdir();
}

document.save(Paths.get(savingCallbacks.getRootFolder(), "document.html").toString(), options);
```

La classe `UserSavingCallbacks` (dovrai implementare `ICssSavingCallback`, `IImageSavingCallback` e `IFontSavingCallback`) ti offre il pieno controllo sulla struttura delle cartelle, permettendoti di tenere i font in una directory dedicata `fonts` mantenendo comunque **l'esportazione corretta dei font**.

## Come incorporare font personalizzati durante la conversione di OneNote in HTML

Incorporare font personalizzati garantisce che il rendering HTML corrisponda al layout originale di OneNote, anche su dispositivi che non hanno quei font installati. Utilizzando `ExportEmbedded` insieme a `FontFaceType.Ttf`, i file TrueType vengono codificati in base‑64 e inseriti direttamente nel CSS generato, eliminando la necessità di ospitare i font esternamente.

## Utilizzare ResourceExportType per controllare l'esportazione delle risorse

`ResourceExportType` ti consente di decidere se CSS, immagini e font siano memorizzati **all'interno** del file HTML (`ExportEmbedded`) o salvati come file **esterni** (`ExportExternal`). Scegli `ExportEmbedded` per una soluzione a file unico, oppure `ExportExternal` quando vuoi sfruttare la cache del browser per risorse di grandi dimensioni.

## Creare OneNote programmaticamente per l'esportazione HTML

Se parti da zero, puoi costruire un documento OneNote interamente in codice, aggiungere sezioni, pagine e testo formattato, e poi applicare le stesse `HtmlSaveOptions` mostrate sopra. Questo ti offre un'automazione end‑to‑end: dalla generazione dei dati a un output HTML completamente stilizzato con font personalizzati incorporati.

## Problemi comuni e suggerimenti

- **Font mancanti nell'output:** Verifica che `setExportFonts(ResourceExportType.ExportEmbedded)` sia impostato e che il file OneNote di origine utilizzi effettivamente font incorporati.  
- **File HTML di grandi dimensioni:** L'incorporamento dei font può aumentare le dimensioni. Se la larghezza di banda è un problema, passa `ExportFonts` a `ExportExternal` e ospita i font su un CDN.  
- **Errori di implementazione dei callback:** Assicurati che le classi di callback scrivano correttamente lo stream e chiudano le risorse per evitare corruzioni dei file.  

## Domande frequenti

**D: Posso convertire più documenti OneNote in HTML in una sola volta?**  
R: Sì, itera su ciascuna istanza `Document` e applica le stesse `HtmlSaveOptions`.  

**D: Aspose.Note per Java supporta altri formati di output oltre a HTML?**  
R: Assolutamente. Puoi esportare in PDF, DOCX, PNG, JPEG e molto altro usando le opzioni di salvataggio appropriate.  

**D: È disponibile una versione di prova per Aspose.Note per Java?**  
R: Sì, scarica una prova gratuita da [here](https://releases.aspose.com/).  

**D: Dove posso ottenere supporto per Aspose.Note per Java?**  
R: Visita il [Aspose.Note forum](https://forum.aspose.com/c/note/28) per assistenza dalla community e dal team ufficiale.  

**D: Come posso acquistare una licenza per Aspose.Note per Java?**  
R: Le licenze sono disponibili sul [sito Aspose](https://purchase.aspose.com/buy).  

## Conclusione

Ora sai **come esportare i font** mentre **salvi OneNote come HTML** usando Aspose.Note per Java. Configurando `HtmlSaveOptions` e, facoltativamente, utilizzando i callback, puoi preservare l'aspetto esatto delle tue pagine OneNote—including i font personalizzati—quando le pubblichi sul web. Sentiti libero di sperimentare con le diverse impostazioni di `ResourceExportType` per adattarle alle esigenze di prestazioni e archiviazione del tuo progetto.

---

**Last Updated:** 2026-02-07  
**Tested With:** Aspose.Note for Java 24.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}