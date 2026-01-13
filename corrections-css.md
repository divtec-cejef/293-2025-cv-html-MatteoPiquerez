## A) `@import` : ligne invalide (il manque le `;`)

À la fin du CSS :
```
@import url(//fonts.googleapis.com/css?family=Open+Sans)
```

À corriger :
```
@import url("[https://fonts.googleapis.com/css?family=Open+Sans](https://fonts.googleapis.com/css?family=Open+Sans)");
```

---

## B) Police : vous mélangez `@import` Google Fonts et `@font-face` (choisir une méthode)

Vous avez :

* `@import` (Google Fonts) pour Open Sans
* `@font-face` mais avec un fichier `myfont.woff2` (non fourni / chemin douteux)

👉 Pour l’exercice, on veut **`@font-face` avec une police locale**.

Option recommandée (conforme consigne) :

* mettre la police dans `./fonts/` (à la racine)
* depuis `css/main.css`, le chemin doit remonter :
```
  @font-face {
  font-family: "MyWebFont";
  src: url("../fonts/myfont.woff2") format("woff2");
  font-weight: 400;
  font-style: normal;
  }

body {
font-family: "MyWebFont", sans-serif;
}
```

💡 *`@font-face` garantit la même police sur tous les PC, même sans Internet.*

> *Chemin important : depuis `css/`, on utilise souvent `../fonts/...`.*

---

## F) Bonus (propreté) : classe `.titre` vide

Vous avez :
```
.titre { }
```

À faire :

* soit supprimer la règle
* soit l’utiliser pour styliser le h1
