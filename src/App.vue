<script>
import TheHeader from "./components/TheHeader.vue"
import TheFooter from "./components/TheFooter.vue"
import NavBar from "./components/NavBar.vue"

export default {
  components: {
    TheHeader,
    TheFooter,
    NavBar
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
        <h2>--&gt;Content goes here&lt;--</h2>
      </div>
    </div>
    <NavBar />
  </main>

  <TheFooter />
</template>

<style lang="scss">
@use "styles/partials/variables" as *;

.my-hero-section {
  background-color: #000;
  color: $text-color-secondary;
}
</style>
