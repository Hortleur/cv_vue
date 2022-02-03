<template>
  <div
    class="flex flex-col justify-between bg-gradient-to-br from-cvGreen to-cvBlueSlate h-full"
  >
    <div id="nav" class="p-5 text-cvLightLime font-bold text-lg">
      <router-link to="/">Accueil</router-link> |
      <router-link to="/skills">Competences</router-link> |
      <router-link to="/exp">Experiences</router-link>
    </div>
    <router-view />
  </div>
</template>

<script>
export default {
  components: {},
};
</script>

<style>
#app {
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #e19d56;
}
</style>
