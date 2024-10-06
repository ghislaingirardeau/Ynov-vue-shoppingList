# Vue Js

- présentation
- Connaissance html, css, js

Jour 1 : Découverte et Syntaxe vue js dans un component
Jour 2 : Gestion des components
Jour 3 : Gestion des route - Router
Jour 4 : Gestion des états - Pinia

## Découverte de Vue

- Framework JavaScript : Vue.js est un framework progressif pour construire des interfaces utilisateur.
- Flexibilité : Il peut être utilisé pour développer des applications simples ou des applications web complexes comme des SPA (Single Page Applications).
- Approche réactive : Vue.js utilise un système de liaison de données réactif, facilitant la mise à jour automatique de l'interface utilisateur en fonction des changements de données.
- Composants modulaires : Il permet de structurer les applications avec des composants réutilisables et isolés.
- Facilité d'intégration : Vue.js peut être intégré facilement dans des projets existants ou utilisé avec d'autres bibliothèques.
- Performance : Sa taille légère et son architecture permettent une bonne optimisation des performances.
- Documentation : Vue.js est reconnu pour sa documentation claire et complète, facilitant l'apprentissage.
- Ecosystème riche : Il dispose d'outils et de bibliothèques comme Vue Router (pour la gestion des routes) et Vuex (pour la gestion de l'état).

## Syntaxe et expression

Les composants Vue peuvent être créés dans deux styles d'API différents : l'Options API et la Composition API.

### Options API

```vue
<script>
export default {
  data() {
    return {
      count: 0
    }
  },
  methods: {
    increment() {
      this.count++
    }
  },
  mounted() {
    console.log(`La valeur initiale de count est ${this.count}.`)
  }
}
</script>

<template>
  <button @click="increment">Count is: {{ count }}</button>
</template>
```

### Composition API.

```vue
<script setup>
import { ref, onMounted } from 'vue'

const count = ref(0)

function increment() {
  count.value++
}

onMounted(() => {
  console.log(`La valeur initiale de count est ${count.value}.`)
})
</script>

<template>
  <button @click="increment">Count is: {{ count }}</button>
</template>
```

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

## 8-Computed

Exo: shopping list
Suivi doc - https://fr.vuejs.org/guide/essentials/computed.html#basic-example

- Ajouter pour chaque objet de item, une propriété 'purchased' qui sera un boolean en false
- Dans la liste d'item affichée, au click sur un item:
  - changer le boolean par sa valeur opposé (!)
  - mettre une class dynamic sur chaque item

## 9-Watch

L'option watch attend un objet où les clés sont les propriétés de l'instance du composant réactif à surveiller (par exemple les propriétés déclarées via data ou computed) - et les valeurs sont les fonctions de rappel correspondantes. La fonction de rappel reçoit à la fois la nouvelle valeur et l'ancienne valeur de la source surveillée.

```js
watch(editing, (nextValue, prevValue) => {
  console.log(nextValue, prevValue)
})
```

Exo: shopping list
Suivi doc - https://fr.vuejs.org/guide/essentials/computed.html#basic-example

- Quand j'annule ma liste de course celle-ci se vide, mon panier devient 0

## 10-Options : Cycle de vie

Suivi doc - https://fr.vuejs.org/guide/essentials/lifecycle.html

```vue
<script setup>
import { onMounted } from 'vue'

onMounted(() => {
  console.log(`the component is now mounted.`)
})
</script>
```
