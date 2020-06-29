
<template>
  <div class="hello">
<ul>
  <li>
    <span>Dinner---></span>{{TotalDinner}}<button @click="IncreaseDinner">+</button>
    <button @click="DecreaseDinner">-</button>
  </li>
  <li>
      <span>Tip-></span>   {{TotalTip}}  <button @click="IncreaseTip">+</button>
    <button @click="DecreaseTip">-</button>
  </li>
  <li>
    <span>TOTAL</span>   {{total}}
  </li>
</ul>
    <VerComponente></VerComponente>
  </div>
</template>

<script>
//I will not use this component for this reactivity example
import VerComponente from "@/components/VerComponente"
export default {
  name: 'HelloWorld',
  components:{
    VerComponente
  },
  data:function (){
    return {
      TotalDinner: "",
      TotalTip: 0,
    }
  },
  computed:{
    total(){
      return this.TotalDinner + this.TotalTip;
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


<style scoped>

</style>
