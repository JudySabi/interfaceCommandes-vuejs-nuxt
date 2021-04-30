<template>
  <div>
    <nav class="navbar navbar-expand-lg navbar-dark bg-dark mb-4">
      <div class="container-fluid container">
        <nuxt-link class="nav-link" to="/">InterfaceCommande</nuxt-link>
        <button
          class="navbar-toggler"
          type="button"
          data-bs-toggle="collapse"
          data-bs-target="#navbarNavDropdown"
          aria-controls="navbarNavDropdown"
          aria-expanded="false"
          aria-label="Toggle navigation"
        >
          <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="navbarNavDropdown">
          <ul class="navbar-nav">
            <li class="nav-item">
              <nuxt-link class="nav-link" to="/">Accueil</nuxt-link>
            </li>
            <li class="nav-item">
              <nuxt-link class="nav-link" to="/commandes">Commandes</nuxt-link>
            </li>
          </ul>
        </div>
      </div>
    </nav>

    <div class="container">
      <Nuxt />
    </div>
  </div>
</template>

<style>
.nav-link {
  color: gold;
}
</style>
