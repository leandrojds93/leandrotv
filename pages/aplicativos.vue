<script setup>
definePageMeta({
  layout: "landing",
  title: "Aplicativos",
  description: "Baixe os aplicativos oficiais para Android TV e Tv Box.",
});

const app1 = "https://sharetvstore.pds01.site/control/actions/imagens_app/180325010058.png";
const app2 = "https://sharetvstore.pds01.site/control/actions/imagens_app/180325010308.png";
const app3 = "https://sharetvstore.pds01.site/control/actions/imagens_app/180325010606.png";

const apps = [
  {
    name: "SHARE IBO SMR",
    title: "Downloader: 1135527",
    dados: {
      src: app1,
      url: "https://sharetvstore.pds01.site/control/actions/aplicativos/SHAREIBOSMR4.apk",
      width: 580,
      height: 580,
    },
  },
  {
    name: "SHARE XC3D",
    title: "Downloader: 1452571",
    dados: {
      src: app2,
      url: "https://sharetvstore.pds01.site/control/actions/aplicativos/SHAREIBOSMR4.apk",
      width: 580,
      height: 580,
    },
  },
  {
    name: "SHARE UNI",
    title: "Downloader: 3314918",
    dados: {
      src: app3,
      url: "https://sharetvstore.pds01.site/control/actions/aplicativos/SHARETVUNI3.apk",
      width: 580,
      height: 580,
    },
  },
];
</script>

<template>
  <LandingContainer>
    <LandingSectionhead>
      <template v-slot:title>Share TV - Play Store</template>
      <template v-slot:desc>Aplicativos para Tv Box e Android TV.</template>
    </LandingSectionhead>

    <div class="flex flex-col gap-3 mx-auto max-w-4xl mt-16">
      <h2 class="font-bold text-3xl text-gray-800">
        Aplicativos disponíveis:
      </h2>
      <p class="text-lg leading-relaxed text-slate-500"> 
        Baixe os aplicativos oficiais para Android TV e Tv Box.
      </p>
    </div>
    <div class="grid md:grid-cols-3 gap-10 mx-auto max-w-4xl mt-12">
      <div v-for="item of apps" class="group">
        <div class="w-full">
          <img
            :src="item.dados.src"
            :width="item.dados.width"
            :height="item.dados.height"
            format="avif"
            alt="apps"
            class="w-full h-full object-cover rounded transition group-hover:-translate-y-1 group-hover:shadow-xl"
          />
        </div>

        <div class="mt-4 text-center">
          <h2 class="text-lg text-gray-800">{{ item.name }}</h2>
          <h3 class="text-sm text-slate-500">{{ item.title }}</h3>
          <a 
          :href="item.dados.url" 
          download 
          class="inline-block mt-2 px-4 py-2 text-white bg-blue-500 rounded hover:bg-blue-600 transition">
          Baixar
          </a>
        </div>
      </div>
      <!-- {
        team.map((item) => (
          <div class="group">
            <div class="w-full aspect-square">
              <Image
                {...item.avatar}
                format="avif"
                alt="Team"
                class="w-full h-full object-cover rounded transition  group-hover:-translate-y-1 group-hover:shadow-xl"
              />
            </div>

            <div class="mt-4 text-center">
              <h2 class="text-lg text-gray-800"> {item.name}</h2>
              <h3 class="text-sm text-slate-500"> {item.title}</h3>
            </div>
          </div>
        ))
      } -->
    </div>
  </LandingContainer>
</template>
