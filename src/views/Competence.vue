<template>
  <div class="flex flex-col justify-center static">
    <div class="flex flex-row justify-evenly">
      <button
        v-if="skills"
        @click="displayComp"
        class="bg-yellow-100 p-3 rounded-lg text-4xl font-medium border-4 border-cvLightCyan hover:text-cvBorderorange hover:border-cvBorderorange hover:font-bold"
      >
        Compétences
      </button>
      <button
        v-else
        @click="displayComp"
        class="bg-yellow-100 p-3 rounded-lg text-4xl font-medium border-4 border-cvLightCyan hover:text-cvBorderorange hover:border-cvBorderorange hover:font-bold"
      >
        Soft Skills
      </button>
    </div>
    <div
      v-if="competence"
      class="flex flex-row flex-wrap justify-between items-center mt-4"
    >
      <div v-for="comp in comps" :key="comp.id" class="w-1/3 mt-12">
        <div
          class="flex flex-col items-center m-4 bg-cvLightCyan w-1/2 p-4 rounded-lg mx-auto"
        >
          <h2 class="text-2xl font-medium text-cvSlate">{{ comp.name }}</h2>
          <img :src="comp.icone" alt="icone competence" width="64" height="64" />
          <div class="h-8 w-full mt-2 rounded-2xl bg-gray-100">
            <div
              class="slide-right bg-gradient-to-r from-cvGrad1 to-cvGrad2 h-full font-bold rounded-l-lg rounded-r-2xl flex flex-row justify-center items-center"
              :style="{ width: comp.level + '%' }"
            >
              {{ comp.level }}%
            </div>
          </div>
        </div>
      </div>
    </div>
    <div v-if="skills" class="flex flex-row flex-wrap justify-between items-center mt-4">
      <div v-for="skill in softSkills" :key="skill.id" class="w-1/3 mt-12">
        <div
          class="flex flex-col items-center m-4 bg-cvLightCyan w-1/2 p-4 rounded-lg mx-auto"
        >
          <h2 class="text-2xl font-medium text-cvSlate">{{ skill.name }}</h2>
          <img :src="skill.emot" alt="émoji niveau" width="64" height="64" />
          <div class="h-8 w-full mt-2 rounded-2xl bg-gray-100">
            <div
              class="slide-right bg-gradient-to-r from-cvGrad1 to-cvGrad2 h-full font-bold rounded-l-lg rounded-r-2xl flex flex-row justify-center items-center"
              :style="{ width: skill.level + '%' }"
            >
              {{ skill.level }}%
            </div>
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
      competence: true,
      skills: false,
      comps: [
        {
          id: 0,
          name: "HTML",
          level: 100,
          icone: require("../assets/html5-with-wordmark-color.svg"),
        },
        {
          id: 1,
          name: "CSS",
          level: 100,
          icone: require("../assets/css3-seeklogo.com.svg"),
        },
        {
          id: 2,
          name: "SASS",
          level: 80,
          icone: require("../assets/sass-seeklogo.com.svg"),
        },
        {
          id: 3,
          name: "javaScript",
          level: 90,
          icone: require("../assets/javascript-js-seeklogo.com.svg"),
        },
        {
          id: 4,
          name: "VueJS",
          level: 85,
          icone: require("../assets/vuejs-seeklogo.com.svg"),
        },
        {
          id: 5,
          name: "GitHub",
          level: 80,
          icone: require("../assets/github-seeklogo.com.svg"),
        },
        {
          id: 6,
          name: "Tailwind",
          level: 80,
          icone: require("../assets/tailwindcss-mark.79614a5f61617ba49a0891494521226b.svg"),
        },
        {
          id: 7,
          name: "Prisma",
          level: 65,
          icone: require("../assets/prisma-seeklogo.com.svg"),
        },
        {
          id: 8,
          name: "Supabase",
          level: 50,
          icone: require("../assets/supabase-logo-icon.svg"),
        },
        {
          id: 9,
          name: "C++",
          level: 30,
          icone: require("../assets/c-seeklogo.com.svg"),
        },
        {
          id: 10,
          name: "NuxtJS",
          level: 40,
          icone: require("../assets/nuxt-seeklogo.com.svg"),
        },
        {
          id: 11,
          name: "GitKraken",
          level: 85,
          icone: require("../assets/gitkraken-seeklogo.com.svg"),
        },
      ],
      softSkills: [
        {
          id: 0,
          name: "Prise de décision",
          emot: require("../assets/1F600.svg"),
          level: 90,
        },
        {
          id: 1,
          name: " Communication",
          emot: require("../assets/1F600.svg"),
          level: 90,
        },
        {
          id: 2,
          name: "Esprit Critique",
          emot: require("../assets/1F601.svg"),
          level: 100,
        },
        {
          id: 3,
          name: "Créativité",
          emot: require("../assets/1F630.svg"),
          level: 40,
        },
        {
          id: 4,
          name: "Collaboration",
          emot: require("../assets/1F601.svg"),
          level: 95,
        },
        {
          id: 5,
          name: "Sens du service",
          emot: require("../assets/1F601.svg"),
          level: 100,
        },
        {
          id: 6,
          name: "Intelligence émotionnelle",
          emot: require("../assets/1F601.svg"),
          level: 95,
        },
        {
          id: 7,
          name: "Capacité d'apprentissage",
          emot: require("../assets/1F601.svg"),
          level: 95,
        },
        {
          id: 8,
          name: "Organisation",
          emot: require("../assets/1F600.svg"),
          level: 90,
        },
      ],
    };
  },
  methods: {
    displayComp() {
      this.competence = !this.competence;
      this.skills = !this.skills;
    },
  },
};
</script>

<style>
.slide-right {
  animation: slide-right 2s forwards;
}
@keyframes slide-right {
  0% {
    transform: scaleX(0);
    transform-origin: 0% 0%;
  }
  100% {
    transform: scaleX(1);
    transform-origin: 0% 0%;
  }
}
</style>
