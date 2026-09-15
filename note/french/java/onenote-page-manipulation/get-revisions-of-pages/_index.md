---
date: 2026-01-10
description: Apprenez comment obtenir la date de dernière modification et récupérer
  les révisions des pages OneNote à l’aide d’Aspose.Note pour Java. Intégrez cela
  dans vos applications Java pour une gestion efficace des documents.
linktitle: Get Revisions of Pages in OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: Comment obtenir la date de dernière modification des pages OneNote – Aspose.Note
url: /fr/java/onenote-page-manipulation/get-revisions-of-pages/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Obtenir les révisions des pages dans OneNote - Aspose.Note

## Introduction

Dans ce tutoriel, vous **obtiendrez l'heure de la dernière modification** des pages d'un document OneNote et explorerez comment récupérer l'historique complet des révisions à l'aide d'Aspose.Note pour Java. Que vous construisiez un système de gestion de documents, audité des changements, ou simplement ayez besoin d'afficher la date de la dernière édition d'une page, ce guide vous montre exactement comment extraire ces informations programmatiquement.

## Quick Answers
- **Que renvoie “get last modified time” ?** Le timestamp de la modification la plus récente sur une page OneNote.  
- **Quelle classe fournit l'historique des révisions ?** `PageHistory` via `Document.getPageHistory(Page)`.  
- **Ai-je besoin d'une licence pour cette fonctionnalité ?** Oui, une licence valide Aspose.Note est requise pour une utilisation en production.  
- **Quelle version de Java est prise en charge ?** Java 8 ou supérieure (JDK 8+).  
- **Puis-je filtrer les révisions par auteur ?** Vous pouvez lire la propriété `Author` de chaque objet `Page` et appliquer votre propre filtre.

## Qu'est-ce que “get last modified time” dans OneNote ?

Le **last modified time** est un champ de métadonnées stocké avec chaque page qui enregistre quand la page a été modifiée pour la dernière fois. Aspose.Note expose cette valeur via la méthode `Page.getLastModifiedTime()`, ce qui facilite l'affichage ou l'enregistrement des dates de changement.

## Pourquoi récupérer les révisions de page ?

- **Traçabilité :** Conservez un enregistrement de qui a changé quoi et quand.  
- **Comparaison de versions :** Créez des fonctionnalités qui comparent deux révisions côte à côte.  
- **Analyse de la collaboration des utilisateurs :** Comprenez les schémas d'édition dans les blocs‑notes partagés.  

## Prérequis

Avant de commencer, assurez‑vous de disposer de ce qui suit :

### Java Development Kit (JDK) installé
Installez JDK 8 ou une version ultérieure depuis le site d'Oracle ou votre gestionnaire de paquets préféré.

### Bibliothèque Aspose.Note pour Java
Téléchargez la bibliothèque depuis le site officiel. Vous pouvez trouver le lien de téléchargement **[ici](https://releases.aspose.com/note/java/)**. Suivez les instructions d'installation dans la documentation **[ici](https://reference.aspose.com/note/java/)**.

## Import Packages

Pour commencer, importez les packages nécessaires dans votre projet Java. Ces packages vous permettront d'exploiter les fonctionnalités fournies par Aspose.Note pour Java.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.PageHistory;
```

Maintenant, décomposons le code d'exemple fourni en plusieurs étapes afin de comprendre chaque composant et son fonctionnement.

## How to Get Last Modified Time of a OneNote Page

### Étape 1 : Définir le répertoire du document
Définissez le répertoire où se trouve votre document OneNote.

```java
String dataDir = "Your Document Directory";
```

### Étape 2 : Charger le document
Chargez le document OneNote dans Aspose.Note.

```java
Document doc = new Document(dataDir + "Sample1.one");
```

### Étape 3 : Obtenir la première page
Récupérez la première page du document.

```java
Page firstPage = doc.getFirstChild();
```

### Étape 4 : Obtenir les révisions de la page
Obtenez l'historique des révisions de la page.

```java
PageHistory revisions = doc.getPageHistory(firstPage);
```

### Étape 5 : Parcourir les révisions de la page
Itérez sur la liste des révisions de la page et récupérez les informations pertinentes, y compris le **last modified time**.

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

## Common Issues and Solutions
- **Null `PageHistory` :** Assurez‑vous que le document contient réellement des révisions ; sinon `getPageHistory` peut renvoyer `null`.  
- **Différences de fuseau horaire** : `getLastModifiedTime()` renvoie un `java.util.Date` dans le fuseau horaire par défaut du système. Convertissez en UTC si nécessaire.  
- **Licence non chargée** : Sans licence valide, Aspose.Note peut fonctionner en mode d'évaluation, limitant le nombre de pages traitées.

## Frequently Asked Questions

### Q1 : Puis‑je utiliser Aspose.Note pour Java afin de créer de nouveaux documents OneNote ?
A1 : Oui, Aspose.Note pour Java offre un support complet pour créer, lire et manipuler des documents OneNote programmatiquement.

### Q2 : Aspose.Note pour Java est‑il compatible avec différentes versions de fichiers OneNote ?
A2 : Oui, Aspose.Note pour Java prend en charge diverses versions des fichiers Microsoft OneNote, garantissant la compatibilité sur différents environnements.

### Q3 : Puis‑je personnaliser le format de sortie lors de l'exportation de documents OneNote ?
A3 : Absolument, Aspose.Note pour Java offre une flexibilité d'exportation des documents OneNote vers différents formats tels que PDF, HTML et images, avec des options de personnalisation.

### Q4 : Aspose.Note pour Java nécessite‑t‑il une licence pour une utilisation commerciale ?
A4 : Oui, une licence valide est requise pour une utilisation commerciale d'Aspose.Note pour Java. Vous pouvez obtenir une licence sur le site Aspose.

### Q5 : Où puis‑je obtenir de l'aide si je rencontre des problèmes ou ai des questions sur Aspose.Note pour Java ?
A5 : Pour le support et l'assistance, vous pouvez visiter le forum Aspose.Note **[ici](https://forum.aspose.com/c/note/28)**, où vous pouvez poser des questions, partager des expériences et interagir avec d'autres utilisateurs et experts.

---

**Last Updated:** 2026-01-10  
**Tested With:** Aspose.Note for Java 23.12 (latest at time of writing)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}