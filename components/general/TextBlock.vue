<template>
  <div class="mx-auto block-style mt-10" style="max-width: 1200px;" :class="{ 'bottom-border' : borderBottom }">
    <div v-if="title" class="w-full text-4xl pb-4">
      {{ title }}
    </div>
    <div v-if="!textOnRight" class="flex flex-row w-full h-full mb-10">
      <div class="h-full text-block pr-5 text-xl">
        <slot />
      </div>
      <div class="picture-block" :style="`background-image: url(/images/${imageUrl});`" :class="{ 'picture-circle' : roundImage }" />
    </div>

    <div v-if="textOnRight" class="flex flex-row w-full h-full mb-10">
      <div class="picture-block" :style="`background-image: url(/images/${imageUrl});`" :class="{ 'picture-circle' : roundImage }" />
      <div class="h-full text-block pl-5 text-xl">
        <slot />
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    name: 'TextBlock',
    props: {
      title: {
        type: String,
        default: ''
      },
      textOnRight: {
        type: Boolean,
        default: false
      },
      borderBottom: {
        type: Boolean,
        default: false
      },
      imageUrl: {
        type: String,
        default: ''
      },
      roundImage: {
        type: Boolean,
        default: false
      }
    }
  }
</script>

<style scoped>
.bottom-border {
  border-bottom: 2px solid #052f5f;
}
.text-block {
  flex-basis: 55%;
}
.picture-block {
  background-color: aquamarine;
  background-position: center;
  background-size: cover;
  background-repeat: no-repeat;
  flex-basis: 45%;
  height: 50vh;
}
.picture-circle {
  max-width: 50vh;
  border-radius: 50%;
  right: 0;
  margin-left: auto;
}
</style>