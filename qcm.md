# QCM : Introduction à Vue.js 3

1. Qu'est-ce que Vue.js ?
   A. Un framework CSS
   B. Un langage de programmation
   C. Un framework JavaScript
   D. Un gestionnaire de base de données
   <ins>Réponse :</ins> C. Un framework JavaScript

2. Quelle est la commande pour créer un nouveau projet Vue.js ?
   A. npm create vue@latest
   B. vue create my-project
   C. npm init vue-app
   D. npm run vue
   <ins>Réponse :</ins> B. npm create vue@latest

3. Comment appelle-t-on la méthode permettant de déclarer l'état dans Vue.js 3 ?
   A. Les stores
   B. Les composables
   C. Les props
   D. Les refs
   <ins>Réponse :</ins> D. Les refs

4. Quelle directive est utilisée pour afficher du contenu conditionnellement dans Vue.js ?
   A. v-if
   B. v-show
   C. v-for
   D. v-bind
   <ins>Réponse :</ins> A. v-if

5. Qu'est ce qui est utilisé dans Vue.js pour regrouper du contenu réutilisable ?
   A. Un composant
   B. Un mixin
   C. Un plugin
   D. Une instance
   <ins>Réponse :</ins> D. Un composant personnalisé

6. Quelle syntaxe est utilisée pour lier une donnée à une propriété dans Vue.js ?
   A. v-data
   B. v-model
   C. v-bind
   D. v-link
   <ins>Réponse :</ins> C. v-bind

7. Quelle fonction dans Vue.js 3 permet de créer des logiques complexes incluant des données réactives ?
   A. computed
   B. watch
   C. ref
   D. reactive
   <ins>Réponse :</ins> C. computed

8. Quelle est la différence entre v-if et v-show ?
   A. v-if affiche toujours l'élément alors que v-show l'affiche conditionnellement
   B. v-show ajoute et enlève l'élément du DOM, tandis que v-if le cache seulement
   C. v-if ajoute et enlève l'élément du DOM, tandis que v-show le cache seulement
   D. Aucune différence
   <ins>Réponse :</ins> C. v-if ajoute et enlève l'élément du DOM, tandis que v-show le cache seulement

9. Quel est le cycle de vie d’un composant dans Vue.js ?
   A. Création → Mise à jour → Destruction
   B. Chargement → Création → Exécution
   C. Initialisation → Rendu → Fermeture
   D. Appel → Réponse → Destruction
   <ins>Réponse :</ins> A. Création → Mise à jour → Destruction

10. Comment transmet-on des données d’un composant parent à un composant enfant dans Vue.js ?
    A. Via props
    B. Via emit
    C. Via data
    D. Via methods
    <ins>Réponse :</ins> A. Via props

# Voici un QCM spécifique à Vue Router, l'outil de routage officiel pour Vue.js :

QCM : Utilisation de Vue Router

1. Qu'est-ce que Vue Router ?
   A. Un outil de gestion d'état global
   B. Un module pour gérer les routes et la navigation dans une application Vue.js
   C. Un composant pour gérer les animations dans Vue.js
   D. Une bibliothèque pour gérer les composants réactifs
   <ins>Réponse :</ins> B. Un module pour gérer les routes et la navigation dans une application Vue.js

2. Quelle commande permet d'installer Vue Router dans un projet Vue.js 3 ?
   A. npm install vue-router
   B. npm install @vue/router
   C. vue add router
   D. npm install vue-router@next
   <ins>Réponse :</ins> D. npm install vue-router@next

3. Quelle est la méthode pour naviguer de manière programmatique à une autre route dans Vue Router ?
   A. this.$goto('/route')
B. this.$router.navigate('/route')
   C. this.$router.push('/route')
D. this.$route.push('/route')
   <ins>Réponse :</ins> C. this.$router.push('/route')

4. Quelle balise est utilisée dans le template pour définir où le contenu des routes doit être rendu ?
   A. <router-link>
   B. <router-view>
   C. <router-outlet>
   D. <route-placeholder>
   <ins>Réponse :</ins> B. <router-view>

5. Quel composant est utilisé pour créer des liens de navigation dans Vue Router ?
   A. <link-to>
   B. <vue-link>
   C. <route-link>
   D. <router-link>
   <ins>Réponse :</ins> D. <router-link>

6. Comment passer des paramètres dynamiques à une route dans Vue Router ?
   A. En utilisant @param
   B. Avec un query string
   C. En utilisant les params dans le chemin de la route (ex: /user/:id)
   D. Via un tableau d'arguments
   <ins>Réponse :</ins> C. En utilisant les params dans le chemin de la route (ex: /user/:id)

7. Quelle méthode permet d'empêcher l'utilisateur de quitter une page si certaines conditions ne sont pas remplies (ex: formulaire non sauvegardé) ?
   A. beforeRouteLeave
   B. beforeRouteEnter
   C. beforeEach
   D. next(false)
   <ins>Réponse :</ins> A. beforeRouteLeave

8. Quel est le rôle de la fonction next() dans les guards de Vue Router ?
   A. Elle permet de rediriger l'utilisateur vers la prochaine route sans conditions
   B. Elle doit être appelée pour indiquer que le guard est terminé et que la navigation peut se poursuivre
   C. Elle est utilisée pour arrêter la navigation
   D. Elle recharge la route actuelle
   <ins>Réponse :</ins> B. Elle doit être appelée pour indiquer que le guard est terminé et que la navigation peut se poursuivre

9. Quelle option permet de rediriger vers une route par défaut si l'utilisateur accède à une route inexistante ?
   A. redirect
   B. fallback
   C. defaultRoute
   D. catchAll
   <ins>Réponse :</ins> A. redirect

10. Quelle fonction permet d'accéder à l'historique de navigation dans Vue Router ?
    A. this.$route.back()
B. this.$router.history()
    C. this.$router.go(-1)
D. this.$route.go()
    <ins>Réponse :</ins> C. this.$router.go(-1)

# QCM : Utilisation de Pinia dans Vue.js 3

1. Qu'est-ce que Pinia ?
   A. Un gestionnaire de formulaires pour Vue.js
   B. Une bibliothèque de routage pour Vue.js
   C. Un outil de gestion d'état pour Vue.js 3
   D. Un outil de gestion des composants
   <ins>Réponse :</ins> C. Un outil de gestion d'état pour Vue.js 3

2. Quelle commande permet d'installer Pinia dans un projet Vue.js 3 ?
   A. npm install @pinia/store
   B. npm install pinia
   C. npm install vuex-pinia
   D. vue add pinia
   <ins>Réponse :</ins> B. npm install pinia

3. Comment créer un store dans Pinia ?
   A. Avec la fonction defineStore
   B. Avec la fonction createStore
   C. En utilisant new Store()
   D. En utilisant initStore
   <ins>Réponse :</ins> A. Avec la fonction defineStore

4. Comment accède-t-on à un store Pinia dans un composant Vue.js ?
   A. this.$pinia
B. useStore()
C. this.$store
   D. piniaStore()
   <ins>Réponse :</ins> B. useStore()

5. Quelle option de Pinia est utilisée pour créer des propriétés calculées basées sur l'état du store ?
   A. methods
   B. getters
   C. actions
   D. computed
   <ins>Réponse :</ins> B. getters

6. Comment modifie-t-on l'état d'un store dans Pinia ?
   A. En modifiant directement l'état
   B. En utilisant setState()
   C. En utilisant des actions définies dans le store
   D. En utilisant des mutations comme dans Vuex
   <ins>Réponse :</ins> C. En utilisant des actions définies dans le store

7. Que faut-il faire pour utiliser Pinia dans un projet Vue.js 3 après l'avoir installé ?
   A. Il suffit de l'importer dans chaque composant
   B. Il faut l'enregistrer dans l'application avec app.use(pinia)
   C. Il faut l'ajouter dans le fichier index.html
   D. Aucune configuration supplémentaire n'est nécessaire
   <ins>Réponse :</ins> B. Il faut l'enregistrer dans l'application avec app.use(pinia)

8. Quel est le cycle de vie du store dans Pinia ?
   A. Création → Modification → Suppression
   B. Initialisation → Rendu → Destruction
   C. Activation → Réinitialisation → Inactivation
   D. Création → Hydratation → Réaction aux changements
   <ins>Réponse :</ins> D. Création → Hydratation → Réaction aux changements

9. Comment réinitialiser l'état d'un store Pinia ?
   A. this.$reset()
    B. store.clear()
    C. store.reset()
    D. pinia.clearState()
<ins>Réponse :</ins> A. this.$reset()
