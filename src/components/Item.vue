<template>
  <div class="card my-2 item-todo">
    <p class="mb-0">{{ tache }}</p>
    <div v-on:click="supr" class="btn-supr btn">X</div>
  </div>
</template>
<script>
export default {
  name: "Item",
  props: ["tache", "supr"]
};
</script>
<style scroped>
.item-todo {
  position: relative;
  padding: 20px 30px;
  font-size: 18px;
  height: 100%;
  color: #747474;
}
.btn-supr {
  position: absolute;
  top: 15px;
  right: 30px;
  border-radius: 50% !important;
  background-color: #F28888 !important;
  border: none !important;
  color: #FFF !important;
}
</style>