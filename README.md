# Vite.js-DocAll

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


### Note:
- Install Xcode (Xcode Command Line Developer Tools)  xcode-select --install ….
- Install NodeJS + Payton first….


## PROSES:

1. install ViteJS : —>  [``` npm create vite@latest ```](#)
2. Buat file ( vite.config.js )
3. Buat folder2 —> src dll
4. Buat folder Fonts untk meyimpan font custom dan jangan lupa gunakan import agar include (build vitejs)
4. Install plugin optimalisasi gltf file (build file .gltf) : —>  [``` npm install --save-dev vite-plugin-gltf ```](#)
5. Install vite-plugin-inspect : -> [``` npm i -D vite-plugin-inspect ```](#) dan copy configurasinya : (https://github.com/antfu-collective/vite-plugin-inspect)
4. Copy file CSS ( core.scss )
5. Install Sass : —>  [``` $ npm i -D sass ```](#)
6. Install Bootstrap : —> [``` npm i bootstrap@v5.2.3 ```](#)
7. Install JQuery : —> [``` npm install jquery ```](#)
8. Install GSAP : —>  [``` npm install gsap ```](#) | [``` npm install ./gsap-bonus.tgz ```](#)
9. Buat file Routing : headerFooterManager.js 
10. Install BarbaJS : —> [``` npm install @barba/core ```](#)
12. Install PixiJS : —> [``` npm install pixi.js ```](#)
11. Install 3d library <model-viewer> : —> [``` npm install @google/model-viewer ```](#)
12. Install Mind-AR : —> [``` npm i mind-ar --save ```](#)
13. Install Threejs : —> [``` npm i three —save-dev ```](#)



## 👾 Vite.JS
Install vitejs 

1. Pada terminal install viteJS :   [``` npm create vite@latest ```](#)
2. Setting pada terminal pilih —> vanilla Javascript, dan ikuti petunjuknya
3. Pilih lokasi folder yang digunakan sebagai projeknya
4. lalu ketik : [``` npm i```](#)  —> untung menginstall
5. Setelah terinstal di folder projeknya buka dan hapus beberapa file yang tidak dibutuhkan
    spt: counter.js, javascript.svg, id=“app” pada index.html dan hapus semua isi file dari file main.js
6. Buat link stylesheet (.css) pada index.html sebagai (.scss) : —>  [``` link rel=“stylesheet” href=“css/main.scss”```](#)
8. Buat folder diroot —> css folder dan buat file  ${{\color{orange}\Huge{\textsf{  main.scss\}}}}\$
9. Install sass : —> [``` npm i -D sass ```](#)
10. Coba Running dengan : —> [``` npm run dev ```](#)



main.js —> in viteJs:

```js
import './style.css'
import javascriptLogo from './javascript.svg'
import viteLogo from '/vite.svg'
import { setupCounter } from './counter.js'
```

File : vite.config.js

```js
// vite.config.js
import { resolve } from 'path'
import { defineConfig } from 'vite'

export default defineConfig({
  build: {
    rollupOptions: {
      input: {
        main: resolve(__dirname, 'index.html'),
        src: resolve(__dirname, 'src/home.html')
      }
    }
  },


  css: {
    preprocessorOptions: {
      scss: {
        api: 'modern-compiler' // or "modern"
      }
    }
  },

  
})


```

## 👾 GSAP
1. Copy file plugin ke dalam root directory projek dengan mendrag filenya… 
2. Kemudian Install :  —> npm install 
3. Link doc : https://gsap.com/docs/v3/Installation?tab=npm&module=esm&method=zip&tier=free&club=true&require=false&trial=true 

### 1. Installation

Setup index.html....
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Main</title>
</head>
<body>
  <special-header></special-header>
    <div id="smooth-wrapper">
        <div id="smooth-content">

          
              <!-- Section 1 -->
              <div class="pull-nav"><h3>Transition<br></h3></div>
              <section class="section1">
                <div class="konten1">
                    <div class="lembar obj01">1</div>
                    <div class="lembar obj02">2</div>
                    <div class="lembar obj03">3</div>
                    <div class="lembar obj04">4</div>
                    <div class="lembar obj05">5</div>
                    <div class="obj06">6</div>
    
    
    
                  </div>
              </section>


              </section>
    
    
              <!-- Section 2 -->
              <div class="col-lg-12"><h3 class="text-center" style="background-color: rgb(24, 24, 24);">Konten 02-00<br></h3></div>
              <section class="section2">
                <div class="konten2">
                    <div class="lembar2 obj01">1</div>
                    <div class="lembar2 obj02">2</div>
                    <div class="lembar2 obj03">3</div>
                    <div class="lembar2 obj04">4</div>
                    <div class="lembar2 obj05">5</div>
                    <div class="obj06">6</div>
      
      
      
                  </div>
              </section>
      
      
      
              <!-- Section 3 -->
              <div class="col-lg-12"><h3 class="text-center" style="background-color: rgb(24, 24, 24);">Konten 03-00<br></h3></div>
              <section class="section3">
                <div class="konten3">
                    <div class="lembar3 obj01">1</div>
                    <div class="lembar3 obj02">2</div>
                    <div class="lembar3 obj03">3</div>
                    <div class="lembar3 obj04">4</div>
                    <div class="lembar3 obj05">5</div>
                    <div class="obj06">6</div>
      
      
      
                  </div>
              </section>
      
      
      
      
              <!-- Section 4 -->
              <div class="col-lg-12"><h3 class="text-center" style="background-color: rgb(24, 24, 24);">Konten 04-00<br></h3></div>
              <section class="section4">
                <div class="konten4">
                    <div class="lembar4 obj01">1</div>
                    <div class="lembar4 obj02">2</div>
                    <div class="lembar4 obj03">3</div>
                    <div class="lembar4 obj04">4</div>
                    <div class="lembar4 obj05">5</div>
                    <div class="obj06">6</div>
      
      
      
                  </div>
              </section>
      
      
      
              <!-- Section 5 -->
              <div class="col-lg-12"><h3 class="text-center" style="background-color: rgb(24, 24, 24);">Konten 05-00<br></h3></div>
              <section class="section5">
                <div class="konten5">
                    <div class="lembar5 obj01">1</div>
                    <div class="lembar5 obj02">2</div>
                    <div class="lembar5 obj03">3</div>
                    <div class="lembar5 obj04">4</div>
                    <div class="lembar5 obj05">5</div>
                    <div class="obj06">6</div>
      
      
      
                  </div>
              </section>
      
      
      
      
              <!-- Section 6 -->
              <div class="col-lg-12"><h3 class="text-center" style="background-color: rgb(24, 24, 24);">Konten 06-00<br></h3></div>
              <section class="section6">
                <div class="konten6">
                    <div class="lembar6 obj01">1</div>
                    <div class="lembar6 obj02">2</div>
                    <div class="lembar6 obj03">3</div>
                    <div class="lembar6 obj04">4</div>
                    <div class="lembar6 obj05">5</div>
                    <div class="obj06">6</div>
      
      
      
                  </div>
              </section>
      
      
      
              <!-- Section 7 -->
              <div class="col-lg-12"><h3 class="text-center" style="background-color: rgb(24, 24, 24);">Konten 07-00<br></h3></div>
              <section class="section7">
                <div class="konten7">
                    <div class="lembar7 obj01">1</div>
                    <div class="lembar7 obj02">2</div>
                    <div class="lembar7 obj03">3</div>
                    <div class="lembar7 obj04">4</div>
                    <div class="lembar7 obj05">5</div>
                    <div class="obj06">6</div>
      
      
      
                  </div>
              </section>
      
      
      
              <!-- Section 8 -->
              <div class="col-lg-12"><h3 class="text-center" style="background-color: rgb(24, 24, 24);">Konten 08-00<br></h3></div>
              <section class="section8">
                <div class="konten8">
                    <div class="lembar8 obj01">1</div>
                    <div class="lembar8 obj02">2</div>
                    <div class="lembar8 obj03">3</div>
                    <div class="lembar8 obj04">4</div>
                    <div class="lembar8 obj05">5</div>
                    <div class="obj06">6</div>
      
      
      
                  </div>
              </section>
      
      
      
      
              <!-- Section 9 -->
              <div class="col-lg-12"><h3 class="text-center" style="background-color: rgb(24, 24, 24);">Konten 09-00<br></h3></div>
              <section class="section9">
                <div class="konten9">
                    <div class="lembar9 obj01">1</div>
                    <div class="lembar9 obj02">2</div>
                    <div class="lembar9 obj03">3</div>
                    <div class="lembar9 obj04">4</div>
                    <div class="lembar9 obj05">5</div>
                    <div class="obj06">6</div>
      
      
      
                  </div>
              </section>
      
      
      
      
              <!-- Section 10 -->
              <div class="col-lg-12"><h3 class="text-center" style="background-color: rgb(24, 24, 24);">Konten 10-00<br></h3></div>
              <section class="section10">
                <div class="konten10">
                    <div class="lembar10 obj01">1</div>
                    <div class="lembar10 obj02">2</div>
                    <div class="lembar10 obj03">3</div>
                    <div class="lembar10 obj04">4</div>
                    <div class="lembar10 obj05">5</div>
                    <div class="obj06">6</div>
      
      
      
                  </div>
              </section>
  


  
  
        </div>
      </div>

    <!-- script js -->
    <script type="module" src="./src/js/headerFooterManager.js"></script>
    <script type="module" src="main.js"></script>

</body>
</html>

```

File style.scss /css

```scss
/* @import "bootstrap/scss/bootstrap"; */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
  }
  
  
  body {
    background-color: #111;
    overscroll-behavior: none;
    font-family: "Signika Negative", sans-serif, Arial;
    margin: 0;
    padding: 0;
    overflow-x: hidden;
    color: white;
  }
  
  /* BG PUTIH */
  #smooth-content {
    overflow: visible;
    width: 100%;
    /* set a height because the contents are position: absolute, thus natively there's no height */
    height: 60000px;
  
    background-image:
    linear-gradient(rgba(255, 255, 255, 0.07) 2px, transparent 2px),
    linear-gradient(90deg, rgba(255, 255, 255, 0.07) 2px, transparent 2px),
    linear-gradient(rgba(255, 255, 255, 0.06) 1px, transparent 1px),
    linear-gradient(90deg, rgba(255, 255, 255, 0.06) 1px, transparent 1px);
    background-size: 100px 100px, 100px 100px, 20px 20px, 20px 20px;
    background-position: -2px -2px, -2px -2px, -1px -1px, -1px -1px;
  
  }
  
  .pull {
  width: 100vw;
  height: 50px;
  color: white;
  padding: 10px;
  text-align: center;
  background-color: rgb(85, 55, 16);
  }

  .pull-nav {
    width: 100vw;
    height: 50px;
    color: white;
    padding: 10px;
    text-align: start;
    background-color: rgb(16, 84, 85);
    }
  /* ======================================================= */


  /* ------- Section 1 ----------------- */

    .section1 {
      width: 100%;
    }
    
    .konten1 {
      height: 700px;
      background-color: #89bab631;
      position: relative;
    }
    
    .lembar {
      width: 50px;
      height: 50px;
      position: absolute;
    }
    
    .obj01 {
      left: 0px;
      top: 0px;
      background-color: rgb(224, 131, 250);
    }
    
    .obj02 {
      right: 0px;
      background-color: rgb(79, 161, 35);
    }
    
    .obj03 {
      right: 0px;
      bottom: 0px;
      background-color: rgb(159, 68, 54);
    }
    
    .obj04 {
      left: 50%;
      top: 50%;
      background-color: rgb(92, 122, 198);
    }
    
    .obj05 {
      bottom: 0px;
      background-color: rgb(230, 53, 148);
    }
    
    .konten1 .obj06 {
      width: 50px;
      height: 50px;
      left: 50%;
      bottom: 0px;
      /* bottom: 0; */
      position: absolute;
      background-color: rgb(230, 186, 53);
    }
    


    
  
    /* ------- Section 2 ----------------- */
  
    .section2 {
      width: 100%;
    }
    
    .konten2 {
      height: 700px;
      background-color: #ba968931;
      position: relative;
    }
    
    .lembar2 {
      width: 50px;
      height: 50px;
      position: absolute;
    }
  
  
  
  
    /* ------- Section 3 ----------------- */
  
    .section3 {
      width: 100%;
    }
    
    .konten3 {
      height: 700px;
      background-color: #89bab631;
      position: relative;
    }
    
    .lembar3 {
      width: 50px;
      height: 50px;
      position: absolute;
    }
  
  
  
  
    /* ------- Section 4----------------- */
  
    .section4 {
      width: 100%;
    }
    
    .konten4 {
      height: 700px;
      background-color: #ba968931;
      position: relative;
    }
    
    .lembar4 {
      width: 50px;
      height: 50px;
      position: absolute;
    }
  
  
  
  
   /* ------- Section 5 ----------------- */
  
    .section5 {
      width: 100%;
    }
    
    .konten5 {
      height: 700px;
      background-color: #89bab631;
      position: relative;
    }
    
    .lembar5 {
      width: 50px;
      height: 50px;
      position: absolute;
    }
  
  
  
  
    /* ------- Section 6 ----------------- */
  
    .section6 {
      width: 100%;
    }
    
    .konten6 {
      height: 700px;
      background-color: #ba968931;
      position: relative;
    }
    
    .lembar6 {
      width: 50px;
      height: 50px;
      position: absolute;
    }
  
  
  
  
    /* ------- Section 7 ----------------- */
  
    .section7 {
      width: 100%;
    }
    
    .konten7 {
      height: 700px;
      background-color: #89bab631;
      position: relative;
    }
    
    .lembar7 {
      width: 50px;
      height: 50px;
      position: absolute;
    }
      
  
  
  
  
    /* ------- Section 8 ----------------- */
  
    .section8 {
      width: 100%;
    }
    
    .konten8 {
      height: 700px;
      background-color: #ba968931;
      position: relative;
    }
    
    .lembar8 {
      width: 50px;
      height: 50px;
      position: absolute;
    }
  
  
  
    /* ------- Section 9 ----------------- */
  
    .section9 {
      width: 100%;
    }
    
    .konten9 {
      height: 700px;
      background-color: #89bab631;
      position: relative;
    }
    
    .lembar9 {
      width: 50px;
      height: 50px;
      position: absolute;
    }
  
  
  
  
    /* ------- Section 10 ----------------- */
  
    .section10 {
      width: 100%;
    }
    
    .konten10 {
      height: 700px;
      background-color: #ba968931;
      position: relative;
    }
    
    .lembar10 {
      width: 50px;
      height: 50px;
      position: absolute;
    }
  

```

File main.js 

```js
main,js
==============

import { gsap } from "gsap";
import { ScrollTrigger } from "gsap/ScrollTrigger";

/* The following plugins are Club GSAP perks */
import { DrawSVGPlugin } from "gsap/DrawSVGPlugin";
import { ScrollSmoother } from "gsap/ScrollSmoother";
import { GSDevTools } from "gsap/GSDevTools";
import { MotionPathHelper } from "gsap/MotionPathHelper";
import { MotionPathPlugin } from "gsap/MotionPathPlugin";
import { ScrollToPlugin } from "gsap/ScrollToPlugin";
import { Draggable } from "gsap/Draggable";
import { Flip } from "gsap/Flip";
import { SplitText } from "gsap/SplitText";



gsap.registerPlugin(gsap, ScrollTrigger, ScrollSmoother, SplitText, DrawSVGPlugin, MotionPathPlugin, MotionPathHelper, GSDevTools, ScrollToPlugin, Draggable, Flip);



// create the smooth scroller FIRST!
let smoother = ScrollSmoother.create({
  smooth: 1,
  effects: true,
  normalizeScroll: true
});

```

## 👾 Bootstrap

- Runing pada Terminal : npm install bootstrap@5.3.3
Style.css

```scss
style.scss
==========

@import "bootstrap/scss/bootstrap";
```

Main.js

```js
main.js
==========

// Import our custom CSS --> disesuaikan lokasi CSS nya yang sudah import bootstramp
import './page.scss';

// Import all of Bootstrap's JS
import * as bootstrap from "bootstrap";

```

## Setup & Run BUILD Multi-Page App

1. Buat konfigurasi file pada projek vite

```js
Buat file pada root :  vite.config.js. 
Isikan filenya : 

// vite.config.js
import { resolve } from 'path'
import { defineConfig } from 'vite'

export default defineConfig({
  build: {
    rollupOptions: {
      input: {
        main: resolve(__dirname, 'index.html'),
        page: resolve(__dirname, 'src/page1.html')
      }
    }
  },

  css: {
    preprocessorOptions: {
      scss: {
        api: 'modern-compiler' // or "modern"
      }
    }
  }


  
})



```

2.  jalankan —> [``` npm i -D vite-plugin-inspect ```](#)

rev doc: ```https://github.com/antfu-collective/vite-plugin-inspect```
         ```https://v3.vitejs.dev/guide/build```

### BUAT HEADER & FOOTER

headerFooterManager.js

```js
headerFooterManager.js
========================

class SpecialHeader extends HTMLElement {
    connectedCallback() {
        this.innerHTML = `
        <style>
          .headku {
            width: 100%;
            height: 50px;
            /*background-color: yellowgreen;*/
            position: fixed;
            z-index: 1000;
          }

          ul {
            list-style-type: none;
            /* margin: 0; */
            margin-right: 50px;
            padding: 0;
            overflow: hidden;
          }

          li {
            float: right;
          }

          li a {
            display: block;
            color: white;
            text-align: center;
            padding: 14px 16px;
            text-decoration: none;
          }

          li a:hover {
            /* background-color: #111; */
          }
        </style>
        <div class="headku">
          <ul>
            <li><a href="#detail">DetailComponent</a></li>
            <li><a href="#businesse">BisnisSection</a></li>
            <li><a href="#fonts">Fonts</a></li>
            <li><a href="#interaction">Interaction</a></li>
            <li><a href="#animation">Animation</a></li>
            <li><a href="/src/page1.html">Transition</a></li>
            <li><a class="active" href="/">Navigation</a></li>
          </ul>
        </div>
        `
    }
}

class SpecialFooter extends HTMLElement {
    connectedCallback() {
        this.innerHTML = `
        <p style="display: flex; justify-content: space-around; background-color: blueviolet;">
        `
    }
}


customElements.define('special-header', SpecialHeader)
customElements.define('special-footer', SpecialFooter)

```
### TERMINAL :
```
- npm run dev -------------------------------------------
- npm run build -----------------------------------------
- npm run preview ---------------------------------------

- Ctrl + C  ——>  refresh to new terminal
```
video : https://www.youtube.com/watch?v=e60d_M-p8nc


## 👾 Barba.JS


## 👾 Pixi.JS


## 👾 Model-Viewer


## 👾  VITE + THREEJS
Three.JS

https://www.youtube.com/watch?v=0C4Ydy20PL4

1. Terminal : npm i three —save-dev
2. buka halaman website threejs  —> pada klik menu dokumentasi —> Create a Scene —> copy code yang paling bawah (js)


## 👾 VITE + MindAR
Mind-AR

Catalan : harus menggunakan nodeJS versi 18.12.1 (versi lama)

1.  Install ThreeJS : ——————>  [``` npm i three —save-dev ```](#)
2.  Install MindAR : ——————> [``` npm i mind-ar --save ```](#)


## 👾  VITE + JQUERY
JQuery

1. Install Jquery : —>  npm install jquery 
2. Buat file( .js) untuk isi dari function jQuery ( _jquery.js), maka semua isi code jQuery ada disini.
3. jangan lupa selalu mendambahkan :
    - import $ from ‘jquery’ ;
    - window.$ = window.jQuery = $;
  
 Contoh File:  _jquery.js
 ```js
import $ from 'jquery';
window.$ = window.jQuery = $;

jQuery(document).ready(function($){
    $('.tabs').on('click', function(){
        var tab = $(this);
        
        tab.addClass('is-active');
        
        if ( tab.siblings().hasClass('is-active') ) {
            tab.siblings().removeClass('is-active');
        }
    });
  });

```

4. Import file _jquery.js yang telah dibuat diatas didalam file javascript produksi contoh file : (animasi.js)
5. jadi file khusus jQuery fungsi filenya terpisah dari file javascript untuk apps dan di import…..
    cari dimana lokasi file jQuery function berada kemudian impor pada file javascript menggunakan :  —>   import './lib/_jquery';

   con: file —> animasi.js
   ```js
   // import dari lokasi file fungsi jQuery
   import './lib/_jquery';


   tambahan : jika terjadi sesuatu yang kurang bisa coba tambahkan "modul" link jquery pada file HTML nya….
   <script type="module" src="https://code.jquery.com/jquery-3.3.1.js"></script>
   atau
   <script type="module" src="../node_modules/jquery/dist/jquery.min.js"></script>
   
   ```

## 👾 VITE + model-viewer
Catatan: Untuk <model-viewer> —> didalamnya sudah terdapat package threejs library
                Jangan install threeJs Library dahulu jika ingin menggunakan library dari  <model-viewer>

### install package
npm install @google/model-viewer

```scss
< MODEL-VIEWER >
1. Instal Model-Viewer dengan NPM install seperti diatas
2. copy code pada HTML :
-------------------------
     <div class="model3d">
        <model-viewer class="tigadimensi" id="orbit-demo"  src="./assets/Chair.glb" alt="A 3D model of an Chair" auto-rotate="" camera-controls="" background-color="#455A64" ar-status="not-presenting" disable-zoom ></model-viewer>
      </div>
      
      
      // import dari javascript .......
      <script type="module" src="/main.js"></script>
      
      

3. style.css
--------------

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
background-color: #111;
font-family: "Signika Negative", sans-serif, Arial;
overscroll-behavior: none;
margin: 0;
padding: 0;
overflow-x: hidden;
/* overflow-y: hidden !important; */
}

/* .model3d{
  width: 800px;
  height: 800px;
  background-color: aqua;
} */


.section39 {
  width: 100%;
  height: 700px;
  background-color: #1c5488;
  display: flex;
  justify-content: center;
  align-items: center;
}

.tigadimensi {
  width: 700px;
  height: 700px;
  /* background-color: #03c9a9; */

}


4. main.js
--------------
import './style.css';
import { ModelViewerElement } from '@google/model-viewer';

```


## 👾 Downgrade/Upgrade NODEJS version ( Node Version Manager )

- install tools di terminal dengan nama : Node Version Manager  : contoh: nvm -v
- https://github.com/nvm-sh/nvm#install--update-script
- https://www.youtube.com/watch?app=desktop&v=PIR0oBVowXU

- instal di terminal/vscode:
- curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.40.1/install.sh | bash
- Catatatan: harus telah menginstal = (Xcode Command Line Developer Tools)  xcode-select --install
- Lihat semua versi NodeJs = nvm ls-remote
- run : ——>  nvm use v18.17.1
- run: ——> nvm install v18.17.1
- node JS berubah versi menjadi v18.17.1



## Library Javascript

1. GSAP
2. Bootstramp
3. ThreeJS
4. Model-Viewer
5. MindAR
6. PixiJS
7. Barba JS
8. Threeasy
9. JQuery






## Overview

Monorepo containing plugins for two popular bundlers (Vite and Rollup) allowing each to process and optimize 3D models used by a web application. While bundlers can process traditional web content — like CSS or images — out of the box or with existing plugins, bundlers lack any understanding of 3D content. This project orchestrates processing of models using the [glTF-Transform](https://gltf-transform.donmccurdy.com/) library, and includes configuration flexible enough to select among existing processing stages or to define and add new methods.



## 🔡 Configuration

Customize your README generation using these CLI options:

| Option            | Description                                   | Default           |
|-------------------|-----------------------------------------------|-------------------|
| `--align`         | Text alignment in header                      | `center`          |
| `--api`           | LLM API service provider                      | `offline`         |
| `--badge-color`   | Badge color name or hex code                  | `0080ff`          |
| `--badge-style`   | Badge icon style type                         | `flat`            |



## 🎨 Examples

View example README files generated by readme-ai across various Tech Stacks:

| Technology | Example Output | Repository | Description |
|------------|---------------|------------|-------------|
| Readme-ai | [readme-ai.md][default] | [readme-ai][readme-ai] | Readme-ai project |
| Apache Flink | [readme-pyflink.md][modern-header] | [pyflink-poc][pyflink] | Pyflink project |
| Streamlit | [readme-streamlit.md][svg-banner] | [readme-ai-streamlit][streamlit] | Streamlit web app |


<sub>Find additional README examples in the [examples directory](https://github.com/eli64s/readme-ai/tree/main/examples).</sub>

---



## 👾 Warna
Referensi warna:

```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```

- ${{\color{Goldenrod}\Huge{\textsf{  gold\ color\ \}}}}\$
- ${{\color{orange}\Huge{\textsf{  orange\ color\ \}}}}\$
- ${{\color{red}\Huge{\textsf{  red\ color\ \}}}}\$
- ${{\color{green}\Huge{\textsf{  green\ color\ \}}}}\$
- ${{\color{greenyellow}\Huge{\textsf{  greenyellow\ color\ \}}}}\$



