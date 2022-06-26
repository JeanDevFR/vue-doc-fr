# Application

## Instance d'application

Chaque application Vue commence par créer une nouvelle instance d'application avec la fonction `createApp` :

```js
import { createApp } from "vue";

const app = createApp({
  /* Les options du composant racine */
});
```

## Le composant racine

L'objet que nous passons dans `createApp` est en fait un composant. Chaque application nécessite un "composant racine" qui peut contenir d'autres composants.

Si vous utilisez des composants à fichier unique (Single-File Component), nous importons généralement le composant racine à partir d'un autre fichier :

```js
import { createApp } from "vue";
// Nous importons le composant racine App depuis un autre fichier
import App from "./App.vue";

const app = createApp(App);
```

Bien que de nombreux exemples de ce guide ne nécessitent qu'un seul composant, la plupart des applications réelles sont organisées en une arborescence de composants imbriqués et réutilisables. Par exemple, l'arborescence des composants d'une application Todo pourrait ressembler à ceci :

```
App (composant racine)
├─ TodoList
│  └─ TodoItem
│     ├─ TodoDeleteButton
│     └─ TodoEditButton
└─ TodoFooter
   ├─ TodoClearButton
   └─ TodoStatistics
```
