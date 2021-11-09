# GhostCSS

[![Netlify Status](https://api.netlify.com/api/v1/badges/7643a1ba-a4c3-4620-993b-522ae3e40282/deploy-status)](https://app.netlify.com/sites/ghostcss/deploys)
![Forks](https://img.shields.io/github/forks/anay-v2/GhostCSS?style=social)
![Stars](https://img.shields.io/github/stars/anay-v2/GhostCSS?style=social)
![Watchers](https://img.shields.io/github/watchers/anay-v2/GhostCSS?style=social)
![Issues](https://img.shields.io/github/issues-raw/anay-v2/GhostCSS)
![PRs'](https://img.shields.io/github/issues-pr-raw/anay-v2/GhostCSS)
![Last Commit](https://img.shields.io/github/last-commit/anay-v2/GhostCSS)
![Commit Activity](https://img.shields.io/github/commit-activity/m/anay-v2/GhostCSS)
![Website](https://img.shields.io/website?down_color=red&down_message=offline&label=site&up_color=green&up_message=working&url=https%3A%2F%2Fghostcss.netlify.app)

Build complex ui's and ux's using ghostCSS, the next generation of css.

[https://ghostcss.netlify.app](https://ghostcss.netlify.app)

## Installation

1. Create a new vite app

```sh
$ npm init vite my-ghost-project
```

2. Install dependencies

```sh
$ cd my-ghost-project
$ npm install -D postcss tailwindcss autoprefixer
```

3. Create config

```sh
$ npx tailwindcss init -p
```

4. Paste this in `tailwind.config.js`

```javascript
module.exports = {
  mode: 'jit',
  purge: ['./src/index.html', './src/*.{html,htm}', './src/**/*.{html,htm}'],
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
      },
      colors: {
        'primary': {
          'light': '#BFDBFE',
          'DEFAULT': '#3B82F6',
          'dark': '#1E40AF'
        },
        'secondary': '#6B7280',
        'light': '#E5E7EB',
        'dark': '#1F2937',
        'success': {
          'light': '#A7F3D0',
          'DEFAULT': '#10B981',
          'dark': '#065F46'
        },
        'danger': {
          'light': '#FECACA',
          'DEFAULT': '#EF4444',
          'dark': '#991B1B'
        },
        'warning': {
          'light': '#FDE68A',
          'DEFAULT': '#F59E0B',
          'dark': '#92400E'
        },
        'info': {
          'light': '#CFFAFE',
          'DEFAULT': '#22D3EE',
          'dark': '#0E7490'
        },
        'special': {
          'light': '#FECDD3',
          'DEFAULT': '#F43F5E',
          'dark': '#9F1239'
        },
        'tropic': {
          'light': '#FED7AA',
          'DEFAULT': '#F97316',
          'dark': '#9A3412'
        },
        'tertiary': {
          'light': '#E9D5FF',
          'DEFAULT': '#A855F7',
          'dark': '#6B21A8'
        }
      }
    },
  },
  variants: {},
  plugins: [],
}
```

paste [this](https://ghostcss.netlify.app/tailwind.css) in `index.css`

*(optional)* paste [this](https://ghostcss.netlify.app/index.js) in `index.js`

```sh
$ npm run dev
```

Now your site is running!

[Docs](https://ghostcss.netlify.app/docs)
