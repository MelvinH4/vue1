<template>
  <div class="hello">
    <ul>
      <li> <span>DINNER----></span>{{TotalDinner}}<button @click="IncreaseDinner">+</button>
           <button @click="DecreaseDinner">-</button></li>
    </ul>
    <ul>
      <li> <span>TIP--></span>{{TotalTip}}<button @click="IncreaseTip">+</button>
           <button @click="DecreaseTip">-</button></li>
    </ul>
    <ul>
      <li> <span>TOTAL COMPRA</span>{{total}}</li>
    </ul>
  </div>
</template>

<script>
//I will not use this component for this example exercise
import VerComponente from "@/components/VerComponente";
export default {
  name: 'HelloWorld',
  component:{
    VerComponente
  },
  data: function (){
    return{
      TotalDinner:"",
      TotalTip:0
    }
  },
  computed:{
    total(){
       return this.TotalDinner+this.TotalTip
    }
  },
  methods:{
    IncreaseDinner(){
      this.TotalDinner++;
    },
    DecreaseDinner(){
      this.TotalDinner--;
    },
    IncreaseTip(){
      this.TotalTip++;
    },
    DecreaseTip(){
      this.TotalTip--;
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
