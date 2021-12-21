<template>
    <h1>Meu nome é: {{ nome }} </h1>
</template>

<script>
export default {
    name: 'LifeCycle',
    data() {
        return {
            nome: 'Ainda não sei'
        }
    },

    created() {
      setTimeout(() => {
        this.nome = 'Matheus'
    }, 1000);

    this.lifecycle()
},
    mounted() {
      setTimeout(() => {
        this.nome = 'Daniel'
    }, 2000);
    
    this.lifecycle()
},
    methods: {
        lifecycle() {
            console.log('executou')
        }
    }
}
</script>

