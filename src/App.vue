<template>
  <v-app>
    <v-app-bar
      app
      color="grey darken-4" 
      dark
    >
    <v-app-bar-nav-icon @click="drawer = !drawer"/>
    <v-toolbar-title class="font-weight-black text-h2" >SCV</v-toolbar-title>
    <v-toolbar-title class="font-weight-regular pl-md-2 pt-md-2 text-subtitle-2" >(Smart ConVeyor Belt)</v-toolbar-title>
    <v-toolbar-title class="font-weight-black pl-md-2 pt-md-2 text-h4" >System</v-toolbar-title>
      <v-spacer></v-spacer>
      <v-img
            :src="require('@/assets/rlogo.png')"
            class="ma-0 grey darken-4"
            contain
            aspect-ratio="9"
            position="right"
      />
    </v-app-bar>
    <v-main>
      <v-container fluid>
      <router-view />
      </v-container>
      <!-- <JsonCov ref="func"/> -->
    </v-main>
    <v-footer dark padless>
      <v-col
        class="text-center grey darken-3"
        cols="12"
      >
        <v-icon class="px-2" color="orange darken-2"> mdi-update</v-icon>
        <strong>Last updated : </strong>{{ this.$dayjs().format('YYYY-MM-DD HH:mm:ss') }} — <strong>SCV</strong>
      </v-col>
    </v-footer>
  </v-app>
</template>

<script>
// import { defineComponent } from '@vue/composition-api'

export default {
  name: 'App',
  created() {
  },
  data: ()=>({
    drawer : false,
  }),
};
</script>


