<template>
    <div>
           <v-app-bar
      color="blue darken-4"
      dark 
      dense
    >
    <div class="d-flex justify-center flex-grow-1" >
         <v-btn color="blue darken-3" @click="redirectTo">
        <v-icon>
            mdi-home
        </v-icon>
        Home
    </v-btn>
    </div>
    </v-app-bar>
    </div>
</template>

<script>
export default {
    name: 'nav-comp',
    // props: {},
    data: function(){
        return {}
    },
    // computed: {},
    methods: {
           redirectTo(){
            console.log(this.$route.path)

            if(this.$route.path== '/'){
                alert('Ya estas en Home.')
                 return
            }
           
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
    
</style>