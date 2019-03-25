# VUE 101

## Objectifs

Comprendre le concept de base d'un framework JS (entre autre Vuejs).

## Étape 1

Faire un rendu Déclaratif :
- Créer votre premier component dans le dossier `src/components`, celui-ci affichera "Bonjour [pseudo] !".
- Ajouter un `Prop` (propriéter) `name` à votre composant, afficher cette `Prop`.
- Dans le composant `App` ajouter un input qui va changer la valeur du nom. 

## Étape 2

Faire un rendu Conditional :
- Créer un nouveau component, celui-ci affichera `Je suis cacher !`.
- Créer un nouvelle attribut `boolean` à la classe de votre component.
- Ajouter une condition sur l'élèment qui contient le texte, qui affichera oui ou non votre texte en fonction de la valeur de votre attribut. 
- Ajouter un boutton "Toggle"
- Créer une nouvelle méthode `toggle`, qui changera l'état de votre attribut `true -> false || false -> true`
- Ajouter un évenement à votre button qui déclanchera la fonction `toggle` au clique.

## Étape 3

Faire un rendu Ittératif :
- Créer un nouveau component, celui-ci affichera `Liste de course`.
- Créer un nouvelle attribut qui sera un tableau de `string` à la classe de votre component.
- Ajouter des valeurs à votre tableau.
- Ajouter un élément `ul` dans votre `template` et un `li` dans le `ul`.
- Faire un boucle sur ce `li` pour afficher toute les valeurs du tableau.
- Ajouter un nouveau formulaire avec un `input` et un `button` dans votre `template`.
- Créer une nouvelle methode qui permettera d'ajouter de nouvelle valeurs dans votre tableau.
- Ajouter un nouvelle attribut `newItem: string`
- Lier cette attributs à votre `input` pour pouvoir ajouter une valeur par la suite.
