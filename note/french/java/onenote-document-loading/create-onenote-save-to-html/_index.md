---
date: 2026-02-07
description: Apprenez à exporter les polices lors de l’enregistrement de OneNote au
  format HTML avec Aspose.Note pour Java. Ce guide vous montre comment créer OneNote
  de manière programmatique et intégrer les polices, le CSS et les images.
linktitle: How to Export Fonts When Saving OneNote as HTML – Java
second_title: Aspose.Note Java API
title: Comment exporter les polices lors de l’enregistrement de OneNote en HTML –
  Java
url: /fr/java/onenote-document-loading/create-onenote-save-to-html/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Comment exporter les polices lors de l'enregistrement de OneNote au format HTML – Java

## Introduction

Dans ce tutoriel, vous découvrirez **comment exporter les polices** lorsque vous **enregistrez OneNote au format HTML** en utilisant Aspose.Note for Java. Nous parcourrons la création d'un document OneNote programmatique, la configuration des options d'enregistrement HTML, et l'intégration des fichiers de police requis afin que le HTML résultant ressemble exactement aux pages OneNote originales. Cette approche est idéale lorsque vous devez préserver la fidélité visuelle du contenu OneNote dans un format adapté au web.

## Quick Answers
- **Quelle bibliothèque gère l'exportation ?** Aspose.Note for Java  
- **Les polices peuvent-elles être intégrées dans le HTML ?** Oui – définissez `ExportFonts` sur `ExportEmbedded`  
- **Ai-je besoin d'une licence pour la production ?** Une licence valide d'Aspose.Note est requise pour une utilisation commerciale  
- **Quelle version de Java est prise en charge ?** Java 8 ou supérieure  
- **Est-il possible d'enregistrer les ressources dans des fichiers séparés ?** Absolument – configurez `ResourceExportType` en conséquence  

## Qu’est‑ce que « comment exporter les polices » dans le contexte de la conversion OneNote en HTML ?

Lorsque vous convertissez un carnet OneNote en HTML, l'apparence visuelle dépend du CSS, des images et surtout des polices utilisées dans les pages originales. **Exporter les polices** signifie intégrer les fichiers de police (par ex., TTF) directement dans le package HTML afin que les navigateurs puissent rendre le texte exactement comme il apparaît dans OneNote, même si l'utilisateur final n'a pas ces polices installées localement.

## Pourquoi créer un OneNote programmatique et l’enregistrer en HTML ?

- **Automatisation :** Générer des rapports, de la documentation ou des articles de base de connaissances à partir de OneNote sans copier‑coller manuellement.  
- **Cohérence :** Conserver la mise en page, le style et les polices personnalisées sur tous les appareils.  
- **Portabilité :** Le HTML est universellement affichable—pas besoin du client OneNote.  

## Prérequis

1. Java Development Kit (JDK) 8 ou plus récent installé.  
2. Bibliothèque Aspose.Note for Java – téléchargez‑la depuis [here](https://releases.aspose.com/note/java/).  
3. Un fichier OneNote d'exemple (`.one`) à charger, ou vous pouvez créer un nouveau programmétiquement.  

## Import Packages

First, import the required classes into your Java project:

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

## How to Export Fonts While Saving OneNote as HTML?

Below is a step‑by‑step guide that shows you **how to export fonts** and other resources.

### Step 1: Create a OneNote document programmatically  

```java
Document document = new Document("Path_to_your_sample_one_file");
```

Cette ligne charge un fichier `.one` existant. Si vous devez **créer un OneNote programmétiquement**, vous pouvez instancier un nouvel objet `Document` et ajouter des sections/pages via l'API (non montré ici afin de garder le focus sur l'exportation des polices).

### Step 2: Save to a memory stream with embedded fonts  

```java
HtmlSaveOptions options = new HtmlSaveOptions();
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);
options.setFontFaceTypes(FontFaceType.Ttf);

ByteArrayOutputStream outputStream = new ByteArrayOutputStream();
document.save(outputStream, options);
```

- `setExportFonts(ResourceExportType.ExportEmbedded)` indique à Aspose.Note d'**exporter les polices** directement dans le package HTML.  
- `setFontFaceTypes(FontFaceType.Ttf)` garantit que des polices TrueType sont utilisées, ce qui bénéficie d’un large support navigateur.

### Step 3: Save as HTML with separate resource files (still exporting fonts)  

```java
HtmlSaveOptions options = new HtmlSaveOptions();
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);

document.save("output_directory/document.html", options);
```

Même si le CSS et les images sont intégrés, vous pouvez changer le `ResourceExportType` en `ExportExternal` si vous préférez des fichiers séparés pour un cache plus facile. La partie clé—**l'exportation des polices**—reste inchangée.

### Step 4: Use callbacks to control where each resource is stored  

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

La classe `UserSavingCallbacks` (vous devrez implémenter `ICssSavingCallback`, `IImageSavingCallback` et `IFontSavingCallback`) vous donne un contrôle total sur la structure des dossiers, vous permettant de placer les polices dans un répertoire dédié `fonts` tout en **exportant correctement les polices**.

## How to embed custom fonts when converting OneNote to HTML

Intégrer des polices personnalisées garantit que le rendu HTML correspond à la mise en page originale de OneNote, même sur des appareils qui ne possèdent pas ces polices. En utilisant `ExportEmbedded` conjointement avec `FontFaceType.Ttf`, les fichiers TrueType sont encodés en base‑64 et insérés directement dans le CSS généré, éliminant ainsi le besoin d’héberger les polices de façon externe.

## Using ResourceExportType to control resource export

`ResourceExportType` vous permet de décider si le CSS, les images et les polices sont stockés **à l'intérieur** du fichier HTML (`ExportEmbedded`) ou enregistrés comme fichiers **externes** (`ExportExternal`). Choisissez `ExportEmbedded` pour une solution monofichier, ou `ExportExternal` lorsque vous souhaitez profiter du cache du navigateur pour de gros actifs.

## Creating OneNote programmatically for HTML export

Si vous partez de zéro, vous pouvez construire un document OneNote entièrement en code, ajouter des sections, des pages et du texte enrichi, puis appliquer les mêmes `HtmlSaveOptions` présentés ci‑dessus. Cela vous offre une automatisation de bout en bout : de la génération des données à une sortie HTML entièrement stylisée avec des polices personnalisées intégrées.

## Common Issues & Tips

- **Polices manquantes dans la sortie :** Vérifiez que `setExportFonts(ResourceExportType.ExportEmbedded)` est bien défini et que le fichier OneNote source utilise réellement des polices intégrées.  
- **Fichiers HTML volumineux :** L’intégration des polices peut augmenter la taille. Si la bande passante est un problème, passez `ExportFonts` à `ExportExternal` et hébergez les polices sur un CDN.  
- **Erreurs d’implémentation des callbacks :** Assurez‑vous que vos classes de callback écrivent correctement le flux et ferment les ressources afin d’éviter la corruption des fichiers.  

## Frequently Asked Questions

**Q : Puis‑je convertir plusieurs documents OneNote en HTML en une seule opération ?**  
R : Oui, parcourez chaque instance `Document` et appliquez les mêmes `HtmlSaveOptions`.  

**Q : Aspose.Note for Java prend‑il en charge d’autres formats de sortie que le HTML ?**  
R : Absolument. Vous pouvez exporter en PDF, DOCX, PNG, JPEG, et plus encore en utilisant les options d’enregistrement appropriées.  

**Q : Existe‑t‑il une version d’essai disponible pour Aspose.Note for Java ?**  
R : Oui, téléchargez une version d’essai gratuite depuis [here](https://releases.aspose.com/).  

**Q : Où puis‑je obtenir du support pour Aspose.Note for Java ?**  
R : Consultez le [Aspose.Note forum](https://forum.aspose.com/c/note/28) pour l’aide communautaire et officielle.  

**Q : Comment puis‑je acheter une licence pour Aspose.Note for Java ?**  
R : Les licences sont disponibles sur le [site Aspose](https://purchase.aspose.com/buy).  

## Conclusion

Vous savez maintenant **comment exporter les polices** tout en **enregistrant OneNote au format HTML** à l’aide d’Aspose.Note for Java. En configurant `HtmlSaveOptions` et éventuellement en utilisant des callbacks, vous pouvez préserver l’aspect exact de vos pages OneNote—y compris les polices personnalisées—lors de leur diffusion sur le web. N’hésitez pas à expérimenter différents paramètres `ResourceExportType` pour répondre aux exigences de performance et de stockage de votre projet.

---

**Last Updated:** 2026-02-07  
**Tested With:** Aspose.Note for Java 24.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}