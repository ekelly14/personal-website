<template>
  <div class="page-container" >
    <TitleBar />
    <div class="px-5" style="padding-top: 64px;">
      <div class="p-5 my-5" style="background-color: blue;">Full Page Header Here</div>
      <div class="flex flex-row">
        <div class="p-5" style="background-color: white; flex-basis: 66%;">
          <h1>Body Title</h1>
          <span>Lots and lots of text</span>
        </div>
        <div style="background-color: black; flex-basis: 33%;">
          Image or somthing idk
        </div>
      </div>
    </div>
  </div>
</template>

<script>
const vueScrollRequire = process.client ? require('vue2-smooth-scroll') : null
const vueSmoothScroll = vueScrollRequire ? vueScrollRequire.VueSmoothScroll : null

import Logo from '~/components/Logo.vue'
import TitleBar from '~/components/header/TitleBar.vue'
import VueTyperWrapper from '~/components/general/VueTyperWrapper.vue'
import TextBlock from '~/components/general/TextBlock.vue'
import BodyText from '~/components/blocks/BodyText.vue'
export default {
  components: {
    Logo,
    TitleBar,
    VueTyperWrapper,
    TextBlock,
    BodyText,
    vueSmoothScroll
  }
}
</script>

<style>
.home {
  width: 100%;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
  background-color: rgba(41, 41, 41, .95);
}
.page-container {
  height: 100vh;
  background-color: burlywood;
}
.header-image {
  width: 100%;
  background-image: url('~assets/images/header.jpg');
}
.title {
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  /*color: #35495e;*/
  letter-spacing: 1px;
}
.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}
.links {
  padding-top: 15px;
}
.shifted-anchor {
  top: -75px;
}
</style>