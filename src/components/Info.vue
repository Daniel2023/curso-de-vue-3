<template>
  <div>
    <p v-if="esta_trabalhando">Estou trabalhando no momento.</p>
    <p v-else>Estou em busca de novas oportunidades!</p>
    <p>Utilizo as seguintes tecnologias para back-end:</p>
    <ul>
      <li
        v-for="(technology, index) in backend_technologies"
        v-bind:key="index"
      >
        {{ technology }}
      </li>
    </ul>
    <p>Utilizo as seguintes tecnologias para front-end:</p>
    <ul>
      <li v-for="technology in frontend_technologies" :key="technology.id">
        {{ technology.language }}
      </li>
    </ul>
    <div>
      <!--<p><input type="checkbox" @click="showEmail" checked> Mostrar E-mail</p> -->
      <button @click="showEmail">{{ botaoTexto }}</button>
    </div>
    <p v-show="mostrar_email">Mande uma mensagem para: {{ email }}</p>
    <p class="teste">
      Para acessar meu portifolio
      <a v-bind:href="meu_link" target="_blank">basta clicar aqui</a>
    </p>
    <Picture />
  </div>
</template>
<script>
import Picture from "./Picture";

export default {
  components: { Picture },
  name: "Info",
  componentes: {
    Picture,
  },

  props: {
    email: String,
    esta_trabalhando: Boolean,
  },
  data() {
    return {
      mostrar_email: false,
      meu_link: "https://google.com",
      botaoTexto: "Mostrar email",
      backend_technologies: ["JavaScript", "PHP", "Python"],
      frontend_technologies: [
        { id: 1, language: "HTML" },
        { id: 2, language: "CSS" },
        { id: 3, language: "VUE" },
      ],
    };
  },
  methods: {
    showEmail() {
      this.mostrar_email = !this.mostrar_email;
      if (!this.mostrar_email) {
        this.botaoTexto = "Mostrar email";
      } else {
        this.botaoTexto = "Esconder email";
      }
    },
  },
};
</script>

<style>
.paragrafo-pai {
  color: red;
}
</style>