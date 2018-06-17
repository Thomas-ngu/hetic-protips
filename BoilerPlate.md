# Documentation npm/parcel

## Principe
"Le principe d’un boilerplate est donc simple. Il faut concevoir la ou les pages HTML avec le contenu, puis ajouter un certain nombre de « class », de balises, etc… qui appellent soit des feuilles styles, soit des javascripts déjà existants. Avec un peu de pratique et des connaissances en HTML/CSS on arrive vite un résultat très correct."

* terminal:
```
npm init
touch index.html index.js
mkdir styles
touch styles/style.scss

package.json:

{
   "scripts": {
      "start": "parcel index.html",
      "build": "parcel index.js"
   },
   "dependencies": {
      "parcel-bundler": "^1.6.2",
      "node-sass": "^4.7.2"
   }
}
```

* terminal:
```
npm install
npm start

mkdir global && mkdir components && mkdir mixins
touch global/_variables.scss && touch global/_reset.scss
touch mixins/_forsize.scss
touch components/_header.scss
```

## autoprefixer
```
touch .postcssrc

{
  "plugins": {
    "autoprefixer": {
      "browsers": [">1%", "last 4 versions", "Firefox ESR", "not ie < 9"],
      "flexbox": "no-2009",
      "grid": true
    }
  }
}

npm run start
```

##ES6
```
npm install -D babel-preset-env

touch .babelsrc

{
   "presets": [
      ["env",{
         "targets": {
            "browsers": ["last 2 versions", "safari >= 7"]
         }
   }]
}
```
