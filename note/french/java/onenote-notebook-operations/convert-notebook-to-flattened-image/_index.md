---
title: Convertir un bloc-notes en image aplatie dans OneNote - Aspose.Note
linktitle: Convertir un bloc-notes en image aplatie dans OneNote - Aspose.Note
second_title: API Java Aspose.Note
description: Découvrez comment convertir un bloc-notes en image aplatie dans OneNote à l’aide d’Aspose.Note pour Java. Conservez sans effort tous les éléments dans un seul fichier image.
weight: 13
url: /fr/java/onenote-notebook-operations/convert-notebook-to-flattened-image/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Convertir un bloc-notes en image aplatie dans OneNote - Aspose.Note

## Introduction

Dans ce didacticiel, nous vous guiderons tout au long du processus de conversion d'un bloc-notes en image aplatie dans OneNote à l'aide d'Aspose.Note pour Java. Cela vous permet d'enregistrer votre bloc-notes sous forme de fichier image, garantissant ainsi que tous les éléments sont conservés dans un seul format d'image.

## Conditions préalables

Avant de commencer, assurez-vous d'avoir les éléments suivants :

1. Kit de développement Java (JDK) installé sur votre système.
2.  Bibliothèque Aspose.Note pour Java téléchargée et configurée dans votre projet Java. Vous pouvez télécharger la bibliothèque depuis[ici](https://releases.aspose.com/note/java/).
3. Connaissance de base de la programmation Java.

## Importer des packages

Pour commencer, vous devez importer les packages nécessaires depuis Aspose.Note pour Java :

```java
import java.io.IOException;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.Notebook;
import com.aspose.note.NotebookImageSaveOptions;
import com.aspose.note.SaveFormat;
```

## Étape 1 : configurer le répertoire de documents

Tout d'abord, définissez le répertoire où se trouve votre fichier notebook :

```java
String dataDir = "Your Document Directory";
```

 Remplacer`"Your Document Directory"` avec le chemin d'accès à votre fichier notebook.

## Étape 2 : Charger le bloc-notes

 Ensuite, chargez le fichier notebook à l'aide du`Notebook` classe:

```java
Notebook notebook = new Notebook(dataDir + "test.onetoc2");
```

 Assurez-vous de remplacer`"test.onetoc2"` avec le nom de votre fichier notebook.

## Étape 3 : Définir les options d'enregistrement de l'image

Maintenant, configurez les options d’enregistrement du bloc-notes en tant qu’image. Nous spécifierons le format de sauvegarde au format PNG et définirons la résolution sur 400 DPI :

```java
NotebookImageSaveOptions saveOptions = new NotebookImageSaveOptions(SaveFormat.Png);
ImageSaveOptions documentSaveOptions = saveOptions.getDocumentSaveOptions();
documentSaveOptions.setResolution(400);
```

Vous pouvez ajuster la résolution selon vos besoins.

## Étape 4 : Aplatir le cahier

Pour garantir que tous les éléments sont aplatis en une seule image, définissez le`flatten` possibilité de`true`:

```java
saveOptions.setFlatten(true);
```

Cela garantit que l’image résultante conserve la mise en page de votre bloc-notes.

## Étape 5 : Enregistrer l'image

Enfin, enregistrez le bloc-notes sous forme d'image aplatie :

```java
notebook.save(dataDir + "ExportImageasFlattenedNotebook_out.png", saveOptions);
```

 Remplacer`"ExportImageasFlattenedNotebook_out.png"` avec le nom de fichier de sortie souhaité.

## Conclusion

En conclusion, en utilisant Aspose.Note pour Java, vous pouvez facilement convertir votre bloc-notes en image aplatie dans OneNote. Ce processus garantit que tous les éléments sont conservés dans un seul format d'image, facilitant ainsi le partage et la visualisation.

## FAQ

### Q1 : Puis-je ajuster la résolution de l’image de sortie ?

 A1 : Oui, vous pouvez ajuster la résolution selon vos besoins en modifiant le`setResolution` paramètre de méthode.

### Q2 : Aspose.Note prend-il en charge d’autres formats d’image pour l’exportation ?

A2 : Oui, Aspose.Note prend en charge divers formats d'image tels que PNG, JPEG, BMP, etc., pour l'exportation de blocs-notes.

### Q3 : Puis-je personnaliser davantage l’image de sortie ?

A3 : Oui, Aspose.Note propose des options étendues pour personnaliser l'image de sortie, notamment la taille de la page, l'orientation et les paramètres de qualité.

### Q4 : Existe-t-il une version d'essai disponible pour Aspose.Note pour Java ?

 A4 : Oui, vous pouvez obtenir une version d'essai gratuite auprès de[ici](https://releases.aspose.com/).

### Q5 : Où puis-je trouver de l'assistance pour Aspose.Note pour Java ?

 A5 : Vous pouvez trouver de l'aide et des ressources sur le forum Aspose.Note[ici](https://forum.aspose.com/c/note/28).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
