<template>
  <div class="hello">
    <h1><a v-bind:href="link">{{msg}}</a></h1>

    <!-- Enviando datos al componente "VerComponente" normal-->
    <VerComponente mensaje-normal="MensajeNormal"></VerComponente>

    <!-- enviando datos al componente "VerComponente" si data es un ARRAY-->
    <VerComponente
    v-for="dato in datos"
    v-bind:key="dato.id"
    v-bind:titulo="dato.titulo"
    v-bind:clase="dato.clase"></VerComponente>
  </div>
</template>

<script>
import VerComponente from "@/components/VerComponente";
export default {
  components:{
    VerComponente
  },
  name: 'HelloWorld',
  props: {
    msg: String,
    link: String,
  },
  data:function () {
    return{
      datos:[
        {id:1, titulo:'TITULO 1', clase:'Entretenimiento'},
        {id:2, titulo:'TITULO 2', clase:'Amor'},
        {id:3, titulo:'TITULO 3', clase:'Ficcion'}
      ]
    }
  }
  }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
