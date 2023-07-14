<template>
  <div class="home">
      <v-container >
    <v-row justify="center" class="mt-16" >
      <v-col cols="12" sm="8" class="box text-center ">
          <div>
             <h1>Desafía las expectativas de los MOBA</h1>
             <p>Épicos héroes y acciones sin cesar en múltiples campos de batalla!!! WOW</p>
             <v-btn color="orange darken-2" dark @click="redirectTo">Ver héroes</v-btn>
          </div>
      </v-col>
    </v-row>
  
  </v-container>
    <v-alert v-model="alert" border="left" color="purple darken-1" dark class="py-5 mt-14" style="opacity: 0.8">      
      ¡Te damos la bienvenida al Nexo! ¡En este reino entre reinos, todo es posible! Elige entre decenas de héroes legendarios de todo el panteón de Blizzard, personaliza sus talentos y habilidades en medio del combate y lucha en una infinidad de campos de batalla que redefinen el género. ¡Esto no es un MOBA promedio, eso es Heroes of th Storm!      
    </v-alert>
  </div>
</template>

<script>
  

  export default {
    name: 'Home-view',

    components: {
    
    },
    methods:{
          redirectTo(){
            this.$router.push('/heroes')
        }
    }
  }
</script>
<style scoped>
  .home{
    background-image: url('@/assets/fondo3.jpg');
    height: 100%;
  }
  .box{
    border: 1px solid whitesmoke;
    color: whitesmoke;
  }
</style>
