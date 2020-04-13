<template>
  <div class="hello">
      <p>{{nombre}} {{apellido}}</p>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: ['nombre','apellido'],

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
