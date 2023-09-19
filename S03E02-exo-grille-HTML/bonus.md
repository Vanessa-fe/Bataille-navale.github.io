# Bonus _Dataset_

[Doc MDN](https://developer.mozilla.org/fr/docs/Apprendre/HTML/Comment/Utiliser_attributs_donnes)

- stocker les données "A1", "B2", "F5", etc.
  - en _dataset_ sur chaque élément "cellule" : `data-cell-name="A2"`
  - et directement dans le code HTML
  - tu peux n'en faire que 3-4 en dur en HTML, et créer les autres dans le Mega-Bonus
  - ou bien tout faire en HTML
- ainsi, lors du listing des cases touchées,
  - on récupère le _dataset_ "cellName" de la cellule
  - puis on affiche en console "A2" plutôt que "case 10" :tada:

# Mega Bonus

- en JS, parcourir chaque élément "cellule" de la grille HTML
- pour chaque cellule,
  - générer le nom de la cellule ("A2", "B3", etc.)
  - stocker ce nom en _dataset_ dans chaque cellule
- :warning: attention, il ne faut définir ces _datasets_ qu'une seule fois (pas à chaque affichage de la grille :wink:)
