<template>
  <main class="min-h-screen p-6 flex flex-col items-center bg-[#F9FAFB]">
    <!-- Cabeçalho -->
    <header class="bg-[#1A2E4A] w-full py-8 text-center shadow-md text-white">
      <h1 class="text-4xl font-bold font-sans">Entre em contato</h1>
      <p class="text-xl mt-2 font-light">Fale comigo ou me acompanhe nas redes sociais</p>
    </header>

    <!-- Formulário de Contato -->
    <section class="bg-white max-w-3xl w-full mt-12 p-8 rounded-lg shadow-lg text-[#1F2937]">
      <h2 class="text-2xl font-semibold text-[#0f172a] mb-6 text-center">Formulário</h2>
      <form class="space-y-6">
        <div>
          <label for="name" class="block text-sm font-medium mb-1">Nome</label>
          <input type="text" id="name" class="w-full px-4 py-2 border rounded-md shadow-sm focus:outline-none focus:ring-2 focus:ring-[#2563EB]">
        </div>
        <div>
          <label for="email" class="block text-sm font-medium mb-1">Email</label>
          <input type="email" id="email" class="w-full px-4 py-2 border rounded-md shadow-sm focus:outline-none focus:ring-2 focus:ring-[#2563EB]">
        </div>
        <div>
          <label for="message" class="block text-sm font-medium mb-1">Mensagem</label>
          <textarea id="message" rows="5" class="w-full px-4 py-2 border rounded-md shadow-sm focus:outline-none focus:ring-2 focus:ring-[#2563EB]"></textarea>
        </div>
        <div class="text-center">
          <button type="button"
            class="bg-[#2563EB] hover:bg-[#1D4ED8] text-white py-2 px-6 rounded-full font-medium transition duration-300">
            Enviar mensagem
          </button>
        </div>
      </form>
    </section>

    <!-- Redes Sociais -->
    <section class="mt-14 text-center w-full max-w-4xl">
      <h2 class="text-2xl font-semibold text-[#0f172a] mb-6">Redes sociais</h2>
      <div class="flex justify-center flex-wrap gap-6 text-[#1F2937]">
        <a href="https://github.com/Plugxhz" target="_blank" class="flex items-center gap-2 bg-[#F1F5F9] px-5 py-3 rounded-lg shadow hover:bg-[#E5E7EB] transition">
          <img src="../assets/images/github.png" alt="GitHub" class="w-6 h-6">
          GitHub
        </a>
        <a href="https://br.linkedin.com/in/enzo-bedendo-sakatauskas-1a5228267" target="_blank" class="flex items-center gap-2 bg-[#F1F5F9] px-5 py-3 rounded-lg shadow hover:bg-[#E5E7EB] transition">
          <img src="../assets/images/linkedin.png" alt="LinkedIn" class="w-6 h-6">
          LinkedIn
        </a>
        <a href="mailto:enzosakatauskas@email.com" class="flex items-center gap-2 bg-[#F1F5F9] px-5 py-3 rounded-lg shadow hover:bg-[#E5E7EB] transition">
          <img src="../assets/images/email.png" alt="Email" class="w-6 h-6">
          Email
        </a>
        <a href="https://www.instagram.com/enzo.saka/" target="_blank" class="flex items-center gap-2 bg-[#F1F5F9] px-5 py-3 rounded-lg shadow hover:bg-[#E5E7EB] transition">
          <img src="../assets/images/instagram.png" alt="Instagram" class="w-6 h-6">
          Instagram
        </a>
        <a href="https://wa.me/5514997479053" target="_blank" class="flex items-center gap-2 bg-[#F1F5F9] px-5 py-3 rounded-lg shadow hover:bg-[#E5E7EB] transition">
          <img src="../assets/images/whatsapp.png" alt="WhatsApp" class="w-6 h-6">
          WhatsApp
        </a>
        <a href="https://discord.gg/4a3SznvyYY" target="_blank" class="flex items-center gap-2 bg-[#F1F5F9] px-5 py-3 rounded-lg shadow hover:bg-[#E5E7EB] transition">
          <img src="../assets/images/discord.png" alt="Discord" class="w-6 h-6">
          Discord
        </a>
      </div>
    </section>
  </main>
</template>