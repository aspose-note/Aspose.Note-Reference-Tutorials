---
title: Obtenir les révisions de page dans OneNote - Aspose.Note
linktitle: Obtenir les révisions de page dans OneNote - Aspose.Note
second_title: API Java Aspose.Note
description: Découvrez comment récupérer les révisions de page dans OneNote à l’aide d’Aspose.Note pour Java. Suivez notre guide étape par étape pour un suivi efficace des modifications.
weight: 14
url: /fr/java/onenote-page-manipulation/get-page-revisions/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Obtenir les révisions de page dans OneNote - Aspose.Note

## Introduction

OneNote est un outil puissant pour organiser et gérer vos notes, mais vous devez parfois suivre les modifications et les révisions apportées à vos pages. Avec Aspose.Note pour Java, vous pouvez facilement récupérer les révisions de page par programme. Dans ce didacticiel, nous vous guiderons tout au long du processus d'obtention de révisions de page dans OneNote à l'aide d'Aspose.Note pour Java.

## Conditions préalables

Avant de commencer, assurez-vous que les conditions préalables suivantes sont remplies :

### 1. Kit de développement Java (JDK)

Assurez-vous que le kit de développement Java (JDK) est installé sur votre système. Vous pouvez télécharger et installer JDK à partir du site Web d'Oracle.

### 2. Aspose.Note pour Java

Téléchargez et installez Aspose.Note pour Java à partir du[lien de téléchargement](https://releases.aspose.com/note/java/).

### 3. Exemple de document OneNote

Préparez un exemple de document OneNote (`Sample1.one`) qui contient les pages dont vous souhaitez récupérer les révisions.

## Importer des packages

Tout d’abord, vous devez importer les packages nécessaires depuis Aspose.Note pour Java.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.LoadOptions;
import com.aspose.note.Page;
```

Maintenant, décomposons l'exemple fourni en plusieurs étapes :

## Étape 1 : configurer le répertoire de documents

Définissez le chemin du répertoire où se trouve votre document OneNote.

```java
String dataDir = "Your Document Directory";
```

## Étape 2 : charger le document OneNote

 Chargez le document OneNote à l'aide de`LoadOptions` pour activer l'historique de chargement.

```java
LoadOptions loadOptions = new LoadOptions();
loadOptions.setLoadHistory(true);
Document document = new Document(dataDir + "Sample1.one", loadOptions);
```

## Étape 3 : Obtenir la première page

Récupérez la première page du document chargé.

```java
Page firstPage = document.getFirstChild();
```

## Étape 4 : Parcourir les révisions de page

Parcourez chaque révision de page et récupérez des informations pertinentes telles que l'heure de la dernière modification, l'heure de création, le titre, le niveau et l'auteur.

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

## Conclusion

Dans ce didacticiel, nous avons appris à récupérer les révisions de page dans OneNote à l'aide d'Aspose.Note pour Java. En suivant ces étapes, vous pouvez suivre efficacement les modifications apportées à vos pages OneNote par programme.

## FAQ

### Q1 : Puis-je utiliser Aspose.Note pour Java pour modifier les révisions de page ?

A1 : Non, Aspose.Note pour Java prend actuellement en charge la récupération des révisions de page, mais pas leur modification.

### Q2 : Aspose.Note pour Java est-il compatible avec différentes versions de documents OneNote ?

A2 : Oui, Aspose.Note pour Java prend en charge différentes versions de documents OneNote, vous permettant de travailler de manière transparente avec différents formats de fichiers.

### Q3 : Aspose.Note pour Java nécessite-t-il une licence pour être utilisé ?

A3 : Oui, vous devez acheter une licence pour utiliser Aspose.Note pour Java dans des projets commerciaux. Cependant, vous pouvez également obtenir une licence temporaire à des fins d'évaluation.

### Q4 : Puis-je demander de l'aide si je rencontre des problèmes lors de l'utilisation d'Aspose.Note pour Java ?

 A4 : Oui, vous pouvez demander de l'aide sur le forum Aspose.Note[ici](https://forum.aspose.com/c/note/28).

### Q5 : Existe-t-il un essai gratuit disponible pour Aspose.Note pour Java ?

 A5 : Oui, vous pouvez accéder à un essai gratuit d'Aspose.Note pour Java à partir du[site web](https://releases.aspose.com/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
