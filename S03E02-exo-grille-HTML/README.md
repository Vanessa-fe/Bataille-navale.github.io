# Grille HTML

C'est cool (ou _coule_) la console, mais afficher notre grille dans une page HTML c'est mieux.

<details>

![captain obvious](https://media.giphy.com/media/gF8vDz0XAUfIWx9jUW/giphy.gif)

</details>

Pour cela, on va apprendre quelques nouveautés spécifiques à JavaScript :

- **DOM** (_Document Object Model_)
- ha bah non, c'est tout :grimacing:

## Le DOM

C'est une interface, un intermédiaire, entre notre code JavaScript et le code HTML de la page.

<details>

![lost](https://media.giphy.com/media/gKsJUddjnpPG0/giphy.gif)

</details>

Par exemple, grâce au DOM, on peut récupérer (dans une variable JavaScript) du texte présent dans le code HTML.

<details>

![interesting](https://media.giphy.com/media/RhPvGbWK78A0/giphy.gif)

</details>

Et, toujours grâce au DOM, on peut modifier le code HTML :tada:  
(et donc modifier le contenu de la page, sans la recharger)

<details>

![awesome](https://media.giphy.com/media/i79P9wUfnmPyo/giphy.gif)

</details>

## Fonctionnalités

- afficher la grille en HTML
- afficher l'état _touché_ ou _plouf_ dans la grille HTML
- afficher automatiquement la grille après chaque tir de missile
- lister en console les cases touchées après chaque tir réussi

## Etapes

### #1 Ajouter le code HTML :computer:

- prendre le code du fichier [`grid.html`](./grid.html) pour l'intégrer dans notre projet
- pareil pour [`reset.css`](./reset.css) et [`style.css`](./style.css)
- :relieved: c'était facile

### #2 Afficher les bateaux :boat:, et missiles :rocket: dans la grille HTML

- on va devoir modifier le contenu texte des cellules
- dans la fonction `displayGrid()`
  - dans la boucle existante permettant d'afficher en console
  - récupérer l'élément de la cellule/case courante
  - modifier son contenu texte

### #3 Colorier les cases selon _touché_ :boom: ou _plouf_ :ocean:

- à nouveau dans la fonction `displayGrid()`
- pour chaque élément "cellule"
  - on va ajouter une classe
    - "hit" si touché
    - "splash" si plouf

### #4 Automatiser l'affichage de la grille :robot:

- on est fainéant, on ne veut plus lancer la fonction `displayGrid()` manuellement :sunglasses:
- donc on va faire en sorte d'afficher la grille après chaque tir de missile

### #5 Résumer les cases touchées :thinking:

- pour information, et dans la console
- après chaque tir réussi
  - afficher la liste complète des cases touchées
- on pourrait avoir un tableau qui enregistre toutes les cases touchées, au fur et à mesure
- mais on va privilégier l'analyse du code HTML (via le DOM)
  - bah oui, toutes les cases _touchées_ ont une classe particulière :wink:

<details><summary>ça fonctionne ?</summary>

![congrats](https://media.giphy.com/media/3o6fJ1BM7R2EBRDnxK/giphy.gif)

</details>

## Bonus

Et oui, même en journée, si on finit plus tôt, on peut faire des bonus :nerd_face:

C'est par ici => [bonus _dataset_](bonus.md)
