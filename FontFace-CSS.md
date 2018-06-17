#Documentation CSS

* La syntaxe CSS

HTML5 est venu avec une bonne et une mauvaise nouvelle. La bonne nouvelle, c'est qu'il est désormais possible d'utiliser n'importe quel caractère dans les identifieurs des attributs class et id. Et la mauvaise nouvelle, c'est que… pas en CSS. Un auteur Belge a dressé la liste des caractères qui ont un sens spécial en CSS et qu'il faut donc échapper caractères spéciaux.

Il reste alors deux caractères de séparation : le trait d'union qu'une règle spéciale permet d'utiliser dans un identifieur sauf en première position, et le underscore.

Toujours donner un nom/une signification à la classe donnée pour se retrouver dans le code. Ex : Cette div est un container qui regroupe plusieurs blocs. Elle fait partie d'une catégorie nommée "Projets". La classe du container s'appelera :

```html
<div class="Projects-container">
    <div></div>
    <div></div>
    <div></div>
</div>
```

## Responsive :

* html:

```html
<head>
   <meta name="viewport" content="width=device-width, initial-scale=1"/>
</head>

Keyframes animation :

.blinking {
   color: #93B7BE;
   -webkit-animation: blinkAnimation 1s infinite;
}

@-webkit-keyframes blinkAnimation {
   0% {
      color: #93B7BE;
   }
   50% {
      color: #000;
   }
   100% {
      color: #93B7BE;
   }
}
```

### Font-face

Les font-face permettent de fournir les fonts du site.

* css :

```css
@font-face {
   font-family: "Open Sans Regular";
   src: url("../fonts/OpenSans-Regular.ttf");
}

.message {
   font-family: "Open Sans";
}

Media-queries

.class {
  background:red;
}

@media (min-width: 768px) {
  .class{
    background:blue;
  }
}

@media (min-width: 1024px) {
  .class{
    background:yellow;
  }
}
```

### Font-face, @import

```css
@font-face {
    font-family: myFirstFont;
    src: url(sansation_light.woff);
}

A mettre au tout début du fichier css.

@import url('')
```
