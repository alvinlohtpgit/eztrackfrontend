<template>
  <v-app>
    <v-app-bar
      app
      color="indigo"
      dark
    >
    
      <div class="d-flex align-center">


    <v-img src='./assets/ezTrack.png'></v-img>
      </div>

      <v-spacer></v-spacer>

      Blah

    </v-app-bar>

    <v-content>
      <v-container>
        <router-view></router-view>
      </v-container>
    </v-content>
  </v-app>
</template>

<script> 

export default {
  name: 'App',

  data: () => ({
    //
  }),
};
</script>
