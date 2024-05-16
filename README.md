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

**Visual Studio Code**

```JSON
// .prettierrc
{
  "singleQuote": true,
  "semi": false
}
```

#### SVG Formatting 🪛

1. 选择语言模式
2. ".svg"的配置文件关联...
3. HTML

### CSS 🎨

```
❗️1rem = 1px❗️
```
