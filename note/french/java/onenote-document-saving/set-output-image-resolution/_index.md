---
title: Définir la résolution de l'image de sortie dans OneNote - Aspose.Note
linktitle: Définir la résolution de l'image de sortie dans OneNote - Aspose.Note
second_title: API Java Aspose.Note
description: Découvrez comment ajuster la résolution de l'image dans les documents OneNote à l'aide d'Aspose.Note pour Java. Suivez notre guide étape par étape pour une mise en œuvre facile
weight: 23
url: /fr/java/onenote-document-saving/set-output-image-resolution/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Définir la résolution de l'image de sortie dans OneNote - Aspose.Note

## Introduction

Cherchez-vous à manipuler la résolution des images dans vos documents OneNote à l’aide de Java ? Aspose.Note pour Java offre une solution robuste pour de telles tâches. Dans ce didacticiel, nous passerons en revue les étapes permettant de définir la résolution de l'image de sortie à l'aide d'Aspose.Note.

## Conditions préalables

Avant de commencer, assurez-vous de disposer des prérequis suivants :

1. Kit de développement Java (JDK) : installez JDK sur votre système.
2. Aspose.Note pour Java : téléchargez et installez Aspose.Note pour Java à partir du[site web](https://releases.aspose.com/note/java/).
3. Environnement de développement intégré (IDE) : choisissez votre IDE préféré comme Eclipse ou IntelliJ IDEA.

## Importer des packages

Dans votre projet Java, importez les packages Aspose.Note nécessaires :

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.SaveFormat;
```

## Étape 1 : charger le document OneNote

Commencez par charger le document OneNote dans votre application Java :

```java
String dataDir = "Your Document Directory";
Document doc = new Document(dataDir + "Sample1.one");
```

 Remplacer`"Your Document Directory"` avec le répertoire réel où réside votre document OneNote.

## Étape 2 : définir les options d'enregistrement de l'image

Définissez les options d'enregistrement de l'image et précisez la résolution souhaitée :

```java
ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.Jpeg);
imageSaveOptions.setResolution(120);
```

 Ici, nous définissons la résolution sur`120 dpi`. Vous pouvez ajuster cette valeur en fonction de vos besoins.

## Étape 3 : Enregistrez le document avec une résolution modifiée

Enregistrez le document avec la résolution d'image mise à jour :

```java
doc.save(dataDir + "SetOutputImageResolution_out.jpeg", imageSaveOptions);
```

Cela enregistrera le document modifié avec la résolution spécifiée.

## Conclusion

Dans ce didacticiel, nous avons expliqué comment définir la résolution de l'image de sortie dans les documents OneNote à l'aide d'Aspose.Note pour Java. En suivant ces étapes simples, vous pouvez manipuler efficacement la résolution des images pour répondre aux exigences de votre application.


## FAQ

### Q1 : Puis-je régler la résolution de l'image à une valeur supérieure à 120 dpi ?

A1 : Oui, vous pouvez définir la résolution sur n'importe quelle valeur souhaitée en fonction de vos besoins.

### Q2 : Aspose.Note prend-il en charge d'autres formats d'image que JPEG ?

A2 : Oui, Aspose.Note prend en charge divers formats d'image tels que PNG, BMP, GIF, etc.

### Q3 : Aspose.Note est-il compatible avec toutes les versions de Java ?

A3 : Aspose.Note est compatible avec Java 1.6 ou les versions ultérieures.

### Q4 : Puis-je manipuler d’autres aspects des images dans les documents OneNote à l’aide d’Aspose.Note ?

A4 : Oui, Aspose.Note fournit des fonctionnalités complètes pour la manipulation d'images, notamment le redimensionnement, le recadrage et la rotation.

### Q5 : Où puis-je obtenir de l'aide pour les requêtes liées à Aspose.Note ?

 A5 : Vous pouvez demander de l'aide au forum communautaire Aspose.Note.[ici](https://forum.aspose.com/c/note/28).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
