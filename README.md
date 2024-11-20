# Vite-JS-DocAll

## 🔗 Quick Links

1. [Vite.JS](#-vitejs)
2. [GSAP](#-gsap)
3. [Bootstrap](#-bootstrap)
4. [JQuery](#-jquery)
5. [Barba.JS](#-barbajs)
6. [Pixi.JS](#-pixijs)
7. [Model-Viewer](#-model-viewer)
8. [Mind-AR](#-mind-ar)
6. [Three.JS](#-threejs)


## Overview

Monorepo containing plugins for two popular bundlers (Vite and Rollup) allowing each to process and optimize 3D models used by a web application. While bundlers can process traditional web content — like CSS or images — out of the box or with existing plugins, bundlers lack any understanding of 3D content. This project orchestrates processing of models using the [glTF-Transform](https://gltf-transform.donmccurdy.com/) library, and includes configuration flexible enough to select among existing processing stages or to define and add new methods.

## 👾 Vite.JS
Install vitejs 

1. Pada terminal install viteJS :   [``` npm create vite@latest ```](#)
2. Setting pada terminal pilih —> vanilla Javascript, dan ikuti petunjuknya
3. Pilih lokasi folder yang digunakan sebagai projeknya
4. lalu ketik : $${\color{orange}npm i}$$  —> untung menginstall
5. Setelah terinstal di folder projeknya buka dan hapus beberapa file yang tidak dibutuhkan
    spt: counter.js, javascript.svg, id=“app” pada index.html dan hapus semua isi file dari file main.js
6. Buat link stylesheet (.css) pada index.html sebagai (.scss) : —>  [link rel=“stylesheet” href=“css/main.scss” ](#)
8. Buat folder diroot —> css folder dan buat file main.scss   ${{\color{Goldenrod}\Huge{\textsf{  npm\ threejs\ install\ pakujawacode\}}}}\$
9. Install sass : —> [``` npm i -D sass ```](#)
10. Coba Running dengan : —> [``` npm run dev ```](#)


## 👾 GSAP

```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```


```diff 
text in purple (and bold)
```

${{\color{Goldenrod}\Huge{\textsf{  Hi\ there\ \}}}}\$

${{\color{Goldenrod}\Large{\textsf{  Hi\ there\ \}}}}\$

${{\color{Goldenrod}Medium{textsf{  Hi there }}}}$

${{\color{orange}\Medium{\textsf{  Hi\ there\ \}}}}\$

${{\color{green}\Medium{\textsf{  Hi\ there\ \}}}}\$

${{\color{greenyellow}\Medium{\textsf{  Hi\ there\ \}}}}\$


${{\color{red}\Medium{\textsf{  Hi\ there\ \}}}}\$

${{\color{blue}\Medium{\textsf{  Hi\ there\ \}}}}\$




### 1. Installation

Rollup:

```shell
npm install --save-dev rollup-plugin-gltf
```

Vite:

```shell
npm install --save-dev vite-plugin-gltf
```

## 👾 Bootstrap
Dependencies:

- [glTF Transform](https://gltf-transform.donmccurdy.com/): general-purpose glTF processing library
- [Draco](https://github.com/google/draco/): compression for mesh geometry
- [Meshoptimizer](https://github.com/zeux/meshoptimizer): compression for mesh geometry, point geometry, animation, and morph targets

### 2. Minimal Configuration

The plugin is unopinionated about which optimizations should be applied to your glTF models. Here is a minimal configuration that simply applies Draco compression of your assets:

```js
// *.config.js
import gltf from "rollup-plugin-gltf"; // (a) Rollup
import gltf from "vite-plugin-gltf"; // (b) Vite

import { draco } from "@gltf-transform/functions";

return {
  // ...
  plugins: [
    gltf({
      transforms: [draco()],
    }),
  ],
};
```

See [advanced configuration](#advanced-configuration) for more complex examples.

_SvelteKit:_ it seems that in SvelteKit SSR should be disabled in order to avoid mysterious `ReferenceError` issues - see issues filed [here](https://github.com/nytimes/rd-bundler-3d-plugins/issues/19) and on the [SvelteKit repo](https://github.com/sveltejs/kit/issues/9000).

### 3. Asset Placement

## 👾 JQuery
Dependencies:

- [glTF Transform](https://gltf-transform.donmccurdy.com/): general-purpose glTF processing library
- [Draco](https://github.com/google/draco/): compression for mesh geometry
- [Meshoptimizer](https://github.com/zeux/meshoptimizer): compression for mesh geometry, point geometry, animation, and morph targets



## 👾 Barba.JS
Dependencies:

- [glTF Transform](https://gltf-transform.donmccurdy.com/): general-purpose glTF processing library
- [Draco](https://github.com/google/draco/): compression for mesh geometry
- [Meshoptimizer](https://github.com/zeux/meshoptimizer): compression for mesh geometry, point geometry, animation, and morph targets



