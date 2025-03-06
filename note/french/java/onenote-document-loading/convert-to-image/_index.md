---
title: Convertir un document OneNote en image - Java
linktitle: Convertir un document OneNote en image - Java
second_title: API Java Aspose.Note
description: Apprenez à convertir OneNote en image à l’aide d’Aspose.Note pour Java. Suivez les étapes simples, chargez le document, initialisez les options et enregistrez-le au format PNG.
weight: 14
url: /fr/java/onenote-document-loading/convert-to-image/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Convertir un document OneNote en image - Java

## Introduction

Dans ce didacticiel, nous vous guiderons tout au long du processus d'utilisation d'Aspose.Note pour Java pour convertir un document OneNote en image. Nous décomposerons chaque étape en instructions faciles à suivre.

## Conditions préalables

Avant de commencer, assurez-vous d'avoir les éléments suivants :

1. Kit de développement Java (JDK) installé sur votre système.
2.  Aspose.Note pour la bibliothèque Java. Vous pouvez le télécharger depuis[ici](https://releases.aspose.com/note/java/).

## Importer des packages

Tout d'abord, importez les packages nécessaires dans votre code Java :

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.SaveFormat;
```

Décomposons maintenant l'exemple de code fourni en plusieurs étapes :

## Étape 1 : Configurer le répertoire de documents

Définissez le répertoire où se trouve votre document OneNote :

```java
String dataDir = "Your Document Directory";
```

 Remplacer`"Your Document Directory"` avec le chemin d’accès à votre document OneNote.

## Étape 2 : Charger le document

Chargez le document OneNote dans Aspose.Note :

```java
Document oneFile = new Document(dataDir + "Sample1.one");
```

 Assurer`"Sample1.one"` correspond au nom de votre fichier de document OneNote.

## Étape 3 : initialiser ImageSaveOptions

 Initialisez le`ImageSaveOptions` objet pour spécifier le format de sauvegarde :

```java
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);
```

Ici, nous enregistrons le document sous forme d'image PNG. Vous pouvez choisir d'autres formats comme JPEG ou BMP si nécessaire.

## Étape 4 : Enregistrez le document en tant qu'image

Enregistrez le document chargé sous forme d'image :

```java
oneFile.save(dataDir + "ConvertToImage_out.png", options);
```

Cette ligne enregistre le document sous forme d'image PNG avec les options spécifiées.

## Étape 5 : Imprimer la confirmation

Imprimez un message pour confirmer que le fichier a été enregistré :

```java
System.out.println("File saved: " + dataDir + "ConvertToImage_out.png");
```

Cette ligne vous informe de la conversion réussie et de l'emplacement du fichier image enregistré.

## Conclusion

En suivant les étapes décrites ci-dessus, vous pouvez facilement convertir un document OneNote en image à l'aide d'Aspose.Note pour Java. C'est un moyen simple et efficace de gérer les conversions de documents dans vos applications Java.

## FAQ

### Q1 : Puis-je convertir plusieurs documents OneNote en une seule fois ?

A1 : Oui, vous pouvez parcourir une liste de documents et effectuer l'opération de conversion pour chaque document.

### Q2 : Aspose.Note prend-il en charge d’autres formats de sortie en dehors des images ?

A2 : Oui, Aspose.Note prend en charge divers formats de sortie tels que les formats PDF, HTML et Microsoft Word.

### Q3 : Aspose.Note est-il compatible avec toutes les versions des fichiers OneNote ?

A3 : Aspose.Note offre une compatibilité avec les fichiers OneNote créés dans différentes versions de Microsoft OneNote.

### Q4 : Puis-je personnaliser la résolution des images de sortie ?

A4 : Oui, vous pouvez ajuster la résolution et d'autres paramètres à l'aide des options disponibles dans Aspose.Note.

### Q5 : Aspose.Note nécessite-t-il une connectivité Internet pour la conversion de documents ?

A5 : Non, Aspose.Note fonctionne localement sans avoir besoin d'une connexion Internet.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
