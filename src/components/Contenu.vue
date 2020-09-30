<template>
  <div class="container">
    <form class="mb-5">
      <div class="form-group">
        <div class="input-group">
          <input
            v-model="formData.tache"
            type="text"
            id="action"
            class="form-control"
            placeholder="Ma tâche ..."
            aria-label="Ma tâche ..."
            aria-describedby="button-action"
          />
          <div class="input-group-append">
            <button
              v-on:click.prevent="creationItem"
              class="btn btn-outline-secondary"
              type="button"
              id="button-action"
            >Créer une tâche</button>
          </div>
        </div>
      </div>
    </form>

    <ul>
      <li :key="index" v-for="(tache, index) in tableauTaches">
        <item v-bind:id="index" :tache="tache" :supr="supr"></item>
      </li>
    </ul>
  </div>
</template>

<script>
import Item from "./Item.vue";
export default {
  name: "Contenu",
  components: {
    item: Item
  },
  data() {
    return {
      formData: {
        tache: ""
      },
      tableauTaches: [
        "Faire le ménage",
        "Appeler Jean",
        "Acheter robe de cocktail"
      ]
    };
  },
  methods: {
    creationItem: function() {
      this.tableauTaches.push(this.formData.tache);
      this.formData.tache = "";
    },
    supr: function(e) {
      this.tableauTaches.splice(e.target.parentNode.id, 1);
    }
  }
};
</script>

<style>
.btn-outline-secondary {
  background-color: #038c8c !important;
  border: none !important;
  color: #fff !important;
}
ul {
  list-style-type: none;
  padding: 0;
}
</style>
