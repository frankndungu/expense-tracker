# expense-tracker

This template should help get you started developing with Vue 3 in Vite.

## Recommended IDE Setup

[VSCode](https://code.visualstudio.com/) + [Volar](https://marketplace.visualstudio.com/items?itemName=Vue.volar) (and disable Vetur).

## Customize configuration

See [Vite Configuration Reference](https://vitejs.dev/config/).

## Project Setup

```sh
npm install
```

### Options API

- Added data to the component array and looped over it using the v-for directive
- ':class' and ':key' directives have been used as well to output the data
```
<li v-for="transaction in transactions" :key="transcation.id" :class="transaction.amount < 0 : 'minus' : 'plus'"> 
</li>

```
