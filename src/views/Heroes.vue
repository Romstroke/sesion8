<template>
  <div class="heroes">
    <div class="background"></div>
    <v-container class="contenedor">
      <div>
        <h1 class="titulo">Heroes</h1>
        <div class="iconos">
          <v-icon class="icon">mdi-sword</v-icon>
          <v-icon class="icon">mdi-shield</v-icon>
          <v-icon class="icon">mdi-crosshairs</v-icon>
          <v-icon class="icon">mdi-heart-plus</v-icon>
          <v-icon class="icon">mdi-dna</v-icon>
        </div>
      </div>
      <v-row justify="center">
        <v-col cols="12" sm="12">
          <v-simple-table dark class="tabla">
            <template v-slot:default>
              <thead>
                <tr>
                  <th class="text-left">Héroes</th>
                  <th class="text-left">Nombre</th>
                  <th class="text-left">Función</th>
                  <th class="text-left">Título</th>
                  <th class="text-left">Ataque</th>
                </tr>
              </thead>
              <tbody>
                <tr v-for="(heroe, index) in heroes" :key="index">
                  <td>
                    <img
                      :src="heroe.imagen"
                      alt=""
                      srcset=""
                      width="200px"
                      height="200px"
                    />
                  </td>
                  <td>{{ heroe.nombre }}</td>
                  <td>{{ heroe.funcion }}</td>
                  <td>{{ heroe.titulo }}</td>
                  <td>{{ heroe.ataque }}</td>
                </tr>
              </tbody>
            </template>
          </v-simple-table>
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>

<script>
import { mapState } from "vuex";

export default {
  name: "heroes-view",
  // props: {},
  data: function () {
    return {};
  },
  computed: {
    ...mapState(["heroes"]),
  },
  //methods: {},
  // watch: {},
  // components: {},
  // mixins: [],
  // filters: {},
  // -- Lifecycle Methods
  // -- End Lifecycle Methods
};
</script>

<style scoped>
.heroes {
    position: fixed;
    width: 100%;
    height: 100%;
}
.background {
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    background: url("../assets/fondo1.jpg");
    background-size: 100%;
    background-attachment: fixed;
    filter: blur(8px);
    z-index: -1;
}

.titulo {
  color: whitesmoke;
}
.tabla {
  max-height: 70vh;
  overflow: auto;
}
.icon {
  padding: 0 10px;
  font-size: 25px;
  color: rgb(238, 238, 238);
}
</style>