<template>
  <div class="Welcome">
      <div class="application-container">
          <h1>Try the technology on desktop or mobile</h1>
          <v-btn class="app-btn margin-top-40" v-on:click ="goToApplication()">
              <span>Launch application</span>
          </v-btn>
      </div>
  </div>
</template>

<script>

export default {
  name: 'Welcome',
  methods: {
    goToApplication() {
      this.$router.push('application')
    }
  }
}
</script>
<style>
    .application-container {
        height: 378px;
        display: flex;
        align-items: center;
        justify-content: center;
        flex-direction: column;
    }
</style>