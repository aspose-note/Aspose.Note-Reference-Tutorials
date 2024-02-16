---
title: Enregistrer dans une image TIFF à l'aide des options d'enregistrement d'image dans OneNote
linktitle: Enregistrer dans une image TIFF à l'aide des options d'enregistrement d'image dans OneNote
second_title: API Java Aspose.Note
description: Convertissez les documents OneNote en TIFF et contrôlez la taille et la qualité des fichiers ! Choisissez la compression Jpeg, PackBits ou Fax en Java. Obtenez des exemples de code et apprenez comment ! #OneNote #Java #Aspose
type: docs
weight: 21
url: /fr/java/onenote-document-saving/save-to-tiff-image-using-image-save-options/
---
## Introduction

Dans ce didacticiel, vous apprendrez à enregistrer un document au format d'image TIFF à l'aide de différentes méthodes de compression dans Aspose.Note pour Java. Nous aborderons les conditions préalables, l'importation de packages et fournirons un guide étape par étape pour chaque méthode de compression.

## Conditions préalables

Avant de commencer, assurez-vous d'avoir les éléments suivants :

- Kit de développement Java (JDK) installé sur votre système.
- Aspose.Note pour la bibliothèque Java téléchargée et configurée.
- Compréhension de base du langage de programmation Java.

## Importer des packages

Tout d'abord, vous devez importer les packages nécessaires dans votre fichier Java :

```java
import com.aspose.note.*;
import java.io.IOException;
import java.nio.file.Paths;
```

## Étape 1 : Enregistrer au format TIFF à l'aide de la compression JPEG

```java
public static void SaveToTiffUsingJpegCompression() throws IOException {
    // Le chemin d'accès au répertoire des documents.
    String dataDir = "Your Document Directory";

    // Chargez le document dans Aspose.Note.
    Document oneFile = new Document(Paths.get(dataDir, "Aspose.one").toString());

    ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);
    options.setTiffCompression(TiffCompression.Jpeg);
    options.setQuality(93);

    oneFile.save(Paths.get(dataDir,"SaveToTiffUsingJpegCompression.tiff").toString(), options);
}
```

-  Chargez le document en utilisant`Document` classe.
-  Créer une instance de`ImageSaveOptions` et spécifiez le type de compression TIFF comme JPEG.
- Définissez la qualité souhaitée (facultatif).
- Enregistrez le document au format TIFF en utilisant les options spécifiées.

## Étape 2 : Enregistrer au format TIFF à l'aide de la compression PackBits

```java
public static void SaveToTiffUsingPackBitsCompression() throws IOException {
    // Le chemin d'accès au répertoire des documents.
    String dataDir = "Your Document Directory";

    // Chargez le document dans Aspose.Note.
    Document oneFile = new Document(Paths.get(dataDir, "Aspose.one").toString());

    ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);
    options.setTiffCompression(TiffCompression.PackBits);

    oneFile.save(Paths.get(dataDir, "SaveToTiffUsingPackBitsCompression.tiff").toString(), options);
}
```

-  Chargez le document en utilisant`Document` classe.
-  Créer une instance de`ImageSaveOptions` et spécifiez le type de compression TIFF comme PackBits.
- Enregistrez le document au format TIFF en utilisant les options spécifiées.

## Étape 3 : Enregistrer au format TIFF à l'aide de la compression de télécopie du groupe 3 du CCITT

```java
public static void SaveToTiffUsingCcitt3Compression() throws IOException {
    // Le chemin d'accès au répertoire des documents.
    String dataDir = "Your Document Directory";

    // Chargez le document dans Aspose.Note.
    Document oneFile = new Document(Paths.get(dataDir, "Aspose.one").toString());

    ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);
    options.setColorMode(ColorMode.BlackAndWhite);
    options.setTiffCompression(TiffCompression.Ccitt3);

    oneFile.save(Paths.get(dataDir, "SaveToTiffUsingCcitt3Compression.tiff").toString(), options);
}
```

-  Chargez le document en utilisant`Document` classe.
-  Créer une instance de`ImageSaveOptions` et spécifiez le type de compression TIFF comme CCITT Group 3 Fax.
- Réglez le mode couleur sur noir et blanc.
- Enregistrez le document au format TIFF en utilisant les options spécifiées.

## Conclusion

Dans ce didacticiel, vous avez appris à enregistrer un document au format d'image TIFF à l'aide de différentes méthodes de compression dans Aspose.Note pour Java. En suivant le guide étape par étape, vous pouvez utiliser efficacement les capacités d'Aspose.Note pour répondre à vos besoins.

## FAQ

### Q1 : Puis-je utiliser Aspose.Note pour Java pour convertir d’autres formats de document en TIFF ?

A1 : Oui, Aspose.Note pour Java prend en charge la conversion de divers formats de documents vers TIFF, y compris les documents OneNote.

### Q2 : Quelle est l'importance de spécifier le type de compression lors de l'enregistrement au format TIFF ?

A2 : La spécification du type de compression vous permet de contrôler la qualité de l'image et la taille du fichier. Différentes méthodes de compression offrent des compromis entre qualité et taux de compression.

### Q3 : Aspose.Note pour Java est-il adapté au traitement par lots de documents ?

A3 : Oui, Aspose.Note pour Java fournit des API pour le traitement par lots, vous permettant d'automatiser efficacement les tâches de conversion de documents.

### Q4 : Puis-je personnaliser davantage les paramètres de compression ?

A4 : Oui, vous pouvez ajuster des paramètres tels que la qualité, la résolution et la méthode de compression pour adapter la sortie en fonction de vos besoins.

### Q5 : Aspose.Note pour Java offre-t-il un support technique ?

A5 : Oui, Aspose fournit une assistance technique complète via des forums et des systèmes basés sur des tickets.