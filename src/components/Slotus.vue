  <template>

  <div class="Slotus">

  <slot name="header"></slot>

  <slot name="default">No text</slot>

   <slot name="footer"></slot>

  </div>

  </template>

<script>
export default {
  name: "Slotus"
}
</script>

<style scoped>

.Slotus{
  min-height:100px;
  box-shadow: inset 0 0 1px 1px orange;
  text-align: center;
  padding: 15px;
}

</style>