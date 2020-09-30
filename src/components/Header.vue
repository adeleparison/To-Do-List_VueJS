<template>
  <div class="header-top">
    <h1 class="title-to-do-list">{{ title }}</h1>
    <p class="intro-to-do-list">{{ intro }}</p>
  </div>
</template>

<script>
export default {
  name: "Header",
  data() {
    return {
      title: "La To-do Liste",
      intro: "#Les choses à ne pas oublier"
    };
  }
};
</script>

<style>
.header-top {
  text-align: center;
  background-color: #026873;
  color: #fff;
  height: 100%;
  margin-bottom: 50px;
}
.title-to-do-list {
  padding: 30px 0 0;
}
.intro-to-do-list {
  padding: 0 0 30px;
  font-style: italic;
}
</style>
