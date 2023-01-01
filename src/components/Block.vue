<template>

  <div class = "Block">
    <h1> {{title}} </h1>
    <h2> {{state}} </h2>
  </div>

</template>

<script>


export default {
  components: {},
  props:['state'],
  name: "block",
  data(){
    return{
      title:'My first App'
    }
  }



}
</script>

<style scoped>

.Block{
  min-height: 100px;
  width: 100%;
  box-shadow: inset 0 0 2px 2px red;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}

</style>