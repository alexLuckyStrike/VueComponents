<template>

<div class="cage">
  <h2>{{state}}</h2>
  <h1>{{counter}}</h1>
  <h3>{{doubleCounter}}</h3>
  <Btn @add-counter="addCounter"/>
    <button @click="plusCounter">Click</button>
</div>

</template>

<script>

import Btn from "./Btn";

export default {

  name: "Cage",
  components: {Btn},

  data(){
    return{
      state:0
    }
  },

  inject:['counter'],

  methods:{

    addCounter(){
      return this.state--
    },

    plusCounter(){
      return this.state++
    }

  },

  watch:{

    state(value){
      console.log('Я слежу за свойством ', value)
    }

  },

  computed:{

    doubleCounter(){

      return this.state*2

    }

  }

}
</script>

<style scoped>

.cage{
  min-height: 100px;
  box-shadow: inset 0 0 1px 1px orange;
  display: flex;
  align-items: center;
  justify-content: center;
}

</style>