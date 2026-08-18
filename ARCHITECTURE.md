# Architecture — Pop!

Version 1.0.0 — 18-08-2026

## 1. Principe général

Pop! est une application web autonome distribuée principalement dans un seul fichier :

`pop.html`

Ce fichier contient la structure HTML, les styles CSS, la logique JavaScript, les textes français et anglais, le stockage local, la gestion des projets, l’impression et le manuel intégré.

Aucun framework ni système de compilation n’est requis.

## 2. Organisation fonctionnelle

L’application comporte trois espaces :

### Mindmap

- sujet central ;
- génération d’un arbre fixe à plusieurs niveaux ;
- révélation des enfants seulement après validation du terme parent ;
- rendu des branches par SVG ;
- placement calculé autour du sujet central ;
- résolution partielle des chevauchements ;
- zoom, déplacement tactile / souris et ajustement de la vue.

### Termes

- extraction de toutes les cellules remplies ;
- vue simple sous forme de flux de termes ;
- vue liste pour l’organisation ;
- tris ;
- ordre manuel ;
- sélection ;
- groupes ;
- termes masqués.

Le sujet central reste traité séparément et conserve une place prioritaire.

### Idées

- éditeur d’idée ;
- titre et texte libre ;
- bibliothèque des idées enregistrées ;
- modification et suppression ;
- création accessible depuis tous les espaces.

## 3. Données

L’état du projet comprend notamment :

- contenu et état de validation des cellules de la mindmap ;
- espace actif ;
- zoom ;
- nom du travail ;
- ordre des termes ;
- type de tri ;
- groupes ;
- termes sélectionnés et masqués ;
- vue simple ou liste ;
- idées ;
- thème ;
- langue.

Le travail est enregistré dans `localStorage`.

Le format de sauvegarde externe est JSON. Pour le public, l’interface utilise les termes **Sauvegarder le projet** et **Ouvrir un projet** plutôt que le vocabulaire technique JSON.

Le nom de fichier suit la forme :

`pop_nomduprojet.json`

## 4. Historique

Un historique interne permet d’annuler et de rétablir les dernières modifications significatives.

Raccourcis principaux :

- `Ctrl/Cmd + Z` : annuler ;
- `Ctrl/Cmd + Shift + Z` ou `Ctrl/Cmd + Y` : rétablir.

## 5. Suppression des branches

Une modification de texte conserve les descendants.

Lorsqu’un terme est vidé :

- si aucun descendant rempli n’existe, la cellule peut être supprimée normalement ;
- si des descendants contiennent des données, Pop! demande confirmation avant d’effacer la branche associée ;
- en cas d’annulation, le terme précédent est restauré.

## 6. Interface bilingue

Les libellés d’interface sont centralisés dans les données de traduction français / anglais.

La langue choisie est mémorisée dans le projet et dans le stockage local.

## 7. Thèmes

Trois styles sont fournis :

- Jour ;
- Nocturne ;
- Licorne.

Les thèmes modifient les variables CSS et les couleurs des interfaces Termes et Idées. Les impressions utilisent volontairement une présentation claire indépendante du thème écran.

## 8. Impression

Deux sorties imprimables sont proposées :

### Termes

Les termes visibles sont présentés sans cellules ni cadres, dans un flux horizontal avec retours automatiques à la ligne.

### Idées

Les idées enregistrées sont mises en page dans un document clair destiné à l’impression ou à l’enregistrement PDF depuis le navigateur.

## 9. Responsive

L’interface comporte des règles spécifiques pour :

- ordinateur ;
- tablette ;
- smartphone.

Sur mobile, la priorité est donnée à l’espace de contenu. Les commandes sont compactées afin de conserver un maximum de hauteur utile pour la mindmap, les termes et les idées.

## 10. Arborescence du dépôt

```text
eigrutel-pop/
├── pop.html
├── index.html
├── README.md
├── NOTICE.md
├── LICENSE.md
├── CHANGELOG.md
├── ARCHITECTURE.md
└── favicon/
    └── favpop.png
```

Le dossier `favicon/` doit contenir l’image `favpop.png` utilisée par `pop.html` et `index.html`.
