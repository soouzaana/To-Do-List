<template>
  <div>
    <div class="ma-4 text-center">
      <h1 class="ma-4">Obrigada!</h1>
      <p class="ma-4">
        Abaixo estão algumas tecnologias que foram utilizadas neste projeto.
      </p>
      <v-divider></v-divider>
    </div>
    <div></div>
    <div class="ma-4 d-flex">
      <AboutCard
        v-for="(item, index) in items"
        :key="index"
        :image="item.image"
        :title="item.title"
        :subtitle="item.subtitle"
        :text="item.text"
      />
    </div>

    <div class="text-center">
      <v-divider class="ma-4"></v-divider>
      <a
      target="_blank"
      href="https://link-service.netlify.app/"
      alt="Minhas mídias sociais"
      >
      <v-btn
      color="primary"
      >Créditos</v-btn>
      </a>
    </div>
  </div>
</template>
<script setup>
import AboutCard from "./AboutCard.vue";
</script>
