<template>
  <div>
    <h2>Meu Formulário:</h2>
    <form action="" @submit="enviarFormulario($event)">
      <div>
        <input type="text" v-model="name">
      </div>
      <div>
        <input type="text" v-model="email">
      </div>
      <div>
        <Submit />
      </div>
    </form>
  </div>
</template>
<script>
import InputText from "./InputText";
import Submit from "./Submit";

export default {
  name: "Form",
  components: {
    InputText,
    Submit,
  },
  data() {
    return {
      name: "",
      email: "",
    }
  },
  methods: {
    enviarFormulario(e) {
      e.preventDefault();

      const name = this.name;
      const email = this.email;

      console.log("Formulario Enviado!");
      console.log("O nome é:" + name);
      console.log("O email é:" + email);
    },
  },
};
</script>