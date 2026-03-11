---
date: 2026-01-10
description: Apprenez le tutoriel sur les révisions de pages Aspose.Note pour Java
  – récupérez les révisions de pages OneNote programmatiquement à l’aide d’Aspose.Note.
  Suivez notre guide étape par étape.
linktitle: Get Page Revisions in OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: Tutoriel des révisions de page aspose.note – Obtenir les révisions de page
  dans OneNote
url: /fr/java/onenote-page-manipulation/get-page-revisions/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Obtenir les révisions de page dans OneNote - Aspose.Note

OneNote est une plateforme de prise de notes puissante, et lorsque vous devez auditer les modifications, le **tutoriel de révisions de page aspose.note** vous montre exactement comment extraire l’historique des révisions avec seulement quelques lignes de code Java. Dans ce guide, nous passerons en revue tout ce dont vous avez besoin — de la configuration de l’environnement à l’affichage des détails de chaque révision — afin que vous puissiez suivre les modifications, les contributions des auteurs et les horodatages sans effort.

## Réponses rapides
- **Que couvre le tutoriel ?** Récupération de l’historique des révisions de page d’un fichier OneNote à l’aide d’Aspose.Note pour Java.  
- **Quelle version de la bibliothèque est requise ?** Toute version récente d’Aspose.Note pour Java qui prend en charge `LoadOptions.setLoadHistory`.  
- **Ai‑je besoin d’une licence ?** Une licence d’évaluation temporaire suffit pour les tests ; une licence commerciale est requise pour la production.  
- **Puis‑je modifier les révisions ?** L’API est en lecture‑seule pour les révisions ; vous ne pouvez que les récupérer.  
- **Quelles sont les principales prérequis ?** Java JDK, Aspose.Note pour Java, et un document OneNote contenant des données de révision.

## Qu’est‑ce que le “tutoriel de révisions de page aspose.note” ?
Le tutoriel montre comment accéder programmatiquement aux versions historiques d’une page OneNote. Chaque révision contient des métadonnées telles que l’auteur, la date de création et la date de modification, vous permettant de créer des pistes d’audit ou des fonctions de journal des changements dans vos applications.

## Pourquoi utiliser Aspose.Note pour le suivi des révisions de page ?
- **Pas de dépendance UI** – fonctionne entièrement en code, idéal pour les services back‑end.  
- **Cross‑platform** – Java s’exécute sous Windows, Linux et macOS.  
- **Contrôle total** – récupérez chaque propriété de révision sans ouvrir OneNote manuellement.  
- **Performance** – le chargement de l’historique est optimisé, même les gros blocs‑notes sont traités rapidement.

## Prérequis

### 1. Java Development Kit (JDK)
Assurez‑vous qu’un JDK récent (8 ou supérieur) est installé et que la variable `JAVA_HOME` est définie.

### 2. Aspose.Note pour Java
Téléchargez la bibliothèque depuis le [lien de téléchargement](https://releases.aspose.com/note/java/).

### 3. Document OneNote d’exemple
Créez ou obtenez un fichier OneNote (par ex. `Sample1.one`) contenant des pages avec un historique de révisions.

## Importer les packages
Tout d’abord, importez les classes Aspose.Note requises.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.LoadOptions;
import com.aspose.note.Page;
```

## Implémentation étape par étape

### Étape 1 : Configurer le répertoire du document
Définissez le dossier où se trouve votre fichier OneNote.

```java
String dataDir = "Your Document Directory";
```

### Étape 2 : Charger le document OneNote avec l’historique activé
Activez le drapeau `LoadOptions` pour extraire les données de révision.

```java
LoadOptions loadOptions = new LoadOptions();
loadOptions.setLoadHistory(true);
Document document = new Document(dataDir + "Sample1.one", loadOptions);
```

### Étape 3 : Obtenir la première page
Récupérez l’objet de la première page ; il servira de point de référence pour récupérer son historique.

```java
Page firstPage = document.getFirstChild();
```

### Étape 4 : Parcourir les révisions de page
Bouclez sur chaque révision et affichez les métadonnées utiles telles que les horodatages, le titre, le niveau et l’auteur.

```java
for (Page pageRevision : document.getPageHistory(firstPage)) {
    System.out.println("LastModifiedTime: " + pageRevision.getLastModifiedTime());
    System.out.println("CreationTime: " + pageRevision.getCreationTime());
    System.out.println("Title: " + pageRevision.getTitle());
    System.out.println("Level: " + pageRevision.getLevel());
    System.out.println("Author: " + pageRevision.getAuthor());
    System.out.println();
}
```

> **Astuce :** Si vous devez filtrer les révisions par un auteur spécifique ou une plage de dates, ajoutez simplement des vérifications conditionnelles à l’intérieur de la boucle `for`.

## Problèmes courants & solutions
- **Aucune révision renvoyée :** Vérifiez que `loadOptions.setLoadHistory(true)` est appelé avant le chargement du document.  
- **Auteur ou titre nul :** Certaines versions plus anciennes de OneNote peuvent ne pas stocker ces champs ; gérez les valeurs `null` avec précaution.  
- **Lenteur sur de gros blocs‑notes :** Chargez uniquement les sections nécessaires ou augmentez la taille du tas JVM.

## Questions fréquentes

**Q1 : Puis‑je utiliser Aspose.Note pour Java afin de modifier les révisions de page ?**  
R1 : Non, l’API ne prend actuellement en charge que l’accès en lecture seule aux révisions de page.

**Q2 : Aspose.Note pour Java est‑il compatible avec différentes versions de documents OneNote ?**  
R2 : Oui, il fonctionne avec divers formats de fichiers OneNote, permettant un traitement transparent entre les versions.

**Q3 : Aspose.Note pour Java nécessite‑t‑il une licence pour être utilisé ?**  
R3 : Une licence commerciale est requise pour la production, mais une licence d’évaluation temporaire est disponible pour les tests.

**Q4 : Puis‑je obtenir de l’aide si je rencontre des problèmes avec Aspose.Note pour Java ?**  
R4 : Oui, vous pouvez poser des questions sur le forum Aspose.Note [ici](https://forum.aspose.com/c/note/28).

**Q5 : Existe‑t‑il un essai gratuit pour Aspose.Note pour Java ?**  
R5 : Oui, vous pouvez télécharger un essai gratuit depuis le [site Web](https://releases.aspose.com/).

---

**Dernière mise à jour :** 2026-01-10  
**Testé avec :** Aspose.Note pour Java (dernière version)  
**Auteur :** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}