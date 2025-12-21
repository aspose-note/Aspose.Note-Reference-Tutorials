---
date: 2025-12-21
description: Apprenez à extraire des images des documents OneNote à l'aide de Java
  avec Aspose.Note. Ce guide étape par étape montre comment extraire des images rapidement
  et de manière fiable.
linktitle: How to Extract Images from OneNote Document using Java
second_title: Aspose.Note Java API
title: Comment extraire des images d’un document OneNote avec Java
url: /fr/java/onenote-hyperlinks-images/extract-images/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Comment extraire des images d’un document OneNote avec Java

## Introduction

Dans ce tutoriel, nous vous guidons à travers **l’extraction d’images** d’un document OneNote en Java à l’aide de la bibliothèque Aspose.Note. Que vous ayez besoin des images pour des rapports, de l’archivage ou un traitement ultérieur, ce guide vous accompagne tout au long du processus.

## Réponses rapides
- **Quelle bibliothèque est recommandée ?** Aspose.Note for Java  
- **Puis‑je extraire des images d’un bloc‑note protégé par mot de passe ?** Oui, Aspose.Note le prend en charge.  
- **Ai‑je besoin d’une licence pour le développement ?** Un essai gratuit suffit pour les tests ; une licence est requise en production.  
- **Quelles versions de Java sont supportées ?** Java 8 et ultérieures (y compris Java 15).  
- **Combien de temps dure l’extraction ?** Généralement quelques secondes pour un bloc‑note standard.

## Qu’est‑ce que l’extraction d’images depuis OneNote ?
Extraire des images consiste à localiser programmatiquement chaque image intégrée dans un fichier OneNote (.one) et à enregistrer chacune d’elles comme fichier image distinct sur le disque. Cela est utile lorsque vous souhaitez réutiliser les graphiques en dehors de l’environnement du bloc‑note.

## Pourquoi extraire des images de OneNote avec Java ?
- **Automatisation :** Traitement par lots de nombreux blocs‑notes sans effort manuel.  
- **Cohérence :** Garantit la même logique d’extraction pour tous les fichiers.  
- **Intégration :** S’associe facilement à d’autres flux de travail Java (par ex., OCR, analyse d’images).  

## Prérequis

Avant de commencer, assurez‑vous de disposer de :

1. **Java Development Kit (JDK)** – Vérifiez que Java est installé sur votre système. Vous pouvez le télécharger et l’installer depuis le [site web](https://www.oracle.com/java/technologies/javase-jdk15-downloads.html).

2. **Bibliothèque Aspose.Note** – Téléchargez et ajoutez la bibliothèque Aspose.Note à votre projet Java. Vous pouvez l’obtenir via le [lien de téléchargement](https://releases.aspose.com/note/java/).

## Importer les packages

Pour commencer, importez les packages nécessaires :

```java
import java.io.IOException;
import java.nio.file.Files;
import java.nio.file.Paths;
import java.util.List;
import com.aspose.note.Document;
import com.aspose.note.Image;
```

## Étape 1 : Charger le document

Tout d’abord, chargez le document OneNote avec Aspose.Note :

```java
String dataDir = "Your Document Directory";
Document doc = new Document(dataDir + "Sample1.one");
```

## Étape 2 : Obtenir toutes les images

Ensuite, récupérez toutes les images du document :

```java
List<Image> list = doc.getChildNodes(Image.class);
System.out.printf("Total Images: %s\n\n", list.size());
```

## Étape 3 : Extraire les images

Parcourez la liste des images et enregistrez chaque image dans un fichier :

```java
for (int i = 0; i < list.size(); i++) {
    Image image = list.get(i);
    String outputFile = "ExtractImages_out" + i + "_" + image.getFileName();
    byte[] buffer = image.getBytes();
    Files.write(Paths.get(dataDir + outputFile), buffer);
    System.out.printf("File saved: %s\n", dataDir);
}
```

## Problèmes courants et solutions
- **Aucune image trouvée :** Vérifiez que le fichier source `.one` contient bien des images intégrées.  
- **Erreurs de permissions de fichier :** Assurez‑vous que le chemin `dataDir` est accessible en écriture.  
- **Formats d’image non pris en charge :** Aspose.Note gère la plupart des formats courants (PNG, JPEG, GIF). Si un format n’est pas supporté, envisagez de convertir le bloc‑note dans OneNote au préalable.

## Conclusion

En suivant les étapes ci‑dessus, vous savez maintenant **comment extraire des images** d’un document OneNote avec Java et la bibliothèque Aspose.Note. Vous pouvez intégrer cette logique dans des applications plus larges, automatiser le traitement par lots ou simplement récupérer des graphiques pour les réutiliser.

## Foire aux questions

**Q : Puis‑je extraire des images de documents OneNote protégés par mot de passe ?**  
R : Oui, Aspose.Note prend en charge l’extraction d’images de blocs‑notes protégés.

**Q : Aspose.Note est‑il compatible avec différentes versions de Java ?**  
R : Aspose.Note fonctionne avec Java 8 et les versions ultérieures, offrant ainsi une grande flexibilité.

**Q : Puis‑je extraire des images de plusieurs documents OneNote en une seule exécution ?**  
R : Absolument. Parcourez une liste de chemins de fichiers et appliquez la même logique d’extraction à chaque document.

**Q : Existe‑t‑il des limites de taille pour les documents OneNote ?**  
R : Aspose.Note gère efficacement les gros blocs‑notes ; il n’y a pas de limite stricte pour l’extraction d’images.

**Q : Aspose.Note permet‑il d’extraire d’autres types de contenu que les images ?**  
R : Oui, vous pouvez également extraire du texte, des pièces jointes et d’autres objets intégrés.

---

**Dernière mise à jour :** 2025-12-21  
**Testé avec :** Aspose.Note for Java 24.12  
**Auteur :** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}