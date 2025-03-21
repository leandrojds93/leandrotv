<template>
  <main class="grid lg:grid-cols-2 place-items-center justify-center w-full min-h-screen py-16 px-5 lg:px-5 text-white rounded-lg">
    <!-- Imagem com tamanho ajustado -->
    <div class="md:order-1 flex justify-center">
      <img
        class="transition-transform transform hover:scale-110 hover:rotate-1 duration-300 w-full max-w-3xl rounded-lg"
        src="~/assets/img/banner.png"
        alt="Starship starts the engine"
        loading="eager"
        format="avif"
      />
    </div>

    <!-- Texto principal -->
    <div>
      <h1 class="text-5xl lg:text-6xl xl:text-7xl font-extrabold lg:tracking-tight mb-4 text-gray-900 drop-shadow-lg">
      O melhor serviço de IPTV do Brasil.
      </h1>      
      <p class="text-lg mt-4 text-slate-400 max-w-xl leading-relaxed">
        Assista o que quiser, onde quiser e quando quiser com a maior
        variedade de conteúdos do Brasil e uma enorme gama de opções de entretenimento.
      </p>
      
      <!-- Botões com interação aprimorada -->
      <div class="mt-8 flex flex-col sm:flex-row gap-4">
        <LandingLink
          href="/pricing"
          rel="noopener"
          class="bg-blue-600 hover:bg-blue-700 text-white px-4 py-2 text-sm font-medium rounded-md shadow-lg transition-all"
        >
          Planos e Valores
        </LandingLink>
        <LandingLink
          size="lg"
          rel="noopener"
          href="https://wa.me/5534984164210?text=Solicitar%20teste%20gr%C3%A1tis!"
          target="_blank"
          class="bg-green-600 hover:bg-green-700 text-white px-4 py23 text-sm font-medium rounded-md shadow-lg transition-all"
        >
          Solicitar teste grátis!
        </LandingLink>
        <LandingLink
          size="lg"
          rel="noopener"
          href="/faq"
          class="bg-green-600 hover:bg-green-700 text-white px-4 py-2 text-sm font-medium rounded-md shadow-lg transition-all"
        >
          Duvidas Frequentes!
        </LandingLink>
      </div>
    </div>
  </main>
</template>
