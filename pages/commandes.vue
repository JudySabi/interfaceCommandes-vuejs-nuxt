<template>
  <div>
    <h1 class="display-1">Commander</h1>
    <h2>Produits disponible</h2>

    <div class="card-group">
      <Produit
        v-for="produit in produits"
        :key="produit.nom"
        v-bind:nom="produit.nom"
        v-bind:prix="produit.prix"
        v-on:commande="ajouterProduit"
        role="commander"
      />
    </div>

    <h2>Produits commandés</h2>
    <div class="card-group">
      <Produit
        v-for="produit in commandes"
        :key="produit.nom"
        v-bind:nom="produit.nom"
        v-bind:prix="produit.prix"
        v-on:commande="supprimerProduit"
        role="supprimer"
      />
    </div>
  </div>
</template>

<script>
import Produit from "@/components/Produit.vue";
import Vue from "Vue";

export default {
  components: {
    Produit
  },
  data() {
    return {
      produits: [
        { nom: "Pizza", prix: 3.0 },
        { nom: "Frites", prix: 2.0 },
        { nom: "Hamburger", prix: 2.5 },
        { nom: "Cheesburger", prix: 3.5 }
      ],
      commandes: []
    };
  },
  methods: {
    ajouterProduit(nom, prix) {
      this.commandes.push({ nom: nom, prix: prix });
    },
    supprimerProduit(nom) {
      this.$delete(this.commandes, nom);
    }
  }
};
</script>

<style scoped></style>
