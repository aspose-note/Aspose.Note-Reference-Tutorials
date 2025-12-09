---
date: 2025-12-02
description: Scopri come esportare i caratteri mentre salvi OneNote in HTML usando
  Aspose.Note per Java. Questa guida ti mostra come creare OneNote programmaticamente
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

# Come esportare i caratteri quando si salva OneNote come HTML – Java

## Introduzione

In questo tutorial scoprirai **come esportare i caratteri** quando **salvi OneNote come HTML** utilizzando Aspose.Note per Java. Ti guideremo nella creazione di un documento OneNote in modo programmatico, nella configurazione delle opzioni di salvataggio HTML e nell'incorporamento dei file di carattere necessari affinché l'HTML risultante abbia esattamente lo stesso aspetto delle pagine OneNote originali. Questo approccio è perfetto quando è necessario preservare la fedeltà visiva del contenuto OneNote in un formato adatto al web.

## Risposte rapide
- **Quale libreria gestisce l'esportazione?** Aspose.Note per Java  
- **È possibile incorporare i caratteri nell'HTML?** Sì – imposta `ExportFonts` su `ExportEmbedded`  
- **È necessaria una licenza per la produzione?** È richiesta una licenza valida di Aspose.Note per l'uso commerciale  
- **Quale versione di Java è supportata?** Java 8 o superiore  
- **È possibile salvare le risorse in file separati?** Assolutamente – configura `ResourceExportType` di conseguenza  

## Cos'è “come esportare i caratteri” nel contesto della conversione HTML di OneNote?

Quando converti un blocco appunti OneNote in HTML, l'aspetto visivo dipende da CSS, immagini e, soprattutto, dai caratteri utilizzati nelle pagine originali. **Esportare i caratteri** significa incorporare i file dei caratteri (ad esempio TTF) direttamente nel pacchetto HTML affinché i browser possano renderizzare il testo esattamente come appare in OneNote, anche se l'utente finale non ha quei caratteri installati localmente.

## Perché creare OneNote programmaticamente e salvarlo come HTML?

- **Automazione:** Genera report, documentazione o articoli per la knowledge‑base da OneNote senza copiare‑incollare manualmente.  
- **Coerenza:** Preserva layout, stile e caratteri personalizzati su tutti i dispositivi.  
- **Portabilità:** L'HTML è visualizzabile universalmente—non è necessario il client OneNote.  

## Prerequisiti

1. Java Development Kit (JDK) 8 o più recente installato.  
2. Libreria Aspose.Note per Java – scaricala da [qui](https://releases.aspose.com/note/java/).  
3. Un file OneNote di esempio (`.one`) da caricare, oppure puoi crearne uno nuovo in modo programmatico.  

## Importare i pacchetti

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

## Come esportare i caratteri durante il salvataggio di OneNote come HTML?

Di seguito trovi una guida passo‑a‑passo che mostra **come esportare i caratteri** e altre risorse.

### Passo 1: Creare un documento OneNote programmaticamente  

```java
Document document = new Document("Path_to_your_sample_one_file");
```

Questa riga carica un file `.one` esistente. Se devi **creare OneNote programmaticamente**, puoi istanziare un nuovo oggetto `Document` e aggiungere sezioni/pagine tramite l'API (non mostrato qui per mantenere il focus sull'esportazione dei caratteri).

### Passo 2: Salvare in uno stream di memoria con i caratteri incorporati  

```java
HtmlSaveOptions options = new HtmlSaveOptions();
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);
options.setFontFaceTypes(FontFaceType.Ttf);

ByteArrayOutputStream outputStream = new ByteArrayOutputStream();
document.save(outputStream, options);
```

- `setExportFonts(ResourceExportType.ExportEmbedded)` indica ad Aspose.Note di **esportare i caratteri** direttamente nel pacchetto HTML.  
- `setFontFaceTypes(FontFaceType.Ttf)` assicura che vengano utilizzati i caratteri TrueType, che hanno ampio supporto nei browser.

### Passo 3: Salvare come HTML con file di risorse separati (continuando a esportare i caratteri)  

```java
HtmlSaveOptions options = new HtmlSaveOptions();
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);

document.save("output_directory/document.html", options);
```

Anche se CSS e immagini sono incorporati, puoi cambiare `ResourceExportType` in `ExportExternal` se preferisci file separati per una più facile cache. La parte chiave—**esportare i caratteri**—rimane invariata.

### Passo 4: Utilizzare i callback per controllare dove viene memorizzata ogni risorsa  

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

La classe `UserSavingCallbacks` (dovrai implementare `ICssSavingCallback`, `IImageSavingCallback` e `IFontSavingCallback`) ti dà il pieno controllo sulla struttura delle cartelle, permettendoti di tenere i caratteri in una directory dedicata `fonts` mantenendo comunque **l'esportazione corretta dei caratteri**.

## Problemi comuni e suggerimenti

- **Caratteri mancanti nell'output:** Verifica che `setExportFonts(ResourceExportType.ExportEmbedded)` sia impostato e che il file OneNote di origine utilizzi effettivamente caratteri incorporati.  
- **File HTML di grandi dimensioni:** L'incorporamento dei caratteri può aumentare le dimensioni. Se la larghezza di banda è un problema, passa `ExportFonts` a `ExportExternal` e ospita i caratteri su un CDN.  
- **Errori di implementazione dei callback:** Assicurati che le classi di callback scrivano correttamente lo stream e chiudano le risorse per evitare corruzioni dei file.  

## Domande frequenti

**D: Posso convertire più documenti OneNote in HTML in un'unica operazione?**  
R: Sì, itera su ciascuna istanza `Document` e applica le stesse `HtmlSaveOptions`.  

**D: Aspose.Note per Java supporta altri formati di output oltre a HTML?**  
R: Assolutamente. Puoi esportare in PDF, DOCX, PNG, JPEG e molto altro utilizzando le opzioni di salvataggio appropriate.  

**D: È disponibile una versione di prova di Aspose.Note per Java?**  
R: Sì, scarica una prova gratuita da [qui](https://releases.aspose.com/).  

**D: Dove posso ottenere supporto per Aspose.Note per Java?**  
R: Visita il [forum Aspose.Note](https://forum.aspose.com/c/note/28) per assistenza della community e del team ufficiale.  

**D: Come posso acquistare una licenza per Aspose.Note per Java?**  
R: Le licenze sono disponibili sul [sito Aspose](https://purchase.aspose.com/buy).  

## Conclusione

Ora sai **come esportare i caratteri** mentre **salvi OneNote come HTML** usando Aspose.Note per Java. Configurando `HtmlSaveOptions` e, opzionalmente, utilizzando i callback, puoi preservare l'aspetto esatto delle tue pagine OneNote—including i caratteri personalizzati—quando le pubblichi sul web. Sentiti libero di sperimentare con le diverse impostazioni di `ResourceExportType` per adattarle alle esigenze di prestazioni e archiviazione del tuo progetto.

---

**Ultimo aggiornamento:** 2025-12-02  
**Testato con:** Aspose.Note per Java 24.12  
**Autore:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}