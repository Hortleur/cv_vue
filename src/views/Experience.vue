<template>
  <div class="border-l-8 border-cvLightCyan w-3/4 mx-auto">
    <div
      v-for="exp in experiences"
      :key="exp.id"
      class="text-cvLightLime flex flex-row relative my-10"
    >
      <div class="bg-cvLightCyan w-8 h-8 rounded-full absolute -left-5"></div>
      <div class="border-2 border-cvLightCyan mx-auto p-7">
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
        <div class="border-t-2 border-cvLightCyan">
          <div>
            {{ exp.lieu }}
          </div>
          <div>
            {{ exp.date }}
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      experiences: [
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
          poste: "Serveur-Barman",
          lieu: "Le Bar Belge",
          image: require("../assets/LOGOFE94-CMJN.webp"),
          commentaire: "",
        },
      ],
    };
  },
};
</script>
