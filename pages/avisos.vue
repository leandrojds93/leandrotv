<script setup>
definePageMeta({
  layout: "landing",
});

const avisos = [
  {
    titulo: "Mudança de DNS",
    mensagem: "Recentemente houve alteração em algumas DNS de nossos servidores. Caso tenha problemas, entre em contato.",
    icone: "🛠️",
  },
  {
    titulo: "Bloqueio das operadoreas",
    mensagem: "As operadoras de internet estão a todo instante bloqueando servidores pela DNS, causando transtornos.",
    icone: "🕒",
  },
  {
    titulo: "Promoção Especial",
    mensagem: "Indique dois amigos e ganhe mais um mês de assinatura totalmente grátis.",
    icone: "🎉",
  },
];
</script>

<template>
  <div class="max-w-4xl mx-auto mt-16">
    <h1 class="text-3xl font-bold text-center mb-8 text-gray-800">Quadro de Avisos</h1>
    <div class="grid md:grid-cols-3 gap-6">
      <div
        v-for="(aviso, index) in avisos"
        :key="index"
        class="p-4 border rounded shadow-md bg-white text-center transition hover:shadow-lg"
      >
        <div class="text-4xl mb-4">{{ aviso.icone }}</div>
        <h2 class="text-xl font-semibold text-gray-800 mb-2">{{ aviso.titulo }}</h2>
        <p class="text-gray-600">{{ aviso.mensagem }}</p>
      </div>
    </div>
  </div>
</template>

<style>
/* Personalize o estilo adicional, se necessário */
</style>