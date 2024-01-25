# 目次

1. [Vue3について](#vue3について)
1. [ツール](#ツール)
1. [Vueプロジェクト作成](#vueプロジェクト作成)
1. [Firebaseについて](#Firebaseについて)

# Vue3について

公式サイト: https://ja.vuejs.org/

### Vue2の終了

### Vueでの登場人物

- Vue.js
- Vue CLI / Vite
- Vuex / Pinia
- Vuetify
- Typescript
    - 公式サイトはJavascriptで表現されていることが多い
    - 開発現場ではTypescriptを利用していることが多い

## 文法の違い

- Options API / Composition API
    - https://ja.vuejs.org/guide/extras/composition-api-faq.html
- SFC(Single-File Components)
- refを使う理由
    - https://ja.vuejs.org/guide/essentials/reactivity-fundamentals

## ツール

- Vite
    - [Vue CLI->Vite推奨](https://vuejs.org/guide/scaling-up/tooling.html)
- VSCode拡張機能
    - [IDE Support](https://vuejs.org/guide/scaling-up/tooling.html#ide-support)
    - Vue Language Features(Volar)
    - Vue Volar extension Pack
    - Vue2のときのVeturは使わない

# 環境

- nvmでnodeのバージョンを管理

# Vue3移行ガイド

https://v3-migration.vuejs.org/

```console
npm install -g yarn
```

# Vueプロジェクト作成

#### Vue CLI

```console
vue create [project]
```

#### Vuetify

```console
yarn create vuetify
```

#### Vite (今回はこれ)

```console
yarn create vite
```

## 既存プロジェクトにvuetifyを追加するとき

https://vuetifyjs.com/en/getting-started/installation/#existing-projects

```console
yarn add vuetify
```

`main.ts`に追記

```ts
import { createApp } from 'vue'
import './style.css'
import App from './App.vue'

// Vuetify
import 'vuetify/styles'
import { createVuetify } from 'vuetify'
import * as components from 'vuetify/components'
import * as directives from 'vuetify/directives'

const vuetify = createVuetify({
  components,
  directives,
})

createApp(App).use(vuetify).mount('#app')
```

# Firebaseについて