# Vue Js

- [Vue Js](#vue-js)
  - [Déroulé](#déroulé)
  - [Découverte de Vue](#découverte-de-vue)
  - [Syntaxe et expression](#syntaxe-et-expression)
    - [Options API](#options-api)
    - [Composition API.](#composition-api)
  - [1-List Rendering](#1-list-rendering)
  - [2-User input](#2-user-input)
  - [3-User Event](#3-user-event)
  - [4-Methods](#4-methods)
  - [5-Condition](#5-condition)
  - [6-HTML binding attribute](#6-html-binding-attribute)
  - [7-Dynamic CSS](#7-dynamic-css)
  - [8-Computed](#8-computed)
  - [9-Watch](#9-watch)
  - [10-Options : Cycle de vie](#10-options--cycle-de-vie)
  - [Component](#component)
    - [Création du component](#création-du-component)
    - [Props](#props)
      - [Exo: shopping list](#exo-shopping-list)
    - [Emits](#emits)
      - [Exo: shopping list](#exo-shopping-list-1)
  - [BONUS](#bonus)

## Déroulé

- présentation
- Connaissance html, css, js

Jour 1 : Découverte et Syntaxe vue js dans un component
Jour 2 : Gestion des components
Jour 3 : Gestion des route - Router
Jour 4 : Gestion des états - Pinia

Pour chaque notion:

- voit ensemble la notion + exemple + la doc
- exo à pratiquer en autonomie
- correction ensemble

2 projets:

- ShoppingList (branche master J1, component J2)
- Travel App

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

Suivi doc - https://vuejs.org/guide/essentials/event-handling.html

Exo: shopping list

- Ajouter pour chaque objet de item, une propriété `purchased` qui sera un boolean en `false`
- Dans la liste d'item affichée, au click sur un item:
  - changer le boolean par sa valeur opposé (!)
  - mettre une class dynamic pour que celle-ci appaissent quand `purchased` est à `true`

## 8-Computed

Suivi doc - https://fr.vuejs.org/guide/essentials/computed.html#basic-example

Exo: shopping list

- Créer un `computed` qui va nous permettre d'afficher tout en bas de notre liste, le nombre total d'items dans celle-ci type `La liste contient XX items`

## 9-Watch

L'option watch attend un objet où les clés sont les propriétés de l'instance du composant réactif à surveiller (par exemple les propriétés déclarées via data ou computed) - et les valeurs sont les fonctions de rappel correspondantes. La fonction de rappel reçoit à la fois la nouvelle valeur et l'ancienne valeur de la source surveillée.

```js
watch(editing, (nextValue, prevValue) => {
  console.log(nextValue, prevValue)
})
```

Suivi doc - https://fr.vuejs.org/guide/essentials/computed.html#basic-example

Exo: shopping list

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

## Component

### Création du component

Dans le dossier /components

Appeler le component quand on a besoin: soit dans une view, soit dans un autre component

### Props

**Pour passer des variables du composant parent à l'enfant**

- props statique vs props dynamique
- typage des props
- Utilisation des props dans le component

```js
const props = defineProps({
  foo: String
})
```

https://fr.vuejs.org/guide/components/props.html#prop-passing-details

#### Exo: shopping list

- Mettre la carte de la liste dans un component et l'appeler
  - Créer un component avec la base de syntaxe vue js
  - Dans le template, on va mettre le `li` avec la class et le click mais sans le v-for !
  - C'est à l'appel du component que l'on va mettre le v-for

### Emits

**Pour changer une variable du composant parent DEPUIS le composant enfant**

Un composant peut émettre des événements personnalisés directement à partir du template (par exemple, dans un gestionnaire d'événement v-on) à l'aide de la méthode native $emit :

```js
const emit = defineEmits(['change', 'delete'])
function buttonClick() {
  emit('submit')
  // SI JE VEUX ENVOYER DES PARAMETRES DEDANS LORS DE EMIT
  emit('submit', 'hello') // ou emit('submit', {...})
}
```

Si je veux juste changer une variable du composant Parent SANS AUTRE LOGIQUE DE LE EMIT, je peux passer par la directive v-model

```js
// dans le component "parent"
;<IntroChild v-model="total" />

// dans le component enfant
const total = defineModel()

// ATTENTION: doit avoir le meme nom !!!
// dans le component enfant, je peux alors modifier comme je le souhaite le model 'total' sans avoir besoin de faire un emit
```

https://fr.vuejs.org/guide/components/events.html

#### Exo: shopping list

- Mettre la partie formulaire dans un component: on aura besoin de props, emit et v-model
- Ajouter 2 shopping list à la page d'index :
  - chaque shopping list correspondra à un membre de la famille `Tom`, `Marc` et `lea`: il faudra donc lui passer une props !
  - Dupliquer le component dans app.js
  - le bouton high priority, n'est pas assez visible, on va le mettre en gras ! Super besoin de le faire une seule fois et non 3 fois

## BONUS

- Ajouter un input qui gère la quantité pour chaque item => donc dans item avoir une propriété qui contiendra le nombre d'article
