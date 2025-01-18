<template>
  <div class="pa-3">
    <br>
    <h1 class="text-center">Sobre</h1>
    <br>
    <p>
      Essa é uma lista de tarefas desenvolvida para fins didáticos com Vue.js.
      Esse projeto foi desenvolvido durante o curso de Vue 3, ministrado pelo professor
      <a href="https://link-service.netlify.app/">Yuri Marcon</a>, na plataforma <a href="https://www.udemy.com/">Udemy</a>.
    </p>
    <br>
    <p>
      Tecnologias Utilizadas:
    </p>
    <v-list>
      <v-list-item v-for="item in tecnologias" :key="item.titulo">
        <v-list-item-content>
          <div class="d-flex align-center">
            <v-icon class="mr-2">{{ item.icon }}</v-icon>
            <v-list-item-title>{{ item.titulo }}</v-list-item-title>
          </div>
        </v-list-item-content>
      </v-list-item>
    </v-list>
    <section>
      <br>
      <p>
        <v-card-title>Obrigada por prestigiar este projeto!</v-card-title>
        <br>
        <v-card-subtitle>Contato:</v-card-subtitle>
        <v-card-text>
          <strong>📨E-mail:</strong> anamariasouza701@gmail.com<br />
          <strong>👩🏽‍💻Ana Maria</strong><br />
          <img src="@/assets/octocat.png" height="20px" alt="imagem octocat" />
          <a href="https://github.com/souzaana">/souzaana</a>
        </v-card-text>
      </p>
    </section>
  </div>
</template>

<script>
export default {
  data() {
    return {
      tecnologias: [
        { icon: "mdi-language-html5", titulo: "HTML" },
        { icon: "mdi-vuejs", titulo: "Vue.js" },
        { icon: "mdi-vuetify", titulo: "Vuetify" },
        { icon: "mdi-vuejs", titulo: "VUEX" },
        { icon: "mdi-vuejs", titulo: "VueRouter" },
        { icon: "mdi-database", titulo: "Localbase DB" },
        { icon: "mdi-transition", titulo: "Animate.css" },
        { icon: "mdi-drag-variant", titulo: "Drag and Drop" },
        { icon: "mdi-git", titulo: "Git" },
        { icon: "mdi-github", titulo: "GitHub" },
        { icon: "mdi-web", titulo: "Netlify" },
      ],
    };
  },
};
</script>

<style scoped>
.d-flex {
  display: flex;
  align-items: center;
}
.mr-2 {
  margin-right: 8px;
}
</style>
