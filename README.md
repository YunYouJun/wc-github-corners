# wc-github-corners

[![Published on webcomponents.org](https://img.shields.io/badge/webcomponents.org-published-blue.svg)](https://www.webcomponents.org/element/wc-github-corners)
[![npm](https://img.shields.io/npm/v/wc-github-corners)](https://www.npmjs.com/package/wc-github-corners)
![npm bundle size](https://img.shields.io/bundlephobia/minzip/wc-github-corners)

A web component by [lit](https://github.com/lit/lit) for [GitHub Corners](https://github.com/tholman/github-corners).

The final product is an ES module, and it can be used alone.

> Anywhere like Vanilla JS / Vue / React / Angular / Svelte ...

[Demo](https://www.yunyoujun.cn/wc-github-corners/)

<!--
```html
<custom-element-demo>
  <template>
    <script
      module
      src="https://cdn.jsdelivr.net/npm/wc-github-corners@0.1.3"
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

```html
<!-- cdn -->
<script
  type="module"
  src="https://cdn.jsdelivr.net/npm/wc-github-corners"
></script>

<github-corners></github-corners>
```

### By NPM

```ts
// main.ts
import "wc-github-corners";
```

```html
<!-- index.html -->
<github-corners></github-corners>
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

| Name       | Privacy | Type      | Default                                 | Description                                   | Inherited From |
| ---------- | ------- | --------- | --------------------------------------- | --------------------------------------------- | -------------- |
| `blank`    |         | `boolean` | `false`                                 | target="\_blank" for link                     |                |
| `color`    |         | `string`  | `"#fff"`                                | Font color                                    |                |
| `fill`     |         | `string`  | `"#151513"`                             | Fill color for github corners                 |                |
| `repo`     |         | `string`  | `"YunYouJun/wc-github-corners"`         | Your GitHub Repo Name                         |                |
| `url`      |         |           | `` `https://github.com/${this.repo}` `` | Generated by repo, you also can custom it.    |                |
| `label`    |         | `string`  | `"View source on GitHub"`               | Hover title                                   |                |
| `reverse`  |         | `boolean` | `false`                                 | Reverse color and fill                        |                |
| `position` |         | `string`  | `"right"`                               | Position of github corners, 'left' or 'right' |                |

<hr/>

<!-- markdownlint-restore -->
<!-- prettier-ignore-end -->

<!-- wc-api:end -->

I written it as a tutorial in my [Bilibili Live Room](https://live.bilibili.com/822719).

Thanks to my fans and [sponsors](https://sponsors.yunyoujun.cn/).
