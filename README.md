# wc-github-corners

[![Published on webcomponents.org](https://img.shields.io/badge/webcomponents.org-published-blue.svg)](https://www.webcomponents.org/element/wc-github-corners)
[![npm](https://img.shields.io/npm/v/wc-github-corners)](https://www.npmjs.com/package/wc-github-corners)
![npm bundle size](https://img.shields.io/bundlephobia/minzip/wc-github-corners)
![jsDelivr hits (npm)](https://img.shields.io/jsdelivr/npm/hy/wc-github-corners)

> [从零开始写一个 Web Component - GitHub Corners | 云游君的小站](https://www.yunyoujun.cn/posts/how-to-write-a-web-component/)

A web component by [lit](https://github.com/lit/lit) for [GitHub Corners](https://github.com/tholman/github-corners).

The final product is an ES module, and it can be used alone.

> Anywhere like Vanilla JS / Vue / React / Angular / Svelte ...

[Demo](https://www.yunyoujun.cn/wc-github-corners/)

<!--
```html
<custom-element-demo>
  <template>
    <script
      type="module"
      src="https://cdn.jsdelivr.net/npm/wc-github-corners@latest"
    ></script>
    <link rel="import" href="github-corners.html" />
    <github-corners></github-corners>
  </template>
</custom-element-demo>
```
-->

## Usage

```bash
npm i wc-github-corners
```

### By CDN

See [demo/index.html](./demo/index.html).

- jsdelivr: `https://cdn.jsdelivr.net/npm/wc-github-corners@latest`
- unpkg: `https://www.unpkg.com/wc-github-corners@latest`

```html
<!-- cdn -->
<script
  type="module"
  src="https://www.unpkg.com/wc-github-corners@latest"
></script>

<github-corners></github-corners>
```

### By NPM

```ts
// main.ts
import 'wc-github-corners'
```

```html
<!-- index.html -->
<github-corners></github-corners>
<github-corners repo="YunYouJun/wc-github-corners" blank />
```

I successfully used it in a vue project - [char-dust](https://github.com/YunYouJun/char-dust).

## API

### Example

```html
<github-corners fill="#0078e7" position="left" reverse></github-corners>
```

<!-- wc-api:start -->
<!-- prettier-ignore-start -->
<!-- markdownlint-disable -->
### `src/index.ts`:

#### class: `GitHubCorners`

##### Superclass

| Name         | Module | Package |
| ------------ | ------ | ------- |
| `LitElement` |        | lit     |

##### Fields

| Name       | Privacy | Type      | Default                         | Description                                                            | Inherited From |
| ---------- | ------- | --------- | ------------------------------- | ---------------------------------------------------------------------- | -------------- |
| `blank`    |         | `boolean` | `false`                         | target="\_blank" for link                                              |                |
| `color`    |         | `string`  | `'#fff'`                        | Font color                                                             |                |
| `fill`     |         | `string`  | `'#151513'`                     | Fill color for github corners                                          |                |
| `repo`     |         | `string`  | `'YunYouJun/wc-github-corners'` | Your GitHub Repo Name, generate url start with \<https\://github.com>. |                |
| `url`      |         | `string`  | `''`                            | You also can custom it to override the url generated by repo.          |                |
| `label`    |         | `string`  | `'View source on GitHub'`       | Hover title                                                            |                |
| `reverse`  |         | `boolean` | `false`                         | Reverse color and fill                                                 |                |
| `position` |         | `string`  | `'right'`                       | Position of github corners, 'left' or 'right'                          |                |

<hr/>

<!-- markdownlint-restore -->
<!-- prettier-ignore-end -->
<!-- wc-api:end -->

I written it as a tutorial in my [Bilibili Live Room](https://live.bilibili.com/822719).

Thanks to my fans and [sponsors](https://sponsors.yunyoujun.cn/).

## FAQ

### [Vue warn]: Failed to resolve component: github-corners

If you write it in vue template, you should make sure to exclude it from component resolution via `compilerOptions.isCustomElement`.

In vite:

```ts
import { defineConfig } from 'vite'
import Vue from '@vitejs/plugin-vue'

export default defineConfig({
  plugins: [
    Vue({
      include: [/\.vue$/, /\.md$/],
      template: {
        compilerOptions: {
          isCustomElement: (tag) => {
            return ['github-corners'].includes(tag)
          },
        },
      },
    }),
  ],
})
```

### Want to use by CDN in vue?

Try [@vueuse/head](https://github.com/vueuse/head).

```html
<script setup lang="ts">
  import { useHead } from "@vueuse/head";

  useHead({
    script: [
      {
        src: "https://cdn.jsdelivr.net/npm/wc-github-corners@latest",
        type: "module",
      },
    ],
  });
</script>
```

## [Sponsors](https://sponsors.yunyoujun.cn)

<p align="center">
  <a href="https://sponsors.yunyoujun.cn">
    <img src='https://cdn.jsdelivr.net/gh/YunYouJun/sponsors/public/sponsors.svg'/>
  </a>
</p>
