# Challenge E01

Si tout va bien, aujourd'hui, sur le projet de la _Bataille Navale_, tu as réussi à afficher la grille en _console_ et à envoyer des missiles :muscle:

Dans ce challenge, on va continuer sur ce projet, en ajoutant les fonctionnalités suivantes :

- détecter un envoi de missile sur une case sur laquelle on a déjà envoyé un missile :rocket:
- détecter la fin de la partie (plus aucun bateau)
- améliorer l'expérience utilisateur en demandant la case à attaquer via un "prompt"
- cette demande se fera "tant que" la partie n'est pas terminée

Et en bonus, on va modifier le contenu de la page HTML grâce à JavaScript ! (si si, c'est possible !)

## Etapes

### #1 - Détecter un doublon :mag_right:

- dans la fonction gérant l'envoi de missile
- ajouter une condition pour savoir si la case ciblée n'a pas déjà reçu un missile
- si c'est le cas, afficher, au choix, un de ces messages dans la console :
  - _Un missile a déjà été envoyé sur cette case, Général_
  - _Un missile a déjà été envoyé sur cette case, Commandant_
  - _Déjà attaqué !_
  - _Tu sais pas lire ta grille ? On a déjà attaqué cette case, banane_
  - _Allooo! Allooooo! Y'a personne au bout du fil ? Faut réfléchir McFly. Faut réfléchir !_

### #2 - Fin de la partie :heavy_check_mark:

- créer une fonction qui va s'occuper de détecter si la partie est terminée
  - retourne `true` si terminée, `false` sinon
- une partie est terminée lorsqu'il n'y a plus de bateau (case `b`)

<details><summary>indices</summary>

Une façon de faire, mais pas la seule :

- parcourir le tableau de la grille
- compter le nombre de case `'b'`
- si ce nombre est > 0 => la partie n'est pas terminée
- sinon => la partie est terminée

</details>

### #3 - Demander la case à attaquer à l'utilisateur :rocket:

- au lieu de lancer manuellement la fonction `sendMissile` dans la console
- on va utiliser la [fonction `prompt` JavaScript](https://developer.mozilla.org/fr/docs/Web/API/Window/prompt)
- une fois la valeur saisie récupérée dans une variable
- on peut alors appeler la fonction `sendMissile`

### #4 - Attaquer "tant que" la partie n'est pas finie :curly_loop:

- après l'étape 3, on constate qu'on ne demande qu'une seule fois la case à attaquer
- il faudrait demander tant que la partie n'est pas finie
- et oui, on parle bien de boucle ici :wink:

<details><summary>indices</summary>

- **tant que** => boucle `while`
- tant que **la partie n'est pas finie** => on aurait pas une fonction qui renvoie justement true/false si la partie est finie ou pas ? :thinking:
- la fonction `prompt` stoppe l'exécution de la page / du code JS, tant que l'utilisateur n'a pas validé sa réponse

</details>

## Bonus

<details><summary>Si ce challenge a été relativement facile, tu vas pouvoir t'attaquer au bonus portant sur une notion qu'on n'a pas encore vu en cours</summary>
  
C'est à toi de voir, mais c'est jamais facile => [bonus](bonus.md) ... :wink:

</details>
