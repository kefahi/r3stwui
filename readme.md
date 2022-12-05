# Setting up Routify3 with STWUI

## 1. Install routify3

```bash
npx @roxi/routify@next create myr3app
cd myr3app
npm install
```

## 2. Enable Typescript 

```bash
npm i svelte-preprocess
mv src/main.js src/main.ts
sed -i 's/main.js/main.ts' index.html

```

Update `vite.config.js`
```javascript
import preprocess from 'svelte-preprocess'
...
preprocess: [
  preprocess(), 
  mdsvex({ extension: 'md' })
  ],
...
```

## 3. Install Tailwind

```bash
npx svelte-add@latest tailwindcss
npm install -D @tailwindcss/forms
yarn install
npm i -D stwui
```

In `index.html` comment out the line that loads milligram.css (which conflicts with TailwindCSS)  

