# ProfileViewer

Outil web local de visualisation, de comparaison, de mesure et d'annotation de profils au format SVG.

ProfileViewer permet de charger des profils à l'échelle 1:1 afin de les superposer, de vérifier leur compatibilité géométrique, de prendre des cotes et d'ajouter des annotations.

---

## Aperçu

<img width="1875" height="868" alt="image" src="https://github.com/user-attachments/assets/d1edc7ed-f887-4a54-ab47-a1020f3a6d17" />

---

## Objectifs du projet

L'outil doit permettre de :

* Visualiser des profils au format SVG.
* Comparer plusieurs profils simultanément.
* Vérifier des compatibilités géométriques.
* Contrôler des dimensions.
* Réaliser des revues techniques rapides.
* Préparer des captures destinées à Teams, Outlook, PowerPoint ou tout autre support d'échange.

---

## Utilisation

### En ligne

Le visualisateur est publié avec GitHub Pages à l'adresse suivante :

https://jlegac.github.io/ProfileViewer/

Si aucun fichier `dataprofils.js` réel n'est disponible, l'application charge automatiquement `sample-dataprofils.js` afin de proposer une démonstration fonctionnelle.

### Données locales

Pour utiliser vos propres profils sans les publier :

Glisser-déposer le fichier `dataprofils.js` dans la zone "Données de profils" ou utiliser le bouton "Choisir un fichier".

Le fichier est lu localement par le navigateur et n'est pas envoyé à un serveur.

### Utilisation locale

Télécharger le dépôt ou le cloner, puis ouvrir `index.html` dans un navigateur compatible.

Pour charger automatiquement les données réelles, le fichier `dataprofils.js` doit être placé dans le même dossier que `index.html`.

---

## Confidentialité

`sample-dataprofils.js` contient uniquement des profils fictifs de démonstration.

---

## Fonctionnalités principales

* Recherche par référence et désignation.
* Placement libre de profils.
* Déplacement, rotation et symétrie.
* Sélection simple, multiple et par fenêtre.
* Copier/coller de profils, cotes et annotations.
* Cotes horizontales et verticales.
* Annotations : flèche, rectangle, cercle, texte.
* Poignées d'édition sur les annotations.
* Annuler / rétablir.
* Navigation par zoom molette et déplacement de vue avec clic molette.

---

## Informations des profils

Chaque profil peut contenir :

* Référence.
* Désignation.
* Dimensions.
* Caractéristiques techniques.

---

## Interface

### Panneau gauche

Recherche instantanée par :

* Référence.
* Désignation.

Affichage de la bibliothèque des profils disponibles.

Un clic sur un profil :

* affiche son aperçu sous la souris ;
* prépare son placement dans la zone graphique.

### Zone graphique centrale

Zone principale de travail.

Elle permet :

* le placement des profils ;
* le déplacement ;
* la sélection ;
* la mesure ;
* les annotations ;
* la comparaison.

### Panneau droit

Affichage contextuel :

* informations du profil sélectionné ;
* informations de mesure ;
* informations d'annotation ;
* aide utilisateur.

---

## Navigation

### Zoom

```text
Molette avant   = Zoom +
Molette arrière = Zoom -
```

### Déplacement de la vue

```text
Clic molette maintenu
+
Déplacement souris
```

Permet le déplacement de la vue.

### Réinitialisation

Bouton :

```text
Vue
```

Retour à la vue initiale.

---

## Placement des profils

Un clic sur un profil dans la bibliothèque :

* charge le profil sous la souris ;
* affiche un aperçu.

Un clic dans la zone graphique :

* place le profil.

Avant placement, les actions suivantes sont disponibles :

```text
↻ ou R = rotation de 90°
⇋ ou M = symétrie horizontale
Échap = annuler le placement
```

---

## Sélection

### Sélection simple

```text
Clic gauche
```

Sélectionne uniquement l'objet cliqué.

### Sélection multiple

```text
Ctrl + clic
```

ou

```text
Maj + clic
```

Ajoute ou retire l'objet de la sélection.

### Fenêtre de sélection

```text
Clic dans le vide
+
Glisser
```

---

## Manipulation de groupe

Les actions suivantes fonctionnent sur plusieurs objets sélectionnés :

* Déplacement.
* Rotation.
* Symétrie.
* Copie.
* Suppression.

Le centre de transformation est le centre global de la sélection.

---

## Copier / Coller

### Copier

```text
⎘ Copier
```

ou

```text
Ctrl + C
```

### Coller

```text
Ctrl + V
```

Le contenu collé apparaît sous la souris.

Avant validation, il peut être :

* tourné ;
* symétrisé.

Un clic valide le placement.

La copie conserve :

* profils ;
* cotes ;
* flèches ;
* rectangles ;
* cercles ;
* textes.

---

## Mesures

La création d'une cote se fait en 3 clics :

1. Premier sommet.
2. Second sommet.
3. Position de la cote.

Les cotes sont uniquement :

* horizontales ;
* verticales.

Les cotes peuvent être :

* déplacées ;
* supprimées ;
* copiées ;
* annulées via `Ctrl + Z`.

Les cotes ne sont pas éditables.

---

## Annotations

Les annotations sont regroupées dans une section dédiée :

```text
Annotations
➜  ▭  ○  T
```

### Flèche

Création par clic-glisser.

Fonctions :

* déplacement ;
* copie ;
* suppression ;
* modification des extrémités.

### Rectangle

Création par clic-glisser.

Fonctions :

* déplacement ;
* copie ;
* suppression ;
* redimensionnement.

### Cercle

Création par clic-glisser.

Fonctions :

* déplacement ;
* copie ;
* suppression ;
* redimensionnement.

### Texte

Création par clic.

Fonctions :

* déplacement ;
* copie ;
* suppression ;
* modification du contenu.

Édition :

```text
Double clic
```

ou

```text
F2
```

---

## Poignées d'édition

Les poignées apparaissent dès qu'une annotation est sélectionnée.

Elles permettent :

* l'ajustement des flèches ;
* le redimensionnement des rectangles ;
* le redimensionnement des cercles.

Les cotes n'affichent aucune poignée.

---

## Historique

### Annuler

```text
Ctrl + Z
```

ou

```text
↶
```

### Rétablir

```text
Ctrl + Y
```

ou

```text
↷
```

---

## Raccourcis clavier

| Action           | Raccourci  |
| ---------------- | ---------- |
| Annuler          | `Ctrl + Z` |
| Rétablir         | `Ctrl + Y` |
| Copier           | `Ctrl + C` |
| Coller           | `Ctrl + V` |
| Rotation         | `R`        |
| Symétrie         | `M`        |
| Modifier texte   | `F2`       |
| Supprimer        | `Suppr`    |
| Annuler commande | `Échap`    |
