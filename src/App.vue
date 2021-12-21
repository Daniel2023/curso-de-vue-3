<template>
  <div>
    <Header :esta_logado=true />
    <PrimeiroComponente />
    <p class="paragrafo-pai">O dado de app é {{ testando }}.</p>
    <LifeCycle />
    <Pessoa />
  </div>
</template>

<script>
  import PrimeiroComponente from './components/PrimeiroComponent'
  import LifeCycle from './components/LifeCycle'
  import Pessoa from './components/Pessoa'
  import Header from './components/Header'


export default {
  name: 'App',
  components: {
    Header,
    PrimeiroComponente,
    LifeCycle,
    Pessoa
  },
  data(){
    return {
      testando: "Teste"
    }
  }
}
</script>

<style>
  body {
    background-color: #333;
    color: #FFF;
  }

  a {
    color: red;
  }

  .teste {
    background-color: #000;
  }

</style>