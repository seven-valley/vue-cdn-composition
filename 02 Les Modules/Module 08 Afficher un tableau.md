# Module 8 - Afficher un tableau
la documentation :
https://vuejs.org/guide/essentials/list.html

## Afficher un tableau simple
```js
setup() {
    const voyages = ref(['Aller à Rome', 'Aller à Paris','Aller à Londres'])
    return {voyages};
}
```

```html
<div id="app">
    <li v-for="voyage in voyages">
        {{ voyage }}
    </li>
</div>
```


## Afficher un tableau avec les index
```js
setup() {
    const voyages = ref(['Aller à Rome', 'Aller à Paris','Aller à Londres'])
    return {voyages}
}
```

```html
<li v-for="(voyage,i) in voyages">
    {{ i }} {{ voyage }}
</li>
```


## Afficher un tableau d'objets
```js
setup() {
    const consoles = ref([
        { id: 1, name: "Playstation 5" },
        { id: 2, name: "Xbox Series X" },
        { id: 3, name: "Nintendo Switch" },
    ]);
return {consoles}
}
```

```html
<li v-for="(console,i) in consoles" key="console.id">
    {{ i }} / {{ console.id }} / {{ console }}
</li>
```