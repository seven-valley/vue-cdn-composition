# Module 03 - Liaison par attribut : attribut binding

La documentation :  
https://vuejs.org/guide/essentials/class-and-style.html


## associer une reference à une classe
<code>:class</code> permet de relier un attribut a une reference

```html
 <div class="alert" :class="classe" role="alert">information</div>
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
        <div class="alert" :class="classe" role="alert">information</div>
        <button @click="changer">GO</button>
      </div>
    </div>
    <script src="https://unpkg.com/vue@3/dist/vue.global.js"></script>
    <script type="module">
      const { createApp, ref } = Vue;
      createApp({
        setup() {
          const test = ref(true);
          const classe = ref("alert-success");
          const changer = () => {
            test.value=!test.value
            if (test.value) {
              classe.value = "alert-success";
            } else {
              classe.value = "alert-danger";
            }
          };
          return {
            classe,
            changer,
          };
        },
      }).mount("#app");
    </script>
  </body>
</html>
```


## Utilisation des ternaire

```html
 <div class="alert" :class="test ? 'alert-success' : 'alert-danger'" role="alert">information</div>
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
        <div class="alert" :class="test ? 'alert-success' : 'alert-danger'" role="alert">information</div>
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
            test,
            changer
          };
        },
      }).mount("#app");
    </script>
  </body>
</html>
```

