<template>
  <div class="border-l-8 border-cvLightCyan w-3/4 mx-auto">
    <div
      v-for="exp in experiences"
      :key="exp.id"
      class="text-cvLightLime flex flex-row relative my-10"
    >
      <div
        class="point bg-cvLightCyan w-8 h-8 rounded-full absolute -left-5 bottom-1/2"
      ></div>
      <div class="border-2 border-cvLightCyan p-7 ml-10 md:mx-auto w-96">
        <div class="flex flex-row items-center">
          <div>
            <img
              :src="exp.image"
              alt="Logo de l'entreprise"
              width="80"
              height="80"
              class="mr-2"
            />
          </div>
          <div>{{ exp.poste }}</div>
        </div>
        <div class="border-t-2 border-cvLightCyan mt-2">
          <div>
            {{ exp.lieu }}
          </div>
          <div>
            {{ exp.date }}
          </div>
        </div>
      </div>
    </div>
    <Footer />
  </div>
</template>
<script>
import Footer from "../components/Footer.vue";
export default {
  data() {
    return {
      experiences: [
        {
          id: "0",
          date: "Août 2021 - Fevrier 2022",
          poste: "Formation de developpeur web",
          lieu: "",
          image: require("../assets/openclassrooms.webp"),
          commentaire: "",
        },
        {
          id: "1",
          date: "Janvier 2021 - Mai 2021",
          poste: "Serveur-Barman",
          lieu: "Le Bar Belge",
          image: require("../assets/logoBarBelge.webp"),
          commentaire: "",
        },
        {
          id: "2",
          date: "Janvier 2015 - Mai 2018",
          poste: "Brancardier",
          lieu: "Hôpital Henri Mondor",
          image: require("../assets/mondor.webp"),
          commentaire: "",
        },
        {
          id: "3",
          date: "Juillet 2013 - Août 2015",
          poste: "Serveur-Barman",
          lieu: "Le Bar Belge",
          image: require("../assets/logoBarBelge.webp"),
          commentaire: "",
        },
        {
          id: "4",
          date: "Août 2009 - Mai 2013",
          poste: "Animateur",
          lieu: "La ligue de l'enseignement",
          image: require("../assets/LOGOFE94-CMJN.webp"),
          commentaire: "",
        },
      ],
    };
  },
  components: { Footer },
};
</script>
