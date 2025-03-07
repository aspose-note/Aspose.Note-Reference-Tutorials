---
title: Enregistrer dans une image en niveaux de gris dans OneNote - Aspose.Note
linktitle: Enregistrer dans une image en niveaux de gris dans OneNote - Aspose.Note
second_title: API Java Aspose.Note
description: Découvrez comment enregistrer un document en tant qu'image en niveaux de gris dans OneNote à l'aide d'Aspose.Note pour Java. Manipulez facilement les documents Microsoft OneNote par programmation.
weight: 17
url: /fr/java/onenote-document-saving/save-to-grayscale-image/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Enregistrer dans une image en niveaux de gris dans OneNote - Aspose.Note

## Introduction

Dans ce didacticiel, nous verrons comment enregistrer un document en tant qu'image en niveaux de gris dans OneNote à l'aide d'Aspose.Note pour Java. Les images en niveaux de gris sont des images monochromatiques dans lesquelles les informations de couleur sont représentées uniquement par des nuances de gris. Aspose.Note est une puissante API Java qui permet la manipulation des documents Microsoft OneNote par programme.

## Conditions préalables

Avant de commencer, assurez-vous d'avoir les éléments suivants :

1. Kit de développement Java (JDK) installé sur votre système.
2.  Aspose.Note pour la bibliothèque Java. Vous pouvez le télécharger depuis[ici](https://releases.aspose.com/note/java/).
3. Compréhension de base de la programmation Java.

## Importer des packages

Pour commencer, importez les packages nécessaires :

```java
import com.aspose.note.ColorMode;
import com.aspose.note.Document;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.SaveFormat;
import java.io.IOException;
```

## Étape 1 : Charger le document

 Tout d’abord, chargez le document dans Aspose.Note. Remplacer`"Your Document Directory"` avec le chemin d'accès à votre répertoire de documents et`"Aspose.one"` avec le nom de votre document OneNote.

```java
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Aspose.one");
```

## Étape 2 : Définir le chemin de sortie et les options

Définissez le chemin de sortie de l'image en niveaux de gris et spécifiez les options d'enregistrement. Nous allons définir le mode de couleur sur niveaux de gris.

```java
dataDir = dataDir + "SaveAsGrayscaleImage_out.png";
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);
options.setColorMode(ColorMode.GrayScale);
```

## Étape 3 : Enregistrez le document

Enfin, enregistrez le document sous forme d'image en niveaux de gris en utilisant les options spécifiées.

```java
oneFile.save(dataDir, options);
```

## Conclusion

Toutes nos félicitations! Vous avez appris avec succès comment enregistrer un document en tant qu'image en niveaux de gris dans OneNote à l'aide d'Aspose.Note pour Java. Cela peut être incroyablement utile pour diverses applications nécessitant des images en niveaux de gris.

## FAQ

### Q1 : Puis-je enregistrer l’image en niveaux de gris dans un format différent ?

 A1 : Oui, vous pouvez. Changez simplement le`SaveFormat` paramètre dans le`ImageSaveOptions` constructeur au format souhaité.

### Q2 : Aspose.Note est-il compatible avec toutes les versions des documents OneNote ?

A2 : Aspose.Note prend en charge Microsoft OneNote 2010 et supérieur.

### Q3 : Aspose.Note nécessite-t-il une licence pour être utilisé ?

A3 : Oui, vous avez besoin d'une licence valide pour utiliser Aspose.Note dans des environnements de production. Cependant, vous pouvez obtenir une licence temporaire à des fins de test.

### Q4 : Puis-je manipuler d’autres aspects du document avant de l’enregistrer sous forme d’image ?

A4 : Absolument ! Aspose.Note fournit un large éventail de fonctionnalités pour modifier des documents OneNote par programme.

### Q5 : Où puis-je trouver de l'aide si je rencontre des problèmes ?

A5 : Vous pouvez trouver de l'aide sur le forum Aspose.Note[ici](https://forum.aspose.com/c/note/28).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
