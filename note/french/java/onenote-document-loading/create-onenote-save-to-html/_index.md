---
date: 2025-12-02
description: Apprenez comment exporter les polices lors de l’enregistrement de OneNote
  au format HTML à l’aide d’Aspose.Note pour Java. Ce guide vous montre comment créer
  OneNote de manière programmatique et intégrer les polices, le CSS et les images.
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

# Comment exporter les polices lors de l’enregistrement de OneNote en HTML – Java

## Introduction

Dans ce tutoriel, vous découvrirez **comment exporter les polices** lorsque vous **enregistrez OneNote en HTML** à l’aide d’Aspose.Note pour Java. Nous parcourrons la création d’un document OneNote de façon programmatique, la configuration des options d’enregistrement HTML, et l’intégration des fichiers de police requis afin que le HTML résultant ressemble exactement aux pages OneNote d’origine. Cette approche est idéale lorsque vous devez préserver la fidélité visuelle du contenu OneNote dans un format adapté au web.

## Quick Answers
- **Quelle bibliothèque gère l’exportation ?** Aspose.Note pour Java  
- **Les polices peuvent‑elles être intégrées dans le HTML ?** Oui – définissez `ExportFonts` sur `ExportEmbedded`  
- **Ai‑je besoin d’une licence pour la production ?** Une licence valide d’Aspose.Note est requise pour une utilisation commerciale  
- **Quelle version de Java est prise en charge ?** Java 8 ou supérieure  
- **Est‑il possible d’enregistrer les ressources dans des fichiers séparés ?** Absolument – configurez `ResourceExportType` en conséquence  

## Qu’est‑ce que « comment exporter les polices » dans le contexte de la conversion OneNote en HTML ?

Lorsque vous convertissez un bloc‑notes OneNote en HTML, l’apparence visuelle dépend du CSS, des images et surtout des polices utilisées dans les pages d’origine. **Exporter les polices** signifie intégrer les fichiers de police (par ex., TTF) directement dans le package HTML afin que les navigateurs puissent rendre le texte exactement comme il apparaît dans OneNote, même si l’utilisateur final n’a pas ces polices installées localement.

## Pourquoi créer un document OneNote de façon programmatique et l’enregistrer en HTML ?

- **Automatisation :** Générer des rapports, de la documentation ou des articles de base de connaissances depuis OneNote sans copier‑coller manuellement.  
- **Cohérence :** Conserver la mise en page, le style et les polices personnalisées sur tous les appareils.  
- **Portabilité :** Le HTML est universellement affichable — pas besoin du client OneNote.  

## Prérequis

1. Java Development Kit (JDK) 8 ou plus récent installé.  
2. Bibliothèque Aspose.Note pour Java – téléchargez‑la depuis [here](https://releases.aspose.com/note/java/).  
3. Un fichier OneNote d’exemple (`.one`) à charger, ou vous pouvez créer un nouveau fichier de façon programmatique.  

## Import Packages

Tout d’abord, importez les classes requises dans votre projet Java :

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

Voici un guide étape par étape qui montre **comment exporter les polices** ainsi que d’autres ressources.

### Step 1: Create a OneNote document programmatically  

```java
Document document = new Document("Path_to_your_sample_one_file");
```

Cette ligne charge un fichier `.one` existant. Si vous devez **créer un OneNote de façon programmatique**, vous pouvez instancier un nouvel objet `Document` et ajouter des sections/pages via l’API (non montré ici afin de rester concentré sur l’exportation des polices).

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

- `setExportFonts(ResourceExportType.ExportEmbedded)` indique à Aspose.Note d’**exporter les polices** directement dans le package HTML.  
- `setFontFaceTypes(FontFaceType.Ttf)` garantit que les polices TrueType sont utilisées, ce qui bénéficie d’une large compatibilité navigateur.

### Step 3: Save as HTML with separate resource files (still exporting fonts)  

```java
HtmlSaveOptions options = new HtmlSaveOptions();
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);

document.save("output_directory/document.html", options);
```

Même si le CSS et les images sont intégrés, vous pouvez changer `ResourceExportType` en `ExportExternal` si vous préférez des fichiers séparés pour un cache plus facile. La partie clé — **l’exportation des polices** — reste inchangée.

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

## Common Issues & Tips

- **Polices manquantes dans la sortie :** Vérifiez que `setExportFonts(ResourceExportType.ExportEmbedded)` est bien défini et que le fichier OneNote source utilise réellement des polices intégrées.  
- **Fichiers HTML volumineux :** L’intégration des polices peut augmenter la taille. Si la bande passante est un problème, passez `ExportFonts` à `ExportExternal` et hébergez les polices sur un CDN.  
- **Erreurs d’implémentation des callbacks :** Assurez‑vous que vos classes de callback écrivent correctement le flux et ferment les ressources afin d’éviter la corruption des fichiers.  

## Frequently Asked Questions

**Q : Puis‑je convertir plusieurs documents OneNote en HTML en une seule fois ?**  
R : Oui, parcourez chaque instance `Document` et appliquez les mêmes `HtmlSaveOptions`.  

**Q : Aspose.Note pour Java prend‑il en charge d’autres formats de sortie que le HTML ?**  
R : Absolument. Vous pouvez exporter en PDF, DOCX, PNG, JPEG, et bien d’autres en utilisant les options d’enregistrement appropriées.  

**Q : Existe‑t‑il une version d’essai d’Aspose.Note pour Java ?**  
R : Oui, téléchargez une version d’essai gratuite depuis [here](https://releases.aspose.com/).  

**Q : Où puis‑je obtenir du support pour Aspose.Note pour Java ?**  
R : Consultez le [Aspose.Note forum](https://forum.aspose.com/c/note/28) pour l’aide de la communauté et le support officiel.  

**Q : Comment puis‑je acheter une licence pour Aspose.Note pour Java ?**  
R : Les licences sont disponibles sur le [site Aspose](https://purchase.aspose.com/buy).  

## Conclusion

Vous savez maintenant **comment exporter les polices** tout en **enregistrant OneNote en HTML** à l’aide d’Aspose.Note pour Java. En configurant `HtmlSaveOptions` et éventuellement en utilisant des callbacks, vous pouvez préserver l’aspect exact de vos pages OneNote — y compris les polices personnalisées — lors de leur diffusion sur le web. N’hésitez pas à expérimenter avec différents réglages de `ResourceExportType` pour répondre aux exigences de performance et de stockage de votre projet.

---

**Last Updated:** 2025-12-02  
**Tested With:** Aspose.Note for Java 24.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}