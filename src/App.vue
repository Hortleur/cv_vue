<template>
<div class=" h-screen flex flex-col justify-between bg-gradient-to-br from-cvGreen to-cvBlueSlate">
  <div id="nav" class=" p-5 text-cvLightLime font-bold text-lg">
    <router-link to="/">Accueil</router-link> |
    <router-link to="/skills">Competences</router-link> |
    <router-link to="/exp">Experiences</router-link>
  </div>
  <router-view/>
  <Footer>
    <FooterVue />
  </Footer>
</div>
  
</template>

<script>
import FooterVue from "./components/Footer.vue";
export default {
  components:{
    FooterVue,
  }
}
</script>

<style>
#app {
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #E19D56;
}
</style>
