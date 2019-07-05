<template>
  <section>
    <NavBar/>
    <div class="container test w-full">
      <div>
        <logo/>
        <h1 class="title">personal-website</h1>
        <h2 class="subtitle">A personal Website</h2>
        <div class="links">
          <a href="https://nuxtjs.org/" target="_blank" class="button--green">Documentation</a>
          <a href="https://github.com/nuxt/nuxt.js" target="_blank" class="button--grey">GitHub</a>
        </div>
        <p>
          Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Maecenas sed enim ut sem viverra aliquet. Facilisi nullam vehicula ipsum a arcu cursus vitae congue. Ornare arcu odio ut sem nulla pharetra diam. Faucibus pulvinar elementum integer enim neque. Blandit massa enim nec dui. Nulla aliquet porttitor lacus luctus accumsan tortor. Mi tempus imperdiet nulla malesuada pellentesque elit. Et leo duis ut diam quam nulla. Velit euismod in pellentesque massa placerat duis ultricies lacus sed. Vel pretium lectus quam id leo in vitae turpis massa. Eu consequat ac felis donec et odio pellentesque diam. Posuere urna nec tincidunt praesent semper feugiat nibh sed. Est pellentesque elit ullamcorper dignissim cras tincidunt lobortis feugiat. Convallis tellus id interdum velit. Nisi quis eleifend quam adipiscing vitae proin sagittis. Eu facilisis sed odio morbi quis commodo odio. Sed viverra ipsum nunc aliquet bibendum enim facilisis. Id velit ut tortor pretium viverra suspendisse potenti nullam.
          Et molestie ac feugiat sed lectus vestibulum mattis ullamcorper. Pharetra convallis posuere morbi leo urna. Nulla at volutpat diam ut. Turpis egestas maecenas pharetra convallis posuere. Interdum velit laoreet id donec ultrices. Netus et malesuada fames ac turpis egestas. Cras fermentum odio eu feugiat. Velit aliquet sagittis id consectetur purus ut faucibus. Duis at tellus at urna condimentum mattis pellentesque. Sit amet venenatis urna cursus eget. Dictum non consectetur a erat nam at lectus.
          Id aliquet lectus proin nibh nisl condimentum id. Amet consectetur adipiscing elit ut aliquam. Posuere ac ut consequat semper viverra nam libero justo laoreet. Non diam phasellus vestibulum lorem sed risus ultricies. Consectetur purus ut faucibus pulvinar elementum integer enim. Pretium viverra suspendisse potenti nullam. Ac odio tempor orci dapibus. Nisl purus in mollis nunc sed id semper risus. Diam quis enim lobortis scelerisque. Velit laoreet id donec ultrices tincidunt arcu non sodales. Consectetur a erat nam at lectus urna. Lectus quam id leo in. Sagittis vitae et leo duis ut.
        </p>
      </div>
    </div>
  </section>
</template>

<script>
import Logo from '~/components/Logo.vue'
import NavBar from '~/components/NavBar.vue'
import background from '~/components/background.vue'

export default {
  components: {
    Logo,
    NavBar,
    background
  },
  created() {
    try {
      // Internet Explorer 6-11
      var isIE = /*@cc_on!@*/ false || !!document.documentMode

      // Edge 20+
      var isEdge = !isIE && !!window.StyleMedia

      if (isEdge || isIE) {
        window.alert(
          //Alert the user that their browser is not supported
          'Your brower is not actively supported by this website.\nWhile the features might work, please be aware that any issues you may encounter might be resolved by utilizing a different browser.'
        )
      }
    } catch (e) {
      console.log('Something must be wrong. ', e)
    }
  }
}
</script>

<style scoped>
/* Sample `apply` at-rules with Tailwind CSS
.container {
  @apply min-h-screen flex justify-center items-center text-center mx-auto;
}
*/
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
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
.test {
  background: linear-gradient(
    45deg,
    rgba(0, 79, 161, 0) 0%,
    rgba(0, 79, 161, 0.5) 45%,
    rgba(0, 79, 161, 0.75) 80%,
    rgba(0, 79, 161, 1) 100%
  );
  height: 200px;
  z-index: -1;
  /* position: absolute; */
  top: 0px;
}
</style>
