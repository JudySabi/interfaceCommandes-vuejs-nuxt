<template>
  <div class="card text-white bg-dark mb-3 m-2" style="max-width: 18rem;">
    <div class="card-header">{{ nom }}</div>
    <div class="card-body">
      <p class="card-text">Prix : {{ prix }} €</p>
      <hr />
      <button
        v-if="role === 'commander'"
        @click="$emit('commande', nom, prix)"
        class="btn btn-success"
      >
        Commander !
      </button>
      <button
        v-if="role === 'supprimer'"
        @click="$emit('commande', nom, prix)"
        class="btn btn-dark"
      >
        Supprimer
      </button>
    </div>
  </div>
</template>

<script>
export default {
  name: "Produit",
  props: ["nom", "prix", "role"]
};
</script>

<style scoped>
.card-header {
  font-size: 18px;
}
.btn-success {
  background-color: gold;
  border: none;
  font-weight: 700;
  color: #212529;
}
.btn-dark {
  background-color: #323336;
}
</style>
