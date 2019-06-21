<template>
  <no-ssr>
    <section
      class="flex flex-row mx-auto fixed bg-teal-300 w-full"
      v-bind:class="{ scrolled: isScrolled }"
    >
      <nuxt-link to="/">
        <div class="px-10 py-5 w-auto hover:bg-teal-400 hover:text-white">Home</div>
      </nuxt-link>
      <nuxt-link to="/about">
        <div class="px-10 py-5 w-auto hover:bg-teal-400 hover:text-white">About Me</div>
      </nuxt-link>
      <nuxt-link to="/about">
        <div class="px-10 py-5 w-auto hover:bg-teal-400 hover:text-white">Hobbies</div>
      </nuxt-link>
      <a href="https://github.com/ekelly14">
        <div class="px-10 py-5 hover:bg-teal-400 hover:text-white">GitHub</div>
      </a>
    </section>
  </no-ssr>
</template>

<script>
export default {
  name: 'NavBar',
  data() {
    return {
      isScrolled: false
    }
  },
  beforeMount() {
    //Check if the page is already scrolled
    this.handleScroll()
    //initializes the event listener for scroll
    window.addEventListener('scroll', this.handleScroll)
  },
  beforeDestroy() {
    //cleanup events before destroy
    window.removeEventListener('scroll', this.handleScroll)
  },
  methods: {
    handleScroll() {
      //Check if the page is scrolled from the original position
      this.isScrolled = window.pageYOffset > 35
    }
  }
}
</script>

<style scoped>
.scrolled {
  background: white;
}
</style>