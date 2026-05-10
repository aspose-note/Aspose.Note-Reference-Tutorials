---
date: 2026-02-28
description: Apprenez à extraire les balises des fichiers OneNote à l'aide d'Aspose.Note
  pour Java. Ce tutoriel montre comment charger un fichier OneNote, récupérer les
  balises OneNote et modifier les balises OneNote efficacement.
linktitle: How to Extract Tags from OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: Comment extraire les étiquettes de OneNote avec Aspose.Note
url: /fr/java/onenote-tag-operations/get-node-tags/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Comment extraire les balises d’un document OneNote avec Aspose.Note

## Introduction
Si vous avez besoin de **comment extraire les balises** d’un document OneNote, vous êtes au bon endroit. Dans ce guide, nous passerons en revue le processus complet de chargement d’un fichier OneNote, d’obtention des balises OneNote, et même de modification de ces balises à l’aide d’Aspose.Note pour Java. À la fin du tutoriel, vous pourrez intégrer l’extraction de balises dans n’importe quelle application Java en toute confiance.

## Réponses rapides
- **Quelle est la classe principale pour ouvrir un fichier OneNote ?** `Document`
- **Quelle méthode renvoie tous les nœuds RichText ?** `doc.getChildNodes(RichText.class)`
- **Peut‑on lire la date de création d’un NoteTag ?** Oui, via `noteTag.getCreationTime()`
- **Ai‑je besoin d’une licence pour une utilisation en production ?** Oui, une licence valide d’Aspose.Note est requise
- **L’API est‑elle compatible avec Java 8 et versions ultérieures ?** Absolument, elle prend en charge les versions modernes de Java

## Qu’est‑ce que “comment extraire les balises” dans OneNote ?
Extraire les balises signifie lire les métadonnées (telles que le statut, le libellé, l’icône et les horodatages) que OneNote attache aux paragraphes, cases à cocher ou autres éléments de contenu. Ces balises sont stockées sous forme d’objets `NoteTag` à l’intérieur des nœuds `RichText`.

## Pourquoi utiliser Aspose.Note pour l’extraction de balises ?
- **Aucune installation de OneNote requise** – travaillez directement avec les fichiers .one.
- **Contrôle total** – récupérez, lisez et modifiez les propriétés des balises par programme.
- **Multiplateforme** – fonctionne sur tout système d’exploitation supportant Java.

## Prérequis
- Un environnement de développement Java (JDK 8+).
- La bibliothèque Aspose.Note téléchargée depuis [here](https://releases.aspose.com/note/java/).
- Un document OneNote d’exemple (par ex., `Sample1.one`) placé dans un répertoire connu.

## Importer les packages
Commencez par importer les classes dont vous aurez besoin. Ces imports vous donnent accès à la gestion des documents, aux interfaces de balises et aux nœuds de texte enrichi.

```java
import java.io.IOException;
import java.util.List;
import com.aspose.note.Document;
import com.aspose.note.ITag;
import com.aspose.note.NoteTag;
import com.aspose.note.RichText;
```

## Comment charger un fichier OneNote
La première étape consiste à charger le fichier OneNote dans un objet `Document`.

```java
// The path to the documents directory.
String dataDir = "Your Document Directory";
// Load the document into Aspose.Note
Document doc = new Document(dataDir + "Sample1.one");
// Get all RichText nodes
List<RichText> nodes = doc.getChildNodes(RichText.class);
// Load the document into Aspose.Note
Document doc = new Document(dataDir + "Sample1.one");
```

> **Astuce :** Conservez le chemin `dataDir` en absolu ou utilisez `Paths.get(...)` pour éviter les erreurs liées aux chemins.

## Comment obtenir les balises OneNote
Après avoir chargé le document, récupérez tous les nœuds `RichText`. Chaque nœud peut contenir une ou plusieurs balises.

```java
// Get all RichText nodes
List<RichText> nodes = doc.getChildNodes(RichText.class);
```

## Parcourir chaque nœud
Bouclez sur chaque nœud `RichText` afin d’inspecter ses balises.

```java
// Iterate through each node
for (RichText richText : nodes) {
    // Process each node here
}
```

## Récupérer les NoteTags (Comment modifier les balises OneNote)
À l’intérieur de la boucle, vérifiez si une balise est un `NoteTag`. Si c’est le cas, vous pouvez lire ses propriétés — ou les modifier si nécessaire.

```java
for (ITag tag : richText.getTags()) {
    if (tag.getClass() == NoteTag.class) {
        NoteTag noteTag = (NoteTag) tag;
        // Retrieve properties
        System.out.println("Completed Time: " + noteTag.getCompletedTime());
        System.out.println("Create Time: " + noteTag.getCreationTime());
        System.out.println("Font Color: " + noteTag.getFontColor());
        System.out.println("Status: " + noteTag.getStatus());
        System.out.println("Label: " + noteTag.getLabel());
        System.out.println("Icon: " + noteTag.getIcon());
        System.out.println("High Light: " + noteTag.getHighlight());
        // Example of modifying a property
        // noteTag.setLabel("Updated Label");
    }
}
```

> **Avertissement :** Modifier une balise change le document sous‑jacent. N’oubliez pas d’enregistrer le document après avoir effectué des modifications.

## Conclusion
Vous savez maintenant **comment extraire les balises**, comment **charger un fichier OneNote**, comment **obtenir les balises OneNote**, et même comment **modifier les balises OneNote** à l’aide d’Aspose.Note pour Java. Intégrez ces extraits dans vos propres projets pour automatiser l’analyse, le reporting ou la migration de notes.

## FAQ
### Aspose.Note est‑il compatible avec toutes les versions de OneNote ?
Aspose.Note prend en charge divers formats de fichiers OneNote, assurant la compatibilité avec différentes versions.

### Puis‑je modifier les propriétés du NoteTag récupéré ?
Oui, Aspose.Note vous permet de modifier et de mettre à jour les propriétés du NoteTag par programme.

### Existe‑t‑il une version d’essai disponible pour Aspose.Note ?
Absolument ! Vous pouvez accéder à la version d’essai gratuite [here](https://releases.aspose.com/).

### Où trouver la documentation complète d’Aspose.Note pour Java ?
Explorez la documentation détaillée [here](https://reference.aspose.com/note/java/).

### Comment obtenir de l’assistance pour des problèmes ou des questions ?
Rendez‑vous sur le forum de support [here](https://forum.aspose.com/c/note/28) pour obtenir de l’aide de la communauté Aspose.

## Questions fréquemment posées
**Q :** *Puis‑je extraire les balises de fichiers OneNote protégés par mot de passe ?*  
**R :** Oui, fournissez le mot de passe lors de la construction de l’objet `Document`.

**Q :** *Dois‑je appeler une méthode de sauvegarde après avoir modifié les balises ?*  
**R :** Absolument. Utilisez `doc.save("UpdatedSample.one");` pour persister les changements.

**Q :** *Est‑il possible de filtrer les balises par statut ?*  
**R :** Vous pouvez vérifier `noteTag.getStatus()` dans la boucle et ne traiter que les statuts souhaités.

**Q :** *Que se passe‑t‑il si un nœud RichText n’a aucune balise ?*  
**R :** `richText.getTags()` renvoie une collection vide ; la boucle le saute simplement.

**Q :** *Puis‑je traiter plusieurs fichiers OneNote en lot ?*  
**R :** Encapsulez la logique ci‑dessus dans une routine d’itération de fichiers et traitez chaque document séquentiellement.

---

**Dernière mise à jour :** 2026-02-28  
**Testé avec :** Aspose.Note pour Java 24.12  
**Auteur :** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}