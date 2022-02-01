<template>
  <div class="flex flex-col h-screen">
    <div class="flex flex-col justify-around my-auto lg:flex-row xl:flex-row">
      <div class="home flex-grow">
        <img
          alt="photo de profil"
          :src="image"
          class="rounded-full mx-auto ring-4 ring-offset-cvLightCyan ring-offset-4 ring-cvLightCyan"
        />
        <h1 class="font-bold text-5xl mt-8 text-cvLightCyan">Kevin Brun</h1>
        <h2 class="font-bold text-4xl text-cvLightCyan">{{ getAge }} ans</h2>
      </div>
      <div class="flex-1 lg:mr-12">
        <div>
          <h2 class="text-4xl text-cvLightLime mt-5">Présentation</h2>
          <div class="text-cvLightLime my-4">
            <p>
              Après avoir travaillé dans l'animation, puis dans la restauration en passant
              par le milieu hospitalier, à presque 30 ans, je me lance dans cette nouvelle
              aventure qu'est le monde du developpement web, un domaine qui m'a toujours
              attiré.
            </p>
          </div>
        </div>
        <div class="text-cvLightLime mt-12">
          <h2 class="text-4xl text-cvLightLime mt-5">Hobbies</h2>
          <ul>
            <li v-for="hobbie in hobbies" :key="hobbie.item">{{ hobbie.item }}</li>
          </ul>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Home",
  data() {
    return {
      hobbies: [{ item: "Musique" }, { item: "Jeux Vidéo" }, { item: "Lecture" }],
      image: require("../assets/profil.webp"),
    };
  },
  computed: {
    getAge: function () {
      let currentDate = new Date();
      let DDN = new Date("1992/03/13");
      let diff = currentDate - DDN;
      let age = Math.floor(diff / 31557600000);
      return age;
    },
  },
  components: {},
};
</script>
