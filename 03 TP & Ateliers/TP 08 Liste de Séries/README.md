# TP 07 Mes Séries préférées

<img src="../../img/tp/tp7.webp" width="400">

- Créer 2 tableaux d'objets séries
```js
const series =ref([])
const tabFav =ref([])
```

- Récupérer un tableau de séries
avec **s=** pour récupérer un tableau
```
http://www.omdbapi.com/?apikey=xxxx&s=star
```
- Ajouter une séries
- Créer une fonction asynchrone 
pour récupéré la note imdb (serie.imdbRating) avec l'id du film(serie.imdbID)
i=serie.imdbID
```
http://www.omdbapi.com/?apikey=xxxx&i=star
```
- Quand on ajoute la série elle s'enlève de la liste de recherche
- Enlever la série de la liste de favories
- Utiliser local storage
