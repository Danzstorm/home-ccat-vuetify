<template>
  <v-app>
    <v-app-bar
      app
      color= rgb(0,0,36,255)
      dark

    >
      <div class="d-flex align-center">
        <v-img    
          class="shrink mr-2"
          contain
          src="./assets/logo-ccat.png"
          transition="scale-transition"
          width="60"
        />

        <v-app-bar-title class="titulo">CENTRO CULTURAL AVANZADA TECNOLOGICA</v-app-bar-title>
     
      </div>

      <v-spacer></v-spacer>

      <v-toolbar-items>
        <v-btn dark color=rgb(0,0,36,255)> Inicio</v-btn>
        <v-menu offset-y>
          <template v-slot:activator="{ on , attrs}">
            <v-btn
              color=rgb(0,0,36,255)
              v-bind="attrs"
              v-on="on"
            >¿Quienes somos?</v-btn>
          </template>
          <v-list>
            <v-list-item
              v-for="(item, index) in items1"
              :key="index"
            >
            <v-list-item-title>{{item.title}}</v-list-item-title>
            </v-list-item>
          </v-list>
        </v-menu>
          <v-menu offset-y>
          <template v-slot:activator="{ on , attrs}">
            <v-btn
              color=rgb(0,0,36,255)
              v-bind="attrs"
              v-on="on"
            >Áreas</v-btn>
          </template>
          <v-list>
            <v-list-item
              v-for="(item, index) in items2"
              :key="index"
            >
            <v-list-item-title>{{item.title}}</v-list-item-title>
            </v-list-item>
          </v-list>
        </v-menu>
         <v-menu offset-y>
          <template v-slot:activator="{ on , attrs}">
            <v-btn
              color=rgb(0,0,36,255)
              v-bind="attrs"
              v-on="on"
            >Proyectos</v-btn>
          </template>
          <v-list>
            <v-list-item
              v-for="(item, index) in items3"
              :key="index"
            >
            <v-list-item-title>{{item.title}}</v-list-item-title>
            </v-list-item>
          </v-list>
        </v-menu>
        <v-btn dark color=rgb(0,0,36,255)>Productos</v-btn>
        <v-btn dark color=rgb(0,0,36,255)>Proximos eventos</v-btn>

      </v-toolbar-items>
    </v-app-bar>

    <v-main>
      <HelloWorld/>
      <Sliders/>
    </v-main>
  </v-app>
</template>

<script>
import HelloWorld from './components/HelloWorld';
import Sliders from './components/Sliders';

export default {
  name: 'App',

  components: {
    HelloWorld,
    Sliders
  },

  data: () => ({
    items1:[
      {title:'Nosotros'},
      {title:'Miembros'}
    ],
    items2:[
      {title:'Direcciones'},
      {title:'Gerencias'}
    ],
    items3:[
      {title:'Proyectos'},
      {title:'Competitivdad'},
      {title:'CODEX'}
    ]
  }),
};
</script>

<style scoped>

.titulo{
 font-size:0.9rem;
}



</style>
