---
title: Créer un document OneNote et l'enregistrer au format HTML - Java
linktitle: Créer un document OneNote et l'enregistrer au format HTML - Java
second_title: API Java Aspose.Note
description: Apprenez à créer et à enregistrer des documents OneNote au format HTML à l'aide d'Aspose.Note pour Java. Intégrez-vous aux applications Java pour la gestion programmatique des fichiers OneNote.

type: docs
weight: 18
url: /fr/java/onenote-document-loading/create-onenote-save-to-html/
---
## Introduction

Aspose.Note pour Java est une bibliothèque puissante qui permet aux développeurs de travailler avec des fichiers Microsoft OneNote par programme. Dans ce didacticiel, nous allons explorer comment créer un document OneNote et l'enregistrer au format HTML à l'aide d'Aspose.Note pour Java.

## Conditions préalables

Avant de commencer, assurez-vous d'avoir les éléments suivants :

1. Kit de développement Java (JDK) installé sur votre système.
2.  Aspose.Note pour la bibliothèque Java. Vous pouvez le télécharger depuis[ici](https://releases.aspose.com/note/java/).
3. Connaissance de base de la programmation Java.

## Importer des packages

Tout d'abord, importez les packages nécessaires dans votre projet Java :

```java
import java.io.ByteArrayOutputStream;
import java.io.File;
import java.io.FileOutputStream;
import java.io.IOException;
import java.io.OutputStream;
import java.io.OutputStreamWriter;
import java.nio.file.Paths;
import com.aspose.note.CssSavingArgs;
import com.aspose.note.Document;
import com.aspose.note.FontFaceType;
import com.aspose.note.FontSavingArgs;
import com.aspose.note.HtmlSaveOptions;
import com.aspose.note.ICssSavingCallback;
import com.aspose.note.IFontSavingCallback;
import com.aspose.note.IImageSavingCallback;
import com.aspose.note.ImageSavingArgs;
import com.aspose.note.ResourceExportType;
```

## Étape 1 : créer un objet de document OneNote

```java
Document document = new Document("Path_to_your_sample_one_file");
```

 Ce code initialise un`Document` objet en chargeant un exemple de fichier OneNote.

## Étape 2 : Enregistrer au format HTML dans le flux de mémoire

```java
HtmlSaveOptions options = new HtmlSaveOptions();
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);
options.setFontFaceTypes(FontFaceType.Ttf);

ByteArrayOutputStream outputStream = new ByteArrayOutputStream();
document.save(outputStream, options);
```

Ici, nous configurons les options d'enregistrement HTML et enregistrons le document dans un flux mémoire.

## Étape 3 : Enregistrer au format HTML avec les ressources dans des fichiers séparés

```java
HtmlSaveOptions options = new HtmlSaveOptions();
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);

document.save("output_directory/document.html", options);
```

Cette étape enregistre le document au format HTML avec des ressources telles que CSS, polices et images dans des fichiers séparés.

## Étape 4 : Enregistrer au format HTML dans le flux de mémoire avec des rappels pour enregistrer les ressources

```java
Document document = new Document("Path_to_your_sample_one_file");

UserSavingCallbacks savingCallbacks = new UserSavingCallbacks();
savingCallbacks.setRootFolder("documentFolder");
savingCallbacks.setCssFolder("css");
savingCallbacks.setKeepCssStreamOpened(true);
savingCallbacks.setImagesFolder("images");
savingCallbacks.setFontsFolder("fonts");

HtmlSaveOptions options = new HtmlSaveOptions();
options.setFontFaceTypes(FontFaceType.Ttf);
options.setCssSavingCallback(savingCallbacks);
options.setImageSavingCallback(savingCallbacks);
options.setFontSavingCallback(savingCallbacks);
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);

File dir = new File(savingCallbacks.getRootFolder());
if (!dir.exists()) {
    dir.mkdir();
}

document.save(Paths.get(savingCallbacks.getRootFolder(), "document.html").toString(), options);
```

Ici, nous enregistrons le document au format HTML dans un flux mémoire à l'aide de rappels pour gérer l'économie des ressources.

## Conclusion

Toutes nos félicitations! Vous avez appris à créer un document OneNote et à l'enregistrer au format HTML à l'aide d'Aspose.Note pour Java. Vous pouvez désormais intégrer cette fonctionnalité dans vos applications Java pour travailler avec les fichiers OneNote par programme.

## FAQ

### Q1 : Puis-je convertir plusieurs documents OneNote en HTML en une seule fois ?

A1 : Oui, vous pouvez parcourir plusieurs documents et appliquer le processus de sauvegarde de manière itérative.

### Q2 : Aspose.Note pour Java prend-il en charge d'autres formats de sortie que HTML ?

A2 : Oui, Aspose.Note pour Java prend en charge divers formats de sortie, notamment PDF, DOCX et les formats d'image.

### Q3 : Existe-t-il une version d'essai disponible pour Aspose.Note pour Java ?

A3 : Oui, vous pouvez télécharger une version d'essai gratuite à partir de[ici](https://releases.aspose.com/).

### Q4 : Où puis-je obtenir de l'assistance pour Aspose.Note pour Java ?

 A4 : Vous pouvez obtenir de l'aide du[Forum Aspose.Note](https://forum.aspose.com/c/note/28).

### Q5 : Comment puis-je acheter une licence pour Aspose.Note pour Java ?

 A5 : Vous pouvez acheter une licence auprès du[Site Aspose](https://purchase.aspose.com/buy).