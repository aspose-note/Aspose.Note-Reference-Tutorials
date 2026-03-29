---
date: 2026-03-08
description: Apprenez à extraire les propriétés de listes des documents OneNote à
  l'aide d'Aspose.Note pour Java. Ce guide étape par étape vous montre le code exact
  et les astuces dont vous avez besoin.
linktitle: How to Extract List Properties in OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: Comment extraire les propriétés de la liste dans OneNote - Aspose.Note
url: /fr/java/onenote-text-manipulation/get-list-properties/
weight: 19
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Comment extraire les propriétés de liste dans OneNote - Aspose.Note

## Introduction
Dans ce tutoriel, vous découvrirez **comment extraire les propriétés de liste** d’un fichier OneNote avec Aspose.Note pour Java. Que vous ayez besoin de lire les détails de police, le formatage des listes ou les attributs de style, ce guide vous accompagne à chaque étape — du chargement du document à l’affichage des valeurs extraites. À la fin, vous disposerez d’un extrait de code prêt à l’emploi qui pourra être intégré à n’importe quel pipeline de traitement de documents basé sur Java.

## Réponses rapides
- **Que signifie « extraire une liste » ?** Cela consiste à lire les détails de formatage (police, taille, couleur, style) des listes numérotées ou à puces stockées dans une structure OneNote.  
- **Quelle bibliothèque est requise ?** Aspose.Note pour Java (dernière version).  
- **Ai‑je besoin d’une licence pour les tests ?** Oui, une licence temporaire est recommandée pour les exécutions non‑production.  
- **Puis‑je exécuter cela sur n’importe quel OS ?** L’API Java fonctionne sous Windows, Linux et macOS.  
- **Combien de temps prend l’implémentation ?** Généralement moins de 10 minutes pour une configuration de base.

## Qu’est‑ce que « comment extraire une liste » dans le contexte de OneNote ?
OneNote stocke chaque élément de liste sous forme d’un `OutlineElement` qui peut contenir un objet `NumberList`. Extraire la liste signifie accéder aux propriétés de cet objet — telles que le nom de police, la taille, la couleur et le formatage—afin de les analyser ou de les modifier programmatiquement.

## Pourquoi utiliser Aspose.Note pour Java afin d’extraire les propriétés de liste ?
- **Pas d’interop COM** – Fonctionne entièrement en Java sans nécessiter le client Windows OneNote.  
- **Fidélité totale** – Préserve tous les détails de formatage, y compris les polices et couleurs personnalisées.  
- **Multiplateforme** – Exécutez le même code sur n’importe quel environnement serveur.  
- **API riche** – Fournit un accès direct aux objets de liste, rendant l’extraction des propriétés simple et directe.

## Prérequis
Avant de commencer, assurez‑vous de disposer de :

- Aspose.Note pour Java : téléchargez la dernière version **[here](https://releases.aspose.com/note/java/)**.  
- Un environnement de développement Java (JDK 8 ou supérieur).  
- Un document OneNote (par ex., `Sample1.one`) placé dans un répertoire connu.

## Import Packages
Tout d’abord, importez les classes dont vous aurez besoin. Cela vous donne accès aux fonctionnalités principales d’Aspose.Note.

```java
import java.io.IOException;
import java.util.List;
import com.aspose.note.Document;
import com.aspose.note.NumberList;
import com.aspose.note.OutlineElement;
```

Passons maintenant à l’implémentation étape par étape.

## Comment extraire les propriétés de liste – Guide étape par étape

### Étape 1 : Charger le document OneNote
Fournissez le chemin correct vers le fichier `.one` et créez une instance `Document`.

```java
// The path to the documents directory.
String dataDir = "Your Document Directory";

// Load the document into Aspose.Note
Document oneFile = new Document(dataDir + "Sample1.one");
```

> **Astuce :** Utilisez des chemins absolus ou configurez un chemin relatif basé sur le dossier des ressources de votre projet afin d’éviter `FileNotFoundException`.

### Étape 2 : Récupérer la collection de nœuds de contour
Chaque liste réside à l’intérieur d’un `OutlineElement`. Récupérez tous ces éléments depuis le document.

```java
// Retrieve a collection of nodes of the outline element
List<OutlineElement> nodes = oneFile.getChildNodes(OutlineElement.class);
```

### Étape 3 : Parcourir les nœuds et localiser les listes
Bouclez sur chaque nœud, en vérifiant s’il contient un `NumberList`. Lorsqu’il en trouve, conservez la référence pour une extraction ultérieure.

```java
// Iterate through each node
for (OutlineElement node : nodes) {
    if (node.getNumberList() != null) {
        NumberList list = node.getNumberList();
        // Continue with further operations on list properties
    }
}
```

### Étape 4 : Extraire les propriétés de liste souhaitées
À l’intérieur de la boucle, vous pouvez maintenant lire n’importe quel attribut exposé par la classe `NumberList`.

```java
// Retrieve font name
System.out.println("Font Name: " + list.getFont());
// Retrieve font length (character count)
System.out.println("Font Length: " + list.getFont());
// Retrieve font size
System.out.println("Font Size: " + list.getFontSize());
// Retrieve font color
System.out.println("Font Color: " + list.getFontColor());
// Retrieve format (e.g., decimal, lowerLetter)
System.out.println("Font format: " + list.getFormat());
// Check bold style
System.out.println("Is bold: " + list.isBold());
// Check italic style
System.out.println("Is italic: " + list.isItalic());
```

La sortie console affichera chaque propriété, vous permettant de consigner, analyser ou traiter davantage les informations de style de la liste.

## Problèmes courants & Dépannage
| Symptom | Likely Cause | Fix |
|---------|--------------|-----|
| `NullPointerException` on `list.getFont()` | Le nœud ne contient pas de `NumberList`. | Ajoutez une vérification de null (`if (node.getNumberList() != null)`). |
| Aucun résultat affiché | `dataDir` pointe vers le mauvais dossier. | Vérifiez le chemin et assurez‑vous que `Sample1.one` existe. |
| La couleur de police apparaît comme `null` | La liste utilise la couleur de thème par défaut. | Utilisez `list.getFontColor()` avec une valeur de secours vers le thème du document. |

## Foire aux questions

**Q : Aspose.Note est‑il compatible avec différentes versions de OneNote ?**  
R : Oui, Aspose.Note prend en charge une large gamme de formats de fichiers OneNote, des versions 2007 aux dernières versions Office 365.

**Q : Puis‑je personnaliser les propriétés de police récupérées ?**  
R : Absolument. Vous pouvez appeler uniquement les getters dont vous avez besoin (par ex., `getFontSize()` ou `isBold()`) et ignorer les autres.

**Q : Où puis‑je trouver une assistance supplémentaire ?**  
R : Pour toute question ou problème, consultez le [Aspose.Note forum](https://forum.aspose.com/c/note/28) pour une aide rapide.

**Q : Ai‑je besoin d’une licence temporaire pour les tests ?**  
R : Oui, vous pouvez obtenir une licence temporaire **[here](https://purchase.aspose.com/temporary-license/)** à des fins d’évaluation.

**Q : Que faire si je souhaite acheter Aspose.Note pour Java ?**  
R : Vous pouvez acheter le produit **[here](https://purchase.aspose.com/buy)** pour débloquer tout son potentiel dans vos projets.

---

**Dernière mise à jour :** 2026-03-08  
**Testé avec :** Aspose.Note pour Java (dernière version)  
**Auteur :** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}