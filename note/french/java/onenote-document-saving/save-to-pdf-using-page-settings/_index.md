---
title: Enregistrer au format PDF à l'aide des paramètres de page dans OneNote - Aspose.Note
linktitle: Enregistrer au format PDF à l'aide des paramètres de page dans OneNote - Aspose.Note
second_title: API Java Aspose.Note
description: Découvrez comment enregistrer des documents OneNote au format PDF en Java à l'aide de la bibliothèque Aspose.Note. Guide étape par étape avec des exemples de code pour différents paramètres de page.
type: docs
weight: 19
url: /fr/java/onenote-document-saving/save-to-pdf-using-page-settings/
---
## Introduction

Dans ce didacticiel, nous apprendrons comment enregistrer des documents OneNote au format PDF en utilisant différents paramètres de page avec Aspose.Note pour Java. Nous aborderons deux méthodes : l'enregistrement avec les paramètres de page Lettre et l'enregistrement avec les paramètres de page A4 sans limite de hauteur.

## Conditions préalables

Avant de commencer, assurez-vous que les conditions préalables suivantes sont remplies :

1. Kit de développement Java (JDK) installé sur votre système.
2. Bibliothèque Aspose.Note pour Java téléchargée et incluse dans votre projet Java.
3. Compréhension de base du langage de programmation Java.

## Importer des packages

Assurez-vous d'avoir importé les packages nécessaires à l'utilisation d'Aspose.Note pour Java dans votre projet. Voici la déclaration d'importation :

```java
import com.aspose.note.*;
import java.io.IOException;
import java.nio.file.Paths;
```

## Enregistrer au format PDF à l'aide des paramètres de page de lettre

### Étape 1 : Charger le document

Tout d'abord, chargez le document OneNote dans Aspose.Note :

```java
Document oneFile = new Document("path/to/your/OneNote.one");
```

### Étape 2 : Définir le chemin de destination

Spécifiez le chemin de destination du fichier PDF :

```java
String dst = "path/to/your/SaveToPdfUsingLetterPageSettings.pdf";
```

### Étape 3 : Enregistrez le document

Enregistrez le document avec les paramètres de la page Lettre :

```java
PdfSaveOptions options = new PdfSaveOptions();
options.setPageSettings(PageSettings.getLetter());
oneFile.save(dst, options);
```

## Enregistrer au format PDF en utilisant les paramètres de page A4 sans limite de hauteur

### Étape 1 : Charger le document

De même, chargez le document OneNote dans Aspose.Note :

```java
Document oneFile = new Document("path/to/your/OneNote.one");
```

### Étape 2 : Définir le chemin de destination

Spécifiez le chemin de destination du fichier PDF :

```java
String dst = "path/to/your/SaveToPdfUsingA4PageSettingsWithoutHeightLimit.pdf";
```

### Étape 3 : Enregistrez le document

Enregistrez le document avec des paramètres de page A4 sans limite de hauteur :

```java
PdfSaveOptions options = new PdfSaveOptions();
options.setPageSettings(PageSettings.getA4NoHeightLimit());
oneFile.save(dst, options);
```

Après avoir suivi ces étapes, vous aurez enregistré avec succès votre document OneNote au format PDF en utilisant différents paramètres de page.

## Conclusion

Dans ce didacticiel, nous avons expliqué comment enregistrer des documents OneNote au format PDF à l'aide de la bibliothèque Aspose.Note pour Java. En suivant le guide étape par étape, vous pouvez facilement intégrer cette fonctionnalité dans vos applications Java.

## FAQ

### Q1 : Puis-je personnaliser davantage les paramètres de la page ?

A1 : Oui, vous pouvez personnaliser les paramètres de la page en fonction de vos besoins à l'aide d'Aspose.Note pour Java.

### Q2 : Aspose.Note prend-il en charge d'autres formats de sortie que le PDF ?

A2 : Oui, Aspose.Note prend en charge divers formats de sortie, notamment les images et HTML.

### Q3 : Aspose.Note est-il compatible avec différentes versions de fichiers OneNote ?

A3 : Oui, Aspose.Note prend en charge les fichiers OneNote de différentes versions, notamment .one et .onetoc2.

### Q4 : Puis-je convertir plusieurs fichiers OneNote en PDF en une seule fois ?

A4 : Oui, vous pouvez traiter par lots plusieurs fichiers OneNote à l'aide d'Aspose.Note pour Java.

### Q5 : Existe-t-il une version d'essai disponible à des fins de test ?

A5 : Oui, vous pouvez obtenir un essai gratuit d'Aspose.Note pour Java sur le site Web.