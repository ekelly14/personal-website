<template>
  <section class="flex flex-row bg-teal-300 mx-auto">
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
</template>

<script>
export default {
  name: 'NavBar'
}
</script>

<style lang="scss" scoped>
</style>