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

        <v-btn href="#" text>
          <!-- <span class="mr-2">cumulative_intelligence</span> -->
          <router-link to="/">cumulative_intelligence</router-link>
        </v-btn>
         <!-- <v-btn href="#" text> -->
          <!-- <span class="mr-2">cBMI Demo</span> -->
          <router-link to="/">cBMI Demo</router-link>
          <router-link to="/about">About</router-link>
      </div>

      <v-spacer></v-spacer>

      <v-btn
        href="#"
        target="_blank"
        class="app-btn"
      >
        <span class="mr-2">Request a call</span>
      </v-btn>
    </v-app-bar>

    <v-main>
        <v-container fluid>
          <router-view />
        </v-container>
    </v-main>
    <v-footer app>
    </v-footer>
  </v-app>
</template>

<style lang="scss">
#app {
  background-color: rgba(0, 0, 0, 0.17);
  font-family: "Montserrat", sans-serif !important;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  padding: 30px;

  a {
    font-weight: bold;
    color: #2c3e50;

    &.router-link-exact-active {
      color: #42b983;
    }
  }
}

.header-style {
    background-color: white !important;
    padding: 0 53px;
}
</style>
