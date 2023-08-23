<script>
import TheHeader from "./components/TheHeader.vue"
import TheFooter from "./components/TheFooter.vue"
import NavBar from "./components/NavBar.vue"
import ComicsContainer from "./components/ComicsContainer.vue"
import productsList from "./db/dc-comics.json"

export default {
  components: {
    TheHeader,
    TheFooter,
    NavBar,
    ComicsContainer
  },
  data() {
    return {
      productsList,
    }
  }
}
</script>

<template>
  <!-- 
    Create un nuovo progetto utilizzando Vite e Vue 3 e 
    definite i componenti necessari per strutturare il layout come da screenshot allegato.
    Quando la struttura a macroblocchi è pronta, popolate le voci di menu dinamicamente usando i data del componente.
    Per oggi diamo priorità alla struttura: quando è tutto bello solido, passiamo al Sass!
    
    Bonus:
    Creare un componente aggiuntivo per gestire la fascia azzurra con le icone.
  -->
  <TheHeader />

  <main>
    <div class="my-hero-section py-5">
      <div class="container">
        <h3>CURRENT SERIES</h3>
      </div>
    </div>
    <ComicsContainer />
    <NavBar />
  </main>

  <TheFooter />
</template>

<style lang="scss">
@use "styles/partials/variables" as *;

main {
  background-color: #1C1C1C;

  .my-hero-section {
    background-image: url(assets/img/jumbotron.jpg);
    background-repeat: no-repeat;
    background-size: cover;
    height: 400px;
    position: relative;

    h3 {
      color: $text-color-secondary;
      position: absolute;
      bottom: -40px;
      background-color: $color-primary;
      padding: 1rem;
      font-weight: bold;
    }
  }
}
</style>
