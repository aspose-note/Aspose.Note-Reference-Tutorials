---
date: 2025-11-29
description: Impara come verificare la crittografia di OneNote in Java usando Aspose.Note
  per Java. Questa guida ti mostra come rilevare i file OneNote crittografati prima
  dell'elaborazione.
language: it
linktitle: Check if OneNote Document is Encrypted - Java
second_title: Aspose.Note Java API
title: Controlla la crittografia di OneNote in Java – Verifica la crittografia del
  documento OneNote
url: /java/onenote-document-loading/check-document-encrypted/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}  
{{< blocks/products/pf/main-container >}}  
{{< blocks/products/pf/tutorial-page-section >}}  

# Verifica se il documento OneNote è crittografato - Java  

## Introduzione  

Quando lavori con file OneNote in un'applicazione Java, la prima cosa da sapere è **se il documento è crittografato**. Tentare di caricare un file crittografato senza la password corretta genera errori e interrompe il flusso di lavoro. In questo tutorial ti mostreremo **come verificare la crittografia di OneNote in Java** con Aspose.Note per Java, così potrai decidere in modo sicuro se chiedere all'utente una password o continuare l'elaborazione del file.  

## Risposte rapide  

- **Quale metodo determina la crittografia?** `Document.isEncrypted`  
- **È necessaria una password per verificare?** No, è possibile interrogare lo stato senza password.  
- **Quale versione dell'API funziona?** Qualsiasi versione recente di Aspose.Note per Java (testata con 24.11).  
- **Posso verificare sia flussi che percorsi file?** Sì – l'API supporta entrambi.  
- **Cosa succede se la password è errata?** Il metodo restituisce `true`, indicando che il file rimane crittografato.  

## Cos'è la verifica della crittografia di OneNote in Java?  

`check onenote encryption java` è il processo di verifica programmatica se un file OneNote (`.one`) è protetto da password prima di tentare di caricarne il contenuto. Conoscere lo stato di crittografia ti aiuta a evitare eccezioni a runtime e a migliorare l'esperienza dell'utente.  

## Perché verificare la crittografia di OneNote prima del caricamento?  

- **Prevenire errori a runtime** – il caricamento di un file crittografato senza password genera un'eccezione.  
- **Migliorare il flusso UI** – puoi chiedere all'utente la password solo quando necessario.  
- **Conformità di sicurezza** – garantisce che tu gestisca i contenuti protetti secondo le policy.  

## Prerequisiti  

1. **Java Development Kit (JDK)** – assicurati di avere Java 11 o versioni successive installate. Scaricalo da [qui](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).  
2. **Aspose.Note per Java** – ottieni la libreria dalla pagina di download ufficiale [qui](https://releases.aspose.com/note/java/).  

## Importare i pacchetti  

Per iniziare, aggiungi gli import necessari al tuo progetto Java:  

```java
import com.aspose.note.Document;
import com.aspose.note.LoadOptions;
import java.io.FileInputStream;
import java.io.IOException;
import java.nio.file.Paths;
```  

## Come verificare la crittografia di OneNote in Java  

Di seguito suddividiamo la soluzione in due scenari pratici: verificare un documento caricato da uno **stream** e verificare un documento caricato direttamente da un **percorso file**.  

### Passo 1: Verificare se un documento caricato da uno stream è crittografato  

```java
public static void CheckIfDocumentFromStreamIsEncrypted() throws IOException {
    // ExStart:CheckIfDocumentFromStreamIsEncrypted
    String dataDir = "Your Document Directory";

    LoadOptions loadOptions = new LoadOptions();
    loadOptions.setDocumentPassword("password");

    FileInputStream stream = new FileInputStream(Paths.get(dataDir, "Sample1.one").toString());

    try {
        Document ref[] = { null };
        if (!Document.isEncrypted(stream, loadOptions, ref)) {
            System.out.println("The document is loaded and ready to be processed.");
        } else {
            System.out.println("The document is encrypted. Provide a password.");
        }
    } finally {
        stream.close();
    }
    // ExEnd:CheckIfDocumentFromStreamIsEncrypted
}
```  

**Spiegazione**  

- `LoadOptions` ti consente di fornire facoltativamente una password (`setDocumentPassword`).  
- `Document.isEncrypted(stream, loadOptions, ref)` verifica lo stato di crittografia dello stream.  
- L'array `ref` riceve un riferimento al `Document` caricato quando il file **non** è crittografato, permettendoti di continuare l'elaborazione senza una seconda chiamata di caricamento.  

### Passo 2: Verificare se un documento caricato da un percorso file è crittografato  

```java
public static void CheckIfDocumentFromFileIsEncrypted() throws IOException {
    // ExStart:CheckIfDocumentFromFileIsEncrypted
    String dataDir = "Your Document Directory";

    Document ref[] = { null };
    if (!Document.isEncrypted(Paths.get(dataDir, "Sample1.one").toString(), "VerySecretPassword", ref)) {
        if (ref[0] != null) {
            System.out.println("The document is decrypted. It is loaded and ready to be processed.");
        } else {
            System.out.println("The document is encrypted. Invalid password was provided.");
        }
    } else {
        System.out.println("The document is NOT encrypted. It is loaded and ready to be processed.");
    }
    // ExEnd:CheckIfDocumentFromFileIsEncrypted
}
```  

**Spiegazione**  

- Questa overload funziona direttamente con un percorso file e una stringa password.  
- Se il file **non** è crittografato, `isEncrypted` restituisce `false` e il riferimento `ref[0]` contiene il documento caricato.  
- Se la password è errata, il metodo restituisce comunque `true`, indicando che il file rimane crittografato.  

## Problemi comuni e consigli  

- **Non inserire mai password in chiaro** nel codice di produzione; recuperale in modo sicuro (ad es., da un vault).  
- Chiudi sempre gli stream in un blocco `finally` o utilizza il try‑with‑resources per evitare perdite di risorse.  
- Se ricevi `true` da `isEncrypted` e `ref[0]` è `null`, il file è crittografato **o** la password fornita è errata. Chiedi all'utente la password corretta e riprova.  

## Domande frequenti  

**D: Posso verificare lo stato di crittografia senza fornire una password?**  
R: Sì. Chiama `Document.isEncrypted` con un'istanza di `LoadOptions` che non imposta una password; il metodo segnalerà semplicemente se il file è crittografato.  

**D: Cosa succede se fornisco una password errata?**  
R: Il metodo restituisce `true`, indicando che il documento è ancora crittografato, e `ref[0]` sarà `null`.  

**D: Esiste un modo per decrittografare il documento programmaticamente?**  
R: Sì. Una volta conosciuta la password corretta, passala a `LoadOptions` (o all'overload che accetta una password) e carica il documento; l'API lo decritterà al volo.  

**D: Aspose.Note funziona con altri formati Microsoft?**  
R: Aspose.Note è progettato esclusivamente per file OneNote (`.one`). Per altri formati Office, considera Aspose.Words, Aspose.Cells, ecc.  

**D: Dove posso trovare altri esempi e supporto?**  
R: Visita il [forum Aspose.Note](https://forum.aspose.com/c/note/28) per assistenza della community e consulta la documentazione ufficiale per ulteriori esempi di codice.  

## Conclusione  

In questa guida abbiamo mostrato **come verificare la crittografia di OneNote in Java** usando Aspose.Note per Java, coprendo sia scenari basati su stream sia basati su file. Integrando questi controlli nella tua applicazione potrai gestire elegantemente i file OneNote crittografati, migliorare l'esperienza utente e mantenere robusto il tuo flusso di elaborazione.  

---  

**Ultimo aggiornamento:** 2025-11-29  
**Testato con:** Aspose.Note 24.11 per Java  
**Autore:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}  

{{< /blocks/products/pf/main-container >}}  
{{< /blocks/products/pf/main-wrap-class >}}  

{{< blocks/products/products-backtop-button >}}