<script setup>
definePageMeta({
  layout: "landing",
  title: "Perguntas Frequentes",
  description: "Respostas às dúvidas mais comuns dos nossos clientes.",
});

const perguntas = [
  {
    pergunta: "Como faço para alterar meu DNS?",
    resposta: "Você pode alterar seu DNS acessando as configurações de rede do seu dispositivo. Caso precise de ajuda, entre em contato com nosso suporte.",
  },
  {
    pergunta: "O que fazer se meu acesso for bloqueado?",
    resposta: "Se o acesso for bloqueado, tente reiniciar o roteador ou use um DNS alternativo. Caso o problema persista, entre em contato conosco.",
  },
  {
    pergunta: "Como funciona a promoção de indicação?",
    resposta: "Indique dois amigos e ganhe um mês de assinatura grátis após eles confirmarem o pagamento.",
  },
];
</script>

<template>
  <div class="max-w-4xl mx-auto mt-16">
    <h1 class="text-3xl font-bold text-center mb-8 text-gray-800">Perguntas Frequentes</h1>
    <div class="space-y-4">
      <div v-for="(faq, index) in perguntas" :key="index" class="p-4 border rounded bg-white shadow-md">
        <details class="group">
          <summary class="text-xl font-semibold cursor-pointer text-gray-800 group-hover:underline">
            {{ faq.pergunta }}
          </summary>
          <p class="mt-2 text-gray-600">{{ faq.resposta }}</p>
        </details>
      </div>
    </div>
  </div>
</template>

<style>
/* Estilo adicional, se necessário */
summary {
  list-style: none; /* Remove o estilo padrão da seta */
}
details[open] summary {
  font-weight: bold; /* Realça o título quando expandido */
}
</style>
