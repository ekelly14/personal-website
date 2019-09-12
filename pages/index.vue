<template>
  <div class="w-full" >
    <TitleBar />
    <div class="header-image">
      <div class="home w-full">
        <div class="w-full px-4">
          <!--<logo />-->
          <h1 class="title text-blue-light">Hi! I'm Elijah.</h1>
          <div class="text-5xl md:text-6xl ">I Can Write Your </div>
          <VueTyperWrapper class="text-5xl md:text-6xl" :text-list="['C++', 'Python', 'JavaScript', 'Vue']" :shuffle="true"></VueTyperWrapper>
          <a href="#about" v-smooth-scroll>
            <img src="~assets/images/angle.png" class="h-16 w-16 mx-auto"/>
          </a>
        </div>
      </div>
    </div>
    <BodyText id="about" style="padding-top: 100px;" />
    <div class="mb-10"/>
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