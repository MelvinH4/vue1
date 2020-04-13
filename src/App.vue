<template>
  <div id="app">
      <button @click="MostrarComponent='HelloWorld'">Componente Dinamico 1</button>
      <button @click="MostrarComponent='VerComponente'">Componente Dinamico 2</button>
      <component :is="MostrarComponent"
                 v-bind="persona"
      ></component>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import VerComponente from "@/components/VerComponente";
export default {
  name: 'App',
  components: {
    HelloWorld, VerComponente
  },
    data:function(){
      return{
          MostrarComponent:'HelloWorld',
          persona:[
              {nombre:'Melvin', apellido:'Hernandez', title:'Ing'}
          ],
          switchCase: String

    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
