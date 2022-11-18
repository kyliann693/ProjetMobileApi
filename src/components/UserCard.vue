<template>
  <div id="user__card">
    <p>Produit: {{ name }}</p>
    <input type="checkbox"/>
    <label> Validé</label>
        <!--checkbox produit-->
  </div>
</template>

<script>
export default {
  name: "UserCard.vue",
  props: {
    name: String,
  }
}
</script>

<style scoped lang="scss">
#user__card {
  border: 1px solid black;
  border-radius: 5px;

  p:first-child {
    color: red;
  }
}
</style>