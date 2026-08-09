---
date: 2026-05-31
description: Apprenez à modifier l'historique des pages OneNote, à changer le titre
  d'une page OneNote et à supprimer l'historique des pages OneNote en utilisant Aspose.Note
  pour Java.
keywords:
- modify onenote page history
- change onenote page title
- Aspose.Note Java
linktitle: Modifier l'historique des pages dans OneNote - Aspose.Note
schemas:
- author: Aspose
  dateModified: '2026-05-31'
  description: Learn how to modify onenote page history, change onenote page title,
    and delete page history onenote using Aspose.Note for Java.
  headline: How to modify onenote page history with Aspose.Note
  type: TechArticle
- description: Learn how to modify onenote page history, change onenote page title,
    and delete page history onenote using Aspose.Note for Java.
  name: How to modify onenote page history with Aspose.Note
  steps:
  - name: Load the OneNote Document
    text: '`Document` loads a OneNote file into memory and provides access to its
      pages and history.'
  - name: Retrieve the First Page and Its History
    text: '`PageHistory` is the Aspose.Note class that stores a notebook’s revision
      list. It offers methods to query, add, or remove historic pages.'
  - name: Delete a Range of History Items
    text: '`removeRange(int start, int count)` removes a consecutive block of history
      entries starting at the specified index.'
  - name: Replace a History Item
    text: '`set_Item(int index, Page page)` replaces the history entry at the given
      position with a new `Page` object.'
  - name: Change the Title of a History Page
    text: '`setTitle(String title)` updates the title of a historic `Page` instance.'
  - name: Add a New History Entry
    text: '`addItem(Page page)` appends a new page to the end of the history collection.'
  - name: Insert a Page at a Specific Position
    text: '`insertItem(int index, Page page)` inserts a page at the specified index,
      shifting subsequent items forward.'
  - name: Save the Modified Notebook
    text: '`save(String path)` writes the updated notebook to the given file location.'
  type: HowTo
- questions:
  - answer: Yes, Aspose.Note for Java integrates seamlessly with Spring, Hibernate,
      Android, and other Java ecosystems.
    question: Can I use Aspose.Note for Java with other Java frameworks?
  - answer: Absolutely—Aspose.Note supports both legacy OneNote 2007 files and the
      modern OneNote 2016/Online formats.
    question: Is Aspose.Note for Java compatible with different versions of OneNote
      files?
  - answer: No, the library is self‑contained; you only need the core JAR and a Java
      runtime.
    question: Does Aspose.Note for Java require any additional dependencies?
  - answer: Yes, you can loop through a directory of `.one` files and apply the same
      history‑editing logic to each notebook.
    question: Can I perform bulk modifications on multiple OneNote files simultaneously?
  - answer: Yes, you can visit the [Aspose.Note forum](https://forum.aspose.com/c/note/28)
      for assistance and to share examples.
    question: Is there a community forum for Aspose.Note for Java where I can ask
      for help?
  type: FAQPage
second_title: Aspose.Note Java API
title: Comment modifier l'historique des pages OneNote avec Aspose.Note
url: /fr/java/onenote-page-manipulation/modify-page-history/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Comment modifier l'historique des pages OneNote avec Aspose.Note

Dans ce tutoriel, vous apprendrez **comment modifier l'historique des pages OneNote** étape par étape en utilisant l'API Aspose.Note pour Java. Que vous ayez besoin de supprimer d'anciennes révisions, de renommer une page historique ou d'insérer une nouvelle entrée, le guide vous accompagne à travers un flux de travail prêt pour la production qui fonctionne avec n'importe quel carnet OneNote.

## Réponses rapides
- **Que signifie « historique des pages » dans OneNote ?**  
  C’est la collection des versions précédentes des pages stockées dans un fichier OneNote.
- **Puis-je supprimer une entrée d'historique spécifique ?**  
  Oui, utilisez les méthodes `removeRange` ou `removeItem` sur l'objet `PageHistory`.
- **La modification du titre d’une page fait‑elle partie de la manipulation de l’historique ?**  
  Absolument — chaque élément d’historique possède son propre titre que vous pouvez modifier.
- **Ai‑je besoin d’une licence pour exécuter ce code ?**  
  Une licence d’évaluation temporaire suffit pour les tests ; une licence complète est requise pour la production.
- **Quelle version de Java est prise en charge ?**  
  Aspose.Note pour Java prend en charge JDK 8 et versions ultérieures.

## Qu’est‑ce que la modification de l’historique des pages OneNote ?
*Modifier l’historique des pages OneNote* désigne la modification programmatique, l’ajout ou la suppression d’entrées dans la liste interne des révisions d’un carnet OneNote. Cela vous permet de ne conserver que les versions pertinentes, de renommer les titres historiques et d’optimiser la taille du carnet tout en réduisant le gonflement global du fichier.

## Pourquoi modifier l’historique des pages OneNote ?
La modification de l’historique des pages peut améliorer considérablement la gestion et les performances du carnet. En éliminant les révisions inutilisées, vous réduisez la taille du fichier, accélérez le chargement et rendez la navigation plus cohérente pour les utilisateurs finaux. Ces avantages sont particulièrement visibles dans les gros carnets contenant des centaines de pages.

Aspose.Note prend en charge **plus de 50 formats d’entrée et de sortie** et peut traiter des carnets contenant **jusqu’à 10 000 pages** sans charger le fichier complet en mémoire, garantissant des opérations haute performance.

## Prérequis

1. **Java Development Kit (JDK)** – JDK 8 ou plus récent installé sur votre machine.  
2. **Aspose.Note for Java library** – téléchargez‑la depuis la [page de téléchargement](https://releases.aspose.com/note/java/).  
3. **A sample OneNote document** – par ex., `Sample1.one` que vous pouvez modifier en toute sécurité.

## Importer les packages

Les classes suivantes sont requises : `Document` représente le carnet complet, `Page` représente une page individuelle, et `PageHistory` gère la collection des pages historiques.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.PageHistory;
```

## Comment modifier l’historique des pages OneNote ?

Chargez le carnet, récupérez sa collection `PageHistory`, puis utilisez les méthodes fournies pour supprimer, remplacer ou insérer des entrées. Toutes les opérations sont effectuées en mémoire, et vous n’avez besoin d’appeler `save` qu’une seule fois à la fin pour enregistrer les modifications.

### Étape 1 : Charger le document OneNote

`Document` charge un fichier OneNote en mémoire et fournit l’accès à ses pages et à son historique.

```java
String dataDir = "Your Document Directory";
Document document = new Document(dataDir + "Sample1.one");
```

### Étape 2 : Récupérer la première page et son historique

`PageHistory` est la classe Aspose.Note qui stocke la liste des révisions d’un carnet. Elle propose des méthodes pour interroger, ajouter ou supprimer des pages historiques.

```java
Page page = document.getFirstChild();
PageHistory pageHistory = document.getPageHistory(page);
```

### Étape 3 : Supprimer une plage d’éléments d’historique

`removeRange(int start, int count)` supprime un bloc consécutif d’entrées d’historique à partir de l’indice spécifié.

```java
pageHistory.removeRange(0, 1);
```

### Étape 4 : Remplacer un élément d’historique

`set_Item(int index, Page page)` remplace l’entrée d’historique à la position donnée par un nouvel objet `Page`.

```java
pageHistory.set_Item(0, new Page());
```

### Étape 5 : Modifier le titre d’une page d’historique

`setTitle(String title)` met à jour le titre d’une instance `Page` historique.

```java
pageHistory.get_Item(1).getTitle().getTitleText().clear().append("New Title");
```

### Étape 6 : Ajouter une nouvelle entrée d’historique

`addItem(Page page)` ajoute une nouvelle page à la fin de la collection d’historique.

```java
pageHistory.addItem(new Page());
```

### Étape 7 : Insérer une page à une position spécifique

`insertItem(int index, Page page)` insère une page à l’indice spécifié, décalant les éléments suivants vers l’avant.

```java
pageHistory.insertItem(1, new Page());
```

### Étape 8 : Enregistrer le carnet modifié

`save(String path)` écrit le carnet mis à jour à l’emplacement de fichier indiqué.

```java
document.save(dataDir + "ModifyPageHistory_out.one");
```

## Pièges courants & astuces
- **Index hors limites :** Vérifiez toujours la taille de la collection avant d’appeler `removeRange` ou `insertItem`.  
- **Titres nuls :** Certaines pages historiques peuvent ne pas avoir de titre ; protégez-vous contre `null` lors de l’appel à `getTitle()`.  
- **Emplacement d’enregistrement :** Assurez‑vous que le chemin de sortie (`ModifyPageHistory_out.one`) est accessible en écriture ; sinon, une `IOException` sera levée.  
- **Astuce de performance :** Lors du traitement de très gros carnets, appelez `document.setLoadOptions(new LoadOptions(LoadFormat.OneNote))` pour activer le chargement paresseux et réduire l’utilisation de la mémoire.

## Questions fréquentes

**Q : Puis‑je utiliser Aspose.Note pour Java avec d’autres frameworks Java ?**  
R : Oui, Aspose.Note pour Java s’intègre parfaitement avec Spring, Hibernate, Android et d’autres écosystèmes Java.

**Q : Aspose.Note pour Java est‑il compatible avec différentes versions de fichiers OneNote ?**  
R : Absolument—Aspose.Note prend en charge les fichiers OneNote 2007 hérités ainsi que les formats modernes OneNote 2016/Online.

**Q : Aspose.Note pour Java nécessite‑t‑il des dépendances supplémentaires ?**  
R : Non, la bibliothèque est autonome ; vous avez seulement besoin du JAR principal et d’un runtime Java.

**Q : Puis‑je effectuer des modifications en masse sur plusieurs fichiers OneNote simultanément ?**  
R : Oui, vous pouvez parcourir un répertoire de fichiers `.one` et appliquer la même logique de modification d’historique à chaque carnet.

**Q : Existe‑t‑il un forum communautaire pour Aspose.Note pour Java où je peux demander de l’aide ?**  
R : Oui, vous pouvez visiter le [forum Aspose.Note](https://forum.aspose.com/c/note/28) pour obtenir de l’aide et partager des exemples.

---

**Dernière mise à jour :** 2026-05-31  
**Testé avec :** Aspose.Note for Java 24.11 (dernière version au moment de la rédaction)  
**Auteur :** Aspose  

{{< blocks/products/products-backtop-button >}}

## Tutoriels associés

- [tutoriel révisions de pages aspose.note – Obtenir les révisions de page dans OneNote](/note/java/onenote-page-manipulation/get-page-revisions/)
- [Comment enregistrer la version d’une page OneNote – Pousser la version actuelle de la page dans OneNote - Aspose.Note](/note/java/onenote-page-manipulation/push-current-page-version/)
- [suivi des modifications onenote – Gérer les révisions de pages avec Aspose.Note](/note/java/onenote-page-manipulation/working-with-page-revisions/)

{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}