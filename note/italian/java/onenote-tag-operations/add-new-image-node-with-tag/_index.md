---
title: Aggiungi un nuovo nodo immagine con tag in OneNote - Aspose.Note
linktitle: Aggiungi un nuovo nodo immagine con tag in OneNote - Aspose.Note
second_title: Aspose.Note API Java
description: Scopri come aggiungere un nuovo nodo immagine con un tag in OneNote utilizzando Aspose.Note per Java. Migliora le tue capacità di programmazione Java senza sforzo.
weight: 10
url: /it/java/onenote-tag-operations/add-new-image-node-with-tag/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aggiungi un nuovo nodo immagine con tag in OneNote - Aspose.Note

## introduzione
Nel regno della programmazione Java, Aspose.Note si distingue come un potente strumento per gestire facilmente i documenti OneNote. Se stai cercando di migliorare le tue capacità e imparare come aggiungere un nuovo nodo immagine con un tag in OneNote utilizzando Aspose.Note, sei nel posto giusto. Questa guida passo passo ti guiderà attraverso il processo, assicurandoti di comprendere a fondo ogni concetto.
## Prerequisiti
Prima di immergerci nel tutorial, assicuriamoci di avere tutto ciò di cui hai bisogno:
1.  Aspose.Note per Java: assicurati di avere la libreria Aspose.Note installata. In caso contrario, puoi scaricarlo[Qui](https://releases.aspose.com/note/java/).
2. Ambiente di sviluppo Java: assicurati di avere un ambiente di sviluppo Java funzionante configurato sul tuo computer.
Ora che abbiamo i prerequisiti, passiamo ai passaggi successivi.
## Importa pacchetti
Nel tuo progetto Java, inizia importando i pacchetti necessari:
```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.Image;
import com.aspose.note.NoteTag;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.SaveFormat;
import com.aspose.note.TagIcon;
```
## Passaggio 1: crea un oggetto documento
```java
// Il percorso della directory dei documenti.
String dataDir = "Your Document Directory";
// creare un oggetto della classe Document
Document doc = new Document();
```
## Passaggio 2: inizializzare l'oggetto classe pagina
```java
// inizializza l'oggetto classe Page
Page page = new Page();
```
## Passaggio 3: inizializzare l'oggetto classe struttura
```java
// inizializza l'oggetto della classe Outline
Outline outline = new Outline();
```
## Passaggio 4: inizializzare l'oggetto classe OutlineElement
```java
// inizializza l'oggetto della classe OutlineElement
OutlineElement outlineElem = new OutlineElement();
```
## Passaggio 5: carica e inserisci l'immagine
```java
// caricare un'immagine
Image image = new Image(null, dataDir + "Input.jpg");
// inserisci l'immagine nel nodo del documento
outlineElem.appendChildLast(image);
```
## Passaggio 6: aggiungi il tag nota all'immagine
```java
// aggiungi un tag di nota stella gialla all'immagine
NoteTag noteTag = NoteTag.createYellowStar();
image.getTags().add(noteTag);
```
## Passaggio 7: aggiungi il nodo dell'elemento del contorno
```java
// aggiungi il nodo dell'elemento del contorno
outline.appendChildLast(outlineElem);
```
## Passaggio 8: aggiungi il nodo del contorno
```java
// aggiungi nodo di contorno
page.appendChildLast(outline);
```
## Passaggio 9: aggiungi il nodo della pagina
```java
// aggiungi nodo di pagina
doc.appendChildLast(page);
```
## Passaggio 10: salva il documento OneNote
```java
// salva il documento OneNote come PDF
doc.save(dataDir + "AddNewImageNodeWithTag_out.pdf", SaveFormat.Pdf);
```
Congratulazioni! Hai aggiunto con successo un nuovo nodo immagine con un tag in OneNote utilizzando Aspose.Note per Java.
## Conclusione
 Padroneggiare Aspose.Note per Java apre interessanti possibilità nella manipolazione dei documenti OneNote. Seguendo questo tutorial, hai acquisito un'abilità pratica che può essere applicata a vari progetti. Continua a esplorare la documentazione di Aspose.Note[Qui](https://reference.aspose.com/note/java/)per funzionalità e possibilità più avanzate.
## Domande frequenti
### Dove posso trovare la documentazione di Aspose.Note?
 Puoi trovare la documentazione[Qui](https://reference.aspose.com/note/java/).
### Come posso scaricare Aspose.Note per Java?
 Puoi scaricarlo dalla pagina delle versioni[Qui](https://releases.aspose.com/note/java/).
### È disponibile una prova gratuita?
 Sì, puoi accedere alla prova gratuita[Qui](https://releases.aspose.com/).
### Dove posso ottenere supporto per Aspose.Note?
 Visita il forum della comunità[Qui](https://forum.aspose.com/c/note/28) per supporto.
### Ho bisogno di una licenza temporanea?
 Se necessario, è possibile ottenere una licenza temporanea[Qui](https://purchase.aspose.com/temporary-license/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
