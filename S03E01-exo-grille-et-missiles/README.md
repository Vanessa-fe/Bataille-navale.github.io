# La bataille navale

On va commencer par le début. Parce qu'on a essayé de commencer une fois par la fin, et, au final, ce fut le début de la fin :disappointed:

Et ce début, c'est le "plateau de jeu" avec les bateaux.  

On a vu qu'on allait stocker ces informations sous forme de tableau à 2 dimensions :

- première dimension : toutes les lignes
- deuxième dimension : dans chaque ligne, toutes les colonnes
- la valeur de chaque colonne va déterminer pour la cellule/case :
  - s'il y a un bateau `'b'`
  - s'il n'y a rien `''`
  - si un missile est tombé dans l'eau `'p'` (plouf :grimacing:)
  - si un missile a touché un bateau `'t'`

Ensuite, on va s'occuper d'afficher cette grille et d'envoyer des missiles :smiling_imp:

<details><summary>Et ensuite, nous allons pouvoir...</summary>

![conquérir le monde !](https://media.giphy.com/media/13tCsW5QkpRMXe/giphy.gif)

</details>

## Etapes

### #1 Créer le tableau :page_facing_up:

- créer une variable `grid` à 2 dimensions représentant un plateau de 8 lignes et 8 colonnes
- ajouter 3 bateaux
- Cool ! (ou _coule_, au choix :smirk:), on peut maintenant envoyer des missiles !

### #2 Envoyer un missile :rocket:

- créer une fonction `sendMissileAt`
  - recevant en argument l'index de la ligne, et l'index de la colonne dans laquelle on souhaite envoyer le missile
  - et retournant `true`/`false` selon le résultat (`true` si bateau atteint)
- tester en console

### #3 Afficher si le tir est réussi :eyes:

- modifier la fonction `sendMissileAt` pour afficher en console si le tir a réussi ou non

### #4 Afficher le plateau :speedboat:

- ça y est, ça se corse un peu
- on sait afficher des infos en console
- on va utiliser la console pour afficher le plateau
- et comme on veut bien cloisonner notre code, on va écrire l'affichage de la grille en console dans une fonction `displayGrid`

<details><summary>résultat attendu</summary>

![](https://user-images.githubusercontent.com/35060565/91989122-69f37f00-ed30-11ea-9ae4-29c60600fcc3.png)

</details>

### #5 Et les tirs réussis/manqués alors ? :boom:

- et oui, on n'a pas gardé l'information après chaque tir de missile
- => go modifier la fonction `sendMissileAt`

<details><summary>c'est génial</summary>

![](https://media.giphy.com/media/hfYnqeqVeO4pO/giphy.gif)

</details>

### #6 `sendMissile('B1');` :rage1:

- bah oui, c'est pas très _user-friendly_ de demander au joueur de renseigner l'index de la ligne et de la colonne
- ajouter une fonction `sendMissile` (sans le _At_ :smirk:) pour accepter un seul argument, une chaîne de caractères représentant une case du plateau
- puis, calculer les index de ligne et colonne correspondants
  - 'A4' => rowIndex=3, columnIndex=0
  - 'C5' => rowIndex=4, columnIndex=2
  - 'G8' => rowIndex=7, columnIndex=6
- et une fois transformé/converti, il suffira d'appeler la fonction `sendMissileAt` avec les index en argument
- :warning: transformer une lettre en chiffre, ce sera pas simple, faudra s'accrocher :muscle:

### #7 Factoriser & améliorer le code

- créer des fonctions si nécessaire
- quand c'est possible, faire en une instruction ce qu'on a fait en plusieurs instructions :boom:
- ouais, je sais :grin: bon courage :wink:

## Et enfin

<details>

![](https://media.giphy.com/media/l4JySAWfMaY7w88sU/giphy.gif)

![](https://media.giphy.com/media/YGJBp5EgyVP9K/giphy.gif)

</details>
