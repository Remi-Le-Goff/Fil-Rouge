#Notice Projet file rouge

##HTML :
Nom de la propiétaire de la page : Affiché en grand, suivi d'un point vert pour accentuer.
Icônes  : Utilise Font Awesome pour ajouter les icônes de Facebook, Instagram, LinkedIn et une icône décorative.
```
# Documentation du Fichier HTML

Ce document HTML présente la structure d'une page web simple pour **Solène Avril**, une photographe d'art, avec un en-tête, une présentation, des catégories de photographie et une galerie d'images. Il utilise Font Awesome pour les icônes et inclut un fichier CSS externe pour les styles.

1. En-tête de la Page

```html
<header>
    <div class="div">
        <p>SOLÈNE AVRIL<span id="vert">.</span></p>
    </div>
    <div class="div1">
        <i class="fa-brands fa-facebook"></i>
        <i class="fa-brands fa-instagram"></i>
        <i class="fa-brands fa-linkedin"></i>
        <i class="fa-solid fa-circle-half-stroke"></i>
    </div>
</header>
```

2. Ligne grise pour séparer l'en-tête du contenu principal, avec une épaisseur de 4 pixels.
```
<hr class="ligne" noshade size="4" width="auto">
```

3. Présentation de Solène Avril.
```
<div class="div2">
    <h1>Hello,<br>Je suis photographe d'art,<br><span id="couleur"> créative et engagée.</span></h1>
</div>
```

4. Texte de description en format paragraphe pour une introduction courte.
```
<div class="div3">
    <h4>Lorem ipsum dolor sit amet consecteur adipiscing elit...</h4>
</div>
```

5. Liste des catégories de photographies disponibles (par exemple, nature, portrait, art).
```
<div class="div4">
    <h3>NATURE</h3>
    <h3 id="portrait">PORTRAIT</h3>
    <h3>ART</h3>
    <h3>URBAIN</h3>
    <h3>ANIMAUX</h3>
</div>
```

6. Grille d'images disposées en 4 colonnes avec des images aléatoires provenant de Picsum.
Les images sont redimensionnées pour conserver un format carré avec un ratio de 1:1.
```
<div class="images">
    <img class="random" src="https://picsum.photos/200/200?random=1" alt="random1" />
    ...
</div>
```

7. Indications de copyright pour Solène Avril et note de projet.
```
<div class="div5">
    <ul>
        <p class="p1">©SOLÈNE AVRIL</p>
        <p class="p2">Exercice HTML - CSS</p>
    </ul>
</div>
```

##CSS :

1. Yeseva One et Montserrat sont définies comme polices principales pour la page.
Fond : La couleur de fond de la page est #041821, avec le texte en blanc.
Texte Gris : La classe .ligne applique une couleur grise #5e5e5e pour certains éléments de texte.
Texte Vert : Les éléments ayant l'ID #vert et la classe .couleur affichent un texte vert #1bd79e.
```
# Documentation du CSS

Ce fichier CSS définit des styles pour une page web incluant des polices personnalisées, une mise en page flexible, et des couleurs spécifiques pour les éléments de texte et de fond.

## Polices Utilisées
```css
@font-face {
    font-family: "Yeseva One", "Montserrat";
    src: url();
    font-weight: normal;
    font-style: normal;
}
```

2. Le header est centré et espacé uniformément avec le texte en blanc sur fond sombre.
```
header {
    background-color: #041821;
    display: flex;
    justify-content: space-between;
    color: white;
}
```

3. .div1 : Utilisé pour aligner les éléments de façon flexible, avec un espace gap de 10px entre eux.
.div2 et .div3 : Ajoutent une marge latérale de 150px pour centrer le contenu dans les écrans plus grands.
.div4 : Centre les éléments et ajoute un gap de 40px pour espacer les éléments.
```
.div1{
    display: flex;
    justify-content: space-around;
    gap: 10px;
    align-items: center
}

.div2{
    margin: 0 150px;
    text-align: left;
}

[...]

.div3{
    margin: 0 150px;
    text-align: left;
}

.div4{
    display: flex;
    justify-content : center;
    gap : 40px;
}
```

5. La grille .images dispose les images en 4 colonnes avec un espacement de 10px. Les images s'ajustent avec un ratio 1:1 et sont centrées.
```
.images {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    gap: 10px;
    max-width: 1200px;
}
.images img {
    width: 100%;
    height: 100%;
    aspect-ratio: 1 / 1;
    object-fit: cover;
}
```

5. #portrait : Fond de couleur verte (#1bd79e).
.div5 : Texte en petite taille (10px) et couleur grise (#5e5e5e).
```
#portrait{
    background-color: #1bd79e;
}
```

Écran > 1024px
Pas de changement, droit hérités
Écran ≤ 1024px
.images passe en 5 colonnes avec des marges réduites à 20px.
.div2 et .div3 passent également à 20px de marge latérale.
Écran ≤ 768px
.images passe en 3 colonnes, avec les marges réduites.
header s'organise en colonne et se centre avec un padding de 10px.
.div1, .div2, et .div3 utilisent des marges latérales de 20px.
.div4 : La taille de police est réduite et l'espacement (gap) est ajusté à 20px.
```
@media (max-width: 1024px) {
    .images {
        grid-template-columns: repeat(5, 1fr);
        gap: 10px;
        margin: 0 20px;
    }
    
    .div2 {
        margin: 0 20px;
    }

    .div3 {
        margin: 0 20px;
    }
}

@media (max-width: 768px) {
    .images {
        grid-template-columns: repeat(3, 1fr);
        margin: 0 20px;
    }

    header {
        flex-direction: column; 
        align-items: center; 
        padding: 10px; 
    }

    .div1 {
        margin-top: 10px; 
    }

    .div2 {
        margin: 0 20px; 
    }

    .div3 {
        margin: 0 20px; 
    }

    .div4 {
        font-size: 9pt;
        gap: 20px;
    }
}
```

##Peu de commit effectué par perte de donné, fichier partiellement retrouvé le 25/10/2024 le matin.
