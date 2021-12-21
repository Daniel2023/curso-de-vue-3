<template>
  <div>
    <img :src="avatar" :alt="descricao" />
    <MudarImagem @mudar-imagem="trocarImagem" />
  </div>
</template>

<script>
import MudarImagem from "./MudarImagem";

export default {
  name: "Picture",
  components: {
    MudarImagem,
  },
  data() {
    return {
      avatar: "/img/avatar.png",
      descricao: "Daniel Silva",
    }
  },
  methods: {
    trocarImagem() {
      this.avatar = "/img/avatar2.png"
    }
  }  
}
</script>