## Module 10 - les fonctions asynchrones avec Axios

Le cdn d'axios
<img src="../img/m13/Axios.webp" width="100">
  
https://axios-http.com/docs/intro 


```html
<script 
src="https://cdnjs.cloudflare.com/ajax/libs/axios/1.7.7/axios.min.js" 
integrity="sha512-DdX/YwF5e41Ok+AI81HI8f5/5UsoxCVT9GKYZRIzpLxb8Twz4ZwPPX+jQMwMhNQ9b5+zDEefc+dcvQoPWGNZ3g==" 
crossorigin="anonymous" referrerpolicy="no-referrer"></script>
```

# 1 - Présentation des fonctions asynchrone
https://developer.mozilla.org/fr/docs/Web/JavaScript/Reference/Statements/async_function  
  
Avec <code>async</code> et <code>await</code>  
- Une fonction synchrone **async** peut contenir une expression **await** qui interrompt l'exécution de la fonction asynchrone et attend la résolution de la promesse passée Promise.  
La fonction asynchrone reprend ensuite puis renvoie la valeur de résolution.
  
- Le mot-clé **await** est uniquement valide au sein des fonctions asynchrones.  

```js
const go = async ()=>{
    const response = await axios.get("https://swapi.dev/api/people/1");
    console.log(response.data);
}
go();
```

A chaque fois que je crée une fonction avec <code>await</code>, je préfixe la fonction <code>async</code>
```html
<div id="app">
  <button @click="test">go</button>
</div>

<script src="https://unpkg.com/axios/dist/axios.min.js"></script>
<script src="https://unpkg.com/vue@3/dist/vue.global.js"></script>
<script type="module">
  const { createApp, ref } = Vue;
  createApp({
    setup() {
      const test = async () => {
        const response = await axios.get("https://swapi.dev/api/people/1");
        console.log(response.data);
      };
      return {
        test,
      };
    },
  }).mount("#app");
</script>
```