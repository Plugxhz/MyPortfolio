<template>
  <main class="min-h-screen p-6 flex flex-col items-center bg-[#F9FAFB]">
    <!-- Cabeçalho -->
    <header class="bg-[#1A2E4A] w-full py-8 text-center shadow-md text-white">
      <h1 class="text-4xl font-bold font-sans">Mais sobre mim</h1>
      <p class="text-xl mt-2 font-light">Minhas habilidades, formação e trajetória</p>
    </header>

    <!-- Sobre mim -->
    <section class="bg-white max-w-5xl mx-4 mt-12 p-8 rounded-lg shadow-lg text-[#1F2937] leading-relaxed">
      <h2 class="text-3xl font-semibold text-[#0f172a] mb-4">Minhas Habilidades</h2>
      <p class="text-lg mb-4">
        Meu nome é Enzo e sou um entusiasta da tecnologia desde 2017. Comecei explorando linguagens de script como Lua, o que me levou a desenvolver interesse por Luau Script, que é uma versão mais avançada de Lua.
      </p>
      <p class="text-lg mb-4">
        Com dedicação e curiosidade, passei a desenvolver projetos a partir de vídeoaulas de programação em Luau Script, os quais me permitiram desenvolver muita maestria com lógica de programação e criar soluções eficientes. Inclusive, esses mesmos projetos já me renderam alguns Euros e Dólares.
      </p>
      <p class="text-lg mb-4">
        Fui longe o suficiente para criar minha própria comunidade online, na qual eu vendia os meus códigos ofuscados para players do Roblox progredirem no jogo de forma ilegal. Talvez para algumas pessoas isso não seja muito ético, mas para mim é um hobby e tanto!
      </p>
    </section>

    <!-- Formação -->
    <section class="bg-[#F1F5F9] w-full max-w-5xl mt-10 p-8 rounded-lg shadow-md">
      <h2 class="text-2xl font-semibold text-[#0f172a] mb-4">Formação Acadêmica</h2>
      <ul class="list-disc list-inside text-lg text-[#1F2937] space-y-2">
        <li>Ensino Médio – Colégio Esmeraldas</li>
        <li>Curso de Análise e Desenvolvimento de Sistemas – UNIMAR</li>
      </ul>
    </section>

    <!-- Trajetória e experiências -->
    <section class="bg-white w-full max-w-5xl mt-10 p-8 rounded-lg shadow-md">
      <h2 class="text-2xl font-semibold text-[#0f172a] mb-4">Trajetória e Projetos</h2>
      <p class="text-lg text-[#1F2937] mb-4">
        Tenho trabalhado em projetos independentes desde que me senti capaz o suficiente para desenvolver interfaces interativas com Luau Script, criar bancos de dados com MySQL e MySQL Workbench, e por fim criar APIs com C#. Também exploro o desenvolvimento frontend com Vue.js, Vite e TailwindCSS.
      </p>
      <p class="text-lg text-[#1F2937]">
        Minha trajetória é marcada por constante evolução, muito tempo em frente ao computador, muito tempo dentro do quarto e a minha busca incansável por me tornar um desenvolvedor profissional.
      </p>

      <div class="flex justify-center mt-6">
        <button @click="showTimeline = !showTimeline"
                class="bg-[#2563EB] hover:bg-[#1D4ED8] text-white py-2 px-6 rounded-full font-medium transition duration-300">
          {{ showTimeline ? 'Esconder timeline' : 'Ver minha timeline' }}
        </button>
      </div>

      <!-- Timeline animada -->
      <transition name="fade">
        <section v-if="showTimeline" class="bg-[#F1F5F9] w-full mt-10 p-8 rounded-lg shadow-md">
          <h2 class="text-2xl font-semibold text-[#0f172a] mb-6">Minha Timeline</h2>
          <ol class="relative border-s border-gray-300 ml-4">
            <li v-for="item in timeline" :key="item.id" class="mb-10 ms-6">
              <span class="absolute flex items-center justify-center w-4 h-4 bg-teal-500 rounded-full -start-2 ring-2 ring-white"></span>
              <time class="mb-1 text-sm font-normal leading-none text-gray-500">{{ item.year }}</time>
              <h3 class="text-lg font-semibold text-gray-900">{{ item.title }}</h3>
              <p class="text-base font-normal text-gray-700">{{ item.description }}</p>
            </li>
          </ol>
        </section>
      </transition>
    </section>
  </main>
</template>

<script setup>
import { ref } from 'vue'

const showTimeline = ref(false)

const timeline = [
  {
    id: 1,
    year: '2017',
    title: 'Início no mundo da programação',
    description: 'Primeiros contatos com Lua e lógica de scripts.'
  },
  {
    id: 2,
    year: '2020–atual',
    title: 'Projetos com Luau Script',
    description: 'Desenvolvimento de scripts comerciais e início da comunidade online.'
  },
  {
    id: 3,
    year: '2023',
    title: 'Formação Técnica',
    description: 'Finalização do Ensino Médio no Colégio Esmeraldas.'
  },
  {
    id: 4,
    year: '2024–atual',
    title: 'Curso Superior',
    description: 'Análise e Desenvolvimento de Sistemas na UNIMAR.'
  },
  {
    id: 5,
    year: '2025–futuro',
    title: 'Desenvolvedor Profissional',
    description: 'Foco em me tornar um desenvolvedor fullstack.'
  }
]
</script>

<style scoped>
.fade-enter-active, .fade-leave-active {
  transition: opacity 0.5s;
}
.fade-enter-from, .fade-leave-to {
  opacity: 0;
}
</style>