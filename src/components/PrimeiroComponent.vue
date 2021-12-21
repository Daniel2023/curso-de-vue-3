<template>
<div>
    <Reutilizacao />
    <h1>Olá Vue!</h1>
    <p>Meu nome é {{ name }} e trabalho como {{ profissao }}.</p>
    <MultiplosEventos />
</div>
    </template>

<script>
import MultiplosEventos from './MultiplosEventos'
import Reutilizacao from './Reutilizacao.vue'

export default {
    name: 'PrimeiroComponente',
    components: {
        MultiplosEventos,
        Reutilizacao
    },
    data() {
        return {
            name: "Daniel",
            profissao: "Programador"
        }
    }
}
</script>