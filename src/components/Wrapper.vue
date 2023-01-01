  <template>
  <div class="wrapper">
  <Block state="Молодец, запомнил"/>
  <Cage/>

    <Slotus>
      <p>Это самый важный текст для нового блока</p>

      <template v-slot:footer>
        <small>Это footer</small>
      </template>

      <template v-slot:header>
      <h3>Это заголовок</h3>
      </template>

    </Slotus>

  </div>
  </template>

<script>

import Block from "./Block";
import Cage from "./Cage";
import Slotus from "./Slotus";

export default {
  name: "wrapper",
  components: {Slotus, Block,Cage},
  provide:{
    counter:'Разделение'
  }
}
</script>

<style scoped>

.wrapper{
  width: 600px;
  min-height: 200px;
  box-shadow: inset 0 0 2px 2px black;
  margin:auto;
}

</style>