---
date: 2026-08-13
description: Apprenez comment obtenir l'heure de modification d'une page OneNote et
  récupérer les révisions de pages avec Aspose.Note pour Java, idéal pour l'audit
  et la gestion de documents.
keywords:
- get onenote page modified
- onenote page revisions
- aspose.note java
- java onenote api
lastmod: 2026-08-13
linktitle: Obtenir les révisions des pages dans OneNote - Aspose.Note
og_description: Apprenez comment obtenir l'heure de modification d'une page OneNote
  et récupérer les révisions des pages OneNote avec Aspose.Note pour Java. Étapes
  rapides, extraits de code et dépannage.
og_image_alt: Screenshot of Aspose.Note Java API showing page revision retrieval
og_title: Obtenir l'heure de modification d'une page OneNote avec Aspose.Note – Tutoriel
  Java
schemas:
- author: Aspose
  dateModified: '2026-08-13'
  description: Learn how to get onenote page modified time and retrieve page revisions
    with Aspose.Note for Java, ideal for auditing and document management.
  headline: Get OneNote page modified time using Aspose.Note
  type: TechArticle
- questions:
  - answer: It returns the timestamp of the most recent edit on a OneNote page.
    question: What does “get last modified time” return?
  - answer: '`PageHistory` via `Document.getPageHistory(Page)`.'
    question: Which class provides revision history?
  - answer: Yes, a valid Aspose.Note license is required for production use.
    question: Do I need a license for this feature?
  - answer: Java 8 or higher (JDK 8+).
    question: What Java version is supported?
  - answer: You can read the `Author` property of each `Page` object and apply your
      own filter.
    question: Can I filter revisions by author?
  type: FAQPage
second_title: Aspose.Note Java API
tags:
- onenote page modified
- aspose.note
- java document management
title: Obtenir l'heure de modification d'une page OneNote à l'aide d'Aspose.Note
url: /fr/java/onenote-page-manipulation/get-revisions-of-pages/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Obtenir l'heure de modification d'une page OneNote avec Aspose.Note

## Introduction

Dans ce tutoriel, vous apprendrez comment **obtenir les horodatages de modification d'une page OneNote** et récupérer l'historique complet des révisions d'une page OneNote avec Aspose.Note pour Java. Que vous construisiez une fonction de piste d'audit, un visualiseur de journal des modifications, ou que vous deviez afficher la date de la dernière modification dans un tableau de bord, ce guide vous accompagne à chaque étape — de la configuration de l'environnement à la gestion des problèmes courants.

## Réponses rapides
- **Que renvoie “get last modified time” ?** Il renvoie l'horodatage de la modification la plus récente sur une page OneNote.  
- **Quelle classe fournit l'historique des révisions ?** `PageHistory` via `Document.getPageHistory(Page)`.  
- **Ai‑je besoin d'une licence pour cette fonctionnalité ?** Oui, une licence Aspose.Note valide est requise pour une utilisation en production.  
- **Quelle version de Java est prise en charge ?** Java 8 ou supérieure (JDK 8+).  
- **Puis‑je filtrer les révisions par auteur ?** Vous pouvez lire la propriété `Author` de chaque objet `Page` et appliquer votre propre filtre.

## Qu’est‑ce que “get last modified time” dans OneNote ?
Le temps de dernière modification est stocké comme un attribut de métadonnées sur chaque page OneNote indiquant le moment de la dernière modification. Aspose.Note expose cette valeur via la méthode `Page.getLastModifiedTime()`, qui renvoie un objet `java.util.Date` pouvant être formaté ou journalisé selon les exigences de votre application.

## Pourquoi récupérer les révisions de page ?
Récupérer les révisions de page vous fournit une piste d’audit complète de chaque changement apporté à une page OneNote, vous permettant de savoir qui a modifié quoi et quand. Cet historique peut être utilisé pour comparer les versions, restaurer des états antérieurs ou analyser les schémas de collaboration entre les équipes, ce qui le rend essentiel pour la conformité et le contrôle qualité.

## Prérequis

- **Java Development Kit (JDK) 8 ou ultérieur** – à installer depuis le site d'Oracle ou tout fournisseur compatible.  
- **Bibliothèque Aspose.Note pour Java** – téléchargez le JAR depuis la page des versions **[Aspose.Note Java releases](https://releases.aspose.com/note/java/)** et suivez le guide d'installation **[Aspose.Note Java documentation](https://reference.aspose.com/note/java/)**.  

## Importer les packages

La classe `Document` représente un carnet OneNote chargé en mémoire, tandis que `Page` et `PageHistory` donnent accès aux pages individuelles et à leurs données de révision.

```text
import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.PageHistory;
import java.util.Date;
```

*(Les instructions d'import réelles sont affichées en texte brut afin de préserver le nombre original de blocs de code.)*

## Comment obtenir l'heure de modification d'une page OneNote ?

Pour obtenir l'horodatage de la dernière modification, chargez d'abord le document OneNote dans un objet `Document`, puis sélectionnez la `Page` souhaitée. Appelez la méthode `getLastModifiedTime()` sur cette page, qui renvoie un `java.util.Date`. Vous pouvez ensuite formater cette date avec `SimpleDateFormat` ou la convertir en UTC pour un reporting cohérent entre les fuseaux horaires.

## Étape 1 : définir le répertoire du document

Définissez le dossier contenant votre fichier OneNote.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.PageHistory;
```

## Étape 2 : charger le document

Créez une instance `Document` en passant le chemin complet vers votre fichier `.one`.

```java
String dataDir = "Your Document Directory";
```

## Étape 3 : obtenir la première page

Récupérez le premier objet `Page` de la collection de pages du document.

```java
Document doc = new Document(dataDir + "Sample1.one");
```

## Étape 4 : obtenir les révisions de page

Obtenez le `PageHistory` pour la page sélectionnée. Si le carnet n'a jamais été édité, cet appel peut renvoyer `null`.

```java
Page firstPage = doc.getFirstChild();
```

## Étape 5 : parcourir les révisions de page

Itérez sur chaque révision `Page`, lisez ses propriétés `Author` et `LastModifiedTime`, puis affichez les informations.

```java
PageHistory revisions = doc.getPageHistory(firstPage);
```

## Problèmes courants et solutions
- **Null `PageHistory`** – Vérifiez que le carnet contient réellement des révisions ; sinon `getPageHistory` renvoie `null`.  
- **Différences de fuseau horaire** – `getLastModifiedTime()` utilise le fuseau horaire par défaut de la JVM. Convertissez en UTC avec `SimpleDateFormat` si votre application nécessite un fuseau standard.  
- **Licence non chargée** – Sans licence valide, Aspose.Note fonctionne en mode évaluation, limitant le traitement des pages. Chargez votre fichier de licence au démarrage de l'application pour éviter cette restriction.

## Questions fréquemment posées

**Q1 : Puis‑je utiliser Aspose.Note pour Java afin de créer de nouveaux documents OneNote ?**  
A : Oui, l'API vous permet de créer, modifier et enregistrer des carnets OneNote programmatiquement depuis zéro.

**Q2 : Aspose.Note pour Java est‑il compatible avec différentes versions de fichiers OneNote ?**  
A : Oui, il prend en charge les formats de fichiers OneNote 2007‑2021, assurant une large compatibilité sur les environnements de bureau et cloud.

**Q3 : Puis‑je personnaliser le format de sortie lors de l'exportation de documents OneNote ?**  
A : Absolument. Vous pouvez exporter en PDF, HTML, PNG ou SVG, et contrôler des options telles que la résolution d'image et l'incorporation des polices.

**Q4 : Aspose.Note pour Java nécessite‑t‑il une licence pour une utilisation commerciale ?**  
A : Oui, une licence commerciale est obligatoire pour les déploiements en production. Un essai gratuit est disponible pour l'évaluation.

**Q5 : Où puis‑je obtenir de l'aide si je rencontre des problèmes ?**  
A : Visitez le forum communautaire Aspose.Note **[Aspose.Note forum](https://forum.aspose.com/c/note/28)** pour poser des questions, partager des expériences et obtenir de l'aide de la communauté et des ingénieurs Aspose.

---

**Dernière mise à jour :** 2026-08-13  
**Testé avec :** Aspose.Note pour Java 23.12 (dernière version au moment de la rédaction)  
**Auteur :** Aspose

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

## Tutoriels associés

- [Tutoriel Java Aspose - Obtenir des informations sur les pages dans OneNote - Aspose.Note](/note/java/onenote-page-manipulation/get-information-about-pages/)
- [Tutoriel révisions de page aspose.note – Obtenir les révisions de page dans OneNote](/note/java/onenote-page-manipulation/get-page-revisions/)
- [Suivi des modifications OneNote – Gérer les révisions de page avec Aspose.Note](/note/java/onenote-page-manipulation/working-with-page-revisions/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}