<template>
  <span>
    <vue-typer :text="textList" :shuffle="shuffle"></vue-typer>
  </span>
</template>

<script>
// this can only be imported client-side
const vueTyperRequire = process.client ? require('vue-typer') : null
const vueTyper = vueTyperRequire ? vueTyperRequire.VueTyper : null
  export default {
    name: "VueTyperWrapper",
    components: {
      vueTyper
    },
    props: {
      textList: {
        type: Array,
        required: true
      },
      shuffle: {
        type: Boolean,
        default: true
      }
    }
  }
</script>

<style scoped>

</style>