<template>
  <div class="flex flex-col justify-center h-screen">
    <div class="flex flex-row justify-evenly">
      <button
        @click="displayComp"
        class="bg-yellow-100 p-3 rounded-lg text-4xl font-medium border-4 border-cvLightCyan hover:text-cvBorderorange hover:border-cvBorderorange hover:font-bold"
      >
        Compétences
      </button>
      <button
        @click="displaySkills"
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
  </div>
</template>
<script>
export default {
  data() {
    return {
      competence: false,
      skills: false,
      comps: [
        {
          id: 0,
          name: "HTML",
          level: 100,
          icone: require("../assets/html-5.png"),
        },
        {
          id: 1,
          name: "CSS",
          level: 100,
          icone: require("../assets/css-3.png"),
        },
        {
          id: 2,
          name: "SASS",
          level: 80,
          icone: require("../assets/sass.png"),
        },
        {
          id: 3,
          name: "javaScript",
          level: 90,
          icone: require("../assets/js.png"),
        },
        {
          id: 4,
          name: "Vue.js",
          level: 85,
          icone: require("../assets/logo.png"),
        },
        {
          id: 5,
          name: "Git",
          level: 80,
          icone: require("../assets/git.png"),
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
      ],
    };
  },
  methods: {
    displayComp() {
      this.competence = !this.competence;
    },
    displaySkills() {
      this.skills = !this.displaySkills;
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
