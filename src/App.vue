<template>
  <v-app>
    <v-app-bar
      app
      color="indigo"
      dark
    >
    
      <div class="d-flex align-center">

		<v-icon large>mdi-account-details</v-icon>

		<div class="headline ml-3">Ez<span class='font-weight-bold'>Track</span></div>

      </div>

      <v-spacer></v-spacer>

      Blah

    </v-app-bar>

    <v-content>
      <router-view></router-view>
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
