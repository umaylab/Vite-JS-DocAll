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
Dependencies:

- General-purpose glTF processing library
- [Draco](https://github.com/google/draco/): compression for mesh geometry
- [Meshoptimizer](https://github.com/zeux/meshoptimizer): compression for mesh geometry, point geometry, animation, and morph targets

1. General-purpose glTF processing library
2. General-purpose glTF processing library
3. General-purpose glTF processing library

## 👾 GSAP

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



