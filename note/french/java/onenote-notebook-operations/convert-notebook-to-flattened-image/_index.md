---
date: 2025-12-25
description: Apprenez à convertir OneNote en PNG avec Aspose.Note pour Java. Ce guide
  montre comment définir la résolution de l'image, aplatir un carnet et enregistrer
  OneNote en tant qu'image de manière efficace.
linktitle: How to Convert OneNote to PNG – Flatten Notebook to Image with Aspose.Note
second_title: Aspose.Note Java API
title: Comment convertir OneNote en PNG – Aplatir le carnet en image avec Aspose.Note
url: /fr/java/onenote-notebook-operations/convert-notebook-to-flattened-image/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Convertir le carnet de notes en image aplatie dans OneNote - Aspose.Note

## Introduction

Dans ce tutoriel, vous découvrirez comment **convertir OneNote en PNG** en transformant un carnet complet en une image aplatie unique à l'aide d'Aspose.Note pour Java. Cette approche est idéale lorsque vous devez partager un carnet sous forme d'image statique, l'intégrer dans des rapports ou l'archiver sans perdre aucun détail visuel.

## Réponses rapides
- **Qu'est-ce que « aplatir le carnet » signifie ?** Il fusionne tous les éléments de page en une seule image raster.  
- **Quel format est utilisé ?** PNG est le format par défaut, offrant une qualité sans perte.  
- **Puis-je modifier le DPI ?** Oui, utilisez `setResolution` sur le `ImageSaveOptions`.  
- **Ai-je besoin d'une licence ?** Un essai gratuit suffit pour l'évaluation ; une licence commerciale est requise pour la production.  
- **Cette fonctionnalité est‑elle prise en charge sur tous les systèmes d'exploitation ?** L'API Java fonctionne partout où Java fonctionne.

## Qu'est-ce que la conversion de OneNote en PNG ?

Convertir OneNote en PNG crée une représentation bitmap de chaque page du carnet, en préservant le texte, les dessins et les objets incorporés dans un fichier image unique. Cela est particulièrement utile pour la documentation, les présentations ou les archives de conformité.

## Pourquoi convertir OneNote en PNG avec Aspose.Note ?

- **Fidélité totale** – Tous les éléments visuels sont conservés.  
- **Sortie en un seul fichier** – Aucun besoin de gérer plusieurs fichiers de pages.  
- **Résolution personnalisable** – Ajustez le DPI pour répondre aux exigences de qualité.  
- **Pas d'installation d'Office** – Fonctionne complètement indépendamment de Microsoft OneNote.

## Prérequis

Avant de commencer, assurez-vous de disposer de ce qui suit :

1. Java Development Kit (JDK) installé sur votre système.  
2. Bibliothèque Aspose.Note pour Java téléchargée et configurée dans votre projet Java. Vous pouvez télécharger la bibliothèque depuis [ici](https://releases.aspose.com/note/java/).  
3. Connaissances de base en programmation Java.

## Importer les packages

Pour commencer, vous devez importer les packages nécessaires depuis Aspose.Note pour Java :

```java
import java.io.IOException;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.Notebook;
import com.aspose.note.NotebookImageSaveOptions;
import com.aspose.note.SaveFormat;
```

## Étape 1 : Configurer le répertoire du document

Tout d'abord, définissez le répertoire où se trouve votre fichier de carnet :

```java
String dataDir = "Your Document Directory";
```

Remplacez `"Your Document Directory"` par le chemin vers votre fichier de carnet.

## Étape 2 : Charger le carnet

Ensuite, chargez le fichier du carnet en utilisant la classe `Notebook` :

```java
Notebook notebook = new Notebook(dataDir + "test.onetoc2");
```

Assurez‑vous de remplacer `"test.onetoc2"` par le nom de votre fichier de carnet.

## Étape 3 : Définir les options d'enregistrement d'image

Maintenant, configurez les options pour enregistrer le carnet en tant qu'image. Nous spécifierons le format d'enregistrement comme PNG et définirons la résolution à 400 DPI :

```java
NotebookImageSaveOptions saveOptions = new NotebookImageSaveOptions(SaveFormat.Png);
ImageSaveOptions documentSaveOptions = saveOptions.getDocumentSaveOptions();
documentSaveOptions.setResolution(400);
```

Vous pouvez ajuster la résolution selon vos besoins. C'est ici que vous **définissez la résolution de l'image** pour contrôler la qualité de sortie.

## Étape 4 : Aplatir le carnet

Pour garantir que tous les éléments soient aplatis en une seule image, définissez l'option `flatten` sur `true` :

```java
saveOptions.setFlatten(true);
```

Définir `flatten` à `true` garantit que le PNG résultant conserve la mise en page exacte de votre carnet.

## Étape 5 : Enregistrer l'image

Enfin, enregistrez le carnet en tant qu'image aplatie :

```java
notebook.save(dataDir + "ExportImageasFlattenedNotebook_out.png", saveOptions);
```

Remplacez `"ExportImageasFlattenedNotebook_out.png"` par le nom de fichier de sortie souhaité. Cette étape **enregistre OneNote en tant qu'image** que vous pouvez partager ou intégrer n'importe où.

## Cas d'utilisation courants

- **Documentation :** Intégrez l'image du carnet dans les manuels techniques ou les guides d'utilisateur.  
- **Présentations :** Utilisez une diapositive PNG haute résolution dans PowerPoint sans vous soucier de la compatibilité des polices ou des objets.  
- **Archivage :** Conservez un instantané en lecture seule d'un carnet pour les audits de conformité.

## Conseils de dépannage

- **Fichier introuvable :** Vérifiez à nouveau le chemin `dataDir` et assurez‑vous que le fichier `.onetoc2` existe.  
- **Image de basse qualité :** Augmentez le DPI en modifiant `documentSaveOptions.setResolution(600);`.  
- **Éléments manquants :** Vérifiez que `saveOptions.setFlatten(true);` est activé ; sinon, certaines couches peuvent rester séparées.

## Foire aux questions

**Q1 : Puis‑je ajuster la résolution de l'image de sortie ?**  
R1 : Oui, vous pouvez ajuster la résolution selon vos besoins en modifiant le paramètre de la méthode `setResolution`.

**Q2 : Aspose.Note prend‑il en charge d'autres formats d'image pour l'exportation ?**  
R2 : Oui, Aspose.Note prend en charge divers formats d'image tels que PNG, JPEG, BMP, etc., pour l'exportation de carnets.

**Q3 : Puis‑je personnaliser davantage l'image de sortie ?**  
R3 : Oui, Aspose.Note offre de nombreuses options pour personnaliser l'image de sortie, y compris la taille de page, l'orientation et les paramètres de qualité.

**Q4 : Existe‑t‑il une version d'essai disponible pour Aspose.Note pour Java ?**  
R4 : Oui, vous pouvez obtenir une version d'essai gratuite depuis [ici](https://releases.aspose.com/).

**Q5 : Où puis‑je trouver du support pour Aspose.Note pour Java ?**  
R5 : Vous pouvez trouver du support et des ressources sur le forum Aspose.Note [ici](https://forum.aspose.com/c/note/28).

---

**Dernière mise à jour :** 2025-12-25  
**Testé avec :** Aspose.Note for Java 24.12  
**Auteur :** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}