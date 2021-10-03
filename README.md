# GhostCSS
[![Netlify Status](https://api.netlify.com/api/v1/badges/7643a1ba-a4c3-4620-993b-522ae3e40282/deploy-status)](https://app.netlify.com/sites/ghostcss/deploys)

Build complex ui's and ux's using ghostCSS, the next generation of css.

https://ghostcss.netlify.app

## Installation

Create a new vite app
```
$ npm init vite my-ghost-project
```

Install dependencies
```
$ cd my-ghost-project
$ npm install -D postcss tailwindcss autoprefixer
```

Create config
```
npx tailwindcss init -p
```

Paste this in `postcss.config.js`
```javascript
module.exports = {
mode: 'jit',
purge: ['./index.html', './*.{html,htm}'],
darkMode: 'media', // or 'media' or 'class'
theme: {
extend: {
zIndex: {
'top': '10000'
},
spacing: {
'128': '32rem',
'144': '36rem',
},
screens: {
'portrait': { 'raw': '(orientation: portrait)' },
'm2xl': { 'max': '1535px' },
'mxl': { 'max': '1279px' },
'mlg': { 'max': '1023px' },
'mmd': { 'max': '767px' },
'msm': { 'max': '639px' },
},
borderWidth: {
'1': '1px'
}
},
},
variants: {},
plugins: [],
}
```

paste https://ghostcss.netlify.app/tailwind.css in `index.css`

```
npm run dev
```
Now your site is running!

<a href="https://ghostcss.netlify.app/docs/index.html">Docs</a>

