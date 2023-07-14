<template>
    <div class="contenedor text-center">
        <h1>Not found</h1>
        <img src="@/assets/5203299.jpg" alt="" srcset="" width="500px" height="500px">
        <p>La página que buscar no existe. Anda a Home.</p>
        <v-btn @click="redirectTo">Volver a Home</v-btn>
    </div>
</template>

<script>
export default {
    name: 'not-found',
    // props: {},
    data: function(){
        return {}
    },
    // computed: {},
    methods: {
        redirectTo(){
            this.$router.push('/')
        }
    }
    // watch: {},
    // components: {},
    // mixins: [],
    // filters: {},
    // -- Lifecycle Methods
    // -- End Lifecycle Methods
}
</script>

<style scoped>
    .contenedor{
        background-image: url('../assets/fondo2.jpg');
    }
</style>