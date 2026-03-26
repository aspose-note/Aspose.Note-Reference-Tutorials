---
date: 2026-01-15
description: Apprenez à suivre les modifications dans OneNote et à gérer les révisions
  de pages dans les documents OneNote à l’aide d’Aspose.Note pour Java. Comprend un
  exemple de résumé des révisions et comment modifier la date de révision.
linktitle: Working with Page Revisions in OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: Suivi des modifications OneNote – Gérer les révisions de pages avec Aspose.Note
url: /fr/java/onenote-page-manipulation/working-with-page-revisions/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Gestion des révisions de page dans OneNote - Aspose.Note

## Introduction

OneNote est un outil puissant pour organiser des notes, et lorsque vous devez **track changes onenote**, la gestion des révisions de page devient essentielle pour une collaboration efficace. Avec Aspose.Note for Java, vous pouvez gérer les révisions de façon programmatique, voir qui a modifié une page, et même ajuster les horodatages. Ce tutoriel vous guide à travers chaque étape, du chargement d'un document à la mise à jour du résumé de révision.

## Réponses rapides
- **Que signifie “track changes onenote” ?** Il s'agit de surveiller qui a modifié une page OneNote et quand.
- **Quelle bibliothèque est requise ?** Aspose.Note for Java.
- **Puis-je modifier l'auteur ou la date d'une révision ?** Oui, en utilisant l'API RevisionSummary (`modify revision date`).
- **Ai-je besoin d'un fichier OneNote au préalable ?** Oui, un fichier d'exemple `.one` est requis.
- **Une licence est‑elle nécessaire pour la production ?** Une licence Aspose.Note valide est requise pour une utilisation commerciale.

## Quel est un exemple de résumé de révision ?

Un *revision summary* fournit des métadonnées sur les modifications les plus récentes d'une page — nom de l'auteur, date de dernière modification et autres détails. Dans ce guide, nous récupérerons et afficherons ces informations, puis montrerons comment **modify revision date**.

## Pourquoi suivre les modifications onenote avec Aspose.Note ?

- **Collaboration :** Voir rapidement qui a effectué les dernières modifications.
- **Audit :** Conserver un historique fiable des modifications pour la conformité.
- **Automatisation :** Intégrer la gestion des révisions dans les services back‑end ou les outils de migration.

## Prérequis

### Environnement de développement Java
Assurez‑vous d'avoir le Java Development Kit (JDK) installé sur votre système.

### Bibliothèque Aspose.Note pour Java
Téléchargez et installez la bibliothèque Aspose.Note pour Java depuis [here](https://releases.aspose.com/note/java/).

### Document OneNote
Préparez un document OneNote d'exemple prêt pour les tests.

## Importer les packages

Dans votre projet Java, importez les packages nécessaires pour travailler avec Aspose.Note pour Java.

```java
import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.RevisionSummary;
import java.io.IOException;
import java.util.Calendar;
```

Décomposons l'exemple fourni en plusieurs étapes pour une compréhension claire.

## Étape 1 : Charger le document OneNote

Tout d'abord, chargez le document OneNote et récupérez la première page enfant.

```java
String dataDir = "Your Document Directory";
Document document = new Document(dataDir + "Sample1.one");
Page page = document.getFirstChild();
```

## Étape 2 : Lire le résumé de révision de la page

Lisez le résumé de révision du contenu pour la page. Il s'agit de l'**revision summary example** qui indique qui a modifié la page en dernier.

```java
RevisionSummary pageRevisionInfo = page.getPageContentRevisionSummary();
System.out.println(String.format("Author:\t%s\nModified:\t%s",
        pageRevisionInfo.getAuthorMostRecent(),
        pageRevisionInfo.getLastModifiedTime().toString()));
```

## Étape 3 : Mettre à jour le résumé de révision de la page

Mettez à jour le résumé de révision de la page avec un nouvel auteur et une nouvelle date de modification. Cela montre comment **modify revision date** de façon programmatique.

```java
pageRevisionInfo.setAuthorMostRecent("New Author");
Calendar modifiedDate = Calendar.getInstance();
pageRevisionInfo.setLastModifiedTime(modifiedDate.getTime());
document.save(dataDir + "WorkingWithPageRevisions_out.one");
```

## Conclusion

La gestion programmatique des révisions de page dans les documents OneNote peut être simplifiée avec Aspose.Note pour Java. En suivant les étapes décrites dans ce tutoriel, vous pouvez efficacement **track changes onenote**, consulter les détails des révisions, et même **modify revision date** pour répondre à votre flux de travail.

## FAQ

### Q1 : Puis‑je utiliser Aspose.Note pour Java avec d'autres bibliothèques Java ?
R : Oui, Aspose.Note pour Java peut être intégré à d'autres bibliothèques Java pour améliorer les fonctionnalités.

### Q2 : Aspose.Note pour Java prend‑il en charge toutes les versions de documents OneNote ?
R : Aspose.Note pour Java prend en charge diverses versions de documents OneNote, y compris les versions plus anciennes.

### Q3 : Aspose.Note pour Java convient‑il aux applications de niveau entreprise ?
R : Absolument, Aspose.Note pour Java est conçu pour répondre aux besoins des applications de niveau entreprise avec des fonctionnalités robustes et une grande évolutivité.

### Q4 : Puis‑je personnaliser les révisions de page avec Aspose.Note pour Java ?
R : Oui, vous pouvez personnaliser les révisions de page selon vos besoins en utilisant Aspose.Note pour Java.

### Q5 : Où puis‑je obtenir du support pour Aspose.Note pour Java ?
R : Vous pouvez obtenir du support pour Aspose.Note pour Java sur le [Aspose.Note forum](https://forum.aspose.com/c/note/28).

---

**Last Updated:** 2026-01-15  
**Tested With:** Aspose.Note for Java 24.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}