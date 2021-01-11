<template>
  <v-app>
    <v-app-bar
      app
      dense
      class="header-style"
    >
      <div class="d-flex align-center">
        <v-img
          alt="Vuetify Logo"
          class="shrink mr-2"
          contain
          src="@/assets/img/logo.png"
          transition="scale-transition"
          width="40"
        />

        <v-btn href="#" text class="app-button">
          <span class="mr-2">cumulative_intelligence</span>
        </v-btn>
         <v-btn href="#" text>
          <span class="mr-2">cBMI Demo</span>
        </v-btn>
      </div>

      <v-spacer></v-spacer>

      <v-btn
        href="#"
        target="_blank"
        color="#5B5D45"
        class="app-btn"
      >
        <span class="mr-2">Request a call</span>
      </v-btn>
    </v-app-bar>

    <v-main>
        <v-container fluid>
          <!-- <router-view></router-view> -->
        </v-container>
    </v-main>
    <v-footer app>
    </v-footer>
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

<style>
  .header-style {
    background-color: white !important;
  }
</style>
