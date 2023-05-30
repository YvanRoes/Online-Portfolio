<script >
import { RouterLink, RouterView } from 'vue-router'

import Navigation from './components/Navigation.vue'
import FooterBar from './components/Footer.vue'

export default {
  name: "App",
  components: {
    Navigation,
    FooterBar
  }
};
</script>

<template>
  <header>
    <Navigation></Navigation>
  </header>  
  <RouterView />
  <FooterBar></FooterBar>
</template>
<style ></style>
