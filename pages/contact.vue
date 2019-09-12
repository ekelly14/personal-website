<template>
  <div>
    <TitleBar />
    <div class="container mx-auto">
      <div class="home">
        <a href="https://github.com/ekelly14">
          <div class="link-container">
            <strong>Github</strong>
            <i>ekelly14</i>
          </div>
        </a>
        <a href="https://www.linkedin.com/in/elijah-kelly-32878917a/">
          <div class="link-container">
            <strong>LinkedIn</strong>
            <i>Elijah Kelly</i>
          </div>
        </a>
        <a href="mailto:ekelly14@ymail.com">
          <div class="link-container">
            <strong>Email</strong>
            <i>ekelly14@ymail.com</i>
            <i>elk8kh@gmail.com</i>
          </div>
        </a>
      </div>
    </div>
  </div>
</template>

<script>
import TitleBar from '~/components/header/TitleBar.vue'
  export default {
    components: {
      TitleBar
    },
    head() {
      return {
        title: "Elijah Kelly | Contact"
      }
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
.link-container {
  padding: 2rem;
  margin-left: 1rem;
  margin-right: 1rem;
  background-color:cadetblue;
  display: flex;
  flex-direction: column;
}
</style>