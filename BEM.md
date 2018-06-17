# Documentation

# Convention BEM

* B -> Block
* E -> Element
* M -> Modifier


```html
<ul class="headerNav mainList--xmas">
    <li class="mainList__item">
      <a href="/Home" class="mainList__itemLink mainList__itemLink--isActive">Home</a>
    </li>
    <li class="mainList__item">
      <a href="/About" class="mainList__itemLink">About</a>
    </li>
    <li class="mainList__item">
      <a href="/Works" class="mainList__itemLink">Works</a>
    </li>
  </ul>
```

```css
.mainList {
  display: flex;
  justify-content: space-between;
  &--xmas {
    background: green;
  }
  &__item {
    list-style: none;
  }
  &__itemLink {
    color: red;
    &--isActive {
      color: white;
    }
  }
}

```

Exemple en CSS du rendu :
```css
.mainList {

}
.mainList--xmas {

}
.mainList__item {

}
.mainList__itemLink {

}
.mainList__itemLink--isActive {

}
```
## Pseudo attributs

Les pseudos attributs 'before' et 'after' permettent de créer des noeurs HTML en CSS.
Ils sont essentiellement utilisés pour ajouter des ornements, des décorations ... On peut bien entendu faire des animations avec, les positionner par rapport à leur parent (relative / absolute). **Ils doivent obligatoirement avoir un 'content: ''`** afin de s'aficher.

## Centrer en 3 lignes de CSS (verticalement)

```HTML
<section class='cover'>
  <h1 class="cover__mainTitle">Présentation des pseudo-attributs</h1>
</section>
```

```CSS
.cover {
  background: #FDFDFD;
  padding: 20px;
  &__mainTitle {
    text-align: center;
    font-size: 24px;
    color: green;
    &::before,
    &::after {
      position: absolute;
      content:'';
      display: block;
      width: 50px;
      height: 50px;
      background: green;
    }
    &::before {
      left: 0;
    }
&::after {
  right: 0;
  }
  }
}
```

## REM, EM , %, VW Sizing



### %

### EM
$ Relative à la taille de son parent direct.
```css
.cover {
  font-size: 100%;
  &__mainTitle {
    font-size: .8em;
  }
}
```

### REM

* le REM est basé sur la taille de la racine (soit la balise <html>) qui, par défaut a une valeur de 16px. Afin d'éviter tout calcul, il est nécessaire de l'écraser en donnant une base de 10px doit 62,5%.
* Le REM est intéressant à utiliser si les media-queries employées sont en rem également. cela vous permettra de garder des proportions égales lorsqu'on va redimensionner la page.
* Ses proportions seront également gardées quand l'utilisateur zoomera dans votre page.

```css
html {
  font-size: 62,5%;
}
.__mainTitle {
  font-size: 1.6rem;
  width: 32em;
}
```

### VW(idth) / VH(eight)

  * Unités relatives à la taille de votre écran (peu importe le device)
  * Attention au VH et à son contenu. 100vh === 100vh quoi qu'il arrive.
  * VW : très utile oour les interfaces fluides.

## Liens utiles

* CanIUse
