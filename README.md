# Site web responsive Première partie
Pour créer un site web la première chose qu'on a besoin c'est la page index.html.

![](/images/index.JPG)

Sur cette page index.html, la première chose à faire, à la deuxième ligne, changer "en" en "fr" pour le site en français, à la sixième ligne c'est cette ligne qui permet d'avoir le site responsive, à la septième ligne je vais changer le titre "Document" en "Site web responsive première partie", ensuite il faut intégrer le fichier style.css qu'on a besoin pour le style.
Le fichier style.css n'existe pas encore je dois en créer.

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
lien du site média queries.

[Media queries](https://developer.mozilla.org/fr/docs/Web/CSS/CSS_media_queries/Using_media_queries#all)

### Type de média queries.
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
La page à imprimer est sans menu et la couleur du fond est blanche, le média queries de type print fonctionne bien.

![](/images/mediaTypePrint.JPG)

Si maintenant je voulais interdire d'imprimer la recette.

fichier style.css
```
@media print {
    .no-print {
        display: none;
    }
}
```
Cette classe (no-print) il faut en créer et appliquer cette dernière (no-print) sur les éléments qu'on voulais interdire d'imprimer, exemple sur élément (header).

fichier index.html
![](/images/classeno-print.JPG)

Maintenant la classe (no-print) est fonctionnelle, ensuite, exemple de média queries de type (all) sur le footer.

fichier style.css
```
@media all {
    .footer{
        border: solid 5px red; 
    }
}
```
fichier index.html
![](/images/footerBorder.JPG)

J'actualise la page index.html.

![](/images/indexFooterBorder.JPG)

J'ai maintenant la bordure rouge sur mon footer, je vais essayer de l'imprimer, mon footer est caché grâce à la classe (no-print).

![](/images/mediaClasseNoprint.JPG)

Si j'enlève la classe (no-print) sur mon footer et essayer de l'imprimer.

![](/images/modifClasseFooter.JPG)

J'assaie de l'imprimer, j'ai mon footer avec la bordure rouge.

![](/images/footerimprimeBordure.JPG)

Si je remplace le type (all) en (screen) de média queries et j'assie de l'iprimer.

fichier style.css

```
@media screen {
    .footer {
        bordure: solid 5px red;
    }
}
```
J'ai cette fois-ci, le footer sans bordure rouge.

![](/images/footerSansBordure.JPG)

### Les caractéristiques de média (*Media feature*).
Les caractéristiques média décrivent certaines caractéristiques spécifiques de l'agent utilisateur, de l'appareil d'affichage ou de l'environnement. Les expressions de caractéristique média testent leur présence ou leur valeur. Chaque expression de caractéristique doit être entourée de parenthèses.

(*Je vais citer quelques uns pour ces exemples*).
- width
- height
- max-width
- min-width
- orientation

Un exemple sur (width) d'élément (body).

fichier style.css
```
@media (width: 1200px) {
    background-color: yellow;
} 
```

