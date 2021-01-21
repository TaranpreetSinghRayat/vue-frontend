<template>
  <v-app>
    <v-app-bar app dense class="header-style">
      <div class="d-flex align-center">
        <v-img
          alt="Vuetify Logo"
          class="shrink mr-2"
          contain
          src="@/assets/img/cumulative-logo-final-5B5D45_bjd@2x.png"
          transition="scale-transition"
          width="40"
        />

        <router-link class="link" to="/">cumulative_intelligence</router-link>
        <router-link class="link" to="/">cBMI Demo</router-link>
        <router-link class="link" to="/about">About</router-link>
      </div>

      <v-spacer></v-spacer>

      <v-btn href="#" target="_blank" class="app-btn">
        <span class="mr-2">Request a call</span>
      </v-btn>
    </v-app-bar>

    <v-main>
      <v-container fluid style="padding:0">
        <router-view />
      </v-container>
    </v-main>
    <v-footer> </v-footer>
  </v-app>
</template>

<style lang="scss">
#app {
  background-image: url("assets/img/Mask_Group_1@2x.png");
  background-repeat: no-repeat;
  background-size: 100% 550px;
  font-family: "Aktiv Grotesk Corp", sans-serif !important;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

.header-style {
  background-color: rbg(0, 0, 0, 0.1);
  background-image: url("assets/img/Mask_Group_1@2x.png");
  background-repeat: no-repeat;

  background-size: 100% 550px;
  padding: 0 53px;
}

.link {
  margin-right: 20px;
  text-decoration: none;

  &.router-link-exact-active {
    color: white;
    font-weight: bold;
  }

  a {
    color: white;
  }
}
</style>
