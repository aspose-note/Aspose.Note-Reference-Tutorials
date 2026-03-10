---
date: 2025-12-21
description: Apprenez comment ajouter une image aux documents OneNote en Java avec
  Aspose.Note pour Java. Suivez notre guide étape par étape pour insérer des images
  et, si vous le souhaitez, enregistrer OneNote au format PDF.
linktitle: Insert an Image in OneNote Document with Java
second_title: Aspose.Note Java API
title: Comment ajouter une image à OneNote avec Java
url: /fr/java/onenote-hyperlinks-images/insert-image/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Insérer une image dans un document OneNote avec Java

## Introduction

Dans ce tutoriel, nous explorerons comment insérer une image dans un document OneNote en utilisant Java avec l'aide d'Aspose.Note for Java. Aspose.Note for Java est une bibliothèque puissante qui permet aux développeurs de travailler avec les fichiers Microsoft OneNote de manière programmatique, permettant diverses opérations telles que la création, la lecture et la manipulation de documents OneNote.

## Réponses rapides
- **Quel est le moyen le plus simple d'ajouter une image à OneNote en utilisant Java ?**  
  Utilisez la classe `Image` d'Aspose.Note for Java et ajoutez‑la à une page.
- **Ai‑je besoin d'une licence pour une utilisation en production ?**  
  Oui, une licence commerciale est requise pour les déploiements en production.
- **Puis‑je définir des dimensions personnalisées pour l'image ?**  
  Absolument – appelez `setWidth()` et `setHeight()` sur l'objet `Image`.
- **Est‑il possible d'enregistrer le fichier OneNote au format PDF après avoir ajouté l'image ?**  
  Oui, appelez `save(..., SaveFormat.Pdf)` pour **enregistrer OneNote au format PDF**.
- **Quelle version de Java est prise en charge ?**  
  Aspose.Note for Java fonctionne avec JDK 8 et versions ultérieures.

## Comment ajouter une image à OneNote en utilisant Java ?

Avant de plonger dans le code, discutons brièvement pourquoi vous pourriez vouloir intégrer des images dans OneNote de manière programmatique. Que vous génériez des comptes‑rendus de réunion, créiez des rapports automatisés ou construisiez un pipeline de documentation, l’insertion d’images donne à vos notes un contexte visuel que le texte brut ne peut fournir. Avec Aspose.Note for Java, vous pouvez faire cela entièrement en code, sans ouvrir l’interface OneNote.

## Prérequis

Avant de commencer, assurez‑vous que vous avez les prérequis suivants configurés :

### 1. Java Development Kit (JDK)
Assurez‑vous d'avoir le Java Development Kit (JDK) installé sur votre système. Vous pouvez télécharger et installer le JDK depuis le site Web d'Oracle.

### 2. Aspose.Note for Java Library
Téléchargez et configurez la bibliothèque Aspose.Note for Java en suivant la [documentation](https://reference.aspose.com/note/java/).

## Importer les packages

Commencez par importer les packages nécessaires dans votre projet Java. Ces packages incluent la bibliothèque Aspose.Note et d'autres dépendances requises.

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.HorizontalAlignment;
import com.aspose.note.Image;
import com.aspose.note.LoadOptions;
import com.aspose.note.Page;
import com.aspose.note.SaveFormat;
```

Décomposons le processus d'insertion d'une image dans un document OneNote en plusieurs étapes :

## Étape 1 : Charger le document OneNote

Tout d'abord, chargez le document OneNote dans lequel vous souhaitez insérer l'image.

```java
LoadOptions options = new LoadOptions();
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Sample1.one", options);
```

## Étape 2 : Obtenir la page

Récupérez la page du document où vous voulez insérer l'image.

```java
Page page = oneFile.getFirstChild();
```

## Étape 3 : Charger l'image

Chargez l'image que vous souhaitez insérer dans le document OneNote.

```java
Image image = new Image(oneFile, dataDir + "Input.jpg");
```

## Étape 4 : Personnaliser les attributs de l'image (Optionnel)

Optionnellement, vous pouvez personnaliser la taille, la position et l'alignement de l'image selon vos besoins. C'est ici que vous **définissez les dimensions de l'image en Java**.

```java
image.setWidth(100);
image.setHeight(100);
image.setVerticalOffset(400);
image.setHorizontalOffset(100);
image.setAlignment(HorizontalAlignment.Right);
```

## Étape 5 : Ajouter l'image à la page

Ajoutez l'image à la page du document OneNote.

```java
page.appendChildLast(image);
```

## Étape 6 : Enregistrer le document

Enregistrez le document modifié, y compris l'image insérée. Vous pouvez également **enregistrer OneNote au format PDF** à cette étape.

```java
try {
    oneFile.save(dataDir + "InsertanImage_out.pdf", SaveFormat.Pdf);
} catch (IOException e) {
    e.printStackTrace();
}
```

## Conclusion

Dans ce tutoriel, nous avons appris comment insérer une image dans un document OneNote en utilisant Java avec l'aide de la bibliothèque Aspose.Note for Java. En suivant le guide étape par étape, vous pouvez incorporer facilement des images dans vos documents OneNote de manière programmatique.

## FAQ

### Q1 : Puis‑je insérer plusieurs images dans un même document OneNote en utilisant cette méthode ?
R1 : Oui, vous pouvez insérer plusieurs images dans un même document OneNote en répétant le processus décrit dans ce tutoriel pour chaque image.

### Q2 : Aspose.Note for Java est‑il compatible avec toutes les versions de OneNote ?
R2 : Aspose.Note for Java prend en charge les fichiers OneNote créés avec Microsoft OneNote 2010 et les versions ultérieures.

### Q3 : Puis‑je insérer des images de différents formats, tels que PNG ou GIF, dans un document OneNote ?
R3 : Oui, Aspose.Note for Java prend en charge l'insertion d'images dans divers formats, y compris PNG, JPEG, GIF, et plus.

### Q4 : Existe‑t‑il une version d'essai d'Aspose.Note for Java disponible à des fins de test ?
R4 : Oui, vous pouvez télécharger une version d'essai gratuite d'Aspose.Note for Java depuis le site Web à des fins d'évaluation.

### Q5 : Comment obtenir le support technique pour Aspose.Note for Java ?
R5 : Vous pouvez obtenir le support technique pour Aspose.Note for Java en visitant le [forum](https://forum.aspose.com/c/note/28) dédié aux produits Aspose.Note.

---

**Last Updated:** 2025-12-21  
**Tested With:** Aspose.Note for Java 24.10  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}