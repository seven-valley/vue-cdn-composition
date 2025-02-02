# Module 04 - Affichage conditionnel : 

la documentation  
https://vuejs.org/guide/essentials/conditional.html  
  
Prise en main de <code>v-if</code> <code>v-else</code>

```html
<div class="alert alert-success" role="alert" v-if="test"> OK</div>
<div class="alert alert-danger" role="alert" v-else>Not OK</div>
```


```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Document</title>
    <link
      href="https://cdn.jsdelivr.net/npm/bootstrap@5.0.2/dist/css/bootstrap.min.css"
      rel="stylesheet"
      integrity="sha384-EVSTQN3/azprG1Anm3QDgpJLIm9Nao0Yz1ztcQTwFspd3yD65VohhpuuCOmLASjC"
      crossorigin="anonymous"
    />
  </head>
  <body>
    <div class="container col-4">
      <div id="app">
        <div class="alert alert-success" role="alert" v-if="test"> OK</div>
        <div class="alert alert-danger" role="alert" v-else>Not OK</div>
        <button @click="changer">GO</button>
      </div>
    </div>
    <script src="https://unpkg.com/vue@3/dist/vue.global.js"></script>
    <script type="module">
      const { createApp, ref } = Vue;
      createApp({
        setup() {
          const test = ref(true);
          const changer = () => {
            test.value=!test.value
                     }
          return {
            changer,
            test
          };
        },
      }).mount("#app");
    </script>
  </body>
</html>
```
