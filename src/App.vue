<script>
import TheHeader from "./components/TheHeader.vue"
import TheFooter from "./components/TheFooter.vue"
import NavBar from "./components/NavBar.vue"
import ComicsCard from "./components/ComicsCard.vue"
import productsList from "./db/dc-comics"

export default {
  components: {
    TheHeader,
    TheFooter,
    NavBar,
    ComicsCard
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

    <div class="comics-container">
      <div class="container my-5">
        <div class="row gy-4 pt-3">
          <div class="col-2" v-for="(product, i) in productsList" :key="`product_${i}`">
            <ComicsCard :img-src="product.thumb" :series="product.series" />
          </div>
        </div>
      </div>
    </div>

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

    .container {
      h3 {
        color: $text-color-secondary;
        position: absolute;
        bottom: 41%;
        left: 15%;
        background-color: $color-primary;
        padding: 1rem;
        font-weight: bold;
      }
    }

  }
}
</style>
