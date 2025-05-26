<template>
  <main class="min-h-screen p-6 flex flex-col justify-center items-center bg-[#F9FAFB]">
    <!-- Cabeçalho -->
    <header class="bg-[#1A2E4A] w-full py-8 text-center shadow-md text-white">
      <h1 class="text-4xl font-bold font-sans">Olá, eu me chamo Enzo</h1>
      <p class="text-xl mt-2 font-light">Futuro Desenvolvedor Full Stack</p>
    </header>

    <!-- Apresentação -->
    <section class="bg-white max-w-4xl mx-4 mt-12 p-6 rounded-lg shadow-lg text-[#1F2937]">
      <h2 class="text-4xl font-semibold mb-2 text-[#0f172a]">Bem-vindo ao meu portfólio!</h2>
      <p class="text-xl mt-4">
        Sou um estudante apaixonado por programação e tecnologias digitais inovadoras. Com o intuito de se tornar um profissional cada vez mais, estou sempre em busca de novos desafios e oportunidades para melhorar a experiência do usuário e transformar ideias em realidade.
      </p>
      <p class="text-xl mt-4">
        Aqui, voce pode encontrar informacoes sobre minhas habilidades e projetos pessoais. Espero que voce tenha uma boa visita!
      </p>
      <div class="mt-6 text-center">
        <button @click="showProjects = !showProjects"
          class="bg-[#2563EB] hover:bg-[#1D4ED8] text-white py-2 px-6 rounded-full font-medium transition duration-300">
          Veja meus projetos
        </button>
      </div>

      <!-- Lista de Projetos -->
      <transition name="fade">
        <div v-if="showProjects" class="grid grid-cols-1 md:grid-cols-2 gap-6 mt-8">
          <div v-for="project in projects" :key="project.id" class="bg-[#F1F5F9] p-4 rounded shadow">
            <h3 class="text-lg font-semibold mb-2">{{ project.title }}</h3>
            <p class="text-sm text-[#4B5563] mb-4">{{ project.description }}</p>
            <a :href="project.link" target="_blank"
              class="inline-block bg-[#2563EB] text-white py-1 px-4 rounded hover:bg-[#1D4ED8] transition">
              Ver projeto
            </a>
          </div>
        </div>
      </transition>
    </section>

    <!-- Seção de habilidades -->
    <section class="mt-14 text-center w-full max-w-6xl">
      <h2 class="text-3xl font-semibold text-[#0f172a] mb-8">Linguagens e Frameworks que Trabalho</h2>
      <div class="grid grid-cols-2 sm:grid-cols-3 lg:grid-cols-4 gap-8 mt-10 bg-gradient-to-r from-[#F3F4F6] to-[#E5E7EB] p-8 rounded-lg shadow-lg">
        <div class="text-[#1F2937] font-medium flex flex-col items-center">
          <img src="../assets/images/lua.png" alt="LUA" class="w-12 h-12 mb-2">
          LUA
        </div>
        <div class="text-[#1F2937] font-medium flex flex-col items-center">
          <img src="../assets/images/python.png" alt="PYTHON" class="w-12 h-12 mb-2">
          PYTHON
        </div>
        <div class="text-[#1F2937] font-medium flex flex-col items-center">
          <img src="../assets/images/csharp.png" alt="C#" class="w-12 h-12 mb-2">
          C#
        </div>
        <div class="text-[#1F2937] font-medium flex flex-col items-center">
          <img src="../assets/images/html.png" alt="HTML" class="w-12 h-12 mb-2">
          HTML
        </div>
        <div class="text-[#1F2937] font-medium flex flex-col items-center">
          <img src="../assets/images/css.png" alt="CSS" class="w-12 h-12 mb-2">
          CSS
        </div>
        <div class="text-[#1F2937] font-medium flex flex-col items-center">
          <img src="../assets/images/php.png" alt="PHP" class="w-12 h-12 mb-2">
          PHP
        </div>
        <div class="text-[#1F2937] font-medium flex flex-col items-center">
          <img src="../assets/images/js.png" alt="JS" class="w-12 h-12 mb-2">
          JS
        </div>
        <div class="text-[#1F2937] font-medium flex flex-col items-center">
          <img src="../assets/images/mysql.png" alt="MYSQL" class="w-12 h-12 mb-2">
          MYSQL
        </div>
      </div>
    </section>
    <section class="mt-5 text-center w-full max-w-6xl">
      <div class="grid grid-cols-2 sm:grid-cols-3 lg:grid-cols-4 gap-8 mt-10 bg-gradient-to-r from-[#F3F4F6] to-[#E5E7EB] p-8 rounded-lg shadow-lg">
        <div class="text-[#1F2937] font-medium flex flex-col items-center">
          <img src="../assets/images/vue.png" alt="VUE" class="w-12 h-12 mb-2">
          VUE
        </div>
        <div class="text-[#1F2937] font-medium flex flex-col items-center">
          <img src="../assets/images/vite.png" alt="VITE" class="w-12 h-12 mb-2">
          VITE
        </div>
        <div class="text-[#1F2937] font-medium flex flex-col items-center">
          <img src="../assets/images/tailwind.png" alt="TAILWIND" class="w-12 h-12 mb-2">
          TAILWIND
        </div>
        <div class="text-[#1F2937] font-medium flex flex-col items-center">
          <img src="../assets/images/dotnet.png" alt=".NET" class="w-12 h-12 mb-2">
          .NET
        </div>

      </div>
    </section>

  </main>
</template>

<script setup>
import { ref } from 'vue'

const showProjects = ref(false)

const projects = [
  {
    id: 1,
    title: 'Projetos em Lua e Luau Script',
    description: 'Projetos desenvolvidos por mim ao longo do tempo em Luau Script para diferentes experiências no jogo Roblox.',
    link: 'https://github.com/Plugxhz/Projects'
  },
  {
    id: 2,
    title: 'Projeto API Dragon Ball',
    description: 'Projeto feito em sala de aula usando HTML, CSS e JavaScript realizando o consumo da API oficial do Dragon Ball.',
    link: 'https://github.com/Plugxhz/Dragon-Ball-Project'
  },
  {
    id: 3,
    title: 'Projeto API Star Wars',
    description: 'Projeto feito por mim quando estava participando de um processo seletivo, foi usado HTML, CSS e JavaScript realizando o consumo da API oficial do Star Wars.',
    link: 'https://github.com/Plugxhz/Star-Wars-Project'
  },
  {
    id: 4,
    title: 'Projeto Player',
    description: 'Projeto em PHP feito na aula de POO do professor Valdir, foi desenvolvido por mim e pelo meu colega de turma Marcos Paulo.',
    link: 'https://github.com/Plugxhz/Player-Project'
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
