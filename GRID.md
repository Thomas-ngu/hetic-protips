# CSS Grid

## Principe
Le module CSS Grid layout (modèle de disposition en grille) est un module de la spécification CSS qui permet de créer des mises en page en divisant l'espace d'affichage en régions utilisables par une application ou en définissant des relations de taille, position et d'empilement entre les éléments HTML.

Comme les tableaux, la grille permet d'aligner des éléments sous forme de colonnes et de lignes mais à la différence des tableaux, la grille n'a pas de structure de contenu. Ainsi, on peut créer de nombreuses mises en page qui n'auraient pas été possibles avec les tableaux. Ainsi, les éléments fils d'un conteneur en grille peuvent être positionnés afin qu'ils se chevauchent ou qu'ils se comportent comme des éléments positionnés.

* html
```html
<div class="wrapper">
  <div class="one">Un</div>
  <div class="two">Deux</div>
  <div class="three">Trois</div>
  <div class="four">Quatre</div>
  <div class="five">Cinq</div>
  <div class="six">Six</div>
</div>
```

* css
```css
.wrapper {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  grid-gap: 10px;
  grid-auto-rows: minmax(100px, auto);
}
.one {
  grid-column: 1 / 3;
  grid-row: 1;
}
.two {
  grid-column: 2 / 4;
  grid-row: 1 / 3;
}
.three {
  grid-column: 1;
  grid-row: 2 / 5;
}
.four {
  grid-column: 3;
  grid-row: 3;
}
.five {
  grid-column: 2;
  grid-row: 4;
}
.six {
  grid-column: 3;
  grid-row: 4;
}
```

* Flexbox :

```css
.container {
  display: flex; /* or inline-flex */
  flex-direction: row | row-reverse | column | column-reverse;
  /* row:left to right | row-reverse:right to left | column: top to bottom | column-reverse: bottom to top */
  flex-wrap: nowrap | wrap | wrap-reverse;
  /* nowrap: inline | wrap: les items passent chacun en dessous en responsive | wrap-reverse: l'inverse de wrap */
  justify-content: flex-start | flex-end | center | space-between | space-around;
  align-items: flex-start | flex-end | center | baseline | stretch;
  align-content: flex-start | flex-end | center | space-between | space-around | stretch;
}
```

* FlexBox Grid

```html
<div class="container-fluid">
    <div class="row between-xs">
        <div class="col-xs-6 col-lg-4">
                <h1>Hey Wassup</h1>
                <p>Excepteur minim amet ea elit mollit labore commodo aliquip dolore velit enim elit mollit deserunt.</p>
        </div>
        <div class="col-xs-6 col-lg-4">
                <h1>Je suis la frr</h1>
                <p>Ut eu irure ad irure nostrud excepteur irure eiusmod enim mollit adipisicing. Ea occaecat est consectetur enim amet non culpa.</p>
        </div>
        <div class="col-xs-6 col-lg-4">
                <h1>Lol wsh</h1>
                <p>Sit commodo proident do irure sit elit aliqua veniam mollit. Sunt amet nostrud velit ut occaecat. Mollit nulla enim incididunt incididunt ut consequat Lorem do laborum et velit non ut elit. Commodo aliquip cupidatat eu deserunt quis sunt.
                    Sit irure est elit ipsum velit aliqua duis labore adipisicing culpa ea sunt qui nisi. Dolor eu duis tempor veniam qui exercitation et cupidatat. Minim incididunt non nisi ad amet veniam eiusmod duis exercitation nostrud ex.</p>
        </div>
        <div class="col-xs-6 col-lg-6">
                <h1>yey</h1>
                <p>Cillum reprehenderit sunt ad anim ea. Ex anim mollit do consectetur reprehenderit quis deserunt. Duis esse dolore quis sit tempor laborum voluptate elit do laborum. Sint sunt sit consectetur incididunt Lorem esse ex est enim. Cupidatat
                    id sunt do labore Lorem esse esse quis culpa.</p>
        </div>
        <div class="col-xs-12 col-lg-5 col-lg-offset-1">
                <h1>yesyeyseyesysy</h1>
                <p>Sint incididunt labore amet laborum mollit commodo           voluptate enim aute ut tempor voluptate aute                 exercitation. Ad dolore labore Lorem id duis. Ipsum          veniam ea aliquip reprehenderit commodo occaecat id          reprehenderit sit fugiat eu sunt. Autecillum
                   consectetur ea in ex. Do ullamco nisi pariatur consequat. Esse enim officia minim elit ad elit. Officia magna aliqua ipsum pariatur dolore est.
                </p>
        </div>
    </div>
</div>
```
