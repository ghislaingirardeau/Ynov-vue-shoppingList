# Table content

## Découverte de Vue

## Syntaxe et expression

## 1-List Rendering

Cours: rendu d'une liste de message (array string)
Suivi doc - https://vuejs.org/guide/essentials/list.html

Exo: shopping list: rendu d'une liste d'un objet

## 2-User input

Cours: v-model
Suivi doc - https://vuejs.org/guide/essentials/forms.html

Exo: shopping list: Créer l'input pour ajouter un item + un checkbox pour definir sa priorité

## 3-User Event

Cours: click, keyup
Suivi doc - https://vuejs.org/guide/essentials/event-handling.html

Exo: shopping list

- au click => ajoute l'item dans le panier

## 4-Methods

Cours: click, keyup
Suivi doc - https://vuejs.org/guide/essentials/event-handling.html

Exo: shopping list

- Mettre l'event dans une méthode
- et faire un reset de la valeur du bouton au click

## 5-Condition

Suivi doc - https://vuejs.org/guide/essentials/conditional.html

Exo: shopping list

- Commenter la liste des produits
- Ajouter un bouton pour afficher / masquer le formulaire
- SI le bouton renvoie true => affiche le formulaire
- SI la liste de courses est vide, affiche un message "Panier vide"

Bonus: si le bouton est true sa valeur est "add item" sinon "cancel"

## 6-HTML binding attribute

Cours:
Suivi doc - https://vuejs.org/guide/essentials/event-handling.html

Exo: shopping list

- désactiver le bouton si text taper par utilisateur fait moins de 5 caractères
- bind le placeholder avec une variable `placeholder`
- bind div class header avec une variable `headerId`

## 7-Dynamic CSS

Exo: shopping list
Suivi doc - https://vuejs.org/guide/essentials/event-handling.html

- Ajouter pour chaque objet de item, une propriété 'purchased' qui sera un boolean en false
- Dans la liste d'item affichée, au click sur un item:
  - changer le boolean par sa valeur opposé (!)
  - mettre une class dynamic sur chaque item

## Computed
