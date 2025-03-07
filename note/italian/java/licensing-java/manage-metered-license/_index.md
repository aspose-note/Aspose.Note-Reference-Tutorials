---
title: Gestisci la licenza a consumo per OneNote in Java
linktitle: Gestisci la licenza a consumo per OneNote in Java
second_title: Aspose.Note API Java
description: Scopri come gestire le licenze a consumo per OneNote in Java utilizzando la libreria Aspose.Note. Controlla l'utilizzo, monitora i crediti e ottimizza i costi in modo efficiente.
weight: 10
url: /it/java/licensing-java/manage-metered-license/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Gestisci la licenza a consumo per OneNote in Java

## introduzione

In questo tutorial impareremo come gestire una licenza a consumo per OneNote utilizzando Aspose.Note per Java. La licenza misurata ti consente di monitorare e controllare il tuo utilizzo in base ai crediti, fornendo una soluzione flessibile ed economica.

## Prerequisiti

Prima di iniziare, assicurati di possedere i seguenti prerequisiti:

1.  Java Development Kit (JDK): assicurati di avere JDK installato sul tuo sistema. Puoi scaricarlo da[Qui](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).
   
2. Aspose.Note per la libreria Java: è necessario disporre della libreria Aspose.Note per Java. Puoi scaricarlo da[sito web](https://releases.aspose.com/note/java/).

## Importa pacchetti

Innanzitutto, importa i pacchetti necessari nel tuo progetto Java:

```java
import com.aspose.note.Document;
import com.aspose.note.Metered;



import java.nio.file.Paths;
```

## Passaggio 1: imposta la licenza a consumo

```java
Metered metered = new Metered();
metered.setMeteredKey("MyPublicKey", "MyPrivateKey");
```

 In questo passaggio inizializziamo il file`Metered` class e impostare la chiave misurata con le chiavi pubbliche e private fornite da Aspose.

## Passaggio 2: caricare il documento ed eseguire le operazioni

```java
String dataDir = "Your Document Directory";
Document doc = new Document(Paths.get(dataDir,"Sample1.one").toString());
doc.save(Paths.get(dataDir,"MeteredLicense.pdf").toString());
```

 Qui carichiamo il documento OneNote dalla directory specificata e lo salviamo come file PDF. Assicurarsi di sostituire`"Your Document Directory"` con il percorso effettivo della directory.

## Passaggio 3: verificare il consumo

```java
System.out.println(String.format("Credit before operation: %.02f", Metered.getConsumptionCredit()));
System.out.println(String.format("Consumption quantity before operation: %.02f", Metered.getConsumptionQuantity()));
```

Questo passaggio recupera e stampa la quantità di credito e consumo prima e dopo l'operazione.

## Conclusione

In questo tutorial abbiamo imparato come gestire una licenza a consumo per OneNote in Java utilizzando la libreria Aspose.Note. Le licenze a consumo offrono flessibilità e controllo sull'utilizzo, garantendo efficienza in termini di costi e gestione efficiente delle risorse.

## Domande frequenti

### Q1: Cos'è una licenza a consumo?

R1: Una licenza misurata consente di monitorare e controllare l'utilizzo di un'API o di un servizio in base ai crediti.
   
### Q2: Come posso ottenere una chiave misurata per i prodotti Aspose?

R2: È possibile ottenere una chiave misurata acquistando una licenza dal sito Web Aspose o richiedendo una licenza temporanea a scopo di valutazione.
   
### D3: Posso utilizzare una licenza a consumo per più applicazioni?

R3: Sì, una licenza a consumo può essere utilizzata per più applicazioni, ma il consumo verrà aggregato.
   
### Q4: È disponibile una prova gratuita per Aspose.Note per Java?

 R4: Sì, puoi scaricare una versione di prova gratuita da[Qui](https://releases.aspose.com/).
   
### Q5: Dove posso ottenere supporto per Aspose.Note per Java?

 R5: Puoi ottenere supporto dai forum della community Aspose[Qui](https://forum.aspose.com/c/note/28).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
