<template>
  <div class="app">
    <TopNavigationVue class="app__nav"/>
    <GalleryVue/>
    <FooterVue class="app__footer"/>
  </div>
</template>

<script>
import TopNavigationVue from '../components/nav/TopNavigation.vue'
import FooterVue from '../components/nav/Footer.vue'
import GalleryVue from '../components/gallery/Gallery.vue'

export default {
  name: 'IndexPage',
  components: { TopNavigationVue, GalleryVue, FooterVue },
}
</script>

<style scoped>
 .app {
  height: 100vh;
  min-height: 100vh;
  background-color: #C8D9EE;
 }

 .app__nav {
  height: 100%;
  position: sticky;
  top: 0;
 }

 .app__footer {
  position:fixed;
  bottom:0;
  width: 100%;
 }

</style>
