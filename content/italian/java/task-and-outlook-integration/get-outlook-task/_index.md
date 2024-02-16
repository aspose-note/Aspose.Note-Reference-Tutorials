---
title: Ottieni attività di Outlook in OneNote - Aspose.Note
linktitle: Ottieni attività di Outlook in OneNote - Aspose.Note
second_title: Aspose.Note API Java
description: Esplora la potenza di Aspose.Note per Java nell'estrazione delle attività di Outlook da OneNote senza sforzo. Segui la nostra guida passo passo e migliora le tue capacità di elaborazione dei documenti.
type: docs
weight: 10
url: /it/java/task-and-outlook-integration/get-outlook-task/
---
## introduzione
Benvenuti nella nostra guida completa sull'utilizzo di Aspose.Note per Java per recuperare facilmente le attività di Outlook in OneNote. Aspose.Note è una potente API Java che consente agli sviluppatori di lavorare con i file Microsoft OneNote senza sforzo. In questo tutorial ti guideremo passo passo attraverso il processo di estrazione delle attività di Outlook da un documento OneNote.
## Prerequisiti
Prima di immergerci nel tutorial, assicurati di disporre dei seguenti prerequisiti:
- Ambiente di sviluppo Java: assicurati di avere un ambiente di sviluppo Java configurato sul tuo computer.
-  Libreria Aspose.Note: scarica e installa la libreria Aspose.Note per Java. Puoi trovare la biblioteca[Qui](https://releases.aspose.com/note/java/).
## Importa pacchetti
Per iniziare, importa i pacchetti necessari nel tuo progetto Java. Aggiungi le seguenti righe al tuo codice:
```java
import java.io.IOException;
import java.util.List;
import com.aspose.note.Document;
import com.aspose.note.ITag;
import com.aspose.note.NoteTask;
import com.aspose.note.RichText;

```
Ora suddividiamo il processo in passaggi gestibili:
## Passaggio 1: configura la directory dei documenti
Definisci la directory in cui si trova il tuo documento OneNote:
```java
String dataDir = "Your Document Directory";
```
## Passaggio 2: caricare il documento OneNote
Carica il documento OneNote utilizzando Aspose.Note:
```java
Document doc = new Document(dataDir + "Sample1.one");
```
## Passaggio 3: ottieni tutti i nodi RichText
Recupera tutti i nodi RichText dal documento:
```java
List<RichText> nodes = (List<RichText>) doc.getChildNodes(RichText.class);
```
## Passaggio 4: scorrere ciascun nodo
Scorri ogni nodo RichText e controlla i tag NoteTask:
```java
for (RichText richText : nodes) {
    for (ITag tag : richText.getTags()) {
        if (tag.getClass() == NoteTask.class) {
            NoteTask noteTask = (NoteTask) tag;
            
            // Recuperare le proprietà
            System.out.println("Completed Time: " + noteTask.getCompletedTime());
            System.out.println("Create Time: " + noteTask.getCreationTime());
            System.out.println("Due Date: " + noteTask.getDueDate());
            System.out.println("Status: " + noteTask.getStatus());
            System.out.println("Icon: " + noteTask.getIcon());
        }
    }
}
```
## Conclusione
Congratulazioni! Hai imparato con successo come utilizzare Aspose.Note per Java per recuperare le attività di Outlook in OneNote. Questa potente API semplifica il processo, rendendolo efficiente e intuitivo per gli sviluppatori.
## Domande frequenti
### Aspose.Note è compatibile con tutte le versioni di OneNote?
Aspose.Note supporta Microsoft OneNote 2010 e versioni successive.
### Posso utilizzare Aspose.Note sia per progetti personali che commerciali?
 Sì, Aspose.Note può essere utilizzato sia per progetti personali che commerciali. Visita[Qui](https://purchase.aspose.com/buy) per esplorare le opzioni di licenza.
### È disponibile una prova gratuita per Aspose.Note?
 Sì, puoi accedere alla prova gratuita[Qui](https://releases.aspose.com/).
### Come posso ottenere supporto per Aspose.Note?
 Visitare il[Aspose.Note Forum](https://forum.aspose.com/c/note/28) per il sostegno della comunità. Per ulteriore assistenza, considera l'acquisto di a[licenza temporanea](https://purchase.aspose.com/temporary-license/).
### Sono disponibili documenti OneNote di esempio per il test?
 È possibile trovare documenti di esempio nella documentazione Aspose.Note[Qui](https://reference.aspose.com/note/java/).