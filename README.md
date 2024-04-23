# Site web responsive Première partie
Pour créer un site web la première chose qu'on a besoin c'est la page index.html.

![](/images/index.JPG)

Sur cette page index.html, la première chose à faire, à la deuxième ligne, changer "en" en "fr" pour le site en français, à la sixième ligne c'est cette ligne qui permet d'avoir le site responsive, à la septième ligne je vais changer le titre "Document" en "Site web responsive première partie", ensuite il faut intégrer le fichier CSS qu'on a besoin pour le style.
Le fichier CSS n'existe pas encore je dois en créer.

### la page index.html modifié avec style.css intégré.

![](/images/indexModifié.JPG)

fichier style.css.
```
body {
    background-color: lightblue;
}
```
Je vais ouvrir le navigateur pour tester le lien de mon fichier style.css.

![](/images/testestyleCss.JPG)

Mon fichier style.css est bien lié, je peux maintenant continuer à coder.

### Media Queries.
lien du site media queries.

[Media queries](https://developer.mozilla.org/fr/docs/Web/CSS/CSS_media_queries/Using_media_queries#all)

### Type de media queries.
- all
- screen
- print
- speech

Pour tester media queries, d'abord j'ajoute le menu et du texte sur ma page index.html.

![Recette Pizza](/images/recettePizza.JPG)

Je vais tester media queries de type (print), quand l'utilisateur imprime la recette, le header ne doit pas apparaître et la couleur du fond doit être blanche, (Pour imprimer une page par défaut la couleur du fond est blanche).

fichier style.css
```
@media print {
    header {
        display: none;
    }   
}
```
La page à imprimer sans menu et la couleur du fond est blanche, le media de type print fonctionne bien.

![](/images/mediaTypePrint.JPG)

Si maintenant je ne voulais interdire d'imprime la recette.

fichier style.css
```
@media print {
    .no-print {
        display: none;
    }
}
```
Ensuite, créer cette classe (no-print) sur les éléments qu'on voulais interdire d'imprimer, exemple sur élément (body).
![](/images/classeno-print.JPG)





