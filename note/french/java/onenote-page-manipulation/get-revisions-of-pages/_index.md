---
title: Obtenir les révisions des pages dans OneNote - Aspose.Note
linktitle: Obtenir les révisions des pages dans OneNote - Aspose.Note
second_title: API Java Aspose.Note
description: Découvrez comment récupérer les révisions de pages dans des documents OneNote à l'aide d'Aspose.Note Java. Intégrez-le dans vos applications Java pour une gestion efficace des documents.
weight: 15
url: /fr/java/onenote-page-manipulation/get-revisions-of-pages/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Obtenir les révisions des pages dans OneNote - Aspose.Note

## Introduction

Dans ce didacticiel, nous examinerons les capacités d'Aspose.Note pour Java, une bibliothèque puissante qui vous permet de travailler de manière transparente avec les fichiers Microsoft OneNote dans vos applications Java. Plus précisément, nous nous concentrerons sur la façon de récupérer les révisions de pages dans un document OneNote. À la fin de ce guide, vous disposerez des connaissances nécessaires pour extraire efficacement les révisions de pages, y compris des détails tels que l'heure de la dernière modification, l'heure de création, le titre, le niveau et l'auteur.

## Conditions préalables

Avant de plonger dans ce didacticiel, assurez-vous d'avoir configuré les conditions préalables suivantes :

### Kit de développement Java (JDK) installé

Assurez-vous que le kit de développement Java est installé sur votre système. Vous pouvez le télécharger et l'installer à partir du site Web d'Oracle ou utiliser un gestionnaire de packages si vous utilisez un système Unix.

### Aspose.Note pour la bibliothèque Java

 Téléchargez et installez la bibliothèque Aspose.Note pour Java à partir du site Web. Vous pouvez trouver le lien de téléchargement[ici](https://releases.aspose.com/note/java/) . Suivez les instructions d'installation fournies dans la documentation[ici](https://reference.aspose.com/note/java/).

## Importer des packages

Pour commencer, importez les packages nécessaires dans votre projet Java. Ces packages vous permettront d'exploiter les fonctionnalités fournies par Aspose.Note pour Java.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.PageHistory;
```

Maintenant, décomposons l'exemple de code fourni en plusieurs étapes pour comprendre chaque composant et ses fonctionnalités.

## Étape 1 : Définir le répertoire des documents

Définissez le répertoire dans lequel se trouve votre document OneNote.

```java
String dataDir = "Your Document Directory";
```

## Étape 2 : Charger le document

Chargez le document OneNote dans Aspose.Note.

```java
Document doc = new Document(dataDir + "Sample1.one");
```

## Étape 3 : Obtenir la première page

Récupérez la première page du document.

```java
Page firstPage = doc.getFirstChild();
```

## Étape 4 : Obtenir les révisions de page

Obtenez l’historique des révisions de la page.

```java
PageHistory revisions = doc.getPageHistory(firstPage);
```

## Étape 5 : Parcourir les révisions de la page

Parcourez la liste des révisions de page et récupérez les informations pertinentes.

```java
for (Page pageRevision : revisions) {
    System.out.println("LastModifiedTime: " + pageRevision.getLastModifiedTime());
    System.out.println("CreationTime: " + pageRevision.getCreationTime());
    System.out.println("Title: " + pageRevision.getTitle());
    System.out.println("Level: " + pageRevision.getLevel());
    System.out.println("Author: " + pageRevision.getAuthor());
    System.out.println();
}
```

## Conclusion

Dans ce didacticiel, nous avons expliqué comment récupérer les révisions de pages dans un document OneNote à l'aide d'Aspose.Note pour Java. En suivant le guide étape par étape et en tirant parti de l'exemple de code fourni, vous pouvez facilement intégrer cette fonctionnalité dans vos applications Java, permettant ainsi une gestion efficace des fichiers OneNote.

## FAQ

### Q1 : Puis-je utiliser Aspose.Note pour Java pour créer de nouveaux documents OneNote ?

A1 : Oui, Aspose.Note pour Java offre une prise en charge complète pour la création, la lecture et la manipulation de documents OneNote par programme.

### Q2 : Aspose.Note pour Java est-il compatible avec différentes versions de fichiers OneNote ?

A2 : Oui, Aspose.Note pour Java prend en charge différentes versions de fichiers Microsoft OneNote, garantissant ainsi la compatibilité entre différents environnements.

### Q3 : Puis-je personnaliser le format de sortie lors de l’exportation de documents OneNote ?

A3 : Absolument, Aspose.Note pour Java offre une flexibilité dans l'exportation de documents OneNote vers différents formats tels que PDF, HTML et images, avec des options de personnalisation.

### Q4 : Aspose.Note pour Java nécessite-t-il une licence pour un usage commercial ?

A4 : Oui, une licence valide est requise pour une utilisation commerciale d'Aspose.Note pour Java. Vous pouvez obtenir une licence sur le site Web Aspose.

### Q5 : Où puis-je demander de l'aide si je rencontre des problèmes ou si j'ai des questions sur Aspose.Note pour Java ?

 A5 : Pour obtenir de l'aide et de l'assistance, vous pouvez visiter le forum Aspose.Note[ici](https://forum.aspose.com/c/note/28)où vous pouvez poser des questions, partager des expériences et interagir avec d'autres utilisateurs et experts.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
