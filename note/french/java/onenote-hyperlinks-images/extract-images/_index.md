---
title: Extraire des images d'un document OneNote à l'aide de Java
linktitle: Extraire des images d'un document OneNote à l'aide de Java
second_title: API Java Aspose.Note
description: Découvrez comment extraire des images de documents OneNote à l'aide de Java avec la bibliothèque Aspose.Note. Suivez notre guide étape par étape pour une extraction d’image transparente.
weight: 14
url: /fr/java/onenote-hyperlinks-images/extract-images/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Extraire des images d'un document OneNote à l'aide de Java

## Introduction

Dans ce didacticiel, nous vous guiderons tout au long du processus d'extraction d'images d'un document OneNote à l'aide de Java à l'aide de la bibliothèque Aspose.Note.

## Conditions préalables

Avant de commencer, assurez-vous d'avoir les éléments suivants :

1.  Kit de développement Java (JDK) : assurez-vous que Java est installé sur votre système. Vous pouvez le télécharger et l'installer à partir du[site web](https://www.oracle.com/java/technologies/javase-jdk15-downloads.html).

2.  Bibliothèque Aspose.Note : téléchargez et incluez la bibliothèque Aspose.Note dans votre projet Java. Vous pouvez l'obtenir auprès du[lien de téléchargement](https://releases.aspose.com/note/java/).

## Importer des packages

Pour commencer, importez les packages nécessaires :

```java
import java.io.IOException;
import java.nio.file.Files;
import java.nio.file.Paths;
import java.util.List;
import com.aspose.note.Document;
import com.aspose.note.Image;
```

## Étape 1 : Charger le document

Tout d’abord, chargez le document OneNote à l’aide d’Aspose.Note :

```java
String dataDir = "Your Document Directory";
Document doc = new Document(dataDir + "Sample1.one");
```

## Étape 2 : Obtenez toutes les images

Ensuite, récupérez toutes les images du document :

```java
List<Image> list = doc.getChildNodes(Image.class);
System.out.printf("Total Images: %s\n\n", list.size());
```

## Étape 3 : Extraire les images

Parcourez la liste des images et enregistrez chaque image dans un fichier :

```java
for (int i = 0; i < list.size(); i++) {
    Image image = list.get(i);
    String outputFile = "ExtractImages_out" + i + "_" + image.getFileName();
    byte[] buffer = image.getBytes();
    Files.write(Paths.get(dataDir + outputFile), buffer);
    System.out.printf("File saved: %s\n", dataDir);
}
```

## Conclusion

L'extraction d'images d'un document OneNote à l'aide de Java peut être réalisée de manière transparente avec la bibliothèque Aspose.Note. En suivant les étapes décrites dans ce didacticiel, vous pouvez facilement récupérer des images de vos documents pour un traitement ou une analyse ultérieure.

## FAQ

### Q1 : Puis-je extraire des images de documents OneNote protégés par mot de passe ?

A1 : Oui, Aspose.Note prend également en charge l'extraction d'images à partir de documents protégés par mot de passe.

### Q2 : Aspose.Note est-il compatible avec différentes versions de Java ?

A2 : Aspose.Note est compatible avec différentes versions de Java, garantissant une flexibilité aux développeurs.

### Q3 : Puis-je extraire des images de plusieurs documents OneNote en une seule exécution ?

A3 : Absolument, vous pouvez parcourir plusieurs documents et extraire des images de chacun d'eux à l'aide d'Aspose.Note.

### Q4 : Existe-t-il des limites de taille pour les documents OneNote ?

A4 : Aspose.Note gère efficacement des documents de différentes tailles, garantissant ainsi l'absence de limitations sur la taille des documents pour l'extraction d'images.

### Q5 : Aspose.Note prend-il en charge l’extraction d’autres types de contenu en dehors des images ?

A5 : Oui, outre les images, Aspose.Note permet l'extraction de texte, de pièces jointes et d'autres types de contenu à partir de documents OneNote.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
