# Vue Template 💮

## Installation 🔧

### npm 📦

```SH
npm i -D unplugin-auto-import
npm i unplugin-vue-components -D
npm i -D unplugin-icons
npm i -D @iconify/json

npm install element-plus --save
```

## Configuration 📝

### Vite 🏗️

```JS
// vite.config.ts
import AutoImport from 'unplugin-auto-import/vite'

import Components from 'unplugin-vue-components/vite'
import { ElementPlusResolver } from 'unplugin-vue-components/resolvers'

import Icons from 'unplugin-icons/vite'
import IconsResolver from 'unplugin-icons/resolver'

export default defineConfig({
  plugins: [
    AutoImport({
      imports: ['vue', 'vue-router'],
      resolvers: [ElementPlusResolver()],
    }),

    Components({
      resolvers: [ElementPlusResolver(), IconsResolver()],
    }),

    Icons(),
  ],
})
```

### Prettier 🪮

```JSON
// .prettierrc
{
  "singleQuote": true,
  "semi": false
}
```
