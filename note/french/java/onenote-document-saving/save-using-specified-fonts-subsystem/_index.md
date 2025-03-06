---
title: Enregistrer à l'aide du sous-système de polices spécifié dans OneNote
linktitle: Enregistrer à l'aide du sous-système de polices spécifié dans OneNote
second_title: API Java Aspose.Note
description: Découvrez comment enregistrer des documents OneNote à l'aide du sous-système de polices spécifié en Java avec Aspose.Note. Garantissez sans effort une représentation cohérente des polices sur toutes les plateformes.
weight: 22
url: /fr/java/onenote-document-saving/save-using-specified-fonts-subsystem/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Enregistrer à l'aide du sous-système de polices spécifié dans OneNote

## Introduction

Aspose.Note pour Java offre des fonctionnalités robustes pour travailler avec des documents OneNote. Une exigence courante lorsque l'on travaille avec de tels documents est de s'assurer que les polices sont correctement conservées, en particulier si le document doit être exporté ou enregistré dans différents formats comme PDF. Ce didacticiel vous guidera tout au long du processus d'enregistrement des documents OneNote tout en spécifiant le sous-système de polices, garantissant ainsi une représentation cohérente et précise du texte sur différentes plates-formes.

## Conditions préalables

Avant de plonger dans le didacticiel, assurez-vous d'avoir configuré les conditions préalables suivantes :

### 1. Kit de développement Java (JDK)

 Assurez-vous que le kit de développement Java (JDK) est installé sur votre système. Vous pouvez le télécharger depuis[ici](https://www.oracle.com/java/technologies/javase-jdk15-downloads.html) si ce n'est pas déjà fait.

### 2. Aspose.Note pour la bibliothèque Java

 Téléchargez et configurez la bibliothèque Aspose.Note pour Java. Vous pouvez le télécharger depuis le[site web](https://releases.aspose.com/note/java/).

## Importer des packages

Assurez-vous d'importer les packages nécessaires dans votre projet Java :

```java
import com.aspose.note.Document;
import com.aspose.note.PdfSaveOptions;
import com.aspose.note.fonts.DocumentFontsSubsystem;
import java.io.FileInputStream;
import java.io.IOException;
import java.io.InputStream;
import java.nio.file.Paths;
```

Décomposons maintenant chaque exemple en plusieurs étapes pour mieux comprendre le processus.

## Étape 1 : Enregistrer à l'aide du sous-système de polices de document avec le nom de police par défaut

Cette étape montre comment enregistrer un document au format PDF en utilisant un nom de police par défaut spécifié.

```java
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontName() throws IOException
{
    // Chargez le document dans Aspose.Note.
    Document oneFile = new Document("missing-font.one");

    // Spécifiez la police par défaut.
    PdfSaveOptions options = new PdfSaveOptions();
    options.setFontsSubsystem(DocumentFontsSubsystem.usingDefaultFont("Times New Roman"));

    // Enregistrez le document au format PDF.
    oneFile.save("SaveUsingDocumentFontsSubsystemWithDefaultFontName_out.pdf", options);
}
```

Dans cette étape :
- Le document OneNote est chargé à l'aide d'Aspose.Note.
- La police par défaut est spécifiée comme « Times New Roman ».
- Le document est enregistré au format PDF avec la police spécifiée.

## Étape 2 : Enregistrer à l'aide du sous-système de polices de document avec la police par défaut du fichier

Cette étape montre comment enregistrer un document au format PDF en utilisant une police par défaut chargée à partir d'un fichier.

```java
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontFromFile() throws IOException
{
    // Chargez le document dans Aspose.Note.
    Document oneFile = new Document("missing-font.one");

    // Spécifiez le chemin d'accès au fichier de police.
    String fontFile = "geo_1.ttf";

    // Spécifiez la police par défaut du fichier.
    PdfSaveOptions options = new PdfSaveOptions();
    options.setFontsSubsystem(DocumentFontsSubsystem.usingDefaultFontFromFile(fontFile));

    // Enregistrez le document au format PDF.
    oneFile.save("SaveUsingDocumentFontsSubsystemWithDefaultFontFromFile_out.pdf", options);
}
```

Dans cette étape :
- Le fichier de police "geo_1.ttf" est chargé.
- La police par défaut est spécifiée à partir du fichier de police chargé.
- Le document est enregistré au format PDF avec la police spécifiée.

## Étape 3 : Enregistrer à l'aide du sous-système de polices de document avec la police par défaut de Stream

Cette étape montre comment enregistrer un document au format PDF à l'aide d'une police par défaut chargée à partir d'un flux.

```java
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontFromStream() throws IOException
{
    // Chargez le document dans Aspose.Note.
    Document oneFile = new Document("missing-font.one");

    // Spécifiez le chemin d'accès au fichier de police.
    String fontFile = "geo_1.ttf";

    // Chargez le fichier de police sous forme de flux.
    InputStream stream = new FileInputStream(fontFile);

    try
    {
        // Spécifiez la police par défaut du flux.
        PdfSaveOptions options = new PdfSaveOptions();
        options.setFontsSubsystem(DocumentFontsSubsystem.usingDefaultFontFromStream(stream));

        // Enregistrez le document au format PDF.
        oneFile.save("SaveUsingDocumentFontsSubsystemWithDefaultFontFromStream_out.pdf", options);
    }
    catch (Exception e)
    {
        stream.close();
    }
}
```

Dans cette étape :
- Le fichier de police "geo_1.ttf" est chargé sous forme de flux.
- La police par défaut est spécifiée à partir du flux chargé.
- Le document est enregistré au format PDF avec la police spécifiée.

## Conclusion

Dans ce didacticiel, nous avons appris à enregistrer des documents OneNote à l'aide du sous-système de polices spécifié en Java à l'aide d'Aspose.Note. En suivant ces étapes, vous pouvez garantir une représentation cohérente des polices sur différentes plates-formes lors de l'exportation ou de l'enregistrement de vos documents.

## FAQ

### Q1 : Puis-je spécifier différentes polices pour différentes parties du document ?

A1 : Oui, vous pouvez spécifier différentes polices pour différentes parties du document à l'aide d'Aspose.Note pour Java.

### Q2 : Aspose.Note est-il compatible avec toutes les versions de OneNote ?

A2 : Aspose.Note prend en charge différentes versions de OneNote, garantissant la compatibilité entre différents environnements.

### Q3 : Comment puis-je gérer les polices manquantes lors de l'enregistrement de documents ?

A3 : Aspose.Note fournit des options pour spécifier les polices par défaut afin de gérer efficacement les polices manquantes lors de l'enregistrement du document.

### Q4 : Puis-je personnaliser les propriétés de la police telles que la taille et le style ?

A4 : Oui, vous pouvez personnaliser les propriétés de police telles que la taille, le style et la couleur à l'aide d'Aspose.Note pour Java.

### Q5 : Existe-t-il une version d'essai disponible pour Aspose.Note pour Java ?

A5 : Oui, vous pouvez obtenir un essai gratuit d'Aspose.Note pour Java sur le site Web.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
