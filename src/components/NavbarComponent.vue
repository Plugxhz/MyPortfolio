<template>
  <nav
    class="bg-[#0f172a] text-white text-2xl py-10 px-8 flex justify-between items-center font-mono"
  >
    <button
      @click="$router.push('/')"
      class="bg-transparend hover:bg-[#1D4ED8] text-white w-40 h-20 rounded-sm px-4 py-2 font-medium transition duration-300"
    >
      My Portfolio
    </button>
    <div class="flex gap-6">
      <button
        @click="$router.push('/')"
        class="bg-transparend hover:bg-[#1D4ED8] text-white py-2 px-6 rounded-full font-medium transition duration-300"
      >
        Home
      </button>
      <button
        @click="$router.push('/about')"
        class="bg-transparend hover:bg-[#1D4ED8] text-white py-2 px-6 rounded-full font-medium transition duration-300"
      >
        Sobre
      </button>
      <button
        @click="$router.push('/contact')"
        class="bg-transparend hover:bg-[#1D4ED8] text-white py-2 px-6 rounded-full font-medium transition duration-300"
      >
        Contato
      </button>
    </div>
  </nav>
</template>


