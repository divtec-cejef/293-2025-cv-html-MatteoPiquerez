## A) Dossier CSS : utiliser `css/` (pas `CSS/`)
- Veuillez renommer le dossier `CSS/` en `css/` (minuscules)
- Puis corriger les liens dans le `<head>` :
```
<link rel="stylesheet" href="./css/normalize.css">
<link rel="stylesheet" href="./css/main.css">
```

## B) Lien de la photo : ajouter la sécurité `rel`
- Vous utilisez `target="_blank"` : veuillez ajouter `rel="noopener noreferrer"`
- Exemple :
```
<a href="./img/images.jpg" target="_blank" rel="noopener noreferrer">
  <img src="./img/images.jpg" alt="Image de raton laveur Pablo">
</a>
```

## C) Mettre des guillemets sur les `id`
- Veuillez écrire les `id` avec guillemets (bonne pratique)
- Exemple :
```
<h2 id="experience">Mon expérience</h2>
<h2 id="formation">Ma formation</h2>
```

## D) Corriger la meta author
- Votre meta auteur n’est pas standard
- Exemple attendu :
```
<meta name="author" content="Matteo Piquerez">
```

## Autres
- balise `meta` pour la `description` du site dans le `head`
