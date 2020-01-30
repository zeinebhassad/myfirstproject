<template>
     <div class="root">
      <h1>Exemple de composant</h1>
      <p>
        <my-field value="je suis un champ texte" v-on:change="doSomething" />
      </p>
      <p>
        Valeur entrée par l’utilisateur : {{ userValue }}
      </p>
    </div>
</template>
<script>
    new Vue({
    render: h => h(App),
    }).$mount('#app')
    export default {
    data () {
        return {
        userValue: null
        }
    },
    components: {
        myField
    },
    methods: {
    doSomething(value) {
        console.log(value)
    }
    }
}
</script>
 <style>
      .root {
  padding: 20px
    }
    </style>