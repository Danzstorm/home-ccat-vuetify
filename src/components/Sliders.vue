<template>
  <v-container>
    <v-row class="text-center">
      <v-col class="mb-4">
        <h1 class=" font-weight-bold mb-3 mt-4">
          CONVENIOS
        </h1>
      </v-col>
    </v-row>
    <v-row class="text-center">
      <v-col class="mb-4">
        <h2 class="font-weight-bold mb-3 mt-4">
          AUSPICIADORES
        </h2>
      </v-col>
      <v-col class="mb-4">
        <h2 class="font-weight-bold mb-3 mt-4">
          ALIADOS
        </h2>
      </v-col>
    </v-row>

    <v-row>
      <v-col cols="12" md="6">
        <v-sheet  class="mx-auto" elevation="8"  max-width="800" >
          <v-slide-group
            show-arrows="always"

          >
            <v-slide-item v-for="item in logos" :key="item.id">

              <v-sheet class="ma-4"
                   height="200"
                   width="200">

                     <v-img
                  max-height="200"
                  max-width="200"
                  :src="item.direccion"
                >
                </v-img>                 
              </v-sheet>
            </v-slide-item>
          </v-slide-group>
        </v-sheet>
      </v-col>
      <v-col cols="12" md="6">
        <v-sheet  class="mx-auto" elevation="8"  max-width="800" >
          <v-slide-group
            show-arrows="always"

          >
            <v-slide-item v-for="item in logos" :key="item.id">

              <v-sheet class="ma-4"
                   height="200"
                   width="200">

                     <v-img
                  max-height="200"
                  max-width="200"
                  :src="item.direccion"
                >
                </v-img>                 
              </v-sheet>
            </v-slide-item>
          </v-slide-group>
        </v-sheet>
      </v-col>

    </v-row>
  </v-container>
</template>

<script>
export default {
  name: "Sliders",
  data: () => ({
    ismounted:false,
    model:null,
  }),
  computed:{
    logos(){
      return [
      { id:1,
        direccion: require("@/assets/ainad-logo.png"),
      },
      { id:2,
        direccion: require("@/assets/dmc-logo.png"),
      },
      { id:3,
        direccion: require("@/assets/fiis-logo.jpg"),
      },
      { id:4,
        direccion: require("@/assets/nucleo-logo.png"),
      },
      { id:5,
        direccion: require("@/assets/proyecta-logo.jpg"),
      },
    ]
    }
  },
  mounted(){
    this.ismounted=true;
  },
};
</script>

<style></style>
