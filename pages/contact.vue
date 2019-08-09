<template>
  <div>
    <TitleBar />
    <div class="container mx-auto">
      <div class="home">
        Contact Me Page still under construction! 
        <br />
        <nuxt-link to="/" class="text-blue-dark">
          Back
        </nuxt-link>
      </div>
    </div>
  </div>
</template>

<script>
import TitleBar from '~/components/header/TitleBar.vue'
  export default {
    components: {
      TitleBar
    }
  }
</script>

<style scoped>
.container {
  height: 100vh;
  width: 100%;
  background-color: bisque;
}
.home {
  background-color: bisque;
  justify-content: center;
  align-items: center;
  text-align: center;
}
</style>