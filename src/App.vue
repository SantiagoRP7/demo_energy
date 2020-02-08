<template>
  <v-app>
    <v-app-bar
      app
      color="#949599"
      dark
    >
      <div class="d-flex align-center">
        <v-app-bar-nav-icon @click="drawer = true"></v-app-bar-nav-icon>
          <v-img
          class="shrink mr-2"
          :src="require('./assets/logo.png')"
          contain
          transition="scale-transition"
          width="145"
        />
      
      </div>

    </v-app-bar> 

    <v-content>
      <HelloWorld/>
    </v-content>

    <v-navigation-drawer
        v-model="drawer"
        absolute
        temporary
      >
      <v-list nav dense>
        <v-list-item-group>
          <v-list-item>
            Pagos
          </v-list-item>

          <v-list-item>
            Contador
          </v-list-item>

          <v-list-item>
            span
          </v-list-item>

        </v-list-item-group>
      </v-list>
      </v-navigation-drawer>
  </v-app>
</template>

<script>
import HelloWorld from './components/HelloWorld';

export default {
  name: 'App',

  components: {
    HelloWorld,
  },

  data: () => ({
    //
    drawer: false,
  }),
};
</script>
