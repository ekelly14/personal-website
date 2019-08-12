<template>
  <no-ssr>
    <section class="flex flex-row mx-auto fixed navbar w-full shadow-xl" :class="{ scrolled: isScrolled }">
      <nuxt-link to="/">
        <div
          class="navitem hover:bg-teal-300 hover:text-white"
          :class="{ itemscrolled: isScrolled }"
        >Home</div>
      </nuxt-link>
      <a href="/#about">
        <div
          class="navitem hover:bg-teal-300 hover:text-white"
          :class="{ itemscrolled: isScrolled }"
        >About Me</div>
      </a>
      <nuxt-link to="/contact">
        <div
          class="navitem hover:bg-teal-300 hover:text-white"
          :class="{ itemscrolled: isScrolled }"
        >Contact Me</div>
      </nuxt-link>
      <a href="https://github.com/ekelly14">
        <div
          class="navitem hover:bg-teal-300 hover:text-white"
          :class="{ itemscrolled: isScrolled }"
        >GitHub</div>
      </a>
    </section>
  </no-ssr>
</template>

<script>
export default {
  name: 'TitleBar',
  data() {
    return {
      isScrolled: false
    }
  },
  beforeMount() {
    // Check if the page is already scrolled
    this.handleScroll()
    // initializes the event listener for scroll
    window.addEventListener('scroll', this.handleScroll)
  },
  beforeDestroy() {
    // cleanup events before destroy
    window.removeEventListener('scroll', this.handleScroll)
  },
  methods: {
    handleScroll() {
      // Check if the page is scrolled from the original position
      this.isScrolled = window.pageYOffset > 35
    }
  }
}
</script>

<style scoped>
.navbar {
  background: rgb(235, 235, 235);
  border-top: 4px solid #052f5f;
  border-bottom: 4px solid #052f5f;
  height: 64px;
  transition: all 0.3s;
  z-index: 1000;
}
.scrolled {
  background: white;
}
.navitem {
  padding-left: 2rem;
  padding-right: 2rem;
  margin: auto;
  min-height: 60px;
  display: flex;
  align-items: center;
}
.navitem:hover {
  color: white;
  background-color: rgb(204, 201, 201);
}
.itemscrolled:hover {
  background-color: rgb(204, 201, 201);
  transition: all 0.3s;
}
</style>
