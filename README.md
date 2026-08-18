# Pop!

Version 1.0.0 — 18 août 2026

Application web bilingue de libre association pour faire émerger des idées à partir d’un sujet central.

Pop! propose un parcours en trois temps : développer une mindmap par associations successives, récupérer les termes produits sous forme brute, puis les recombiner pour faire surgir et noter de nouvelles idées.

Le programme est conçu et développé par Simon Léturgie dans le cadre d’Eigrutel BD Academy et d’Eigrutel Lab — Atelier d’outils libres pour la bande dessinée.

---

## Français

### Présentation

Pop! est une application web autonome réunie dans un unique fichier HTML.

L’outil repose sur une méthode de divergence puis de recombinaison :

1. indiquer un sujet central ;
2. produire des associations libres autour de ce sujet ;
3. poursuivre chaque branche en ne tenant plus compte du sujet central mais seulement du terme dont elle part ;
4. répéter l’opération sur plusieurs niveaux ;
5. passer dans **Termes** pour relire la matière obtenue ;
6. rapprocher quelques termes du sujet central ou les mettre en relation entre eux ;
7. noter dans **Idées** toutes les pistes qui apparaissent, même improbables ou farfelues.

Principe général : **dans la mindmap, associer sans juger ; dans Termes, recombiner ; dans Idées, conserver ce qui surgit.**

### Espaces de travail

Pop! comporte trois espaces permanents :

- **Mindmap** — développement arborescent des associations ;
- **Termes** — récupération, tri, masquage, regroupement et recombinaison des mots ou expressions saisis ;
- **Idées** — bibliothèque des idées apparues pendant le travail.

### Fonctionnalités

- interface bilingue français / anglais ;
- français utilisé par défaut ;
- mindmap à plusieurs niveaux avec révélation progressive des branches ;
- conservation des descendants lors d’une simple correction de texte ;
- confirmation avant suppression d’une branche contenant des descendants ;
- vue **Termes** simple par défaut, avec retour automatique à la ligne ;
- vue liste pour organiser les termes ;
- tri alphabétique ou par longueur ;
- réorganisation manuelle ;
- création de groupes de termes ;
- masquage et réaffichage des termes ;
- création, modification et suppression d’idées ;
- bouton permanent **✦ Nouvelle idée** ;
- annuler / rétablir ;
- zoom et vue entière de la mindmap ;
- styles Jour, Nocturne et Licorne ;
- sauvegarde locale dans le navigateur ;
- sauvegarde d’un projet au format `pop_nomduprojet.json` ;
- ouverture d’un projet précédemment sauvegardé ;
- impression des termes ;
- impression des idées ;
- manuel intégré ;
- interface responsive pour ordinateur, tablette et téléphone ;
- favicon et icône Apple : `favicon/favpop.png` ;
- fonctionnement autonome sans dépendance externe ;
- code commenté en français et en anglais.

### Utilisation

#### 1. Mindmap

Saisir le sujet central puis renseigner les branches par libre association : contraires, analogies, personnalités, événements, objets, souvenirs, situations ou toute autre piste pertinente.

Pour le niveau suivant, faire volontairement abstraction du sujet central : chaque terme devient le seul point de départ de ses propres associations.

Continuer de la même manière sur les niveaux suivants.

#### 2. Termes

La vue simple affiche les termes les uns à côté des autres afin de retrouver une matière brute, débarrassée de la structure de la mindmap.

Quelques termes peuvent alors être rapprochés du sujet central ou les uns des autres. C’est souvent à ce moment que de nouvelles idées apparaissent.

La vue liste permet de trier, sélectionner, masquer, réordonner et constituer des groupes.

#### 3. Idées

Utiliser **✦ Nouvelle idée** dès qu’une piste apparaît. Une idée peut être notée même si elle semble absurde, excessive ou très éloignée de la première intention.

### Sauvegarde du projet

Le travail courant est conservé automatiquement dans le stockage local du navigateur.

**Sauvegarder le projet** crée également un fichier portable dont le nom suit la forme :

`pop_nomduprojet.json`

**Ouvrir un projet** recharge un fichier Pop! précédemment sauvegardé.

Une sauvegarde externe est recommandée pour conserver un projet indépendamment du navigateur ou le transférer vers un autre appareil.

### Impression

**Imprimer les termes** produit une présentation dépouillée : les termes sont disposés les uns à la suite des autres, sans cellules ni cadres.

**Imprimer les idées** produit une version lisible des idées enregistrées.

La mise en page d’impression est indépendante des styles Jour, Nocturne et Licorne afin de rester adaptée au papier et au PDF.

### Vie privée

Pop! ne nécessite aucun compte utilisateur.

Les données saisies sont conservées localement dans le navigateur. Le programme ne prévoit aucune transmission automatique des projets vers un serveur.

### Compatibilité

Pop! est conçu pour les versions récentes de :

- Firefox ;
- Chromium et Google Chrome ;
- Microsoft Edge ;
- Safari sur macOS, iPadOS et iOS.

Les comportements de stockage local, téléchargement et impression peuvent légèrement varier selon le navigateur et le système.

### Installation

Aucune installation n’est nécessaire.

1. Télécharger `pop.html`.
2. Conserver le dossier `favicon` à côté du fichier si l’icône doit être affichée.
3. Ouvrir `pop.html` avec un navigateur web moderne.

Après activation de GitHub Pages, l’application pourra également être utilisée directement depuis le dépôt.

### Structure du dépôt

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

---

## English

### Overview

Pop! is a self-contained bilingual web application designed to generate ideas through free association and recombination.

The workflow has three stages: build a multi-level mindmap from a central subject, extract the resulting terms as raw material, then reconnect selected terms to the original subject or to one another until new ideas emerge.

General principle: **associate without judging in the mindmap; recombine in Terms; keep what emerges in Ideas.**

### Workspaces

- **Mindmap** — develops successive associations;
- **Terms** — extracts, sorts, hides, groups and recombines the resulting words and phrases;
- **Ideas** — stores ideas that appear during the process.

### Features

- bilingual French / English interface;
- French selected by default;
- progressive multi-level mindmap;
- descendants preserved when a term is merely edited;
- confirmation before deleting a populated branch;
- simple Terms view selected by default;
- list view for organisation;
- alphabetical and length sorting;
- manual reordering;
- term groups;
- hidden terms;
- idea creation, editing and deletion;
- permanent **✦ New idea** action;
- undo / redo;
- map zoom and fit-to-view;
- Day, Night and Unicorn themes;
- automatic browser storage;
- project files named `pop_projectname.json`;
- project opening and restoration;
- term printing;
- idea printing;
- built-in manual;
- responsive desktop, tablet and mobile interface;
- standalone HTML distribution;
- bilingual source-code comments.

### Method

1. Enter the central subject.
2. Add free associations around it.
3. On the next level, deliberately ignore the central subject and associate only from the parent term.
4. Continue the same process through the following levels.
5. Open **Terms** and look at the raw vocabulary without the mindmap structure.
6. Connect a few terms back to the central subject, or combine them with one another.
7. Record every idea that appears, even strange or unlikely ones.

### Local data and project files

The current project is automatically stored in the browser’s local storage.

**Save project** creates a portable project file. **Open project** restores one.

The external project file is useful for long-term backup and transfer between browsers or devices.

### Print

**Print terms** places the terms in a simple flowing text layout without cards or boxes.

**Print ideas** creates a clean printable version of the stored ideas.

### Compatibility

Pop! is designed for recent versions of Firefox, Chromium / Chrome, Microsoft Edge and Safari on macOS, iPadOS and iOS.

---

## Version

Stable version: **1.0.0**  
Date: **18 August 2026**

## Auteur / Author

Simon Léturgie  
Eigrutel BD Academy  
Eigrutel Lab — Atelier d’outils libres pour la bande dessinée

Site: https://www.stripmee.com

## Licences

- Code source / Source code: GNU Affero General Public License v3.0 or later.
- Documentation et modèles / Documentation and templates: Creative Commons Attribution-ShareAlike 4.0 International, unless otherwise stated.
- Marques, logos et signes distinctifs / Trademarks, logos and distinctive signs: Eigrutel, Eigrutel Lab and Eigrutel BD Academy are reserved.

See `LICENSE.md` and `NOTICE.md`.
