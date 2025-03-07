---
title: Créez un document OneNote et enregistrez-le au format HTML dans Aspose.Note
linktitle: Créez un document OneNote et enregistrez-le au format HTML dans Aspose.Note
second_title: API Aspose.Note .NET
description: Découvrez comment créer et enregistrer des documents Microsoft OneNote au format HTML dans des applications .NET à l'aide de l'API Aspose.Note. Suivez notre didacticiel complet avec des exemples étape par étape.
weight: 14
url: /fr/net/loading-and-saving-operations/create-onenote-doc-save-to-html/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Créez un document OneNote et enregistrez-le au format HTML dans Aspose.Note

## Introduction

Aspose.Note pour .NET est une API puissante qui permet aux développeurs de travailler avec des documents Microsoft OneNote par programmation dans leurs applications .NET. Avec Aspose.Note, vous pouvez créer, manipuler et convertir des fichiers OneNote sans effort. Dans ce didacticiel, nous allons explorer comment créer un document OneNote et l'enregistrer au format HTML à l'aide de diverses options fournies par l'API Aspose.Note pour .NET.

## Conditions préalables

Avant de commencer, assurez-vous de disposer des prérequis suivants :

- Connaissance de base du langage de programmation C#.
- Visual Studio installé sur votre système.
-  Aspose.Note pour l'API .NET installée dans votre projet. Vous pouvez le télécharger depuis[ici](https://releases.aspose.com/note/net/).
- Familiarité avec la structure des documents Microsoft OneNote.

## Importer des espaces de noms

Avant de plonger dans la partie codage, importons les espaces de noms nécessaires :

```csharp
using System;
using System.Drawing;
using System.Globalization;
using System.IO;

using Aspose.Note.Saving;
using Aspose.Note.Saving.Html;

```

Maintenant, décomposons chaque exemple en plusieurs étapes et voyons comment créer un document OneNote et l'enregistrer au format HTML à l'aide d'Aspose.Note pour .NET.

## Étape 1 : Créer un document OneNote avec les options par défaut

```csharp
public static void CreateAndSaveToHTMLUsingDefaultOptions()
{
    // Initialiser le document OneNote
    Document doc = new Document();
    Page page = doc.AppendChildLast(new Page());

    // Style par défaut pour tout le texte du document.
    ParagraphStyle textStyle = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
    page.Title = new Title()
    {
        TitleText = new RichText() { Text = "Title text.", ParagraphStyle = textStyle },
        TitleDate = new RichText() { Text = new DateTime(2011, 11, 11).ToString("D", CultureInfo.InvariantCulture), ParagraphStyle = textStyle },
        TitleTime = new RichText() { Text = "12:34", ParagraphStyle = textStyle }
    };

    // Enregistrer au format HTML
    string dataDir = "Your Document Directory";
    string outputPath = Path.Combine(dataDir, "CreateOneNoteDocAndSaveToHTML_out.html");
    doc.Save(outputPath);

    Console.WriteLine("\nOneNote document created successfully.\nFile saved at " + outputPath);
}
```

Dans cette étape, nous initialisons un nouveau document OneNote, ajoutons une page avec un titre et l'enregistrons au format HTML en utilisant les options par défaut.

## Étape 2 : créer et enregistrer une plage de pages spécifique au format HTML

```csharp
public static void CreateAndSavePageRange()
{
    // Initialiser le document OneNote
    Document doc = new Document();
    Page page = doc.AppendChildLast(new Page());

    // Style par défaut pour tout le texte du document.
    ParagraphStyle textStyle = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
    page.Title = new Title()
    {
        TitleText = new RichText() { Text = "Title text.", ParagraphStyle = textStyle },
        TitleDate = new RichText() { Text = new DateTime(2011, 11, 11).ToString("D", CultureInfo.InvariantCulture), ParagraphStyle = textStyle },
        TitleTime = new RichText() { Text = "12:34", ParagraphStyle = textStyle }
    };

    // Enregistrer au format HTML
    string dataDir = "Your Document Directory";
    string outputPath = Path.Combine(dataDir, "CreateAndSavePageRange_out.html");
    doc.Save(outputPath, new HtmlSaveOptions { PageCount = 1, PageIndex = 0 });

    Console.WriteLine("\nOneNote document created successfully and saved as page range.\nFile saved at " + outputPath);
}
```

Ici, nous montrons comment créer un document et enregistrer une plage de pages spécifique au format HTML.

## Étape 3 : Enregistrer au format HTML dans le flux de mémoire avec les ressources intégrées

```csharp
public static void SaveAsHTMLToMemoryStreamWithEmbeddedResources()
{
    // Charger le document OneNote
    string dataDir = "Your Document Directory";
    var document = new Document(Path.Combine(dataDir, "Aspose.one"));

    // Spécifier les options d'enregistrement HTML
    var options = new HtmlSaveOptions()
    {
        ExportCss = ResourceExportType.ExportEmbedded,
        ExportFonts = ResourceExportType.ExportEmbedded,
        ExportImages = ResourceExportType.ExportEmbedded,
        FontFaceTypes = FontFaceType.Ttf
    };

    // Enregistrez le document dans un flux mémoire
    var memoryStream = new MemoryStream();
    document.Save(memoryStream, options);
}
```

Cette étape illustre comment enregistrer un document OneNote au format HTML avec des ressources intégrées (CSS, polices et images) dans un flux mémoire.

## Étape 4 : Enregistrer au format HTML dans un fichier avec des ressources dans des fichiers séparés

```csharp
public static void SaveAsHTMLToFileWithResourcesInSeparateFiles()
{
    // Charger le document OneNote
    string dataDir = "Your Document Directory";
    var document = new Document(Path.Combine(dataDir, "Aspose.one"));

    // Spécifier les options d'enregistrement HTML
    var options = new HtmlSaveOptions()
    {
        ExportCss = ResourceExportType.ExportAsStream,
        ExportFonts = ResourceExportType.ExportAsStream,
        ExportImages = ResourceExportType.ExportAsStream,
        FontFaceTypes = FontFaceType.Ttf
    };

    // Enregistrez le document dans un fichier HTML avec les ressources stockées dans des fichiers séparés
    document.Save(Path.Combine(dataDir, "document_out.html"), options);
}
```

Dans cette étape, nous enregistrons un document OneNote au format HTML avec toutes les ressources (CSS, polices et images) stockées dans des fichiers séparés.

## Étape 5 : Enregistrer au format HTML dans le flux de mémoire avec des rappels pour enregistrer les ressources

```csharp
public static void SaveAsHTMLToMemoryStreamWithCallBacksToSaveResources()
{
    // Spécifier la configuration des rappels d'enregistrement
    var savingCallbacks = new UserSavingCallbacks()
    {
        RootFolder = "documentFolder",
        CssFolder = "css",
        KeepCssStreamOpened = true,
        ImagesFolder = "images",
        FontsFolder = "fonts"
    };

    // Spécifier les options d'enregistrement HTML
    var options = new HtmlSaveOptions
    {
        FontFaceTypes = FontFaceType.Ttf,
        CssSavingCallback = savingCallbacks,
        FontSavingCallback = savingCallbacks,
        ImageSavingCallback = savingCallbacks
    };

    // Charger le document OneNote
    string dataDir = "Your Document Directory";
    var document = new Document(Path.Combine(dataDir, "Aspose.one"));

    // Enregistrez le document au format HTML avec des ressources gérées par des rappels définis par l'utilisateur
    using (var stream = File.Create(Path.Combine(savingCallbacks.RootFolder, "document.html")))
    {
        document.Save(stream, options);
    }

    // Ajouter manuellement des données au flux CSS
    using (var writer = new StreamWriter(savingCallbacks.CssStream))
    {
        writer.WriteLine();
        writer.WriteLine("/* This line is appended to stream manually by user */");
    }
}
```

Ici, nous montrons comment enregistrer un document OneNote au format HTML avec des ressources gérées par des rappels définis par l'utilisateur.

## Conclusion

Dans cet article, nous avons expliqué comment utiliser des documents OneNote et les enregistrer au format HTML à l'aide d'Aspose.Note pour .NET. En suivant le guide étape par étape, vous pouvez facilement

 intégrez cette fonctionnalité dans vos applications .NET, vous permettant de manipuler efficacement les fichiers OneNote.

## FAQ

### Q1 : Puis-je personnaliser l'apparence du fichier HTML enregistré ?

A1 : Oui, vous pouvez personnaliser l'apparence en modifiant les feuilles de style CSS générées lors du processus de conversion.

### Q2 : Aspose.Note prend-il en charge la conversion vers d’autres formats que HTML ?

A2 : Oui, Aspose.Note prend en charge la conversion vers divers formats tels que PDF, images et documents Microsoft Word.

### Q3 : Aspose.Note est-il compatible avec les applications .NET Core ?

A3 : Oui, Aspose.Note est compatible avec les applications .NET Framework et .NET Core.

### Q4 : Puis-je extraire du texte et des images de documents OneNote à l’aide d’Aspose.Note ?

A4 : Oui, vous pouvez extraire du texte et des images ainsi qu'effectuer diverses autres manipulations à l'aide de l'API Aspose.Note.

### Q5 : Existe-t-il une version d'essai disponible pour tester les fonctionnalités d'Aspose.Note ?

 A5 : Oui, vous pouvez télécharger une version d'essai gratuite à partir de[ici](https://releases.aspose.com/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
